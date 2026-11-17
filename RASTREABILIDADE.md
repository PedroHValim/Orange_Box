# Matriz de rastreabilidade de IHC

A matriz deve ser atualizada ao longo do semestre. Ela ajuda a demonstrar que a interface não surgiu arbitrariamente e registra **como o conhecimento da equipe evoluiu**.

Para projetos cujo TCC não previa interface, esta matriz é especialmente importante: deve ficar visível a passagem da **contribuição técnica do TCC** para um **cenário de uso plausível**, e desse cenário para as decisões de interação.

## 1. Derivação do escopo de IHC a partir do TCC

| Elemento | Registro da equipe | Evidência/justificativa | Estado |
|---|---|---|---|
| Tema do TCC | Detecção Automatizada do Ácaro da Leprose na Citricultura via Redes Neurais Convolucionais em Dispositivos Móveis | TCC | definido |
| Resultado técnico esperado | Sistema/Modelo | N/A | definido |
| O TCC previa interface? | Sim | TCC  | definido |
| Capacidade/contribuição central | Monitoramento com geolocalização de infestações de pragas e fácil acesso a detecção de pragas. | TCC | definido |
| Possíveis beneficiários/stakeholders | Inspetor de campo (pragueiro/trabalhador treinado) e responsável pelo manejo (dono/gestor, possivelmente agrônomo); stakeholders indiretos removidos | Entrega 1 revisada, seções 2.2 e 2.3 | hipótese (H26) |
| Usuário escolhido para IHC | Inspetor de campo (P02, primária); P01 e P03 secundárias/proto-personas | Atividade A01 (frequente e documentada no TCC [F16], [F18]); papéis de P01/P03 não confirmados | proposta / a validar |
| Objetivo principal do usuário | Inspetor: saber durante a inspeção se há sinal da praga e registrar a ocorrência (H29). Responsável pelo manejo: entender a distribuição das ocorrências para decidir (H21) — objetivos separados | Entrega 1 revisada, seção 3.1 | hipótese |
| Contexto de uso adotado | Campo aberto, pouca/nenhuma internet [F13]; sol forte, caminhada e pouco tempo por planta são hipótese (H30) | TCC; sem observação de campo registrada | parcialmente hipótese |
| Interface/recorte de IHC | Fluxo 1 (captura → resultado → registro) como principal; Fluxo 2 (mapa/decisão) como hipótese de trabalho condicionada a H21/H22 | Entrega 1 revisada, seção 7 | proposta / revisada |
| Relação com o TCC | parte prevista | TCC | definido |

> Se o escopo de IHC mudar ao longo do semestre, preserve a decisão anterior no histórico e registre **qual evidência motivou a mudança**.

## 2. Registro de hipóteses e lacunas da Entrega 1

Use esta tabela para itens importantes marcados como `[H]` ou `[?]`. Preserve o histórico: não apague uma hipótese refutada.

