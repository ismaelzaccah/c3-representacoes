# Entrega da Etapa 2 — Especificação funcional

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026 • Autorização F32.

## Resultado para revisão

O [pacote ESF-C3-0.1](../02-requisitos/especificacao-funcional-v0.1.md) reúne 73 folhas funcionais rastreáveis aos 48 IDs da descoberta. Inclui onze RNFs com critérios de demonstração, treze grupos de dados, matriz de permissões e seis fluxos Mermaid editáveis. As folhas abrangem controles internos, a condição de eventual arquivo específico e a fronteira de lançamento externo. A contagem não representa 73 funcionalidades adicionais ao MVP.

A matriz anterior foi preservada no [histórico da Etapa 1](../00-governanca/historico/matriz-requisitos-etapa-1-v0.21.md). A [matriz corrente](../02-requisitos/matriz-requisitos.md) identifica agrupadores, folhas, fontes e classificação de escopo. As aprovações existentes fundamentam o pacote, enquanto todos os documentos novos permanecem PROPOSTO.

## Entregáveis

| Entregável | Referência |
|---|---|
| Entrada única e controle da especificação | [Especificação funcional](../02-requisitos/especificacao-funcional-v0.1.md) |
| Campos, tipos, vínculos e validações | [Dicionário](../02-requisitos/dicionario-dados-v0.1.md) |
| Sete módulos funcionais com critérios CA | RF-01 a RF-07, relacionados na entrada única |
| Segurança, integridade, arquivos, carga e operação | [RNFs](../02-requisitos/requisitos-nao-funcionais-v0.1.md) |
| Ações e alcance por perfil | [Permissões](../03-fluxos-permissoes/matriz-permissoes-v0.1.md) |
| Contexto e processos editáveis | [Fluxos](../03-fluxos-permissoes/fluxos-v0.1.md) |
| Correspondência com descoberta e exclusões | [Rastreabilidade](../02-requisitos/matriz-requisitos.md) |

## Decisões para aprovação do responsável

1. PT-01/02. Login por e-mail, recuperação assistida por Master e sessão de oito horas com inatividade de trinta minutos.
2. PT-03. Quantidades Wega inteiras, precisão de UNIT até seis casas, arredondamento de metade para cima e total geral pela soma dos totais de linha já arredondados. Três casas de TOTAL e MULTI mínimo continuam fundamentados nas respostas aprovadas.
3. PT-04/05. Tipos/limites de arquivos, limites de texto, datas inclusivas e procedimentos de correção de campanha/aviso.
4. PT-06. Escritório alimenta compras por lote com validação e publicação. Chave, atualização integral/incremental e ajustes só serão fechados com a amostra.
5. PT-07. Exportações administrativas pelo Escritório/Master. Concessão de exportação a Promotores aguarda decisão explícita.
6. PT-08. Master retifica registros após envio externo, com histórico e tratamento manual pelo Escritório junto ao fornecedor.
7. Campos exclusivos Master propostos para retificação de CNPJ e placa. Confirmar parâmetros de configuração, acesso ao combustível após troca de veículo. A exclusividade de veículo por promotor foi posteriormente confirmada em F35.
8. Metas de carga, navegadores, acessibilidade, precisões de combustível, timeout de posição e demais detalhes novos do dicionário/RNFs. Retenção, RPO/RTO e disponibilidade serão dimensionados com infraestrutura e custos.

## Solicitações prioritárias à C3

| Prioridade | Material ou decisão | Uso |
|---|---|---|
| 1 | Amostra anonimizada de Excel de compras faturadas, incluindo compras repetidas, cancelamentos/devoluções e procedimento de atualização | DP-01, homologar RF-07.05 e evitar dupla contagem |
| 2 | Exemplo preenchido de cotação Wega e PDF esperado com casos de arredondamento/mínimo | DP-05, homologar mapeamento e precisão |
| 3 | Relação de fornecedores pretendidos no conjunto contratado e amostra/processo de cada um | DP-02/06, delimitar tratamentos e eventual saída específica |
| 4 | Relação promotor–veículo–identificador Upcar e disponibilidade de João Vitor para homologar a API com Ismael | DP-03, validar identidade, autorização e horários. Credenciais já estão com Ismael e devem ser fornecidas apenas pelo mecanismo protegido da implantação |
| 5 | Volumes aproximados, aparelhos usados, responsáveis pelos dados e acesso administrativo ao domínio existente | DP-04, dimensionar carga, hospedagem, retenção e custo |

## Verificações e limites da entrega

Foram conferidos IDs de origem, critérios por folha, referências locais e preservação dos originais. Os arquivos de cliente permanecem ignorados pelo Git. A verificação documental não demonstra comportamento de software. Os diagramas precisam de conferência visual no visualizador Mermaid escolhido. Compras e fornecedores futuros têm critérios específicos ainda dependentes de materiais.

## Encaminhamento

A Etapa 2 entrega a especificação para revisão. A próxima etapa tratará arquitetura e dimensionamento, conforme o plano mestre, após autorização pertinente. O prazo de trinta dias até entrega para homologação permanece pendente de validação técnica considerando 80 h/mês de capacidade de Ismael. A implantação conserva R$ 24.000 e o serviço mensal posterior R$ 8.000 por 80 horas. Evolução mensal segue o ciclo posterior aprovado, sem ser presumida incluída no preço da implantação.

## Inventário de arquivos da etapa

Arquivos criados, todos PROPOSTO.

- `docs/02-requisitos/especificacao-funcional-v0.1.md`
- `docs/02-requisitos/dicionario-dados-v0.1.md`
- `docs/02-requisitos/rf-01-acesso-v0.1.md`
- `docs/02-requisitos/rf-02-cadastros-v0.1.md`
- `docs/02-requisitos/rf-03-visitas-v0.1.md`
- `docs/02-requisitos/rf-04-campanhas-v0.1.md`
- `docs/02-requisitos/rf-05-pedidos-v0.1.md`
- `docs/02-requisitos/rf-06-abastecimentos-v0.1.md`
- `docs/02-requisitos/rf-07-consultas-v0.1.md`
- `docs/02-requisitos/requisitos-nao-funcionais-v0.1.md`
- `docs/03-fluxos-permissoes/matriz-permissoes-v0.1.md`
- `docs/03-fluxos-permissoes/fluxos-v0.1.md`
- `docs/06-planejamento/situacao-etapa-2.md`
- `docs/00-governanca/historico/matriz-requisitos-etapa-1-v0.21.md`

Arquivos atualizados.

- `docs/README.md`
- `docs/00-governanca/fontes.md`
- `docs/00-governanca/decisoes.md`
- `docs/00-governanca/pendencias.md`
- `docs/02-requisitos/matriz-requisitos.md`
- `docs/03-fluxos-permissoes/README.md`
- `docs/06-planejamento/prontidao-etapa-2.md`

