# Matriz de rastreabilidade MVP/Pós-MVP

Status PROPOSTO • ESF-C3-0.2 • 10/11/2026.

A [ESF-C3-0.3](especificacao-funcional-v0.3.md) é a entrada corrente. As tabelas de base abaixo preservam a descoberta e a versão 0.1. As alterações de atores, alcance, permissões e novos grupos estão no adendo 0.2 e na retirada 0.3 e prevalecem nos IDs afetados. Esta matriz preserva os IDs da descoberta e aponta suas folhas detalhadas. A [matriz da Etapa 1 v0.21](../00-governanca/historico/matriz-requisitos-etapa-1-v0.21.md) conserva a referência histórica.

| ID preservado | Requisito de origem | Folhas detalhadas | Módulo | Fontes | Escopo |
|---|---|---|---|---|---|
| RF-01.01 | Autenticar usuário por login | RF-01.01 | [Detalhe](rf-01-acesso-v0.1.md) | F01 RF-01 | MVP |
| RF-01.02 | Encerrar sessão no logout | RF-01.02 | [Detalhe](rf-01-acesso-v0.1.md) | F01 RF-01 | MVP |
| RF-01.03 | Aplicar autorização no servidor aos atores Escritório e Promotores e ao perfil reservado Master | RF-01.03 | [Detalhe](rf-01-acesso-v0.1.md) | F08 D04; F11/F13 | MVP |
| RF-01.04 | Ativar e desativar contas de funcionários, inclusive no desligamento | RF-01.04.01, RF-01.04.02 | [Detalhe](rf-01-acesso-v0.1.md) | F01 RF-01; F11/F14; DEC-F17 | MVP |
| RF-02.01 | Cadastrar, consultar e ajustar cliente por estabelecimento com CNPJ único e campos básicos aprovados | RF-02.01.01, RF-02.01.02, RF-02.01.03, RF-02.01.04, RF-02.01.05 | [Detalhe](rf-02-cadastros-v0.1.md) | F01 RF-02; F25; DEC-F32/F33/F34 | MVP |
| RF-02.02 | Cadastrar contas de funcionários, incluindo promotores | RF-02.02 | [Detalhe](rf-02-cadastros-v0.1.md) | F01 RF-02; F11 | MVP |
| RF-02.03 | Cadastrar e manter fornecedores e sua situação ativa/inativa | RF-02.03.01, RF-02.03.02, RF-02.03.03, RF-02.03.04 | [Detalhe](rf-02-cadastros-v0.1.md) | F01 RF-02; F25; DEC-F34 | MVP |
| RF-02.04 | Manter associações cliente–fornecedor e vínculo fixo promotor–veículo | RF-02.04.01, RF-02.04.02 | [Detalhe](rf-02-cadastros-v0.1.md) | F01 RF-02; F23/F25; DEC-F33–F35; F35/DEC-F48 | MVP |
| RF-03.01 | Consultar e selecionar qualquer cliente cadastrado para visita | RF-03.01 | [Detalhe](rf-03-visitas-v0.1.md) | F01 RF-03; F25; DEC-F33 | MVP |
| RF-03.02 | Registrar check-in com data/hora do sistema, cliente e promotor, com uma visita aberta por promotor | RF-03.02 | [Detalhe](rf-03-visitas-v0.1.md) | F01 RF-03; F18; DEC-F26/F29 | MVP |
| RF-03.03 | Registrar check-out com data/hora do sistema na visita aberta | RF-03.03 | [Detalhe](rf-03-visitas-v0.1.md) | F01 RF-03; F18; DEC-F26/F29 | MVP |
| RF-03.04 | Registrar e ajustar motivo e observações básicas enquanto a visita estiver aberta | RF-03.04 | [Detalhe](rf-03-visitas-v0.1.md) | F01 RF-03; F18; DEC-F27/F28 | MVP |
| RF-03.05 | Consultar seus próprios registros de visitas anteriores | RF-03.05 | [Detalhe](rf-03-visitas-v0.1.md) | F01 RF-03; F25; DEC-F33 | MVP |
| RF-03.06 | Acompanhar visitas administrativamente | RF-03.06 | [Detalhe](rf-03-visitas-v0.1.md) | F01 RF-03 | MVP |
| RF-03.07 | Aplicar regras de visita aberta, edição, horários e falhas. Master regulariza visita encerrada/esquecida com justificativa e histórico | RF-03.07.01 | [Detalhe](rf-03-visitas-v0.1.md) | F01 RF-03; F18; DEC-F26–F29 | MVP |
| RF-04.01 | Registrar solicitação de campanha com cliente, fornecedor e responsável | RF-04.01 | [Detalhe](rf-04-campanhas-v0.1.md) | F01 RF-04; F26; DEC-F36 | MVP |
| RF-04.02 | Registrar aprovação ou rejeição externa do fornecedor | RF-04.02 | [Detalhe](rf-04-campanhas-v0.1.md) | F01 RF-04; F26; DEC-F37 | MVP |
| RF-04.03 | Anexar um ou mais folders à campanha | RF-04.03 | [Detalhe](rf-04-campanhas-v0.1.md) | F01 RF-04; F26; DEC-F37 | MVP |
| RF-04.04 | Definir vários clientes-alvo e início/fim da vigência | RF-04.04 | [Detalhe](rf-04-campanhas-v0.1.md) | F01 RF-04; F26; DEC-F36/F37 | MVP |
| RF-04.05 | Exibir campanhas aprovadas com folder e dentro da vigência ao selecionar cliente-alvo | RF-04.05 | [Detalhe](rf-04-campanhas-v0.1.md) | F01 RF-03/04; F25/F26; DEC-F37 | MVP |
| RF-04.06 | Consultar histórico e estados de campanhas, preservando solicitações e decisões | RF-04.06 | [Detalhe](rf-04-campanhas-v0.1.md) | F01 RF-04; F26; DEC-F37/F39 | MVP |
| RF-04.07 | Retirar campanha vencida das ativas e permitir cancelamento pelo Escritório com motivo | RF-04.07.01, RF-04.07.02 | [Detalhe](rf-04-campanhas-v0.1.md) | F26; DEC-F39 | MVP |
| RF-05.01 | Registrar manualmente solicitação com cliente e fornecedor | RF-05.01 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05 | MVP |
| RF-05.02 | Anexar arquivos originais da solicitação | RF-05.02 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05 | MVP |
| RF-05.03 | Importar layouts homologados, com Wega como fonte atualmente disponível | RF-05.03.01, RF-05.03.02 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05; F09/F16; DEC-F21 | MVP |
| RF-05.04 | Gerar cotação PDF com código e Grupo como descrição, QTD, UNIT direto da planilha, TOTAL e MULTI | RF-05.04.01, RF-05.04.02 | [Detalhe](rf-05-pedidos-v0.1.md) | F10/F11/F15/F16; DEC-F20 | MVP |
| RF-05.05 | Criar nova versão quando o cliente solicitar alteração, preservando a anterior | RF-05.05 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05; F17; DEC-F24 | MVP |
| RF-05.06 | Registrar decisão do cliente, data, responsável e anexo de mensagem, print ou e-mail do canal de origem | RF-05.06 | [Detalhe](rf-05-pedidos-v0.1.md) | F08/F17; DEC-F23/F25 | MVP |
| RF-05.07 | Registrar revisão humana interna pelo Escritório | RF-05.07 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05; F17; DEC-F22/F24 | MVP |
| RF-05.08 | Registrar autorização interna do Escritório vinculada à versão | RF-05.08 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05; F17; DEC-F22/F24 | MVP |
| RF-05.09 | Registrar manualmente envio ao fornecedor | RF-05.09 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05 | MVP |
| RF-05.10 | Registrar resultado do pedido externo | RF-05.10 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05 | MVP |
| RF-05.11 | Preservar histórico de alterações e responsáveis | RF-05.11 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05 | MVP |
| RF-05.12 | Definir eventual arquivo específico para fornecedor | RF-05.12 | [Detalhe](rf-05-pedidos-v0.1.md) | F01 RF-05 | CONDICIONAL DP-06 |
| RF-06.01 | Cadastrar e manter veículo com placa, identificação e referência externa do rastreador | RF-06.01.01, RF-06.01.02 | [Detalhe](rf-06-abastecimentos-v0.1.md) | F01 RF-02/06; F25; DEC-F35 | MVP |
| RF-06.02 | Registrar abastecimento com veículo, data, hodômetro, litros e valor total obrigatórios | RF-06.02 | [Detalhe](rf-06-abastecimentos-v0.1.md) | F01 RF-06; F27; DEC-F40/F41 | MVP |
| RF-06.03 | Consultar histórico e totais de abastecimentos | RF-06.03.01, RF-06.03.02 | [Detalhe](rf-06-abastecimentos-v0.1.md) | F01 RF-06; F27; DEC-F40 | MVP |
| RF-06.04 | Corrigir abastecimento salvo com justificativa e histórico | RF-06.04 | [Detalhe](rf-06-abastecimentos-v0.1.md) | F27; DEC-F42 | MVP |
| RF-06.05 | Registrar abastecimento retroativo com data real e justificativa | RF-06.05 | [Detalhe](rf-06-abastecimentos-v0.1.md) | F27; DEC-F43 | MVP |
| RF-07.01 | Consultar pedidos e aprovações no painel | RF-07.01 | [Detalhe](rf-07-consultas-v0.1.md) | F01 RF-07 | MVP |
| RF-07.02 | Filtrar consultas por período, cliente, promotor, fornecedor, veículo e situação, conforme a operação | RF-07.02 | [Detalhe](rf-07-consultas-v0.1.md) | F01 RF-07; F28; DEC-F45 | MVP |
| RF-07.03 | Apresentar contagens de visitas abertas/encerradas, pedidos por situação/fornecedor, campanhas por situação/vigência e totais de abastecimentos por veículo/período | RF-07.03.01, RF-07.03.02, RF-07.03.03, RF-07.03.04 | [Detalhe](rf-07-consultas-v0.1.md) | F01 RF-07; F28; DEC-F44 | MVP |
| RF-07.04 | Exportar em Excel listagens filtradas de visitas, pedidos, campanhas e abastecimentos | RF-07.04.01, RF-07.04.02, RF-07.04.03, RF-07.04.04 | [Detalhe](rf-07-consultas-v0.1.md) | F28; DEC-F46 | MVP |
| RF-01.05 | Gerenciar contas, configurações e correções excepcionais | RF-01.05.01, RF-01.05.02, RF-01.05.03 | [Detalhe](rf-01-acesso-v0.1.md) | F13/F14; DEC-F17 | MVP |
| RF-03.08 | Criar avisos internos vinculados a cliente e período e exibi-los ao selecionar o cliente | RF-03.08.01, RF-03.08.02 | [Detalhe](rf-03-visitas-v0.1.md) | F08/F26; DEC-F38 | MVP |
| RF-05.13 | Usar PRODUTO e QTD no lançamento aprovado no sistema do fornecedor, como Wega, para realizar pedido e faturamento | RF-05.13 | [Detalhe](rf-05-pedidos-v0.1.md) | F08 D02; F11; DEC-F15 | FRONTEIRA EXTERNA |
| RF-07.05 | Mostrar valor comprado no período e data da última compra por cliente/fornecedor com origem em planilha Excel | RF-07.05.01, RF-07.05.02, RF-07.05.03 | [Detalhe](rf-07-consultas-v0.1.md) | F08/F28; DEC-F47 | MVP |
| RF-03.09 | Obter posição do veículo fixo do promotor pela API do rastreador nos eventos de check-in/out | RF-03.09 | [Detalhe](rf-03-visitas-v0.1.md) | F19/F23; DEC-F30/F31; MC-01 | MVP |

