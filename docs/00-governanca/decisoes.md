# Registro de decisões

Status do documento PROPOSTO • Versão 0.26 • 10/11/2026.

As decisões registram aprovações e esclarecimentos de F01 a F46. A versão corrente é ESF-C3-0.2, com alterações recentes identificadas nos registros DEC-F49–F58. As linhas históricas preservam a rastreabilidade. As regras comerciais correntes são DEC-C16–C22, conforme F30/F31. Vencimento por fechamento de competência substitui a referência anterior de quinto dia útil.

| ID | Domínio | Decisão registrada | Estado da decisão / fonte | Consequência e limite |
|---|---|---|---|---|
| DEC-01 | Funcional | MVP híbrido; registrar operações externas sem presumir executá-las | APROVADO NA ORIGEM / F01 §5 | Automações existentes não serão substituídas automaticamente |
| DEC-F02 | Funcional | Plataforma web responsiva, mobile-first, até dez usuários iniciais | APROVADO NA ORIGEM / F01 §4 | Compatibilidade e metas de desempenho ainda exigem definição |
| DEC-F03 | Funcional | Perfis iniciais Administrador, Escritório e Promotor, com autorização no servidor | PARCIALMENTE SUPERADA por DEC-F07/F08 / F01 RF-01; F08 | Inclusão de Master e diretriz de Administradores/Promotores recebidas. Destino de Escritório pendente |
| DEC-F04 | Funcional | Pedidos com revisão humana interna e registro de autorização | APROVADO NA ORIGEM / F01 RF-05; complementada por DEC-F09 | F08 atribui revisão e autorização aos administradores. Efeito de nova versão ainda pendente |
| DEC-F05 | Funcional | Sem catálogo permanente próprio; importação limitada a layouts homologados e proposta em modelo aprovado | APROVADO NA ORIGEM / F01 RF-02/05 | Quantidade de layouts e regras pendentes em D01/D02 |
| DEC-F06 | Funcional | Preservar exclusões expressas do MVP | APROVADO NA ORIGEM / F01 §6; F07 | Referências visuais/planilhas não adicionam escopo |
| DEC-A01 | Arquitetural | Avaliar prioritariamente a stack indicada em F01, antes de aprová-la | APROVADO NA ORIGEM como diretriz de avaliação / F01 §8 | Não há framework, versão, licença ou serviço tecnicamente homologado |
| DEC-A02 | Arquitetural | Preferir monólito modular, sem microserviços inicialmente | APROVADO NA ORIGEM como preferência / F01 §8 | Topologia final e hospedagem ainda não foram decididas |
| DEC-A03 | Arquitetural/UX | Liberdade de identidade visual e framework, priorizando produtividade, acessibilidade e consistência | APROVADO NA ORIGEM como diretriz / F01 §§3/13 | Artifact não fixa identidade ou componentes |
| DEC-C01 | Comercial | Implantação R$ 24.000: R$ 12.000 no fechamento e R$ 12.000 no aceite do MVP | APROVADO NA ORIGEM / F01 §10; F07 | Não converter preço em capacidade de horas de implantação |
| DEC-C02 | Comercial | Evolução R$ 8.000/mês, 80 h/mês; modalidades 3, 6 ou 12 meses, mesmo preço mensal | APROVADO NA ORIGEM / F01 §10; F07, complementado por F29/DEC-C13 | F29 coloca a implantação na capacidade de 80 h mensais de Ismael. Competências e contabilização comercial em D14 |
| DEC-C03 | Comercial | As 80 h incluem análise, planejamento, desenvolvimento, testes, documentação, reuniões e manutenção evolutiva; registrar horas mensalmente | APROVADO NA ORIGEM / F01 §10 | Saldo, horas extras e suporte pendentes; demandas extras exigem orçamento/autorização |
| DEC-C04 | Comercial | Correções cobertas pela garantia não consomem franquia de evolução | APROVADO NA ORIGEM / F01 §10, complementado por F30/DEC-C18 | Garantia comercial durante a contratação mensal. Detalhar atendimento e cobertura na etapa contratual |
| DEC-C05 | Comercial | Referência original de primeira mensalidade 30 dias após contratação e demais no quinto dia útil | SUPERADA por F30/F31 e DEC-C16/C20 | Regra corrente inicia serviço mensal após o ciclo do MVP, por competências contadas do início e pagas no fechamento |
| DEC-C06 | Comercial | Previsão de 30 dias corridos e avaliação de viabilidade nos primeiros cinco dias úteis | APROVADO NA ORIGEM / F01 §9, complementado por DEC-C12/F12 | Marcos esclarecidos em D13. Capacidade e viabilidade permanecem em análise |
| DEC-C07 | Comercial | Cliente dispõe de cinco dias úteis para homologar entregas formalmente apresentadas | APROVADO NA ORIGEM / F01 §11, complementado por DEC-C12/F12 | Janela inicia após apresentação formal para testes. Critérios de aceite serão vinculados aos requisitos aprovados |
| DEC-C08 | Comercial/governança | Ajustes de escopo, preço ou prazo dependem de aprovação bilateral; sem redução unilateral | APROVADO NA ORIGEM / F01 §§9/11 | Exige solicitação de mudança com descrição, impacto e estimativa |
| DEC-C09 | Comercial | Expediente de segunda a sexta, exceto feriados nacionais, do Ceará e Fortaleza, além de 24/12, 31/12 e 02/01 | APROVADO NA ORIGEM / F01 §9 | Prazo segue em dias corridos; calendário concreto depende do marco |
| DEC-G01 | Governança | Uma especificação versionada, IDs únicos e histórico de decisões | APROVADO NA ORIGEM / F01 §14 | Matriz corrente evoluirá para especificação; documentos derivados referenciam sua versão |
| DEC-G02 | Governança | Originais preservados e `fontes-cliente` fora do Git | APROVADO NA ORIGEM / F01 §§3/15; F07 item 1 | Sem alterações nas planilhas ou regra de exclusão |
| DEC-G03 | Governança | Autorizar apenas Etapa 1 e seus sete produtos; todos PROPOSTO; interromper antes da Etapa 2 | APROVADO NA ORIGEM / F07 | Não implementar, instalar, publicar ou enviar materiais |
| DEC-C10 | Comercial/contratual | Sistema específico destinado à C3 conforme contrato; reservar reutilizáveis genéricos; portfólio depende de autorização escrita | APROVADO NA ORIGEM como diretriz / F01 §12 | Delimitação de titularidade, infraestrutura e componentes exige instrumento e revisão jurídica |
| DEC-C11 | Comercial/contratual | Minuta e cláusula de evolução durante eventual atraso devem passar por revisão jurídica antes de assinatura | APROVADO NA ORIGEM como encaminhamento / F01 §§10/12/13 | Não constitui parecer jurídico nem aprovação de redação contratual |

