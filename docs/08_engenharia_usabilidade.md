# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** {{dd/mm/aaaa}}  
**Status:** ⬜ não iniciada  
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e **metas de usabilidade verificáveis**, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

Antes das características da plataforma, separe:

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| contribuição técnica do TCC | {{algoritmo/modelo/API/análise...}} | desempenho técnico não é substituído pelo teste de IHC |
| camada de interação da disciplina | Fluxo do agrônomo (P03): pedidos de parecer e detecções novas, mapa do talhão com a situação de cada ponto, tela da detecção com histórico do ponto, veredito (confirmar, rejeitar, pedir nova foto), histórico, delimitação da área, parecer e repasse ao gestor (A01–A03 e A05–A07 da Entrega 6). | compreensão, eficácia, eficiência, satisfação, erros, acessibilidade etc. |
| integrações/dados simulados | Fluxo do agrônomo (P03): detecções, fotos, localização e histórico dos pontos; envio do pedido de nova foto à rota do trabalhador (P02); recebimento do pedido de parecer vindo do gestor (P01) e entrega do parecer ao gestor. | As detecções serão fictícias ou retiradas de imagens do dataset do TCC, com o resultado da IA definido pela equipe. Falhas de envio e atrasos serão simulados por estados prontos no Figma. O teste avalia a interação, não a qualidade das detecções. |

Em um protótipo de disciplina, é aceitável simular processamento ou resultados quando a implementação técnica não estiver integrada, desde que isso seja declarado e a simulação seja suficiente para avaliar a interação.

**Fluxo do agrônomo (P03):** as telas citadas nesta entrega seguem a numeração do protótipo em papel (Entrega 6), mas descrevem o protótipo que será avaliado no Figma (Entrega 11). O histórico do ponto na tela da detecção, com o atalho "ver histórico deste ponto" (A03/F03), os filtros de período e local do histórico (A05/F05) e o aviso de que o parecer não substitui o receituário agronômico (A07/F07) não foram desenhados no papel, mas fazem parte do MoLIC M01 (S3, S5 e S7) e entram no Figma. As metas que dependem deles, como a MU06, valem para o protótipo do Figma.

## 1. Características da plataforma

| Característica | Descrição | Consequência para IHC |
|---|---|---|
| Software | Fluxo do agrônomo (P03): aplicação web acessada pelo navegador, com conta do agrônomo vinculada às propriedades que atende; os dados vêm do servidor que recebe as inspeções sincronizadas pelo celular de P02. Plataforma proposta a partir da persona (trabalho no escritório, uso de e-mail e planilhas), a confirmar com a pergunta 3 da entrevista I02. | O agrônomo não precisa instalar nada. A interface segue padrões web conhecidos (lista, mapa, filtros, botões com rótulo) para reduzir o aprendizado. |
| Hardware/dispositivos | Fluxo do agrônomo (P03): computador ou notebook com tela de 13" ou mais; uso eventual em tablet ou celular durante visitas (hipótese). | A tela da detecção (A03) mostra foto ampliável, metadados e histórico do ponto lado a lado, atendendo à concorrência do CTT T07. Em telas menores, o histórico passa para baixo da foto, sem mudar de tela. |
| Capacidades | Fluxo do agrônomo (P03): tela grande para comparar fotos; mapa da propriedade com talhões e pontos geolocalizados; ampliação da foto original; filtros por período e local; registro do veredito por ponto; parecer com os pontos vinculados automaticamente. | Reduz a reconstrução do contexto relatada no C03 (fotos soltas, local de memória). Pelo GOMS T06, o atalho "ver histórico deste ponto" (M3) fica na própria tela da detecção. |
| Restrições | Fluxo do agrônomo (P03): a validação depende da qualidade da foto feita em campo; o agrônomo não examina o fruto pessoalmente; o sistema não recomenda produto nem dose. | A saída "pedir nova foto" (botão em A03) evita forçar confirmar ou rejeitar. Produto, dose e período são campos livres: o sistema apenas registra o julgamento do agrônomo (HTA T05, 4.2). |
| Conectividade/latência | Fluxo do agrônomo (P03): escritório com internet estável (hipótese); as fotos só chegam depois que o celular de P02 sincroniza, o que pode levar horas. | Mostrar a data e hora da captura e da sincronização, para o agrônomo saber se o dado é recente, e manter pendentes os pontos com pedido de nova foto ainda não atendido. |
| Segurança/privacidade | Fluxo do agrônomo (P03): fotos e coordenadas revelam a localização e a situação sanitária da propriedade; o parecer identifica o profissional responsável. | Acesso apenas às propriedades atendidas pelo agrônomo; autoria e data do veredito e do parecer sempre visíveis; mapas não expostos publicamente. |
| Volume de dados/histórico | Fluxo do agrônomo (P03): ciclos de cerca de 14 dias ao longo do ano [F16], várias propriedades por agrônomo e vários pontos por talhão; centenas de detecções por propriedade em um ano (estimativa a confirmar). | Histórico em lista única com filtros de período e local (A05), período padrão das últimas 8 semanas e ordenação da mais recente para a mais antiga. A mesma lista é aberta a partir de A01, A02 ou A03, já filtrada conforme a origem (GOMS T06). |
| Tempo de processamento | Fluxo do agrônomo (P03): a detecção já chega processada do celular; o que leva tempo é carregar o mapa e as fotos originais e enviar o parecer. | Indicador de carregamento no mapa e na foto; envio do parecer com o pedido marcado como "concluído" em A01 e, em caso de falha, nova tentativa em A07 sem perder o texto. |
| Papéis/permissões | Fluxo do agrônomo (P03): o agrônomo valida detecções e emite parecer; o gestor (P01) pede parecer e recebe a recomendação; o trabalhador (P02) recebe o pedido de nova foto na rota. | Apenas o agrônomo registra veredito. O sistema mostra quem pediu o parecer e para quem ele vai, para que o repasse seja explícito (síntese da Entrega 3). Não há tela de administração de usuários neste recorte. |

