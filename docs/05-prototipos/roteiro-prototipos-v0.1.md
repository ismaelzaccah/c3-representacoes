# Protótipos de navegação e telas

Status PROPOSTO • UX-C3-0.1 • 10/11/2026.

Base ESF-C3-0.1 revisão 1, ARQ-C3-0.1 e autorização de continuidade F38. O [protótipo navegável](prototipo-navegavel-v0.1.html) é um estudo local de interface com dados fictícios e estados simplificados. A direção visual é proposta para revisão de Ismael e Caio. Os controles externos de perfil e cenário servem à exploração das telas, sem constituir funções operacionais do produto.

## Direção de interface

Identificação textual C3, azul como destaque e superfícies claras/escuras conforme aparência do ambiente. A marca gráfica definitiva aguarda validação. Hierarquia prioriza cliente, estado da operação e ação seguinte. No celular, campos são empilhados e navegação adapta-se à largura. No computador, o Escritório tem menu lateral e conteúdo administrativo. Tabelas podem ter rolagem própria quando necessário.

Conteúdo e campos são rastreáveis à especificação. A escolha visual não adiciona obrigações funcionais. Exemplo de nome, empresa, veículo, valores e horários é fictício. A prévia usa 10/11/2026 como data operacional de demonstração e novembro de 2026 como vigência. A reprodução visual de PDF/folder é ilustrativa e aguarda o material da C3.

## Inventário e rastreabilidade

| Tela / estado | Conteúdo representado | Perfil de exploração | Requisitos |
|---|---|---|---|
| T00 — Acesso | Entrada com conta de exemplo e indicação de recuperação assistida | Todos | RF-01.01/02/05.03 |
| T01 — Clientes | Busca, lista e acesso a qualquer cliente cadastrado | Promotor | RF-02.01.03, RF-03.01 |
| T02 — Cliente e visita | Veículo exclusivo, motivo/observação, check-in/out, posição e exceção justificada | Promotor | RF-03.02–04/09, F35 |
| T03 — Histórico de visitas | Autoria, situação e conferência | Promotor próprias, Escritório geral | RF-03.05/06, RF-07.03.01 |
| T04 — Visão geral | Visitas abertas/encerradas e pedido em acompanhamento | Escritório/Master | RF-07.01/03 |
| T05 — Pedido | Itens, mínimo, valores, versão, revisão, autorização e envio registrado | Escritório | RF-05.04–11 |
| T06 — Resposta cliente | Decisão, motivo, evidência fictícia e encaminhamento de rejeição | Escritório | RF-05.06 |
| T07 — Nova versão | Quantidade/motivo e perda da liberação da versão anterior | Escritório | RF-05.05/07/08 |
| T08 — Conteúdo de cotação | Cabeçalhos PRODUTO/QTD/UNIT/TOTAL/MULTI e versão | Escritório | RF-05.04, DP-05 |
| T09 — Campanhas e avisos | Estado, alvo, vigência, folder, decisão/cancelamento e aviso | Escritório | RF-04, RF-03.08 |
| T10 — Folder | Conteúdo gráfico de exemplo | Promotor/Escritório | RF-04.03/05 |
| T11 — Solicitação de campanha | Cliente, fornecedor, título e descrição | Promotor | RF-04.01 |
| T12 — Combustível | Veículo, totais e histórico | Promotor veículo fixo, Escritório geral | RF-06.03, RF-07.03.04 |
| T13 — Lançamento combustível | Data, hodômetro, litros, total e justificativa retroativa | Promotor/Escritório | RF-06.02/05 |
| T14 — Cadastros | Clientes, identificação do fornecedor/veículo e responsabilidades | Escritório | RF-02, RF-06.01 |
| T15 — Cliente novo | Campos básicos e indicação de complementos | Escritório | RF-02.01.01, D-02 |
| T16 — Compras | Indisponibilidade da base e campos dos indicadores esperados | Escritório | RF-07.05, DP-01 |
| T17 — Funcionários | Situação, desativação/reativação e preservação histórica | Master | RF-01.04/05 |
| T18 — Conta nova | Nome, e-mail e perfil em exemplo de formulário | Master | RF-02.02 |
| T19 — Veículo por promotor | Vínculo exclusivo e identificador Upcar ainda pendente | Master | RF-02.04.02, F35, DP-03 |
| T20 — Correção excepcional | Valor anterior, valor revisado e justificativa | Master | RF-06.04, D-13 |

