# Registro de pendências D01–D16

Status PROPOSTO • Versão 0.21 • 10/11/2026 • Fontes F01, F06–F31.

As decisões gerais de negócio e condições comerciais coletadas estão consolidadas. D14/D15 foram resolvidas em F31. D01/D02/D04/D11/D12/D16 mantêm dependências de materiais, especificação, dimensionamento ou logística identificadas. A integração do rastreador e a planilha de compras exigem validação técnica e estimativa. A revisão de prontidão propõe iniciar a Etapa 2 com essas dependências documentadas. Registrar fonte, responsável, data e impacto de cada definição futura.

## Prioridade imediata — primeiro bloco de descoberta

| ID | Decisão a esclarecer e perguntas objetivas | Material/evidência de resolução | Interlocutor sugerido e aprovação | Rastreabilidade e impacto |
|---|---|---|---|---|
| D01 | Wega é a fonte disponível. Próximas fontes dependem do aceite contratual e poderão ser planilha, PDF ou procedimento no site. Delimitar conjunto inicial e processo de inclusão por fornecedor | F09 e F16. Receber materiais quando disponíveis e definir tratamento manual/automatizado, validações, escopo e impacto no prazo | Responsável esclareceu F16 em 09/11/2026. Demais fontes aguardam oportunidade contratual e materiais | RF-05.03/05.12; DEC-F18/F21. Estado PARCIALMENTE ESCLARECIDA para o conjunto contratual de fontes |
| D02 | Regras gerais RESOLVIDAS. PDF com código e Grupo como descrição, UNIT direto da planilha e TOTAL = QTD × UNIT com três casas decimais. Detalhar precisão de UNIT, empates de arredondamento e eventual arquivo de envio | F15/F16. Homologar exemplo preenchido e casos de arredondamento. Modelo de envio ao fornecedor permanece condicionado à referência específica | Responsável definiu F16 em 09/11/2026. Escritório valida exemplos na homologação | RF-05.04/05.12/05.13; DEC-F19/F20. Estado PARCIALMENTE ESCLARECIDA apenas quanto aos detalhes de especificação/homologação |
| D03 | Mesma pessoa do Escritório pode revisar e autorizar. Resposta do cliente registra decisão, data, responsável e anexo. Alteração gera nova versão. Mudança após autorização exige nova revisão/autorização. Rejeição registra motivo e decisão de revisar ou encerrar | Aprovação expressa F17, 09/11/2026. Evidência vinculada à versão e histórico preservado | Responsável aprovou as cinco regras apresentadas | RF-05.05–05.11; DEC-F22–F25. Estado RESOLVIDA |
| D04 | Atores, responsabilidades e acesso geral aprovados, incluindo clientes compartilhados, visitas próprias, avisos e abastecimentos por veículo | F13/F14/F25–F28 consolidam as regras gerais. Campos, fonte detalhada de compras e permissões por operação serão especificados | Responsável aprovou os blocos. Matriz detalhada na Etapa 2 | RF-01–07 conforme matriz. Regras gerais RESOLVIDAS, detalhamento PENDENTE |
| D13 | Início após aceite da proposta e assinatura do contrato, com ambas as condições atendidas. Término na apresentação formal do MVP para testes, opção A | Resposta expressa do responsável F12, 09/11/2026. Avaliação de viabilidade nos primeiros cinco dias úteis. Homologação em até cinco dias úteis após apresentação | Definido pelo responsável para o planejamento e futura redação contratual | DEC-C12, complementa DEC-C06/07. Estado RESOLVIDA. Capacidade/viabilidade tratadas em D12 e planejamento |

## Prioridade seguinte — comportamento operacional e qualidade

