# Matriz rastreável de requisitos MVP/Pós-MVP

Status do documento PROPOSTO • Versão 0.21 • 10/11/2026 • Base diagnóstico v0.1, F01–F03 e F07–F31.

Esta é a referência corrente de requisitos preliminares, mantendo IDs do diagnóstico histórico. Não é ainda a especificação contratual atômica da Etapa 2. Campos completos, validações, exceções e testes detalhados não foram produzidos. Consulte o [inventário de fontes](../fontes.md), as [decisões](../decisoes.md) e as [pendências](../pendencias.md).

O estado PROPOSTO deste documento é distinto do estado dos itens. Uma decisão APROVADA na origem não aprova a matriz. MVP indica inclusão preliminar segundo F01, sem fechar detalhes; condicional depende de aceite formal; Pós-MVP é candidato FORA DO MVP, sem contratação, data ou consumo automático das 80 horas.

P0/P1 são sequência sugerida de análise, sendo P0 base/controle crítico e P1 operação prevista. D03 está resolvida em F17 e D13 em F12. D05 está resolvida em F18. D06 está resolvida operacionalmente em F23. MC-01 registra homologação técnica e impacto da integração ainda pendentes. Referências de F02/F03 são da aba Planilha1. Consultas de visitas, campanhas e abastecimentos estão em RF-03.06, RF-04.06 e RF-06.03. A estimativa integral deve contemplar os requisitos previstos.

## 1. MVP e condições de inclusão

