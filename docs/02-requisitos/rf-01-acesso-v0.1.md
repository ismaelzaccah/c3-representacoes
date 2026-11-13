# RF-01 — Acesso e contas

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Escopo MVP, prioridade P0 em todos os itens. Bases F01 RF-01, F13/F14/F25 e DEC-F16/F17/F35. Regras de atores estão aprovadas. PT-01/PT-02, proteção de última conta Master e procedimentos de recuperação são detalhes PROPOSTOS. Aplicam-se CT-01–CT-08, D-01 e D-13. FL-01 representa o fluxo geral de autorização.

### RF-01.01 — Autenticar conta

| Aspecto | Especificação proposta |
|---|---|
| Ator e campos | Todos os perfis, e-mail e senha de D-01 |
| Validações | Conta ativa, identidade válida, limites de tentativa de RNF-01. Credencial informada tratada pelo provedor de autenticação escolhido |
| Fluxo | Informar dados, validar no servidor, emitir sessão e abrir área permitida pelo perfil |
| Exceções | Conta inválida/inativa ou credencial incorreta recebe erro genérico. Falha de serviço preserva estado não autenticado e oferece nova tentativa |
| Aceite CA-RF-01.01 | Dada conta ativa e credencial válida, quando autenticar, então acessar somente as ações do perfil. Com credencial inválida, sessão não é emitida e a mensagem não expõe detalhes da conta |
| Fonte e estado | F01 RF-01. Base aprovada, detalhamento PROPOSTO |

### RF-01.02 — Encerrar sessão

| Aspecto | Especificação proposta |
|---|---|
| Ator e campos | Usuário autenticado, sessão atual |
| Validações | Identificar sessão vigente. Repetição produz resultado consistente |
| Fluxo | Solicitar logout, invalidar sessão no servidor e retornar à entrada |
| Exceções | Sessão já encerrada retorna à entrada. Falha de comunicação exige confirmação posterior do estado pelo servidor |
| Aceite CA-RF-01.02 | Dada sessão ativa, quando logout for confirmado, então reutilizar sua credencial de sessão em operação protegida resulta em acesso recusado |
| Fonte e estado | F01 RF-01. Detalhamento PROPOSTO |

### RF-01.03 — Autorizar ação e registro

| Aspecto | Especificação proposta |
|---|---|
| Ator e campos | Servidor em toda operação, perfil, situação da conta, ação, recurso e campos enviados |
| Validações | Conferir matriz de permissões. Uma ação não concedida é recusada. Parâmetro de promotor/veículo informado pelo cliente não altera o alcance autorizado |
| Fluxo | Validar sessão, verificar ação/registro/campos, executar somente dentro do alcance permitido |
| Exceções | Sessão expirada exige autenticação. Ação proibida, ID de outro usuário ou campo reservado resulta em recusa sem alteração |
| Aceite CA-RF-01.03 | Dado Promotor, quando enviar diretamente pedido de edição de cliente ou ID de visita de outro promotor, então recusar. Escritório não acessa a gestão de contas mesmo por chamada direta |
| Fonte e estado | F13/F14/F25/F27, matriz de permissões da versão. Detalhamento PROPOSTO |

### RF-01.04.01 — Desativar conta

| Aspecto | Especificação proposta |
|---|---|
| Ator e campos | Master, conta-alvo e motivo administrativo proposto |
| Validações | Proteger última conta Master ativa. Verificar pendências da conta e preservar autoria de fatos |
| Fluxo | Master confirma desativação, sistema altera situação e revoga sessões. Pendências operacionais são exibidas para regularização |
| Exceções | Contas inativas mantêm estado. Conflito de revisão exige recarregar. Último Master é protegido conforme D-01 |
| Aceite CA-RF-01.04.01 | Dada conta com visitas/pedidos anteriores, quando desativada, então perde acesso e seu nome permanece nos registros históricos |
| Fonte e estado | F14 e DEC-F17. Base aprovada, detalhamento PROPOSTO |

### RF-01.04.02 — Ativar conta

| Aspecto | Especificação proposta |
|---|---|
| Ator e campos | Master, conta e perfil vigente |
| Validações | Identidade única e perfil válido. Promotor precisa de vínculo ativo para iniciar novas visitas, conforme D-01/D-04 |
| Fluxo | Confirmar ativação, salvar situação e permitir próxima autenticação |
| Exceções | Cadastro inconsistente mostra campos a regularizar. Nenhuma sessão anterior é restaurada automaticamente |
| Aceite CA-RF-01.04.02 | Dada conta inativa regularizada, quando ativada, então autenticação válida usa o perfil atual e os vínculos vigentes |
| Fonte e estado | F01 RF-01, F14. Detalhamento PROPOSTO |

### RF-01.05.01 — Ajustar conta de funcionário

| Aspecto | Especificação proposta |
|---|---|
| Ator e campos | Master, nome, e-mail, perfil e situação de D-01. Criação está em RF-02.02 e vínculo de veículo em RF-02.04.02 |
| Validações | E-mail único, perfil da enumeração fixa e controle de última conta Master. Alteração de perfil revoga sessões para reaplicar acesso |
| Fluxo | Carregar revisão atual, alterar campos, justificar mudança sensível e gravar com auditoria |
| Exceções | Conflito de e-mail, perda da última conta administrativa ou revisão antiga impede salvar |
| Aceite CA-RF-01.05.01 | Dada conta Promotor, quando Master altera seu perfil, então a próxima operação usa as novas permissões e o histórico identifica autor, data e mudança |
| Fonte e estado | F11/F13/F14. Base aprovada, detalhamento PROPOSTO |

### RF-01.05.02 — Ajustar configurações reservadas

| Aspecto | Especificação proposta |
|---|---|
| Ator e campos | Master, parâmetros explicitamente permitidos na configuração aprovada. Lista inicial proposta inclui motivos de visita e identificação administrativa de contatos da C3 |
| Validações | Parâmetro deve pertencer à lista aprovada e respeitar tipo/limite. Alteração estrutural de política ou escopo segue governança |
| Fluxo | Master edita parâmetro existente, sistema valida e registra nova revisão. Dados históricos preservam seus valores originais |
| Exceções | Parâmetro desconhecido ou tentativa de conceder permissão arbitrária é recusado |
| Aceite CA-RF-01.05.02 | Dado parâmetro aprovado, quando Master altera, então novos usos adotam a nova revisão e consultas históricas preservam seu significado. Escritório recebe recusa |
| Fonte e estado | F13/F14. Capacidade reservada aprovada, lista de parâmetros PROPOSTA e PENDENTE de revisão |

### RF-01.05.03 — Recuperar acesso de forma assistida

| Aspecto | Especificação proposta |
|---|---|
| Ator e campos | Master, conta-alvo e confirmação de identidade administrativa |
| Validações | Utilizar mecanismo protegido do provedor escolhido. Segredos são geridos pela solução de autenticação |
| Fluxo | Master inicia procedimento documentado de recuperação, confirma conclusão e revoga sessões antigas |
| Exceções | Falha na confirmação de identidade ou indisponibilidade do provedor mantém conta sem alteração |
| Aceite CA-RF-01.05.03 | Dada recuperação concluída, quando credencial antiga/sessão anterior for usada, então acesso é recusado, enquanto a credencial válida permite nova sessão |
| Fonte e estado | F01 RF-01, RNF-01. PROPOSTO como detalhamento de autenticação, procedimento depende da arquitetura |
