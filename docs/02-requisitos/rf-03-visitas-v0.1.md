# RF-03 — Visitas, avisos e posição do veículo

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Escopo MVP. Regras gerais aprovadas em F18/F19/F23/F25/F26. Campos em D-05/D-06/D-07, convenções CT e fluxos FL-02/FL-03. Detalhamento desta versão PROPOSTO. DP-03 condiciona a homologação real da API. Dados de posição identificam o veículo associado ao evento.

### RF-03.01 — Selecionar cliente para visita

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Promotor, P1, cliente_id e identificação de D-02 |
| Validações | Cliente ativo e existente. Seleção independe da autoria das visitas anteriores |
| Fluxo | Pesquisar cliente, selecionar e apresentar identificação, campanhas e avisos aplicáveis |
| Exceções | Cliente inativado exige recarregar. Busca sem resultado orienta contato com Escritório para cadastro |
| Aceite CA-RF-03.01 | Dado cliente ativo visitado por outro promotor, quando selecionado, então o promotor atual pode preparar sua visita e consultar campanhas/avisos desse cliente |
| Fonte | F25, DEC-F33 |

### RF-03.02 — Registrar check-in

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Promotor, P0, D-05/D-06 e chave de requisição |
| Validações | Conta, cliente e veículo válidos, um vínculo fixo e ausência de visita ABERTA. Avaliar posição por RF-03.09 e recolher justificativa quando necessário |
| Fluxo | Solicitar início, identificar veículo, obter posição/condição, confirmar dados e salvar visita com data/hora do sistema. Exibir confirmação e ID |
| Exceções | Visita aberta direciona para ela. Posição em exceção permite justificativa. Erro ao salvar exige aviso/repetição. Duplo toque reutiliza a mesma operação |
| Aceite CA-RF-03.02 | Dado promotor sem visita aberta, quando check-in é confirmado, então há uma visita vinculada ao cliente/veículo/autor. Duas requisições simultâneas não criam duas abertas. Falha após persistir e repetição com a mesma chave devolvem a visita já criada |
| Fonte | F18/F19/F23, DEC-F26/F29/F30/F31 |

### RF-03.03 — Registrar check-out

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Promotor autor, P0, visita, campos de encerramento, posição e chave de requisição |
| Validações | Visita ABERTA do próprio promotor. Horário de encerramento igual/posterior ao início. Veículo da visita preservado, inclusive em eventual alteração administrativa posterior de vínculo |
| Fluxo | Abrir visita, solicitar encerramento, avaliar posição/justificativa e salvar checkout com hora do sistema |
| Exceções | Visita já encerrada conserva seu primeiro encerramento. Tentativa de outro promotor é recusada. Falha de posição usa conferência. Falha de persistência permite nova tentativa |
| Aceite CA-RF-03.03 | Dada visita aberta, quando checkout é salvo, então passa a ENCERRADA com horários e snapshots corretos. Repetição retorna o estado encerrado e preserva o instante original |
| Fonte | F18/F19/F23, DEC-F26/F29/F30/F31 |

### RF-03.04 — Editar motivo e observações na visita aberta

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Promotor autor, P1, motivo e observações de D-05 |
| Validações | Visita ABERTA, campos permitidos e revisão atual |
| Fluxo | Alterar motivo/observações e salvar com histórico |
| Exceções | Visita encerrada entre leitura e gravação impede editar. Campos de horário, autor e veículo seguem ações próprias |
| Aceite CA-RF-03.04 | Dada visita própria aberta, quando motivo é atualizado, então consulta mostra o novo conteúdo e auditoria registra a mudança. Após encerramento, o mesmo comando é recusado |
| Fonte | F18, DEC-F27 |

### RF-03.05 — Consultar visitas próprias

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Promotor, P1, filtros de período/cliente/situação e paginação |
| Validações | Restringir autoria à conta da sessão. Exibir horário, motivo, observações e situação permitidos |
| Fluxo | Consultar lista, aplicar filtro e abrir detalhe próprio |
| Exceções | ID de visita alheia é recusado. Resultado vazio mantém filtros visíveis |
| Aceite CA-RF-03.05 | Dados registros de dois promotores no mesmo cliente, quando um deles consulta histórico próprio, então recebe apenas os registros de sua autoria. O cliente continua disponível para novas visitas de ambos |
| Fonte | F01 RF-03, bloco F25 e DEC-F33 |

