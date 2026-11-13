# Documentação C3 — Descoberta e especificação

Status PROPOSTO • Versão 0.29 • 12/11/2026 • Documentação interna de descoberta, especificação, arquitetura, protótipos e proposta preliminar.

A referência funcional corrente retorna à [ESF-C3-0.3](02-requisitos/especificacao-funcional-v0.3.md), com os [ajustes de cadastro e interface 0.5](02-requisitos/ajustes-cadastro-interface-v0.5.md). O [protótipo UX-C3-0.5](05-prototipos/README.md) foi reconstruído diretamente da v0.3 conforme F54.

O primeiro filtro da versão 1.0 e seus desdobramentos documentais foram desfeitos por solicitação de Ismael. A v0.4 foi descartada. O [planejamento anterior](06-planejamento/backlog-estimativas-v0.2.md) e a [proposta preliminar anterior](07-comercial/proposta-tecnico-comercial-preliminar-v0.1.md) retomam sua condição de referências propostas para revisão. As novas alterações de interface estão no [relatório 0.5](06-planejamento/ajustes-prototipo-v0.5.md).

| Grupo | Documento | Finalidade |
|---|---|---|
| Governança | [Fontes](00-governanca/fontes.md) | Evidências, autoridade e identificação dos originais |
| Governança | [Decisões](00-governanca/decisoes.md) | Decisões aprovadas na origem e propostas ainda sem aceite |
| Governança | [Pendências D01–D16](00-governanca/pendencias.md) | Perguntas, responsáveis sugeridos e evidências para resolução |
| Descoberta | [Roteiro de entrevistas e materiais](00-governanca/roteiro-entrevistas-materiais.md) | Preparação da coleta junto à C3; nada foi enviado |
| A | [Visão do produto](01-visao-produto/visao-produto.md) | Confirmado, proposto, pendente e limites |
| B | [Matriz MVP/Pós-MVP](02-requisitos/matriz-requisitos.md) | Rastreabilidade entre descoberta, folhas detalhadas e fontes |
| C | [Fluxos e permissões](03-fluxos-permissoes/README.md) | Permissões e fluxos da base funcional restaurada |
| D | [Arquitetura](04-arquitetura/README.md) | Arquitetura, tecnologias, modelo de dados, ADRs e levantamento Upcar |
| E | [Protótipos](05-prototipos/README.md) | UX-C3-0.5 derivado da v0.3, com ajustes solicitados por perfil |
| F | [Situação e próximos passos](06-planejamento/situacao-etapa-1.md) | Resultado e encaminhamento da Etapa 1 |
| F | [Prontidão para a Etapa 2](06-planejamento/prontidao-etapa-2.md) | Parecer proposto, estado de D01–D16, responsáveis e próximos entregáveis |
| G | [Estrutura da apresentação](07-comercial/estrutura-apresentacao-preliminar.md) | Índice comentado, sem deck ou proposta final |
| H | [Contratual](08-contratual/README.md) | Reserva de estrutura; sem minuta produzida |

## Versão corrente após material do cliente

[ESF-C3-0.3](02-requisitos/especificacao-funcional-v0.3.md) e [UX-C3-0.5](05-prototipos/README.md) são as entradas correntes. F54 desfaz o primeiro filtro e define alterações específicas de interface e cadastro. O prazo conserva sua condição de negociação e revisão técnica.

## Controle documental

- Todos os documentos desta etapa são PROPOSTO. O estado de uma decisão citada pode ser APROVADO na fonte, sem aprovar o documento que a registra.
- IDs de requisitos do diagnóstico são mantidos. A ESF-C3-0.3 é a referência corrente e a matriz é seu índice de rastreabilidade; o diagnóstico não será atualizado como segunda especificação paralela.
- Referências usam fonte e seção/célula, requisito, pendência e decisão. A Etapa 2 acrescentou campos, regras, exceções e critérios na ESF-C3-0.1 após F32.
- Toda resposta deve registrar evidência, responsável e data. Somente aprovação expressa encerra uma decisão pendente. Nenhuma resposta foi presumida.
- Mudanças em decisões aprovadas exigem registro de motivo, impacto em escopo/prazo/preço e aprovação pertinente. Não editar silenciosamente a decisão anterior.
- `fontes-cliente` permanece fora do Git. Nenhum documento desta etapa contém cópia das planilhas ou credenciais.

## Histórico

