# C3 Representação e Marketing — diagnóstico preliminar

Versão 0.1 • 06/11/2026 • Status: PROPOSTO, para revisão do responsável.

Este relatório atende somente à primeira tarefa do Prompt Mestre v1.2. Não é especificação contratual, proposta comercial final ou autorização de desenvolvimento. As decisões expressamente aprovadas no prompt são preservadas; o detalhamento abaixo ainda depende de validação.

## 1. Conclusão executiva

O material permite iniciar a especificação de um MVP híbrido para até dez usuários, centralizando registros, documentos, acompanhamento e aprovações. As automações atuais podem continuar operando externamente.

**A viabilidade de entregar todo o escopo em 30 dias corridos não está comprovada.** O principal ponto de incerteza é pedidos e propostas: não foram encontrados arquivos de fornecedores, layouts homologados, regras comerciais ou modelo aprovado de proposta. Visitas, permissões, arquivos e critérios de aceite também precisam de decisões antes de uma estimativa defensável.

As planilhas descrevem uma operação mais ampla do que o MVP delimitado no prompt. Suas funcionalidades adicionais devem permanecer fora do compromisso inicial até aprovação expressa. Não foi identificada uma especificação contratual aprovada no projeto.

## 2. Inspeção e inventário de fontes

Inspeção local em modo somente leitura dos originais: árvore de arquivos, estado do Git, conteúdo das células das duas planilhas e textos dos objetos de desenho presentes nos arquivos XLSX. Não houve renderização visual das planilhas; cores, posições de formas e conectores não foram usados para inferir regras. Não foram localizadas instruções AGENTS.md nos diretórios consultados.

| ID | Fonte | Situação e evidência | Autoridade e limites |
|---|---|---|---|
| F01 | Prompt Mestre v1.2, anexo `Pasted text.txt`, 06/11/2026 | Lido integralmente; contém contexto, limites, condições comerciais e primeira tarefa | Instrução atual do responsável. RFs são preliminares; não transformar detalhes pendentes em aprovação |
| F02 | `fontes-cliente/FLUXOGRAMA.xlsx` | 13.967 bytes; uma aba `Planilha1`; células e textos de desenho examinados | Fonte original de processos; tempos e indicação de API não foram validados operacionalmente |
| F03 | `fontes-cliente/APP CAIO COSTA PROMOTORES.xlsx` | 11.772 bytes; uma aba `Planilha1`; células e texto de desenho examinados | Requisitos preliminares, inclusive funções excluídas pelo prompt |
| F04 | Artifact C3 Visitas: `https://claude.ai/artifact/3F3rLsa6LrU9s6frGGUq8x` | Referenciado em F01; não acessado nesta etapa, em respeito à restrição de ações externas | Descrição fornecida pelo usuário, sem verificação independente nesta inspeção; não é contrato nem identidade visual obrigatória |
| F05 | `.gitignore` | Contém `fontes-cliente`; a pasta de originais está ignorada no Git | Ignorar no Git não constitui backup, controle de acesso ou proteção contra perda |
| F06 | Repositório local | Antes deste relatório, apenas `.gitignore` e as duas planilhas foram encontrados fora dos metadados Git; árvore de trabalho sem alterações reportadas | Sem aplicação, testes, dependências ou documentação funcional local identificados |

Hashes SHA-256 para identificação dos originais:

```text
FLUXOGRAMA.xlsx
326531634FFE9974EB8924EF73FE1EAAB1A6AFC2A2B451AAADB06562E4136531

APP CAIO COSTA PROMOTORES.xlsx
F674ED999BC7B6E21A18C07E4D018C252A80955CB04F00C3E32551AA2D6EBEFE
```

Não foram encontrados: modelos reais de importação/exportação, proposta comercial padrão, dicionário de campos, amostras de pedidos com alterações, matriz de acesso aprovada, contratos de infraestrutura, documentação de integrações ou comprovação de acessibilidade das APIs. Não é necessário obter credenciais de produção para iniciar a especificação; exemplos anonimizados são preferíveis.