O inventário inclui estados e formulários de uma mesma jornada, não vinte e uma novas funcionalidades. O menu de Master mostra uma seleção de gestão para exploração. A matriz de permissões continua definindo seu acesso geral ao sistema. Exemplos de opções em listas e dos campos de formulário permanecem sujeitos à revisão da ESF.

## Percursos sugeridos para revisão

1. Selecionar Promotor, buscar cliente e abrir Autopeças Horizonte. Conferir veículo, aviso, campanha/folder e indisponibilidade das compras.
2. Escolher cenário de posição antiga. Tentar iniciar visita sem justificativa, preencher motivo da exceção e confirmar. Encerrar com justificativa e consultar Minhas visitas.
3. Selecionar Escritório e abrir Pedidos. Liberar revisão e autorizar. Alterar a quantidade, criar nova versão e verificar pendência de resposta, revisão e autorização.
4. Explorar resposta do cliente, prévia de cotação e registro manual do envio. O PDF esperado será revisado quando a C3 encaminhar o exemplo.
5. Explorar decisão e cancelamento de campanha, folder e impacto na exibição do cliente.
6. Registrar combustível, provocar hodômetro incoerente e depois informar valores válidos. Conferir histórico e totais.
7. Selecionar Master, desativar conta de exemplo e retornar ao Promotor para ver o bloqueio. Reativar pelo Master e conferir acesso/histórico.
8. Conferir correção excepcional e vínculo exclusivo. Revisar rótulos, ordem dos campos e separação das responsabilidades.

## Alcance da simulação

| Elemento | Comportamento deste estudo |
|---|---|
| Dados e gravação | Memória local da demonstração. Recarregar reinicia dados fictícios. Preferência de perfil/tela pode ser lembrada pelo visualizador |
| Perfil e acesso | Alternância externa para revisar telas. Controles visuais ilustram responsabilidades. Autenticação/autorização real depende de servidor futuro |
| Posição Upcar | Cenários fixos atual/antiga/indisponível, escolhidos externamente. Nenhuma chamada à API |
| Visita e combustível | Estados locais e validações exemplificativas, sem transação, idempotência ou concorrência reais |
| Nova versão | Quantidade exemplificada e reset das decisões atuais. Histórico textual resumido, sem implementação completa da trilha auditável |
| Rejeição/alteração | Formulário ilustra evidência e encaminhamento. Rejeição exibe a escolha no retorno local. O ciclo completo de encerramento e revisão pertence aos fluxos/CA da especificação |
| Anexos, PDF e Excel | Representação de conteúdo ou descrição de colunas. Arquivos não são processados, gerados ou transmitidos |
| Solicitação de campanha e criação de conta | Formulários com retorno ilustrativo. Fluxo entre usuários e persistência não são reproduzidos |
| Cadastros | Amostra de campos e inclusão local de cliente. Validação completa de CNPJ, duplicidade, UF e todos os campos complementares permanece na ESF |
| Campanhas/tempo | Uma campanha fixa de novembro de 2026 e simulação local de decisão/cancelamento. Calendário de produção ainda será implementado |
| Veículos | Um vínculo de exemplo. O estudo apresenta a exclusividade aprovada. Proteção concorrente será testada na implementação |

## Conferência realizada

Foram percorridos busca de cliente, visita com justificativa, encerramento, nova versão invalidando autorização anterior, validação de hodômetro, totalização e desativação/reativação de conta de exemplo. Navegação principal nos três perfis foi verificada em larguras de 320, 390, 768 e 1280 px, em Microsoft Edge headless com Playwright disponível no ambiente. Os percursos verificados tiveram zero erro de JavaScript e zero requisição HTTP da demonstração.

Foram inspecionadas imagens da tela móvel de cliente e da tela administrativa de pedido. A conferência verifica o estudo de interface. Teste em aparelhos reais, Safari, teclado/leitor de tela e avaliação integral de contraste permanecem para validação específica. Os testes funcionais do produto seguem os critérios ESF e o plano de testes futuro.

## Pontos para aprovação

Direção visual, nomes dos menus, prioridade de informação na visita, separação das decisões da cotação, disposição dos campos e mensagens de exceção. O exemplo preenchido da C3 fechará conteúdo/identificação da cotação. Os materiais pendentes continuam ligados a DP-01–06.
