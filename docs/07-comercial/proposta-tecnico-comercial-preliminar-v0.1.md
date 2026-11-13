# C3 — Proposta técnico-comercial preliminar

Status PROPOSTO • Versão 0.1 • 11/11/2026 • Material interno para revisão de Ismael Zaccah.

Base documental ESF-C3-0.3 e UX-C3-0.3. Preparada após a validação do protótipo por Ismael. A revisão com Caio Costa deverá fechar escopo, materiais, prazo e critérios da implantação.

## 1. Objetivo

Organizar a operação da C3 em uma plataforma web com prioridade para o uso em celular. A solução reunirá atendimento aos clientes, visitas, campanhas, pedidos, despesas e informações comerciais, com histórico das ações e acesso conforme a responsabilidade de cada pessoa.

## 2. Contexto da operação

Pedidos e decisões chegam por WhatsApp e e-mail. Fornecedores disponibilizam informações em formatos próprios, e o faturamento ocorre nos sistemas dos fornecedores. Promotores usam veículos da empresa e obtêm informações comerciais durante as visitas. A plataforma centralizará os registros necessários para acompanhar essas atividades e suas decisões.

## 3. Perfis de acesso

| Perfil | Responsabilidade prevista |
|---|---|
| Admin | Visão geral, gestão de contas, estados de atuação, vínculos de veículos, configurações e ajustes reservados com histórico |
| Escritório | Rotinas administrativas, pedidos, revisão/autorização, campanhas, cadastros e consultas permitidas |
| Promotores | Visitas, cadastro e atualização de clientes nos estados de atuação, histórico compartilhado na ficha, números comerciais, tarefas, campanhas e despesas permitidas |

Cada promotor utiliza um veículo fixo e exclusivo. Clientes são acessíveis conforme os estados de atuação. A ficha do cliente reúne as visitas da equipe com identificação de autoria.

## 4. Escopo pretendido para negociação

| Grupo | Entrega prevista | Rastreabilidade |
|---|---|---|
| Acesso e cadastros | Contas, permissões, clientes, fornecedores, veículos e vínculos com histórico | RF-01/02 e RF-06.01 |
| Visitas | Entrada/saída, relatório, histórico, avisos, justificativas e verificação de localização do veículo | RF-03 e RF-03.10–13 |
| Campanhas | Solicitação, decisão externa registrada, folders, vigência, clientes-alvo e acompanhamento | RF-04 e RF-08.02 |
| Pedidos | Entrada de dados, cotação PDF, versões, resposta do cliente, revisão e autorização | RF-05 |
| Combustível e despesas | Lançamentos, comprovantes conforme política a definir, consultas, aprovação e correções permitidas | RF-06 e RF-10 |
| Informação comercial | Compras, vendido, estoque, projeção, original recebido e atualização identificada | RF-07 e RF-07.06 |
| Metas e performance | Acompanhamento de visitas, campanhas e indicadores de custo e quilômetros | RF-08 |
| Tarefas e lembretes | Responsável, cliente, vencimento, conclusão/reabertura e avisos com canais a definir | RF-09 |
| Trajetos e orientação | Histórico e quilômetros do rastreador, com orientação de destino no Waze | RF-11 |
| Qualidade operacional | Acesso protegido, arquivos privados, histórico, backup, testes e orientação de uso | RNF-01–11 e controles transversais |

O [anexo funcional corrente](../02-requisitos/especificacao-funcional-v0.3.md) identifica regras, estados de aprovação e dependências de cada grupo. A contratação deverá definir quais itens integram cada marco, inclusive os condicionados à entrega de materiais.

## 5. Regras operacionais destacadas

Promotores poderão visitar e atualizar clientes dos seus estados de atuação. A meta aprovada é de oito visitas diárias, com ideal de doze. A primeira visita tem janela de 8h a 8h20, com justificativa e aviso ao Admin quando ocorrer fora dela. A última visita deve ocorrer após 17h30. As regras incluem distância de pelo menos 500 m da residência nos eventos aplicáveis, limite de 70 m do cliente e justificativa na terceira visita semanal para todos os promotores.

