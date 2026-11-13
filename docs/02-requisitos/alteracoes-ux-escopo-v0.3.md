# Ajustes de experiência e retirada de Dicas e IA

Status PROPOSTO • ESF-C3-0.3 / UX-C3-0.3 • 10/11/2026 • Fonte F47.

## MC-04 — Retirada de produto

F47 determina a remoção integral de Dicas e IA. A retirada abrange navegação, telas, dicas em texto/áudio, assistente, sugestões e análises por IA, dados específicos, permissões, integrações, estimativas e apresentação comercial dessas funcionalidades. A decisão substitui a parcela de IA de F42/DEC-F53 e a previsão anterior de futura implantação de IA de F29. O módulo deixa também o conjunto de candidatos Pós-MVP. Uma eventual retomada exigirá nova solicitação e avaliação de escopo.

| Item rastreável | Estado corrente | Consequência |
|---|---|---|
| RF-12.01 | RETIRADO por F47 | Dicas, áudio e compartilhamento específico deixam o produto |
| RF-12.02 | RETIRADO por F47 | Assistente e consulta por IA deixam o produto |
| RF-12.03 | RETIRADO por F47 | Sugestões e análise por IA de clientes em queda deixam o produto |
| DP-10 | CANCELADA por F47 | Provedor, transcrição, contexto e custos de IA deixam de ser dependências |
| PM-01 e PM-08, parcelas de IA/dicas/áudio | RETIRADAS por F47 | As demais parcelas conservam sua classificação própria |
| Dados Dica/IA e contexto de IA | RETIRADOS por F47 | Excluir do planejamento do modelo e das autorizações |

Indicadores comerciais convencionais, tarefas, números, metas e performance conservam as regras aprovadas. A fórmula econômica permanece proposta em DEC-P07. O esforço do escopo remanescente ainda requer reestimativa. Valores comerciais e condição de renegociação de prazo permanecem vinculados às suas decisões registradas.

## Comportamento de interface solicitado

| ID | Regra corrente | Critério de verificação |
|---|---|---|
| UX-03.01 | Ações com formulários e notificações abrem card sobreposto à tela atual | Solicitar campanha, cadastro/edição de cliente, números, despesas, contas e notificações deixam de aparecer no rodapé |
| UX-03.02 | Card desliza da parte inferior até o centro da tela ao abrir e no sentido inverso ao fechar | Entrada e saída animadas, respeitando preferência de movimento reduzido. Centralização e altura disponível do navegador conforme F48 |
| UX-03.03 | Botão X funcional no canto superior direito | Solicita confirmação para descartar alterações digitadas. Cancelar mantém campos e card |
| UX-03.04 | Envio exige confirmação explícita | Cancelar envio mantém dados. Confirmar executa a ação uma vez |
| UX-03.05 | Fechamento após envio depende de sucesso confirmado | Erro mantém card e dados, com mensagem. Sucesso final inicia animação de saída. Etapas intermediárias da visita mantêm o fluxo aberto |
| UX-03.06 | Tela inicial de login demonstrativo | E-mail e senha vazios permitem entrar. Sair retorna ao login. Autenticação de produção continua sujeita aos requisitos de identidade e autorização da base |
| UX-03.07 | Página selecionada tem indicador visual e semântico | Item ativo na navegação. Mais fica ativo quando a página pertence ao grupo secundário e expande os itens imediatamente abaixo do menu móvel |
| UX-03.08 | Rodapé acompanha data/hora do dispositivo | Atualiza automaticamente enquanto aberto, na virada de dia e ao retornar ao foco, conforme F49 |

## Decisões de detalhamento adotadas

Confirmação de descarte é apresentada quando houve edição. Cards de consulta sem edição fecham diretamente pelo X. Escape segue a mesma proteção do X. Clicar no fundo mantém o card aberto. O protótipo usa uma janela de aplicação com conteúdo rolável e prioriza alvos de toque móveis. Esses detalhes de experiência são PROPOSTO para avaliação no estudo.

Os registros da demonstração são locais e ilustrativos. A indicação de sucesso representa a conclusão da ação simulada. A implementação futura deverá usar o retorno confirmado da operação persistida antes de fechar o card. O acesso demonstrativo com campos vazios é exclusivo do protótipo.
