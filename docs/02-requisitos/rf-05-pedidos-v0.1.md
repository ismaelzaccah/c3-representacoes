# RF-05 — Solicitações, cotação e pedidos

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Ator operacional Escritório, com acesso geral do Master. Campos D-08–D-11, convenções CT, fluxo FL-05 e matriz de permissões integram cada requisito. P0 identifica controles essenciais, P1 os demais fluxos MVP. Toda gravação identifica autor, instante e versão. Detalhes de campos e transições são PROPOSTO, com bases aprovadas indicadas nas fontes.

### RF-05.01 — Registrar solicitação manualmente

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, cliente, fornecedor, canal WhatsApp/e-mail, data recebida, descrição e responsável D-08 |
| Validações | Cliente/fornecedor ativos. Uma solicitação por fornecedor é proposta para manter autorização e saída inequívocas |
| Fluxo | Informar origem, selecionar vínculos e salvar rascunho com identificador |
| Exceções | Vínculo ausente impede gravação. Repetição usa CT-03 |
| Aceite CA-RF-05.01 | Dada origem informada, quando salva, então solicitação possui autor, vínculos e estado de rascunho consultáveis |
| Prioridade/fonte | MVP P1, F01 RF-05, F17 |

### RF-05.02 — Vincular arquivos originais

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, solicitação e arquivo D-11 |
| Validações | RNF-04, associação autorizada e conteúdo válido. Tipos propostos PDF/JPG/PNG até 10 MB, XLSX conforme PT-04 |
| Fluxo | Enviar, validar e associar original à solicitação preservando conteúdo |
| Exceções | Falha de envio mantém indicação de pendência e permite repetir sem substituir silenciosamente o anterior |
| Aceite CA-RF-05.02 | Dado arquivo aceito, quando consultado por pessoa autorizada, então conteúdo corresponde ao original e vínculo identifica solicitação e autor |
| Prioridade/fonte | MVP P1, F01 RF-05, PT-04 |

### RF-05.03.01 — Validar entrada Wega

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, arquivo e fornecedor Wega. A código, C Grupo/descrição, E mínimo e G preço líquido da Sheet1 |
| Validações | Cabeçalhos homologados, código não vazio/único no lote, mínimo e preço numéricos válidos. Quantidade inteira e UNIT até seis casas são PT-03. Demais colunas preservadas apenas no original |
| Fluxo | Receber lote, conferir estrutura e apresentar resultado com linhas válidas/erros antes de confirmar |
| Exceções | Layout divergente ou linha inválida bloqueia publicação integral, informando linha/campo. Arquivo de outro fornecedor exige homologação DP-02 |
| Aceite CA-RF-05.03.01 | Dada amostra F09, quando validada, então 3.839 linhas são reconhecidas com os quatro campos mapeados. Código duplicado, preço inválido e cabeçalho divergente são recusados em amostras de teste |
| Prioridade/fonte | MVP P0, F09/F16, DEC-F20/F21 |

### RF-05.03.02 — Publicar lote para cotação

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, lote validado, finalidade e confirmação D-11 |
| Validações | Publicação integral e idempotente. Mesmo arquivo/finalidade não duplica lote publicado. Cotação conserva referência à origem utilizada |
| Fluxo | Confirmar lote validado e disponibilizar linhas para compor cotação |
| Exceções | Falha parcial mantém lote indisponível. Nova fonte não altera preços/descrições de versões anteriores. Sem formação de catálogo mestre permanente |
| Aceite CA-RF-05.03.02 | Dado lote validado, quando publicação é repetida após perda de resposta, então existe uma única publicação e versões anteriores conservam seus preços |
| Prioridade/fonte | MVP P0, F01 RF-05, F09/F16, CT-03/04, PT-03 |

