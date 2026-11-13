# Revisão de prontidão para a Etapa 2

Status PROPOSTO • Versão 0.1 • 10/11/2026 • Base documental v0.21, fontes F01–F31.

Registro histórico. Autorização recebida em F32, 10/11/2026. Resultado corrente em [Entrega da Etapa 2](situacao-etapa-2.md).

## Parecer proposto

Há definições suficientes para iniciar a especificação funcional detalhada. As decisões de atores, cadastros, pedidos, visitas, campanhas, abastecimentos, indicadores e condições comerciais foram consolidadas com as aprovações do responsável. Propõe-se avançar à Etapa 2 após autorização expressa, com as dependências abaixo vinculadas ao trabalho de especificação, arquitetura e homologação.

A viabilidade técnica dos 30 dias permanece pendente. A análise deverá considerar a capacidade de Ismael Zaccah de 80 h/mês, todos os módulos previstos, a API do rastreador e a alimentação das compras por Excel. MC-01 registra a alteração do recorte da API de rastreamento.

## Estado de D01–D16

| ID | Decisão consolidada | Encaminhamento remanescente |
|---|---|---|
| D01 | Wega disponível. Demais fornecedores serão apresentados conforme aceite contratual, com fontes potencialmente em planilha, PDF ou site | Formalizar conjunto inicial e condições de inclusão por fornecedor no anexo técnico. Identificar materiais e estimar cada tratamento antes do compromisso detalhado |
| D02 | PDF com código e Grupo como descrição, UNIT direto da planilha, TOTAL = QTD × UNIT em três casas e MULTI mínimo | Especificar precisão de UNIT, modo de arredondamento, exemplos, arquivo específico de fornecedor quando aplicável e critérios de homologação |
| D03 | Revisor/autorizador pode ser a mesma pessoa do Escritório. Evidência anexada, versões preservadas, reautorização após mudança e encaminhamento de rejeição definidos | Desdobrar fluxos e cenários de teste |
| D04 | Escritório e Promotores são atores operacionais. Master gerencia contas/configurações/correções excepcionais. Clientes compartilhados, visitas próprias e abastecimentos do veículo fixo | Construir matriz detalhada de ações, campos e alcance dos registros conforme as decisões aprovadas |
| D05 | Uma visita aberta por promotor, horário do sistema, edição durante abertura, regularização por Master e confirmação após salvar | Especificar repetição de operações, concorrência e exceções sem alterar as regras aprovadas |
| D06 | API do veículo fixo, posição com até cinco minutos e justificativa/conferência nas exceções | Configuração protegida e homologação autenticada da API, permissões, tempo/fuso, disponibilidade e esforço da integração |
| D07 | Estabelecimento/CNPJ único, campos básicos, cadastro pelo Escritório, acesso de todos os promotores e inativação com histórico | Dicionário de dados, validações e exemplos |
| D08 | Campanhas por fornecedor/vários clientes, decisão externa, folders, vigência, avisos internos e cancelamento | Campos, tipos/tamanhos de arquivos e cenários de borda |
| D09 | Lançamento por promotor/Escritório, acesso por veículo, campos, validações, correção por Master e retroativos pelo Escritório | Precisão, mensagens e exemplos cronológicos de hodômetro |
| D10 | Indicadores, filtros e saídas Excel definidos. Métricas de compras por cliente/fornecedor com fonte Excel | Obter amostra da planilha de compras. Definir alimentação, periodicidade, identificação, ajustes e duplicidade |
| D11 | C3 custeia infraestrutura e futura IA. Nuvem/hospedagem serão criadas. Crescimento esperado, volumes desconhecidos | Confirmar domínio/titularidade, levantar volumes e propor cenários, custos, segurança, retenção, backup e metas de operação |
| D12 | Ismael desenvolve dentro de 80 h/mês, incluindo implantação | Estimar trabalho e confrontar capacidade com a previsão comercial de 30 dias |
| D13 | Início após aceite da proposta e assinatura. Término na entrega formal para testes. Homologação em cinco dias úteis | Registrar datas reais e procedimento de apresentação |
| D14 | R$ 12.000 pré/R$ 12.000 pós-MVP. Serviço mensal inicia depois, em ciclos da data de início e vencimento no fechamento | Redigir calendário e regras de contagem no instrumento contratual |
| D15 | Horas expiram, garantia durante contratação mensal, suporte WhatsApp/e-mail seg–sex 9h–17h e rescisão confirmada sem multa adicional | Redigir cobertura, rito de suporte, encerramento e obrigações na minuta para revisão jurídica |
| D16 | Caio Costa valida requisitos, testa e aceita entregas | Combinar disponibilidade e canal de apresentação/aceite |

