# Apresentação técnico-comercial — índice e estrutura preliminar

Status PROPOSTO • Versão 0.22 • 10/11/2026 • Roteiro editorial interno.

Este roteiro editorial em Markdown incorpora F08–F38. Conteúdos dependentes de esclarecimento devem manter essa identificação na apresentação futura.

Atualização corrente de 11/11/2026. O conteúdo consolidado está na [proposta técnico-comercial preliminar 0.1](proposta-tecnico-comercial-preliminar-v0.1.md), com base na ESF-C3-0.3, na experiência validada por Ismael e no planejamento revisado. O índice abaixo conserva a estrutura editorial anterior como histórico. Para a próxima apresentação, usar os atores, escopo e condições do conteúdo consolidado.

Público previsto: administração C3 e responsável pela contratação. Objetivo proposto: apresentar diagnóstico, solução híbrida, limites e condições preservadas, permitindo discutir os pontos ainda necessários à especificação e à análise de viabilidade.

## Índice comentado

| Nº | Seção / título sugerido | Mensagem e conteúdo previstos | Referências e pendências | Tratamento de evidência |
|---|---|---|---|---|
| 1 | C3 — centralização da operação comercial | Identificação, propósito e versão da apresentação | Visão; F01/F07 | Exibir PROPOSTO e caráter preliminar |
| 2 | Operação atual e necessidades | WhatsApp, e-mail, planilhas, portais e automações existentes; problemas a confirmar | F01 §2; F02; visão | Distinguir descrição fornecida e hipótese de problema; sem economia prometida |
| 3 | Objetivos e benefícios esperados | Consulta centralizada, histórico de propostas/autorizações, apoio às visitas e abastecimentos | Visão; matriz | Benefícios qualitativos propostos, sem ROI ou percentuais não medidos |
| 4 | Como funciona o MVP híbrido | Representar registros internos e ações humanas/externas separadamente | DEC-01; RF-05.* | Não sugerir substituição de Claude/WhatsApp/portais ou execução automática |
| 5 | Usuários e canais | Escritório e Promotores são atores operacionais. Escritório mantém cadastros e ajustes da rotina. Master gerencia contas, configurações e correções excepcionais com histórico | DEC-F16/F17; F13/F14 | Classificar campos/exceções e alcance dos dados. Desligamento desativa conta e preserva autoria |
| 6 | Escopo preliminar do MVP | Resumir os sete grupos e o que cada um registra/consulta | Matriz corrente | Vincular IDs e versão; resumo não substitui anexo técnico |
| 7 | Pedidos e propostas | Cotação PDF Wega, Grupo como descrição e total em três casas. Escritório revisa e autoriza, registra evidência por versão e exige reautorização após mudança | RF-05.01–13; F16/F17; D01/D02 | Demais fontes com processo a delimitar. Rejeição permite revisar ou encerrar com motivo registrado |
| 8 | Visitas e campanhas | Visitas com veículo fixo e localização via rastreador. Campanhas por fornecedor/vários clientes, folders, vigência, decisões externas e avisos internos por cliente/período | RF-03.*; RF-04.*; F26; MC-01 | Campanhas/avisos aprovados. Homologação técnica e estimativa da API pendentes |
| 9 | Cadastros, abastecimentos e consultas | Cadastros e abastecimentos com acesso definido. Indicadores operacionais, filtros e saídas Excel aprovados. Compras por cliente/fornecedor com valor no período e última compra, a partir de Excel | RF-02.*; RF-06.*; RF-07.*; F28 | Homologar layout da planilha de compras e detalhar alimentação/periodicidade |
| 10 | Experiência de uso prevista | Selecionar exemplos do UX-C3-0.1 para promotor no celular e administração | Grupo E; D04/D05 | Telas PROPOSTO com dados fictícios, selecionadas conforme o recorte a negociar |
| 11 | Direção técnica e qualidade | Web responsiva, preferência por monólito modular, autorização no servidor, rastreabilidade e arquivos | DEC-A01/A02; RNFs; D11 | Stack candidata, sem versões/serviços aprovados nem garantia de disponibilidade |
| 12 | Plano de trabalho e avaliação do prazo | Início após aceite da proposta e assinatura do contrato. Prazo de 30 dias corridos para apresentação formal. Cinco dias úteis de homologação após apresentação | DEC-C12; D12/D16 | Avaliação técnica nos primeiros cinco dias úteis. Viabilidade pendente |
| 13 | Investimento de implantação | R$ 24.000: R$ 12.000 no fechamento e R$ 12.000 no aceite do MVP | DEC-C01 | Não converter implantação em horas de evolução; não adicionar preços |
| 14 | Desenvolvimento contínuo | Após ciclo do MVP, R$ 8.000 por 80 h/mês. Competência contada da data de início, paga no fechamento. Horas expiram, garantia comercial durante contratação e suporte WhatsApp/e-mail seg–sex 9h–17h | DEC-C16–C21; F30/F31 | Redigir condições completas na etapa contratual e planejar atendimento |
| 15 | Pagamentos, homologação e mudanças | R$ 12.000 pré/R$ 12.000 pós-MVP. Homologação de cinco dias úteis. Rescisão no fim da competência em que se completam 30 dias de aviso, com última mensalidade e sem multa adicional em 3/6/12 meses | DEC-C16/C20/C22; F31 | Formalização e revisão jurídica posteriores |
| 16 | Exclusões, premissas e próximos acordos | Sintetizar exclusões, complementos de D01–D04 e materiais necessários | Matriz; pendências; roteiro | Solicitar esclarecimentos e aprovação documental. Viabilidade técnica pendente |