| Versão | Data | Origem | Registro |
|---|---|---|---|
| Diagnóstico v0.1 | 06/11/2026 | F01 | Inspeção e plano preliminar, preservados em `diagnostico-preliminar-v0.1.md` |
| Etapa 1 v0.1 | 06/11/2026 | F07 | Diagnóstico aprovado com ressalvas; descoberta autorizada nos limites da mensagem do responsável. Documentos novos PROPOSTO; execução interrompida antes da Etapa 2 |
| Etapa 1 v0.2 | 09/11/2026 | F08–F10 | Amostra de entrada e referência visual recebidas. D01–D04 parcialmente esclarecidas, D13 em esclarecimento. Diretrizes de Master, aprovação administrativa, MULTI e lançamento registradas. Avisos e métricas aguardam detalhamento e avaliação de impacto |
| Etapa 1 v0.3 | 09/11/2026 | F11 | MULTI mínimo aceita 7 com mínimo 6. Gerente geral/Master gerencia contas de funcionários. Escritório mantém o nome, com permissões em detalhamento. PRODUTO/QTD destinados ao sistema do fornecedor. D13 segue em esclarecimento |
| Etapa 1 v0.4 | 09/11/2026 | F12 | D13 resolvida. Início após aceite da proposta e assinatura do contrato. Término na apresentação formal para homologação. Cinco dias úteis de testes após apresentação. Pergunta de D04 explicada como identificação do grupo Escritório em relação a Administradores |
| Etapa 1 v0.5 | 09/11/2026 | F13 | Identificação de atores resolvida. Escritório e Promotores são os atores operacionais. Master é perfil reservado de gerenciamento, criação de contas e ajustes elevados. Documentos correntes consolidados com essa nomenclatura |
| Etapa 1 v0.6 | 09/11/2026 | F14 | Divisão geral aprovada. Escritório realiza cadastros e ajustes de rotina. Master gerencia contas, configurações e correções excepcionais. Desligamento por desativação com histórico preservado. |
| Etapa 1 v0.7 | 09/11/2026 | F15 | Amostra identificada como Wega. Layouts próprios por fornecedor. Cotação em PDF com código/descrição e preço unitário direto da planilha. Lista de layouts, descrição e totalização aguardam complementos. |
| Etapa 1 v0.8 | 09/11/2026 | F16 | Grupo fornece descrição. TOTAL = QTD × UNIT em três casas decimais. Wega é fonte disponível. Próximos fornecedores após aceite contratual podem usar planilha, PDF ou procedimento em site, com tratamento a delimitar. |
| Etapa 1 v0.9 | 09/11/2026 | F17 | D03 resolvida. Mesma pessoa do Escritório pode revisar/autorizar, com evidência por versão, nova revisão/autorização após mudança e decisão registrada na rejeição. Próxima coleta D05, com regras PROPOSTO. |
| Etapa 1 v0.10 | 09/11/2026 | F18 | D05 resolvida. Uma visita aberta por promotor, horários do sistema, edição enquanto aberta, regularização excepcional por Master e confirmação após salvar. Próxima decisão D06, localização pontual, com proposta registrada. |
| Etapa 1 v0.11 | 09/11/2026 | F19–F21 | D06 aprovada com ressalva, localização pela API do veículo. Documentação pública consultada e preservada nas fontes. MC-01 registra mudança de escopo e impacto pendente. Vínculo, atualidade e autenticação em esclarecimento. |
| Etapa 1 v0.12 | 10/11/2026 | F22 | Responsável já recebeu login, senha e token. Configuração protegida e homologação da autenticação previstas para implementação autorizada. Descoberta de D06 segue com vínculo de veículo e idade da posição. |
| Etapa 1 v0.13 | 10/11/2026 | F23 | D06 resolvida operacionalmente. Veículo fixo por promotor, posição de até cinco minutos e justificativa/conferência acima do limite. Homologação técnica da API e impacto MC-01 seguem pendentes. |
| Etapa 1 v0.14 | 10/11/2026 | F24 | Sequência de fechamento da descoberta organizada. Bloco atual D07 e carteira em D04, com regras PROPOSTO aguardando decisão. Próximos blocos de campanhas, abastecimentos, métricas, capacidade e condições comerciais. |
| Etapa 1 v0.15 | 10/11/2026 | F25 | D07 aprovada com ressalva. Todos os promotores podem visitar qualquer cliente cadastrado. Campos, manutenção, associações, inativação e responsabilidades sobre contas/veículos consolidados. Próximo bloco D08, campanhas e avisos, PROPOSTO. |
| Etapa 1 v0.16 | 10/11/2026 | F26 | D08 resolvida. Campanhas, folders, vigência, clientes-alvo, avisos internos e cancelamento aprovados. Próximo bloco D09, abastecimentos, PROPOSTO. |
| Etapa 1 v0.17 | 10/11/2026 | F27 | D09 resolvida. Abastecimentos, campos, acesso, validações, correções e retroativos aprovados. Próximo bloco D10, com indicadores/exportações PROPOSTO e fonte de compras a esclarecer. |
| Etapa 1 v0.18 | 10/11/2026 | F28 | D10 com regras gerais aprovadas. Indicadores, filtros e saídas Excel definidos. Compras têm fonte Excel, com amostra/layout a homologar. Próximo bloco D11/D12/D16, capacidade/operação/responsáveis. |
| Etapa 1 v0.19 | 10/11/2026 | F29 | Ismael Zaccah desenvolverá dentro de 80 h/mês, incluindo implantação. Caio Costa homologa. C3 custeia infraestrutura e futura IA. Volumes desconhecidos. Competências e alocação comercial seguem em D14. |
| Etapa 1 v0.20 | 10/11/2026 | F30 | Serviço mensal inicia após o ciclo de pagamento do MVP e remunera mês já trabalhado. Horas expiram. Garantia durante contratação mensal. Aviso de rescisão de 30 dias e última mensalidade de R$ 8.000. Complementos de calendário, suporte e encerramento pendentes. |
| Etapa 1 v0.21 | 10/11/2026 | F31 | Ciclo da data de início e pagamento no fechamento. Suporte WhatsApp/e-mail seg–sex 9h–17h. Rescisão confirmada sem multa adicional. Parecer de prontidão preparado, com dependências e autorização da Etapa 2 pendente. |