| ID | Requisito preliminar | Ator | Recorte / prioridade | Status | Evidência inicial de aceite | Fonte | Pendências |
|---|---|---|---|---|---|---|---|
| DEC-01 | Adotar MVP híbrido, mantendo operações externas registradas manualmente | Todos | MVP / P0 | APROVADO | Fluxos distinguem ação humana externa de registro interno | F01 §5 | D03/D13 |
| RF-01.01 | Autenticar usuário por login | Todos | MVP / P0 | PROPOSTO | Credenciais válidas permitem acesso; inválidas são recusadas | F01 RF-01 | D04/D11 |
| RF-01.02 | Encerrar sessão no logout | Todos | MVP / P0 | PROPOSTO | Sessão encerrada deixa de autorizar operações protegidas | F01 RF-01 | D04/D11 |
| RF-01.03 | Aplicar autorização no servidor aos atores Escritório e Promotores e ao perfil reservado Master | Todos | MVP / P0 | PROPOSTO; atores definidos em F13 | Áreas exclusivas do Master e alcance dos registros respeitam as permissões aprovadas | F08 D04; F11/F13 | D04/D11 |
| RF-01.04 | Ativar e desativar contas de funcionários, inclusive no desligamento | Master | MVP / P0 | PROPOSTO; regra aprovada em F14 | Conta desativada tem acesso bloqueado. Nome e vínculos permanecem nos registros anteriores | F01 RF-01; F11/F14; DEC-F17 | D04/D11 |
| RF-02.01 | Cadastrar, consultar e ajustar cliente por estabelecimento com CNPJ único e campos básicos aprovados | Escritório cadastra/ajusta. Promotores consultam | MVP / P0 | PROPOSTO; regras aprovadas em F25 | Nome/razão social, CNPJ, endereço, cidade e UF obrigatórios. Campos complementares conforme D07. Todos os promotores acessam clientes para visita | F01 RF-02; F25; DEC-F32/F33/F34 | D07 RESOLVIDA |
| RF-02.02 | Cadastrar contas de funcionários, incluindo promotores | Master | MVP / P0 | PROPOSTO; ator esclarecido em F11 | Conta criada tem papel e vínculo operacional identificados | F01 RF-02; F11 | D04/D07 |
| RF-02.03 | Cadastrar e manter fornecedores e sua situação ativa/inativa | Escritório | MVP / P0 | PROPOSTO; regras aprovadas em F25 | Fornecedor associa-se a clientes, campanhas e pedidos. Inativação preserva histórico | F01 RF-02; F25; DEC-F34 | D07 RESOLVIDA |
| RF-02.04 | Manter associações cliente–fornecedor e vínculo fixo promotor–veículo | Escritório mantém associações operacionais. Master mantém vínculo de conta/veículo | MVP / P0 | PROPOSTO; regras aprovadas em F25 | Cliente pode ter vários fornecedores. Todos os promotores podem visitar qualquer cliente. Veículo fixo associado ao promotor | F01 RF-02; F23/F25; DEC-F33–F35 | D07 RESOLVIDA |
| RF-03.01 | Consultar e selecionar qualquer cliente cadastrado para visita | Promotor | MVP / P1 | PROPOSTO; acesso aprovado em F25 | Acesso ao cliente independe do promotor que o visitou. Nova visita identifica seu próprio promotor autor | F01 RF-03; F25; DEC-F33 | D07 RESOLVIDA |
| RF-03.02 | Registrar check-in com data/hora do sistema, cliente e promotor, com uma visita aberta por promotor | Promotor | MVP / P1 | PROPOSTO; regras aprovadas em F18 | Início confirmado após salvar. Visita aberta deve ser encerrada ou regularizada antes de novo check-in. Falha exibe aviso e permite nova tentativa | F01 RF-03; F18; DEC-F26/F29 | D05 RESOLVIDA; D06 RESOLVIDA operacionalmente; API a homologar |
| RF-03.03 | Registrar check-out com data/hora do sistema na visita aberta | Promotor | MVP / P1 | PROPOSTO; regras aprovadas em F18 | Encerramento confirmado após salvar, preservando início. Falha exibe aviso e permite nova tentativa | F01 RF-03; F18; DEC-F26/F29 | D05 RESOLVIDA; D06 RESOLVIDA operacionalmente; API a homologar |
| RF-03.04 | Registrar e ajustar motivo e observações básicas enquanto a visita estiver aberta | Promotor | MVP / P1 | PROPOSTO; regra aprovada em F18 | Promotor ajusta motivo/observações durante a visita. Correção excepcional de registro encerrado segue RF-03.07 | F01 RF-03; F18; DEC-F27/F28 | D05 RESOLVIDA |
| RF-03.05 | Consultar seus próprios registros de visitas anteriores | Promotor | MVP / P1 | PROPOSTO; regra de acesso do bloco F25 | Consulta respeita autoria das visitas. Clientes podem ser selecionados por qualquer promotor | F01 RF-03; F25; DEC-F33 | D07 RESOLVIDA |
| RF-03.06 | Acompanhar visitas administrativamente | Escritório | MVP / P1 | PROPOSTO | Visitas registradas aparecem com cliente, promotor e situação | F01 RF-03 | D04/D05/D06 |
| RF-03.07 | Aplicar regras de visita aberta, edição, horários e falhas. Master regulariza visita encerrada/esquecida com justificativa e histórico | Promotor/Master conforme ação | MVP / P0 | PROPOSTO; regras gerais aprovadas em F18, origem da localização definida em F19, integração em detalhamento | Uma visita aberta por promotor, horário do sistema, edição durante abertura e correção excepcional com preservação dos registros originais. Confirmação após salvar | F01 RF-03; F18; DEC-F26–F29 | D05 RESOLVIDA; D06 RESOLVIDA operacionalmente; API a homologar |
| RF-04.01 | Registrar solicitação de campanha com cliente, fornecedor e responsável | Escritório/Promotor | MVP / P1 | PROPOSTO; regra aprovada em F26 | Solicitação mantém vínculos e identifica autor. Uma campanha pertence a um fornecedor e atende vários clientes-alvo | F01 RF-04; F26; DEC-F36 | D08 RESOLVIDA |
| RF-04.02 | Registrar aprovação ou rejeição externa do fornecedor | Escritório | MVP / P1 | PROPOSTO; regra aprovada em F26 | Decisão, responsável e alteração de estado permanecem no histórico | F01 RF-04; F26; DEC-F37 | D08 RESOLVIDA |
| RF-04.03 | Anexar um ou mais folders à campanha | Escritório | MVP / P1 | PROPOSTO; regra aprovada em F26 | Arquivos associados à campanha ficam disponíveis aos usuários autorizados | F01 RF-04; F26; DEC-F37 | D08 RESOLVIDA; limites de arquivos em D11 |
| RF-04.04 | Definir vários clientes-alvo e início/fim da vigência | Escritório | MVP / P1 | PROPOSTO; regra aprovada em F26 | Vínculos e período persistidos determinam consulta e exibição | F01 RF-04; F26; DEC-F36/F37 | D08 RESOLVIDA |
| RF-04.05 | Exibir campanhas aprovadas com folder e dentro da vigência ao selecionar cliente-alvo | Promotor | MVP / P1 | PROPOSTO; regra aprovada em F26 | Qualquer promotor visualiza campanhas ativas vinculadas ao cliente selecionado | F01 RF-03/04; F25/F26; DEC-F37 | D08 RESOLVIDA |
| RF-04.06 | Consultar histórico e estados de campanhas, preservando solicitações e decisões | Escritório | MVP / P1 | PROPOSTO; regra aprovada em F26 | Campanhas vencidas, rejeitadas e canceladas permanecem consultáveis no histórico administrativo | F01 RF-04; F26; DEC-F37/F39 | D08 RESOLVIDA |
| RF-04.07 | Retirar campanha vencida das ativas e permitir cancelamento pelo Escritório com motivo | Escritório/Sistema conforme evento | MVP / P1 | PROPOSTO; regra aprovada em F26 | Fim da vigência encerra exibição ativa. Cancelamento registra motivo e autoria. Histórico preservado | F26; DEC-F39 | D08 RESOLVIDA |
| RF-05.01 | Registrar manualmente solicitação com cliente e fornecedor | Escritório | MVP / P1 | PROPOSTO | Solicitação identifica origem informada e vínculos aprovados | F01 RF-05 | D03/D04/D11 |
| RF-05.02 | Anexar arquivos originais da solicitação | Escritório | MVP / P1 | PROPOSTO | Arquivos ficam associados à solicitação com acesso controlado | F01 RF-05 | D03/D04/D11 |
| RF-05.03 | Importar layouts homologados, com Wega como fonte atualmente disponível | Escritório | MVP / P0 | PROPOSTO; conjunto inicial a delimitar | Wega possui mapeamento validável. Próximas fontes serão avaliadas conforme aceite contratual e materiais, incluindo planilha, PDF e procedimentos externos | F01 RF-05; F09/F16; DEC-F21 | D01 |
| RF-05.04 | Gerar cotação PDF com código e Grupo como descrição, QTD, UNIT direto da planilha, TOTAL e MULTI | Escritório | MVP / P0 | PROPOSTO; regras gerais aprovadas em F16 | TOTAL = QTD × UNIT com arredondamento para três casas decimais, por exemplo R$ 12,345. QTD respeita MULTI mínimo. Homologar saída com exemplo | F10/F11/F15/F16; DEC-F20 | D02 |
| RF-05.05 | Criar nova versão quando o cliente solicitar alteração, preservando a anterior | Escritório | MVP / P1 | PROPOSTO; regra aprovada em F17 | Versões anteriores e respostas permanecem identificáveis. Mudança após autorização exige nova revisão e autorização | F01 RF-05; F17; DEC-F24 | D03 RESOLVIDA |
| RF-05.06 | Registrar decisão do cliente, data, responsável e anexo de mensagem, print ou e-mail do canal de origem | Escritório | MVP / P1 | PROPOSTO; regra aprovada em F17 | Evidência identifica a versão. Na rejeição, registrar motivo e decisão do Escritório de revisar ou encerrar | F08/F17; DEC-F23/F25 | D03 RESOLVIDA |
| RF-05.07 | Registrar revisão humana interna pelo Escritório | Escritório | MVP / P0 | PROPOSTO; regra aprovada em F17 | A mesma pessoa pode revisar e autorizar. Cada nova versão alterada após autorização exige revisão atualizada | F01 RF-05; F17; DEC-F22/F24 | D03 RESOLVIDA |
| RF-05.08 | Registrar autorização interna do Escritório vinculada à versão | Escritório | MVP / P0 | PROPOSTO; regra aprovada em F17 | Mesmo usuário pode revisar e autorizar. Mudança da proposta exige nova revisão/autorização e mantém a anterior no histórico | F01 RF-05; F17; DEC-F22/F24 | D03 RESOLVIDA |
| RF-05.09 | Registrar manualmente envio ao fornecedor | Escritório | MVP / P1 | PROPOSTO | Envio identifica versão autorizada e responsável pelo registro | F01 RF-05 | D03/D04/D11 |
| RF-05.10 | Registrar resultado do pedido externo | Escritório | MVP / P1 | PROPOSTO | Resultado fica associado ao pedido e seu histórico | F01 RF-05 | D03/D04/D11 |
| RF-05.11 | Preservar histórico de alterações e responsáveis | Sistema | MVP / P0 | PROPOSTO | Mudanças relevantes podem ser atribuídas a usuário e momento | F01 RF-05 | D03/D04/D11 |
| RF-05.12 | Definir eventual arquivo específico para fornecedor | Responsável pelo projeto | Condicional / P0 | PENDENTE | Inclusão exige layout, validações e aceite formal no anexo | F01 RF-05 | D01/D02 |
| RF-06.01 | Cadastrar e manter veículo com placa, identificação e referência externa do rastreador | Escritório | MVP / P1 | PROPOSTO; regra aprovada em F25 | Veículo pode receber abastecimento. Master mantém vínculo fixo com o promotor | F01 RF-02/06; F25; DEC-F35 | D07/D09 RESOLVIDAS |
| RF-06.02 | Registrar abastecimento com veículo, data, hodômetro, litros e valor total obrigatórios | Promotor no veículo fixo. Escritório em qualquer veículo | MVP / P1 | PROPOSTO; regras aprovadas em F27 | Litros e valor positivos. Hodômetro coerente com a sequência cronológica do veículo | F01 RF-06; F27; DEC-F40/F41 | D09 RESOLVIDA |
| RF-06.03 | Consultar histórico e totais de abastecimentos | Promotor no veículo fixo. Escritório/Master visão geral | MVP / P1 | PROPOSTO; acesso aprovado em F27 | Histórico e gastos respeitam vínculo ao veículo e filtros de período | F01 RF-06; F27; DEC-F40 | D09 RESOLVIDA |
| RF-06.04 | Corrigir abastecimento salvo com justificativa e histórico | Master | MVP / P1 | PROPOSTO; regra aprovada em F27 | Alteração preserva autoria, momento e valores anteriores | F27; DEC-F42 | D09 RESOLVIDA |
| RF-06.05 | Registrar abastecimento retroativo com data real e justificativa | Escritório | MVP / P1 | PROPOSTO; regra aprovada em F27 | Cronologia e hodômetro consistentes com registros anteriores e posteriores do veículo | F27; DEC-F43 | D09 RESOLVIDA |
| RF-07.01 | Consultar pedidos e aprovações no painel | Escritório | MVP / P1 | PROPOSTO | Consulta reflete estados e decisões registradas | F01 RF-07 | D04/D10 |
| RF-07.02 | Filtrar consultas por período, cliente, promotor, fornecedor, veículo e situação, conforme a operação | Perfil autorizado à consulta | MVP / P1 | PROPOSTO; regra aprovada em F28 | Aplicar filtros pertinentes e alcance de dados aprovado. Recorte consistente entre listagem, totais e exportação | F01 RF-07; F28; DEC-F45 | D10 RESOLVIDA |
| RF-07.03 | Apresentar contagens de visitas abertas/encerradas, pedidos por situação/fornecedor, campanhas por situação/vigência e totais de abastecimentos por veículo/período | Perfil autorizado à operação | MVP / P1 | PROPOSTO; conjunto aprovado em F28 | Valores conferem com registros e filtros pertinentes, respeitando alcance de acesso | F01 RF-07; F28; DEC-F44 | D10 RESOLVIDA |
| RF-07.04 | Exportar em Excel listagens filtradas de visitas, pedidos, campanhas e abastecimentos | Perfil autorizado à consulta/exportação conforme detalhamento | MVP / P1 | PROPOSTO; formato/saídas aprovados em F28 | Arquivo reproduz dados e filtros da consulta autorizada. Campos/layout de cada listagem serão especificados | F28; DEC-F46 | D10 RESOLVIDA |

