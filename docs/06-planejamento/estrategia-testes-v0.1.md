# Estratégia preliminar de testes e homologação

Status PROPOSTO • ARQ-C3-0.1 • 10/11/2026.

Referência ESF-C3-0.1 revisão 1. Critérios CA-RF das 73 folhas, CA-RNF-01–11 e seis fluxos orientam o plano. A revisão de Ismael e a aprovação funcional de Caio consolidarão o conjunto de aceite. Este documento organiza testes futuros e não registra testes de software executados.

## Camadas e evidências

| Camada | Cobertura planejada | Ferramenta candidata / evidência |
|---|---|---|
| Regras | Cálculo decimal, mínimo, vigência, idade da posição, validações e transições | Vitest, casos tabulados e resultados |
| Banco e casos de uso | Restrições, transações, versões, auditoria, idempotência e alcance de dados | Banco isolado de teste e chamadas ao servidor, evidências de consistência |
| Integração documental | Wega, compras homologadas, PDF/XLSX e arquivos privados | Amostras controladas, comparação de campos/valores, hashes e revisão visual |
| Upcar | Contrato, permissões, horário, posições e falhas | Simulações para cenários repetíveis e consulta real autorizada para confirmar contrato |
| Ponta a ponta | Jornadas de Escritório, Promotor e Master | Playwright, roteiro de aparelho real e evidências da execução |
| Operação e qualidade | Acessibilidade, carga, logs, privacidade, backup/restauração | Relatórios por RNF com ambiente/carga e observações |

Ferramentas são candidatas conforme avaliação da stack. Dados reais necessários à integração ficam em ambiente controlado e com acesso autorizado. Amostras de testes devem ser anonimizadas ou sintéticas sempre que permitirem demonstrar a regra. Ambientes de teste/homologação e produção terão dados e credenciais separados.

## Casos críticos de regressão

| Caso | Critério e resultado esperado |
|---|---|
| T01 | RF-01.03/RNF-01. Manipular usuário, registro, filtro ou URL de arquivo não amplia permissão |
| T02 | RF-01.04.01. Desativar conta bloqueia próxima operação protegida e conserva autoria passada |
| T03 | RF-02.04.02/F35. Dois comandos tentam associar o mesmo veículo a promotores diferentes. Apenas um vínculo vigente é confirmado |
| T04 | RF-03.02. Dois check-ins simultâneos ou repetidos geram uma visita aberta. Resposta perdida permite recuperar o resultado |
| T05 | RF-03.03/07. Repetir check-out preserva instante original. Master corrige encerramento com motivo e anterior preservado |
| T06 | RF-03.09. Posição com idade 300 s é atual, 301 s exige justificativa. Posição ausente/inválida, futuro temporal e erro API não produzem validade falsa |
| T07 | RF-03.09. Alteração de vínculo durante consulta externa exige revalidar antes da gravação e não permite atribuir veículo errado |
| T08 | RF-04.05/07. Aprovação sem folder não ativa. Início/fim inclusivos são testados. Expiração/cancelamento encerram exibição e conservam histórico |
| T09 | RF-05.03. Layout divergente ou linha inválida bloqueia publicação integral. Repetição do lote não duplica efeito |
| T10 | RF-05.04. Mínimo 6 aceita 7 e recusa 5. Caso com mínimo 1, UNIT 1,2345/QTD 1 resulta 1,235 na proposta half-up. Validar soma geral e representação no PDF |
| T11 | RF-05.05–09. Alteração de conteúdo após autorização gera nova versão. Decisão da anterior não autoriza envio da atual |
| T12 | RF-05.06/07. Rejeição recebe motivo, evidência e decisão de revisar/encerrar. Revisão AJUSTAR impede autorização |
| T13 | RF-05.08. A mesma pessoa do Escritório pode revisar e autorizar versão aprovada e inalterada |
| T14 | RF-06.02/05. Retroativo verifica vizinhos anterior/posterior e serializa lançamentos concorrentes por veículo |
| T15 | RF-06.04. Escritório não corrige registro salvo. Master retifica com motivo e totais usam só valor atual |
| T16 | RF-07.02/04. Filtros, alcance, todas as páginas e totais coincidem em tela/Excel. Texto de célula não se torna fórmula |
| T17 | RF-07.05. Excel de compras é conciliado, repetição não duplica, ajustes seguem layout homologado. Base ausente mostra indisponível, base válida sem compras permite zero |
| T18 | RNF-04/08. Arquivo privado negado a perfil sem acesso. Restauração recupera base, referências e conteúdo pronto conferido |
| T19 | RNF-05/06/07. Medir carga no ambiente acordado e percorrer fluxos em dispositivos, teclado e critérios de acessibilidade |

T01–19 são cenários de maior risco, complementares ao conjunto de critérios da especificação. Cada folha funcional e cada RNF terão resultado individual no registro de execução. Campos/layout ainda dependentes de materiais receberão casos específicos após homologação.

## Registro de execução

| Campo | Preenchimento obrigatório |
|---|---|
| Identificação | ID do teste e critério CA-RF/CA-RNF, versão ESF/ARQ e versão do sistema |
| Contexto | Ambiente, navegador/aparelho, dados de entrada e permissões da conta |
| Resultado | Esperado, observado, aprovado/reprovado/bloqueado e evidência |
| Responsável | Executor e data. Caio registra manifestação funcional |
| Não conformidade | Referência, severidade, impacto, responsável e reteste |

Não conformidades são classificadas em defeito, requisito contratado não atendido, alteração/nova demanda ou dependência externa/material ausente. Severidade proposta crítica para acesso indevido, perda/corrupção de dados, duplicidade de pedido por falha interna ou bloqueio de jornada central. Demais severidades serão classificadas pelo impacto e possibilidade de continuidade aprovada.

## Rito de apresentação e aceite

1. Consolidar versão de escopo aprovada, critérios, dados e ambiente de homologação.
2. Ismael apresentar versão identificada, evidências técnicas, instruções e lista de pendências por natureza.
3. Registrar disponibilização formal para testes. Esse evento encerra o prazo de entrega para homologação conforme D13.
4. Caio executar/revisar cenários e manifestar aceite ou apontar não conformidades vinculadas aos requisitos dentro dos cinco dias úteis previstos.
5. Ismael corrigir defeitos atribuíveis à entrega, demonstrar reteste e registrar nova apresentação quando aplicável, conforme rito contratual a formalizar.

Como proposta de prontidão, critérios críticos devem estar aprovados e critérios bloqueados precisam de tratamento formal antes da apresentação integral. Mudanças e entregas parciais exigem acordo próprio. O procedimento de homologação não presume aceite por silêncio, cujo efeito dependeria de cláusula aprovada na etapa contratual.
