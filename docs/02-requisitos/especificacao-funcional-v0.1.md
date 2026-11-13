# Especificação funcional C3

Status PROPOSTO • Identificação ESF-C3-0.1 • 10/11/2026 • Etapa 2 autorizada em F32.

Registro da base histórica. A versão corrente é [ESF-C3-0.2](especificacao-funcional-v0.2.md), que explicita as mudanças aprovadas e a precedência do adendo nos IDs afetados.

## Controle da versão

Este documento é a entrada única da especificação ESF-C3-0.1. Os arquivos relacionados abaixo compõem a mesma versão e devem ser revisados em conjunto. A aprovação do documento e de seus detalhes será registrada pelo responsável. As decisões aprovadas na descoberta permanecem identificadas por fonte, enquanto campos, validações e critérios novos são PROPOSTOS para revisão.

| Parte | Documento | Conteúdo |
|---|---|---|
| Dados | [Dicionário funcional](dicionario-dados-v0.1.md) | Campos, tipos, obrigatoriedade, validações e vínculos |
| RF-01 | [Acesso e contas](rf-01-acesso-v0.1.md) | Autenticação, autorização, ativação e gestão reservada |
| RF-02 | [Cadastros](rf-02-cadastros-v0.1.md) | Clientes, fornecedores, funcionários e associações |
| RF-03 | [Visitas e avisos](rf-03-visitas-v0.1.md) | Check-in/out, edição, correção e posição do veículo |
| RF-04 | [Campanhas](rf-04-campanhas-v0.1.md) | Solicitação, decisão externa, folders e vigência |
| RF-05 | [Pedidos e propostas](rf-05-pedidos-v0.1.md) | Entrada, importação, PDF, versões, decisões e envio externo |
| RF-06 | [Veículos e abastecimentos](rf-06-abastecimentos-v0.1.md) | Cadastro, lançamentos, retroativos e correções |
| RF-07 | [Consultas e métricas](rf-07-consultas-v0.1.md) | Indicadores, filtros, Excel e compras faturadas |
| RNF | [Qualidade e requisitos transversais](requisitos-nao-funcionais-v0.1.md) | Segurança, integridade, arquivos, desempenho e operação |
| Permissões | [Matriz por ação e alcance](../03-fluxos-permissoes/matriz-permissoes-v0.1.md) | Escritório, Promotores e Master |
| Fluxos | [Estados e diagramas Mermaid](../03-fluxos-permissoes/fluxos-v0.1.md) | Contexto e fluxos funcionais editáveis |
| Rastreabilidade | [Matriz de requisitos](matriz-requisitos.md) | Correspondência dos IDs da descoberta às definições desta versão |

## Diretrizes que governam a especificação

- Dois atores operacionais, Escritório e Promotores, e perfil reservado Master. Escritório realiza rotina, Master gerencia contas/configurações e correções excepcionais. F13/F14.
- Todos os promotores consultam e selecionam qualquer cliente cadastrado para visita. Histórico de visitas do promotor segue sua autoria. F25.
- Atividades de WhatsApp, e-mail e portais continuam externas, com registro interno de andamento e decisões. DEC-01 e F01.
- Cotação Wega usa código e Grupo, preço direto da planilha, mínimo de quantidade e total em três casas decimais. F15/F16.
- Posição no check-in/out vem da API do veículo fixo. Até cinco minutos, com justificativa e conferência em exceções. F19/F23.
- Campanhas/avisos, abastecimentos e métricas seguem F26–F28. Compras faturadas têm origem Excel com amostra ainda aguardada.
- Implantação de R$ 24.000, mensalidade posterior de R$ 8.000/80 h, competências pagas no fechamento, suporte e rescisão seguem F29–F31. Estas condições ficam no registro de decisões e serão formalizadas na etapa contratual.

As fontes e decisões estão no inventário e no registro de governança. [Fontes](../00-governanca/fontes.md) e [decisões](../00-governanca/decisoes.md).

## Identificadores, prioridade e aprovação

Os IDs RF da descoberta permanecem como referências. Quando um item agrupava ações, seus subitens recebem sufixos `.01`, `.02` e seguintes. Cada folha abaixo tem uma ação principal, ator, campos, fluxo, validações/exceções e aceite próprio. Um ID pai desdobrado é agrupador de rastreabilidade. O aceite deve usar seus subitens.

Todos os registros desta versão têm detalhamento PROPOSTO. O campo Base informa a decisão aprovada que fundamenta a ação. P0 representa proteção ou dependência crítica e P1 a operação prevista. Ambas integram o dimensionamento do MVP. CONDICIONAL identifica capacidade que depende de material e inclusão formal, especialmente fontes futuras e arquivos próprios de fornecedor.

Cada critério identificado como `CA-<ID>` constitui cenário verificável proposto, a ser usado na homologação. A expressão Dado/Quando/Então indica pré-condição, ação e resultado esperado. Os cenários transversais de autorização, concorrência e falha são cumulativos aos cenários específicos.

## Convenções transversais CT