## Requisitos não funcionais

| ID | Referência corrente | Fonte | Critério |
|---|---|---|---|
| RNF-01 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-01 |
| RNF-02 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-02 |
| RNF-03 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-03 |
| RNF-04 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-04 |
| RNF-05 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-05 |
| RNF-06 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-06 |
| RNF-07 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-07 |
| RNF-08 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-08 |
| RNF-09 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-09 |
| RNF-10 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-10 |
| RNF-11 | [Metas e ensaios](requisitos-nao-funcionais-v0.1.md) | F01 §7 e referências específicas | CA-RNF-11 |

## Classificação histórica da base e exclusões preservadas

| ID | Tema | Classificação | Fonte | Condição |
|---|---|---|---|---|
| PM-01 | Captura automática de WhatsApp/e-mail, interpretação por IA e download automático | Pós-MVP/candidato | F01 RF-05; F02 F7:O10 | Validar integração, acesso, dados e fluxo humano |
| PM-02 | Consulta a portais e envio automático de pedido via site/API | Pós-MVP/candidato | F01 RF-05; F02 F20:H25 | Exigir evidência técnica; “TALVEZ” não comprova integração |
| PM-03 | Importação genérica e saídas para todos os layouts de fornecedores | Fora do MVP; universalidade não prometida | F01 RF-05 | Avaliar cada novo layout, sem promessa de formato universal |
| PM-04 | Catálogo mestre permanente de produtos, preços e estoque | Fora do MVP; sem demanda aprovada | F01 RF-02/05 | Nova decisão de produto; linhas históricas de proposta não formam catálogo |
| PM-05 | GPS contínuo, trajetos e KM rodado | Pós-MVP/candidato | F01 RF-03/06; F03 A44:A45 | Justificativa, privacidade e análise técnica próprias |
| PM-06 | Metas, ranking, projeções e BI avançado | Pós-MVP/candidato | F01 RF-03/07; F02 F45:F53 | Definir indicadores, fontes e objetivo |
| PM-07 | Notificações externas e regras de primeira/última visita | Pós-MVP/candidato | F01 RF-03/04; F03 E3, A39:A41 | Nova aprovação; 8h–8h20, 17h30 e 500 m não são regras aprovadas do MVP |
| PM-08 | Áudio, IA na visita e tarefas/lembretes completos | Pós-MVP/candidato | F01 RF-03; F03 A36 | Validar necessidade, custo e privacidade |
| PM-09 | Solicitação automática de campanha e leitura automática de resposta | Pós-MVP/candidato | F01 RF-04; F02 E12:M15 | Avaliar integração e controles por fornecedor |
| PM-10 | Pagamentos automatizados, investimento e premiação avançados | Pós-MVP/candidato | F01 RF-04; F02 E12:M15, F28:I29 | Definir regras e responsabilidades sem presumir módulo financeiro |
| PM-11 | Trajetos, consumo por trajetos e manutenção de frota | Pós-MVP/candidato | F01 RF-06; F19 | A consulta pontual à API do rastreador foi solicitada em F19 e está em RF-03.09/MC-01 |
| PM-12 | Brindes, sell-out, despesas gerais, bônus e rotinas comerciais adicionais | Pós-MVP/candidato | F02 F31:I34, F37:H53; F01 §§3/6 | Descoberta própria; presença em planilha não amplia MVP |
| PM-13 | Editor complexo de permissões individuais | FORA DO MVP | F01 RF-01; F11 | Gestão de contas está coberta por RF-01.05. Eventual editor dinâmico exige demanda própria |

