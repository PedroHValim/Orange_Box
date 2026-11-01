# Entrega 10 — MoLIC

**Data:** 01/11/2026<br>
**Status:** 🟨 em andamento — conversa M02 especificada; diagramas e consolidação pendentes.<br>
**Responsabilidade:** 1 solução completa por integrante.

## Objetivo da atividade

Modelar a interação como conversa entre usuário e preposto do designer, incluindo caminhos principais, alternativas, rupturas e formas de recuperação.

## M01 — {{objetivo do agrônomo}}

**Autor(a):** Guilherme — {{matrícula}}<br>
**Cenário de interação de origem:** CI03<br>
**Objetivo(s):** {{IDs fixados na Entrega 9}}<br>
**Tarefa(s) relacionada(s):** {{...}}<br>
**Signos relevantes:** {{...}}

### Diagrama

![MoLIC M01](../assets/10_molic/molic_m01.svg)

**Fonte editável:** {{inserir link}}

### Leitura do diagrama

#### Caminho principal

1. {{...}}
2. {{...}}

#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

### Checklist específico de modelagem

- [ ] Ponto de abertura, cenas e encerramento identificados.
- [ ] Falas, processamento e rupturas seguem a notação da aula.
- [ ] Objetivos e signos são coerentes com a Entrega 9.
- [ ] Diagrama e fonte editável foram inseridos e conferidos.

## M02 — Inspecionar a rota e repassar os achados

**Autor(a):** Lucas — 24.123.032-5<br>
**Cenário de interação de origem:** CI02 — inspeção dos frutos e repasse dos achados.<br>
**Objetivo(s):** O01 — inspecionar os pontos da rota; O02 — obter uma foto analisável; O03 — entender o resultado da foto; O04 — registrar o achado e seu local; O05 — confirmar o repasse dos registros.<br>
**Tarefa(s) relacionada(s):** T01 — inspecionar a rota e repassar achados; T02 — verificar um fruto e encaminhar o resultado; T03 — relação temporal da inspeção e do repasse.<br>
**Signos relevantes:** ponto planejado, situação do ponto, foto do fruto, qualidade da foto, situação da análise, resultado da foto, data e hora, local do achado, situação do registro, destinatário e situação do envio.

### Diagrama

O arquivo abaixo é o **local reservado** para o diagrama. Desenhá-lo com a notação MoLIC e a legenda apresentadas na aula, usando a especificação das cenas e transições que segue.

![MoLIC M02](../assets/10_molic/molic_m02.svg)

**Fonte editável:** {{inserir link do arquivo .drawio ou outro formato editável após desenhar M02}}

### Cenas, processamento e encerramentos para desenhar

| Elemento | Tópico ou função na conversa | Conteúdo que precisa aparecer |
|---|---|---|
| Ponto de abertura | Início da inspeção | Antônio abre a rota que recebeu para o dia. |
| S1 — Orientar a rota | “Qual ponto devo inspecionar?” | Talhão, linha e árvore do próximo ponto; distinção entre pontos planejados, com registro e pendentes. |
| S2 — Preparar a foto | “A imagem está adequada?” | Orientações de distância, foco e iluminação; possibilidade de fotografar, ajustar ou voltar à rota. |
| Processamento do sistema | Analisar a foto capturada | Indicação de que a análise está ocorrendo no celular; possibilidade de cancelar. Representar conforme a notação de processamento ensinada na aula. |
| S3 — Interpretar o resultado | “O que esta foto indica?” | Uma das mensagens: “sinal suspeito”, “nenhum sinal nesta foto” ou “resultado inconclusivo”. Explicitar que a IA não confirmou a infestação. |
| S4 — Identificar o achado | “Onde esta foto foi tirada?” | Local obtido por GPS ou identificação manual por talhão, linha e árvore; indicação da origem do local. |
| S5 — Confirmar o registro | “A foto e o resultado foram guardados?” | Confirmação de que foto, resultado, data, hora e local foram salvos no celular. |
| S6 — Conferir a rota | “O que já tem registro e o que falta?” | Pontos planejados com registro e pendentes; opção de continuar ou encerrar com pendência explicitada. |
| S7 — Conferir o repasse | “Os achados chegaram ao gestor?” | Estados “aguardando conexão”, “enviando”, “enviado” e “falha no envio”. “Enviado” não significa “lido”. |
| Encerramento com objetivo concluído | Rota conferida e registros enviados | O usuário sabe quais pontos têm registro e que os achados foram disponibilizados ao gestor. |
| Encerramento com pendência | Inspeção interrompida ou rota incompleta | Registros locais preservados e pontos não cobertos identificados; o usuário pode retomar depois. |

