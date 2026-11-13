# Dicionário funcional de dados

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Os campos abaixo detalham o modelo funcional. Tipos lógicos e limites novos são propostas de especificação. A arquitetura determinará representações físicas. IDs são opacos, estáveis e únicos. Toda entidade persistida recebe ID, instante de criação, autor, instante da última mudança e revisão para concorrência. Relações usam IDs, com preservação de referências históricas.

## D-01 — Conta de funcionário

| Campo | Tipo e obrigatoriedade | Validação e uso |
|---|---|---|
| nome | Texto, obrigatório, 2–120 caracteres | Aparar espaços externos, preservar nome de exibição |
| email | Texto, obrigatório, até 254 | Formato de e-mail e unicidade sem distinção de caixa. Proposta PT-01 para login |
| perfil | Enum obrigatório | ESCRITORIO, PROMOTOR, MASTER. Master é reservado. Alteração pelo próprio Master segue proteção de última conta ativa |
| situacao | Enum obrigatório | ATIVA ou INATIVA. Inativação bloqueia acesso e preserva autoria |
| segredo de autenticação | Gerido pela solução de autenticação | Cadastro/recuperação seguem procedimento protegido. Logs e consultas operacionais omitem o segredo |
| veiculo_fixo_id | Referência | Obrigatório para habilitar novas visitas/abastecimentos de um Promotor. Vinculado por Master. Proposta de ativação funcional |

A criação inicial de Master será procedimento técnico controlado, a registrar na entrega. A última conta Master ativa exige manutenção de outro responsável habilitado antes da inativação. Essa proteção é PROPOSTA para evitar perda de administração.

## D-02 — Cliente/estabelecimento

| Campo | Tipo e obrigatoriedade | Validação e uso |
|---|---|---|
| nome_razao_social | Texto, obrigatório, 2–200 | Nome mostrado em busca e documentos |
| cnpj | Identificador textual obrigatório | Quatorze posições, normalizado em maiúsculas e sem separadores. Aceitar numérico existente e alfanumérico, com validação de dígitos verificadores. Unicidade global entre ativos/inativos |
| endereco | Texto, obrigatório, até 300 | Logradouro e número/complemento quando fornecidos |
| cidade | Texto, obrigatório, até 120 | Preservar acentuação |
| uf | Texto obrigatório, duas letras | Seleção de UF brasileira. Lista controlada de interface |
| bairro | Texto opcional, até 120 | Complementar |
| cep | Texto opcional | Oito dígitos quando informado, com máscara de exibição |
| telefone | Texto opcional, até 30 | Preservar código internacional e formato legível |
| contato | Texto opcional, até 120 | Pessoa de contato informada pela C3 |
| email | Texto opcional, até 254 | Validar formato quando informado |
| situacao | Enum obrigatório | ATIVO ou INATIVO. Inativo continua no histórico |

Todos os promotores consultam e selecionam clientes ativos. A autoria das visitas é vínculo próprio do registro. Um cliente pode ter vários fornecedores. CNPJ compartilhado por dois cadastros deve ser tratado como duplicidade, conforme F25. Uma filial com inscrição própria constitui outro estabelecimento.

