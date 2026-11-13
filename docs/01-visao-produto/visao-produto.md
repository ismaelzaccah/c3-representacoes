# Visão do produto

Status PROPOSTO • Versão 0.21 • 10/11/2026 • Fontes F01–F03 e F07–F31.

Referência corrente [ESF-C3-0.3](../02-requisitos/especificacao-funcional-v0.3.md). F47 retira Dicas e IA de todo o produto, incluindo a previsão anterior de futura IA. Atores Admin, Escritório e Promotores e demais decisões preservam as substituições já registradas. O conteúdo abaixo mantém o histórico da descoberta.

Atualização corrente em 10/11/2026. F41–F45 definem Admin, Escritório e Promotores, acesso por estados, ficha de histórico compartilhado e escopo pretendido ampliado com prazo a renegociar. As seções anteriores preservam o contexto de descoberta. A [ESF-C3-0.2](../02-requisitos/especificacao-funcional-v0.2.md) registra as substituições e a classificação corrente.

## Informações confirmadas nas fontes

A C3 Representação e Marketing atua em representação comercial de produtos automotivos, em Fortaleza/CE, com administradores, escritório e promotores, atendendo varejistas e fornecedores como Wega, Hella, Starke, Paraflu e NTN. WhatsApp, e-mail, planilhas e portais fazem parte da operação atual. Existem automações com Claude em navegadores autenticados, cuja substituição não foi aprovada para o MVP (F01 §§2–5).

O direcionamento confirmado é uma plataforma web responsiva, mobile-first, para até dez usuários iniciais. Promotores usam prioritariamente Android. Escritório utiliza notebooks e dispositivos Android/Apple. F13 consolida dois atores operacionais, Escritório e Promotores, além do perfil reservado Master para administração e ajustes do sistema.

O MVP será híbrido: centraliza registros, arquivos, acompanhamento e aprovações; atividades externas podem permanecer nos processos atuais. Pedidos exigem revisão e autorização humanas internas. Não haverá catálogo permanente de produtos, preços ou estoque próprio (F01 §§5–6).

## Problemas e objetivos propostos

| Hipótese de problema | Objetivo proposto | Evidência de benefício a definir |
|---|---|---|
| Informação distribuída entre conversas, planilhas e portais | Reunir referências e estados operacionais em um local | Medir tempo para localizar uma solicitação e seus documentos antes/depois |
| Versões e autorizações podem ser difíceis de reconstruir | Preservar versão da proposta, resposta, revisão e responsável | Verificar reconstrução de um caso completo, sem presumir automação externa |
| Visitas e campanhas usam controles separados | Associar visita, cliente, promotor e campanhas vigentes | Validar com promotor um atendimento com consulta de folder |
| Abastecimentos precisam de consulta centralizada | Registrar veículo, data, hodômetro, litros e valor | Conferir histórico e totais com amostra validada |

São hipóteses de benefício, sem percentuais de economia ou resultados financeiros prometidos. Frequência, gravidade e linha de base ainda dependem de entrevistas.

## Atores e limites propostos

| Ator | Participação prevista | Confirmação necessária |
|---|---|---|
| Master, perfil reservado de gerenciamento | Visão geral, gestão de contas, configurações e correções excepcionais. Desativa contas no desligamento com histórico preservado, conforme F14 | Classificar ações/campos de exceção no detalhamento — D04 |
| Escritório, ator operacional | Cadastros e ajustes da rotina, acesso operacional geral, revisão e autorização de pedidos, conforme F13/F14 | Detalhar campos e alcance dos dados — D04. Regras de revisão e versão aprovadas em F17 |
| Promotores | Visitas, campanhas, avisos referentes às visitas, visualização de combustível e métricas de compras do cliente, conforme F08 | Todos os clientes disponíveis para visita conforme F25. Avisos internos definidos em F26. Lançamento/consulta de combustível definidos em F27. Métricas aprovadas em F28, com fonte Excel a homologar |
| Cliente/varejista | Solicitar, responder e aprovar propostas por processo externo | Decisão, data, responsável e anexo da resposta definidos em F17 |
| Fornecedor | Decidir campanhas e receber pedidos externamente | Layouts e documentos — D01/D02; sem integração automática presumida |
| Responsável pelo projeto | Aprovar decisões e consolidar escopo | Identificação, substituto e disponibilidade — D16 |

