# RF-07 — Consultas, indicadores e saídas Excel

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Todos MVP/P1. Bases F01 RF-07, F28 e DEC-F44–F47. CT-09 e matriz de permissões se aplicam a cada folha. Layouts de tela e XLSX abaixo são PROPOSTO. Nenhum filtro aumenta o alcance de dados do perfil.

### RF-07.01 — Consultar pedidos e aprovações

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master, solicitação, cliente, fornecedor, versão, resposta, revisão, autorização e envio |
| Validações | Estados independentes por versão, sem contabilizar versões históricas como pedidos adicionais |
| Fluxo | Listar solicitação com versão atual e acessar histórico/decisões |
| Exceções | Ausência de resposta aparece pendente, sem inferir aprovação |
| Aceite CA-RF-07.01 | Dada solicitação com três versões, quando listada, então aparece uma solicitação e permite identificar as três versões no histórico |
| Fonte | F01 RF-07, F17 |

### RF-07.02 — Aplicar filtros pertinentes

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Perfil autorizado. Período, cliente, promotor, fornecedor, veículo e situação quando pertinentes |
| Validações | Início menor ou igual ao fim. Período inclusivo local PT-05. Visitas usam início, pedidos recebimento, combustível ocorrência, compras faturamento. Campanhas filtram vigência por interseção, PROPOSTO |
| Fluxo | Validar filtros, aplicar autorização e atualizar listagem/totais/saída |
| Exceções | Filtro incompatível informa erro. Paginação mantém filtros e ordenação estável proposta por data/ID |
| Aceite CA-RF-07.02 | Dado filtro válido, quando pagina ou exporta, então mantém o mesmo universo autorizado. URL manipulada para outro promotor não amplia acesso |
| Fonte | F28, DEC-F45, CT-09 |

### RF-07.03.01 — Contar visitas

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master geral, Promotor próprias visitas. Período, cliente e promotor autorizado |
| Validações | Uma visita por ID, estado atual aberta/encerrada, mesma base da listagem |
| Fluxo | Mostrar contagem por situação |
| Exceções | Período sem registros retorna zero |
| Aceite CA-RF-07.03.01 | Dadas duas abertas e três encerradas no recorte, quando consultado, então exibe 2 e 3 |
| Fonte | F28, DEC-F44, RF-03.05/06 |

### RF-07.03.02 — Contar pedidos

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master, período, fornecedor e situação |
| Validações | Solicitação contada uma vez por agrupamento, usando versão atual e eixo selecionado de decisão/revisão/envio |
| Fluxo | Mostrar contagens por situação/fornecedor com nome explícito do eixo |
| Exceções | Eixos independentes não são somados como se fossem estados mutuamente exclusivos |
| Aceite CA-RF-07.03.02 | Dada solicitação aprovada e enviada, quando contado eixo envio, então conta uma enviada e não duas solicitações |
| Fonte | F28, DEC-F44, D-08/D-10 |

### RF-07.03.03 — Contar campanhas

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master, fornecedor, cliente, situação e vigência |
| Validações | Uma campanha por ID mesmo com vários clientes. Separar decisão de condição ativa/vencida |
| Fluxo | Apresentar contagens e critérios de vigência |
| Exceções | Campanha aprovada sem folder não entra na contagem ativa |
| Aceite CA-RF-07.03.03 | Dada campanha para três clientes, quando consulta geral, então conta uma campanha |
| Fonte | F26/F28, DEC-F37/F44 |

### RF-07.03.04 — Exibir totais de combustível

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Mesmos atores, campos e alcance de RF-06.03.02 |
| Validações | Reusar cálculo definido em RF-06.03.02 |
| Fluxo | Apresentar litros/valor por veículo e período |
| Exceções | Registro corrigido contribui apenas com valor atual |
| Aceite CA-RF-07.03.04 | Dado mesmo filtro, quando consulta indicador e histórico, então totais coincidem |
| Fonte | F28, DEC-F44 |

### RF-07.04.01 — Exportar visitas em XLSX

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master PT-07. ID, cliente, promotor, veículo, início, fim, situação, motivo e marcação para conferência |
| Validações | Mesmo recorte da consulta, todas as páginas, RNF-04. Coordenadas/evidências sensíveis excluídas do layout inicial proposto |
| Fluxo | Gerar XLSX com filtros/data de geração e cabeçalhos |
| Exceções | Falha informa erro e permite repetir. Dados textuais não executam fórmulas |
| Aceite CA-RF-07.04.01 | Dado filtro com 120 visitas e página de 20, quando exportado, então contém 120 linhas autorizadas |
| Fonte | F28, DEC-F46, PT-07 |