## 3. Evidências, divergências e lacunas

| ID | Evidência localizada | Relação com F01 | Tratamento preliminar |
|---|---|---|---|
| C01 | F03, E3 e A39:A41: primeira visita entre 8h e 8h20, última após 17h30, notificações e limite de 500 m do endereço de casa | F01 §6/RF-03 não aprova essas regras e exclui notificações externas | Não aplicar horários nem raio por padrão. Registrar eventual demanda futura separadamente |
| C02 | F03, A44:A45: localização em tempo real e KM rodado | F01 exclui GPS contínuo e rastreamento de trajetos | FORA DO MVP. Geolocalização pontual permanece PENDENTE |
| C03 | F03, A5: promotor deve cadastrar cliente novo; A6:A13: endereço, contatos e CNPJ | F01 pede selecionar cliente e cadastros essenciais, sem aprovar permissão de criação pelo promotor | Decidir cadastro direto, solicitação de cadastro ou cadastro exclusivo pelo escritório |
| C04 | F03, A15:A17: trabalha com Hella/Wega/Starke; A20:A36: contato, motivos, observações e lembretes | F01 limita a visita a motivo e observações básicas; não inclui gestão completa de tarefas | Validar lista de motivos e associações com fornecedores. Questionário ampliado e lembretes não entram automaticamente |
| C05 | F02, E12:M15: campanhas com formulário, acompanhamento, fechamento, pagamento e datas do mês | F01 inclui solicitação, decisão, folder, vigência e consulta; exclui pagamentos automatizados e controle avançado de investimento | Definir fronteira do registro de campanha. Datas da planilha não viram prazos de sistema automaticamente |
| C06 | F02, F7:O10: pedido, cotação, retorno ao cliente, lançamento em grupo e PDF | F01 descreve versões, não aprovação, revisão e autorização interna obrigatórias | Prevalece F01 para a especificação proposta. Esclarecer significado de “liberado” e evidência das aprovações |
| C07 | F02, F20:J25: BI e API; Wega/Hella/Starke com API “TALVEZ”, Paraflu/NTN “NÃO” | Não há documentação técnica comprobatória | Não afirmar existência, ausência definitiva ou viabilidade de integração com base nessa tabela |
| C08 | F02, F28:I34 e F37:H53: investimentos, brindes, sell-out, despesas, bônus, metas, projeção e clientes em queda | Excede os sete módulos preliminares do MVP | Backlog futuro para avaliação, sem compromisso inicial |
| C09 | F03, A47:A54: endereço residencial do promotor | Não há finalidade aprovada para esse dado no MVP | Não incluir automaticamente. Avaliar necessidade e privacidade se a demanda for mantida |
| C10 | F02, O9, H29:I34 e G38: tempos operacionais e referências a Claude | Não são estimativas de engenharia, capacidade ou metas de desempenho do novo software | Usar somente como hipótese para diagnóstico do processo, após confirmar medição e frequência |

Não se trata de rejeitar os documentos originais: eles descrevem necessidades e processos cuja contratação inicial foi delimitada por F01. Divergências futuras devem manter fonte, decisão, responsável, data e impacto.

## 4. Estrutura de pastas sugerida

Somente `docs/diagnostico-preliminar-v0.1.md` foi criado nesta etapa. A estrutura abaixo é uma proposta para os próximos entregáveis, sem criar aplicação ou instalar ferramentas.

```text
fontes-cliente/                     # originais preservados; atualmente fora do Git
docs/
  diagnostico-preliminar-v0.1.md
  00-governanca/                    # inventário, decisões, pendências, mudanças e versões
  01-visao-produto/                 # grupo A
  02-requisitos/                    # grupo B: especificação única e versionada
  03-fluxos-permissoes/             # grupo C: Mermaid e matriz de acesso
  04-arquitetura/                   # grupo D: alternativas e decisões técnicas
  05-prototipos/                    # grupo E: protótipos vinculados a requisitos
  06-planejamento/                  # grupo F: backlog, estimativas, riscos e testes
  07-comercial/                     # grupo G: apresentação e condições
  08-contratual/                    # grupo H: minuta e anexos para revisão jurídica
```

