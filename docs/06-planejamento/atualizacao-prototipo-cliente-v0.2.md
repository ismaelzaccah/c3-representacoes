# Atualização após análise do protótipo C3

Status PROPOSTO • UX-C3-0.2 / ESF-C3-0.2 • 10/11/2026.

Registro histórico da revisão 0.2. A [ESF-C3-0.3](../02-requisitos/especificacao-funcional-v0.3.md) tem precedência. F47 retira integralmente Dicas e IA do produto e atualiza a experiência do protótipo.

## Resultado

O [protótipo atualizado](../05-prototipos/prototipo-navegavel-v0.2.html) aproxima a navegação e a organização funcional do material enviado pela C3, preservando o fluxo de pedidos construído na descoberta. O [relatório de análise](../05-prototipos/analise-prototipo-cliente-v0.1.md) registra trinta combinações de perfil/tela e doze detalhes adicionais examinados na referência, além das regras lidas no código da aplicação.

Foram extraídas as duas variantes da logo C3 e incorporadas ao estudo. Dez nomes e os estados/vínculos de referência vieram do seletor Ver como. Telefones de pessoas foram omitidos da versão derivada. O original, seus recursos e as planilhas permanecem preservados em `fontes-cliente`.

## Decisões esclarecidas durante a análise

| Tema | Decisão de Ismael |
|---|---|
| Atores | Admin, Escritório e Promotores. Admin assume funções antes denominadas Master |
| Acesso regional | Promotor acessa clientes dos seus estados |
| Histórico | Ficha regional compartilha visitas da equipe. Histórico pessoal continua próprio |
| Cadastro | Promotor cadastra/atualiza contato, endereço e linhas de clientes da região |
| Escopo | Metas, performance, tarefas, despesas adicionais, trajetos/Waze e IA entram no escopo pretendido, com prazo a renegociar |
| Fonte de localização/KM | Rastreador do veículo via Upcar, inclusive trajetos |
| Visitas | Mínimo 8/ideal 12 ao dia, primeira 8h–8h20, última após 17h30, residência a pelo menos 500 m e cliente a até 70 m |
| Atraso da primeira | Permitido com justificativa e aviso ao Admin |
| Repetição | Terceira visita semanal exige motivo de todos, inclusive Daysilane e contas-chave |
| Números | Promotor pode enviar vendido/estoque/projeção e é responsável por cobrar os dados em cada visita |
| Economia | Fórmula dos três melhores meses com piso de 85% permanece como proposta para validação posterior |

As decisões F41–F46 foram registradas na governança e na [especificação corrente](../02-requisitos/especificacao-funcional-v0.2.md). O [adendo](../02-requisitos/alteracoes-escopo-v0.2.md) registra alterações nos requisitos anteriores, 21 unidades adicionais de detalhamento e novas dependências. A [matriz de permissões](../03-fluxos-permissoes/matriz-permissoes-v0.2.md) explicita ações e alcance por ator.

## Ajustes de interface

Hoje prioriza visita atual e próxima ação. Navegação móvel fica junto ao cabeçalho, com Mais para as opções complementares. O computador tem menu lateral. A ficha reúne contexto cadastral, linhas, histórico e números. O relatório da visita ocorre em etapas e mantém o registro aberto antes do encerramento.

Foram preservados os velocímetros de metas/campanhas, barras por linha/promotor e colunas mensais da performance. Gráficos têm rótulos e valores de exemplo. A adaptação ajusta a área mensal e os controles para celular. A consulta de números e sua prévia de relatório obedecem à mesma região. Combustível mantém hodômetro, litros, valor e veículo. Pedido mantém decisão, revisão e autorização vinculadas à versão.

## Verificação do estudo

Foram percorridos os menus dos três atores em 320, 390, 768 e 1280 px. As verificações incluem dez pessoas no seletor, restrição regional em clientes/números, primeira visita fora de horário com justificativa, check-in/out, nova versão de pedido invalidando autorização anterior, distâncias 499/500 m e 70/71 m, posição no limite de cinco minutos, relatório regional, hodômetro obrigatório e resposta de IA identificada como simulação.

Os percursos de verificação em Microsoft Edge headless registraram zero erro de JavaScript e zero requisição HTTP da demonstração. Foram inspecionadas imagens móveis de Hoje e performance, além do painel administrativo. Os testes verificam estados e navegação do estudo local, sem comprovar autorização de servidor, banco, sensores ou integração real. Aparelhos reais, Safari e avaliação completa de acessibilidade ainda requerem validação.

## Limites e próximos detalhes

A versão usa dados de demonstração e referência operacional de 20/10/2026, mantida do material recebido. Contas reais, veículos, arquivos e fontes precisam de confirmação. Posições, distâncias e horários são cenários locais. Documentos e IA têm prévias simuladas. Upcar, georreferência de cliente/residência, WhatsApp, processamento de arquivos e IA aguardam homologação técnica e custos.

A fórmula econômica permanece proposta conforme resposta expressa. Ainda é necessário detalhar tratamento de números não recebidos, comprovantes, custos elegíveis, lembretes, formatos adicionais e política de dados. A exceção individual de repetição foi removida do estudo conforme F46.

MC-02 amplia a base de esforço. A faixa anterior de 134–388 h dimensionava a versão anterior e requer revisão. O prazo será renegociado conforme F42. Os valores aprovados continuam registrados em R$ 24.000 de implantação e R$ 8.000 mensais posteriores por 80 horas, sujeitos a eventual decisão bilateral futura.

## Arquivos novos desta atualização

- `docs/05-prototipos/prototipo-navegavel-v0.2.html`
- `docs/05-prototipos/analise-prototipo-cliente-v0.1.md`
- `docs/05-prototipos/roteiro-prototipos-v0.2.md`
- `docs/05-prototipos/assets/c3-logo-color.png`
- `docs/05-prototipos/assets/c3-logo-light.png`
- `docs/02-requisitos/especificacao-funcional-v0.2.md`
- `docs/02-requisitos/alteracoes-escopo-v0.2.md`
- `docs/03-fluxos-permissoes/matriz-permissoes-v0.2.md`
- `docs/06-planejamento/atualizacao-prototipo-cliente-v0.2.md`

Índices, visão, governança, matriz de rastreabilidade e estrutura comercial foram atualizados para apontar a versão corrente. As versões anteriores permanecem como histórico. Todos os documentos novos e a interface derivada estão PROPOSTO, com decisões aprovadas identificadas na origem.
