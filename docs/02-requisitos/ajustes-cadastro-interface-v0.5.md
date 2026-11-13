# Ajustes de cadastro e interface a partir da v0.3

Status PROPOSTO • Versão 0.5 • 12/11/2026 • Diretrizes aprovadas em F54.

## Referência funcional restaurada

O primeiro filtro da versão 1.0 e seus desdobramentos foram desfeitos por solicitação de Ismael. A [ESF-C3-0.3](especificacao-funcional-v0.3.md) retorna à condição de referência funcional, com os ajustes específicos abaixo. A versão de interface [UX-C3-0.5](../05-prototipos/prototipo-navegavel-v0.5.html) deriva diretamente do HTML v0.3.

## Alterações por perfil

| Perfil / tela | Alteração solicitada |
|---|---|
| Admin e Escritório / Painel | Remover Visitas da equipe em outubro, Junte e Troque WEGA, Hella - Iluminação e Trajetos de hoje |
| Admin e Escritório / Painel | Posicionar Avisos no topo, imediatamente após o conjunto de indicadores cujo último card é Despesas a Pagar |
| Promotor / Hoje | Remover Trajetos do veículo e mover Minhas tarefas para imediatamente após Bom dia |
| Todos / Navegação | Remover página Metas e seus acessos |
| Todos / Cabeçalho | Remover botão de notificações do canto superior direito |
| Admin / Configurações | Adicionar CPF para pessoas com perfil Escritório e Promotor. Admin fica sem esse campo no editor |
| Admin / Configurações | Para Promotor, adicionar Veículo com informação da placa do veículo da empresa |

O card de despesas existente na v0.3 usa o rótulo Despesas a aprovar. A versão 0.5 apresenta o rótulo Despesas a Pagar para corresponder ao ponto de referência mencionado por Ismael. Seu indicador usa a mesma base de despesas da v0.3.

## Campos de pessoa

CPF é apresentado no editor conforme o perfil selecionado e salvo no cadastro local da demonstração. O campo fica disponível para nova conta e para edição. Um CPF já registrado é preservado ao alternar o perfil, respeitando sua exibição conforme a regra solicitada.

Veículo identifica o vínculo pela placa, apresentada em letras maiúsculas ao salvar. O vínculo atualizado é refletido nas consultas que usam o veículo do promotor. A regra anterior de veículo exclusivo impede atribuir a mesma placa a dois promotores ativos. As placas e CPFs reais serão fornecidos pela C3.

A manutenção continua reservada ao Admin, conforme RF-01.05/RF-02.02. O detalhamento de validação de documentos e os controles efetivos de dados pessoais serão aplicados na implementação.

## Complementos de F55

Os seis promotores recebem placas fictícias distintas na demonstração, disponíveis no campo Veículo e nas consultas que apresentam o vínculo. O login usa CPF/CNPJ como identificador textual, com teclado numérico sugerido em dispositivos móveis. A entrada com campos vazios continua disponível para demonstração. Os dados reais serão associados na implementação, conforme o cadastro e a autorização aplicáveis.

## Critérios de conferência

- Nos painéis Admin/Escritório, os quatro cards indicados deixam de aparecer e Avisos precede Equipe hoje, logo após os indicadores de topo.
- Em Hoje do Promotor, Minhas tarefas é o segundo card, após Bom dia. O card de trajetos foi removido.
- Metas sai dos menus desktop/móvel e do roteamento do protótipo.
- O cabeçalho fica sem sino. O card Avisos conserva acesso ao seu conteúdo pelo botão Ver todos.
- Admin no editor fica sem CPF. Escritório mostra CPF. Promotor mostra CPF e Veículo.
- Salvar/reabrir pessoa preserva CPF e placa informados. Alteração de perfil atualiza os campos exibidos.
- Cards continuam centralizados, com animação e confirmação de envio/descarte. O relógio acompanha o dispositivo.
