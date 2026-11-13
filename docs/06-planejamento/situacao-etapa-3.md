# Etapa 3 — Arquitetura e dimensionamento preliminares

Status PROPOSTO • ARQ-C3-0.1 • 10/11/2026 • Continuidade autorizada em F36.

## Resultado

Foi preparado o pacote de arquitetura e planejamento que pode avançar com as informações atuais. O [documento de arquitetura](../04-arquitetura/arquitetura-preliminar-v0.1.md) é a entrada do pacote. Usa ESF-C3-0.1 revisão 1, com exclusividade do veículo aprovada em F35. A autorização de continuar o planejamento não aprova automaticamente os detalhes técnicos propostos na Etapa 2 ou nesta etapa.

| Entrega | Resultado para revisão |
|---|---|
| Arquitetura | Monólito modular, responsabilidades, segurança, arquivos privados, integração pontual e operação |
| Tecnologias | Avaliação documental de versões/famílias, integração, licenças e provas para congelamento |
| Dados | Modelo lógico, cardinalidades, versões, vínculo exclusivo, transações e índices candidatos |
| Decisões | Nove ADRs propostos, com contexto, consequências e prova necessária |
| Planejamento | Doze pacotes de trabalho, dependências, três cenários de esforço e marcos |
| Riscos | Doze riscos e sete provas técnicas, com responsáveis e evidências esperadas |
| Testes | Camadas, dezenove cenários críticos e rito de homologação ligados à especificação |

## Parecer preliminar de capacidade

O esforço remanescente atualmente dimensionável foi estimado por decomposição em 134–388 h, com cenário mais provável de 240 h. A reserva proposta de 20% leva esse cenário a 288 h. Frente à capacidade informada de 80 h/mês, o cenário com reserva equivale a 3,6 ciclos de capacidade. Mesmo o cenário otimista sem reserva excede a referência nominal mensal.

O resultado sinaliza incompatibilidade preliminar entre escopo integral, capacidade e prazo previsto de trinta dias. São estimativas de engenharia para revisão de Ismael, sem produtividade medida ou execução de prova técnica. Fontes adicionais e espera por terceiros podem alterar esforço e calendário. A conclusão técnica definitiva depende de revisar estimativas e executar as provas prioritárias.

Este cálculo não altera preço, escopo, capacidade aprovada ou prazo contratual. R$ 24.000 de implantação e R$ 8.000 mensais posteriores por 80 horas continuam registrados nas decisões comerciais. Eventual ajuste exige aprovação bilateral. Os ciclos de capacidade não são cobrança automática de mensalidades. A evolução mensal tem o marco posterior aprovado.

## Revisões que Ismael pode fazer agora

1. Revisar as faixas por pacote e informar experiência, componentes próprios reutilizáveis e disponibilidade efetiva que possam mudar a estimativa. Qualquer reutilização deve demonstrar aderência e licença.
2. Revisar direção técnica de monólito, PostgreSQL, arquivos privados e candidato de autenticação. Aprovação final da stack exige conjunto exato e prova integrada.
3. Revisar os detalhes PT-01–08, limites, campos Master, permissões e critérios da ESF. A exclusividade do veículo já foi resolvida em F35.
4. Escolher a ordem de validação e preparar os dados de teste e critérios antes da futura execução técnica.

## Itens que aguardam evidência

| Dependência | Informação | Consequência |
|---|---|---|
| DP-01 | Excel de compras faturadas e procedimento de atualização | Finalizar modelo/adaptador, chave, ajustes e conciliação |
| DP-02/06 | Fornecedores do conjunto contratado e materiais | Estimar cada fonte e eventual arquivo específico |
| DP-03 | Relação promotor/veículo/Upcar, conta/permissões e apoio de João Vitor | Homologar identidade, autenticação, fuso e posição pontual |
| DP-04 | Volumes, domínio, dispositivos e aprovação de orçamento | Fechar ambiente, custos, retenção, carga e recuperação |
| DP-05 | Cotação preenchida e PDF esperado | Homologar mapeamento, precisão e apresentação |

F35 resolve que cada veículo é exclusivo do promotor. A lista ainda é necessária para identificar quem utiliza cada veículo e qual registro Upcar consultar. Ismael fará a solicitação à Gabriella pelo canal escolhido e repassará o retorno.

## Inventário de arquivos criados

- `docs/04-arquitetura/arquitetura-preliminar-v0.1.md`
- `docs/04-arquitetura/avaliacao-stack-v0.1.md`
- `docs/04-arquitetura/modelo-dados-v0.1.md`
- `docs/04-arquitetura/decisoes-arquiteturais-v0.1.md`
- `docs/06-planejamento/backlog-estimativas-v0.1.md`
- `docs/06-planejamento/riscos-validacoes-v0.1.md`
- `docs/06-planejamento/estrategia-testes-v0.1.md`
- `docs/06-planejamento/situacao-etapa-3.md`

Índices, governança e referências correntes foram atualizados. ESF, dicionário e RF-02.04.02 receberam a confirmação de exclusividade, com critério de recusa de vínculo simultâneo. As fontes da matriz foram conferidas para manter separados os identificadores F e DEC-F. A matriz histórica mantém seu conteúdo de descoberta.

## Verificação da entrega

Revisão estrutural dos documentos, referências locais, cobertura dos 48 IDs originais e critérios das 73 folhas. Conferência aritmética das estimativas e preservação por hash dos originais. Os diagramas Mermaid são editáveis, com renderização visual ainda pendente no visualizador adotado. Compatibilidade, carga, segurança e comportamento de software aguardam as provas executáveis. A infraestrutura continua dependente de dimensionamento/cotação aprovados.

## Próximo encaminhamento

Revisar arquitetura e dimensionamento com Ismael, incorporar os materiais conforme chegarem e fechar as decisões da especificação. A execução técnica e a contratação de serviços terão autorização própria. O pacote preliminar já permite decidir a viabilização do prazo com base nas faixas, dependências e critérios explicitados.