| ID | Perguntas a resolver | Material/evidência de resolução | Interlocutor sugerido e aprovação | Rastreabilidade e impacto |
|---|---|---|---|---|
| D05 | Uma visita aberta por promotor, horário do sistema, edição de motivo/observações enquanto aberta, regularização excepcional por Master com justificativa/histórico e confirmação após salvar, com aviso/repetição na falha | Aprovação expressa F18, 09/11/2026. Cenários de exceção e repetição serão detalhados conforme a regra aprovada | Responsável aprovou as cinco regras apresentadas | RF-03.02–04/07; DEC-F26–F29. Estado RESOLVIDA quanto às regras gerais |
| D06 | Veículo fixo por promotor, posição pela API do rastreador no check-in/out e idade máxima de cinco minutos. Posição antiga ou indisponível permite registro com justificativa e conferência | F19/F23 definem regras operacionais. F22 informa credenciais recebidas. Homologação da API e impacto da MC-01 seguem como atividades técnicas | Responsável aprovou F23 em 10/11/2026. Técnico valida integração na etapa autorizada | RF-03.07/09; RNF-02/03/11; DEC-F30/F31. Estado RESOLVIDA quanto às regras operacionais |
| D07 | CNPJ único por estabelecimento, campos básicos obrigatórios, manutenção pelo Escritório e clientes acessíveis a todos os promotores. Associações com vários fornecedores, inativação com histórico e responsabilidades sobre contas/veículos definidas | Aprovação expressa com ressalva F25, 10/11/2026. Todos os promotores podem visitar qualquer cliente cadastrado | Responsável aprovou o bloco. Campos e validações serão especificados | RF-02.01–04; RF-03.01; RF-06.01; DEC-F32–F35. Estado RESOLVIDA quanto às regras gerais |
| D08 | Campanhas solicitadas por Escritório/Promotores, um fornecedor e vários clientes, decisão externa registrada pelo Escritório, folders e vigência. Exibição durante visita, avisos por cliente/período e cancelamento com motivo | Aprovação expressa F26, 10/11/2026. Campo completo e arquivos serão detalhados na especificação | Responsável aprovou o bloco apresentado | RF-04.01–07; RF-03.08; DEC-F36–F39. Estado RESOLVIDA quanto às regras gerais |
| D09 | Promotor lança e consulta seu veículo fixo. Escritório lança para qualquer veículo e registra retroativos com data real/justificativa. Campos obrigatórios, litros/valor positivos, hodômetro cronologicamente coerente. Master corrige com histórico | Aprovação expressa F27, 10/11/2026. Campos e validações completas serão especificados | Responsável aprovou as seis regras apresentadas | RF-06.01–05; DEC-F40–F43. Estado RESOLVIDA quanto às regras gerais |
| D10 | Indicadores operacionais, filtros e exportações Excel aprovados. Compras por cliente/fornecedor com valor no período e data da última compra. Fonte em planilha Excel | Aprovação F28, 10/11/2026. Obter amostra da planilha de compras e detalhar atualização, identificação e cálculos | Responsável aprovou o conjunto e informou a origem | RF-07.01–05; DEC-F44–F47. Estado RESOLVIDA quanto às regras gerais, fonte detalhada em homologação |

## Pendências de viabilidade, governança e contratação