### Complementos expressos em 09/11/2026

| ID | Necessidade recebida | Ator | Recorte e estado | Fonte | Pendências e impacto |
|---|---|---|---|---|---|
| RF-01.05 | Gerenciar contas, configurações e correções excepcionais | Master, perfil reservado | Diretriz APROVADA, detalhamento PROPOSTO | F13/F14; DEC-F17 | Classificar ações/campos de exceção e registrar autoria e momento das alterações |
| RF-03.08 | Criar avisos internos vinculados a cliente e período e exibi-los ao selecionar o cliente | Escritório cria, Promotores consultam | Regra APROVADA em F26, detalhamento PROPOSTO | F08/F26; DEC-F38 | D08 RESOLVIDA. Especificar campos, mensagens e limites no detalhamento |
| RF-05.13 | Usar PRODUTO e QTD no lançamento aprovado no sistema do fornecedor, como Wega, para realizar pedido e faturamento | Operador externo a confirmar | Destino esclarecido, detalhamento PROPOSTO | F08 D02; F11; DEC-F15 | D02/D03. Definir eventual arquivo específico e evidência do resultado externo |
| RF-07.05 | Mostrar valor comprado no período e data da última compra por cliente/fornecedor com origem em planilha Excel | Promotores, Escritório e Master conforme acesso aprovado | Indicadores e tipo de fonte APROVADOS, detalhamento PROPOSTO | F08/F28; DEC-F47 | D10 regras gerais RESOLVIDAS. Amostra/layout, alimentação, periodicidade, identificação e ajustes aguardam homologação |
| RF-03.09 | Obter posição do veículo fixo do promotor pela API do rastreador nos eventos de check-in/out | Sistema, com consulta por Escritório/Master | Regras operacionais APROVADAS, detalhamento PROPOSTO | F19/F23; DEC-F30/F31; MC-01 | Aceitar posição com até cinco minutos de idade. Acima do limite ou indisponível, registrar justificativa e conferência. Preservar veículo, origem e horários do evento/posição/consulta. Homologação técnica pendente |