O formato de CNPJ contempla os identificadores alfanuméricos previstos pela Receita e os numéricos existentes. A validação local não comprova situação cadastral fiscal. [Receita Federal](https://www.gov.br/receitafederal/pt-br/acesso-a-informacao/acoes-e-programas/programas-e-atividades/cnpj-alfanumerico).

## D-03 — Fornecedor e associação

| Campo | Tipo e obrigatoriedade | Validação e uso |
|---|---|---|
| nome | Texto obrigatório, 2–150 | Nome operacional único normalizado, proposta de prevenção de duplicidade |
| identificador_externo | Texto opcional, até 100 | Código do fornecedor no material externo, quando aplicável |
| situacao | ATIVO/INATIVO obrigatório | Inativação preserva pedidos/campanhas |
| cliente_id, fornecedor_id | Par de referências obrigatório | Associação única por par, mantida pelo Escritório |

Wega, Hella, Starke, Paraflu e NTN são nomes de contexto, sujeitos ao cadastro real. Layouts homologados são identificados separadamente por fornecedor e versão.

## D-04 — Veículo e vínculo fixo

| Campo | Tipo e obrigatoriedade | Validação e uso |
|---|---|---|
| placa | Identificador textual obrigatório | Normalizar caixa/separadores. Até sete caracteres alfanuméricos, conforme formato da placa brasileira a homologar. Unicidade entre veículos |
| identificacao | Texto obrigatório, até 150 | Descrição reconhecível pela equipe |
| referencia_api | Texto | Identificador estável do veículo no provedor, obrigatório para obter posição. Placa pode auxiliar conferência da associação |
| situacao | ATIVO/INATIVO obrigatório | Impedir novas operações com veículo inativo |
| promotor_id, veiculo_id | Referências obrigatórias no vínculo | Um veículo fixo vigente por promotor e um único promotor vigente por veículo. Exclusividade APROVADA em F35, complementando F23 |
| inicio_vigencia, fim_vigencia | Instantes, fim opcional | Mudança pelo Master preserva associação anterior e seus eventos |

A troca excepcional do vínculo afeta eventos futuros. Visitas e abastecimentos preservam o veículo usado no registro original. A mudança com visita aberta exige regularização ou definição explícita do Master para manter o vínculo da visita, proposta PT de integridade.

## D-05 — Visita

| Campo | Tipo e obrigatoriedade | Validação e uso |
|---|---|---|
| cliente_id, promotor_id, veiculo_id | Referências obrigatórias | Cliente e veículo ativos no início. Promotor vem da sessão e veículo do vínculo fixo |
| checkin_em | Instante obrigatório | Atribuído pelo sistema ao salvar. Preservar instante original |
| checkout_em | Instante opcional até encerramento | Deve ser igual ou posterior ao início |
| situacao | ABERTA/ENCERRADA | Uma ABERTA por promotor, garantida inclusive sob concorrência |
| motivo | Texto obrigatório proposto, até 120 | Lista inicial a validar usando F03 A21:A33, com opção Outro e descrição. Lista definitiva PENDENTE |
| observacoes | Texto opcional, até 2.000 | Editável pelo promotor enquanto aberta |
| justificativa_regularizacao | Texto obrigatório na correção, 10–1.000 | Master registra motivo e novos valores. Fato original preservado |

Visita esquecida mantém situação ABERTA até encerramento ou regularização. O sistema apresenta o registro aberto para resolução. A aprovação de regras não criou encerramento automático por horário.

## D-06 — Posição do veículo no evento

| Campo | Tipo e obrigatoriedade | Validação e uso |
|---|---|---|
| evento | CHECKIN/CHECKOUT obrigatório | Snapshot vinculado à visita e ao evento |
| origem, veiculo_id, referencia_api | Obrigatórios quando há consulta | Origem UP­CAR. Guardar identificador do veículo consultado |
| evento_em, consultado_em | Instantes obrigatórios | Separar instante da visita e da consulta |
| posicao_em | Instante quando fornecido | Interpretar fuso do provedor na homologação DP-03 |
| latitude, longitude | Decimais quando fornecidos | Faixas −90 a 90 e −180 a 180. Coordenada zero pode ser válida |
| valida | Booleano/ausente | Usar indicação do provedor. Ausência precisa de tratamento homologado |
| condicao | ATUAL, ANTIGA, INVALIDA, AUSENTE, ERRO_API, SEM_VINCULO | Categoria de conferência e rastreabilidade |
| justificativa | Texto 10–1.000, obrigatório na exceção | Promotor informa para concluir evento sem posição utilizável |

Posição atual tem idade entre zero e 300 segundos no evento, coordenadas válidas e sinal de validade aceitável. Idade exatamente 300 é aceita. Posição acima de 300 usa exceção. Horário ausente/futuro, validade ausente e divergência de veículo têm tratamento conservador PROPOSTO de conferência até a homologação da API. Timeout externo proposto de dez segundos por evento, sujeito a DP-03. A visita confirmada não muda automaticamente ao chegar uma posição posterior.

## D-07 — Campanha, folder e aviso

| Campo | Tipo e obrigatoriedade | Validação e uso |
|---|---|---|
| titulo | Texto obrigatório, 3–150 | Identificação da solicitação |
| solicitante_id, responsavel_id | Referências obrigatórias | Solicitante pela sessão, responsável operacional a definir/confirmar pelo Escritório |
| fornecedor_id | Referência obrigatória | Um fornecedor por campanha |
| clientes_alvo | Lista de referências, mínimo um | Associação única por cliente. Vários clientes permitidos |
| descricao_solicitacao | Texto obrigatório proposto, até 2.000 | Conteúdo necessário ao encaminhamento externo |
| decisao | SOLICITADA, APROVADA, REJEITADA, CANCELADA | Histórico de decisões e autoria. Vigência é dimensão distinta |
| inicio_vigencia, fim_vigencia | Datas obrigatórias para ativar | Início menor ou igual ao fim. Datas inclusivas propostas PT-05 |
| folders | Uma ou mais referências para ativar | Arquivos autorizados. PT-04 para tipos/tamanhos |
| motivo_rejeicao_cancelamento | Texto obrigatório proposto, 10–1.000 | Rejeição/cancelamento registram encaminhamento e responsável |
| aviso.cliente_id, texto, inicio, fim | Obrigatórios | Texto 1–2.000, período coerente. Escritório cria e promotor consulta ao selecionar cliente |

Ativa é condição calculada de campanha APROVADA, com folder pronto, dentro da vigência e vínculo ao cliente selecionado. Expiração preserva decisão e histórico. Campanha cancelada perde exibição ativa. Períodos sobrepostos e múltiplos avisos por cliente são permitidos como proposta de detalhe.

## D-08 — Solicitação e versão de proposta

| Campo | Tipo e obrigatoriedade | Validação e uso |
|---|---|---|
| cliente_id, fornecedor_id | Referências obrigatórias | Uma solicitação por cliente e fornecedor. Pedido que envolva vários fornecedores deve ser separado por fornecedor, proposta de detalhe |
| canal_origem | WHATSAPP/EMAIL obrigatório | Registro manual do processo externo |
| recebido_em | Instante obrigatório | Data informada do recebimento. Criado_em registra a entrada no sistema |
| descricao | Texto obrigatório, até 4.000 | Conteúdo da solicitação |
| responsavel_id | Referência obrigatória | Operador do Escritório |
| anexos_originais | Lista opcional na entrada | Fonte preservada e associada à solicitação |
| versao_numero | Inteiro crescente por solicitação | Único e sequencial a partir de 1 |
| estado_versao | RASCUNHO, APRESENTADA, ALTERACAO_SOLICITADA, APROVADA_CLIENTE, REJEITADA_CLIENTE, SUBSTITUIDA | Revisão interna e envio são dimensões próprias, definidas nos fluxos |
| itens, pdf_id, lote_origem_id | Relações | Itens de versão, PDF imutável da versão apresentada e proveniência |

Documento apresentado ao cliente preserva snapshot de identidade, código/descrição, quantidade, mínimo, preço e cálculo. Alterações geram outra versão. A fonte de fornecedor não atualiza automaticamente versões apresentadas.

## D-09 — Linha da proposta Wega

| Campo | Tipo e obrigatoriedade | Regra |
|---|---|---|
| codigo_produto | Texto obrigatório, até 100 | F09 coluna A. Preservar letras, barras e hífens |
| descricao | Texto obrigatório, até 300 | F09 coluna C, Grupo, conforme F16 |
| quantidade | Número exato obrigatório | Inteiro positivo proposto PT-03 para Wega, maior ou igual ao mínimo |
| minimo | Número exato obrigatório | F09 coluna E. F11 define mínimo, permitindo 7 quando mínimo é 6 |
| unitario | Decimal exato obrigatório | F09 coluna G, preço direto. Preservar até seis casas como proposta de limite. Rejeitar perda de precisão silenciosa |
| total_item | Decimal calculado, três casas | Quantidade × unitário, arredondamento de metade para cima proposto PT-03 |
| ordem | Inteiro obrigatório | Ordem do PDF e do resumo para lançamento |

Proposta de total geral é a soma dos totais de linha já arredondados. Esta definição e a exibição de UNIT com precisão da origem aguardam revisão. Exemplo técnico `QTD=1`, `UNIT=1,2345` resulta `TOTAL=1,235` sob PT-03. A decisão aprovada é três casas decimais, enquanto o tratamento do empate é proposta desta versão.

## D-10 — Resposta, revisão, autorização e envio externo

| Campo | Tipo e obrigatoriedade | Regra |
|---|---|---|
| resposta.versao_id, decisao, data, autor_registro | Obrigatórios | Decisão APROVACAO, ALTERACAO ou REJEICAO. Anexo de evidência obrigatório conforme F17 |
| resposta.motivo_encaminhamento | Texto | Obrigatório para rejeição e alteração, proposto para rastreabilidade |
| revisao.versao_id, resultado, autor, instante | Obrigatórios | Resultado LIBERAR ou AJUSTAR, proposto para o fluxo. Escritório realiza |
| autorizacao.versao_id, autor, instante | Obrigatórios | Exige versão aprovada pelo cliente e revisão interna liberada. A mesma pessoa pode revisar/autorizar |
| envio.versao_id, enviado_em, operador, referencia | Obrigatórios, referência opcional | Registro manual da operação no fornecedor, com versão autorizada |
| resultado.situacao, registrado_em, operador | Obrigatórios | ACEITO, REJEITADO ou PENDENTE como proposta de vocabulário. Protocolo/observações quando houver |

Aceitação pelo fornecedor é fato diferente de compra faturada. Uma evidência de resultado preserva o texto/protocolo disponível. Faturamento efetivo será apurado a partir da fonte de compras homologada.

## D-11 — Arquivo e lote de entrada

Arquivo recebe identificador, proprietário funcional, nome original, nome interno opaco, tipo detectado, tamanho, hash, situação de validação e autor. O acesso segue a entidade vinculada. Credenciais de provedor usam configuração técnica protegida.

| Campo do lote | Regra proposta |
|---|---|
| fornecedor_id, layout_versao, finalidade | Obrigatórios. Finalidade TABELA_FORNECEDOR ou COMPRAS_FATURADAS |
| arquivo_id, hash, recebido_em, autor | Proveniência obrigatória |
| estado | RECEBIDO, VALIDADO, REJEITADO, PUBLICADO |
| erros | Linha/campo/regra e mensagem, sem despejar dados sensíveis em logs |
| chave_lote | Impede reaplicar acidentalmente o mesmo conteúdo na mesma finalidade |

Importação proposta usa validação completa antes de publicar. Arquivo inválido mantém o lote anterior utilizável. Layout desconhecido requer homologação. Fórmulas e macros não são executadas como parte da leitura de dados. Política de fórmulas com valores armazenados deverá ser definida por layout.

## D-12 — Compra faturada e abastecimento

| Entidade/campo | Obrigatoriedade e regra |
|---|---|
| compra.cliente_id, fornecedor_id, data_compra, valor | Necessários à métrica aprovada. Campo de identificação/ajuste e granularidade dependem de DP-01 |
| compra.chave_origem, lote_id | Propostos para deduplicar e reconstruir origem. Chave definitiva depende da amostra |
| compra.tipo_ajuste | PENDENTE, definir cancelamentos/devoluções e sinal de valores com a C3 |
| abastecimento.veiculo_id, data, hodometro, litros, total | Obrigatórios. Hodômetro não negativo. Litros e total positivos |
| abastecimento.autor, criado_em | Gerados pelo sistema |
| abastecimento.justificativa_retroativo | Obrigatória para data passada lançada pelo Escritório, 10–1.000 caracteres |
| abastecimento.justificativa_correcao | Master informa, com valores anteriores e revisados |

Precisão proposta para abastecimento é hodômetro em km com até três casas, litros com até três e valor pago com duas casas. A precisão de três casas aprovada para cotação continua vinculada à cotação. A data de abastecimento determina sequência de hodômetro. Mesma data exige hora operacional ou ordem explícita a homologar. Lançamento retroativo deve respeitar vizinhos anteriores e posteriores. Troca de painel/hodômetro é exceção a definir com Master, preservando evidências.

## D-13 — Auditoria

Evento registra ID do objeto, ação, ator, instante, versão anterior/posterior, justificativa quando exigida e correlação de requisição. A leitura administrativa é do Master, com histórico operacional permitido ao Escritório na entidade. Valores de senhas/tokens são omitidos. Retenção e descarte têm política PENDENTE em DP-04. A inativação de contas e entidades conserva os vínculos dos fatos históricos.