A especificação do grupo B deverá ser a referência única. Os demais materiais apontarão para IDs e versão, sem criar cópias divergentes de requisitos. Preservar os originais e decidir separadamente seu armazenamento seguro e backup; não alterar o `.gitignore` nesta etapa.

## 5. Matriz preliminar de requisitos

Legenda: **APROVADO** identifica decisões expressas de F01; **PROPOSTO** identifica requisitos preliminares sujeitos a detalhamento e aceite; **PENDENTE** indica decisão sem definição suficiente; **FORA DO MVP** preserva exclusões. Prioridades P0/P1 abaixo são recomendações de sequência, não autorização para retirar itens do escopo: P0 = base ou controle crítico; P1 = operação prevista. Todos os itens MVP precisam ser considerados na estimativa integral.

Nesta etapa a matriz registra comportamento, ator, fonte e evidência inicial de aceite. Campos completos, validações, exceções e cenários serão desenvolvidos na próxima etapa, após aprovação do plano.

| ID | Requisito preliminar | Ator | Recorte / prioridade | Status | Evidência inicial de aceite | Fonte |
|---|---|---|---|---|---|---|
| DEC-01 | Adotar MVP híbrido, mantendo operações externas registradas manualmente | Todos | MVP / P0 | APROVADO | Fluxos distinguem ação humana externa de registro interno | F01 §5 |
| RF-01.01 | Autenticar usuário por login | Todos | MVP / P0 | PROPOSTO | Credenciais válidas permitem acesso; inválidas são recusadas | F01 RF-01 |
| RF-01.02 | Encerrar sessão no logout | Todos | MVP / P0 | PROPOSTO | Sessão encerrada deixa de autorizar operações protegidas | F01 RF-01 |
| RF-01.03 | Aplicar os três perfis fixos no servidor | Todos | MVP / P0 | PROPOSTO | Tentativa direta de operação sem permissão é recusada | F01 RF-01 |
| RF-01.04 | Ativar e inativar usuários | Administrador, a validar | MVP / P0 | PROPOSTO | Usuário inativo não consegue operar, conforme política de sessão a definir | F01 RF-01 |
| RF-02.01 | Cadastrar e consultar cliente/varejista | Administrador/Escritório, a validar | MVP / P0 | PROPOSTO | Cadastro persiste campos aprovados e pode ser selecionado em operação | F01 RF-02; F03 A5:A13 |
| RF-02.02 | Cadastrar usuários/promotores | Administrador, a validar | MVP / P0 | PROPOSTO | Usuário tem perfil e vínculo operacional definidos | F01 RF-02 |
| RF-02.03 | Cadastrar fornecedores | Administrador/Escritório, a validar | MVP / P0 | PROPOSTO | Fornecedor pode ser associado a campanha e pedido | F01 RF-02 |
| RF-02.04 | Manter associações operacionais aprovadas | A definir | MVP / P0 | PENDENTE | Relações cliente/promotor/fornecedor/veículo respeitam cardinalidade aprovada | F01 RF-02 |
| RF-03.01 | Selecionar cliente para visita | Promotor | MVP / P1 | PROPOSTO | Cliente selecionado fica vinculado ao registro | F01 RF-03; F03 A5 |
| RF-03.02 | Registrar check-in com data, horário e promotor | Promotor | MVP / P1 | PROPOSTO | Registro associa início, cliente e autor | F01 RF-03; F03 E2 |
| RF-03.03 | Registrar check-out da visita | Promotor | MVP / P1 | PROPOSTO | Encerramento vincula-se à visita correta e preserva o início | F01 RF-03; F03 A38 |
| RF-03.04 | Registrar motivo e observações básicas | Promotor | MVP / P1 | PROPOSTO | Dados informados podem ser consultados na visita | F01 RF-03; F03 A21:A34 |
| RF-03.05 | Consultar visitas anteriores | Promotor | MVP / P1 | PROPOSTO | Consulta respeita o alcance de acesso aprovado | F01 RF-03 |
| RF-03.06 | Acompanhar visitas administrativamente | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Visitas registradas aparecem com cliente, promotor e situação | F01 RF-03 |
| RF-03.07 | Definir visita aberta, edição, horários, localização pontual e falhas de conexão | Responsável pelo projeto | MVP / P0 | PENDENTE | Regras e cenários de falha aprovados antes da implementação | F01 RF-03 |
| RF-04.01 | Registrar solicitação de campanha com cliente, fornecedor e responsável | Administrador/Promotor | MVP / P1 | PROPOSTO | Solicitação pode ser consultada com seus vínculos | F01 RF-04 |
| RF-04.02 | Registrar aprovação ou rejeição externa da campanha | Operador interno a definir | MVP / P1 | PROPOSTO | Decisão, autor do registro e mudança de estado ficam identificáveis | F01 RF-04 |
| RF-04.03 | Anexar folder à campanha | Operador interno a definir | MVP / P1 | PROPOSTO | Arquivo permitido pode ser recuperado por usuário autorizado | F01 RF-04 |
| RF-04.04 | Definir clientes-alvo e vigência da campanha | Operador interno a definir | MVP / P1 | PROPOSTO | Relações e período aprovado são persistidos | F01 RF-04 |
| RF-04.05 | Exibir campanhas ativas e folders do cliente selecionado | Promotor | MVP / P1 | PROPOSTO | Campanhas de outro cliente ou fora da regra de atividade não aparecem como ativas | F01 RF-03/04 |
| RF-04.06 | Consultar histórico e estados das campanhas | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Consulta apresenta solicitação e decisões registradas | F01 RF-04 |
| RF-05.01 | Registrar manualmente solicitação com cliente e fornecedor | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Solicitação identifica origem informada e vínculos aprovados | F01 RF-05 |
| RF-05.02 | Anexar arquivos originais da solicitação | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Arquivos ficam associados à solicitação com acesso controlado | F01 RF-05 |
| RF-05.03 | Importar planilha de layout homologado | Administrador/Escritório, a validar | MVP / P0 | PROPOSTO | Arquivo válido é importado; erro de layout gera mensagem e tratamento definido | F01 RF-05; layouts ausentes |
| RF-05.04 | Gerar proposta em modelo aprovado | Administrador/Escritório, a validar | MVP / P0 | PROPOSTO | Arquivo gerado confere com exemplo de referência e regras aprovadas | F01 RF-05; modelo ausente |
| RF-05.05 | Registrar nova versão e solicitação de alteração | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Versões anteriores permanecem consultáveis e identificadas | F01 RF-05 |
| RF-05.06 | Registrar aprovação ou não aprovação do solicitante | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Resposta referencia a versão pertinente e permite encaminhamento humano | F01 RF-05 |
| RF-05.07 | Registrar revisão humana interna obrigatória | Revisor a definir | MVP / P0 | PROPOSTO | Encaminhamento interno exige revisão registrada, inclusive na não aprovação | F01 RF-05 |
| RF-05.08 | Registrar autorização interna para prosseguir | Autorizador a definir | MVP / P0 | PROPOSTO | Fluxo interno não permite marcar envio sem autorização aplicável à versão; não controla o portal externo | F01 RF-05 |
| RF-05.09 | Registrar manualmente envio ao fornecedor | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Envio identifica versão autorizada e responsável pelo registro | F01 RF-05 |
| RF-05.10 | Registrar resultado do pedido externo | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Resultado fica associado ao pedido e seu histórico | F01 RF-05 |
| RF-05.11 | Preservar histórico de alterações e responsáveis | Sistema | MVP / P0 | PROPOSTO | Mudanças relevantes podem ser atribuídas a usuário e momento | F01 RF-05 |
| RF-05.12 | Definir eventual arquivo específico para fornecedor | Responsável pelo projeto | Condicional / P0 | PENDENTE | Inclusão exige layout, validações e aceite formal no anexo | F01 RF-05 |
| RF-06.01 | Cadastrar veículo | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Veículo cadastrado pode receber abastecimento | F01 RF-02/06 |
| RF-06.02 | Registrar abastecimento com veículo, data, hodômetro, litros e total | Perfil a definir | MVP / P1 | PROPOSTO | Registro válido persiste os campos e vínculo; regras numéricas serão aprovadas | F01 RF-06; F02 F30 |
| RF-06.03 | Consultar histórico e totais básicos de abastecimento | Perfil a definir | MVP / P1 | PROPOSTO | Totais conferem com registros do recorte aprovado | F01 RF-06 |
| RF-07.01 | Consultar pedidos e aprovações no painel | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Consulta reflete estados e decisões registradas | F01 RF-07 |
| RF-07.02 | Filtrar consultas operacionais | Administrador/Escritório, a validar | MVP / P1 | PROPOSTO | Filtros aprovados retornam somente registros correspondentes | F01 RF-07 |
| RF-07.03 | Definir indicadores simples | Responsável pelo projeto | MVP / P1 | PENDENTE | Fórmula, período, fonte e visibilidade aprovados para cada indicador | F01 RF-07 |
| RF-07.04 | Definir exportações homologadas | Responsável pelo projeto | MVP / P1 | PENDENTE | Cada saída possui formato, campos e exemplo de aceite | F01 RF-07 |