### RF-03.06 — Acompanhar visitas administrativamente

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Escritório/Master, P1, período/cliente/promotor/situação, identificação e condição da localização |
| Validações | Visão geral autorizada. Horários da visita e da posição são mostrados separadamente |
| Fluxo | Listar, filtrar e abrir detalhe com histórico e eventuais marcações para conferência |
| Exceções | Posição sem dados mostra a condição registrada. Consulta não altera a evidência original |
| Aceite CA-RF-03.06 | Dadas visitas de vários promotores, quando Escritório filtra um período, então consulta os registros correspondentes e identifica visitas abertas e posições em exceção |
| Fonte | F01 RF-03, F19/F23 |

### RF-03.07.01 — Regularizar visita encerrada ou esquecida

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Master, P0, visita, valores corrigidos, motivo e revisão atual |
| Validações | Preservar original, coerência entre horários e autoria. Fechar visita esquecida exige data/hora informadas e justificadas, distinguidas do instante de regularização |
| Fluxo | Master examina histórico, informa correção ou encerramento, justifica e confirma uma revisão auditada |
| Exceções | Horário incoerente, alteração concorrente ou tentativa pelo Escritório recebe recusa. Troca de cliente/promotor/veículo em visita existente exige conferência explícita do impacto, proposta de exceção |
| Aceite CA-RF-03.07.01 | Dada visita esquecida, quando Master regulariza, então fica encerrada com valores informados, original preservado, motivo e horário da correção. O registro não atribui automaticamente a hora de correção como hora da visita |
| Fonte | F14/F18, DEC-F28. RF-03.07 é agrupador para as regras já distribuídas em RF-03.02/03/04 e esta correção |

### RF-03.08.01 — Criar aviso interno por cliente e período

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Escritório, P1, cliente, texto e início/fim de D-07 |
| Validações | Cliente existente, conteúdo e período válidos, datas inclusivas propostas PT-05 |
| Fluxo | Preencher, validar e publicar aviso vinculado ao cliente |
| Exceções | Período invertido ou campo vazio impede salvar. Conteúdo é tratado como texto seguro |
| Aceite CA-RF-03.08.01 | Dado aviso válido, quando salvo, então fica disponível ao selecionar o cliente durante a vigência e sua autoria é identificável |
| Fonte | F26, DEC-F38 |

### RF-03.08.02 — Exibir avisos aplicáveis

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Promotor, P1, cliente selecionado e data operacional |
| Validações | Filtrar cliente e vigência. Promotor pode consultar qualquer cliente ativo |
| Fluxo | Ao selecionar cliente, carregar os avisos vigentes e mostrar seus textos/períodos |
| Exceções | Ausência de avisos apresenta estado vazio. Erro de carga informa falha e permite recarregar |
| Aceite CA-RF-03.08.02 | Dados avisos de dois clientes e um aviso vencido, quando cliente A é selecionado, então aparecem apenas os vigentes vinculados a A |
| Fonte | F25/F26, DEC-F38 |

### RF-03.09 — Registrar posição do veículo no evento

| Aspecto | Especificação proposta |
|---|---|
| Ator/prioridade/campos | Sistema, com justificativa do Promotor, P0, campos de D-06 e veículo fixo de D-04 |
| Validações | Consultar veículo correto, posição válida e coordenadas plausíveis. Idade de zero a 300 segundos aceita. Acima de 300 ou posição inutilizável exige justificativa/conferência. Tempo do provedor depende de DP-03 |
| Fluxo | Resolver ID externo do veículo, consultar última posição, classificar condição e associar snapshot ao check-in/out. Segredos permanecem no servidor |
| Exceções | API indisponível, veículo sem acesso, posição antiga/inválida/ausente, horário futuro ou sem fuso conhecido recebem condição explícita. Falha ao salvar visita é tratada por CT-02, distinta da exceção de localização |
| Aceite CA-RF-03.09 | Dado evento com posição de 300 s, quando validada, então aceita como atual. Com 301 s, exige justificativa e marca conferência. Com API em erro, permite a mesma exceção aprovada e conserva causa/horários. Consulta administrativa mostra posição do veículo e instante original |
| Fonte | F19/F21/F23, DEC-F30/F31, MC-01. Regras operacionais aprovadas, detalhes técnicos PROPOSTOS e homologação PENDENTE |
