# Alterações funcionais após análise do protótipo C3

Status PROPOSTO • ESF-C3-0.2 • 10/11/2026 • Fontes F39–F46.

Registro histórico da revisão 0.2. A [ESF-C3-0.3](especificacao-funcional-v0.3.md) tem precedência. F47 retira integralmente Dicas e IA do produto e atualiza a experiência do protótipo.

As diretrizes aprovadas nas respostas de Ismael estão identificadas abaixo. Campos, fórmulas, exceções e critérios novos são PROPOSTO para detalhamento. Este adendo integra a [especificação corrente](especificacao-funcional-v0.2.md), substituindo as regras indicadas da base ESF-C3-0.1 revisão 1. O escopo pretendido ampliado exige reestimativa e prazo a renegociar.

## MC-02 — Ampliação do escopo pretendido

| Campo | Registro |
|---|---|
| Origem | F39/F40, protótipo fornecido e solicitação de análise funcional |
| Aprovação | F42 inclui metas, performance, tarefas, despesas além de combustível, trajetos/Waze e IA no escopo pretendido, com prazo a renegociar |
| Base afetada | PM-05/06/07/08/11/12, parcialmente, e RF-03/06/07 |
| Efeito | Acrescentar os grupos detalhados nesta versão e suas dependências. Conservar itens não abrangidos, como manutenção de frota, pagamentos automatizados, integrações universais e editor complexo de permissões |
| Esforço e prazo | Estimativa de 134–388 h referia-se à base anterior. Reestimativa e composição de entrega serão preparadas após detalhar os novos grupos. A orientação atual permite renegociar prazo |
| Comercial | R$ 24.000 de implantação e R$ 8.000 mensais posteriores por 80 h permanecem decisões registradas. Eventual alteração exige aprovação bilateral |
| Situação | Direção de ampliação APROVADA. Especificação contratual, estimativa e compromisso de entrega PENDENTES |

## MC-03 — Atores, alcance e operação de visita

| Regra / IDs afetados | Diretriz aprovada | Critério atualizado para revisão |
|---|---|---|
| RF-01.03/04/05, RF-02.02 | Admin assume o nome e as funções antes reservadas ao Master. Três atores, Admin, Escritório e Promotores, F41 | Escritório/Promotor não criam contas ou executam correção excepcional. Caio e Ana Paula representam Admin no estudo |
| RF-02.01.03, RF-03.01 | Promotor acessa clientes dos seus estados de atuação, F42 | Promotor CE encontra cliente CE e não acessa cliente PA diretamente, por busca, ficha, indicadores ou exportação |
| RF-02.01.01/02, RF-02.04.01 | Promotor cadastra e atualiza contato, endereço e linhas de clientes da região, F43 | Inclusão fora da UF é recusada. Atualização preserva autoria e histórico. Retificação excepcional de identidade continua reservada ao Admin |
| RF-03.05/06 e novo RF-03.10 | Histórico pessoal permanece próprio. Ficha do cliente acessível mostra visitas da equipe, F42 | Daysilane vê visitas de Walter no cliente CE, com autoria identificada. Seu Histórico pessoal continua contendo visitas próprias |
| RF-03.07/09 e novo RF-03.12 | Mínimo 8 e ideal 12 visitas/dia. Primeira 8h–8h20, última após 17h30. Residência a pelo menos 500 m, cliente a até 70 m, F44 | Posição atual a 70 m do cliente atende limite, 71 m exige regularização. Primeira/última a 499 m da residência é bloqueada, 500 m atende limite. Posição precisa ser válida e ter até 300 s |
| Novo RF-03.12 | Primeira visita fora da janela pode ser registrada com justificativa e aviso ao Admin, F45 | Primeira às 9h52 exige motivo e gera aviso atribuído ao Admin, conservando horário real |
| Novo RF-03.13 | Terceira visita semanal ao mesmo cliente exige motivo, F44 | Terceira visita sem justificativa impede confirmar. Motivo acompanha o registro. Critério de semana segue em detalhamento. F46 exige a justificativa de todos |
| RF-07.05 e novo RF-07.06 | Promotor cobra números em cada visita e pode enviá-los para clientes da região, F44 | Formulário e arquivo respeitam região e autoria. Cobrança e ausência de retorno precisam de tratamento que preserve dado ausente |
| RF-03.09/RF-11 | Origem de posições e quilômetros é o rastreador do veículo, F43 | Dados de navegação Waze não são tratados como medição de quilômetros. Histórico/telemetria exige prova Upcar |

