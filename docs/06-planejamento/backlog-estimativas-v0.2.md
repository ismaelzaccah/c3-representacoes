# Backlog e dimensionamento do escopo pretendido

Status PROPOSTO • PL-C3-0.2 • 11/11/2026 • Base ESF-C3-0.3 e UX-C3-0.3.

## Base e método

Esta revisão incorpora F41–F47 e a continuidade autorizada por Ismael em F50. A experiência do protótipo foi validada por Ismael como referência de interface. O esforço abaixo corresponde à implementação futura, às verificações técnicas e à preparação da entrega. A elaboração do protótipo e dos documentos já produzidos é trabalho concluído.

As faixas são hipóteses de engenharia elaboradas pelo agente para revisão por Ismael, sem medição de produtividade do projeto. O, M e P representam cenários otimista, central e pessimista. O cenário central é uma referência de planejamento. A homologação autenticada Upcar, a amostra de compras e as demais fontes podem alterar as faixas. Espera por materiais e decisões deve ser acrescentada ao calendário conforme ocorrer.

A decomposição preserva os pacotes B01–B12 da [estimativa anterior](backlog-estimativas-v0.1.md) e explicita os incrementos necessários para o escopo pretendido. Wega é a amostra disponível dimensionada em pedidos. Cada fornecedor adicional exige identificação de fonte, processo e esforço antes de integrar uma entrega contratada.

## Base preservada para comparação

| Pacote | Conteúdo | O h | M h | P h |
|---|---|---|---|---|
| B01 | Provas técnicas, arquitetura executável e ambientes | 4 | 8 | 16 |
| B02 | Identidade, contas, recuperação e autorização | 8 | 16 | 24 |
| B03 | Cadastros e vínculos de veículo exclusivo | 10 | 18 | 28 |
| B04 | Visitas, avisos, regularização e histórico | 16 | 28 | 44 |
| B05 | Upcar para posição dos eventos e exceções | 8 | 16 | 28 |
| B06 | Campanhas, folders, vigência e decisões | 10 | 18 | 28 |
| B07 | Pedido Wega, PDF, versões e autorização | 24 | 40 | 64 |
| B08 | Combustível e correções com histórico | 10 | 16 | 24 |
| B09 | Painéis, Excel e compras faturadas | 12 | 20 | 36 |
| B10 | Arquivos privados, implantação, backup e monitoramento | 8 | 16 | 28 |
| B11 | Regressão integrada, concorrência, carga e segurança | 16 | 28 | 44 |
| B12 | Orientação, documentação e preparação da homologação | 8 | 16 | 24 |
| Subtotal histórico | Referência anterior | 134 | 240 | 388 |

## Incrementos propostos da revisão

| Pacote | Trabalho incremental e rastreabilidade | Dependências e limite da contagem | O h | M h | P h |
|---|---|---|---|---|---|
| N01 | UF, histórico compartilhado, cadastro regional e campos reservados. RF-01/02/03.10, F41–F43 | Reutiliza B02/B03. Somente autorização regional e alterações da base anterior | 6 | 10 | 16 |
| N02 | Regras de primeira/última visita, distâncias e repetição. RF-03.11–13 | Reutiliza B04/B05 e arquivos B10. Exige coordenadas e definição de calendário | 10 | 18 | 30 |
| N03 | Vendido, estoque, projeção, original, cobrança e atualização. RF-07.06 | Reutiliza cadastro, arquivos e importação B09. Incremento cobre campos e revisão próprios dos números comerciais, a conciliar com a amostra | 12 | 24 | 40 |
| N04 | Metas, contribuição de campanhas e performance. RF-08.01–04 | Reutiliza indicadores B09. Calendário, custos e fórmula econômica ainda sujeitos à validação | 16 | 28 | 48 |
| N05 | Tarefas, conclusão/reabertura e lembretes. RF-09.01–03 | Avisos internos e aviso ao Admin. Integração externa de WhatsApp depende de canal e avaliação própria | 10 | 18 | 30 |
| N06 | Despesas adicionais, comprovantes, aprovação e consulta. RF-10.01–03 | Reutiliza combustível B08 e arquivos B10. Saída Excel. Formatos adicionais precisam de decisão específica | 8 | 16 | 28 |
| N07 | Histórico de trajetos, quilômetros e destino Waze. RF-11.01–03 | Incremento sobre posição pontual B05. Depende da prova de histórico, odômetro, intervalos e limites Upcar | 12 | 24 | 40 |
| N08 | Aplicação da experiência validada aos fluxos reais. UX-03.01–07 e F48/F49 | Incremento de interface sobre B02–B09. Cards, confirmação, envio/erro, navegação e relógio. Login produtivo integra B02 | 8 | 14 | 24 |
| N09 | Regressão, orientação e aceite dos grupos acrescentados | Incremento transversal sobre B11/B12. Testes locais pertencem aos pacotes N01–N08 | 10 | 18 | 30 |
| Subtotal incremental | Escopo da revisão | RF-12 retirado por MC-04 | 92 | 170 | 286 |
| Total revisado | Base e incrementos | Hipótese de esforço remanescente | 226 | 410 | 674 |

