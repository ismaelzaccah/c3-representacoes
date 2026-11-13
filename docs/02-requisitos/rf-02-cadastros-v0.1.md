# RF-02 — Cadastros e associações

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Escopo MVP, prioridade P0. Bases F01 RF-02, F14/F23/F25. Campos em D-01–D-04. Aplicam-se CT-01–CT-09. A matriz de permissões e FL-01 governam cada operação. As regras gerais foram aprovadas e o detalhamento é PROPOSTO.

### RF-02.01.01 — Cadastrar estabelecimento cliente

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, D-02. Master tem acesso administrativo superior |
| Validações | Nome, CNPJ, endereço, cidade e UF obrigatórios. CNPJ válido e único normalizado, inclusive contra inativos |
| Fluxo | Preencher, validar e criar cliente ativo. Mostrar identificação salva |
| Exceções | Duplicidade informa existência do cadastro ao operador autorizado. Corrida de cadastros conserva um único CNPJ |
| Aceite CA-RF-02.01.01 | Dado CNPJ ainda inexistente e campos válidos, quando salvar, então o cliente passa a estar disponível a todos os promotores. Duas requisições concorrentes para o mesmo CNPJ resultam em um cadastro |
| Base | F25, DEC-F32/F33 |

### RF-02.01.02 — Editar dados rotineiros do cliente

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, nome/endereço e contatos de D-02. CNPJ proposto como identidade reservada ao Master após criação |
| Validações | Campos obrigatórios mantidos. Revisão atual e acesso por campo. Alteração preserva autoria |
| Fluxo | Consultar cadastro, ajustar rotina e salvar nova revisão |
| Exceções | Campo reservado ou revisão desatualizada recebe recusa com orientação de regularização |
| Aceite CA-RF-02.01.02 | Dado cliente existente, quando Escritório altera telefone, então consulta reflete o novo contato e a auditoria preserva o anterior. Tentativa de alterar CNPJ exige a ação reservada |
| Base | F14/F25. Classificação específica de CNPJ como correção excepcional é PROPOSTA |

### RF-02.01.03 — Consultar clientes

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master em visão geral. Promotores acessam clientes ativos com dados necessários à visita de D-02 |
| Validações | Busca por nome/CNPJ normalizado e paginação. Exibir situação nos contextos administrativos |
| Fluxo | Pesquisar, escolher cliente e abrir identificação, campanhas e avisos aplicáveis |
| Exceções | Busca vazia apresenta orientação. Cliente inativado entre busca e gravação é revalidado no servidor |
| Aceite CA-RF-02.01.03 | Dado cliente visitado por outro promotor, quando um Promotor pesquisa, então o cliente ativo pode ser consultado e selecionado para nova visita |
| Base | F25, DEC-F33 |

### RF-02.01.04 — Inativar cliente

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, cliente e motivo proposto |
| Validações | Preservar vínculos históricos. Tratar visita já aberta e pedido em andamento como fatos existentes |
| Fluxo | Confirmar, salvar situação INATIVO e registrar autoria. Operações existentes continuam consultáveis |
| Exceções | Inativação repetida é consistente. Novas operações que exigem cliente ativo são recusadas. Visita aberta continua apta a encerramento |
| Aceite CA-RF-02.01.04 | Dado cliente com visita aberta, quando inativado, então sai da seleção para novos check-ins e a visita existente pode ser encerrada e consultada |
| Base | F25, DEC-F34. Tratamento de operação em curso PROPOSTO |

### RF-02.01.05 — Corrigir identidade do cliente

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Master, CNPJ/identificação afetada, justificativa e referência do cadastro |
| Validações | CNPJ válido e único. Manter mesma entidade somente quando a ação corrige erro de cadastro. Mudança real de estabelecimento requer novo cadastro, proposta a validar |
| Fluxo | Master revisa impacto, informa motivo e grava retificação auditada |
| Exceções | Colisão com outro cadastro exige decisão humana. Versões de propostas apresentadas conservam snapshots originais |
| Aceite CA-RF-02.01.05 | Dado erro identificado, quando Master retifica, então o histórico conserva os dois valores, responsável e motivo, e os documentos emitidos preservam seu conteúdo |
| Base | F14/F25. Detalhamento PROPOSTO |