## Atualizações funcionais expressas de 09/11/2026

| ID | Decisão recebida | Estado e fonte | Efeito e pendência residual |
|---|---|---|---|
| DEC-F07 | Master com acesso total, CRUD de perfis e controle/ajuste de ferramentas e configurações de funcionários | APROVADO como diretriz em F08, esclarecido por DEC-F14/F11 | CRUD significa gestão de contas pelo gerente geral. Ferramentas/configurações ainda requerem detalhamento |
| DEC-F08 | Administradores com acesso dos promotores e acesso geral, exceto gestão de contas e ferramentas de configuração de funcionários | APROVADO como diretriz em F08, complementado por F11 | Nome Escritório mantido. Sua relação com o perfil Administradores e permissões específicas requer confirmação |
| DEC-F09 | Administradores realizam revisão e autorização. Cliente comunica aprovação, alteração ou rejeição no canal de origem, WhatsApp ou e-mail | APROVADO pelo responsável em F08 | RF-05.06–08 atualizados. Ainda definir evidência manual, efeito de nova versão e sequência após rejeição |
| DEC-F10 | Proposta ao cliente segue referência com PRODUTO, QTD, UNIT, TOTAL e MULTI | APROVADO em F08/F10, complementado por DEC-F13/F11 | MULTI tem regra de mínimo esclarecida. Mapeamento, cálculos e formato final pendentes |
| DEC-F11 | Após aprovação, modelo de lançamento contém PRODUTO e QTD | APROVADO em F08, complementado por DEC-F15/F11 | Destino é o sistema do fornecedor. Layout de arquivo específico, quando necessário, depende de homologação |
| DEC-F12 | Promotores visualizam gastos de combustível, campanhas, avisos de visita e métricas sobre compras do cliente | NECESSIDADE EXPRESSA pelo responsável em F08 | Combustível detalha acesso existente. Avisos e métricas são acréscimos frente à baseline F01. Registrar conteúdo, origem, alcance e impacto em prazo/escopo antes de compromisso contratual detalhado |

### Esclarecimentos complementares recebidos em F11

| ID | Decisão esclarecida | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-F13 | MULTI é quantidade mínima. Com MULTI igual a 6, quantidade 7 é permitida | APROVADO pelo responsável em F11, 09/11/2026 | Documentar validação QTD ≥ MULTI. Regra de quantidade inteira/fracionada e mapeamento da entrada ainda dependem de detalhamento |
| DEC-F14 | CRUD de perfis corresponde à gestão de contas de funcionários pelo gerente geral/Master, incluindo criação e exclusão de contas. Nome Escritório pode ser mantido | APROVADO pelo responsável em F11, 09/11/2026 | RF-01.04/05 e RF-02.02 atualizados. Definir tratamento da exclusão com preservação de autoria/histórico. Relação de Escritório com Administradores permanece pendente |
| DEC-F15 | PRODUTO e QTD são lançados no sistema do fornecedor, como Wega, para realizar o pedido e faturar | APROVADO pelo responsável em F11, 09/11/2026 | Define o destino da entrada reduzida. Pedido, resultado externo e eventual faturamento devem permanecer distinguíveis nos registros |

As necessidades de avisos e métricas de F08 aguardam detalhamento e avaliação de impacto. F11 esclarece o controle de contas previsto para Master. PM-13 segue como exclusão de editor complexo de permissões na baseline.

## Propostas e decisões ainda não tomadas

### Fechamento comercial em F31