| ID | Perguntas a resolver | Material/evidência de resolução | Interlocutor sugerido e aprovação | Rastreabilidade e impacto |
|---|---|---|---|---|
| D11 | C3 arca com custos de domínio, infraestrutura e futura IA. Hospedagem/nuvem serão criadas. Domínio e titularidade a confirmar. Volumes desconhecidos, com crescimento esperado | F29. Técnico propõe cenários de escala identificados como hipóteses, infraestrutura, custos, retenção e recuperação | Ismael prepara análise, Caio confirma domínio/contas e aprova orçamento. Volumes serão levantados com a C3 | RNF-02/04–09; DEC-A04/C15. Diretrizes recebidas, parâmetros técnicos PENDENTES |
| D12 | Ismael Zaccah desenvolverá o sistema e a implantação dentro de 80 h mensais | Informação expressa F29. Estimativa precisa incluir análise, desenvolvimento, testes, documentação e reuniões. Competência e contabilização comercial em D14 | Ismael informou a capacidade. Planejamento deverá confrontar esforço e disponibilidade | DEC-C13. Equipe/capacidade RESOLVIDAS, viabilidade e cronograma PENDENTES |
| D14 | Implantação R$ 12.000 pré/R$ 12.000 pós-MVP. Serviço mensal começa depois, em ciclos contados da data de início, com pagamento no fechamento | F30/F31, DEC-C16/C20. Registrar datas efetivas no contrato | Ismael/Caio formalizam as condições. Revisão jurídica na etapa contratual | Estado RESOLVIDA quanto às condições gerais |
| D15 | Horas expiram. Garantia durante contratação mensal. Suporte WhatsApp/e-mail, segunda a sexta 9h–17h. Saída no fim da competência em que completarem 30 dias de aviso, última mensalidade de R$ 8.000 e sem multa adicional em 3/6/12 meses | F30/F31, DEC-C17–C22. Procedimentos e cobertura serão redigidos na minuta | Ismael/Caio formalizam. Revisão jurídica antes de assinatura | Estado RESOLVIDA quanto às condições gerais |
| D16 | Caio Costa, proprietário da C3, valida requisitos, testa entregas e formaliza aceite | Resposta F29, 10/11/2026. Disponibilidade e rito serão detalhados com o responsável | Caio Costa como homologador principal. Ismael organiza a apresentação das entregas | DEC-C14. Responsável principal RESOLVIDO, logística de homologação a planejar |

Embora D16 não esteja no bloco prioritário solicitado, identificar interlocutores é pré-condição logística para coletar D01–D04 e D13. D12 pode ser levantada internamente em paralelo à coleta, sem envolver automaticamente o cliente.

## Registro de resposta

### D07 aprovada com ressalva em F25

As regras abaixo foram aprovadas em F25, com alteração no item de carteira. O documento continua PROPOSTO. A fonte da proposta original foi D07, F03 e a divisão de responsabilidades de F14.

| Tema | Regra proposta para decisão |
|---|---|
| Identificação do cliente | Cadastro por estabelecimento, identificado por CNPJ único. Confirmar eventual atendimento a clientes sem CNPJ |
| Campos do cliente | Nome/razão social, CNPJ, endereço, cidade e UF obrigatórios. Bairro, CEP, telefone, contato e e-mail complementares |
| Cadastro e manutenção | Escritório realiza cadastro e ajustes rotineiros. Promotor consulta e seleciona clientes. Correções excepcionais seguem a atribuição do Master |
| Acesso a clientes | Todos os promotores podem consultar e visitar qualquer cliente cadastrado. Cada promotor consulta seus próprios registros de visita. Escritório e Master têm visão geral |
| Fornecedores | Um cliente pode estar associado a vários fornecedores. Escritório mantém esses cadastros e associações operacionais |
| Inativação | Escritório pode inativar cliente/fornecedor, preservando histórico de operações |
| Contas e veículos | Master mantém nome, e-mail, perfil e situação das contas e o vínculo fixo promotor–veículo. Escritório mantém cadastro do veículo, com placa, identificação e referência externa do rastreador |

## Sequência de fechamento da descoberta

### D08 aprovada em F26 — campanhas e avisos

As regras deste bloco foram aprovadas pelo responsável em F26. O documento mantém status PROPOSTO. A proposta foi derivada de F01 RF-04, dos avisos de F08 e do acesso compartilhado a clientes definido em F25.

| Tema | Regra proposta |
|---|---|
| Solicitação | Escritório e Promotores podem solicitar campanha para cliente cadastrado |
| Vínculos | Campanha pertence a um fornecedor e pode atender vários clientes-alvo |
| Decisão externa | Escritório registra aprovação ou rejeição do fornecedor e mantém histórico da solicitação |
| Folders e vigência | Escritório anexa um ou mais folders e informa início e fim da vigência |
| Exibição | Campanha aparece como ativa quando aprovada, com folder e dentro da vigência. Todos os promotores a visualizam ao selecionar um cliente-alvo |
| Avisos | Escritório cria avisos internos vinculados a cliente e período de exibição. Promotores os veem ao selecionar o cliente |
| Encerramento | Fim da vigência retira a campanha da lista de ativas e preserva histórico. Escritório pode cancelar com motivo registrado |