As cenas representam **assuntos da conversa**. P01–P07, da Entrega 6, podem ajudar a implementar essas cenas no Figma, mas não são os nomes das cenas no MoLIC.

### Leitura do diagrama

#### Caminho principal

1. Antônio abre a inspeção. Em **S1**, pergunta implicitamente qual ponto deve visitar; o sistema informa o próximo ponto planejado e o que já possui registro.
2. Ele escolhe o ponto e entra em **S2**. O sistema orienta o enquadramento. Antônio ajusta a imagem e comunica a decisão de fotografar.
3. O sistema **processa a foto** e comunica que a análise está em andamento. Quando termina, inicia-se **S3**.
4. Em **S3**, Antônio interpreta a indicação da foto. Diante de “sinal suspeito”, entende que o resultado precisa de confirmação e escolhe registrar o achado.
5. Em **S4**, confere o local obtido. O sistema salva foto, resultado, data, hora e local e confirma em **S5** que o registro está no celular.
6. Antônio pode voltar a **S2** para outro fruto ou consultar **S6** para verificar a rota. Ao encerrar, o sistema informa os pontos que permaneceram pendentes.
7. Em **S7**, Antônio verifica se os registros estão aguardando conexão, em envio ou enviados. O caminho termina quando ele compreende a cobertura da rota e a situação do repasse.

#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| Foto desfocada ou mal enquadrada. | S2 — preparar a foto. | `D: Ajuste o foco ou a distância antes de fotografar.` | Antônio reposiciona o celular e permanece em S2; também pode voltar a S1. |
| Antônio cancela a análise. | Processamento após S2. | `D: Análise cancelada. A foto ainda não gerou resultado.` | Volta a S2 para fotografar novamente ou a S1 para abandonar aquele ponto. |
| Análise falha. | Processamento após S2. | `D: Não foi possível analisar esta foto.` | Tenta novamente ou refaz a foto em S2, sem marcar o ponto como analisado. |
| Nenhum sinal na foto. | S3 — interpretar o resultado. | `D: Nenhum sinal nesta foto; isso não garante que a árvore esteja livre.` | Salva o resultado, se fizer parte do registro da inspeção, ou segue para outro fruto sem registrar ausência de praga em toda a árvore. |
| Resultado inconclusivo. | S3 — interpretar o resultado. | `D: Não foi possível concluir. Refaça a foto ou guarde para conferir.` | Volta a S2 ou segue a S4 mantendo o resultado identificado como inconclusivo. |
| GPS indisponível. | S4 — identificar o achado. | `D: Local não obtido. Informe talhão, linha e árvore.` | Antônio fornece esses campos; o sistema marca “local manual, sem coordenadas”. |
| Identificação manual incompleta. | S4 — identificar o achado. | `D: Informe o campo que falta para salvar o local.` | Corrige o campo indicado e permanece em S4; a foto e o resultado são preservados. |
| Falha ao salvar no celular. | Transição de S4 para S5. | `D: Registro não salvo. Tente novamente.` | Nova tentativa sem descartar foto e resultado; se desistir, o ponto permanece pendente. |
| Rota encerrada com pontos pendentes. | S6 — conferir a rota. | `D: Há pontos sem registro. A rota será marcada como incompleta.` | Retoma a inspeção em S1 ou encerra mantendo a pendência visível. |
| Sem internet. | S7 — conferir o repasse. | `D: Salvo no celular; aguardando conexão para enviar.` | Antônio pode encerrar o uso; os registros permanecem locais para envio posterior. |
| Falha no envio. | S7 — conferir o repasse. | `D: Não foi possível enviar. Seus registros continuam salvos.` | Tenta novamente quando houver conexão, sem repetir registros já enviados. |

**Acesso à rota durante a inspeção:** se representado como acesso ubíquo no diagrama, ele deverá retornar a **S1/S6** preservando a foto ou o registro já salvo. Sua finalidade é permitir conferir o ponto atual e as pendências, não abrir uma navegação genérica.

### Checklist específico de modelagem — M02