| ID | Decisão | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-C20 | Competência mensal contada da data de início do serviço de suporte/evolução, com vencimento no fechamento do ciclo trabalhado | APROVADO pelo responsável em F31, 10/11/2026 | Resolve calendário geral de D14. Exemplo de referência, início no dia 15 e fechamento do ciclo no dia 14 seguinte. A convenção para meses de tamanhos diferentes será detalhada no instrumento |
| DEC-C21 | Suporte por WhatsApp e e-mail, de segunda a sexta-feira, das 9h às 17h | APROVADO pelo responsável em F31, 10/11/2026 | Registrar expediente em horário de Fortaleza e exclusões de dias já previstas em F01. Prazos por severidade e responsabilidades de operação serão especificados posteriormente |
| DEC-C22 | Rescisão ao fim da competência em que se completarem os 30 dias de aviso, mediante pagamento final de R$ 8.000, sem multa adicional, inclusive nas modalidades de 3/6/12 meses | CONFIRMADO pelo responsável em F31, 10/11/2026 | Completa DEC-C19 e resolve a intenção comercial de saída. Detalhar rito e obrigações de encerramento no contrato sujeito à revisão jurídica |

D14 e D15 estão RESOLVIDAS quanto às decisões comerciais gerais. F31 complementa os registros históricos de F30. A redação das condições, cobertura da garantia e procedimentos de encerramento será preparada na etapa contratual prevista no plano.

### Condições comerciais recebidas em F30

| ID | Decisão ou intenção comercial | Estado e fonte | Efeito e esclarecimento restante |
|---|---|---|---|
| DEC-C16 | Receber R$ 12.000 pré-MVP e R$ 12.000 pós-MVP. Depois iniciar o primeiro mês de suporte/adição de funcionalidades, remunerado por R$ 8.000 após o mês trabalhado | APROVADO pelo responsável em F30, 10/11/2026 | Serviços mensais sucedem a implantação. Confirmar ciclos de competência e vencimento no mês seguinte |
| DEC-C17 | Horas mensais não utilizadas expiram. A intenção é utilizar integralmente as 80 h em demandas priorizadas | APROVADO pelo responsável em F30, 10/11/2026 | Registrar uso mensal e atividades. Planejar o trabalho segundo a capacidade informada |
| DEC-C18 | Garantia comercial de correção de defeitos enquanto estiver vigente a contratação mensal de R$ 8.000 | INFORMADO pelo responsável em F30, 10/11/2026 | Correções cobertas seguem DEC-C04, com atendimento e cobertura a detalhar na minuta sujeita a revisão jurídica |
| DEC-C19 | Rescisão mediante comunicação prévia de 30 dias, conclusão do mês contratado e pagamento final de R$ 8.000 | DIRETRIZ RECEBIDA em F30, 10/11/2026 | Confirmar alinhamento dos 30 dias ao fim da competência e existência de multa adicional nas modalidades de 3, 6 e 12 meses |

F30 esclareceu a sequência temporal entre implantação e contratação mensal, usando a capacidade informada em F29. F31 completou competência, vencimento, suporte e rescisão em DEC-C20–C22. A redação contratual será preparada posteriormente, com revisão jurídica conforme F01.

### Equipe, homologação e custos definidos em F29

| ID | Decisão ou informação | Estado e fonte | Efeito e dependência |
|---|---|---|---|
| DEC-C13 | Ismael Zaccah executará o desenvolvimento, incluindo implantação, dentro da capacidade informada de 80 h mensais | INFORMADO pelo responsável em F29, 10/11/2026 | Substitui a hipótese de capacidade de implantação separada. Estimar todas as atividades contra esse limite. D14 definirá competências remuneradas e contabilização da implantação/evolução |
| DEC-C14 | Caio Costa, proprietário da C3, valida requisitos, testa entregas e formaliza aceite | CONFIRMADO em F29, 10/11/2026 | Resolve o responsável principal de D16. Disponibilidade e canais formais serão combinados no planejamento |
| DEC-C15 | C3/Caio Costa arca com domínio, hospedagem/nuvem e demais custos recorrentes, incluindo futuros serviços de IA | APROVADO pelo responsável em F29, 10/11/2026 | Apresentar alternativas e custos para aprovação antes de contratar. Futuras funções de IA seguem o roadmap e as decisões específicas |
| DEC-A04 | Hospedagem/nuvem serão criadas no projeto. O domínio `costaltda.com` é hipótese decorrente do e-mail da C3. Volumes atuais desconhecidos e crescimento esperado | INFORMADO em F29, 10/11/2026 | Confirmar domínio, acesso, titularidade e orçamento. Dimensionar cenários de carga com premissas explícitas antes de fixar metas de escala e custo |

Os valores são R$ 24.000 de implantação e R$ 8.000 mensais. F29 define capacidade de 80 h/mês. F30/F31 definem que o serviço mensal começa após o ciclo do MVP, em competências pagas no fechamento. O prazo de 30 dias segue com viabilidade técnica pendente, considerando capacidade e integrações/arquivos identificados.

### Indicadores e exportações aprovados em F28

