# RF-06 — Veículos e abastecimentos

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Todos MVP/P1. Bases F25/F27, DEC-F35/F40–F43. Campos D-04/D-12, CT, FL-06 e permissões integram cada requisito. Precisões propostas para litros/hodômetro são três casas, valores de combustível duas casas. A regra aprovada de três casas da cotação permanece específica a RF-05.

### RF-06.01.01 — Cadastrar veículo

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, placa, identificação, referência externa do rastreador e situação |
| Validações | Placa normalizada única conforme D-04. Referência externa necessária à obtenção de posição |
| Fluxo | Salvar veículo e disponibilizar para vínculo Master/abastecimento |
| Exceções | Sem referência válida, consulta de posição segue exceção justificada RF-03.09 |
| Aceite CA-RF-06.01.01 | Dada placa já cadastrada, quando novo cadastro a repete, então bloqueia duplicidade |
| Fonte | F25, DEC-F35 |

### RF-06.01.02 — Manter veículo

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, identificação, referência externa e situação. Retificação de placa por Master é detalhamento PROPOSTO |
| Validações | Alteração versionada, sem mudar veículo nos eventos passados. Inativação com vínculo/visita aberta exige regularização prévia, regra PROPOSTO |
| Fluxo | Ajustar rotina e registrar alteração. Vínculo fixo usa RF-02.04.02 |
| Exceções | Mudança concorrente exige recarregar. Histórico permanece identificável |
| Aceite CA-RF-06.01.02 | Dada referência de rastreador alterada, quando consulta visita anterior, então a origem histórica permanece preservada |
| Fonte | F14/F25, D-04 |

### RF-06.02 — Registrar abastecimento

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Promotor no veículo fixo, Escritório em qualquer veículo. Veículo, data, hodômetro, litros e valor total obrigatórios |
| Validações | Litros/valor positivos, hodômetro não negativo e coerente com registros anterior/posterior. Sem leitura automática de hodômetro presumida. Ordenação no mesmo dia depende de horário/sequência propostos D-12 |
| Fluxo | Selecionar veículo autorizado, preencher, validar e confirmar persistência |
| Exceções | Conflito cronológico ou edição concorrente bloqueiam confirmação e informam motivo. Repetição CT-03 não duplica |
| Aceite CA-RF-06.02 | Dado anterior 1.000 e posterior 1.200, quando tenta inserir hodômetro 1.300 entre eles, então bloqueia. Valor zero é recusado. Promotor não registra em outro veículo |
| Fonte | F27, DEC-F40/F41 |

### RF-06.03.01 — Consultar histórico

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Promotor no veículo fixo, Escritório/Master geral. Veículo e período |
| Validações | Alcance do perfil aplicado antes dos filtros. Política de acesso após troca de vínculo será confirmada na revisão, proposta de consultar seu veículo atualmente vinculado |
| Fluxo | Listar data, veículo, hodômetro, litros, valor e indicação de correção/retroatividade |
| Exceções | Veículo fora do alcance é negado inclusive por acesso direto |
| Aceite CA-RF-06.03.01 | Dado Promotor vinculado a A, quando consulta B diretamente, então acesso é negado |
| Fonte | F27, DEC-F40 |

### RF-06.03.02 — Totalizar abastecimentos

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Mesmos perfis/alcance de RF-06.03.01, período e veículo |
| Validações | Somar litros e valor dos mesmos registros filtrados, sem somar versões antigas de correção |
| Fluxo | Apresentar totais juntamente à consulta |
| Exceções | Sem registros retorna zero identificado para período consultado |
| Aceite CA-RF-06.03.02 | Dados dois lançamentos de 10/20 litros e R$ 50/100, quando ambos filtrados, então totais são 30 litros e R$ 150 |
| Fonte | F27/F28, DEC-F40/F44 |

### RF-06.04 — Corrigir abastecimento salvo

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Master, registro, campos alterados e justificativa D-12/D-13 |
| Validações | Mesmas regras numéricas/cronológicas, preservando anterior, autor original e responsável pela correção |
| Fluxo | Registrar retificação e refletir valor atual nas consultas/totais |
| Exceções | Troca de hodômetro ou exceção cronológica requer evidência e marcação específica, tratamento PROPOSTO sujeito à revisão |
| Aceite CA-RF-06.04 | Dado lançamento salvo, quando Escritório tenta corrigir, então nega. Master com motivo registra correção sem perder anterior |
| Fonte | F14/F27, DEC-F42 |

### RF-06.05 — Registrar abastecimento retroativo

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, campos de abastecimento, data real e justificativa |
| Validações | Conferir vizinhos cronológicos do veículo, incluindo posterior, com consistência sob gravações simultâneas |
| Fluxo | Informar ocorrência passada, justificar, validar e salvar marcando data real e instante de registro separadamente |
| Exceções | Incoerência impede inclusão comum e exige análise Master. Sem mudança silenciosa de datas |
| Aceite CA-RF-06.05 | Dado abastecimento ocorrido anteriormente, quando salvo com justificativa, então filtro usa data real e auditoria preserva instante de inclusão |
| Fonte | F27, DEC-F43 |