Campos explicitamente disponíveis: cliente em F03 A5:A13; motivo e observações em F03 A21:A34; abastecimento em F01 RF-06; campanha em F01 RF-04. Sua presença na fonte não resolve obrigatoriedade, unicidade, edição, exclusão ou alcance de acesso.

### Requisitos não funcionais para detalhamento

Os critérios abaixo são propostas de verificação. Não representam SLA ou metas de infraestrutura aprovadas.

| ID | Tema | Verificação proposta | Status / fonte |
|---|---|---|---|
| RNF-01 | Autenticação e autorização | Cobrir acessos permitidos e negados de cada perfil no servidor; definir expiração, recuperação de acesso e inativação | PROPOSTO / F01 §7 |
| RNF-02 | Privacidade | Inventariar finalidade, acesso, retenção e destino de cada categoria de dado, inclusive eventual localização; questões legais para revisão específica | PROPOSTO / F01 §7 |
| RNF-03 | Integridade e rastreabilidade | Verificar vínculos, transições e concorrência; registrar autor e momento de aprovações e alterações relevantes | PROPOSTO / F01 §7 |
| RNF-04 | Arquivos | Definir tipos/tamanhos permitidos e armazenamento privado; testar rejeição e acesso por usuário sem permissão | PROPOSTO / F01 §7 |
| RNF-05 | Desempenho e escala inicial | Definir operações, volume de dados/arquivos e carga concorrente; medir latência em ambiente acordado para público inicial de até dez usuários | PENDENTE / F01 §§4/7 |
| RNF-06 | Responsividade e compatibilidade | Aprovar matriz de aparelhos, navegadores, versões e larguras; testar fluxos de promotor em Android e administrativos nas plataformas indicadas | PROPOSTO / F01 §§4/7 |
| RNF-07 | Acessibilidade | Aprovar critérios e verificar navegação por teclado, foco, rótulos, mensagens e contraste nos fluxos críticos | PROPOSTO / F01 §7 |
| RNF-08 | Backup e recuperação | Definir retenção, responsabilidade e objetivos após análise de custo; testar restauração de banco e arquivos em conjunto | PENDENTE / F01 §7 |
| RNF-09 | Disponibilidade e monitoramento | Definir janela de serviço, alertas, responsáveis e custos antes de assumir disponibilidade garantida | PENDENTE / F01 §7 |
| RNF-10 | Manutenibilidade e testabilidade | Vincular critérios de aceite a testes, documentar configuração e demonstrar instalação reproduzível em ambiente de teste | PROPOSTO / F01 §7 |
| RNF-11 | Falhas e repetição de operações | Especificar comportamento em queda de conexão e repetição de check-in/importação/aprovação para evitar registros ambíguos ou duplicados | PROPOSTO / F01 §7 |