| ID | Decisão | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-F44 | Indicadores de visitas abertas/encerradas por período, cliente e promotor. Contagem de pedidos por situação/fornecedor e campanhas por situação/vigência. Totais de litros/gastos por veículo/período | APROVADO pelo responsável em F28, 10/11/2026 | Definir fórmulas e recortes completos conforme acesso aprovado de cada operação |
| DEC-F45 | Filtros por período, cliente, promotor, fornecedor, veículo e situação, conforme consulta | APROVADO pelo responsável em F28, 10/11/2026 | Aplicar os filtros pertinentes a cada listagem e aos indicadores |
| DEC-F46 | Exportar em Excel as listagens filtradas de visitas, pedidos, campanhas e abastecimentos | APROVADO pelo responsável em F28, 10/11/2026 | Layouts e campos de cada saída serão especificados. A exportação respeita permissões e recorte da consulta |
| DEC-F47 | Métricas de compras incluem valor comprado no período e data da última compra por cliente/fornecedor. A origem é planilha Excel | APROVADO pelo responsável em F28, 10/11/2026 | Obter amostra e definir layout, identificação de cliente/fornecedor, data e valor das compras, periodicidade, duplicidade e ajustes na homologação da fonte |

D10 está RESOLVIDA quanto ao conjunto geral de indicadores, formatos de saída e tipo da fonte de compras. A planilha de compras ainda aguarda amostra. O tratamento de alimentação/atualização será detalhado com base no layout e nas definições do dado. A amostra de tabela de produtos Wega F09 possui finalidade diferente da fonte de compras faturadas informada em F28.

### Abastecimentos aprovados em F27

| ID | Decisão | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-F40 | Promotor registra abastecimentos do veículo fixo e consulta seu histórico/gastos. Escritório registra para qualquer veículo. Escritório e Master têm visão geral | APROVADO pelo responsável em F27, 10/11/2026 | Define responsáveis e alcance de acesso em RF-06.02/03 |
| DEC-F41 | Veículo, data, hodômetro, litros e valor total obrigatórios. Litros/valor positivos e hodômetro coerente com a sequência cronológica do veículo | APROVADO pelo responsável em F27, 10/11/2026 | Especificar validações com exemplos de lançamento atual e retroativo |
| DEC-F42 | Correção de abastecimento salvo é feita por Master com justificativa e histórico | APROVADO pelo responsável em F27, 10/11/2026 | Preservar responsável, momento e conteúdo das alterações |
| DEC-F43 | Escritório pode lançar abastecimento retroativo com data real e justificativa | APROVADO pelo responsável em F27, 10/11/2026 | Validações de hodômetro respeitam a sequência cronológica, incluindo registros anteriores e posteriores |

D09 está RESOLVIDA quanto às regras gerais. Os campos de abastecimento serão preenchidos no processo aprovado. A integração de localização nas visitas mantém seu escopo em RF-03.09/MC-01. O próximo bloco é D10.

### Campanhas e avisos aprovados em F26

| ID | Decisão | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-F36 | Escritório e Promotores podem solicitar campanha. Cada campanha pertence a um fornecedor e pode atender vários clientes-alvo | APROVADO pelo responsável em F26, 10/11/2026 | Registrar cliente, fornecedor e responsável. Vários promotores podem consultar a campanha do cliente-alvo |
| DEC-F37 | Escritório registra aprovação/rejeição recebida do fornecedor, anexa um ou mais folders e informa início/fim da vigência. Campanha aprovada, com folder e dentro da vigência aparece como ativa ao selecionar cliente-alvo | APROVADO pelo responsável em F26, 10/11/2026 | Exibição e consulta administrativas respeitam estado, período e vínculos aprovados |
| DEC-F38 | Escritório cria avisos internos vinculados a cliente e período de exibição, apresentados aos promotores ao selecionar o cliente | APROVADO pelo responsável em F26, 10/11/2026 | Resolve a regra funcional de RF-03.08. Campos e limites serão detalhados na especificação |
| DEC-F39 | Fim da vigência retira campanha da lista de ativas e preserva histórico. Escritório pode cancelar campanha com motivo registrado | APROVADO pelo responsável em F26, 10/11/2026 | Cancelamento e término da vigência preservam a rastreabilidade da solicitação e das decisões |

D08 está RESOLVIDA quanto às regras gerais. Tipos e tamanhos de folders, campos e cenários de borda serão detalhados na especificação. O bloco seguinte é D09, abastecimentos.

### Cadastros aprovados com ressalva em F25

| ID | Decisão | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-F32 | Cadastro de cliente por estabelecimento e CNPJ único, com nome/razão social, CNPJ, endereço, cidade e UF obrigatórios. Bairro, CEP, telefone, contato e e-mail complementares | APROVADO pelo responsável em F25, 10/11/2026 | Detalhar campos e validações na especificação |
| DEC-F33 | Todos os promotores podem consultar e selecionar qualquer cliente cadastrado para visita | APROVADO COM RESSALVA pelo responsável em F25, 10/11/2026 | Substitui a proposta de carteira exclusiva. Cada visita preserva o vínculo com o promotor que a realizou |
| DEC-F34 | Escritório cadastra e ajusta dados de rotina de clientes/fornecedores, mantém associações cliente–fornecedor e pode inativá-los preservando histórico | APROVADO pelo responsável em F25, 10/11/2026 | Um cliente pode estar associado a vários fornecedores. Promotor consulta e seleciona clientes. Correções excepcionais seguem com Master |
| DEC-F35 | Escritório mantém cadastro de veículos. Master mantém contas de funcionários e o vínculo fixo promotor–veículo | APROVADO pelo responsável em F25, 10/11/2026 | Veículo inclui placa, identificação e referência externa do rastreador. Conta inclui nome, e-mail, perfil e situação |