### RF-05.04.01 — Gerar cotação PDF por versão

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, versão, linhas código/Grupo, QTD, UNIT, TOTAL e MULTI D-09 |
| Validações | QTD positiva e maior ou igual ao mínimo, sem exigir múltiplo. UNIT vem de G sem ajuste comercial presumido. TOTAL decimal QTD × UNIT com três casas. Half-up e soma dos totais arredondados são PT-03 |
| Fluxo | Selecionar linhas do lote homologado, quantidades, conferir e gerar PDF identificado por solicitação/versão |
| Exceções | Quantidade abaixo do mínimo impede concluir. Falha na geração permite repetir com o mesmo conteúdo. IPI/ICMS existentes na origem não viram acréscimo presumido |
| Aceite CA-RF-05.04.01 | Dado mínimo 6, quando QTD é 7, então aceita. QTD 5 é recusada. Para outro item com mínimo 1, UNIT 1,2345 e QTD 1, TOTAL proposto é 1,235. PDF mostra código e Grupo e mantém os valores da versão |
| Prioridade/fonte | MVP P0, F10/F11/F15/F16, DEC-F20, DP-05 |

### RF-05.04.02 — Registrar apresentação ao cliente

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, versão/PDF e data/canal de apresentação |
| Validações | PDF concluído e versão atual. Registro manual de comunicação externa |
| Fluxo | Operador entrega PDF pelo canal de origem e registra apresentação |
| Exceções | Falha na comunicação externa mantém apresentação pendente |
| Aceite CA-RF-05.04.02 | Dado PDF pronto, quando Escritório confirma apresentação, então histórico identifica versão, canal, autor e data |
| Prioridade/fonte | MVP P1, F01 RF-05, F17. Registro detalhado PROPOSTO |

### RF-05.05 — Criar nova versão

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, versão anterior, linhas alteradas e motivo |
| Validações | Numeração sequencial por solicitação. Conteúdo anterior, decisões e autorização permanecem históricos |
| Fluxo | Criar rascunho sucessor. Apresentar alteração e coletar decisões referentes à nova versão. Nova revisão/autorização obrigatórias após mudança |
| Exceções | Versão concorrente exige recarregar. Depois de envio externo, retificação segue PT-08 e requer tratar efeitos externos manualmente |
| Aceite CA-RF-05.05 | Dada versão autorizada, quando quantidade muda, então nova versão não herda liberação de envio e a autorização anterior continua atribuída à versão anterior |
| Prioridade/fonte | MVP P1, F17, DEC-F24. Nova aprovação do cliente para conteúdo alterado é detalhamento PROPOSTO |

### RF-05.06 — Registrar resposta do cliente

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, versão, aprovação/alteração/rejeição, data, autor e evidência do WhatsApp/e-mail. Motivo e decisão de revisar/encerrar na rejeição |
| Validações | Evidência obrigatória vinculada à versão apresentada, sem promover automaticamente mensagem externa a decisão |
| Fluxo | Conferir resposta externa, anexar evidência e registrar decisão. Alteração abre sucessor RF-05.05. Rejeição recebe encaminhamento do Escritório |
| Exceções | Resposta de versão antiga permanece histórica e não libera versão atual. Falta de evidência impede concluir decisão |
| Aceite CA-RF-05.06 | Dada rejeição, quando registrada com evidência e motivo, então histórico mostra revisão ou encerramento escolhido e bloqueia autorização dessa versão rejeitada |
| Prioridade/fonte | MVP P1, F08/F17, DEC-F23/F25 |

### RF-05.07 — Revisar internamente

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, versão, resultado LIBERAR/AJUSTAR e observações D-10 |
| Validações | Conferir produtos, quantidades, preço, mínimo, cálculo e resposta vinculada. Resultado pertence à revisão atual |
| Fluxo | Conferir versão, registrar resultado e manter autoria. AJUSTAR retorna à correção e nova versão quando altera conteúdo apresentado |
| Exceções | Dados alterados durante revisão impedem usar liberação obsoleta |
| Aceite CA-RF-05.07 | Dada revisão AJUSTAR, quando tenta autorizar, então bloqueia até revisão liberada da versão atual |
| Prioridade/fonte | MVP P0, F17, DEC-F22/F24 |