Os tipos/limites de arquivos e campos completos serão detalhados na especificação com base na aprovação de F26.

### D09 aprovada em F27 — abastecimentos

As regras deste bloco foram aprovadas pelo responsável em F27. O documento mantém status PROPOSTO. A origem da proposta foi F01 RF-06, veículo fixo em F23 e responsabilidades em F14/F25.

| Tema | Regra proposta |
|---|---|
| Lançamento | Promotor registra abastecimento de seu veículo fixo. Escritório pode registrar abastecimento de qualquer veículo |
| Campos | Veículo, data do abastecimento, hodômetro, litros e valor total obrigatórios |
| Validações | Litros e valor total positivos. Hodômetro consistente com a sequência cronológica do histórico do veículo |
| Consulta | Promotor visualiza histórico e gastos do seu veículo. Escritório e Master têm visão geral |
| Correção após salvar | Master corrige com justificativa e histórico de alterações |
| Data passada | Escritório pode lançar abastecimento retroativo com data real e justificativa |

Precisão dos campos, mensagens e exemplos de hodômetro serão detalhados com base em F27. A integração ao rastreador cobre a localização das visitas. Abastecimentos seguem o processo aprovado neste bloco.

### D10 aprovada em F28 — consultas, indicadores e exportações

O responsável aprovou este bloco em F28 e informou planilha Excel como origem das compras faturadas. O documento mantém status PROPOSTO. A amostra e o layout da fonte serão necessários ao detalhamento e à homologação.

| Tema | Regra proposta para decisão |
|---|---|
| Visitas | Contagem de abertas e encerradas por período, cliente e promotor |
| Pedidos | Contagem de solicitações por situação e fornecedor |
| Campanhas | Contagem por situação e vigência |
| Abastecimentos | Totais de litros e valor gasto por veículo e período, respeitando acesso de F27 |
| Filtros | Período, cliente, promotor, fornecedor, veículo e situação, conforme a consulta |
| Exportações | Excel das listagens filtradas de visitas, pedidos, campanhas e abastecimentos. Campos e layouts serão especificados |

Para compras, foram aprovados valor comprado no período e data da última compra por cliente/fornecedor. A origem é planilha Excel, conforme F28. Solicitar amostra anonimizada quando disponível, com significado das colunas e período coberto. Precisam ser identificáveis cliente, fornecedor, data e valor das compras para as métricas aprovadas.

O detalhamento da fonte de compras deve explicar se os valores são faturados, líquidos de devoluções/cancelamentos e qual data define a compra. Modo de alimentação, periodicidade e duplicidade serão especificados conforme os dados reais. Esse material integra as dependências técnicas para RF-07.05.

### Respostas de D11/D12/D16 recebidas em F29

Equipe/capacidade e homologador foram informados em F29. Custos de infraestrutura são da C3. Volumes ainda precisam de levantamento e parâmetros técnicos serão analisados posteriormente.

| Tema | Pergunta objetiva |
|---|---|
| Equipe de implantação | Ismael Zaccah, com implantação dentro da capacidade de 80 h mensais |
| Homologação | Caio Costa, proprietário da C3 |
| Infraestrutura | Criada no projeto, com custos pagos pela C3/Caio. Domínio `costaltda.com` provável a confirmar, assim como titularidade/acesso às contas |
| Volumes iniciais | Desconhecidos. Dimensionamento deverá usar cenários explícitos e considerar crescimento |

F29 altera a premissa anterior de capacidade de implantação separada. A capacidade disponível de Ismael é 80 h/mês, com uso na implantação. D14 precisa esclarecer competência remunerada e contabilização de serviços. Ismael prepara dimensionamento e Caio confirma domínio e aprova custos antes de contratação.

### D14/D15 resolvidas em F30/F31