A localização virá da API Upcar do veículo. A posição terá idade máxima de cinco minutos para uso regular. Posição antiga ou indisponível seguirá o tratamento de exceção justificada e conferência. O levantamento técnico deverá demonstrar como os dados disponíveis suportam os eventos e trajetos.

Os promotores serão responsáveis por solicitar os números comerciais em cada visita e poderão encaminhar os dados e o arquivo recebido. Periodicidade, ausência de retorno e revisão de valores precisam ser concluídas com a C3.

## 6. Fluxo de pedidos e cotação

O Escritório registra a solicitação e utiliza a fonte do fornecedor. A amostra disponível é a planilha Wega. A cotação apresenta código e descrição pela coluna Grupo, preço unitário da planilha e total calculado por quantidade multiplicada pelo preço, com três casas decimais conforme a regra aprovada. MULTI corresponde à quantidade mínima permitida.

O cliente recebe a proposta em PDF. Sua resposta será registrada com a evidência do WhatsApp ou e-mail de origem. A revisão e a autorização internas ficam vinculadas à versão. Alterações geram nova versão e nova revisão/autorização. Após autorização, o pedido é lançado no sistema do fornecedor com PRODUTO e QTD para processamento e faturamento.

Cada novo fornecedor deverá ter seu formato e procedimento identificados antes do fechamento da respectiva entrega. A C3 e Ismael validarão exemplos de totalização e o PDF final.

## 7. Experiência de uso

A referência de interface é o [protótipo UX-C3-0.3](../05-prototipos/prototipo-navegavel-v0.3.html), validado por Ismael. O celular tem navegação junto ao cabeçalho e opções complementares em Mais. O computador tem menu lateral. Formulários abrem em cards que sobem até o centro da tela, com confirmação de envio e proteção dos dados digitados ao fechar. O rodapé acompanha a data e a hora do dispositivo.

O estudo usa cenários demonstrativos. A homologação da plataforma avaliará dados persistidos, perfis reais e integrações conforme os critérios contratados.

## 8. Direção técnica

A arquitetura proposta reúne aplicação web responsiva, servidor, banco relacional e armazenamento privado de arquivos. As permissões serão aplicadas no servidor. A integração com o rastreador utilizará credenciais protegidas. Backup, restauração, registros de falha e histórico de alterações compõem a preparação operacional. A escolha definitiva de serviços depende do dimensionamento e orçamento de infraestrutura.

## 9. Benefícios esperados

- Consulta conjunta do cadastro, das visitas e das informações do cliente.
- Acompanhamento de pedidos e autorizações por versão.
- Visibilidade sobre campanhas, tarefas, despesas e resultados da equipe.
- Dados rastreáveis para apoiar a gestão e a conferência operacional.

## 10. Prazo e marcos

O escopo pretendido foi ampliado durante a análise do protótipo do cliente, e o prazo será renegociado. A referência comercial anterior de 30 dias corridos deverá ser revista junto ao conjunto de entregas e à capacidade disponível de Ismael, informada como 80 horas mensais. A viabilidade técnica dessa janela permanece pendente.

O marco inicial acordado exige aceite da proposta e assinatura do contrato. A apresentação formal da versão contratada abre o período de cinco dias úteis de homologação pela C3. Caio Costa será o responsável pela homologação.

| Marco proposto | Resultado a apresentar |
|---|---|
| Fechamento de escopo e prazo | Anexo de requisitos, critérios, materiais e cronograma negociados |
| Base e provas técnicas | Acesso, cadastros, vínculos e resultados das provas de integração |
| Operação de campo | Visitas, campanhas, tarefas e despesas demonstráveis |
| Pedidos e informação comercial | Cotação, decisões e dados comerciais conciliados |
| Gestão e preparação de entrega | Metas, indicadores, trajetos e verificações integradas |
| Apresentação e homologação | Versão entregue para testes, registro de divergências e aceite |

