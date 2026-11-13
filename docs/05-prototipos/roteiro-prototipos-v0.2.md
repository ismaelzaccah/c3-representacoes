# Roteiro do protótipo alinhado à referência C3

Status PROPOSTO • UX-C3-0.2 • 10/11/2026.

Registro histórico da revisão 0.2. A [ESF-C3-0.3](../02-requisitos/especificacao-funcional-v0.3.md) tem precedência. F47 retira integralmente Dicas e IA do produto e atualiza a experiência do protótipo.

Base funcional ESF-C3-0.2. O [protótipo navegável corrente](prototipo-navegavel-v0.2.html) deriva da aplicação fornecida pela C3 e incorpora o fluxo de pedidos preparado anteriormente. A [versão 0.1](prototipo-navegavel-v0.1.html) foi preservada como histórico de exploração. A [análise funcional](analise-prototipo-cliente-v0.1.md) detalha o material, os paralelos, as divergências e as aprovações recebidas durante o trabalho.

## O que mudou

- Dez nomes no seletor Ver como, com os perfis Admin, Escritório e Promotor e estados do material fornecido.
- Logo original C3 extraída nas variantes escura/clara e aplicada nas telas. As imagens derivadas estão em `assets/c3-logo-color.png` e `assets/c3-logo-light.png`.
- Hoje como entrada do promotor, com situação atual, retomada da visita, metas, clientes da região, tarefas e trajetos do veículo.
- Clientes e números limitados aos estados de atuação, inclusive prévia de relatório. Histórico da equipe compartilhado na ficha do cliente permitido.
- Cadastro e atualização de clientes da região pelo promotor, incluindo contato, endereço e linhas.
- Jornada de visita em seleção, contexto, relatório e check-out, com entrada aberta antes do relatório final.
- Regras de janela da primeira visita, justificativa de atraso, distâncias e repetição semanal, conforme respostas de Ismael.
- Metas, gráficos de performance, tarefas, despesas, trajetos e dicas/IA representados no escopo pretendido ampliado.
- Pedidos com código/Grupo, MULTI mínimo, versão, resposta, revisão, autorização e envio manual registrado.

## Percursos de revisão

| Percurso | Como explorar | Resultado esperado no estudo |
|---|---|---|
| Pessoas e perfis | Alternar dez nomes em Ver como | Admin tem gestão de contas/configurações, Escritório operação geral e promotor região própria |
| Região CE x PA/AP | Abrir Clientes e Números com Daysilane e depois Peterson | Conjuntos diferentes e limitados às UFs do perfil |
| Histórico compartilhado | Abrir um cliente CE com visitas de outro promotor | Autoria e observação aparecem na ficha. Histórico pessoal continua próprio |
| Cadastro do promotor | Cadastrar/atualizar cliente com nome, CNPJ, endereço, cidade/UF e contato | UF limitada à região do perfil. Atualização de identidade existente é tratada separadamente |
| Visita | Continuar registro aberto em Hoje ou usar perfil sem visita aberta para novo check-in | Registro aberto identificável antes do relatório, retomada e encerramento do mesmo registro |
| Horário e posição | Abrir Cenários de teste da demonstração no contexto da visita | Atraso da primeira exige justificativa, posição antiga/indisponível exige conferência, distâncias têm limites conhecidos |
| Motivos e próximo passo | Preencher relatório com motivos/observação e tarefa/data | Relatório parcial preserva a visita aberta, encerramento atualiza histórico e tarefa |
| Campanha | Explorar Campanhas, folder, solicitação e decisão/cancelamento em perfil administrativo | Fluxo comercial e acompanhamento ficam visíveis |
| Números | Enviar valores de exemplo por cliente/linha e visualizar prévia de relatório | Cliente e relatório respeitam UF, com indicação da cobrança a cada visita |
| Despesas | Alternar tipo, preencher valor/data e, para combustível, litros/hodômetro/veículo | Validação local dos campos essenciais. Admin tem aprovação/rejeição e correção excepcional |
| Performance | Alternar custo por visita, combustível e km/visita | Colunas mensais, barras, metas e comparações são exemplos com unidades e contexto |
| Pedido | Liberar revisão, autorizar, criar nova versão e abrir prévia de cotação | Autorização/envio não migram automaticamente para nova versão |
| Tarefas | Criar tarefa, filtrar abertas/atrasadas/feitas e marcar conclusão | Escopo próprio do promotor e gestão administrativa |
| Dicas e IA | Explorar dica/texto/áudio e consulta/sugestão | Resposta identificada como simulação local, sem inferência real sobre a C3 |

## Limites da representação

Nomes e referência de perfis vieram da C3 por solicitação de Ismael. Demais dados são exemplos do material e da simulação. A data operacional de referência continua sendo 20/10/2026, usada no material do cliente. A data documental é 10/11/2026.

O estudo usa memória local. Controles de posição, horário e distância simulam cenários e não representam sensores. Veículos e identificadores precisam da lista real. Fotos, arquivos, PDF/Word/Excel e IA têm prévias locais. Processamento, armazenamento, autorização de servidor, integração Upcar/WhatsApp e decisões definitivas de tecnologia dependem de implementação e homologação.

Fórmula de economia, transcrição, regras de lembrete, premiação e formatos adicionais têm detalhamento pendente. F46 confirma justificativa de repetição para todos e mantém a fórmula econômica como proposta. Os gráficos preservam o tipo e a organização da referência com dados ilustrativos. A fonte real de compras faturadas ainda é necessária para indicadores de compra.

## Direção mobile-first

Cabeçalho compacto com logo e pessoa, abas principais próximas ao cabeçalho e demais opções em Mais. Campos e botões têm alvos móveis maiores, conteúdo empilhado e gráficos mensais adaptados à largura. Tabelas longas ficam em área de rolagem local. A navegação evita sobrepor controles a formulários ou exigir menu lateral no celular.

As telas e os gráficos são PROPOSTO para revisão. A nomenclatura e as regras expressamente aprovadas estão na especificação 0.2. O relatório de atualização registra as verificações e limitações de teste.