D07 está RESOLVIDA quanto às regras gerais. A ressalva de F25 altera o acesso aos clientes. A regra proposta de consulta aos próprios registros de visita é preservada. Compartilhamento do cadastro de clientes e histórico de autoria são tratados nos respectivos requisitos.

### Localização de veículo aprovada com ressalva em F19

| ID | Decisão | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-F30 | Localização pontual de check-in/out será fornecida pela API do rastreador do veículo da empresa usado pelo promotor. Escritório/Master consultam os registros. Falha de localização permite justificativa e conferência | APROVADO COM RESSALVA pelo responsável em F19, 09/11/2026 | Origem substitui a proposta de localização do aparelho do promotor. Identificar vínculo vigente promotor/veículo, limite de idade, validade e disponibilidade da posição. MC-01 registra alteração da baseline de F01 RF-06 |

D06 está RESOLVIDA quanto às regras operacionais por F23 e DEC-F31. F22 informa credenciais já disponíveis ao responsável. A configuração protegida, a homologação autenticada e a estimativa de impacto da integração permanecem atividades técnicas. O [levantamento da API](../04-arquitetura/levantamento-api-rastreador.md) reúne essas dependências.

### Vínculo e atualidade aprovados em F23

| ID | Decisão | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-F31 | Cada promotor usa veículo fixo. A posição do rastreador pode ter até cinco minutos de idade no evento de check-in/out. Posição acima do limite permite registro com justificativa e marcação para conferência | APROVADO pelo responsável em F23, 10/11/2026 | Complementa DEC-F30 e resolve D06 funcionalmente. Preservar o veículo e o horário da posição usados no evento. Homologar os limites com posição atual, de cinco minutos e superior a cinco minutos |

### Visitas aprovadas em F18

| ID | Decisão | Estado e fonte | Requisitos relacionados |
|---|---|---|---|
| DEC-F26 | Cada promotor mantém uma visita aberta por vez. Check-in e check-out recebem data e hora do sistema | APROVADO pelo responsável em F18, 09/11/2026 | RF-03.02/03/07 |
| DEC-F27 | Promotor pode ajustar motivo e observações durante a visita aberta | APROVADO pelo responsável em F18, 09/11/2026 | RF-03.04/07 |
| DEC-F28 | Master corrige ou regulariza visita encerrada ou esquecida, com justificativa e histórico que preserva os registros originais | APROVADO pelo responsável em F18, 09/11/2026 | RF-03.07; RNF-03 |
| DEC-F29 | O sistema confirma o registro após recebê-lo e salvá-lo. Na falha de conexão, apresenta aviso e permite nova tentativa | APROVADO pelo responsável em F18, 09/11/2026 | RF-03.02/03/07; RNF-11 |

D05 está RESOLVIDA quanto às cinco regras apresentadas. Cenários de repetição de operações e demais exceções serão detalhados na especificação com essas decisões como base. Localização pontual permanece em D06 para decisão própria.

### Revisão e autorização de pedidos aprovadas em F17

| ID | Decisão | Estado e fonte | Requisitos relacionados |
|---|---|---|---|
| DEC-F22 | A mesma pessoa do Escritório pode revisar e autorizar um pedido | APROVADO pelo responsável em F17, 09/11/2026 | RF-05.07/08 |
| DEC-F23 | Registrar decisão do cliente, data, responsável pelo registro e anexo da mensagem, print ou e-mail recebido pelo canal de origem | APROVADO pelo responsável em F17, 09/11/2026 | RF-05.06/11 |
| DEC-F24 | Solicitação de alteração do cliente gera nova versão, preservando a anterior. Mudança da proposta após autorização exige nova revisão e autorização | APROVADO pelo responsável em F17, 09/11/2026 | RF-05.05/07/08 |
| DEC-F25 | Na rejeição, Escritório registra o motivo e decide entre revisar a proposta ou encerrar a solicitação | APROVADO pelo responsável em F17, 09/11/2026 | RF-05.06/07 |

D03 está RESOLVIDA. As decisões complementam DEC-F04/F09/F16. As autorizações e evidências serão vinculadas à versão correspondente, com preservação do histórico. Exemplos e cenários de teste serão preparados no detalhamento autorizado posteriormente.

### Fornecedores e proposta definidos em F15

| ID | Decisão | Estado e fonte | Efeito e complemento |
|---|---|---|---|
| DEC-F18 | A amostra LISTA COMPLETA ELETROPARTS.xlsx pertence à Wega. O MVP terá layouts de entrada próprios de cada fornecedor | APROVADO pelo responsável em F15, 09/11/2026 | Delimitar fornecedores e variantes e obter amostras para homologação individual. Apenas a amostra Wega foi recebida até esta atualização |
| DEC-F19 | Proposta ao cliente em PDF. PRODUTO contém código e descrição. UNIT vem diretamente do preço da planilha | APROVADO pelo responsável em F15, 09/11/2026 | Complementa DEC-F10. Identificar origem da descrição na entrada Wega e definir fórmula, precisão e arredondamento de TOTAL |

