# Backlog e dimensionamento preliminar

Status PROPOSTO • ARQ-C3-0.1 • 10/11/2026.

Referência histórica. O [dimensionamento 0.2](backlog-estimativas-v0.2.md) incorpora o escopo pretendido ESF-C3-0.3 e tem precedência no planejamento corrente, com faixas propostas para revisão de Ismael.

Base ESF-C3-0.1 revisão 1, F29/F35/F36 e arquitetura proposta. Estimativa de engenharia por decomposição, preparada pelo agente para revisão por Ismael. Não há medição de produtividade deste projeto, prova de stack ou ensaio da API. As faixas representam hipóteses de esforço remanescente, incluindo preparação técnica, desenvolvimento, testes e entrega. Documentação já produzida não é recontada como trabalho futuro.

Atualização de base. Esta estimativa dimensiona ESF-C3-0.1 revisão 1. A ampliação MC-02/F42 exige reestimativa. O [relatório corrente](atualizacao-prototipo-cliente-v0.2.md) e a ESF-C3-0.2 registram o escopo pretendido ampliado e o prazo a renegociar.

## Pacotes de trabalho

O é cenário otimista, M é mais provável, P é pessimista. Horas são esforço de um responsável. Espera por cliente/terceiro não está embutida como horas trabalhadas. Todos os requisitos MVP permanecem no backlog. RF-05.12 é condicional e RF-05.13 é operação externa, com suporte interno incluído em B07.

| ID | Trabalho e rastreabilidade | Dependências | O h | M h | P h | Saída verificável |
|---|---|---|---|---|---|---|
| B01 | Provas técnicas, congelamento de arquitetura/versões e preparação de ambientes | Revisão do pacote, contas/infra para execução | 4 | 8 | 16 | Registro das provas, versões e limitações |
| B02 | Acesso, contas, recuperação e autorização RF-01, RF-02.02 | B01, revisão PT-01/02 | 8 | 16 | 24 | Matriz permitida/negada demonstrada |
| B03 | Cadastros, associações e veículo exclusivo RF-02, RF-06.01 | B02, F35 | 10 | 18 | 28 | Cadastro e vínculos com histórico e concorrência |
| B04 | Visitas, avisos e regularização RF-03 | B03, contrato da integração B05 | 16 | 28 | 44 | Fluxo check-in/out e exceções, histórico e correção |
| B05 | Integração Upcar RF-03.09/MC-01 | B01, identificadores, conta/permissões e João Vitor | 8 | 16 | 28 | Autenticação, snapshot, limite 300 s e falhas homologados |
| B06 | Campanhas, folders e vigência RF-04 | B03, armazenamento privado | 10 | 18 | 28 | Solicitação, decisões e exibição por cliente |
| B07 | Wega, cotação PDF, versões, decisões e envio registrado RF-05 | B03, exemplo PDF, revisão PT-03, arquivos | 24 | 40 | 64 | Fluxo aprovado e auditável com amostra Wega |
| B08 | Abastecimentos, cronologia, histórico/correção RF-06 | B03, precisão e ordem cronológica revisadas | 10 | 16 | 24 | Totais e retroativos consistentes |
| B09 | Painéis, filtros, XLSX e compras faturadas RF-07 | B04/B06/B07/B08, DP-01 | 12 | 20 | 36 | Indicadores e saídas conciliados com fonte |
| B10 | Arquivos privados, implantação, backup/restauração e monitoramento | B01, DP-04 e orçamento aprovado | 8 | 16 | 28 | Ambiente, proteção de arquivos e restauração demonstrados |
| B11 | Regressão integrada, concorrência, dispositivos, carga e segurança | Módulos entregues, RNF-01–11 | 16 | 28 | 44 | Relatório de critérios e defeitos resolvidos |
| B12 | Revisão de telas/fluxos com Caio, orientação, documentação operacional e entrega para homologação | Disponibilidade de Caio e critérios aprovados | 8 | 16 | 24 | Rito de testes, versão entregue e evidências |
| TOTAL | Escopo atualmente dimensionável | Sem fontes futuras indefinidas | 134 | 240 | 388 | Base para revisão, sem compromisso de prazo |

