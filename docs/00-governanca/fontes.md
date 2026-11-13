# Inventário de fontes

Status PROPOSTO • Versão 0.21 • 10/11/2026.

| ID | Fonte e localização | Evidência disponível | Uso e limite |
|---|---|---|---|
| F01 | Prompt Mestre v1.2 de 06/11/2026; anexo local `C:/Users/maelz/.codex/attachments/19c4bb11-eb7c-40f1-91e4-91e5c433c5fe/Pasted text.txt` | Texto lido no diagnóstico | Diretrizes, decisões expressas, RFs preliminares, exclusões e condições comerciais. O anexo está fora do repositório |
| F02 | [FLUXOGRAMA.xlsx](../../fontes-cliente/FLUXOGRAMA.xlsx), aba Planilha1, 13.967 bytes | Células e textos de desenhos extraídos no diagnóstico; sem renderização visual | Operação atual; não é lista integral do MVP nem estimativa de engenharia |
| F03 | [APP CAIO COSTA PROMOTORES.xlsx](../../fontes-cliente/APP%20CAIO%20COSTA%20PROMOTORES.xlsx), aba Planilha1, 11.772 bytes | Células e texto de desenho extraídos no diagnóstico; sem renderização visual | Necessidades preliminares, sujeitas aos limites de F01 |
| F04 | Artifact C3 Visitas, endereço registrado no diagnóstico | Descrição fornecida em F01; sem nova inspeção externa | Referência de interação, sem força contratual, comprovação de implementação ou identidade visual obrigatória |
| F05 | [.gitignore](../../.gitignore) | Regra `fontes-cliente` | Preservar exclusão dos originais do Git |
| F06 | Repositório e [diagnóstico preliminar](../diagnostico-preliminar-v0.1.md) | Inspeção local e análise anterior | Diagnóstico é documento derivado, não substitui fontes primárias |
| F07 | Mensagem do responsável autorizando a Etapa 1, nesta conversa, 06/11/2026 | Aprovação do diagnóstico com ressalvas e sete atividades autorizadas | Todos os novos documentos PROPOSTO; sem implementação, instalação, envio, publicação ou avanço à Etapa 2. Mantidos valores e separação da evolução |
| F08 | Respostas do responsável a D01/D02/D03/D04 e pedido de esclarecimento de D13, nesta conversa, 09/11/2026 | Diretrizes expressas sobre materiais, MULTI, lançamento, revisores, canal de resposta e perfis | Fonte atual das decisões funcionais. Substituições e acréscimos registrados em decisões e pendências |
| F09 | [LISTA COMPLETA ELETROPARTS.xlsx](../../fontes-cliente/LISTA%20COMPLETA%20ELETROPARTS.xlsx), 342.790 bytes | Uma aba visível Sheet1, 3.839 linhas de dados e cabeçalho A1:S1. Leitura estrutural e de células, em modo somente leitura | Amostra Wega, identificada em F15. Demais fornecedores têm layouts próprios ainda a receber e delimitar |
| F10 | [cotação a ser enviada ao cliente.jpeg](../../fontes-cliente/cota%C3%A7%C3%A3o%20a%20ser%20enviada%20ao%20cliente.jpeg), 9.203 bytes | Imagem examinada visualmente, 321 × 141 px. Cabeçalhos PRODUTO, QTD, UNIT, TOTAL, MULTI | Referência visual para proposta em PDF. F15 define código e descrição em PRODUTO e UNIT direto da planilha. Fórmula e arredondamento pendentes |
| F11 | Respostas do responsável às três perguntas complementares, nesta conversa, 09/11/2026 | MULTI é mínimo e permite 7 quando vale 6. Escritório pode manter o nome. CRUD significa gestão de contas de funcionários pelo gerente geral. PRODUTO/QTD são lançados no sistema do fornecedor, como Wega | Esclarece regras de D01/D02/D04 e complementa F08. Registro funcional em DEC-F13–F15 |
| F12 | Definição de D13 pelo responsável, nesta conversa, 09/11/2026 | Início após aceite da proposta e assinatura do contrato. Opção A para o término, com entrega para homologação | Resolve os marcos de D13 para planejamento. Parecer de viabilidade e data concreta de início dependem dos respectivos dados |
| F13 | Esclarecimento final de atores pelo responsável, nesta conversa, 09/11/2026 | Dois atores operacionais, Escritório e Promotores. Master é perfil reservado de gerenciamento, com visão geral, criação de contas e ajustes elevados em dados de clientes e funcionários | Resolve a identificação dos atores de D04. As atribuições operacionais antes chamadas Administradores passam a Escritório. Campos e ações exclusivos do Master serão detalhados |
| F14 | Aprovação expressa “sim” à divisão de responsabilidades proposta, nesta conversa, 09/11/2026 | Escritório realiza cadastros e ajustes de rotina. Master gerencia contas, configurações e correções excepcionais. Alterações mantêm histórico de autoria. Desligamento por desativação da conta, preservando registros anteriores | Aprova a regra geral de D04 e o tratamento de desligamento. Exemplos de campos e ferramentas apresentados na pergunta serão classificados no detalhamento |
| F15 | Respostas do responsável sobre fornecedores e proposta, nesta conversa, 09/11/2026 | Amostra pertence à Wega. Cada fornecedor tem layout próprio. PRODUTO mostra código e descrição. UNIT vem diretamente do preço da planilha. Proposta entregue em PDF | Resolve identificação da amostra, conteúdo de PRODUTO, origem de UNIT e formato de saída. Lista de layouts, origem da descrição e cálculo/arredondamento de TOTAL seguem pendentes |
| F16 | Complementos do responsável sobre descrição, totalização e futuras fontes, nesta conversa, 09/11/2026 | Descrição vem de Grupo. Aprova TOTAL = QTD × UNIT com três casas decimais. Apenas Wega disponível agora. Próximos fornecedores dependem do aceite contratual e podem fornecer planilha, PDF ou procedimento no site | Resolve descrição e regra geral de totalização. Próximas fontes exigem identificação do processo, formato e tratamento a contratar |
| F17 | Aprovação expressa das cinco regras propostas para D03, nesta conversa, 09/11/2026 | Mesma pessoa do Escritório pode revisar e autorizar. Registrar decisão, data, responsável e anexo da resposta. Alteração gera nova versão e preserva anterior. Mudança após autorização exige nova revisão/autorização. Rejeição registra motivo e decisão de revisar ou encerrar | Resolve D03 e autoriza prosseguir na coleta das próximas decisões de descoberta |
| F18 | Aprovação expressa das cinco regras propostas para D05, nesta conversa, 09/11/2026 | Uma visita aberta por promotor. Data/hora do sistema no check-in/out. Promotor edita motivo/observações enquanto aberta. Master regulariza visita encerrada/esquecida com justificativa e histórico. Confirmação após salvar, com aviso e nova tentativa na falha | Resolve as regras gerais de D05. A próxima decisão de descoberta é D06, localização pontual |
| F19 | Aprovação com ressalva de D06 pelo responsável, nesta conversa, 09/11/2026 | Promotor usa veículo da empresa. A API do rastreador fornecerá os dados de localização | Altera origem de D06 e o limite anterior de integração com rastreadores. MC-01 registra impacto pendente |
| F20 | Orientação atribuída ao responsável técnico João Vitor, reproduzida pelo usuário em F19 | Documentação Upcar. Autenticação por login, senha e token de API, com dados limitados pelas permissões do usuário | Relato fornecido pelo usuário. Fluxo de autenticação requer conciliação com F21 |
| F21 | [Documentação Upcar](https://upcar.rastrosystem.com.br/api/v3/docs) e [OpenAPI](https://upcar.rastrosystem.com.br/api/v3/openapi.yaml), consultadas em 09/11/2026 | Documentação pública v3 com JWT, veículos e última posição. Cópia local em `fontes-cliente/upcar-openapi-v3-2026-11-09.yaml` | Especificação observada, com homologação autenticada pendente. Ver levantamento em grupo D |
| F22 | Esclarecimento do responsável, nesta conversa, 10/11/2026 | João Vitor já forneceu ao responsável login, senha e token para uso na implementação futura | Disponibilidade das credenciais informada. Configuração protegida e homologação da autenticação serão realizadas na etapa técnica autorizada |
| F23 | Definições operacionais do responsável para D06, nesta conversa, 10/11/2026 | Cada promotor utiliza veículo fixo. Idade máxima aceita da posição é cinco minutos. Acima do limite, registrar justificativa e marcação para conferência | Resolve vínculo operacional e atualidade da posição. Homologação autenticada e avaliação de impacto permanecem como trabalho técnico |
| F24 | Orientação do responsável para prosseguir na descoberta, nesta conversa, 10/11/2026 | Conduzir as próximas dúvidas até reunir condições para avançar de etapa | Continuidade da coleta por blocos, com registro de cada resposta. Limite da Etapa 1 segue em F07 |
| F25 | Aprovação com ressalva do bloco D07 pelo responsável, nesta conversa, 10/11/2026 | Aprova identificação, campos, manutenção, associações, inativação e veículos. Ressalva que todos os promotores podem visitar qualquer cliente cadastrado | Resolve regras gerais de D07. Cliente tem acesso compartilhado entre promotores para consulta/seleção de visita. Registros operacionais mantêm autoria |
| F26 | Aprovação expressa do bloco D08 pelo responsável, nesta conversa, 10/11/2026 | Campanhas solicitadas por Escritório/Promotores, um fornecedor e vários clientes-alvo, decisão externa registrada pelo Escritório, um ou mais folders, vigência e exibição ao selecionar cliente. Avisos internos por cliente/período. Cancelamento com motivo e histórico | Resolve regras gerais de campanhas e avisos. A coleta segue para abastecimentos em D09 |
| F27 | Aprovação expressa do bloco D09 pelo responsável, nesta conversa, 10/11/2026 | Promotor lança/consulta abastecimentos do veículo fixo, Escritório lança para qualquer veículo, campos obrigatórios definidos, litros/valor positivos e hodômetro consistente. Master corrige com justificativa/histórico. Escritório lança retroativos com data real e justificativa | Resolve regras gerais de abastecimentos. Próximo bloco D10, indicadores, filtros, exportações e fonte das compras |
| F28 | Aprovação de D10 e informação de origem pelo responsável, nesta conversa, 10/11/2026 | Indicadores operacionais, filtros, exportação Excel das listagens e métricas de valor comprado no período/última compra por cliente e fornecedor aprovados. Fonte das compras é planilha Excel | Resolve indicadores e origem geral. Amostra, layout, campos, frequência de atualização e tratamento de duplicidades/cancelamentos serão detalhados e homologados |
| F29 | Respostas sobre equipe, aceite, infraestrutura e volumes, nesta conversa, 10/11/2026 | Ismael Zaccah desenvolverá dentro das 80 h mensais. Caio Costa, dono da C3, valida requisitos e entregas. Domínio `costaltda.com` inferido do e-mail, a confirmar. Hospedagem/nuvem serão criadas no projeto. C3/Caio arca com custos, inclusive futura IA. Volumes desconhecidos e crescimento esperado | Capacidade de implantação informada altera a premissa anterior de capacidade separada. Competência de cobrança e alocação comercial seguem em D14. Escalabilidade será dimensionada com cenários identificados como hipóteses |
| F30 | Definições comerciais do responsável, nesta conversa, 10/11/2026 | Pagamento 50% pré-MVP e 50% pós-MVP. Depois começa o primeiro mês de suporte/adição de funcionalidades, pago posteriormente ao mês trabalhado. Horas expiram e há intenção de usar as 80 h. Garantia durante a contratação mensal. Rescisão com aviso de 30 dias, conclusão do mês contratado e última mensalidade de R$ 8.000 | Altera a regra de início do serviço mensal e a referência anterior de primeira mensalidade após contratação. Confirmar ciclo/competência, vencimento exato, alinhamento do aviso e eventual multa. Canal/horário de suporte ainda aguardam resposta |
| F31 | Confirmações comerciais finais do responsável, nesta conversa, 10/11/2026 | Competência mensal contada da data de início, com pagamento no fechamento. Suporte por WhatsApp e e-mail, segunda a sexta, 9h–17h. Confirma término ao fim da competência em que se completam os 30 dias de aviso, com última mensalidade de R$ 8.000 e sem multa adicional nas modalidades de 3/6/12 meses | Resolve D14/D15 quanto às decisões comerciais gerais. Regra corrente de vencimento é o fechamento do ciclo. Instrumento final permanece sujeito à revisão jurídica prevista |

Hierarquia de F01: aprovação expressa do responsável → especificação contratual aprovada → originais do cliente → observações do artifact → hipóteses técnicas. F07 rege o alcance desta etapa. Não foi localizada especificação contratual aprovada.

## Identificação dos originais

| Arquivo | SHA-256 de referência |
|---|---|
| FLUXOGRAMA.xlsx | `326531634FFE9974EB8924EF73FE1EAAB1A6AFC2A2B451AAADB06562E4136531` |
| APP CAIO COSTA PROMOTORES.xlsx | `F674ED999BC7B6E21A18C07E4D018C252A80955CB04F00C3E32551AA2D6EBEFE` |
| LISTA COMPLETA ELETROPARTS.xlsx | `499BAAA48357555D3E54D4FE78FF426B5FFBCC163CDE05E9247A2D376AF08A47` |
| cotação a ser enviada ao cliente.jpeg | `AC9C886E02D7960329645B2117E9CDE56B9831AFECB0A6DD3F88FDE01CC0D33E` |
| upcar-openapi-v3-2026-11-09.yaml | `07E31A3CC263D09FE1D4F25706B52DEDE46A762839A8C26594BAF8F4157EB74C` |

Não modificar originais nem adicioná-los ao Git. Backup e responsável pela custódia ainda precisam ser definidos; a exclusão do Git não resolve essa pendência.

## Materiais ausentes

Amostra Wega e referência visual recebidas em F09/F10. F15/F16 definem PDF, código acompanhado de Grupo como descrição, preço unitário da planilha e totalização em três casas decimais. As próximas fontes serão identificadas conforme aceite contratual. Aguardam delimitação de fornecedores, materiais e procedimentos, além de exemplos preenchidos para homologação e detalhes de permissões, métricas e avisos. Rever a coleta conforme o [registro de pendências](pendencias.md).

## Observações da amostra recebida em D01

F09 contém cabeçalhos em A1:S1, dimensão declarada A1:U3840 e ausência de conteúdo em T/U. Foram encontradas 3.839 linhas de dados com código de produto preenchido, sem códigos repetidos na leitura dos valores das células. Ausência de fórmulas na aba. A renderização visual e a homologação de importação permanecem etapas posteriores.

| Localização | Campo observado | Relação proposta a validar |
|---|---|---|
| A1 | Cód Produto | Código exibido em PRODUTO, conforme F15 |
| C1 | Grupo | Descrição exibida junto ao código em PRODUTO, conforme F16 |
| E1 | Qtde Múltiplo Venda | Candidato a MULTI. F11 define quantidade mínima e confirma 7 unidades como válidas quando o mínimo vale 6. Validar o mapeamento da coluna na homologação |
| F1 | Embalag Caixa Fechada | Campo distinto de E. Necessidade na regra comercial a esclarecer |
| G1 | Vlr Preço Liquido-Tabela 329 (imp) | Preço usado diretamente como UNIT. TOTAL = QTD × UNIT com arredondamento para três casas decimais, conforme F15/F16 |
| H1:J1 | Alíquota IPI, Alíquota ICMS, CST | Colunas presentes na entrada. A diretriz F15 determina uso direto do preço da planilha para UNIT |
| B1:D1, K1:S1 | Classe, grupo, linha de veículo, dados de identificação/logística e lançamento | Dados presentes na entrada, cuja utilização depende das regras aprovadas |

F15 identifica a amostra como Wega e F16 seleciona Grupo para a descrição. Vigência, tratamento de dados e variantes serão verificados na homologação. A interpretação registrada para a precisão monetária é três casas após a vírgula, por exemplo R$ 12,345. Regras de empate do arredondamento e precisão exibida de UNIT serão detalhadas na especificação.

## Fontes acrescentadas na Etapa 2

| ID | Fonte e localização | Evidência | Uso e limite |
|---|---|---|---|
| F32 | Mensagem do responsável em 10/11/2026, “Sim, vamos a etapa 2.” | Autorização expressa nesta conversa | Iniciar especificação funcional detalhada. Aprovação dos detalhes novos e implementação dependem de atos próprios |
| F33 | [Receita Federal — CNPJ alfanumérico](https://www.gov.br/receitafederal/pt-br/acesso-a-informacao/acoes-e-programas/programas-e-atividades/cnpj-alfanumerico) | Referência pública consultada na Etapa 2 | Compatibilidade de CNPJ numérico/alfanumérico. Validação proposta em D-02 |
| F34 | [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/) | Recomendação pública consultada na Etapa 2 | Meta técnica proposta de acessibilidade RNF-07. Conformidade depende de avaliação futura |

## Continuidade de planejamento e confirmação operacional

| ID | Fonte | Evidência | Efeito |
|---|---|---|---|
| F35 | Resposta de Ismael na conversa em 10/11/2026 | “cada veículo é exclusivo do promotor.” | Confirma exclusividade de veículo por promotor. D-04 e RF-02.04.02 passam a vedar vínculo vigente simultâneo com outro promotor |
| F36 | Instrução de Ismael na conversa em 10/11/2026 | “enquanto essas informações não chegam vamos continuar, assim que chegarem eu lhe repasso” | Autoriza continuidade do planejamento com informações atuais, mantendo coleta de materiais como dependência |
| F37 | Documentação pública oficial e licenças consultadas na Etapa 3 | Links no [estudo de tecnologias](../04-arquitetura/avaliacao-stack-v0.1.md) | Fundamenta avaliação documental. Composição exata, execução, custo e homologação permanecem propostos/pendentes |

## Direção de negociação e protótipos

| ID | Fonte | Evidência | Efeito |
|---|---|---|---|
| F38 | Orientação de Ismael em 10/11/2026 | Levar o conflito de prazo à proposta para negociar requisitos funcionais e caber no prazo estipulado, seguido de “próximo” | Preservar o sinal de risco e preparar negociação futura. Autoriza continuidade com protótipos, mantendo escopo de referência e detalhes propostos identificados |

## Protótipo C3 recebido e conciliação funcional

| ID | Fonte | Evidência | Uso e limite |
|---|---|---|---|
| F39 | Arquivo C3 Visitas.html e pasta C3 Visitas_files | Navegação local, leitura de aplicação, estilos e dados. Contêiner SHA-256 395718D400CB474F6D9DAE84373B5F9048AAF3651414BE7506CFE29AAE091457. Aplicação saved_resource.html SHA-256 51D2EA1FA1C093CCB4FCDD63036C83FEA1C54768DE159150E647DF2F8E57637D | Trinta combinações de perfil/tela e doze detalhes adicionais examinados. Material de exemplo, originais preservados e ignorados pelo Git |
| F40 | Solicitação de Ismael de 10/11/2026 | Analisar minuciosamente a referência, ajustar funções/permissões, copiar nomes/perfis e extrair/aplicar a marca, com prioridade móvel | Autoriza análise e derivação do estudo UX-C3-0.2 |
| F41 | Resposta sobre Admin | Três atores Admin, Escritório e Promotores. Admin assume funções antes chamadas Master | Substitui nomenclatura/organização anterior na versão corrente |
| F42 | Respostas sobre região, histórico e ampliação | Restringir por estados, compartilhar histórico na ficha e incluir metas/performance/tarefas/despesas/trajetos/IA no escopo pretendido, com prazo a renegociar | Aprovação de diretrizes, requer especificação e reestimativa da ampliação |
| F43 | Respostas sobre cadastro e telemetria | Promotor cadastra/atualiza contato/endereço/linhas na região. Rastreador do veículo continua fonte de trajetos e quilômetros | Regras conciliadas no adendo ESF-C3-0.2 |
| F44 | Respostas sobre regras e números | Adotar 8/12 visitas, primeira 8h–8h20, última após 17h30, residência 500 m, cliente 70 m e motivo da terceira visita semanal. Promotor envia e cobra números em cada visita | Regras aprovadas no escopo pretendido. Fórmulas e dependências adicionais seguem detalhamento |
| F45 | Resposta sobre atraso da primeira visita | Permitir fora da janela com justificativa e aviso ao Admin | Define tratamento da exceção de horário |

| ID | Fonte | Evidência | Efeito |
|---|---|---|---|
| F46 | Respostas complementares de Ismael em 10/11/2026 | Exigir justificativa de repetição de todos. Manter fórmula econômica como proposta para validar depois | Remove exceção individual de Daysilane/contas-chave na versão ajustada. Fórmula econômica não recebe aprovação funcional definitiva |

## Ajustes solicitados ao protótipo e ao produto

| ID | Fonte | Evidência | Efeito |
|---|---|---|---|
| F47 | Solicitação de Ismael em 10/11/2026 | Retirar Dicas e IA do protótipo e de todo o sistema. Ações em cards sobrepostos com animação ascendente/descendente, X, confirmação de descarte/envio e fechamento após sucesso. Login demonstrativo com campos vazios. Indicador de página selecionada e Mais abaixo do menu móvel | MC-04 retira RF-12 e cancela DP-10. UX-C3-0.3 e ESF-C3-0.3 consolidam a direção aprovada e o detalhamento proposto |

## Consolidação de interface e continuidade em 11/11/2026

| ID | Fonte | Evidência | Efeito |
|---|---|---|---|
| F48 | Solicitação anterior de Ismael, registrada nesta consolidação | Corrigir faixa branca que prejudicava a interface e fazer o modal subir até o centro da página | Altura disponível do navegador, card centralizado e animação inferior preservada na UX-C3-0.3 |
| F49 | Solicitação de Ismael sobre data e hora | Rodapé deve acompanhar data e hora do sistema | Relógio local do dispositivo com atualização automática e virada de dia verificada |
| F50 | Continuidade de Ismael em 11/11/2026 | O protótipo está ótimo, vamos continuar | Validação da experiência como referência por Ismael e continuidade ao planejamento/proposta preliminar. Requisitos pendentes e condições contratuais conservam seus estados próprios |

## Restauração e ajustes específicos

| ID | Fonte | Evidência | Efeito |
|---|---|---|---|
| F51–F53 | Mensagens anteriores sobre triagem e seleção da versão 1.0 | Análise de requisitos, primeiro filtro e esclarecimentos correlatos | Desdobramentos documentais e protótipo 0.4 desfeitos por F54. Conservados aqui como referência histórica da reversão |
| F54 | Correção de Ismael em 12/11/2026 | Desfazer o primeiro filtro em todos os documentos, descartar v0.4 e partir da v0.3. Remover cards indicados e página Metas, reposicionar Avisos/Minhas tarefas, remover sino superior, incluir CPF por perfil e placa do veículo para Promotor | Restaura a base funcional 0.3 e produz UX-C3-0.5 com os ajustes específicos de interface e cadastro |
| F55 | Ajustes de Ismael em 12/11/2026 | Preencher as placas dos promotores com dados fictícios e usar CPF/CNPJ no lugar do e-mail na tela de login | Atualiza a demonstração UX-C3-0.5 e os identificadores apresentados na entrada |