A restrição por estado substitui a permissão geral anterior somente no alcance de clientes. Não cria exclusividade de cliente por promotor dentro da região. Veículo continua fixo e exclusivo por promotor, F35. CLT/PJ são referências cadastrais do protótipo e não definem dispensa automática das regras aprovadas.

## Requisitos acrescentados ao escopo pretendido

As linhas abaixo são unidades de detalhamento com critérios propostos, ainda sujeitas ao dicionário e aos fluxos completos revisados. Cada CA usa o mesmo ID. Prioridade PROPOSTO, P0 para integridade/alcance e P1 para operação.

| ID | Ator / função e dados | Validações, fluxo e exceções | Aceite proposto | Prioridade / fonte |
|---|---|---|---|---|
| RF-03.10 | Promotor consulta contexto compartilhado na ficha regional | Cliente permitido, visitas com autor/data, sem ampliar o Histórico pessoal | CA-RF-03.10 mostra visitas da equipe no cliente permitido e nega ficha fora da UF | P0, F42 |
| RF-03.11 | Promotor registra contato da visita, motivos, observações, foto e próximo passo | Registro aberto, anexo autorizado, tarefa com responsável/data. Motivos e exigência de observação ainda detalhados | CA-RF-03.11 mantém entrada aberta e associa relatório/tarefa ao mesmo registro sem duplicar visita | P1, F39/F40 |
| RF-03.12 | Sistema aplica janela, identificação de primeira/última e georreferência | Parâmetros aprovados acima. Horários do sistema, justificativa fora da janela e aviso ao Admin. Sem posição utilizável, conservar exceção justificada e conferência | CA-RF-03.12 demonstra 8h/8h20, atraso justificado, 70/71 m e 499/500 m com fonte conhecida | P0, F44/F45 |
| RF-03.13 | Sistema exige motivo da terceira visita semanal | Contagem por promotor/cliente, motivo vinculado. Semana civil no fuso operacional é proposta. Justificativa obrigatória para todos, F46 | CA-RF-03.13 recusa terceira ocorrência sem motivo e mantém autoria do motivo registrado | P1, F44 |
| RF-07.06 | Promotor/Escritório/Admin enviam números comerciais e original recebido | Cliente/linha/período, vendido, estoque e projeção. Promotor limitado à região e responsável por cobrar a cada visita. Revisão, duplicidade e periodicidade a detalhar | CA-RF-07.06 identifica origem, autor e atualização, mantém ausência como ausência e impede dado fora do alcance | P0, F43/F44 |
| RF-08.01 | Promotor acompanha meta diária/mensal e gestão acompanha equipe | Meta de visitas mínima 8/ideal 12 ao dia. Calendário e meses parciais precisam de definição | CA-RF-08.01 confere feito/meta/falta com a mesma base e período da consulta | P1, F42/F44 |
| RF-08.02 | Promotor/gestão acompanham resultados de campanha | Unidade, meta, realizado, contribuição e atualização por campanha/cliente. Aprovador e possibilidade de correção a detalhar | CA-RF-08.02 totaliza contribuições uma vez e conserva histórico de alterações | P1, F39/F42 |
| RF-08.03 | Promotor vê performance própria e gestão visão de equipe | Visitas, custo/visita, km/visita e combustível/km, com fonte/denominador explícitos. Período sem dado ou denominador zero requer indicação própria | CA-RF-08.03 concilia os indicadores com visitas, despesas elegíveis e telemetria do período | P1, F39/F42 |
| RF-08.04 | Sistema apresenta comparação mensal e meta econômica proposta | Fórmula observada dos três melhores meses com piso de 85% da média ainda PROPOSTO. Critérios de custo/meses e efeitos de premiação pendentes | CA-RF-08.04 usa casos de cálculo homologados e distingue mês parcial. Nenhum bônus financeiro é inferido | P1, F39/F42 |
| RF-09.01 | Promotor/gestão criam tarefas por cliente/responsável/data | Promotor na região e tarefas próprias. Escritório/Admin atribuem conforme alcance do responsável. Texto e vencimento obrigatórios propostos | CA-RF-09.01 cria tarefa identificada e impede atribuição incompatível com região | P1, F39/F42 |
| RF-09.02 | Responsável conclui/reabre e consulta tarefas | Estados aberta/atrasada/feita calculados com data e conclusão, mantendo eventos | CA-RF-09.02 conclusão/reabertura preservam autor e histórico, com filtros consistentes | P1, F39/F42 |
| RF-09.03 | Sistema emite lembretes e avisos | Canais, modelo WhatsApp, consentimentos, custos, repetição e escalonamento a definir. Aviso ao Admin por primeira visita fora da janela aprovado | CA-RF-09.03 repete entrega com controle de duplicidade, registra resultado e respeita destinatários aprovados | P0, F42/F45 |
| RF-10.01 | Usuário lança despesas próprias, gestão consulta conforme perfil | Combustível, hotel, alimentação, refeição com cliente, brinde, pedágio, estacionamento/outros. Valor positivo, data, observação e comprovante conforme política pendente. Combustível mantém RF-06 | CA-RF-10.01 vincula autor e veículo quando aplicável, preservando comprovante e situação | P1, F39/F42 |
| RF-10.02 | Admin aprova/rejeita despesas | Decisão com autor/data, motivo na rejeição PROPOSTO. Correção de fato salvo segue trilha excepcional. Reembolso/pagamento não está definido | CA-RF-10.02 Escritório/Promotor não aprovam despesa, Admin registra decisão e motivo aplicável | P0, F39/F42 |
| RF-10.03 | Perfis consultam/exportam despesas e totais autorizados | Admin/Escritório visão administrativa, Promotor próprias e combustível do seu veículo. Formatos adicionais Word/PDF observados, aprovação específica pendente | CA-RF-10.03 tela e relatório conciliam mesmos filtros, alcance e tratamento de recusadas | P0, F39/F42 |
| RF-11.01 | Admin consulta trajetos gerais, Promotor seu veículo | Histórico de rotas via Upcar, vínculo por vigência e limites de consulta. Escritório mantém posições dos eventos e não recebe trajetos gerais por padrão observado | CA-RF-11.01 percurso é identificado com veículo, origem e intervalos, com acesso negado fora do alcance | P0, F39/F43 |
| RF-11.02 | Sistema totaliza quilômetros para indicadores | Definir odômetro ou cálculo sobre rotas, lacunas, intervalos, arredondamento e reconciliação do fornecedor | CA-RF-11.02 total calculado é conferível com a fonte homologada, sem estimativa aleatória de produção | P0, F43 |
| RF-11.03 | Promotor utiliza orientação de destino no Waze | Cliente/endereço permitido, navegação externa independente da medição Upcar. Contrato de retorno/estado de deslocamento pendente | CA-RF-11.03 destino corresponde ao cliente escolhido e a medição continua vinculada ao veículo | P1, F39/F43 |
| RF-12.01 | Equipe compartilha dicas por área/linha, texto/áudio | Autoria, finalidade, arquivos e eventual transcrição. Acesso/moderação, retenção e direitos precisam de política | CA-RF-12.01 dica preserva autor/origem e só integra fontes permitidas da consulta | P1, F39/F42 |
| RF-12.02 | Usuário consulta assistente com dados autorizados | Fonte, provedor/modelo, custos, tratamento de dados e limites de resposta a aprovar. Interface identifica resposta simulada no protótipo | CA-RF-12.02 não recupera dado fora da região/perfil e identifica base/período utilizado | P0, F42 |
| RF-12.03 | Sistema sugere ações e análise de clientes em queda | Definir métrica de queda, janela, dados mínimos, explicação e revisão humana. Sugestão depende de fonte homologada | CA-RF-12.03 explica a comparação e indica falta de base, sem inventar queda ou número | P1, F29/F42 |