### Exclusões a preservar

**FORA DO MVP segundo F01:** catálogo permanente de produtos/preços/estoque; editor complexo de permissões; metas, ranking, GPS contínuo, áudio, IA e tarefas completas; captura de WhatsApp/e-mail; download ou consulta automática a portais; importação genérica; geração para todos os layouts; envio automático de pedidos; solicitação/leitura automática de campanhas; pagamentos automatizados e controle avançado de investimento/premiação; integração com rastreadores, trajetos, consumo por trajeto e manutenção de frota; BI completo, projeções e relatórios não especificados.

As demais rotinas amplas de F02, como brindes, bônus e despesas gerais, são referências para evolução, sem inclusão automática no MVP. Localização pontual, cadastro de cliente pelo promotor e arquivo específico de fornecedor são pendências, não exclusões ou inclusões já decididas.

## 6. Decisões pendentes e materiais necessários

| ID | Decisão ou material | Quem deve esclarecer | Impacto |
|---|---|---|---|
| D01 | Quantos layouts de entrada e quais fornecedores entram no MVP? Obter exemplos anonimizados válidos, inválidos e com variações | C3 / escritório | Bloqueia dimensionamento de importação |
| D02 | Qual o modelo de proposta, formato de saída, fórmulas, arredondamentos, impostos, descontos e regras de itens? | C3 / comercial | Bloqueia geração e aceite de propostas |
| D03 | Quem revisa e autoriza pedidos? Pode ser a mesma pessoa? Como comprovar resposta do cliente? Alteração de versão invalida aprovação? | C3 / administração | Determina estados, permissões e trilha de auditoria |
| D04 | Promotor vê somente seus clientes/visitas? Pode cadastrar cliente, solicitar campanha e registrar abastecimento? Escritório pode autorizar? | C3 / administração | Define matriz de acesso e alcance dos dados |
| D05 | Visitas simultâneas são permitidas? Como encerrar visita esquecida, corrigir dados e lidar com falta de internet? | C3 / operação | Define fluxo mobile e esforço; offline completo não está aprovado |
| D06 | Haverá localização pontual? Em qual evento, com qual finalidade e qual tratamento para recusa/erro de precisão? | C3 / operação e responsável por privacidade | Afeta experiência, dados e homologação; não aprova raio ou horário |
| D07 | Quais campos são obrigatórios e únicos? Um cliente é estabelecimento, CNPJ ou grupo? Como tratar duplicidades e inativação? | C3 / escritório | Evita inconsistências nos vínculos |
| D08 | Campanha pode ter vários clientes e folders? Quem registra decisão externa? O que define ativa, cancelada ou encerrada? | C3 / comercial | Define modelo e exibição durante visita |
| D09 | Quem registra abastecimento? Pode corrigir retroativamente? Como validar hodômetro, veículo compartilhado, valores e litros? | C3 / administração | Define validações e histórico |
| D10 | Quais filtros, indicadores e exportações são necessários para aceite inicial? | C3 / administração | Limita relatórios e esforço de homologação |
| D11 | Quais volumes de dados/arquivos, limites, retenção, hospedagem, orçamento recorrente e responsáveis por backup/operação? | Responsável técnico + C3 | Necessário para RNFs e custo total |
| D12 | Qual a equipe, dedicação efetiva e capacidade da implantação? As 80 h mensais são de evolução distinta? | Desenvolvedor + responsável comercial | Impede confundir franquia de evolução com capacidade para entregar implantação |
| D13 | Qual o marco de início e o significado de entrega em 30 dias: disponibilização para homologar ou aceite concluído? | Ambas as partes | Compatibilizar 30 dias corridos com cinco dias úteis de homologação |
| D14 | Como atribuir competências à primeira mensalidade e às seguintes sem sobreposição? Como identificar serviço de evolução distinto da implantação? | Ambas as partes + revisão jurídica | Evita ambiguidade de cobrança, especialmente com atraso do MVP |
| D15 | Duração da garantia, limites do suporte, horas não utilizadas/adicionais, rescisão e responsabilidades de infraestrutura/IP | Ambas as partes + revisão jurídica | Necessário antes da minuta final e assinatura |
| D16 | Quem aprova requisitos e quem homologa? Qual disponibilidade para respostas e testes? | Responsável pelo projeto / C3 | Define responsáveis e dependências de prazo |

