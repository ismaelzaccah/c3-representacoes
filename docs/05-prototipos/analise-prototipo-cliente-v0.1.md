# Análise funcional do protótipo enviado pela C3

Status PROPOSTO • UX-C3-0.2 • 10/11/2026 • Fontes F39–F46.

## Material e método

Arquivo de entrada `fontes-cliente/C3 Visitas.html`, acompanhado de `C3 Visitas_files`. A página principal contém o contêiner da plataforma de origem. A aplicação está em `C3 Visitas_files/saved_resource.html`. Ambos foram preservados. Foram separados os elementos da plataforma de publicação e a aplicação para navegação local isolada, com recursos já salvos e acesso de rede bloqueado durante a análise.

Foram identificadas as dez pessoas do seletor Ver como, conferidos os menus de todas elas e percorridas trinta combinações de perfil e tela com Caio, Gabriella e Daysilane. Foram examinados doze detalhes adicionais, incluindo fichas de cliente em perfis distintos, cadastro/edição de pessoas, performance detalhada e as etapas de seleção, contexto, relatório e check-out. Também foram lidos os dados, permissões, regras, filtros e eventos responsáveis pelos comportamentos. Os gráficos e as telas de Hoje/Painel foram inspecionados visualmente.

O cliente forneceu um protótipo clicável com dados de exemplo. A validação anterior de usabilidade é informação de Ismael. A análise presente examina os comportamentos observáveis e sua relação com as decisões do projeto. A aplicação usa datas, valores, posições, distâncias, cadastros e indicadores de demonstração. Nomes das pessoas foram reproduzidos por solicitação expressa. Telefones de pessoas presentes na fonte foram omitidos da versão derivada.

## Pessoas e atores

| Pessoa no seletor | Perfil | Referência territorial/vínculo no material |
|---|---|---|
| Caio | Admin | Gestão |
| Ana Paula | Admin | Gestão |
| Gabriella | Escritório | Operação administrativa |
| Airton | Escritório | Operação administrativa |
| Daysilane Uchôa | Promotor | CE · CLT |
| Walter Junior | Promotor | CE · CLT |
| Matheus Silva | Promotor | CE · CLT |
| João Ribeiro | Promotor | PI/MA · PJ |
| Valber Holanda | Promotor | MA · PJ |
| Peterson | Promotor | PA/AP · CLT |

F41 confirma três atores, Admin, Escritório e Promotores. Admin assume as funções antes denominadas Master. Os estados e vínculos da tabela reproduzem referências do protótipo, cuja manutenção cadastral caberá ao Admin. Cada promotor continua com veículo exclusivo, conforme F35. Identificação real de veículo e Upcar segue pendente.

## Navegação e disposição observadas