## Complementos do dicionário funcional

| Entidade/campo | Definição corrente ou proposta |
|---|---|
| Conta.perfil | ADMIN, ESCRITORIO ou PROMOTOR. ADMIN substitui a denominação MASTER, preservando a responsabilidade de gestão |
| Conta.estados_atuacao | Lista de UFs, obrigatória para Promotor e mantida pelo Admin. Determina seleção, leitura, cadastro, relatório e contexto de IA |
| Cliente e histórico | Cliente por estabelecimento/CNPJ. Compartilhamento permitido entre promotores com acesso à UF, com autoria individual em visitas e alterações |
| Visita.contato/motivos/anexos | Contato atendido, um ou mais motivos e anexos da visita como proposta de detalhamento. Preservar origem e acesso da entidade |
| Visita.primeira/ultima/justificativas | Identificação operacional, justificativa de atraso, repetição e exceção de posição, com autoria e aviso pertinente |
| Georreferência | Coordenadas do cliente e referência residencial do promotor com finalidade e acesso restritos. Origem/atualização e retenção dependem de DP-07 |
| Número comercial | Cliente, fornecedor/linha, competência, vendido, estoque, projeção, arquivo original, autor e instante de envio. Granularidade e revisão pendentes |
| Cobrança de números | Cliente/visita, responsável, data de solicitação e resultado ou ausência de retorno, como modelo proposto para DP-12 |
| Tarefa | Cliente, responsável, texto, data, situação e histórico de conclusão/reabertura. Estado de entrega de lembrete separado da conclusão |
| Despesa | Autor, tipo, data, valor, cliente opcional, comprovante e decisão. Combustível conserva veículo, litros e hodômetro. Correções mantêm antes/depois |
| Trajeto | Veículo, vínculo vigente, intervalo, referência Upcar, posições/odômetro ou distância e condição de qualidade. Forma concreta depende de DP-08 |
| Dica/IA | Autor, área/linha, texto/áudio, fontes permitidas, contexto autorizado e identificação da resposta/modelo quando implementado |

