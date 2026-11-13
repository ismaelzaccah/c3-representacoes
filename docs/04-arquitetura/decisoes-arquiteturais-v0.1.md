# Registro arquitetural proposto

Status PROPOSTO • ARQ-C3-0.1 • 10/11/2026.

Os registros abaixo derivam das diretrizes DEC-A01–03 e da ESF-C3-0.1 revisão 1. Todos os ADRs estão PROPOSTO e aguardam revisão de Ismael, com custos aprovados por Caio quando aplicável. A autorização de continuar o planejamento consta em F36.

| ID | Contexto e alternativas | Proposta | Consequências / prova | Rastreabilidade |
|---|---|---|---|---|
| ADR-001 | Público inicial até dez pessoas, múltiplos processos correlacionados. Comparação entre aplicação integrada e serviços independentes | Monólito modular, aplicação web/servidor em um projeto | Facilita transações e implantação inicial. Separação de módulos exige disciplina. Validar build e limites do host | F01 §8, DEC-A02, RF-01–07 |
| ADR-002 | Histórico, versões e consistência concorrente. Avaliar PostgreSQL gerenciado e autogerenciado | PostgreSQL com restrições e transações, preferencialmente gerenciado | Custo e operação dependem de plano. Ensaiar unicidade, bloqueios, migração e restauração | RNF-03/08, D-01–13 |
| ADR-003 | Contas individuais e Master reservado. Avaliar solução consolidada compatível com Next.js/Prisma | Better Auth como candidato, perfis funcionais fixos controlados pela aplicação | Provar revogação imediata no próximo acesso e recuperação assistida. Aplicação continua responsável pela autorização dos objetos | PT-01/02, RF-01 |
| ADR-004 | Originais, folders, PDF e evidências privadas. Avaliar objetos privados e disco persistente com backup | Armazenamento de objetos privado, metadados no banco e estados de validação | Evita depender de disco temporário. Consistência entre serviços exige preparação/confirmação/limpeza e manifesto de backup | RNF-04/08, D-11 |
| ADR-005 | Check-in/out depende de posição pontual de terceiro | Adaptador Upcar no servidor, consulta fora da transação, snapshot por evento | Homologar autenticação, permissões e tempo. Exceção de posição permite continuidade justificada. Operação continua dependente da gravação local | MC-01, F19/F23, RF-03.09 |
| ADR-006 | Fornecedores usam fontes diferentes. Avaliar importação universal ou adaptador por layout | Adaptador Wega homologado e contratos internos por finalidade. Cada fonte adicional é avaliada | Preserva escopo e evidência. Compras faturadas têm adaptador próprio pendente da amostra | RF-05.03, RF-07.05, DP-01/02 |
| ADR-007 | Cotação aprovada deve preservar conteúdo e decisões | Snapshot imutável por versão apresentada, decimal exato e autorização vinculada à versão atual | Aumenta rastreabilidade e armazenamento. Exige invalidar permissões de prosseguir quando conteúdo muda | RF-05.04–11, PT-03 |
| ADR-008 | Um responsável com capacidade de 80 h/mês. Avaliar serviços gerenciados e máquina virtual | Cotar opção gerenciada para aplicação, banco e arquivos sob contas C3 | Comparar custo total, operação, região, conexão, limites e recuperação. Provedor/plano permanecem pendentes | F29, DP-04, RNF-05/08/09 |
| ADR-009 | Retentativas e alterações simultâneas podem duplicar eventos | Idempotência por comando, revisão otimista, restrições e bloqueios curtos por entidade | Complexidade controlada nos casos críticos. Ensaiar respostas perdidas, vínculos e sequência de hodômetro | CT-02–05, RNF-03/11 |

## Como aprovar ou alterar

Registrar ID, versão exata do pacote, aprovador, data, evidência da prova e condições. Mudança posterior gera novo registro com motivação, alternativas, impacto e relação ao registro substituído. Aprovar uma direção preliminar permite aprofundá-la. Aprovação final da composição depende das provas listadas na avaliação de tecnologias e dos custos envolvidos.