## 2. Princípios gerais do projeto

Inclua apenas normas, leis, padrões e princípios realmente relevantes, explicando **como** afetam o projeto. Não transforme esta seção em lista de links.

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Contexto de uso | Fluxo do agrônomo (P03): decide a distância, dependendo do que o campo registra, e atende várias propriedades (P03, C03). | Alertas agrupados por propriedade e talhão (A01); entrada direta no foco; local, data, hora e árvore gravados automaticamente na captura, sem depender da memória de quem fotografou. | Entregas 1/3 |
| LGPD, se aplicável | Fluxo do agrônomo (P03): o sistema guarda dados pessoais do agrônomo (autoria do parecer) e do trabalhador (quem fez a foto), além da localização da propriedade, que pode identificar o dono. | Coletar apenas o necessário para rastrear quem validou e quem fotografou; restringir o acesso às propriedades atendidas; no parecer, mostrar apenas nome e função. | Lei nº 13.709/2018 (LGPD), art. 6º (finalidade, necessidade, segurança) |
| Acessibilidade | Fluxo do agrônomo (P03): aplicação web em que a situação dos pontos no mapa seria difícil de distinguir só por cor (daltonismo, monitores ruins). | Situação dos pontos indicada por cor e símbolo (○ pendente, ● confirmado, × rejeitado, contorno tracejado = detecção anterior); contraste mínimo de 4,5:1 para texto; alvos de pelo menos 24 × 24 px; texto alternativo na foto com ponto, árvore e data. | WCAG 2.2: 1.4.1, 1.4.3, 2.5.8 e 1.1.1 |
| Responsabilidade técnica pela recomendação de defensivos | Fluxo do agrônomo (P03): a prescrição de agrotóxicos é feita por receituário agronômico emitido por profissional legalmente habilitado. | O parecer do sistema registra a recomendação, mas não substitui o receituário agronômico; isso fica explícito em A07, e o sistema não sugere produto nem dose. | Lei nº 14.785/2023 (substituiu a Lei nº 7.802/1989) |

## 3. Metas de usabilidade