| Tema | Decisão pendente |
|---|---|
| Início do serviço mensal | RESOLVIDO em F30, serviço mensal começa após a sequência 50% pré-MVP/50% pós-MVP e é pago após o mês trabalhado |
| Competência e vencimento | RESOLVIDO em F31, ciclos mensais contados do início do serviço, com pagamento no fechamento |
| Horas não utilizadas | RESOLVIDO em F30, expiram. Intenção de usar integralmente as 80 h |
| Garantia | Condição comercial recebida em F30, correção de defeitos durante a contratação mensal. Detalhar cobertura na etapa contratual |
| Suporte | RESOLVIDO em F31, WhatsApp/e-mail, segunda a sexta, 9h–17h |
| Rescisão | RESOLVIDA em F31, fim da competência em que se completam os 30 dias de aviso, última mensalidade de R$ 8.000 e ausência de multa adicional em 3/6/12 meses |

Valores aprovados são R$ 24.000 de implantação e R$ 8.000/mês por 80 h. F30/F31 definem serviço mensal após o ciclo do MVP, contado do início e pago no fechamento da competência. A redação jurídica será tratada na etapa contratual. O [parecer de prontidão](../06-planejamento/prontidao-etapa-2.md) classifica as dependências remanescentes e o trabalho proposto para a próxima etapa.

F24 orienta conduzir os blocos seguintes a cada resposta, com coleta contínua até a revisão de prontidão para a Etapa 2.

| Bloco | Pendências | Decisões necessárias |
|---|---|---|
| 1. Cadastros e alcance dos dados | D07 e parte de D04 | Proposta acima, campos, carteira e associações |
| 2. Campanhas e avisos | D08, parte de D04/D10 | Solicitantes, registro da decisão externa, clientes-alvo, folders, vigência, estados e conteúdo dos avisos |
| 3. Abastecimentos | D09 | Quem lança, campos obrigatórios, consistência de hodômetro e correções |
| 4. Consultas e métricas | D10 e parte de D04 | Fonte das compras efetivas, indicadores e exportações finitos, acesso por perfil |
| 5. Capacidade e operação | D11/D12/D16 | Volumes, equipe/dedicação, responsáveis, infraestrutura e disponibilidade para homologar |
| 6. Limites de contratação | D01/D02/D14/D15 | Tratamento das próximas fontes, critérios de cálculo/saídas, competências, garantia, suporte, saldo e adicionais |

A passagem à Etapa 2 requer decisões de negócio suficientes para especificar os fluxos e pendências remanescentes identificadas com responsável, impacto e momento de resolução. Exemplos de arquivos e homologação da API serão tratados como dependências técnicas. A estimativa de esforço e o parecer de viabilidade seguem os marcos já registrados. A revisão jurídica ficará vinculada aos documentos contratuais posteriores.

### D03 resolvida em F17

O responsável aprovou as cinco regras de revisão, autorização, evidência, versionamento e rejeição apresentadas na conversa. O registro DEC-F22–F25 e a matriz de requisitos refletem essa aprovação. A coleta segue para D05.

### D05 aprovada em F18 — visitas

As cinco regras abaixo foram aprovadas pelo responsável em F18, em 09/11/2026. O documento mantém status PROPOSTO. As referências a proposta na última coluna registram a origem histórica das regras.

| Tema | Regra proposta | Fonte da proposta |
|---|---|---|
| Visitas simultâneas | Cada promotor mantém uma visita aberta por vez | Hipótese para resolver D05, com base em F01 RF-03 |
| Horários | Check-in e check-out recebem data e hora do sistema quando confirmados | F01 RF-03; proposta para D05 |
| Edição durante a visita | Promotor pode ajustar motivo e observações enquanto a visita estiver aberta | Proposta para D05 |
| Visita encerrada ou esquecida | Master faz a correção excepcional ou regularização, com justificativa e histórico, preservando os registros originais | F14 e proposta de aplicação a D05 |
| Falha de conexão | O registro é confirmado quando o sistema recebe e salva a operação. Na falha, exibir aviso e permitir nova tentativa | F01 RF-03; proposta para D05 |