F13 consolida Escritório e Promotores como atores operacionais. Master é o perfil reservado de gerenciamento. F14 aprova cadastros e ajustes da rotina para Escritório e gestão de contas, configurações e correções excepcionais para Master. Desligamentos usam desativação com histórico preservado. Campos e exemplos serão classificados no detalhamento de D04. A concessão efetiva segue RF-01.03. Avisos internos por cliente/período foram aprovados em F26. F28 aprovou valor comprado no período e última compra por cliente/fornecedor, com fonte em Excel. A amostra e o tratamento da alimentação aguardam detalhamento.

## 2. Requisitos não funcionais preliminares

| ID | Tema | Verificação proposta | Status / fonte |
|---|---|---|---|
| RNF-01 | Autenticação e autorização | Cobrir acessos permitidos e negados de cada perfil no servidor; definir expiração, recuperação de acesso e inativação | PROPOSTO / F01 §7 |
| RNF-02 | Privacidade | Inventariar finalidade, acesso, retenção e destino de cada categoria de dado, inclusive eventual localização; questões legais para revisão específica | PROPOSTO / F01 §7 |
| RNF-03 | Integridade e rastreabilidade | Verificar vínculos, transições e concorrência; registrar autor e momento de aprovações e alterações relevantes | PROPOSTO / F01 §7 |
| RNF-04 | Arquivos | Definir tipos/tamanhos permitidos e armazenamento privado; testar rejeição e acesso por usuário sem permissão | PROPOSTO / F01 §7 |
| RNF-05 | Desempenho e escala inicial | Definir operações, volume e carga com cenários explícitos. F29 informa volumes desconhecidos e crescimento. Medir latência no ambiente e carga aprovados para público inicial de até dez usuários | PENDENTE / F01 §§4/7 |
| RNF-06 | Responsividade e compatibilidade | Aprovar matriz de aparelhos, navegadores, versões e larguras; testar fluxos de promotor em Android e administrativos nas plataformas indicadas | PROPOSTO / F01 §§4/7 |
| RNF-07 | Acessibilidade | Aprovar critérios e verificar navegação por teclado, foco, rótulos, mensagens e contraste nos fluxos críticos | PROPOSTO / F01 §7 |
| RNF-08 | Backup e recuperação | Definir retenção, responsabilidade e objetivos após análise de custo; testar restauração de banco e arquivos em conjunto | PENDENTE / F01 §7 |
| RNF-09 | Disponibilidade e monitoramento | Definir janela de serviço, alertas, responsáveis e custos antes de assumir disponibilidade garantida | PENDENTE / F01 §7 |
| RNF-10 | Manutenibilidade e testabilidade | Vincular critérios de aceite a testes, documentar configuração e demonstrar instalação reproduzível em ambiente de teste | PROPOSTO / F01 §7 |
| RNF-11 | Falhas e repetição de operações | Especificar comportamento em queda de conexão e repetição de check-in/importação/aprovação para evitar registros ambíguos ou duplicados | PROPOSTO / F01 §7 |