B02–B09 incluem testes locais das respectivas regras. B11 cobre integração e avaliações transversais, evitando duplicar a mesma atividade. B10 reúne o mecanismo comum de arquivos usado por vários módulos. B12 inclui ajustes ordinários de entendimento e preparação da homologação, sem presumir cinco dias úteis de dedicação integral de Ismael. Novos fornecedores, arquivo específico não definido e complexidade ainda desconhecida de compras exigem reestimativa ao receber materiais.

## Reserva e capacidade

Proposta de reserva de 20% sobre cada cenário para incerteza residual, a revisar após as provas e os materiais. A reserva não incorpora novos requisitos ou fornecedores indefinidos.

| Cenário | Base h | Reserva h, arredondada para cima | Referência total h | Capacidade de 80 h/mês em ciclos equivalentes |
|---|---|---|---|---|
| Otimista | 134 | 27 | 161 | 2,01 |
| Mais provável | 240 | 48 | 288 | 3,60 |
| Pessimista | 388 | 78 | 466 | 5,83 |

Mesmo a base otimista de 134 h excede a referência nominal de 80 h de capacidade mensal. O cenário mais provável com reserva exige 288 h, equivalentes a 3,6 ciclos de capacidade. Isso sinaliza incompatibilidade preliminar entre a entrega integral em trinta dias e a capacidade informada. O resultado depende da revisão de Ismael e das provas. A eventual chegada tardia de materiais aumenta o tempo de calendário e pode alterar esforço.

Os ciclos equivalentes são cálculo de capacidade, sem constituir novo prazo contratual ou mensalidades adicionais. Preço da implantação R$ 24.000 e mensalidade posterior R$ 8.000 por 80 h permanecem decisões comerciais aprovadas. A estimativa não converte automaticamente horas em cobrança nem presume evolução incluída na implantação.

## Sequência de execução proposta

| Marco | Conteúdo | Condição de saída |
|---|---|---|
| M0 | Revisão dos detalhes ESF/PT e da arquitetura; organização de responsáveis e materiais | Decisões registradas e pontos pendentes com responsável |
| M1 | B01 e provas prioritárias Upcar/arquivos/autorização | Parecer técnico com esforço revisado e divergências explícitas |
| M2 | B02/B03/B10 base e B04/B05 | Fluxo de visita integrado, veículo exclusivo e arquivos privados |
| M3 | B06/B07/B08 | Campanha, pedido e combustível demonstráveis por critérios |
| M4 | B09, conclusão B10/B11/B12 | Indicadores, exportações, restauração e critérios demonstrados |
| M5 | Apresentação formal do MVP para homologação | Versão/escopo e instruções formalmente apresentados |
| M6 | Cinco dias úteis de homologação, conforme contrato | Caio registra aceite ou não conformidades vinculadas aos critérios |

Há interdependências e atividades sobrepostas apenas quando a capacidade permitir. Um responsável não executa pacotes simultaneamente como se houvesse equipe adicional. O início contratual continua sendo o atendimento conjunto de aceite da proposta e assinatura. Os marcos técnicos organizam o trabalho e não substituem esse início aprovado.

## Parecer nos primeiros cinco dias úteis

Proposta de reservar até 20 h da capacidade inicial para provas prioritárias, com distribuição diária a confirmar por Ismael. As horas pertencem aos pacotes B01/B05/B07/B10/B11 correspondentes, sem acréscimo duplicado ao total. Verificar autenticação/temporalidade Upcar, sessão/permissões, processamento Wega/PDF, arquivos privados e caminho de restauração. Materiais ausentes serão identificados com efeito na conclusão do parecer.

Ao final, apresentar evidências, faixas revisadas, custo operacional e alternativas de viabilização. Havendo incompatibilidade, levar para decisão bilateral mudança de prazo ou capacidade e seus impactos. Alteração de escopo também exigiria aprovação bilateral específica. Nenhum item do MVP é retirado por esta estimativa.

## O que pode avançar enquanto chegam os arquivos

Revisão da arquitetura, modelo lógico, critérios, permissões, inventário de telas e sequência de trabalho podem continuar documentalmente. A revisão de Ismael pode reduzir incerteza da stack e da estimativa. A escolha definitiva de alimentação de compras depende do Excel. Fontes futuras aguardam amostras. API autenticada depende de execução técnica autorizada e acesso protegido. Infraestrutura depende de cotação e aprovação da C3.