A forma de geolocalização e suas exceções serão discutidas separadamente em D06. D05 está registrada nas decisões DEC-F26–F29 e nos requisitos relacionados.

### D06 aprovada com ressalva em F19 — localização pelo veículo

Origem aprovada é a API do rastreador do veículo da empresa. Nos eventos de check-in/out, a localização será vinculada ao veículo usado pelo promotor. Escritório e Master consultam os registros para conferência. Em falha de localização, a regra aprovada permite justificativa e indicação de conferência.

A especificação pública F21 documenta última posição conhecida, data informada pelo rastreador e validade do GPS. A captura da posição e o evento de visita podem ter horários distintos. O schema consultado oferece validade, enquanto a disponibilidade de precisão numérica depende de confirmação do provedor.

| Complemento pendente | Decisão ou material necessário |
|---|---|
| Vínculo promotor–veículo | RESOLVIDO em F23, veículo fixo por promotor. Cadastro e identificação externa serão detalhados na especificação |
| Atualidade da posição | RESOLVIDA em F23, até cinco minutos no evento. Acima do limite, justificativa e conferência |
| Autenticação | Credenciais já fornecidas ao responsável conforme F22. Confirmar uso efetivo de login/senha/token frente ao contrato v3 durante a homologação técnica |
| Homologação técnica | Conta autorizada com acesso aos veículos da C3, exemplos de posição válida, antiga, inválida e ausente, limites e frequência do provedor |
| Retenção | Responsabilidade, prazo e acesso registrados em RNF-02 e D11 |

MC-01 registra a alteração da exclusão anterior de API de rastreadores, com estimativa e impacto ainda pendentes. Ver [levantamento da API](../04-arquitetura/levantamento-api-rastreador.md). D06 está funcionalmente resolvida em F23. As regras de D05 definem horário do evento e confirmação de salvamento.

### D06 resolvida operacionalmente em F23

Em 10/11/2026, o responsável definiu veículo fixo e aceitou cinco minutos como idade máxima da posição. Esses subitens estão RESOLVIDOS. Posição acima do limite segue com justificativa e marcação para conferência, conforme a exceção aprovada. A homologação técnica deverá validar posição atual, de exatamente cinco minutos, antiga, inválida e ausente.

### Histórico de disponibilidade de credenciais — F22

Em 10/11/2026, o responsável informou que João Vitor já lhe entregou login, senha e token. A disponibilidade das credenciais está esclarecida. Configuração protegida no servidor e validação autenticada serão atividades da etapa técnica autorizada. A diferença documental entre F20/F21 fica como item de homologação. A descoberta operacional segue com vínculo promotor/veículo e idade máxima da posição.

### Histórico dos complementos de pedidos e propostas em F15

F15 resolveu fornecedor da amostra, formato PDF, código/descrição e origem do preço unitário. F16 complementou a descrição como Grupo e aprovou QTD × UNIT com três casas decimais. As respostas gerais de cotação estão consolidadas. Permanecem detalhes de especificação e exemplos de homologação.

### Fontes futuras e precisão esclarecidas em F16

Apenas Wega está disponível. Os demais fornecedores dependem do aceite contratual, com fontes potencialmente distintas, planilha, PDF e procedimento no site. O conjunto de capacidades a contratar permanece pendente de delimitação. A coleta poderá ser externa no MVP híbrido. Registrar separadamente necessidade de extração/importação de PDF ou obtenção automática caso essas capacidades sejam demandadas.

Para a resposta sobre “três casas decimais nos centavos”, o registro adota três casas no valor em reais, por exemplo R$ 12,345. A precisão e a fórmula estão definidas, enquanto o modo de tratar empate de arredondamento será detalhado na especificação.

### Respostas recebidas em 09/11/2026

Origem e aprovação das diretrizes são a mensagem do responsável F08. Materiais F09 e F10 foram recebidos e inspecionados localmente. Cada resposta aparece na linha D01–D04 e no registro DEC-F07–F12. D13 recebeu pedido de explicação. O fechamento de cada pendência depende apenas dos complementos agora indicados.