### RF-07.04.02 — Exportar pedidos em XLSX

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master. ID, cliente, fornecedor, data, versão atual, decisão cliente, revisão, autorização e envio |
| Validações | Mesmas regras de RF-07.04.01 e uma linha por solicitação |
| Fluxo | Exportar listagem filtrada com estados em colunas distintas |
| Exceções | Versões antigas permanecem no histórico e não duplicam linhas |
| Aceite CA-RF-07.04.02 | Dado pedido com duas versões, quando exportado, então uma linha identifica versão atual e estados correspondentes |
| Fonte | F28, DEC-F46, PT-07 |

### RF-07.04.03 — Exportar campanhas em XLSX

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master. ID, título, fornecedor, clientes-alvo, decisão, início/fim e condição ativa |
| Validações | Mesmas regras de RF-07.04.01 e uma linha por campanha, clientes-alvo agrupados como texto |
| Fluxo | Exportar recorte administrativo |
| Exceções | Campanha multicliente não duplica contagem |
| Aceite CA-RF-07.04.03 | Dada campanha para três clientes, quando exportada, então uma linha identifica os três alvos |
| Fonte | F28, DEC-F46, PT-07 |

### RF-07.04.04 — Exportar abastecimentos em XLSX

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master. ID, veículo, data real, autor, hodômetro, litros, valor, retroatividade e correção |
| Validações | Mesmas regras de RF-07.04.01, números como células numéricas e identificadores como texto |
| Fluxo | Exportar registros atuais e totais conferíveis |
| Exceções | Valores anteriores à correção não são somados |
| Aceite CA-RF-07.04.04 | Dados registros filtrados, quando exportados, então soma de litros/valores coincide com RF-06.03.02 |
| Fonte | F28, DEC-F46, PT-07 |

### RF-07.05.01 — Alimentar compras faturadas por Excel

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, proposta PT-06. Lote, cliente, fornecedor, data e valor D-12 |
| Validações | DEPENDENTE DP-01. Exigir amostra para mapear identificadores, documentos/itens, devoluções, cancelamentos, duplicidades e atualização |
| Fluxo | Proposta de validar lote, exibir erros e confirmar publicação integral. Definir substituição integral ou incremental após conhecer a fonte |
| Exceções | Layout não homologado permanece indisponível para cálculo. Mesma compra não pode ser contada duas vezes. Chave concreta aguarda amostra |
| Aceite CA-RF-07.05.01 | Dado layout homologado futuramente, quando lote válido é confirmado duas vezes, então base reflete uma publicação lógica. Erros impedem publicação parcial |
| Fonte | F28, DEC-F47, PT-06, DP-01. Critério específico do layout PENDENTE |

### RF-07.05.02 — Calcular valor comprado no período

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Promotores para qualquer cliente cadastrado, Escritório/Master. Cliente, fornecedor, período |
| Validações | Usar apenas compras faturadas do lote publicado. Regra de ajustes/devoluções depende de DP-01 |
| Fluxo | Somar valores do recorte e mostrar origem e atualização da base |
| Exceções | Sem base disponível mostrar indisponibilidade. Zero somente quando base válida não contém compras no recorte |
| Aceite CA-RF-07.05.02 | Dada base homologada com compras 100 e 50 no recorte, quando consulta, então mostra 150. Base ausente mostra indisponível |
| Fonte | F28, DEC-F47, DP-01 |

### RF-07.05.03 — Mostrar última compra

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Mesmos perfis de RF-07.05.02, cliente/fornecedor |
| Validações | Maior data de compra faturada válida na base, independentemente do filtro de soma por período, semântica PROPOSTO |
| Fluxo | Exibir última data com origem/atualização |
| Exceções | Base válida sem compras mostra sem compra registrada. Base ausente mostra indisponível |
| Aceite CA-RF-07.05.03 | Dadas compras em 01/10 e 05/11, quando consulta última compra, então mostra 05/11, mesmo com soma filtrada em outubro |
| Fonte | F28, DEC-F47, DP-01 |