## Entrega corrente da Etapa 2

A ESF-C3-0.1 reúne 73 folhas funcionais vinculadas aos 48 IDs da descoberta, onze RNFs, dicionário, permissões e seis fluxos. Detalhes novos são PROPOSTO. Matriz v0.21 preservada em [Histórico](00-governanca/historico/matriz-requisitos-etapa-1-v0.21.md). Revisões e materiais prioritários no [relatório da Etapa 2](06-planejamento/situacao-etapa-2.md).


## Continuidade corrente — Arquitetura e dimensionamento

A instrução F36 autorizou continuar enquanto chegam materiais. O [pacote ARQ-C3-0.1](04-arquitetura/arquitetura-preliminar-v0.1.md) e o [relatório da Etapa 3](06-planejamento/situacao-etapa-3.md) reúnem as propostas. A ESF-C3-0.1 revisão 1 incorpora veículo exclusivo por promotor, F35. A [estimativa](06-planejamento/backlog-estimativas-v0.1.md) sinaliza conflito preliminar entre escopo integral, prazo de trinta dias e capacidade de 80 h/mês. As faixas requerem revisão de Ismael e provas técnicas.

## Entrega corrente — Protótipos UX-C3-0.1

F38 orienta tratar a negociação dos requisitos para o prazo de trinta dias na proposta. A Etapa 4 apresenta [protótipo e roteiro](05-prototipos/README.md), com Promotor, Escritório e Master, dados fictícios e direção visual proposta. O [relatório da etapa](06-planejamento/situacao-etapa-4.md) registra percursos, verificação de interface e decisões pendentes. O escopo de referência segue na ESF, com eventual recorte sujeito a aprovação bilateral.




| Revisão | Data | Origem | Registro |
|---|---|---|---|
| ESF/UX-C3-0.3 | 10/11/2026 | F47 | Retirada de Dicas e IA, cards animados, confirmações, login demonstrativo e navegação móvel |
| Planejamento/proposta preliminar | 11/11/2026 | F48–F50 | Experiência validada por Ismael, dimensionamento revisado e conteúdo da proposta para revisão interna |


| Revisão | Data | Origem | Registro |
|---|---|---|---|

| Revisão | Data | Origem | Registro |
|---|---|---|---|
| Restauração e UX-C3-0.5 | 12/11/2026 | F54 | Primeiro filtro desfeito, v0.4 descartada e interface reconstruída da v0.3 |