## Recorte do MVP

Sete grupos preliminares: autenticação/permissões; cadastros essenciais; promotores/visitas; campanhas/folders; pedidos/propostas; veículos/abastecimentos; consultas e relatórios básicos. O detalhe rastreável consta na [matriz](../02-requisitos/matriz-requisitos.md). Indicadores, layouts e regras não definidos continuam pendentes, sem autorização para removê-los unilateralmente.

Wega é a única fonte disponível atualmente. Próximos fornecedores serão incluídos conforme aceite contratual e poderão fornecer planilha, PDF ou procedimento para obter dados no site. Cada fonte exige delimitação de processo, escopo e homologação (D01). Para Wega, a proposta PDF mostra código e Grupo como descrição, QTD, UNIT direto da planilha, TOTAL = QTD × UNIT arredondado para três casas decimais e MULTI mínimo. Exemplo de precisão monetária registrado como R$ 12,345. Após aprovação, PRODUTO e QTD são lançados no sistema do fornecedor (F11/F15/F16).

Avisos de visita, métricas de compras e os controles específicos de Master foram solicitados expressamente em F08. Essas alterações estão registradas para delimitação e avaliação de impacto. F28 definiu fonte Excel para valor comprado no período e última compra por cliente/fornecedor. A amostra e o tratamento das compras efetivas serão homologados. F26 definiu avisos internos criados pelo Escritório, por cliente e período, exibidos aos promotores na seleção do cliente.

Ficam fora do MVP as automações externas, importação genérica, múltiplos layouts ilimitados, catálogo permanente, GPS contínuo, metas/ranking, IA/áudio, notificações externas, tarefas completas, pagamentos automatizados, controle avançado de investimentos/premiações, manutenção de frota e BI avançado, conforme F01. Funções adicionais das planilhas não ampliam o escopo.

## Informações pendentes

D03 está resolvida em F17 e D05 em F18. D06 está resolvida operacionalmente em F23, com veículo fixo e posição de até cinco minutos. A homologação técnica da API segue pendente. Seguem os complementos de D01/D02/D04. Os marcos de D13 foram definidos em F12. As regras gerais de visita e conexão estão aprovadas em F18. Também dependem de resposta localização pontual, cadastros, campanhas, abastecimentos, relatórios, volumes, infraestrutura, equipe, cobrança, suporte e homologadores.

Cadastro de clientes e ajustes de rotina pertencem ao Escritório, conforme F25. Promotores consultam e visitam qualquer cliente cadastrado. Modo offline, regra de 500 m e horários especiais permanecem conforme as decisões de escopo anteriores. Não há stack, hospedagem, SLA, RPO ou RTO aprovados.

## Restrições confirmadas e visão futura

Valores aprovados são R$ 24.000 de implantação e R$ 8.000/mês por 80 horas, nas modalidades de 3, 6 ou 12 meses. Em F29, Ismael Zaccah informou que executará a implantação dentro dessa capacidade mensal de 80 h. F30 definiu a sequência de R$ 12.000 pré-MVP e R$ 12.000 pós-MVP, seguida do início do serviço mensal de suporte/adição de funcionalidades. A mensalidade paga o período já trabalhado. F31 define ciclo mensal contado da data de início do serviço e vencimento no fechamento da competência.

Os 30 dias corridos começam após o aceite da proposta e a assinatura do contrato, quando ambas as condições estiverem atendidas. O término corresponde à apresentação formal do MVP para testes. A C3 dispõe então de cinco dias úteis para homologar (F12, DEC-C12). A avaliação técnica ocorre nos primeiros cinco dias úteis da janela de desenvolvimento. A viabilidade técnica permanece pendente. Mudanças de escopo, preço ou prazo exigem aprovação bilateral (F01 §9).

A evolução poderá avaliar integrações, automações e indicadores adicionais por demanda priorizada e autorizada, sem compromisso de incluí-los na mensalidade de forma ilimitada. O backlog Pós-MVP é candidato, sem entrega ou data aprovada.



## Aprovações e versões dos pedidos

