# Matriz de permissões

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Escritório e Promotores são atores operacionais. Master é perfil reservado com visão geral, gestão de contas e ajustes elevados. Bases F13/F14/F25–F28. O detalhamento abaixo aplica as diretrizes e ainda exige revisão dos pontos explicitamente propostos. Toda concessão é verificada no servidor por ação, registro e campo, inclusive download, filtro e exportação. Ação ausente é negada até especificação/aprovação.

| Ação / requisitos | Promotores | Escritório | Master | Base / detalhe |
|---|---|---|---|---|
| Login/logout RF-01.01/02 | Própria conta ativa | Própria conta ativa | Própria conta ativa | F01, PT-01/02 |
| Criar/editar/ativar/desativar contas RF-01.04/05, RF-02.02 | Negado | Negado | Permitido | F11/F14. Gestão de contas, sem editor dinâmico de permissões |
| Recuperação assistida RF-01.05.03 | Solicita por canal de suporte | Solicita por canal de suporte | Executa procedimento protegido | PT-01 |
| Configurações RF-01.05.02 | Negado | Negado | Permitido para parâmetros especificados | F14. Lista de parâmetros em revisão |
| Consultar clientes RF-02.01.03 | Todos cadastrados | Todos | Todos | F25. Sem carteira exclusiva |
| Criar/editar rotina/inativar cliente RF-02.01 | Negado | Permitido | Permitido | F14/F25 |
| Retificar CNPJ/identidade RF-02.01.05 | Negado | Negado | Com motivo/histórico | Campo exclusivo Master PROPOSTO, sujeito a revisão |
| Manter fornecedores/associações RF-02.03/04.01 | Consulta identificação pertinente | Permitido | Permitido | F25 |
| Manter veículos RF-06.01 | Consulta veículo fixo | Rotina | Rotina e retificação excepcional | F25. Retificação de placa exclusiva Master PROPOSTO |
| Fixar vínculo promotor–veículo RF-02.04.02 | Negado | Negado | Permitido com histórico | F23/F25 |
| Check-in/out RF-03.02/03 | Próprias visitas | Acompanhamento | Regularização excepcional | F18. Master não se faz passar pelo promotor |
| Editar motivo/observação RF-03.04 | Própria visita aberta | Negado | Correção justificada | F18/F14 |
| Consultar visitas RF-03.05/06 | Próprias | Todas | Todas | Cliente compartilhado não amplia histórico de autoria |
| Regularizar visita encerrada/esquecida RF-03.07 | Negado | Negado | Permitido com justificativa | F18 |
| Consultar posição do evento RF-03.09 | Condição da própria visita, sem rastreamento geral | Eventos das visitas | Eventos das visitas | F19/F23. Exibição detalhada de coordenadas ao Promotor permanece pendente |
| Criar aviso RF-03.08.01 | Negado | Permitido | Permitido | F26 |
| Ler avisos/campanhas ativas RF-03.08.02, RF-04.05 | Cliente selecionado | Todos | Todos | F25/F26 |
| Solicitar campanha RF-04.01 | Permitido | Permitido | Permitido | F26 |
| Decidir campanha, folders, alvos, período, cancelar RF-04.02–07 | Negado | Permitido | Permitido | F26 |
| Histórico administrativo de campanha RF-04.06 | Negado | Permitido | Permitido | F26. Solicitação do Promotor conserva autoria |
| Retificar decisão passada de campanha | Negado | Negado | Com motivo/histórico | Aplicação PROPOSTO de F14 |
| Solicitação, anexos, importação Wega, PDF RF-05.01–04 | Negado | Permitido | Permitido | F01/F17 |
| Nova versão, resposta/evidência, revisão, autorização RF-05.05–08 | Negado | Permitido | Permitido | F17, mesma pessoa pode revisar/autorizar |
| Registrar envio/resultado RF-05.09/10 | Negado | Permitido | Permitido | F01/F11 |
| Retificação pós-envio PT-08 | Negado | Encaminha e trata fornecedor externamente | Registra correção com motivo | PROPOSTO, sem apagar envio anterior |
| Registrar abastecimento RF-06.02 | Veículo fixo | Qualquer veículo | Qualquer veículo | F27 |
| Consultar combustível RF-06.03 | Veículo fixo | Todos | Todos | F27. Após troca de vínculo, política proposta no módulo |
| Corrigir abastecimento salvo RF-06.04 | Negado | Negado | Com motivo/histórico | F27 |
| Inclusão retroativa RF-06.05 | Negado | Permitido | Permitido | F27 |
| Painel pedidos/campanhas RF-07.01/03 | Somente conteúdo autorizado em cliente/visita | Geral | Geral | F28. Sem painel administrativo global para Promotor |
| Indicadores de visitas/combustível RF-07.03 | Próprias visitas/veículo fixo | Geral | Geral | F27/F28 |
| Compras por cliente/fornecedor RF-07.05.02/03 | Qualquer cliente | Todos | Todos | F25/F28 |
| Alimentar compras Excel RF-07.05.01 | Negado | Permitido, proposta PT-06 | Permitido | DP-01, ator de alimentação PROPOSTO |
| Exportações XLSX RF-07.04 | PENDENTE, negar até decisão | Permitido | Permitido | PT-07. Formato aprovado, concessão por perfil em revisão |
| Ler auditoria/evidências administrativas | Negado | Registros operacionais autorizados | Geral | F14/F17. Sem senha/token em histórico |
| Ler arquivos privados | Folders ativos pertinentes ao cliente | Arquivos das operações autorizadas | Arquivos das operações autorizadas | Acesso por vínculo da entidade, sem URL pública permanente |
| Excluir fisicamente fatos/versões/contas históricas | Negado | Negado | Negado no fluxo operacional | Preservação F14/F17. Retenção/descarte será decisão de governança própria |
| Obter credenciais da API pela interface/exportação | Negado | Negado | Negado | Configuração protegida na implantação, sem exposição de segredo ao usuário |

## Casos obrigatórios de autorização

1. Promotor A tenta consultar visita de B diretamente pelo ID. Negar, mesmo com acesso ao mesmo cliente.
2. Escritório tenta criar funcionário ou alterar o próprio perfil para Master. Negar no servidor.
3. Promotor altera filtro/veículo em consulta de combustível. Aplicar vínculo autorizado antes do filtro.
4. Conta desativada tenta reutilizar sessão ou baixar arquivo. Negar.
5. Link de evidência administrativa é acessado sem autorização da solicitação. Negar.
6. Master corrige fato encerrado. Exigir motivo e registrar anterior, autor e momento.

Cada caso integra CA-RNF-01 e os critérios dos requisitos associados.
