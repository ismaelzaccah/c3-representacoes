# RF-04 — Campanhas

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Escopo MVP, prioridade P1. Bases F01 RF-04 e F25/F26, DEC-F36–F39. Campos em D-07/D-11. Aplicam-se CT, FL-04, permissões e RNF-04. Avisos internos são definidos em RF-03.08. O detalhamento é PROPOSTO.

### RF-04.01 — Solicitar campanha

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Promotor, título, fornecedor, cliente-alvo inicial e descrição. Solicitante pela sessão |
| Validações | Cliente/fornecedor ativos, texto obrigatório e responsável operacional conforme D-07 |
| Fluxo | Criar solicitação no estado SOLICITADA. Encaminhamento ao fornecedor ocorre no processo externo |
| Exceções | Falta de vínculos ou entidade inativada impede nova solicitação. Solicitação repetida com a mesma chave gera um registro |
| Aceite CA-RF-04.01 | Dado cliente ativo, quando Promotor solicita campanha, então a solicitação aparece ao Escritório com autor, cliente e fornecedor identificados |
| Fonte | F01 RF-04, F26 |

### RF-04.02 — Registrar decisão externa do fornecedor

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, campanha, APROVADA/REJEITADA, data da resposta e observações. Motivo na rejeição proposto D-07 |
| Validações | Campanha no estado compatível e revisão atual. Registrar quem informou e quando o fez |
| Fluxo | Receber resposta externamente, registrar a decisão e salvar histórico |
| Exceções | Decisões concorrentes exigem recarregar. Retificação posterior usa Master com justificativa, proposta de aplicação de F14 |
| Aceite CA-RF-04.02 | Dada solicitação pendente, quando Escritório registra rejeição, então histórico identifica decisão, autor, data e motivo. Aprovação registrada ainda depende de folder/vigência para aparecer ativa |
| Fonte | F26, DEC-F37 |

### RF-04.03 — Anexar folder

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, campanha e um ou mais arquivos D-11 |
| Validações | Tipo, tamanho e verificação de conteúdo conforme RNF-04/PT-04. Arquivo pronto vinculado à campanha |
| Fluxo | Enviar, validar e associar arquivo. Folders anteriores conservam referência no histórico quando substituídos |
| Exceções | Falha no upload informa estado e mantém campanha consistente. Arquivo rejeitado não conta para a condição ativa |
| Aceite CA-RF-04.03 | Dada campanha aprovada com vigência atual, quando folder permitido é validado, então aparece no detalhe do cliente-alvo. Arquivo excedente/rejeitado preserva os folders válidos existentes |
| Fonte | F26, DEC-F37 |

### RF-04.04 — Definir clientes-alvo e vigência

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, conjunto de clientes e datas de D-07 |
| Validações | Pelo menos um cliente, referências existentes e início menor/igual ao fim. Preservar histórico de mudanças |
| Fluxo | Atualizar seleção de alvos/período e recalcular condição de atividade |
| Exceções | Datas incoerentes impedem salvar. Alteração em campanha já vigente avisa impacto e fica auditada, proposta de detalhe |
| Aceite CA-RF-04.04 | Dada campanha com alvos A/B, quando vigência válida é salva, então ambos os clientes exibem o folder no período e C permanece fora da exibição |
| Fonte | F26, DEC-F36/F37 |

### RF-04.05 — Exibir campanhas ativas do cliente

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Promotor, cliente selecionado, data operacional e metadados dos folders |
| Validações | Cliente vinculado, decisão APROVADA, folder pronto e período vigente. Limites de datas inclusivos PT-05 |
| Fluxo | Carregar campanhas/folders ao selecionar cliente ou abrir visita |
| Exceções | Campanha aprovada sem material/período permanece no administrativo com condição incompleta. Erro de carga permite nova tentativa |
| Aceite CA-RF-04.05 | Dadas campanhas vigentes, vencidas, canceladas e de outro cliente, quando Promotor seleciona A, então aparecem somente as ativas de A, acessíveis a qualquer promotor |
| Fonte | F25/F26, DEC-F37 |

### RF-04.06 — Consultar histórico administrativo

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master, cliente, fornecedor, situação, vigência e solicitante |
| Validações | Recorte autorizado e distinção entre decisão e condição de atividade |
| Fluxo | Listar, filtrar e abrir sequência de solicitações, decisões, folders e mudanças |
| Exceções | Vencimento ou cancelamento mantém registro consultável. Exibição de entidade inativa preserva identificação histórica |
| Aceite CA-RF-04.06 | Dada campanha vencida, quando Escritório consulta o histórico, então encontra solicitação, decisão e material com a condição vencida identificada |
| Fonte | F01 RF-04, F26 |

### RF-04.07.01 — Aplicar expiração da vigência

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Sistema, datas e decisão da campanha |
| Validações | Data operacional fora do período deixa condição ativa falsa. Preservar decisão do fornecedor |
| Fluxo | Avaliar condição em consultas e indicadores usando a mesma regra de período |
| Exceções | Cache, se houver, deve respeitar mudança do dia e atualização de vigência |
| Aceite CA-RF-04.07.01 | Dada campanha válida até hoje, quando consulta ocorrer no dia seguinte, então sai das ativas e continua no histórico, conservando aprovação e folders |
| Fonte | F26, DEC-F39 |

### RF-04.07.02 — Cancelar campanha

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, campanha e motivo |
| Validações | Motivo obrigatório, revisão atual e estado cancelável. Cancelamento repetido conserva primeiro evento |
| Fluxo | Confirmar, registrar CANCELADA com motivo/autor/data e retirar exibição ativa |
| Exceções | Retificação de cancelamento deve ser explícita por Master com histórico, proposta de correção excepcional |
| Aceite CA-RF-04.07.02 | Dada campanha ativa, quando cancelada com motivo, então deixa a lista dos clientes-alvo e continua consultável no administrativo com evidência da mudança |
| Fonte | F26, DEC-F39 |
