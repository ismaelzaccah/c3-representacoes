# Levantamento preliminar da API do rastreador

Status PROPOSTO • Versão 0.3 • 10/11/2026 • Fontes F19–F23 • Vinculado a D06 e MC-01.

## Diretriz recebida

O responsável aprovou D06 com ressalva de origem. O promotor utiliza veículo da empresa e a localização será fornecida pela API do rastreador desse veículo. A consulta será associada aos eventos de check-in e check-out. Escritório e Master consultarão o registro para conferência. A exceção aprovada de localização indisponível permite salvar o evento com justificativa e indicação de conferência, agora aplicada à fonte do rastreador.

## Evidências consultadas

Em 09/11/2026 foram consultados dois recursos públicos por GET. A página de documentação aponta o arquivo OpenAPI utilizado pelo Swagger. A especificação declara OpenAPI 3.0.3 e versão de API 1.0.0. [Página oficial](https://upcar.rastrosystem.com.br/api/v3/docs) e [OpenAPI](https://upcar.rastrosystem.com.br/api/v3/openapi.yaml).

A cópia da especificação está em `fontes-cliente/upcar-openapi-v3-2026-11-09.yaml`, com 138.032 bytes e SHA-256 `07E31A3CC263D09FE1D4F25706B52DEDE46A762839A8C26594BAF8F4157EB74C`. A pasta permanece ignorada no Git. Foram lidas as descrições públicas de autenticação, veículos e posição. A homologação autenticada com dados da C3 permanece pendente.

| Recurso documentado | Observação para a descoberta |
|---|---|
| Base `/api/v3` | Host é o subdomínio da empresa, conforme a especificação |
| `POST /auth/token/` | Emite access/refresh token com usuário e senha, ou renova access token via refresh. É descrição de endpoint, sem execução nesta etapa |
| JWT Bearer | Especificação define envio do access token no cabeçalho de autorização |
| `GET /veiculos/` | Lista veículos com última posição, sujeita às permissões do usuário e vínculos de acesso |
| `GET /veiculos/{id}/` | Retorna dados do veículo e última posição conhecida |
| `Posicao.latitude` e `longitude` | Coordenadas do veículo |
| `Posicao.data` | Horário informado pelo aparelho. Pode estar ausente |
| `Posicao.valida` | Indica confiabilidade do GPS. Coordenada com valor falso requer tratamento como posição inválida |
| `posicao` nula | Pode ocorrer com ausência de equipamento ou coordenada ainda sem reporte |

O schema de posição consultado oferece validade do GPS. Uma precisão numérica em metros ainda precisa ser confirmada com o fornecedor, caso necessária. A presença do recurso na documentação fundamenta análise, enquanto disponibilidade real, latência, frequência de atualização, fuso e permissões da conta C3 precisam de validação.

## Autenticação e configuração na etapa técnica

F22 informa que João Vitor já entregou login, senha e token ao responsável para implementação futura. A disponibilidade desses dados está esclarecida. A implementação deverá usar configuração protegida do servidor, por variáveis de ambiente ou gerenciador de segredos conforme a infraestrutura aprovada, com valores acessíveis ao serviço responsável pela integração.

F20 descreve login, senha e token de API. O schema TokenRequest de F21 apresenta username/password e JWT/refresh. A forma de uso dos dados fornecidos será validada na homologação autenticada para a conta C3. Essa verificação fica registrada para a etapa técnica, com regras operacionais de veículo fixo e posição de até cinco minutos definidas em F23.

O perfil Master da plataforma C3 e o perfil Administrador do rastreador pertencem a sistemas distintos. A conta da integração precisa das permissões necessárias para consultar os veículos da C3. Os direitos do usuário no provedor são uma dependência própria.

## Tratamento proposto dos dados

Registrar o vínculo vigente entre visita, promotor, veículo e identificador externo do veículo na API. Para cada evento, preservar horário da visita, horário da consulta e horário informado pelo rastreador. Guardar coordenadas, origem, identificador e condição de validade quando disponíveis. F23 define veículo fixo por promotor. O vínculo do cadastro deve identificar esse veículo. Os registros de visita preservam o veículo associado ao evento para rastreabilidade.

Uma resposta com sucesso pode conter posição antiga, inválida ou nula. O comportamento aprovado permite justificativa e conferência nas falhas de localização. F23 aprova idade máxima de cinco minutos no check-in/out. Posição acima desse limite permite registro com justificativa e conferência. Homologar o caso de exatamente cinco minutos como aceito e o caso superior como exceção. Consultas posteriores para regularização e detalhes de comparação temporal serão especificados nas etapas autorizadas.

## MC-01 — alteração do recorte da integração

| Campo | Registro |
|---|---|
| Baseline afetada | F01 RF-06 excluía API de rastreadores. D06 vinha sendo proposta com origem no aparelho do promotor |
| Alteração expressa | F19 exige posição proveniente do rastreador do veículo da empresa nos eventos de visita |
| Estado | Origem funcional APROVADA pelo responsável, com detalhamento técnico e impacto PENDENTES |
| Impacto a avaliar | Autenticação, permissões, vínculo promotor/veículo, atualidade da posição, falhas do provedor, armazenamento, testes, operação e custos |
| Estimativa | Ainda sem estimativa validada. Prazo comercial de 30 dias continua com viabilidade pendente |
| Limite funcional registrado | Consulta de posição do veículo para os eventos de visita. GPS contínuo, trajetos, comandos remotos e outras capacidades são referências da documentação e permanecem sujeitos às respectivas decisões de escopo |
| Próximo encaminhamento | Regras operacionais definidas em F23, veículo fixo e até cinco minutos. Configurar credenciais disponíveis conforme F22 e homologar autenticação, permissões e dados temporais na etapa técnica. Consolidar impacto e anexo técnico |

Este levantamento faz parte da descoberta. As diretrizes de implementação serão definidas nas etapas autorizadas de especificação e arquitetura.

