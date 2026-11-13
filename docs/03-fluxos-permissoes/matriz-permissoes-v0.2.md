# Permissões por ator após análise da referência C3

Status PROPOSTO • ESF-C3-0.2 • 10/11/2026.

Registro histórico da revisão 0.2. A [ESF-C3-0.3](../02-requisitos/especificacao-funcional-v0.3.md) tem precedência. F47 retira integralmente Dicas e IA do produto e atualiza a experiência do protótipo.

Admin assume as responsabilidades antes denominadas Master, F41. Regiões, histórico compartilhado, manutenção de cadastro e envio de números foram aprovados em F42–F44. As permissões dos grupos novos abaixo aplicam o comportamento observado como proposta de detalhamento, com aprovação contratual e implementação de servidor futuras. A matriz da versão 0.1 é histórica nos pontos substituídos.

| Ação | Admin | Escritório | Promotores | Base / estado |
|---|---|---|---|---|
| Consultar clientes | Todos | Todos | Estados cadastrados no seu perfil | F42 APROVADO |
| Cadastrar cliente | Sim | Sim | Dentro dos estados de atuação | F43 APROVADO |
| Atualizar contato/endereço/linhas | Sim | Sim | Clientes da região | F43 APROVADO, autoria preservada |
| Corrigir identidade/CNPJ existente | Com motivo/histórico | Encaminha ao Admin | Encaminha ao Admin | Detalhe reservado PROPOSTO da base |
| Selecionar cliente para visita | Visão de gestão | Visão administrativa | Clientes da região | F42 |
| Histórico pessoal de visitas | Geral na gestão | Geral na gestão | Própria autoria | RF-03.05 preservado |
| Histórico na ficha de cliente | Geral | Geral | Visitas da equipe em cliente permitido | F42 APROVADO |
| Check-in/out e relatório | Correção excepcional | Acompanhamento | Próprias visitas | Base e F44/F45 |
| Corrigir visita encerrada/esquecida | Com motivo/histórico | Encaminha | Encaminha | Responsabilidade reservada preservada |
| Posição do evento da visita | Geral | Acompanhamento dos eventos | Próprios eventos e condição | RF-03.09. Fonte Upcar |
| Trajetos e quilômetros gerais | Sim | Sem acesso geral por padrão | Próprio veículo exclusivo | Comportamento observado, RF-11 PROPOSTO |
| Orientação Waze | Referência de gestão | Referência administrativa | Destino autorizado | RF-11.03 PROPOSTO |
| Cobrar/enviar números comerciais | Todos | Todos | Clientes da região, em cada visita | F44 APROVADO |
| Consultar números | Todos | Todos | Clientes da região | F42/F44 |
| Importar compras faturadas | Sim | Sim | Permissão específica a detalhar | RF-07.05 permanece com DP-01. Envio de números não define automaticamente importador de faturamento |
| Solicitar campanha | Sim | Sim | Cliente regional | Base e ampliação |
| Registrar decisão externa, folders e vigência | Sim | Sim | Consulta/solicitação | RF-04 preservado |
| Atualizar resultado de campanha | Geral | Conforme regra da campanha | Campanhas atribuídas e clientes permitidos | Referência, RF-08.02 PROPOSTO |
| Ver metas e performance | Geral | Geral | Própria, com contexto permitido | F42, fórmulas a homologar |
| Alterar parâmetros econômicos/gerais | Sim, com histórico | Leitura | Leitura | Aplicação da divisão de configuração |
| Criar tarefa | Sim | Sim | Própria, cliente da região | RF-09 PROPOSTO |
| Concluir/reabrir tarefa | Gestão | Gestão | Próprias | RF-09 PROPOSTO. Mostrar contexto compartilhado não concede alteração de tarefa alheia |
| Receber aviso de primeira visita fora da janela | Sim | Sem concessão automática | Confirmação da própria ocorrência | F45 APROVADO |
| Cadastrar despesa | Próprias/rotina administrativa | Próprias/rotina administrativa | Próprias | RF-10 PROPOSTO |
| Registrar combustível | Qualquer veículo | Qualquer veículo | Veículo exclusivo | F27/F35 preservados |
| Consultar despesas/combustível | Geral | Geral | Próprias e combustível do veículo | Base e referência |
| Aprovar/rejeitar despesa | Sim | Não concedido | Não concedido | Referência, RF-10.02 |
| Corrigir abastecimento salvo | Com motivo/histórico | Encaminha | Encaminha | RF-06.04 preservado |
| Registrar combustível retroativo | Sim, com motivo | Sim, com motivo | Não concedido | RF-06.05 preservado |
| Pedidos, PDF, resposta, revisão e autorização | Geral | Operação completa | Não concedido | RF-05 preservado |
| Criar/editar/ativar/desativar conta | Sim | Não concedido | Não concedido | F41, perfis fixos |
| Alterar estados de atuação/vínculo de veículo | Sim, preservando histórico | Encaminha | Consulta próprio | F41/F35 |
| Editor dinâmico de perfis/permissões | Em detalhamento | Não concedido | Não concedido | A referência mostra a função. Inclusão específica ainda não foi aprovada |
| Dicas e áudio | Acesso da equipe/moderação a definir | Compartilhamento | Compartilhamento | RF-12.01 PROPOSTO |
| IA | Dados autorizados | Dados autorizados | Alcance regional e fontes compartilhadas permitidas | RF-12 PROPOSTO. Permissão deve ser aplicada antes da recuperação de contexto |
| Prévia de relatórios/exportação | Geral autorizado | Geral autorizado | Próprios registros ou clientes da região conforme relatório | Comportamento observado representado. Formatos adicionais e concessões específicas precisam de homologação |
| Excluir fatos históricos/contas com autoria | Fluxo de desativação/correção | Fluxo de desativação/correção | Sem exclusão histórica | Política de retenção/descarte será definida separadamente |

## Regras transversais para implementação

Autorizar ação, entidade e campo no servidor, antes de filtros, agregações, relatório, download e contexto de IA. Acesso ao histórico compartilhado limita-se ao cliente permitido. A região não transforma os clientes em carteira exclusiva de uma pessoa. Trocas de UF e de veículo exigem histórico e definição do efeito sobre acesso retrospectivo.

O protótipo aplica restrições locais para ilustrar a matriz. O seletor Ver como é controle de exploração. A validação real de identidade, transações, concorrência e autorização integra a implementação futura.