## Controles de cobertura

48 IDs funcionais de origem preservados, desdobrados em 73 folhas. Onze RNFs, treze registros de escopo PM e seis fluxos FL compõem o pacote. A classificação condicional de RF-05.12 e a fronteira externa RF-05.13 são preservadas. RF-03.09 decorre da mudança MC-01 já registrada.

As fontes de cada regra estão nas folhas e no registro de fontes. PT-01–08 são detalhes novos PROPOSTO. DP-01–06 são dependências abertas. P0/P1 ordenam o trabalho sem retirar itens do MVP. Critérios dependentes de layout/material só poderão ser fechados após a evidência correspondente.

## Alterações da versão corrente ESF-C3-0.2

[Adendo MC-02/MC-03](alteracoes-escopo-v0.2.md) atualiza Admin/Escritório/Promotores, UF, cadastro, ficha compartilhada, horários/distâncias, cobrança de números e escopo pretendido ampliado. [Permissões 0.2](../03-fluxos-permissoes/matriz-permissoes-v0.2.md) substituem a matriz anterior nos pontos afetados.

| Grupos de origem | Situação corrente |
|---|---|
| PM-05/11 | Trajetos e quilômetros do veículo entram no escopo pretendido RF-11. GPS contínuo do celular e manutenção de frota conservam classificação própria |
| PM-06 | Metas e performance entram em RF-08. BI preditivo e projeções não definidas dependem de decisão específica |
| PM-07/08 | Regras aprovadas de primeira/última, tarefas, dicas e IA passam ao escopo pretendido. Canais, cadência e integrações exigem detalhamento |
| PM-12 | Despesas adicionais e números comerciais passam a RF-10/RF-07.06. Rotinas de bônus/brindes avançadas não são inferidas |
| PM-10/13 | Pagamentos automatizados, premiação financeira e editor complexo de permissões continuam pendentes de demanda/aprovação específica |