F11 complementou as respostas na mesma data. Encerrados os subitens de significado de MULTI, natureza do CRUD de perfis, manutenção do nome Escritório e destino do lançamento PRODUTO/QTD. D01/D02/D04 continuam parciais por seus demais pontos. F12 encerrou a escolha dos marcos de D13.

### Histórico do esclarecimento de D13

D13 define dois marcos. Primeiro, qual evento inicia os 30 dias corridos, por exemplo assinatura, pagamento inicial ou confirmação de que os materiais essenciais estão disponíveis. Segundo, qual evento cumpre a entrega prevista nesses 30 dias.

| Alternativa para o término | Exemplo relativo | Efeito no planejamento |
|---|---|---|
| A. Disponibilização para homologação | Ao fim dos 30 dias, o MVP é apresentado para a C3 testar. A janela de cinco dias úteis de homologação começa depois dessa apresentação | O aceite pode acontecer após o período de 30 dias |
| B. Aceite concluído | Ao fim dos 30 dias, a C3 já concluiu a homologação e formalizou o aceite | A entrega para testes precisa acontecer antes, reservando a janela de homologação dentro dos 30 dias |

O responsável escolheu a alternativa A em F12. O evento inicial é o atendimento de ambas as condições, aceite da proposta e assinatura do contrato. A avaliação técnica ocorre nos primeiros cinco dias úteis dessa janela. A entrega para testes abre o período de cinco dias úteis de homologação. A segunda parcela segue vinculada ao aceite. A viabilidade técnica dos 30 dias segue pendente.

### Aprovação da divisão de responsabilidades em F14

O responsável aprovou a divisão geral de cadastros e ajustes de rotina para Escritório e gestão de contas, configurações e correções excepcionais para Master. Aprovou também histórico de alterações e desativação no desligamento, preservando autoria e vínculos dos registros. Estes subitens estão RESOLVIDOS. O detalhamento de campos, exemplos de exceção e alcance dos dados permanece para a especificação futura.

### Histórico da identificação de atores em F13

F13 encerrou a dúvida. Os atores operacionais são Escritório e Promotores. Escritório é a denominação corrente para as funções antes chamadas Administradores. Master é o perfil reservado de gerenciamento com visão geral e ajustes elevados, incluindo criação de contas e manutenção de dados de clientes/funcionários. A identificação dos grupos está resolvida. D04 permanece parcial para definir ações e campos específicos, alcance de registros e demais detalhes operacionais.

Modelo a preencher somente quando houver informação: `Dxx | resposta | evidência/localização | fornecido por | data | aprovado por/data | RFs/decisões afetados | mudança necessária | estado`.

Estados de acompanhamento sugeridos: ABERTA → EM ESCLARECIMENTO → AGUARDANDO APROVAÇÃO → RESOLVIDA. Mudança de escopo segue controle próprio e aprovação bilateral; não encerrar pendência apenas por hipótese técnica.






## Encaminhamento após autorização da Etapa 2

Status PROPOSTO • Atualização de 10/11/2026 • F32.

A Etapa 2 foi autorizada e produziu o pacote ESF-C3-0.1. Os estados históricos D01–D16 permanecem neste registro. Os detalhes correntes estão na [especificação](../02-requisitos/especificacao-funcional-v0.1.md) e na [entrega da Etapa 2](../06-planejamento/situacao-etapa-2.md).

| Pendência de origem | Tratamento corrente | Próxima evidência |
|---|---|---|
| D01/D02 | RF-05, PT-03/04, DP-02/05/06 | PDF preenchido, precisão, fornecedores e layouts |
| D03/D04 | RF-01/02/05 e permissões | Revisão dos campos Master, exportações e exceções |
| D05/D06 | RF-03, D-06 e FL-02/03 | Homologação de horários, autenticação e permissões API |
| D07/D08/D09 | RF-02/04/06 e dicionário | Revisão dos limites, datas e detalhes cronológicos |
| D10 | RF-07, PT-06, DP-01 | Excel de compras com chaves, ajustes e atualização |
| D11/D12/D15 | RNFs e DP-04 | Volumes, infraestrutura, custos e objetivos operacionais |
| D13 | Marco aprovado mantido | Datas reais após eventos contratuais |
| D14/D16 | Decisões comerciais e critérios CA | Revisão contratual e aprovação da especificação |