| ID | Afirmação / dúvida inicial | Tipo | Por que importa | Como/onde investigar | Evidência obtida | Estado atual | Impacto no projeto |
|---|---|---|---|---|---|---|---|
| H01 | Disponibilização do dataset do ácaro (contribuição técnica do TCC) | H | Contribuição técnica prevista | TCC | TCC | aberta | Fora do escopo de IHC |
| H02 | Trabalhadores que aplicam o produto podem não ser os que usam o app; aplicação localizada afetaria quem aplica | H | Define o repasse da decisão (T04 5.2) | Entrega 7 | PENDENTE | aberta | Repasse explícito em G08 (a validar) |
| H03 | Nem todos têm o mesmo nível de leitura/familiaridade tecnológica | H | Define simplicidade da interface | Entrega 7 | PENDENTE | aberta | Hipótese a decompor (H20, H28) |
| H05 | Como o acompanhamento da disseminação é feito hoje | ? | Justifica comparação entre ciclos (T08) | Entrega 7 | PENDENTE | aberta | — |
| H06 | Decidir onde aplicar é a atividade mais crítica | H | Prioriza T04/T08 | Entrega 7 | PENDENTE | aberta | — |
| H09 | Necessidade de histórico/rastreabilidade de onde já foi inspecionado | H | Cobertura da rota (T01 3.1, T09) | Entrega 7 | PENDENTE; ausência de registro do percurso não confirmada | aberta | — |
| H20 | Pouca familiaridade com aplicativos técnicos (decompor) | H | Simplicidade | Entrega 3/7 | PENDENTE | aberta | — |
| H21 | O dono/gestor acompanha a evolução e usaria o mapa | H | Justifica o Fluxo 2 | Entrega 3/7 | PENDENTE | aberta | Mapa = hipótese de trabalho |
| H23–H25 | Benefícios esperados (rebaixados de F03, F04, F05): detecção sem pragueiro, menor esforço, geolocalização auxilia gestão | H | Benefício só confirmável com uso | Entrega 14 | PENDENTE | aberta | — |
| H26 | Inspetor e responsável pelo manejo são papéis/pessoas diferentes | H | Define personas | Entrega 7 | PENDENTE | aberta | P01/P02/P03 como proto-personas |
| H27 | Pode ser necessária confirmação humana da detecção; falsos positivos/negativos têm consequências distintas | H | Divisão pessoa × IA | Entrega 7 | PENDENTE | aberta | Validação humana em T07 (a validar) |
| H28 | Uso de celular sem prática com apps técnicos (rebaixado de F12) | H | — | Entrega 7 | PENDENTE | aberta | — |
| H29/H30 | Objetivo do inspetor; condições de campo prováveis (sol, caminhada, pouco tempo) | H | Contexto | Entrega 7 | PENDENTE | aberta | — |
| H31–H33 | Etapa de processamento, alertas e "mais simples" (rebaixados de F28, F30, F31) | H | Evita requisitos sem evidência | Entrega 7/14 | PENDENTE | aberta | — |
| [?] | O que acontece depois que a praga é encontrada (registro, comunicação, consolidação, decisão, unidade espacial) | ? | Justifica o mapa e a decisão de manejo | Entrega 3/4/7 | PENDENTE | aberta | — |
| H04 | Quem decide no dia a dia onde e quando aplicar o produto de controle (dono/gestor ou agrônomo) | ? | Define o destinatário do parecer do agrônomo e o papel de P03 no fluxo (validar e recomendar, sem decidir a execução) | Entrega 7, entrevista I02 (perguntas 2 e 11) | Ainda sem coleta; cenário C03 e HTA T05 assumem que o agrônomo recomenda e o dono decide [H04] | aberta | Parecer enviado ao gestor (A07, MoLIC M01 S7 → P5; situação do pedido em A01/S1); se o agrônomo decidir a execução, o repasse muda de destinatário |
| H07 | O profissional precisa saber se há sinais da praga, em quais pontos, com que intensidade e se a situação exige ação imediata | H | Define o conteúdo mínimo da detecção que o agrônomo valida a distância | Entrega 7, entrevista I02 (perguntas 5, 6, 12 e 17) | Ainda sem coleta; necessidades de P03 (Entrega 3) e respostas hipotéticas do C03 (Q2) | aberta | Tela da detecção com foto original, data, hora, árvore, localização e histórico do ponto (A03, FA03); só pontos validados por humano entram na área de aplicação (A06, FA06) |
| H22 | Existe necessidade de guardar histórico das inspeções (visão do agrônomo) | H | Justifica o histórico do ponto na tela da detecção e o histórico com filtros | Entrega 5 (GOMS T06) e Entrega 7, entrevista I02 (perguntas 8 e 10) | GOMS T06 indica o histórico como base da comparação temporal do parecer; ainda sem coleta com agrônomos | aberta | Histórico do ponto em A03/FA03 e histórico com filtros em A05/FA05 (MoLIC M01 S5) |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos

| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação / signos | MoLIC | Tela(s) Figma | Heurística / problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | {{ex.: recomendação de otimização}} | {{...}} | {{P01}} | {{C01}} | {{T01}} | {{links}} | {{...}} | {{M01}} | {{F01...}} | {{V01 ou —}} | {{UT01}} | {{...}} |
| R02 |  |  |  |  |  |  |  |  |  |  |  |  |
| R03 | Detecção da praga em foto com geolocalização registrada na captura | O agrônomo recebe relatos de campo informais, sem local nem data, e precisa achar o foco | P03 | C03 | O13 / T05 (passos 1 e 2.1) | [HTA T05](docs/05_analise_tarefas.md) | CI03; pedido de parecer, propriedade, talhão, solicitante, pontos pendentes, situação da validação | M01 (S1, S2) | FA01, FA01V, FA02 | — (nenhuma violação ligada a O13 na Entrega 13) | UT07 → U03 (16/11/2026): pedido aberto, mas o certo foi escolhido por eliminação entre dois pedidos de Jaime → AU02 | Pedido de parecer agrupado por propriedade e talhão, levando direto ao mapa do talhão do foco. **AU02 (Entrega 14):** mostrar em FA01 o que distingue pedidos do mesmo gestor (talhão, pontos pendentes, data), a confirmar com novo teste |
| R04 | Resultado da detecção da IA por foto | Separar "sinal da IA" de "confirmação humana" antes de dimensionar a área | P03 | C03 | O14 / T07 | [CTT T07](docs/05_analise_tarefas.md) | CI03; detectado pela IA, avaliação da IA, veredito, validado por, observação técnica | M01 (S2, S3, P1) | FA02, FA02V, FA02R, FA03, FA03A, FA03E | V04, V05, V10, V11, V12, V13 (A02) | UT07 → U03: ponto 3 confirmado sem abrir a avaliação da IA (QA20); QA19 parcial → AU01 (via UT06) | Avaliação da IA recolhida até o agrônomo pedir (decisão a testar); situação da validação com cor e símbolo; progresso salvo por ponto. Correções de V04, V05, V13 e demais não aplicadas antes do teste (Entrega 12, QA21). **Entrega 14:** U03 decidiu sem abrir a avaliação da IA; AU01 recomenda indicar o autor do veredito no histórico |
| R05 | Registro geolocalizado das detecções ao longo dos ciclos | Comparar o foco atual com inspeções anteriores do mesmo ponto ou talhão | P03 | C03 | O15 / T06 | [GOMS T06](docs/05_analise_tarefas.md) | CI03; histórico de detecções, período, local, detecções anteriores do ponto | M01 (S5, P3, acesso ubíquo) | FA03, FA05, FA05V | V05, V09 (A02) | UT06 → U03: resposta correta em 64 s, QA06 não atingida (≤ 20 s); autor do veredito não identificado → AU01 | Detecções anteriores na própria tela da detecção (M3); lista única de histórico, filtrada conforme a origem. **AU01 (Entrega 14):** em FA03 e FA05, mostrar quem decidiu (“confirmada pelo agrônomo”) e a avaliação da IA em campo separado |
| R06 | Captura de foto em campo pelo aplicativo do trabalhador | Foto insuficiente para o parecer; hoje o agrônomo liga ou agenda visita | P03 (P02 recebe o pedido) | C03 | O16 / T07 (saída *Solicitar nova foto ao campo*) | [CTT T07](docs/05_analise_tarefas.md) | CI03; pedido de nova foto | M01 (S3 → P2) | FA03, FA02N | V06 (A02) | UT05 / pós-teste → U03: entendeu que a árvore L5-11 aguarda nova foto (QA19, parte atendida); nenhum AU | Botão em A03/FA03 que envia o pedido, ligado ao ponto e à árvore, à rota do trabalhador; o ponto continua "pendente" até a nova foto ser avaliada |
| R07 | Mapa dos pontos com detecção (geolocalização) | Recomendação em área maior ou menor que a afetada (C03, Q5) | P03 | C03 | O17 / T05 (passos 3 e 4) | [HTA T05](docs/05_analise_tarefas.md) | CI03; área de aplicação, pontos confirmados, produto, dose, período de aplicação | M01 (S6, P4) | FA06, FA06E | V03, V07, V08 (A02) | UT05 → U03: citou os pontos 2, 3 e 5, QA05 atingida; nenhum AU | Área delimitada sobre o mapa só com pontos confirmados; aviso de pendências sem bloquear; produto e dose apenas registrados |
| R08 | Registro das detecções e dos vereditos vinculados aos pontos | Parecer que se perde em mensagens soltas e não chega com clareza ao gestor | P03 → P01 | C03 | O18, O19 / T05 (passo 5) | [HTA T05](docs/05_analise_tarefas.md) | CI03; parecer técnico, pontos vinculados, destinatário do parecer, situação do pedido | M01 (S7, P5, S1) | FA07, FA07E, FA01C | V01, V02, V11 (A02) | UT05 → U03: disse que Jaime recebeu pelo aviso verde de FA01C, QA08 atingida; nenhum AU | Parecer com pontos vinculados automaticamente; após o envio, o pedido aparece como "concluído" na lista (A01/FA01); falha no envio mantém o texto para nova tentativa |