## 7. Plano proposto para os próximos entregáveis

O avanço depende da aprovação do responsável. A sequência abaixo organiza os grupos A–H; não é cronograma contratual já aceito.

| Etapa | Entregáveis | Dependências | Condição de conclusão |
|---|---|---|---|
| 1. Consolidar descoberta | A: visão e limites; inventário versionado; registro de decisões; respostas a D01–D10 e D16 | Aprovação deste plano e exemplos operacionais | Responsável confirma processos, atores e limites; lacunas remanescentes ficam explícitas |
| 2. Especificar comportamento | B: RFs/RNFs atômicos com campos, validações, regras, exceções e aceite; C: matriz de acesso e fluxos Mermaid | Etapa 1; layouts e modelo de proposta | Revisão dos fluxos normal, alteração, rejeição, autorização, erro e acesso negado |
| 3. Avaliar solução e capacidade | D: monólito modular, dados, arquivos, autenticação, hospedagem, custos e decisões; F: backlog estimado, dependências, riscos e plano de testes | D11–D13; comportamento suficientemente definido | Parecer explícito sobre os 30 dias, com capacidade, estimativas e opções para decisão bilateral |
| 4. Validar experiência | E: protótipos mobile-first de visita/campanha e telas administrativas de pedidos, abastecimentos e cadastros | Requisitos rastreáveis; permissões definidas | Validação dos fluxos pelos usuários; diferenças geram mudança documentada |
| 5. Preparar contratação | G: apresentação comercial; H: minuta e anexos vinculados à mesma versão de requisitos | Escopo, viabilidade, protótipos e condições pendentes resolvidos | Aprovação do responsável e revisão jurídica da minuta antes de assinatura |