## Estrutura de cada seção futura

Usar título, mensagem principal, conteúdo de apoio, evidência/fonte, IDs relacionados e pendências. Se houver tela ou diagrama futuro, identificar a versão dos requisitos representados e o caráter ilustrativo. Uma funcionalidade exibida não amplia o compromisso contratual.

## Formulações obrigatórias para evitar compromisso indevido

- Prazo — “Previsão comercial de 30 dias corridos após aceite da proposta e assinatura do contrato para apresentar o MVP à homologação. A C3 terá cinco dias úteis após apresentação para testar e formalizar o aceite. A avaliação técnica ocorrerá nos primeiros cinco dias úteis da janela de desenvolvimento.”
- Escopo: “MVP híbrido, com registros e aprovações internos e atividades externas mantidas nos processos atuais quando aplicável.”
- Investimento — “Implantação de R$ 24.000 e mensalidade de R$ 8.000 por 80 horas. Ismael executará o projeto com implantação dentro dessa capacidade mensal. Suporte/evolução mensal começa após o ciclo do MVP e é pago posteriormente ao mês trabalhado. A competência mensal é contada do início do serviço e paga no fechamento, conforme F31.”
- Situação: “Material preliminar PROPOSTO, sujeito ao fechamento das pendências e aprovação dos documentos.”

## Condições para futura finalização e eventual envio

Validar narrativa e audiência com o responsável; resolver ou explicitar layouts, proposta, aprovações, acesso e marcos; vincular a versão de requisitos; incluir parecer real de viabilidade quando existir; revisar valores e exclusões; obter autorização para a ação externa. Nesta etapa somente o índice e sua estrutura estão preparados.












## Capacidade e custos recebidos em F29

A apresentação deverá informar Ismael Zaccah como desenvolvedor, implantação dentro de 80 h/mês e Caio Costa como homologador. A C3 custeará infraestrutura. F47 retirou a previsão de serviços de IA do produto. Volumes, domínio, titularidade e orçamento técnico dependem de confirmação/dimensionamento. A análise dos 30 dias considerará a capacidade informada. F30/F31 consolidam sequência de pagamento, competências, suporte e rescisão.




## Direção aprovada para a negociação — F38 / DEC-C23

A proposta deverá sinalizar o conflito identificado entre escopo integral, capacidade e prazo comercial de trinta dias. Ismael decidiu negociar requisitos funcionais com a C3 para definir um conjunto que caiba no prazo estipulado. O planejamento atual permanece como referência, com estimativas ainda preliminares e materiais pendentes. As opções apresentadas deverão ser rastreáveis e submetidas à decisão bilateral.

Na seção de prazo e plano de trabalho, incluir o problema de capacidade, as premissas e as opções de recorte funcional para discussão. Para cada requisito ou grupo proposto, identificar IDs, conteúdo da entrega, dependências, esforço revisado e efeito de eventual adiamento. Manter distinto o escopo de referência, a alternativa de negociação e o recorte efetivamente aprovado. Não presumir que item adiado será automaticamente absorvido pelas 80 horas de uma competência mensal.

Usar as telas do [UX-C3-0.1](../05-prototipos/roteiro-prototipos-v0.1.md) para explicar jornadas. Identificar demonstrações como PROPOSTO, com dados fictícios. Após acordo, atualizar especificação, critérios, planejamento e anexo técnico na mesma versão. Os preços aprovados seguem em R$ 24.000 de implantação e R$ 8.000 por 80 horas mensais posteriores. A viabilidade do recorte de trinta dias exige dimensionamento e condições explícitas.

## Atualização posterior — F42 / DEC-C24

A análise do protótipo recebido resultou em aprovação de ampliar o escopo pretendido com metas, performance, tarefas, despesas adicionais e trajetos, com prazo a renegociar. Essa é a orientação corrente para a proposta. A referência de trinta dias e o estudo anterior de alternativas permanecem históricos da negociação. A nova apresentação deverá explicitar o escopo ampliado, dependências, reestimativa, condições de entrega e eventual acordo bilateral de escopo/prazo/preço.

Utilizar [UX-C3-0.2](../05-prototipos/roteiro-prototipos-v0.2.md), [ESF-C3-0.2](../02-requisitos/especificacao-funcional-v0.2.md) e o [relatório da análise](../06-planejamento/atualizacao-prototipo-cliente-v0.2.md). Os valores aprovados continuam registrados até nova decisão bilateral. A fórmula econômica da performance permanece proposta, conforme F46.


## Atualização corrente F47

Status PROPOSTO. Retirar Dicas e IA de todos os itens e exemplos da apresentação, da proposta e da estimativa de produto. A versão corrente é a [ESF-C3-0.3](../02-requisitos/especificacao-funcional-v0.3.md). Apresentar o escopo remanescente e sua reestimativa com prazo a renegociar, mantendo R$ 24.000 de implantação e R$ 8.000 mensais por 80 horas. Os 30 dias continuam dependentes de negociação e validação técnica.