## Atualização durante arquitetura preliminar

F35 resolve a exclusividade do veículo. D-04/RF-02.04.02 foram atualizados na revisão 1 da ESF-C3-0.1. A identificação efetiva de cada promotor/veículo/Upcar continua dependente da lista da C3.

A continuidade F36 resultou no pacote ARQ-C3-0.1. D12 passa a contar com [estimativa preliminar](../06-planejamento/backlog-estimativas-v0.1.md), ainda sujeita à revisão e provas. A faixa de esforço excede a capacidade nominal de um mês e requer tratar a viabilização do prazo. DP-01–06 seguem vinculadas aos materiais e aprovações pertinentes. O [relatório corrente](../06-planejamento/situacao-etapa-3.md) centraliza as revisões possíveis agora.

## Encaminhamento de prazo e telas — F38

Ismael decidiu tratar a negociação dos requisitos funcionais para o prazo de trinta dias durante a elaboração/apresentação da proposta, DEC-C23. O risco D12 permanece sinalizado. As opções deverão preservar IDs, dependências, efeitos e aprovação bilateral do recorte final. O escopo de referência continua na ESF-C3-0.1 revisão 1.

O [protótipo UX-C3-0.1](../05-prototipos/roteiro-prototipos-v0.1.md) está disponível para revisão de linguagem e navegação. Os materiais DP-01–06 continuam pendentes conforme coleta junto à C3.

## Revisão com protótipo do cliente — F39–F45

Atores, alcance por UF, histórico compartilhado, cadastro pelo promotor, cobrança/envio de números, regras operacionais e origem Upcar dos trajetos foram esclarecidos nas respostas. A especificação corrente passa a ESF-C3-0.2. MC-02 amplia o escopo pretendido e torna necessária nova estimativa/prazo a negociar. D12 continua sinalizada sob essa base revisada.

As novas dependências DP-07–13 estão no [adendo](../02-requisitos/alteracoes-escopo-v0.2.md), incluindo georreferência, histórico de rotas, custos/fórmulas, comprovantes, canais de lembrete, IA, ausência de números e exceção de contas-chave. DP-01–06 permanecem vinculadas aos materiais solicitados.

F46 resolve a exceção individual de repetição, exigindo justificativa de todos. A fórmula econômica permanece PROPOSTO por decisão expressa. O [relatório da atualização](../06-planejamento/atualizacao-prototipo-cliente-v0.2.md) consolida resultados, regras e dependências.

## Atualização por F47

DP-10 está CANCELADA. Dicas e IA foram retiradas do produto e deixam de gerar solicitação de fornecedor, dados, transcrição, orçamento ou integração. A parcela de futura IA em D11 também foi retirada. As demais dependências conservam seus estados. Referência corrente [ESF-C3-0.3](../02-requisitos/especificacao-funcional-v0.3.md).

## Planejamento e proposta após F50

Status PROPOSTO • Atualização de 11/11/2026.

Ismael validou a experiência do protótipo e autorizou continuar. D12 passa a usar o [dimensionamento revisado](../06-planejamento/backlog-estimativas-v0.2.md), cujas faixas exigem revisão de Ismael. A [proposta preliminar](../07-comercial/proposta-tecnico-comercial-preliminar-v0.1.md) apresenta o escopo pretendido e o prazo a negociar. Permanecem prioritários Excel de compras/números, vínculos de pessoas/UF/veículos/Upcar, volumes, infraestrutura e definições operacionais DP-07–09/11–13. A validação visual conserva o estado próprio das decisões funcionais ainda propostas.