DEC-F18/F19 foram complementadas por F16. A regra corrente de totalização e o tratamento das fontes futuras estão registrados em DEC-F20/F21.

### Descrição, precisão e futuras fontes esclarecidas em F16

| ID | Decisão | Estado e fonte | Efeito e detalhamento |
|---|---|---|---|
| DEC-F20 | Na proposta Wega, PRODUTO contém código e descrição obtida de Grupo. TOTAL = QTD × UNIT, arredondado para três casas decimais | APROVADO pelo responsável em F16, 09/11/2026 | Registro usa três casas após a vírgula, por exemplo R$ 12,345. Na homologação, validar dados de entrada, saída e casos de arredondamento |
| DEC-F21 | Apenas a fonte Wega está disponível atualmente. Próximos fornecedores serão incluídos conforme aceite contratual e poderão ter planilhas, PDFs ou procedimentos para obter dados no site | DIRETRIZ RECEBIDA em F16, 09/11/2026 | Identificar por fornecedor material, processo, tratamento manual/automatizado, esforço e inclusão contratual. Coleta em site poderá continuar externa no MVP híbrido. Cada nova capacidade depende de análise e definição de escopo |

A necessidade de obter dados em site pode envolver uma atividade humana externa seguida de arquivo homologado. Extração de PDF e obtenção automática em portal são capacidades distintas que requerem definição expressa quando as fontes forem apresentadas. O contrato deverá explicitar o conjunto inicial e o processo para incorporar os demais fornecedores.

### Consolidação de atores e perfil de gerenciamento em F13

| ID | Decisão | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-F16 | Dois atores operacionais, Escritório e Promotores. Master é perfil reservado à administração do sistema, com permissões elevadas, criação de contas, ajustes de dados de clientes/funcionários e visão geral | APROVADO pelo responsável em F13, 09/11/2026 | Escritório assume as funções operacionais antes atribuídas a Administradores, incluindo revisão e autorização de pedidos. Master concentra gestão de contas e ajustes exclusivos. Definir campos/ações reservados no detalhamento de D04 |

A nomenclatura anterior Administradores fica registrada nas decisões históricas. A documentação corrente usa Escritório para esse conjunto de atribuições operacionais. A criação de contas de funcionários é exclusiva do Master, conforme F11/F13. O detalhamento dos ajustes exclusivos de clientes e funcionários deve explicitar quais alterações o Escritório pode realizar.

### Divisão de responsabilidades aprovada em F14

| ID | Decisão | Estado e fonte | Efeito |
|---|---|---|---|
| DEC-F17 | Escritório realiza cadastros e ajustes da rotina. Master concentra gestão de contas, configurações e correções excepcionais. Alterações preservam histórico de autoria. Funcionário desligado tem conta desativada, com nome e vínculos preservados nos registros anteriores | APROVADO pelo responsável em F14, 09/11/2026 | Complementa DEC-F14/F16. O desligamento passa a usar desativação. A classificação detalhada de ações/campos seguirá a divisão aprovada, com exemplos para revisão na especificação |

F14 aprova a divisão geral apresentada. Os exemplos de correção de CNPJ, troca de responsável e ferramentas de configuração ainda serão classificados no detalhamento. O histórico registra responsável e momento da alteração, conforme requisitos de rastreabilidade.

### Marcos de prazo aprovados em F12

| ID | Decisão | Estado e fonte | Consequência |
|---|---|---|---|
| DEC-C12 | Os 30 dias corridos começam após o aceite da proposta e a assinatura do contrato, quando ambas as condições estiverem atendidas. O prazo termina na disponibilização formal do MVP para homologação, opção A | APROVADO pelo responsável em F12, 09/11/2026 | Após apresentação formal, a C3 dispõe de cinco dias úteis para homologar. Aceite e segunda parcela seguem vinculados à aprovação do MVP. A avaliação de viabilidade dos primeiros cinco dias úteis integra a janela de desenvolvimento |

Data concreta do marco será registrada quando os eventos ocorrerem. D13 está RESOLVIDA quanto à escolha dos marcos. Viabilidade técnica e capacidade seguem tratadas no planejamento.

| ID | Tema | Estado | Encaminhamento |
|---|---|---|---|
| DEC-P01 | Sequência de entrevistas, prioridades e participantes sugeridos | PROPOSTO | Responsável valida roteiro e interlocutores; nenhum contato realizado |
| DEC-P02 | Detalhamento da matriz corrente e classificação de candidatos Pós-MVP | PROPOSTO | Validar após respostas; não implica inclusão contratual |
| DEC-P03 | Stack, autenticação, versões, hospedagem, arquivos e níveis de serviço | PENDENTE | Avaliar posteriormente com compatibilidade, licenças, custos e riscos |
| DEC-P04 | Quantidade de layouts, proposta, aprovação, acesso e marco temporal | PARCIALMENTE ESCLARECIDO / F08–F12 | D13 resolvida por DEC-C12. Complementos de D01–D04 seguem no registro de pendências |

## Registro de novas decisões

