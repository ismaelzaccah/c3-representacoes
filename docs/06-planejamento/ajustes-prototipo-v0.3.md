# Ajustes do protótipo e do escopo C3

Status PROPOSTO • UX-C3-0.3 / ESF-C3-0.3 • 10/11/2026 • Fonte F47.

## Entrega corrente

- [Protótipo 0.3](../05-prototipos/prototipo-navegavel-v0.3.html) com login demonstrativo, formulários e notificações em cards sobrepostos, entrada ascendente, saída descendente, X e confirmações de descarte/envio.
- Navegação com página selecionada identificada e expansão de Mais junto ao menu móvel.
- [Adendo de escopo e experiência](../02-requisitos/alteracoes-ux-escopo-v0.3.md), [especificação corrente](../02-requisitos/especificacao-funcional-v0.3.md), [permissões](../03-fluxos-permissoes/matriz-permissoes-v0.3.md) e [roteiro](../05-prototipos/roteiro-prototipos-v0.3.md).
- Dicas e IA retiradas de telas, navegação, ações, dados próprios e permissões da versão corrente. RF-12.01–03 retirados e DP-10 cancelada no planejamento do sistema.

## Verificações executadas

Testes locais no Microsoft Edge, com larguras de 320, 390, 768 e 1280 pixels. Exploração de Admin, Escritório e Promotores, indicador ativo, ausência de transbordamento horizontal, posicionamento de Mais, login vazio e saída. Verificados abertura/fechamento de card, animação de saída após sucesso, confirmação de envio/descarte, cancelamento preservando dados e falha de validação mantendo o formulário aberto. Telas de login, menu móvel e solicitação de campanha foram inspecionadas visualmente. A execução registrou zero erros JavaScript e zero requisições externas.

## Detalhamento e limites

O card pede descarte após edição. O fundo mantém o card aberto. Escape usa a mesma proteção do X. Preferência de movimento reduzido é respeitada. O protótipo ocupa a altura disponível no navegador, com rolagem no conteúdo. O card sobe da parte inferior até o centro da janela e desce ao fechar.

Após o relato de faixa branca e a solicitação de centralização, foram verificados os tamanhos 1660 × 960, 1280 × 720, 390 × 844, 320 × 568 e 667 × 375 no Edge. O conteúdo alcança a base da janela, o último componente permanece acessível por rolagem e o modal fica centralizado com margem de segurança. Capturas de desktop e celular foram inspecionadas visualmente.

O sucesso corresponde à ação simulada local. Persistência, autenticação real e integrações ainda dependem da implementação. O comportamento foi testado no Edge. Outros navegadores e dispositivos físicos ainda requerem validação.

As versões 0.1/0.2 e os materiais originais permanecem preservados para rastreabilidade. A documentação histórica deve ser interpretada pelas alterações correntes. A remoção do módulo exige reestimativa do escopo remanescente, mantendo a renegociação de prazo e os valores comerciais aprovados.
