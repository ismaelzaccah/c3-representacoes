# Riscos e roteiro de validação técnica

Status PROPOSTO • ARQ-C3-0.1 • 10/11/2026.

Base ESF-C3-0.1 revisão 1, DP-01–06 e [dimensionamento preliminar](backlog-estimativas-v0.1.md). Probabilidade e impacto são avaliações qualitativas propostas. Dono técnico Ismael. Caio responde pela decisão de negócio e materiais da C3, com Gabriella auxiliando na coleta conforme interlocução de Ismael.

## Registro de riscos

| ID | Risco / probabilidade / impacto | Sinal e efeito | Tratamento / responsável |
|---|---|---|---|
| R01 | Capacidade insuficiente para 30 dias / alta / alto | Faixa inicial de 144–388 h supera 80 h de referência mensal | Ismael revisa estimativa e executa provas iniciais. Apresentar decisão bilateral de viabilização antes de firmar compromisso técnico detalhado |
| R02 | Compras faturadas sem layout / alta / alto | Duplicação de documentos, mistura de itens/cabeçalhos, ajustes ou ausência de chaves | C3 fornece amostra. Ismael homologa granularidade, atualização e conciliação antes de finalizar adaptador |
| R03 | Fontes futuras indeterminadas / alta / alto | Cada fornecedor pode exigir XLSX, PDF ou procedimento em site | C3 prioriza e fornece material. Ismael estima por fonte e formaliza conjunto contratado |
| R04 | Autenticação/permissões Upcar divergentes / média / alto | Texto do fornecedor e OpenAPI descrevem credenciais de forma diferente | Ismael/João Vitor homologam fluxo e acesso apenas aos veículos necessários, por meio protegido |
| R05 | Posição antiga, sem fuso ou com identificação incorreta / média / alto | Evento usa veículo errado ou calcula idade incorretamente | Testar veículo/horário conhecido, limite 300 s, posições nulas/inválidas e falhas. Aplicar exceção justificada e conferência |
| R06 | Arredondamento/PDF ainda sem exemplo preenchido / média / médio | Divergência comercial em preço, total de linha ou soma geral | Caio valida exemplos e PT-03. Ismael compara PDF com referência preenchida |
| R07 | Infraestrutura, custos e domínio pendentes / alta / alto | Plano insuficiente para processamento, backup ou memória | Ismael dimensiona e cota. C3 confirma titularidade e aprova custos antes de contratar |
| R08 | Stack documental sem prova conjunta / média / alto | Incompatibilidade de versão, runtime, driver ou autenticação | Congelar e testar conjunto exato, licenças e advisories. Evitar assumir que documentação equivale a build validado |
| R09 | Retentativa, concorrência ou alteração obsoleta / média / alto | Visita dupla, veículo compartilhado indevidamente ou autorização antiga | Restrições no banco, idempotência, revisão e teste simultâneo dos fluxos críticos |
| R10 | Arquivos privados ou backup inconsistente / média / alto | Exposição de evidência ou restauração incompleta | Testar download negado, estados de preparação, manifesto e restauração conjunta. Definir retenção com custo |
| R11 | Disponibilidade de homologação / média / médio | Retorno tardio impede corrigir não conformidade no ciclo esperado | Caio e Ismael organizam roteiro e agenda. Registrar apresentação e manifestações ligadas aos critérios |
| R12 | Retenção e responsabilidades por dados pendentes / média / alto | Posições, evidências e históricos sem política definida | C3/Ismael organizam inventário. Revisão jurídica e política de retenção antes da produção |

## Provas propostas

As provas são roteiro de execução futura. Resultados estão PENDENTES. A estimativa contempla o trabalho de prova nos respectivos pacotes e a reestimativa posterior. Provas autenticadas usam apenas permissões necessárias e credenciais protegidas. Não reproduzir dados pessoais ou segredos nos relatórios.

| ID | Prova / entrada | Evidência de aprovação | Dependência / pacote |
|---|---|---|---|
| V01 | Congelar runtime, framework, banco, autenticação e dependências | Versões exatas, licenças, advisories, build/migração executados e matriz de compatibilidade | Aprovação técnica de execução, B01/B02 |
| V02 | Upcar autenticação e veículo conhecido | Fluxo documentado, consulta autorizada e identificação coerente. Registrar diferença entre horário dispositivo/consulta e fuso confirmado | DP-03, Ismael/João Vitor, B05 |
| V03 | Wega e cálculo/PDF | Mapeamento A/C/E/G, 3.839 linhas reconhecidas, mínimos 6/quantidade 7 aceita, casos de arredondamento e saída conferida | DP-05 para fechar resultado, B07 |
| V04 | Compras faturadas | Granularidade/chave, atualização, ajustes e totais de amostra reconciliados com C3 | DP-01, B09 |
| V05 | Autorização e concorrência | Promotor A não lê visita B, Escritório não cria conta, veículo exclusivo e visita aberta únicos sob acesso simultâneo | ESF/permissões revisadas, B02/B03/B04/B11 |
| V06 | Arquivos e operação | Upload inválido recusado, documento privado protegido, PDF/XLSX dentro dos limites e restauração com arquivos íntegros | DP-04, B07/B10/B11 |
| V07 | Dispositivos e carga | Resultados dos fluxos nos aparelhos acordados e métricas do cenário RNF-05 | Aparelhos/ambiente aprovados, B11/B12 |

Cada registro de prova deve conter versão do pacote, ambiente, entrada anonimizada, procedimento, resultado esperado/observado, evidência, autor/data e pendências. Falha atualiza o risco e a estimativa. A decisão de aceitar limitação precisa indicar escopo, custo/prazo e aprovadores pertinentes.

## Decisões que podem ser revisadas agora

Ismael pode revisar direção do monólito, modelo lógico, papéis, regra de exclusividade e estimativas sem aguardar a coleta. A revisão dos detalhes PT-01–08 e dos RNFs reduz incerteza. Dados da C3 fecharão os contratos de importação, conjunto de fornecedores e dimensionamento. Custos e versões exatas ficam sujeitos às suas respectivas evidências.