| Área | Organização observada | Tratamento no protótipo C3 ajustado |
|---|---|---|
| Estrutura | Menu lateral em computador, cabeçalho com marca/perfil e navegação móvel resumida com Mais | Estrutura incorporada, com abas móveis junto ao cabeçalho e conteúdo empilhado. A adaptação permite ao visualizador exibir a página completa |
| Hoje | Saudação, situação atual, retomada da visita, próxima ação, metas, clientes a visitar, tarefas e trajetos | Prioridade para visita aberta/check-in, veículo, metas e contexto regional |
| Painel | Indicadores, velocímetros, equipe hoje, avisos, trajetos e vendas por linha | Organização representada por ator, com dados de exemplo e origem Upcar indicada para telemetria |
| Clientes | Busca por nome/CNPJ, lista com cidade, promotor da última visita, linhas e tempo sem visita | Busca regional e ficha com histórico compartilhado, conforme F42 |
| Ficha do cliente | Cadastro, linhas/segmentos, visitas, tarefas e números comerciais | Contexto preservado, cadastro editável na região e identificação de autoria das visitas |
| Visita | Seleção → contexto → relatório → check-out, motivos, contato, observações, próxima tarefa e foto | Jornada incorporada. A abertura passa a ser registrada na simulação ao confirmar check-in, antes do relatório final |
| Metas/campanhas | Velocímetro, meta/feito/falta, contribuição de promotores e lançamento de resultado | Representado no escopo pretendido, com solicitação/decisão/folder preservados do fluxo aprovado anteriormente |
| Números | Arquivo original, entrada de vendido/estoque/projeção por cliente/linha e situação de atualização | Promotor responsável por cobrar a cada visita e enviar números da sua região, F44 |
| Despesas | Tipo, valor, data, comprovante, aprovação e totais | Tipos de despesa representados. Combustível mantém veículo, litros e hodômetro obrigatórios |
| Performance | Custo/visita, km/visita, combustível/km, comparação com meses próprios e meta de economia | Gráficos reproduzidos como modelo proposto. Fórmulas, bases, exclusões e premiação exigem detalhamento |
| Tarefas | Abertas/atrasadas/feitas, cliente, responsável, data e lembretes | Representação local e criação de tarefa. Integração de lembretes fica para homologação |
| Dicas e IA | Registro de dicas por área/linha, áudio, consulta e sugestão para o dia | Fluxo representado com resposta simulada e fonte autorizada; fornecedor/modelo e transcrição são decisões técnicas pendentes |
| Equipe | Pessoas, estados, vínculo e área de atuação | Referências de equipe incorporadas |
| Configurações | Pessoas, modelos de perfil, permissões individuais e regras operacionais | Admin concentra contas e ajustes. Editor avançado de permissões individuais permanece em detalhamento, com três perfis funcionais fixos |
| Pedidos | A referência de visitas não contém o fluxo completo de cotação/revisão/autorização definido na descoberta | Módulo de pedidos mantido no estudo ajustado, vinculado à versão e com MULTI mínimo |

## Gráficos observados e significado de negócio

| Representação | Uso na referência | Regra ou dependência |
|---|---|---|
| Velocímetro semicircular 0–125% | Visitas do mês/dia e resultado de campanhas | Meta, feito e falta identificados. Cores da referência dividem até 70%, 70–100% e acima de 100%. Marco de ritmo do mês usa dias úteis |
| Barras horizontais | Realizado por promotor/linha e custo por visita por mês | Comparar unidades homogêneas. Rótulos mantêm valor e denominador |
| Colunas mensais | Custo por visita, combustível no mês e km/visita | Comparação do promotor com o próprio histórico. Escala começa em zero; a referência usa linha de meta e selos dos três menores valores |
| Variação e indicadores | Diferença percentual em relação ao mês anterior e razões de custo/atividade | Tratar ausência de dados e denominador zero. Dados fictícios não demonstram economia real |
| Meta de economia | Média dos três meses mais econômicos, limitada inferiormente a 85% da média | Fórmula observada, ainda PROPOSTO para aprovação específica e para esclarecer combustível, outras despesas, períodos parciais e reembolsos recusados |

Na versão ajustada, gráficos de colunas usam área proporcional ao celular e rótulos maiores. Tabelas extensas têm rolagem local. Os valores de meta, custo e campanhas são exemplos. O mínimo de oito e o ideal de doze visitas/dia foram aprovados em F44. A fórmula de economia e seus efeitos comerciais ainda precisam de validação própria.

## Permissões observadas e divergências corrigidas