| ID | Convenção proposta | Verificação |
|---|---|---|
| CT-01 | Autorização aplicada no servidor por ação, registro e campo. Master possui visão geral e poderes reservados | Chamada direta com identidade sem permissão é recusada e preserva dados |
| CT-02 | Toda gravação confirma sucesso após persistência. Erro exibe mensagem acionável e conserva o formulário quando viável | Simular perda de conexão antes e depois da gravação |
| CT-03 | Operação repetida reconhece seu identificador de requisição. Mudanças concorrentes usam versão/revisão do registro | Duas tentativas produzem um efeito. Edição baseada em versão antiga exige recarregar |
| CT-04 | Operação funcional e evento de auditoria formam uma unidade consistente | Falha durante a operação preserva estado anterior ou conclui ambos |
| CT-05 | Histórico de fatos, evidências e versões é preservado. Retificações registram autor, instante, motivo e valores anteriores | Corrigir e reconstruir sequência original e retificada |
| CT-06 | Datas técnicas preservam instante e fuso. Exibição operacional usa America/Fortaleza | Conferir virada de dia, ordenação e filtros pela data operacional |
| CT-07 | Campos de escolha referenciam entidades existentes. Entidade inativa preserva histórico e fica indisponível para novas operações que dependam de atividade | Consultar histórico inativo e tentar nova vinculação |
| CT-08 | Limites, precisão e validações do dicionário são aplicados ao formulário e ao servidor | Enviar diretamente valores fora de limite ou campos proibidos |
| CT-09 | Consultas e exportações usam os mesmos critérios de acesso, recorte e cálculo | Comparar conjunto filtrado, indicadores e arquivo exportado |
| CT-10 | Integração preserva proveniência e separa erro do provedor de erro ao salvar a visita | Posição ausente permite exceção aprovada. Falha de persistência exige nova tentativa conforme D05 |

## Propostas técnicas para revisão PT

| ID | Detalhe proposto nesta versão | Situação |
|---|---|---|
| PT-01 | Login por e-mail e senha, recuperação mediante procedimento conduzido por Master, contas individuais | PROPOSTO. Produto de autenticação será escolhido na arquitetura |
| PT-02 | Sessão absoluta de oito horas, inatividade de trinta minutos e revogação na desativação/alteração sensível de conta | PROPOSTO, sujeito à adequação operacional |
| PT-03 | Quantidades Wega em unidades inteiras positivas. UNIT preserva precisão da origem e total usa arredondamento decimal de metade para cima em três casas | PROPOSTO para detalhes novos. Origem do preço, mínimo e três casas estão aprovados em F16 |
| PT-04 | Folder JPG/PNG/PDF, até 10 MB por arquivo. Arquivo XLSX até 20 MB descompactado até 100 MB, 10 mil linhas e limite de execução a dimensionar | PROPOSTO. Validar com arquivos reais e custos. Precisões e limites constam no dicionário |
| PT-05 | Campanhas e avisos usam datas inclusivas no fuso operacional. Semântica de dia final e mudanças após publicação seguem os fluxos desta versão | PROPOSTO para fronteiras e correções |
| PT-06 | Fonte de compras passa por lote de validação, confirmação e publicação consistente. Layout, chaves e ajustes aguardam amostra | PROPOSTO e dependente de material. Indicadores e origem Excel aprovados em F28 |
| PT-07 | Exportação administrativa em XLSX. Promotor mantém consultas aprovadas em tela. Exportação por promotor fica PENDENTE de decisão específica | PROPOSTO para concessão por perfil. Saídas Excel aprovadas em F28 |
| PT-08 | Correções após envio externo de pedido exigem Master para retificação interna com motivo e acompanhamento externo pelo Escritório | PROPOSTO para exceção. As decisões externas permanecem sob revisão humana |

Os valores PT constituem propostas revisáveis. Sua aprovação deverá ser explícita. A rastreabilidade distingue alterações de detalhe de mudanças de escopo.

## Dependências DP

| ID | Dependência | Efeito | Responsável e momento |
|---|---|---|---|
| DP-01 | Fonte Excel de compras faturadas | Layout, identidade de compra, cliente/fornecedor, datas, valores, devoluções e atualização aguardam amostra | Caio fornece, Ismael analisa antes de homologar a alimentação |
| DP-02 | Próximos fornecedores | Identificar formato/processo e inclusão contratual por fornecedor | Caio/Ismael e aprovação bilateral no anexo técnico |
| DP-03 | API Upcar | Homologar autenticação, permissões, temporalidade, disponibilidade e latência com a conta C3 | Ismael com apoio de João Vitor na etapa técnica autorizada |
| DP-04 | Infraestrutura e volumes | Metas definitivas, custos, retenção, backup e disponibilidade dependem de orçamento/carga | Ismael propõe cenários, Caio confirma/aprova |
| DP-05 | Precisão e exemplos Wega | Homologar mapeamento e casos monetários com PDF esperado | Ismael/Caio na revisão desta especificação |
| DP-06 | Arquivo de fornecedor | Layout de saída específico exige referência e aceite próprio | Caio fornece e ambas as partes aprovam inclusão |

## Fronteiras de escopo e aceite

O conjunto de fornecedores futuros permanece uma demanda com inclusão condicionada ao detalhamento de cada fonte. A especificação detalha a amostra Wega disponível e registra as condições das demais fontes. O anexo técnico deverá expressar o conjunto efetivamente contratado, com impactos aprovados.

GPS contínuo, trajetos, comandos remotos de rastreador, integrações automáticas de WhatsApp/e-mail/portais, catálogo permanente, estoque, metas/ranking, tarefas completas, IA e BI avançado mantêm a classificação da matriz de escopo. A consulta pontual ao rastreador foi adicionada por F19 e MC-01.

A homologação usará a versão aprovada do pacote e os critérios de suas folhas. A entrega para testes e os cinco dias úteis de homologação seguem D13. O prazo de 30 dias ainda depende de avaliação técnica, considerando a capacidade de Ismael de 80 h/mês.

## Revisão 1 — Exclusividade do veículo

Em 10/11/2026, F35 confirma que cada veículo é exclusivo do promotor. D-04 e RF-02.04.02 passam a exigir também unicidade do vínculo vigente por veículo. Acrescenta o caso de recusa de associação simultânea do mesmo veículo a dois promotores. Os demais detalhes propostos aguardam revisão. A arquitetura ARQ-C3-0.1 usa ESF-C3-0.1 revisão 1.