### RF-05.08 — Autorizar versão

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, versão atual e confirmação de autorização |
| Validações | Aprovação do cliente com evidência, revisão LIBERAR e versão inalterada. Mesmo funcionário pode revisar e autorizar |
| Fluxo | Registrar autorização com usuário, instante e versão exata |
| Exceções | Rejeição/alteração pendente ou revisão anterior bloqueiam. Repetição da mesma confirmação não duplica autorização |
| Aceite CA-RF-05.08 | Dada versão aprovada e revisada, quando o revisor a autoriza, então autorização é aceita. Qualquer mudança posterior exige nova revisão/autorização |
| Prioridade/fonte | MVP P0, F17, DEC-F22/F24 |

### RF-05.09 — Registrar envio manual ao fornecedor

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, versão autorizada, data e referência/protocolo quando disponível |
| Validações | Versão atual autorizada. Operador confirma realização externa |
| Fluxo | Realizar lançamento externo RF-05.13 e registrar envio |
| Exceções | Falha no portal permanece pendente. Repetição de registro não significa reenviar pedido externo |
| Aceite CA-RF-05.09 | Dada versão sem autorização, quando tenta registrar envio, então bloqueia. Com autorização, registra operador e versão enviada |
| Prioridade/fonte | MVP P1, F01 RF-05, F11/F17 |

### RF-05.10 — Registrar resultado externo

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Escritório, envio, resultado ACEITO/REJEITADO/PENDENTE proposto, data e referência externa |
| Validações | Resultado vinculado ao envio/versionamento. Correção pós-envio segue PT-08 |
| Fluxo | Conferir retorno do fornecedor e registrar manualmente |
| Exceções | Sem retorno mantém pendência. Pedido aceito não alimenta automaticamente compras faturadas |
| Aceite CA-RF-05.10 | Dado envio, quando retorno é registrado, então consulta identifica resultado e referência e indicador de compras permanece dependente do Excel faturado |
| Prioridade/fonte | MVP P1, F01 RF-05, F28, PT-08 |

### RF-05.11 — Preservar trilha de decisões

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Sistema, eventos D-13 ligados à solicitação/versão |
| Validações | Alteração e auditoria consistentes CT-04, sem apagar autoria anterior |
| Fluxo | Registrar criação, alteração, apresentação, resposta, revisão, autorização e envio/resultados |
| Exceções | Falha em registrar evento obrigatório impede confirmar alteração correspondente |
| Aceite CA-RF-05.11 | Dado histórico com duas versões, quando consultado pelo Escritório/Master, então cada decisão referencia conteúdo, autor e momento correspondentes |
| Prioridade/fonte | MVP P0, F01 RF-05, F17 |

### RF-05.12 — Delimitar eventual arquivo específico de fornecedor

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Responsável pelo projeto/C3, layout, exemplo, regras e aceite de inclusão DP-06 |
| Validações | Dependência contratual. Formato não definido pela referência visual de cotação |
| Fluxo | Receber layout, avaliar e submeter inclusão com impactos e critério específico |
| Exceções | Ausência de material mantém PENDENTE e não gera promessa de exportador universal |
| Aceite CA-RF-05.12 | Dado layout recebido, quando avaliado, então anexo identifica fornecedor, formato, validações e inclusão aprovada antes de assumir entrega |
| Prioridade/fonte | CONDICIONAL P0, F01 RF-05, F11, DP-06 |

### RF-05.13 — Lançamento no sistema do fornecedor

| Aspecto | Especificação proposta |
|---|---|
| Ator/campos | Operador externo do Escritório, PRODUTO e QTD da versão autorizada |
| Validações | Fronteira operacional externa. Identificação de produto deve corresponder ao código aprovado |
| Fluxo | Operador acessa sistema do fornecedor, como Wega, e lança somente os dados necessários PRODUTO/QTD. Registra resultado em RF-05.09/10 |
| Exceções | Divergência no fornecedor requer conferência humana e eventual nova versão. Faturamento externo depende do fornecedor |
| Aceite CA-RF-05.13 | Dada versão autorizada, quando operador realiza lançamento, então os produtos/quantidades usados correspondem à versão e registro interno identifica o envio |
| Prioridade/fonte | FRONTEIRA EXTERNA, F08/F11. Automação classificada em PM-02 |