- [x] Existe ponto de abertura coerente com o início do objetivo.
- [x] As cenas especificadas representam tópicos da conversa.
- [x] As falas e transições foram descritas como comunicação entre usuário e sistema.
- [x] Há encerramento para conclusão e para interrupção com pendências.
- [ ] O processamento foi desenhado com a notação MoLIC adotada em aula.
- [x] As rupturas especificadas possuem feedback e recuperação.
- [x] O possível acesso à rota possui justificativa semântica.
- [x] Estão descritos caminhos alternativos além do principal.
- [x] Objetivos, tópicos e signos seguem a parte de Lucas da Entrega 9.
- [ ] O diagrama foi produzido e verificado em tamanho normal no GitHub.
- [x] A especificação modela a conversa com o usuário, não o interior do algoritmo.
- [x] Processamento, registro e envio incluem retornos e falhas relevantes.

**Situação de M02:** a especificação textual está pronta; os itens referentes ao **desenho** permanecem abertos até a criação e conferência do SVG editável.

## M03 — {{objetivo do gestor}}

**Autor(a):** Pedro — {{matrícula}}<br>
**Cenário de interação de origem:** CI01<br>
**Objetivo(s):** {{IDs fixados na Entrega 9}}<br>
**Tarefa(s) relacionada(s):** {{...}}<br>
**Signos relevantes:** {{...}}

### Diagrama

![MoLIC M03](../assets/10_molic/molic_m03.svg)

**Fonte editável:** {{inserir link}}

### Leitura do diagrama

#### Caminho principal

1. {{...}}
2. {{...}}

#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

### Checklist específico de modelagem

- [ ] Ponto de abertura, cenas e encerramento identificados.
- [ ] Falas, processamento e rupturas seguem a notação da aula.
- [ ] Objetivos e signos são coerentes com a Entrega 9.
- [ ] Diagrama e fonte editável foram inseridos e conferidos.

## Consolidação da equipe

### Cobertura dos objetivos

| Objetivo | MoLIC que cobre | Lacunas/duplicidades | Decisão |
|---|---|---|---|
| O01 — inspecionar pontos da rota | M02 | Conferir a ligação com a rota orientada pelo gestor em M03. | Manter em M02 a conversa de inspeção de P02. |
| O02 — obter foto analisável | M02 | Nenhuma identificada na especificação de Lucas. | Representar preparação, ajuste e nova captura. |
| O03 — entender resultado da foto | M02 | Conferir nomenclatura com a validação humana de M01. | Separar “resultado da IA” de “veredito do agrônomo”. |
| O04 — registrar achado e local | M02 | Conferir quais dados M01 e M03 recebem do registro. | Reutilizar os mesmos signos de foto, data, hora e local. |
| O05 — confirmar repasse | M02 | Conferir a passagem do registro ao gestor em M03. | Distinguir “enviado” de “lido” ou “avaliado”. |
| {{objetivos de Guilherme}} | M01 | {{...}} | {{...}} |
| {{objetivos de Pedro}} | M03 | {{...}} | {{...}} |

A consolidação final depende dos diagramas dos três integrantes e da fixação dos IDs de objetivos na Entrega 9.

### Preparação para o Figma

**Estados necessários para o fluxo de Lucas, derivados das conversas M02:**

- Rota com próximo ponto e pontos pendentes — S1.
- Câmera com orientação de foco — S2.
- Foto inadequada e ajuste — ruptura em S2.
- Análise em andamento, cancelada ou com falha — processamento.
- Resultado suspeito, sem sinal na foto ou inconclusivo — S3.
- Local obtido por GPS ou identificação manual incompleta/completa — S4.
- Confirmação de registro salvo ou falha ao salvar — S5.
- Revisão da rota completa ou com pendências — S6.
- Registro aguardando conexão, em envio, enviado ou com falha — S7.

**Estados de Guilherme:** {{derivar de M01}}.

**Estados de Pedro:** {{derivar de M03}}.

Antes de produzir o Figma, conferir se cada estado possui uma conversa ou ruptura correspondente no MoLIC.

## Erros frequentes a evitar

- Desenhar apenas caixas com nomes de telas e setas de navegação.
- Omitir falhas, cancelamento, volta ou recuperação.
- Usar rótulos genéricos sem tópico de conversa.
- Criar no Figma caminhos ausentes do MoLIC.
- Entregar diagrama sem legenda, fonte editável ou texto legível.
