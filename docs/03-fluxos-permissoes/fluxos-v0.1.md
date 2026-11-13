# Contexto e fluxos funcionais

Status PROPOSTO • ESF-C3-0.1 • 10/11/2026.

Diagramas Mermaid editáveis. Regras e critérios completos estão nos módulos RF e dicionário. Decisões na origem aprovadas permanecem citadas nesses módulos. Transições detalhadas desta versão são PROPOSTO. FL-01–06 cobrem os processos MVP e a fronteira da integração pontual com rastreador.

## FL-01 — Contexto, acesso e cadastros

```mermaid
flowchart LR
    P[Promotores] -->|Visitas, campanhas, combustível e métricas permitidas| C3[Plataforma C3]
    E[Escritório] -->|Cadastros e operações administrativas| C3
    M[Master reservado] -->|Contas, vínculos, configurações e correções| C3
    C3 -->|Consulta pontual de posição| API[API Upcar]
    E -->|Importa fontes homologadas e compras faturadas| C3
    C3 -->|PDF e consultas ou Excel autorizados| E
    CLI[Cliente] <-->|WhatsApp ou e-mail operados pelo Escritório| E
    FOR[Fornecedor e seu sistema] <-->|Campanhas e lançamento manual PRODUTO e QTD| E
    E -->|Registra decisões e resultados externos| C3
```

RF-01 valida sessão e permissão antes de cada operação. RF-02 e RF-06.01 mantêm entidades. Master cria contas e vínculo fixo ao veículo. Nenhuma seta entre atores externos e Escritório representa integração automática da plataforma.

## FL-02 — Visita e gravação com exceções

```mermaid
flowchart TD
    A[Promotor seleciona cliente ativo] --> B[Exibir campanhas e avisos vigentes]
    B --> C{Já tem visita aberta?}
    C -->|Sim| D[Encerrar ou solicitar regularização]
    C -->|Não| E[Solicitar check-in com veículo fixo]
    E --> F[Obter posição conforme FL-03]
    F --> G{Posição válida com idade entre 0 e 300 s?}
    G -->|Sim| H[Preparar evento com posição atual]
    G -->|Não| I[Exigir justificativa e marcar conferência]
    I --> H
    H --> J{Persistiu visita e evento?}
    J -->|Não| K[Informar falha e permitir repetir mesma operação]
    K --> E
    J -->|Sim| L[Confirmar visita aberta]
    L --> N[Promotor registra motivo e observações]
    N --> O[Solicitar check-out]
    O --> Q[Consultar posição e aplicar mesma regra de exceção]
    Q --> R{Persistiu encerramento?}
    R -->|Não| S[Manter aberta e permitir repetir]
    S --> O
    R -->|Sim| T[Confirmar encerrada e preservar histórico]
```

RF-03.02/03 garantem uma visita aberta e idempotência. Falha ao consultar posição permite a exceção justificada. Falha na gravação não confirma o evento. Somente o Master regulariza registros encerrados/esquecidos, com horário informado separado do instante da correção.

## FL-03 — Posição pontual do veículo

```mermaid
sequenceDiagram
    participant P as Promotor
    participant S as Servidor C3
    participant U as API Upcar
    participant D as Dados C3
    P->>S: Solicitar evento de visita
    S->>S: Autorizar conta e resolver veículo fixo
    S->>U: Consultar última posição com credencial protegida
    alt Resposta recebida
        U-->>S: Veículo, posição, validade e instante do dispositivo
        S->>S: Validar coordenadas, validade e idade
    else Falha ou ausência de posição
        S->>S: Classificar indisponibilidade
    end
    alt Posição fora da regra ou indisponível
        S-->>P: Solicitar justificativa para conferência
        P->>S: Confirmar evento com justificativa
    end
    S->>D: Salvar evento e fotografia dos dados recebidos
    alt Gravação concluída
        D-->>S: Identificador persistido
        S-->>P: Confirmar evento
    else Falha ao salvar
        S-->>P: Informar falha e permitir repetição segura
    end
```

Aplicam-se RF-03.09, D-06 e DP-03. Token, permissões reais, fuso da posição e latência aguardam homologação. O snapshot não muda depois do evento. Instantes de evento, consulta e dispositivo permanecem separados. Horário desconhecido/futuro, `valida=false` ou coordenadas inválidas exigem classificação de exceção. Timeout inicial de dez segundos é proposta D-06.

## FL-04 — Campanhas e avisos