Datas e duração dos marcos serão preenchidas após a revisão técnica e a negociação. O [dimensionamento interno](../06-planejamento/backlog-estimativas-v0.2.md) registra as hipóteses que Ismael deverá revisar antes de definir o calendário com a C3.

## 11. Investimento de implantação

O investimento aprovado é de R$ 24.000, dividido em duas parcelas de R$ 12.000. A primeira corresponde ao momento pré-MVP. A segunda é vinculada ao aceite do MVP. O anexo e o cronograma negociados deverão identificar o conjunto de entregas coberto pela implantação.

## 12. Suporte e evolução mensal

Após o ciclo de entrega e pagamento do MVP, inicia-se o serviço mensal de R$ 8.000 por 80 horas. A competência é contada da data de início do serviço e paga no seu fechamento. As horas expiram ao final da competência. Atendimento por WhatsApp e e-mail, de segunda a sexta, das 9h às 17h.

A garantia comercial está vinculada à vigência da contratação mensal, conforme a condição já acordada. A rescisão exige comunicação prévia de 30 dias e encerramento conforme o fechamento da competência aplicável, com o pagamento final do serviço prestado. A redação completa dessas condições será consolidada na etapa contratual para revisão.

## 13. Infraestrutura e responsabilidades

A C3 custeará domínio, hospedagem, nuvem e serviços necessários à operação, mediante orçamento e aprovação. O domínio e a titularidade das contas precisam ser confirmados. Ismael será responsável pelo desenvolvimento e pela preparação técnica. Caio Costa validará os critérios e homologará a entrega. Gabriella e Airton apoiarão a coleta dos materiais administrativos.

## 14. Materiais prioritários para fechar o planejamento

| Material ou definição | Finalidade |
|---|---|
| Excel de compras e números comerciais, com exemplo e periodicidade | Fechar origem, campos, atualização, revisão e indicadores |
| Usuários, estados de atuação e vínculo de cada promotor com veículo e identificador Upcar | Preparar acesso regional e integração com o veículo correto |
| Quantidade de clientes, visitas, pedidos, arquivos e crescimento esperado | Dimensionar operação, armazenamento e infraestrutura |
| Domínio e titularidade das contas, responsável e orçamento de serviços | Preparar os ambientes e a operação |
| Coordenadas dos clientes e referência residencial, com responsável pela manutenção | Validar regras de distância e qualidade das posições |
| Calendário, política de despesas e forma de cobrar números ausentes | Concluir metas, performance, aprovações e rotinas pendentes |

Ismael e o responsável técnico da Upcar também deverão verificar autenticação, permissões, datas das posições, histórico de rotas, quilômetros e limites de uso da API.

## 15. Limites para composição da entrega

O escopo seguirá a versão funcional e o anexo aprovados. Dicas e IA foram retiradas do produto por solicitação de Ismael. Novos fornecedores, canais externos de lembrete, formatos adicionais de relatório e integrações requerem delimitação específica de fonte, custo, esforço e prazo. A fórmula econômica permanece proposta para validação posterior.

## 16. Acordos necessários para finalizar

1. Revisar o escopo e as hipóteses técnicas com Ismael.
2. Concluir os materiais e as definições prioritárias com a C3.
3. Negociar prazo e marcos para o conjunto pretendido.
4. Fechar critérios de aceite e responsabilidades de fornecimento dos dados.
5. Consolidar a proposta e seus anexos para a etapa contratual.

## Referências internas de preparação

- [Especificação corrente](../02-requisitos/especificacao-funcional-v0.3.md).
- [Permissões por ator](../03-fluxos-permissoes/matriz-permissoes-v0.3.md).
- [Retirada de escopo e ajustes de experiência](../02-requisitos/alteracoes-ux-escopo-v0.3.md).
- [Planejamento revisado](../06-planejamento/backlog-estimativas-v0.2.md).
- [Fontes e decisões](../00-governanca/decisoes.md).