Usar: ID, domínio, estado, contexto, alternativas consideradas, decisão, fonte/evidência, aprovador, data, consequências, requisitos e pendências afetados. Para substituir uma decisão aprovada, criar novo registro com referência ao anterior e aprovação expressa. Não preencher aprovador ou data por suposição.

## Autorização e propostas da Etapa 2

| ID | Domínio | Decisão e estado | Fonte | Consequência |
|---|---|---|---|---|
| DEC-G04 | Governança | APROVADO iniciar Etapa 2 de especificação funcional | F32, 10/11/2026 | Atualiza a pausa registrada em DEC-G03. Mantém preservação, escopo e trabalho documental |
| DEC-P05 | Especificação | PROPOSTO pacote ESF-C3-0.1, PT-01–08, campos, limites, fluxos, permissões e RNFs | Derivação de F01–F34 e decisões aprovadas | Revisão conjunta pelo responsável, dependências DP-01–06. Autorizar a etapa não aprova automaticamente os detalhes novos |

A especificação corrente está em [ESF-C3-0.1](../02-requisitos/especificacao-funcional-v0.1.md). O [relatório da Etapa 2](../06-planejamento/situacao-etapa-2.md) reúne decisões para revisão e materiais prioritários.

## Atualização de planejamento — F35/F36

| ID | Domínio | Estado e decisão | Fonte | Consequência |
|---|---|---|---|---|
| DEC-F48 | Funcional | APROVADO veículo exclusivo do promotor | F35, 10/11/2026 | Vínculo fixo é único também por veículo vigente. Histórico das trocas permanece preservado. Atualiza D-04/RF-02.04.02 na ESF-C3-0.1 revisão 1 |
| DEC-G05 | Governança | APROVADO continuar planejamento enquanto chegam materiais | F36, 10/11/2026 | Preparar arquitetura e dimensionamento preliminares. Os detalhes propostos da ESF e da arquitetura continuam sujeitos à revisão |
| DEC-P06 | Arquitetura/planejamento | PROPOSTO ARQ-C3-0.1 e estimativa remanescente de 134–388 h, cenário mais provável 240 h antes de reserva | Derivação da ESF e F37 | Revisão de Ismael, provas técnicas e materiais necessários para consolidar. Conflito preliminar com 30 dias/80 h exige decisão de viabilização pertinente |

Os ADR-001–009 detalham propostas arquiteturais em [registro próprio](../04-arquitetura/decisoes-arquiteturais-v0.1.md). O [relatório da Etapa 3](../06-planejamento/situacao-etapa-3.md) apresenta esforço, capacidade e revisões necessárias. Não há alteração automática de condição comercial ou escopo pela estimativa.


## Orientação para a proposta e continuidade de UX

| ID | Domínio | Estado e decisão | Fonte | Consequência |
|---|---|---|---|---|
| DEC-C23 | Comercial/planejamento | APROVADO levar o conflito de prazo à proposta para negociação dos requisitos funcionais dentro do prazo estipulado | F38, 10/11/2026 | Manter risco explícito e preparar opções rastreáveis. O recorte final dependerá de aprovação bilateral. Nenhum requisito foi retirado por esta orientação |
| DEC-G06 | Governança | APROVADO continuar para os protótipos após arquitetura preliminar | F38, 10/11/2026 | Produzir UX-C3-0.1 com telas PROPOSTO e dados fictícios |
| DEC-UX01 | Experiência de uso | PROPOSTO UX-C3-0.1, navegação por perfil, hierarquia mobile-first e direção visual azul | Derivação da ESF-C3-0.1 revisão 1 | Revisão de Ismael/Caio. Marca gráfica, conteúdo final do PDF e detalhes pendentes continuam em revisão |

## Revisão após referência do cliente — ESF-C3-0.2

| ID | Decisão | Estado / fonte | Efeito |
|---|---|---|---|
| DEC-G07 | Analisar referência C3 e ajustar o protótipo, aproveitando funcionalidades, organização, nomes e marca com prioridade móvel | APROVADO F40 | UX-C3-0.2 derivado, documentação PROPOSTO e fontes preservadas |
| DEC-F49 | Admin assume gestão antes chamada Master, com Escritório e Promotores formando três atores | APROVADO F41 | Substitui a nomenclatura anterior na especificação corrente, sem alterar autoria histórica |
| DEC-F50 | Promotor acessa clientes pelos estados de atuação | APROVADO F42 | Substitui a concessão geral de F25/DEC-F33 nesse alcance. Cliente não se torna exclusivo de um promotor dentro da região |
| DEC-F51 | Histórico da equipe é compartilhado na ficha do cliente permitido | APROVADO F42 | Histórico pessoal continua por autoria. Ficha regional mostra outros promotores identificados |
| DEC-F52 | Promotor cadastra e atualiza contato/endereço/linhas de clientes da região | APROVADO F43 | Amplia responsabilidade de rotina. Retificação excepcional de identidade preserva tratamento reservado |
| DEC-F53 | Metas, performance, tarefas, despesas adicionais, trajetos/Waze e IA integram o escopo pretendido | APROVADO como direção em F42 | MC-02 registra ampliação. Detalhamento, estimativa e compromisso contratual pendentes |
| DEC-F54 | Trajetos e quilômetros terão origem no rastreador do veículo | APROVADO F43 | Upcar precisa de prova para histórico de rotas/quilômetros. Navegação Waze tem finalidade própria |
| DEC-F55 | Adotar regras de visitas 8/12 por dia, primeira 8h–8h20, última após 17h30, residência 500 m, cliente 70 m e motivo da terceira visita semanal | APROVADO F44 | Limites passam ao escopo pretendido. Georreferência e exceção de contas-chave a detalhar |
| DEC-F56 | Promotor envia números comerciais e é responsável por cobrá-los em cada visita | APROVADO F44 | Região, autoria, original e atualização devem ser preservados. Ausência de retorno requer detalhamento |
| DEC-F57 | Primeira visita fora da janela permitida com justificativa e aviso ao Admin | APROVADO F45 | Horário real preservado, exceção identificada e destinatário definido |
| DEC-C24 | Escopo pretendido ampliado terá prazo a renegociar | APROVADO F42 | Atualiza encaminhamento de DEC-C23 à luz da ampliação. Valores registrados não mudam automaticamente. Esforço anterior não dimensiona novos grupos |
| DEC-UX02 | Organização e gráficos da referência, marca original e fluxo de pedidos na versão UX-C3-0.2 | PROPOSTO derivado de F39–F45 | Revisão de telas e critérios pendentes no roteiro da versão corrente |