```mermaid
flowchart TD
    A[Escritório ou Promotor solicita campanha] --> B[Solicitação registrada]
    B --> C[Escritório trata com fornecedor externamente]
    C --> D{Decisão externa?}
    D -->|Pendente| B
    D -->|Rejeitada| E[Registrar rejeição e conservar histórico]
    D -->|Aprovada| F[Registrar aprovação]
    F --> G[Definir alvos, vigência e folders]
    G --> H{Aprovada, folder pronto e dentro da vigência?}
    H -->|Sim| I[Exibir ao selecionar cliente-alvo]
    H -->|Não| J[Manter consultável administrativamente]
    I --> K{Venceu ou foi cancelada?}
    K -->|Sim| J
    K -->|Não| I
    N[Escritório cria aviso por cliente e período] --> O{Dentro da vigência e cliente correspondente?}
    O -->|Sim| Q[Exibir aviso ao selecionar cliente]
    O -->|Não| R[Conservar registro sem exibição ativa]
```

Decisão externa e condição de exibição são dimensões distintas. Uma campanha aprovada pode estar futura, sem folder, ativa ou vencida. Cancelamento com motivo interrompe exibição e preserva histórico. Datas inclusivas são PT-05. RF-04 e RF-03.08 definem campos e critérios.

## FL-05 — Cotação, decisões e envio manual

```mermaid
flowchart TD
    A[Registrar solicitação manual e anexos] --> B[Validar e publicar lote Wega homologado]
    B --> C[Compor versão e gerar PDF]
    C --> D[Escritório apresenta pelo canal de origem]
    D --> E{Resposta do cliente?}
    E -->|Alteração| F[Criar nova versão preservando anterior]
    F --> C
    E -->|Rejeição| G[Registrar motivo e evidência]
    G --> H{Escritório decide?}
    H -->|Revisar| F
    H -->|Encerrar| I[Encerrar com histórico]
    E -->|Aprovação| J[Registrar evidência vinculada à versão]
    J --> K[Revisar internamente]
    K --> L{Revisão liberada?}
    L -->|Não| F
    L -->|Sim| M[Autorizar versão atual]
    M --> N[Operador lança PRODUTO e QTD no fornecedor]
    N --> O[Registrar envio e resultado externo]
    O --> Q[Preservar versão e protocolo]
    M -->|Mudança antes do envio| F
```

### Dimensões e guardas de estado

| Dimensão | Valores e regra |
|---|---|
| Conteúdo | Rascunho editável antes de apresentação. Alteração de conteúdo apresentado gera sucessor numerado. Anterior permanece histórico |
| Resposta cliente por versão | RASCUNHO, APRESENTADA, ALTERACAO_SOLICITADA, APROVADA_CLIENTE, REJEITADA_CLIENTE. SUBSTITUIDA identifica versão sucedida sem apagar decisões anteriores |
| Revisão interna por versão | Sem revisão, AJUSTAR ou LIBERAR. Liberação só vale para conteúdo conferido |
| Autorização por versão | Ausente ou registrada com autor/instante. Requer cliente aprovado, revisão liberada e versão atual |
| Envio externo | Não enviado ou envio registrado para versão autorizada, com data e referência disponível |
| Resultado externo | PENDENTE, ACEITO ou REJEITADO propostos. Pedido aceito não equivale a compra faturada |
| Encerramento por rejeição | Escritório registra revisar ou encerrar com motivo. Revisar gera nova versão |
| Mudança após envio | PT-08 propõe Master para retificação interna e Escritório para tratar efeitos externos. Preservar o que foi efetivamente enviado |

RF-05 detalha cada guarda. As contagens administrativas informam qual dimensão está sendo contada. Revisão e autorização podem ser feitas pela mesma pessoa. Captura de respostas e envio ao fornecedor são operações humanas externas.

## FL-06 — Abastecimento e correção

```mermaid
flowchart TD
    A[Selecionar veículo autorizado] --> B[Informar data, hodômetro, litros e valor]
    B --> C{Lançamento retroativo?}
    C -->|Sim| D[Exigir Escritório ou Master e justificativa]
    C -->|Não| E[Validar campos obrigatórios e valores]
    D --> E
    E --> F[Conferir registros cronológicos anterior e posterior]
    F --> G{Consistente e revisão atual?}
    G -->|Não| H[Informar conflito sem confirmar gravação]
    G -->|Sim| I[Salvar lançamento e autoria]
    I --> J[Atualizar histórico e totais autorizados]
    J --> K{Necessita correção?}
    K -->|Sim| L[Master justifica e retifica preservando anterior]
    L --> F
```

RF-06 exige consistência do veículo sob concorrência. Data real do abastecimento e instante de inclusão são distintos. Empate de ordem no mesmo dia e troca de hodômetro são detalhes propostos em D-12. Correção substitui contribuição atual nos totais e conserva trilha.

## Verificação documental

Os diagramas foram revisados em conjunto com as tabelas de regras e critérios. A validação de execução ocorrerá na implementação. A renderização visual Mermaid ainda deverá ser conferida no visualizador adotado pelo projeto.