Usabilidade deve ser discutida **no contexto de uso**. Metas quantitativas devem dizer o que será medido, em qual tarefa, com qual população e qual limite será considerado aceitável.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| Compreensão da diferença entre "detectado pela IA" e "validado por humano" | P03 / T07 (A02, A03) | O participante explica com as próprias palavras que um ponto confirmado passou pela sua análise e um pendente ainda não. | Principal decisão de design de P03 (Entrega 3) e base do dimensionamento da área. |
| Compreensão do que acontece após pedir nova foto | P03 / T07 (A02, A03) | Após pedir nova foto, o participante explica que o ponto continua pendente porque espera a nova foto do campo. | O ponto não tem situação própria de "aguardando"; é preciso verificar se isso não leva a pedir a mesma foto duas vezes. |
| Compreensão da situação do parecer após o envio | P03 / T05 (A07, A01) | O participante diz, a partir de "concluído" em A01, se o parecer já chegou ao gestor, e o que fazer em caso de falha. | Hoje o parecer se perde em mensagens soltas (C03). |
| Confiança no contexto reunido | P03 / T05 e T06 (A03, A05) | O participante declara ter informação suficiente para decidir ou, quando não tem, usa o pedido de nova foto em vez de decidir sem certeza. | Dor central do C03 (decidir sem local, data e histórico). |
| Percepção de que a avaliação da IA não atrapalha o julgamento | P03 / T07 (A03) | Relato do participante sobre quando abriu a avaliação da IA e se sentiu falta dela antes. | Decisão a testar, ligada ao possível viés de confirmação (CTT T07). |

### 3.2 Metas quantitativas

| ID | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | eficácia | taxa de conclusão sem ajuda | T01 | ≥ {{x}}% | teste observado | {{...}} |
| MU02 | eficiência | tempo mediano | T02 | ≤ {{tempo}} | cronômetro/log | {{...}} |
| MU03 | satisfação | escala pós-tarefa | T01–T03 | ≥ {{valor}} | questionário | {{...}} |
| MU04 | eficácia | conclusão sem ajuda do fluxo completo: abrir o pedido, validar os 5 pontos pendentes do talhão, delimitar a área e enviar o parecer | T07 + T05 (A01 → A07) | todos os participantes concluem; no máximo 1 precisa de 1 dica | teste observado, registrando pedidos de ajuda | Fluxo central de P03 e candidato ao teste (síntese da Entrega 5). Com 3 participantes finais (Entrega 14), a meta é expressa em número de pessoas, e não em porcentagem. |
| MU05 | eficácia (erro) | pontos não confirmados (pendentes, inclusive com pedido de nova foto, ou rejeitados) incluídos na área de aplicação | T05, passo 4.1 (A06) | 0 ocorrências | conferência da área delimitada ao fim da tarefa | O erro relatado no C03 (aplicar em área maior que a afetada) ocorre nessa etapa. |
| MU06 | eficiência | tempo para responder "este ponto já teve detecção antes?" a partir da tela da detecção | T06, método M3 (A03) | mediana ≤ 20 s | cronômetro, da exibição de A03 até a resposta verbal | O GOMS T06 indica M3 como o caminho mais curto; tempo alto indica histórico do ponto pouco visível. |
| MU07 | eficiência | tempo total do fluxo para um talhão com 5 pontos pendentes | T07 + T05 (A01 → A07) | mediana ≤ 8 min | cronômetro | Hoje reunir o contexto por telefone pode levar horas ou dias (C03); o fluxo deve caber em uma sessão curta de trabalho. |
| MU08 | eficácia (compreensão) | participantes que identificam corretamente a situação do parecer após o envio, inclusive na falha simulada | T05, passo 5.3 (A07, A01) | todos os participantes | pergunta pós-tarefa e observação | Parecer que não chega ao gestor não gera manejo (síntese da Entrega 3). |
| MU09 | satisfação | Single Ease Question (SEQ, 1 a 7) após cada tarefa | T05, T06 e T07 | média ≥ 5,5 em cada tarefa | questionário pós-tarefa | Escala curta, adequada a poucas tarefas e poucos participantes. |

### 3.3 Priorização das metas (se exigida na disciplina)

Se o professor solicitar porcentagens que somem 100%, trate-as como **peso de prioridade**, não como métrica de usabilidade.

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| MU01 | {{...}}% | {{...}} |
| **Total** | **100%** | |

## 4. Como o ciclo será iterado

Explique que artefatos serão revisitados após protótipos e avaliações.

## Checklist

- [ ] Capacidades e restrições têm impacto de IHC explicitado.
- [ ] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [ ] Resultados/processamento simulados no protótipo foram explicitados.
- [ ] Metas de usabilidade avaliam a interação, não substituem métricas técnicas do TCC.
- [ ] Normas/princípios estão contextualizados, não apenas copiados.
- [ ] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [ ] Eficácia, eficiência e satisfação são consideradas quando pertinentes.
- [ ] Metas poderão ser verificadas nas Entregas 12–14.