O [adendo funcional](../02-requisitos/alteracoes-escopo-v0.2.md) registra MC-02/MC-03, novos IDs e dependências. A [especificação 0.2](../02-requisitos/especificacao-funcional-v0.2.md) passa a ser a entrada corrente. Registros anteriores permanecem como histórico.

| ID | Decisão | Estado / fonte | Efeito |
|---|---|---|---|
| DEC-F58 | Justificativa da terceira visita semanal exigida de todos os promotores | APROVADO F46 | Exceção individual observada para Daysilane/contas-chave é removida da versão corrente |
| DEC-P07 | Fórmula econômica dos três melhores meses com piso de 85% segue proposta | PROPOSTO, estado confirmado em F46 | Exibir como estudo para validação, sem inferir política de premiação |

## Revisão corrente por F47

| ID | Decisão | Estado / fonte | Efeito |
|---|---|---|---|
| DEC-F59 | Retirar Dicas e IA de todo o produto | APROVADO F47 | MC-04 cancela RF-12.01–03 e DP-10 e substitui a parcela de IA de DEC-F53/F29. Retirar de planejamento e apresentação comercial |
| DEC-UX03 | Cards animados, X, confirmações, login demonstrativo vazio, seleção de página e Mais junto ao menu | Direção APROVADA F47, detalhamento PROPOSTO | UX-03.01–07 e protótipo UX-C3-0.3 |

A [ESF-C3-0.3](../02-requisitos/especificacao-funcional-v0.3.md) é a entrada corrente. Registros anteriores preservam a evolução das decisões.

## Continuidade após validação de interface

Status documental PROPOSTO • Registro de 11/11/2026.

| ID | Decisão | Estado / fonte | Efeito |
|---|---|---|---|
| DEC-UX04 | Interface ocupa a altura disponível e modal sobe até o centro | APROVADO como direção em F48 | Ajuste incorporado ao protótipo 0.3 e verificado em desktop/celular |
| DEC-UX05 | Rodapé acompanha data/hora do dispositivo | APROVADO F49 | Atualização automática, incluindo retorno ao foco e mudança de dia |
| DEC-UX06 | Protótipo 0.3 validado por Ismael como referência de experiência | VALIDADO F50 | Base visual para proposta e implementação futura. Detalhes funcionais ainda propostos conservam revisão específica |
| DEC-G08 | Continuar para planejamento revisado e proposta preliminar | AUTORIZADO F50 | Pacote interno da Etapa 5 |
| DEC-P08 | Dimensionamento revisado e sequência de marcos | PROPOSTO pelo agente, sem aceite de esforço/prazo | 226/410/674 h antes de reserva. Revisão de Ismael e negociação com a C3 pendentes |

## Reversão do primeiro filtro e interface em F54

Status documental PROPOSTO • 12/11/2026.

O primeiro filtro e os desdobramentos F51–F53 foram desfeitos por orientação expressa de Ismael. Os documentos gerados pelo recorte e o protótipo 0.4 foram descartados. As decisões DEC-F60–F65 e DEC-A05 decorrentes daquele recorte deixam de compor a referência corrente. A base funcional retorna à ESF-C3-0.3, acrescida dos ajustes específicos de F54.

| ID | Decisão | Estado / fonte | Efeito |
|---|---|---|---|
| DEC-G09 | Desfazer primeiro filtro e descartar v0.4 | APROVADO F54 | Restauração documental e reconstrução diretamente da v0.3 |
| DEC-UX08 | Remover/reordenar os cards indicados, retirar página Metas e sino superior | APROVADO F54 | Protótipo UX-C3-0.5 |
| DEC-F66 | CPF no cadastro de Escritório/Promotores, exceto Admin. Placa em Veículo para Promotor | APROVADO F54 | Campos no editor de pessoas mantido pelo Admin, com persistência local da demonstração |