## 4. Rastreabilidade de padrões de interface

Use esta tabela quando o projeto incorporar padrões como dashboard, relatório, histórico, filtros ou administração. O objetivo é **justificar o padrão**, não apenas listar telas.

| ID da tela/fluxo | Padrão de interface | Objetivo/tarefa que justifica | Informação/ação principal | Evidência de necessidade | Artefatos relacionados |
|---|---|---|---|---|---|
| F01 | dashboard | {{T01}} | {{...}} | {{H01/evidência...}} | {{C01/M01}} |
| F02 | histórico com filtros | {{T02}} | {{...}} | {{...}} | {{...}} |
| F03 | administração/CRUD | {{T03}} | {{...}} | {{...}} | {{...}} |
| FA01 | alertas/ocorrências | T05 (passo 1) | Pedidos de parecer e detecções novas por propriedade e talhão, com pontos pendentes | Hipótese: C03 (relatos informais sem contexto); P03 atende várias propriedades [C03, Q4 e Q6, em aberto] | C03, CI03, M01/S1 |
| FA03 | explicabilidade/detalhamento | T07 | Foto original, metadados, detecções anteriores e avaliação da IA; veredito | H07; CTT T07 (análise concorrente na mesma tela) | C03, CI03, M01/S3 |
| FA05 | histórico com filtros | T06 | Lista única de detecções com filtros de período e local, aberta de FA01, FA02 ou FA03 | H22; GOMS T06 (métodos M1, M2 e M3); ciclos de cerca de 14 dias ao longo do ano [F16] | C03, CI03, M01/S5 |
| FA06/FA07 | encaminhamento e registro | T05 (passos 4 e 5) | Área de aplicação, parecer e repasse ao gestor | Hipótese: risco de área maior ou menor que a necessária [C03, Q5, em aberto; sem caso registrado]; [H04] quem inspeciona não é quem decide | C03, CI03, M01/S6–S7 |

## 5. Registro de mudanças de escopo