### RF-02.02 — Criar conta de funcionário

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Master, nome, e-mail, perfil e situação de D-01 |
| Validações | Identidade única e perfil da lista fixa. Provisionamento protegido de acesso conforme PT-01 |
| Fluxo | Master cadastra, sistema cria identidade individual e orienta procedimento de acesso |
| Exceções | E-mail já existente ou dados inválidos mantêm cadastro sem duplicação. Cadastro de Promotor sem veículo exige vinculação antes de novas visitas |
| Aceite CA-RF-02.02 | Dado funcionário novo, quando Master cria conta, então existe uma identidade individual com papel definido. A tentativa pelo Escritório é recusada |
| Base | F11/F14/F25, DEC-F35 |

### RF-02.03.01 — Cadastrar fornecedor

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, D-03 |
| Validações | Nome obrigatório e prevenção de duplicidade operacional |
| Fluxo | Registrar fornecedor ativo para associação a clientes, pedidos e campanhas |
| Exceções | Duplicidade sugere consultar fornecedor existente. Cadastro não homologa automaticamente um layout |
| Aceite CA-RF-02.03.01 | Dado fornecedor novo, quando salvo, então pode ser associado às operações e seu processamento de arquivos depende dos layouts homologados |
| Base | F01 RF-02, F25 |

### RF-02.03.02 — Editar fornecedor

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, nome e identificação de D-03 |
| Validações | Revisão atual e unicidade operacional. Preservar ID e documentos já emitidos |
| Fluxo | Atualizar dados e registrar histórico |
| Exceções | Conflito exige recarregar. Mudança de identidade real exige revisão humana |
| Aceite CA-RF-02.03.02 | Dado fornecedor existente, quando nome é corrigido, então vínculos continuam no mesmo ID e versões anteriores preservam seus snapshots |
| Base | F14/F25 |

### RF-02.03.03 — Consultar fornecedor

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório/Master. Promotores consultam identificação vinculada às campanhas/métricas autorizadas |
| Validações | Filtrar situação e nome conforme contexto e alcance |
| Fluxo | Pesquisar e selecionar fornecedor em operação permitida |
| Exceções | Inativo permanece em histórico e é retirado de novas seleções operacionais |
| Aceite CA-RF-02.03.03 | Dado fornecedor ativo, quando Escritório prepara solicitação, então pode selecioná-lo. Identificações históricas continuam acessíveis após inativação |
| Base | F01 RF-02, F25 |

### RF-02.03.04 — Inativar fornecedor

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, fornecedor e motivo proposto |
| Validações | Preservar histórico e vínculos. Operações já apresentadas precisam manter encaminhamento humano |
| Fluxo | Confirmar INATIVO e registrar evento |
| Exceções | Novas operações requerendo fornecedor ativo são recusadas. Ações de conclusão de processos existentes são preservadas |
| Aceite CA-RF-02.03.04 | Dado fornecedor com pedidos anteriores, quando inativado, então pedidos e evidências continuam consultáveis e ele sai da seleção para novas solicitações |
| Base | F25, DEC-F34 |

### RF-02.04.01 — Associar cliente a fornecedor

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, cliente_id e fornecedor_id de D-03 |
| Validações | Referências existentes e par único. Vários fornecedores por cliente |
| Fluxo | Adicionar/remover associação operacional, com histórico de vigência quando afetar operações |
| Exceções | Associação repetida conserva um vínculo. Remoção mantém fatos históricos |
| Aceite CA-RF-02.04.01 | Dado cliente com Wega, quando outro fornecedor é associado, então ambos os vínculos existem e uma tentativa repetida não cria duplicata |
| Base | F25, DEC-F34 |

### RF-02.04.02 — Manter vínculo fixo promotor–veículo

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Master, promotor, veículo e início de vigência de D-04 |
| Validações | Promotor/veículo válidos, um vínculo vigente por promotor, veículo exclusivo desse promotor e tratamento de visita aberta conforme D-04 |
| Fluxo | Criar ou substituir vínculo, encerrando a vigência anterior e preservando histórico |
| Exceções | Veículo sem referência externa sinaliza pendência de integração. Veículo já vinculado a outro promotor não pode receber segundo vínculo vigente. Vínculo concorrente exige recarregar |
| Aceite CA-RF-02.04.02 | Dado Promotor vinculado ao veículo A, quando Master muda para B, então eventos futuros usam B e registros anteriores conservam A. Tentativa de associar B simultaneamente a outro promotor é recusada |
| Base | F23/F25/F35, DEC-F31/F35/F48. Exclusividade aprovada em F35. Procedimento de troca PROPOSTO |