| Observação na referência | Relação com a regra de negócio | Tratamento |
|---|---|---|
| Admin tem todas as permissões e configurações. Escritório tem acesso operacional sem gestão de contas | Compatível com a divisão esclarecida em F41 | Admin substitui o nome Master na versão corrente |
| Promotor tem clientes filtrados por UF | Divergia da decisão anterior de acesso geral | F42 aprova a restrição por estados, substituindo a decisão anterior nesse alcance |
| Ficha mostra visitas de outros promotores | Divergia de limitar todas as consultas à autoria | F42 aprova histórico compartilhado na ficha regional. Histórico pessoal segue próprio |
| Modelo de perfil marca num_edit falso para Promotor, mas a tela e a condição `ou é promotor` permitem enviar números | Permissão declarada e comportamento efetivo divergem | F44 confirma a permissão e a responsabilidade. Versão ajustada alinha o modelo à função |
| Lista de números renderiza todos os clientes e exportação usa toda a base NUMS | Pode ultrapassar a região autorizada | Lista e prévia de exportação passam pelo mesmo alcance regional |
| Ações de cadastro/linhas podem ser executadas pelo promotor na região | Exigia ampliar a regra de cadastro antes reservada ao Escritório | F43 aprova cadastro e atualização de contato/endereço/linhas na região. Retificação excepcional de identidade continua sob Admin |
| Editor permite criar perfis e alterar permissões individuais | Excede a gestão de contas com papéis fixos registrada anteriormente | Permissões funcionais ficam explícitas. O editor avançado requer definição própria |
| Escritório vê performance e pode alterar piso econômico por campo de tela | Parâmetro altera regra geral sem permissão de configuração | Campo fica de leitura para Escritório/Promotor, ajuste reservado ao Admin |
| Avisos e algumas ações dependem mais da exibição que de autorização central | Protótipo não constitui controle de segurança de servidor | Restrições locais foram reforçadas nos fluxos representados. A matriz orienta a implementação futura |
| Check-in da referência só consolida o registro ao finalizar a jornada | Pode ocultar uma visita em andamento se o processo for interrompido | A versão ajustada cria o registro aberto ao confirmar entrada e atualiza o mesmo registro no encerramento |
| Trajeto/quilômetros da referência são gerados com dados de exemplo e algumas operações usam aleatoriedade | Não comprova integração ou medição | F43 mantém rastreador do veículo como origem. Fonte Upcar e dependência técnica ficam identificadas |
| IA e downloads dependem de capacidades da plataforma de publicação | Não demonstra integração contratada nem funcionamento independente | Respostas e documentos têm prévias locais. Processamento e integração efetivos serão homologados |

## Regras operacionais conciliadas

F44 aprova mínimo de oito e ideal de doze visitas/dia, janela da primeira visita 8h–8h20, identificação da última após 17h30, distância mínima de 500 m da residência na primeira/última, distância máxima de 70 m do cliente e motivo para terceira visita semanal. F45 permite primeira visita fora da janela com justificativa e aviso ao Admin. A posição continua sendo do rastreador, com até cinco minutos, mantendo a exceção justificada já aprovada para posição antiga/indisponível.

Na referência, Daysilane possui uma exceção individual para visitas repetidas em contas-chave. F46 determina exigir justificativa de todos, inclusive Daysilane e contas-chave. A versão ajustada aplica a regra geral. Limite por distância depende de coordenadas verificáveis do cliente e residência, dados válidos do rastreador e política para posição indisponível. A referência simula Google/Receita e utiliza dados locais; essas telas não comprovam serviços externos disponíveis.

## Escopo e próximos fechamentos

F42 inclui metas, performance, tarefas, despesas adicionais, trajetos/Waze e IA no escopo pretendido, com prazo a renegociar. A mudança está registrada em MC-02. O recorte contratado, o esforço e a implantação ainda dependerão da especificação revisada e da negociação. As estimativas anteriores referem-se à base anterior. Preços aprovados continuam no registro comercial, sujeitos a eventual decisão bilateral futura.

Pendências de detalhamento incluem fórmula econômica e premiação, exigência/guarda de comprovantes, tratamento de cliente sem números disponíveis, canais/cadência de lembrete, formatos adicionais de exportação, critérios da IA e georreferenciamento de residência/clientes. As dependências estão no [adendo de requisitos](../02-requisitos/alteracoes-escopo-v0.2.md).