Conforme F17, a mesma pessoa do Escritório pode revisar e autorizar. A resposta externa do cliente é registrada com decisão, data, responsável e anexo. Alterações geram nova versão e preservam a anterior. Uma proposta alterada após autorização exige nova revisão e autorização. Rejeição registra motivo e decisão do Escritório entre revisar a proposta ou encerrar a solicitação.

## Regras gerais de visitas aprovadas

Conforme F18, cada promotor mantém uma visita aberta por vez. Check-in/out usam data e hora do sistema. Promotor ajusta motivo e observações durante a visita aberta. Master regulariza visitas encerradas ou esquecidas com justificativa e histórico. O registro é confirmado após salvar, com aviso e nova tentativa na falha. F19 definiu localização pela API do rastreador do veículo da empresa. F23 definiu vínculo fixo por promotor e posição de até cinco minutos. Acima do limite, usar justificativa e marcação para conferência.

## Origem da localização nas visitas

Conforme F19, a localização dos eventos de visita virá da API do rastreador do veículo da empresa usado pelo promotor. Essa decisão altera a exclusão anterior da API em F01 RF-06. A consulta deve preservar o horário informado pelo rastreador e o vínculo ao veículo. O levantamento documental confirmou descrição de última posição e validade do GPS, com homologação autenticada pendente. F23 definiu veículo fixo e idade máxima de cinco minutos. Posição antiga ou indisponível exige justificativa e conferência. Autenticação e disponibilidade da API serão homologadas tecnicamente. MC-01 registra o impacto ainda a estimar.


## Cadastros e clientes compartilhados

F25 aprovou D07 com acesso de todos os promotores a qualquer cliente cadastrado para consulta e visita. Cada cliente é identificado por estabelecimento/CNPJ único. Escritório mantém cadastros, associações a fornecedores e inativação com histórico. As visitas preservam o promotor autor. Master mantém contas e vínculo fixo com veículo, cujo cadastro é mantido pelo Escritório.

## Campanhas e avisos aprovados

F26 aprovou solicitações por Escritório/Promotores, um fornecedor e vários clientes-alvo por campanha. Escritório registra a decisão externa, folders e vigência. A campanha aparece ativa quando aprovada, com folder e no período vigente. Escritório cria avisos internos por cliente/período e pode cancelar campanhas com motivo. Vencimento e cancelamento preservam histórico.

## Abastecimentos aprovados

Conforme F27, Promotores registram e consultam abastecimentos do veículo fixo. Escritório lança para qualquer veículo e tem visão geral junto ao Master. Veículo, data, hodômetro, litros e total são obrigatórios. Quantidades e valores são positivos e o hodômetro respeita a sequência cronológica. Master corrige registros salvos com justificativa/histórico. Escritório pode lançar retroativos com data real e justificativa.

## Indicadores e exportações aprovados

F28 aprovou contagens de visitas abertas/encerradas, pedidos por situação/fornecedor e campanhas por situação/vigência, além de totais de litros/gastos por veículo/período. Filtros aplicam-se conforme consulta e acesso. As listagens de visitas, pedidos, campanhas e abastecimentos serão exportadas em Excel. Métricas de compras incluem valor no período e última compra por cliente/fornecedor, com fonte Excel cujo layout será homologado.

## Responsáveis e infraestrutura

F29 define Ismael Zaccah como desenvolvedor e Caio Costa, proprietário da C3, como responsável por validar requisitos, testar e aceitar entregas. A C3 custeará domínio, hospedagem/nuvem e futuros serviços de IA. Hospedagem/nuvem serão criadas no projeto, com custos a aprovar. O domínio costaltda.com é uma hipótese decorrente do e-mail informado. Titularidade e acesso serão confirmados. Volumes ainda desconhecidos exigem cenários de dimensionamento que contemplem crescimento.

## Condições de continuidade recebidas em F30

Horas não utilizadas expiram, com intenção de uso integral das 80 h. A garantia comercial de correção de defeitos acompanha a vigência da contratação mensal. A diretriz de rescisão é aviso de 30 dias, conclusão do mês contratado e pagamento da última mensalidade de R$ 8.000. F31 define suporte por WhatsApp/e-mail de segunda a sexta 9h–17h e encerramento no fim da competência em que se completam os 30 dias de aviso, com pagamento final de R$ 8.000 e sem multa adicional em 3/6/12 meses. As condições serão detalhadas no instrumento contratual sujeito à revisão jurídica.