## Dados e decisões pendentes

| Dependência | Informação / decisão | Responsável |
|---|---|---|
| DP-07 | Georreferência de cliente/residência, origem das coordenadas, atualização e guarda restrita | C3/Ismael. Serviço de geocodificação, se necessário, exige avaliação de custo |
| DP-08 | Histórico de rotas/odômetro Upcar, permissão, fuso, paginação, limite e custo | Ismael/João Vitor. OpenAPI local documenta `/veiculos/{id}/historico-rotas/`, sem prova autenticada |
| DP-09 | Custos elegíveis, reembolsos recusados, comprovante obrigatório e fórmula de economia | Caio/Ismael |
| DP-10 | Provedor de IA, fontes permitidas, qualidade, transcrição, retenção e custos | Ismael propõe, Caio aprova |
| DP-11 | WhatsApp, modelos, destinatários, canais, agenda e escalonamento de lembretes | C3/Ismael e fornecedor de canal a avaliar |
| DP-12 | Ausência de números na visita, prazo de cobrança, revisão de envio e atualização histórica | Caio/Ismael, com amostra da fonte |
| DP-13 | Calendário de metas, interpretação de última visita e formatos de relatório | Caio/Ismael |

As dependências DP-01–06 anteriores continuam aplicáveis. O expediente de suporte de Ismael 9h–17h permanece decisão comercial própria. As regras de visita da equipe são outro domínio operacional.

