# Restauração documental e ajustes do protótipo

Status PROPOSTO • UX-C3-0.5 • 12/11/2026 • F54.

## Resultado

O primeiro filtro da versão 1.0 foi desfeito nos índices, requisitos, visão, permissões, planejamento, arquitetura, testes e proposta afetados. Os documentos gerados para aquele recorte e o HTML v0.4 foram descartados. A referência funcional retorna à ESF-C3-0.3. Fontes e decisões registram a reversão.

O [protótipo 0.5](../05-prototipos/prototipo-navegavel-v0.5.html) foi reconstruído diretamente da v0.3. A base v0.3 e os originais do cliente permanecem preservados. Os [ajustes de cadastro e interface](../02-requisitos/ajustes-cadastro-interface-v0.5.md) descrevem as alterações por perfil e campos.

## Conteúdo alterado

- Painel administrativo com retirada dos quatro cards indicados e Avisos no topo, após Despesas a Pagar.
- Hoje do Promotor com Minhas tarefas após Bom dia e retirada do card Trajetos do veículo.
- Página Metas removida para todos os perfis.
- Botão de notificações superior removido. Consulta pelo card Avisos preservada.
- CPF em Escritório/Promotores e placa do veículo para Promotor, no editor reservado ao Admin.

## Verificação

A conferência local no Edge percorreu Admin, Escritório e Promotor em 320, 390, 768 e 1280 pixels. Foram verificadas a retirada dos cards, a ordem de Avisos/Minhas tarefas, a remoção dos acessos Metas e do sino, a exibição de CPF/Veículo por perfil, a persistência ao salvar/reabrir e a troca de perfil no editor. A tentativa de usar a mesma placa em dois promotores ativos mostrou erro e preservou o card. Foram registrados zero erros JavaScript, zero requisições externas e ausência de transbordamento horizontal nos percursos. Capturas de painel desktop e Hoje móvel foram inspecionadas visualmente.

A validação representa o comportamento local da demonstração. Persistência no servidor e validação de dados reais serão tratadas na implementação.

## Detalhamento adotado

Avisos fica após o conjunto de indicadores do topo, cujo último elemento é o card de despesas citado. O rótulo desse indicador foi ajustado de Despesas a aprovar para Despesas a Pagar. A base do indicador é a mesma da v0.3. Os CPFs começam vazios na demonstração. F55 solicita placas fictícias para os seis promotores e CPF/CNPJ como identificador na tela de login. As placas de exemplo estão preenchidas no cadastro e identificadas como fictícias na apresentação do veículo.