| Data | O que mudou | Evidência/feedback que motivou | Artefatos afetados | Responsável |
|---|---|---|---|---|
| 22/10/2026 | Fluxo do agrônomo (P03) proposto como aplicação web acessada pelo computador, e não pelo aplicativo de celular usado em campo | CTT T07 pede foto, zoom e histórico na mesma tela (Entrega 5), o que o protótipo em papel em formato de celular não atendia (A02, A03 e A05 em telas separadas, Entrega 6); hipótese de que P03 analisa fotos e histórico no escritório antes do parecer (Entrega 3, proto-persona) | Entregas 6 (nota sobre o formato), 8 e 11 (fluxo do agrônomo) | Guilherme Morais Escudeiro |
| 08/11/2026 | Usuário prioritário passa a ser o inspetor de campo (P02); P01/P03 secundárias/proto-personas; mapa e decisão de manejo tornam-se hipótese de trabalho; fatos F03–F05, F12, F24, F28, F30, F31 rebaixados a hipótese; RC01–RC07 reclassificadas; cenários C01–C03 refeitos com Q1–Q8 e `[Qn]`; HTA/GOMS/CTT corrigidos formalmente | Feedback do professor (Entregas 1 a 6) | Entregas 1 a 6 | Equipe |
| 15/11/2026 | Protótipo FA do fluxo do agrônomo mantido sem as correções apontadas na inspeção heurística (V01–V13, A02) para o teste com U03 | Comparar os problemas da inspeção com o comportamento do participante (Entrega 14, seção F) | Entregas 12 (QA21), 13 e 14 | Guilherme Morais Escudeiro |

## 6. Personas, cenários, tarefas e protótipos (Entregas 3 a 6)

Cadeia: **necessidade/problema → persona → cenário → tarefa → modelo de tarefa → fluxo de protótipo → tela/estado**. Estado: *proto-persona* = sem entrevista/observação registrada; nenhum cenário foi validado com pessoas reais.

| Persona | Tipo / estado | Hipóteses relacionadas | Cenário | Tarefas (modelos) | Fluxo de protótipo | Telas | Situação |
|---|---|---|---|---|---|---|---|
| P03 Marcelo Fidalgo | secundária; proto-persona (só F08 é fato) | H04, H07, H21, H22 | C03 (Q1–Q8; casos passados fictícios removidos) | T05 HTA, T06 GOMS, T07 CTT | PF03, PF04; MoLIC M01 | A01–A03, A05–A07 (papel); FA01–FA07 e estados (Figma, Entrega 11) | Papel avaliado por Lucas e Pedro (Entrega 6, sem notas individuais); telas FA produzidas (Entrega 11) e inspecionadas (Entrega 13, V01–V13 de A02); entrevista I02 (Entrega 7) não aplicada, por isso P03 permanece proto-persona; teste com U03 (Entrega 14) ainda não realizado |

| Item | Estado |
|---|---|
| Walkthrough (Entrega 6) | Formativo: comentários de Vitor no aplicativo e avaliação cruzada entre integrantes. Guilherme avaliou PF01/PF02 e PF05/PF06 em 08/11/2026 (7 observações registradas); a avaliação de PF03/PF04 por Lucas e Pedro não tem notas individuais |
| Alterações pós-simulação (Entrega 6, item 5) | Registradas no aplicativo; das observações de Guilherme, botão de captura e contagem de ácaros atendidos (`Camera.jpeg`, `Historico.jpeg`), demais pendentes |
| Cenários C01–C03: hipóteses vs. fatos | Hipóteses marcadas `[H]` e perguntas `[Qn — em aberto]`; confirmação na Entrega 7 |
| Padrões da Entrega 2 | RC01 (candidata), RC02 (candidata), RC03 (hipótese), RC04 (reforça decisão do TCC), RC05 (reformulada), RC06 (diretriz), RC07 (diretriz) |

## Como usar

- Use identificadores estáveis (`H01`, `P01`, `C01`, `T01`, `M01`, `F01`, `UT01`).
- Quando uma necessidade/problema tiver origem em hipótese da Entrega 1, cite o ID correspondente.
- Em TCC sem interface original, pelo menos uma linha deve mostrar claramente **como uma capacidade técnica chega até uma tarefa de usuário e uma tela/fluxo**.
- Uma linha pode se desdobrar quando um objetivo possui múltiplos caminhos.
- Não force relação inexistente: se algo ainda não foi modelado, marque `PENDENTE`.
- Ao remover uma funcionalidade, registre a decisão em vez de apagar silenciosamente o histórico.
- Dashboard, CRUD, filtros e relatórios só devem aparecer quando houver objetivo/tarefa que os justifique.
