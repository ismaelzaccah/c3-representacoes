# Etapa 4 — Protótipos e experiência de uso

Status PROPOSTO • UX-C3-0.1 • 10/11/2026 • Continuidade F38.

## Decisão recebida

Ismael orientou levar o conflito entre escopo, capacidade e prazo para a proposta a apresentar à C3, para negociar requisitos funcionais que caibam no prazo estipulado. O risco permanece registrado na arquitetura e no planejamento. A futura proposta deverá relacionar as opções aos IDs dos requisitos, explicitar o conteúdo da entrega de trinta dias e registrar aprovação bilateral das mudanças pertinentes. O escopo atual continua como referência para essa negociação.

A orientação permite seguir com os protótipos enquanto chegam os materiais. As telas representam a ESF-C3-0.1 revisão 1. O avanço documental não aprova automaticamente detalhes pendentes nem viabilidade técnica do prazo.

## Resultado para revisão

Foi produzido um [protótipo navegável](../05-prototipos/prototipo-navegavel-v0.1.html) com dados fictícios, cobrindo experiência de Promotor, Escritório e gestão reservada Master. O [roteiro](../05-prototipos/roteiro-prototipos-v0.1.md) identifica 21 telas/estados, requisitos relacionados, percursos, simplificações e pontos de aprovação.

| Área | Conteúdo representado |
|---|---|
| Promotor | Clientes compartilhados, visita, veículo exclusivo, posição e justificativa, campanha/folder, aviso, histórico e combustível |
| Escritório | Visão geral, pedido/cotação, resposta e decisões por versão, campanhas, consultas, cadastros e compras aguardando fonte |
| Master | Contas, desativação/reativação, vínculo exclusivo e correção com motivo |
| Estados de interface | Posição atual/antiga/indisponível, decisões pendentes, nova versão, erro de hodômetro e indisponibilidade da base de compras |

## Conferência

Navegação principal percorrida nos três perfis em 320, 390, 768 e 1280 px, com ausência de transbordamento da página nos percursos verificados. Foram testados busca, justificativa de posição, encerramento de visita, nova versão bloqueando autorização/envio anterior, combustível e desativação/reativação local. As verificações registraram zero erro de JavaScript e zero chamada HTTP da demonstração. Foram inspecionadas visualmente a tela móvel de cliente e a tela administrativa de pedido.

As verificações ocorreram em Microsoft Edge headless com ferramentas já disponíveis. A simulação usa memória local e estados simplificados. Autorização de servidor, concorrência, processamento de arquivos, comunicação Upcar, PDF/XLSX e persistência pertencem à implementação futura. Avaliação em aparelhos reais e de acessibilidade integral permanece pendente. Os limites detalhados estão no roteiro.

## Decisões de apresentação propostas

Identificação textual C3, azul como cor de destaque, menus por responsabilidade, campos de visita empilhados no celular e pedido com conteúdo/decisões separados no computador. A marca gráfica, o conteúdo final de cotação e as opções definitivas de alguns campos aguardam revisão. Os seletores de perfil e cenário de posição são controles externos de exploração do estudo.

Ismael e Caio podem revisar agora linguagem, navegação, hierarquia da visita, cotação e decisões, além da disposição dos campos. A amostra da C3 fechará indicadores de compras e conteúdo documental. A lista de veículos identificará os vínculos reais para homologação técnica posterior.

## Arquivos criados

- `docs/05-prototipos/prototipo-navegavel-v0.1.html`
- `docs/05-prototipos/roteiro-prototipos-v0.1.md`
- `docs/06-planejamento/situacao-etapa-4.md`

Índices, fontes, decisões e estrutura da apresentação foram atualizados. O registro da negociação não altera automaticamente nenhum requisito aprovado. Todos os documentos e telas desta entrega são PROPOSTO.

## Próximo encaminhamento

Revisar os protótipos e consolidar a apresentação técnico-comercial preliminar com opções de escopo para negociação dos trinta dias. A apresentação deverá preservar preços, identificar dependências e diferenciar escopo de referência, recorte proposto e decisão efetivamente aprovada. Os dados recebidos da C3 serão incorporados com rastreabilidade.