A avaliação técnica deverá acontecer nos primeiros cinco dias úteis do marco contratual, como exige F01. Recomenda-se antecipar a coleta de documentos e as decisões críticas durante a pré-venda. Se a avaliação indicar incompatibilidade, apresentar ajustes de escopo, preço ou prazo para aprovação bilateral, sem redução unilateral.

A stack listada em F01 é candidata. Versões, compatibilidade e licenças não foram verificadas nesta etapa, e não há stack aprovada. Essa verificação faz parte da etapa 3, antes de qualquer decisão técnica definitiva.

Rastreabilidade futura: `fonte → requisito/versão → fluxo/tela → item de backlog → critério/teste → evidência de homologação`. Registrar decisões e mudanças com responsável, data e impacto; não renumerar IDs já publicados sem registrar a substituição.

## 8. Riscos preliminares de prazo e escopo

Classificações qualitativas para priorizar investigação, sem probabilidade quantitativa ou estimativa de esforço validada.

| Risco | Exposição preliminar | Consequência | Ação proposta |
|---|---|---|---|
| Layouts e regras comerciais desconhecidos | Alta | Importação e geração de propostas podem exigir mais esforço do que o previsto | Homologar conjunto finito de layouts e amostras antes da estimativa |
| Sete módulos mais controles transversais em 30 dias corridos | Alta | Segurança, testes e homologação disputam a mesma janela | Estimar por fluxo, incluir trabalho transversal e comparar com capacidade real |
| Capacidade de implantação não informada | Alta | Não é possível converter escopo em calendário confiável | Definir equipe, dedicação e disponibilidade; manter evolução de 80 h separadamente identificada |
| Expansão por planilhas e protótipo | Alta | Incorporar GPS, metas, bônus ou automações altera materialmente o MVP | Validar exclusões e usar solicitação de mudança com impacto e aprovação |
| Revisão interna e permissões indefinidas | Alta | Pedido pode ser registrado como encaminhado sem evidência adequada | Aprovar estados, atores e regras de autorização por versão |
| Decisão tardia sobre uso sem conexão | Alta | Offline e sincronização podem mudar arquitetura e estimativa | Definir comportamento mínimo e cenários antes dos protótipos finais |
| Prazo de entrega versus prazo de homologação | Alta | Aceite e segunda parcela podem cair fora da janela comercial imaginada | Definir marco, data de disponibilização e cinco dias úteis de validação |
| Ausência de critérios mensuráveis de qualidade | Alta | Dificulta provar entrega e dimensionar testes | Aprovar RNFs, matriz de dispositivos e critérios de aceite |
| Mudanças externas de fornecedores | Média/alta | Layouts podem mudar e inviabilizar processamento homologado | Versionar layouts; rejeitar formatos incompatíveis de forma controlada |
| Arquivos, restauração e custos operacionais indefinidos | Média/alta | Perda de dados, acesso indevido ou custo omitido | Dimensionar armazenamento, acesso, backup e restauração antes de comprometer níveis de serviço |
| Cobrança e competências mensais ambíguas | Alta | Sobreposição de períodos ou serviços não distinguíveis | Definir competências e registrar serviços efetivos; revisão jurídica |