## Dependências com responsáveis e momento de resolução

| Dependência | Responsável pelo encaminhamento | Quando resolver | Efeito enquanto pendente |
|---|---|---|---|
| Planilha de compras faturadas, com significado de data/valor e identificação de cliente/fornecedor | Caio fornece amostra, Ismael analisa | Durante especificação da alimentação e antes de homologar o layout | A regra do indicador está definida. O processamento da fonte depende do arquivo real |
| Próximas fontes de fornecedores e conjunto inicial contratado | Caio apresenta materiais, Ismael estima e ambas as partes aprovam | No detalhamento do anexo técnico e em cada inclusão posterior | Preservar a demanda expressa de múltiplos fornecedores e registrar condições de inclusão. Evitar compromisso genérico sem identificar formato/processo |
| Uso efetivo da API Upcar e permissões da conta C3 | Ismael valida na etapa técnica, com João Vitor para esclarecimentos | Antes da aprovação técnica da integração e da entrega do fluxo integrado | Evidência atual é documental. Credenciais estão com o responsável conforme F22 |
| Volumes, arquivos e crescimento | Caio informa dados quando disponíveis, Ismael propõe cenários | Antes de aprovar infraestrutura e metas mensuráveis | Cenários devem ser identificados como hipóteses e aprovados com custos |
| Domínio costaltda.com, titularidade e acesso às contas | Caio confirma com o provedor atual, Ismael orienta requisitos técnicos | Antes de contratar/configurar produção | E-mail informado sugere domínio, mas sua situação permanece a confirmar |
| Parecer de prazo e capacidade | Ismael prepara estimativas e riscos | Após detalhamento suficiente, respeitando avaliação dos primeiros cinco dias úteis do marco contratual | Viabilidade de 30 dias ainda em aberto. Mudanças de escopo/preço/prazo exigem aprovação bilateral |
| Revisão jurídica | Responsável encaminha minuta ao advogado | Antes da assinatura | Condições comerciais registram intenção aprovada, com formalização jurídica futura |

## Trabalho proposto para a Etapa 2

1. Desdobrar a matriz corrente em requisitos identificados individualmente, com ator, campos, obrigatoriedade, validações, regras, fluxo normal e exceções.
2. Produzir critérios de aceite verificáveis, vinculados às decisões e às fontes, mantendo rastreabilidade e classificação de escopo.
3. Elaborar matriz de permissões no servidor para Escritório, Promotores e Master, incluindo alcance de consulta, criação, edição e correção excepcional.
4. Preparar diagramas Mermaid editáveis de contexto, pedidos/aprovações, visitas, campanhas/avisos e abastecimentos.
5. Definir dicionário de dados funcional e contratos de entrada/saída conhecidos. Marcar os layouts futuros e a planilha de compras como dependências até sua análise.
6. Propor requisitos não funcionais mensuráveis e cenários de validação, levando parâmetros de infraestrutura/custo para a etapa de arquitetura quando necessário.
7. Apresentar a especificação e os conflitos/pendências remanescentes ao responsável para revisão antes do planejamento técnico definitivo.

O parecer propõe preparação da especificação e dos fluxos. Desenvolvimento, contratação de serviços, publicação e comunicações externas continuam sujeitos às autorizações correspondentes. A decisão de iniciar a Etapa 2 ainda depende do responsável, conforme F07.