## 3. Dependências dos requisitos não funcionais

| IDs | Pendências | O que falta |
|---|---|---|
| RNF-01 | D03/D04/D11 | Política de sessão e matriz de autorização |
| RNF-02 | D06/D07/D11/D15 | Finalidades, retenção e responsabilidades |
| RNF-03 | D03/D05/D08/D09 | Transições e correções auditáveis |
| RNF-04 | D01/D02/D08/D11 | Tipos, tamanhos, acesso e armazenamento |
| RNF-05 | D11/D12 | Carga, ambiente e metas mensuráveis |
| RNF-06 | D05/D11 | Dispositivos, versões e comportamento de conexão |
| RNF-07 | D11/D16 | Critérios e responsáveis pela validação |
| RNF-08/RNF-09 | D11/D15 | Custos, objetivos de recuperação, operação e suporte |
| RNF-10 | D12/D16 | Capacidade e rito de verificação |
| RNF-11 | D01/D03/D05 | Repetição de operações, falhas e consistência |

## 4. Pós-MVP e exclusões rastreadas

Esta seção registra exclusões de F01 e candidatos a evolução com status **FORA DO MVP**. As fontes PDF/site mencionadas em F16 aguardam definição de tratamento. A obtenção externa de arquivos pode integrar o fluxo híbrido. Capacidades automáticas requerem escopo expresso. F11 esclareceu o CRUD como gestão de contas de funcionários, prevista em RF-01.05. Cada avaliação futura exige priorização, estimativa e autorização pertinente.