A base continua com 48 IDs de origem e 73 folhas históricas. O adendo acrescenta 21 unidades de detalhamento no escopo pretendido. Contagem não substitui a revisão de escopo e contrato.

## Revisão corrente ESF-C3-0.3

F47 e [MC-04](alteracoes-ux-escopo-v0.3.md) retiram RF-12.01–03, dicas, áudio do módulo e funcionalidades de IA de todo o produto. DP-10 está cancelada. A parcela de IA de PM-01/08 também é retirada. Permanecem os IDs históricos para rastreabilidade. Das 21 unidades adicionais da versão 0.2, 18 permanecem no escopo pretendido e três estão retiradas. Os demais estados e dependências conservam sua classificação.

| ID | Estado corrente | Fonte | Referência |
|---|---|---|---|
| RF-12.01 | RETIRADO | F47 | MC-04 |
| RF-12.02 | RETIRADO | F47 | MC-04 |
| RF-12.03 | RETIRADO | F47 | MC-04 |
| UX-03.01–07 | Direção aprovada, detalhamento PROPOSTO | F47 | Adendo 0.3 e UX-C3-0.3 |

As [permissões 0.3](../03-fluxos-permissoes/matriz-permissoes-v0.3.md) e a [especificação 0.3](especificacao-funcional-v0.3.md) têm precedência sobre o histórico acima.

## Ajustes específicos de F54

O primeiro filtro foi desfeito e a base funcional retorna à ESF-C3-0.3. Os [ajustes de cadastro e interface 0.5](ajustes-cadastro-interface-v0.5.md) acrescentam CPF para Escritório/Promotores e placa do veículo para Promotor, relacionados a RF-01.05/RF-02.02/RF-02.04.02. A retirada da página Metas e as mudanças de cards estão registradas como alterações da interface solicitadas em F54.