O modelo de dados e a arquitetura da versão anterior precisam incorporar números comerciais, tarefas, despesas, metas e trajetos antes de sua implementação. Esse trabalho está distribuído nos pacotes funcionais correspondentes. Os incrementos devem ser revisados junto à base para eliminar sobreposição quando os contratos de dados forem conhecidos.

## Reserva e capacidade

Reserva de 20% herdada como hipótese da revisão anterior. A reserva cobre incerteza residual dos itens dimensionados. Novos fornecedores, canais e mudanças de requisitos recebem avaliação própria.

| Cenário | Base h | Reserva h, arredondada para cima | Referência total h | Ciclos equivalentes de capacidade a 80 h/mês |
|---|---|---|---|---|
| Otimista | 226 | 46 | 272 | 3,40 |
| Central | 410 | 82 | 492 | 6,15 |
| Pessimista | 674 | 135 | 809 | 10,11 |

Esses ciclos expressam capacidade de trabalho. O calendário depende da distribuição efetiva das 80 horas, da sequência das integrações e do retorno da C3. A janela de cinco dias úteis de homologação começa após a apresentação formal, conforme a decisão comercial registrada.

O esforço preliminar excede a capacidade nominal de um mês em todos os cenários. O prazo integral deve ser renegociado a partir da revisão de Ismael e das evidências técnicas. A estimativa serve à discussão interna e precisa ser validada antes de compor um cronograma de compromisso com a C3.

## Sequência proposta

| Marco | Pacotes principais | Evidência de saída |
|---|---|---|
| M0 — Fechamento da proposta | Revisão de escopo, esforço, materiais e critérios | Anexo de escopo e prazo negociado, com responsáveis pelas pendências |
| M1 — Provas e base técnica | B01/B02/B03/B10 inicial, N01 e provas B05/B07/N07 | Identidade, alcance regional, vínculos e contratos das integrações demonstrados |
| M2 — Operação de campo | B04/B05/B06/B08, N02 e N05/N06 | Visitas, campanhas, tarefas e despesas com fluxo de validação |
| M3 — Pedidos e informação comercial | B07/B09 e N03 | Wega/PDF e fontes comerciais conciliadas com exemplos homologados |
| M4 — Gestão e trajetos | N04/N07, conclusão N08/B10 | Metas e indicadores conferíveis, telemetria homologada e experiência aplicada |
| M5 — Verificação e apresentação | B11/B12/N09 | Critérios verificados e versão apresentada formalmente à homologação |
| M6 — Homologação C3 | Testes de Caio e correções pertinentes | Aceite ou registro de divergências vinculado ao anexo aprovado |

A sequência admite ajustes de ordem conforme a chegada de materiais e reutilização técnica. Os marcos distribuem o escopo pretendido dentro da implantação. A mensalidade de suporte e evolução tem início conforme as condições comerciais já registradas.

## Revisões antes de fechar o prazo

1. Ismael revisa cada faixa, sobreposições e capacidade real disponível.
2. C3 fornece Excel de compras/números, lista de usuários/UF/veículos e volumes de operação.
3. Ismael e João Vitor homologam os recursos Upcar necessários em execução técnica autorizada, usando credenciais protegidas.
4. Caio define calendário, despesas elegíveis, tratamento de dados ausentes e canais de lembrete.
5. As partes fecham o anexo de escopo, o cronograma e os critérios de aceite.

## Condições comerciais usadas no planejamento

Implantação de R$ 24.000, em R$ 12.000 pré-MVP e R$ 12.000 após aceite. Continuidade por R$ 8.000 mensais para 80 horas, com competência contada do início do serviço e pagamento no fechamento. As horas mensais expiram. Evolução mensal e implantação conservam os ciclos comerciais acordados. A estimativa de esforço orienta o planejamento e qualquer alteração comercial exige decisão das partes.