| ID | Capacidade ou limite registrado | Recorte | Fonte | Condição para eventual avaliação |
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

Não classificar automaticamente como Pós-MVP: localização via API do veículo tem regras operacionais aprovadas e integração em homologação futura (D06/MC-01). F25 atribui cadastro e ajustes de rotina de clientes ao Escritório e consulta/seleção aos Promotores; arquivo específico de fornecedor continua CONDICIONAL (RF-05.12); a confirmação online com aviso e nova tentativa na falha foi aprovada em D05/F18. Modo offline completo permanece fora da decisão aprovada. Questionário ampliado da visita, endereço residencial e relatórios não especificados não entram por inferência das planilhas.

## 5. Encaminhamento para especificação futura

Após autorização da Etapa 2, completar cada ID com ator aprovado, campos/tipos/obrigatoriedade, validações, fluxo, exceções, regras e critérios de aceite verificáveis. Respostas de entrevistas devem apontar evidência e aprovador antes de alterar o estado do requisito.

F29 informou Ismael Zaccah com implantação dentro de 80 h/mês e Caio Costa como homologador. Estimativas e cronograma devem usar essa capacidade e o detalhamento dos requisitos. Volumes ainda precisam de levantamento. Os marcos de D13 estão definidos em F12 e DEC-C12. A viabilidade técnica dos 30 dias permanece pendente. DEC-01 mantém o identificador do diagnóstico e do registro de decisões.













## Restrições de capacidade e operação informadas em F29

Ismael Zaccah executará o projeto com implantação dentro de 80 h mensais. Caio Costa valida requisitos e entregas. A C3 custeará infraestrutura e futuros serviços de IA, cuja contratação dependerá de definições próprias. Hospedagem/nuvem serão criadas. Domínio e titularidade serão confirmados. Volumes e metas de escala ainda exigem dimensionamento. F30/F31 definem implantação em duas parcelas e serviço mensal posterior, em competências contadas do início e pagas no fechamento. Horas expiram. O suporte usa WhatsApp/e-mail, seg–sex 9h–17h. O dimensionamento técnico das 80 h/mês continua pendente.



## Nota de arquivamento

Conteúdo da matriz v0.21 preservado para consulta histórica. Três caminhos de links internos foram ajustados à pasta de histórico em 10/11/2026. A referência corrente está na ESF-C3-0.1.