### Método para avaliar os 30 dias

1. Definir marco contratual, equipe e horas disponíveis de implantação; não assumir que R$ 24.000 equivalem a uma quantidade de horas contratada nem que a franquia de 80 h pertence à implantação.
2. Decompor requisitos em atividades com faixas de esforço, premissas e dependências: análise, interface, dados, segurança, arquivos, importação, geração, testes, documentação, preparação de ambiente e homologação.
3. Identificar caminho crítico e capacidade efetiva, incluindo reuniões, correções e esperas de terceiros. Tempos operacionais de F02 não medem desenvolvimento.
4. Montar calendário a partir da data real de início. Uma janela de 30 dias contém de 20 a 22 dias de segunda a sexta, antes de descontar feriados e exclusões do expediente; nenhum calendário local foi verificado nesta etapa.
5. Tratar os cinco dias úteis de análise inicial e os cinco dias úteis de homologação explicitamente. Não somá-los ou descontá-los de forma silenciosa do prazo contratual.
6. Apresentar parecer de viabilidade com incertezas e alternativas. Sem esses dados, manter a conclusão como **viabilidade não comprovada**, sem prometer o escopo integral ou retirar obrigações.

## 9. Condições comerciais preservadas como entradas

Conforme F01, sem alteração ou proposta final: implantação de R$ 24.000, em R$ 12.000 no fechamento e R$ 12.000 no aceite; evolução de R$ 8.000/mês por 80 h, nas modalidades de 3, 6 ou 12 meses, com mesmo valor mensal. As horas incluem análise, planejamento, desenvolvimento, testes, documentação, reuniões e manutenção evolutiva. Defeitos cobertos por garantia não devem consumir a franquia de evolução.

Primeira mensalidade prevista 30 dias após contratação; demais no quinto dia útil de cada mês. Competências, serviços distintos em caso de atraso, horas remanescentes/adicionais, suporte, garantia e rescisão permanecem pendentes de definição contratual e revisão jurídica. Este diagnóstico não redige nem valida juridicamente essas cláusulas.

## 10. Aprovação solicitada para a próxima etapa

Solicita-se aprovação para iniciar **a etapa 1 do plano**, consolidando a visão, o registro de decisões e a coleta de exemplos e respostas pendentes. A aprovação deste plano não aprova automaticamente a matriz preliminar, a stack, a viabilidade dos 30 dias ou uma minuta contratual.

A pausa antes dessa etapa decorre da instrução expressa de F01 §15: “Solicitar aprovação antes de avançar para a próxima etapa.”
