# Entrega 4 — Cenários de análise/problema

**Data:** 07/10/2026  
**Status:** 🟩 concluído
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Descrever situações atuais em que o usuário tenta alcançar um objetivo e encontra dificuldades. O cenário de análise/problema deve tornar visível **o contexto, os atores, as ações e as rupturas**, sem antecipar a interface que será projetada.

> **Regra central:** cenário de problema é a “história do problema”. Se o texto já diz “o sistema mostra”, “o aplicativo resolve” ou descreve botões/telas futuras, provavelmente está misturando problema com solução.

Sempre que possível, o cenário deve aprofundar uma **situação concreta já registrada na Entrega 1**.

### Quando o TCC não possuía interface

O cenário continua sendo uma história de **problema/atividade humana**, não uma história do futuro sistema. Descreva como o profissional realiza hoje uma atividade semelhante ou como lida atualmente com dados, resultados, configurações, logs, decisões e limitações que o tema do TCC pretende apoiar.

Exemplo: em vez de “o DBA abre o novo dashboard e executa o algoritmo”, descreva “o DBA precisa investigar uma consulta lenta, reúne informações em ferramentas distintas, compara planos manualmente e tem dificuldade para estimar o impacto de uma mudança”.

A interface da disciplina aparecerá somente depois, nos cenários de interação.

Se o integrante escolher um novo problema/situação, explique por que ele passou a ser relevante e indique a evidência que motivou sua inclusão.

> **Método de refinamento.** C01, C02 e C03 explicitam os sete elementos característicos (ambiente/contexto, atores, objetivos, planejamento, ações, eventos e avaliação) e vinculam as questões à narrativa refinada por `[Qn]`. Sem coleta com pessoas reais, fatos do TCC e literatura são distintos de hipóteses; questões sem resposta viram perguntas para a Entrega 7. Nenhum episódio passado é apresentado como observado sem registro.

## Cenário C01 — Planejamento do manejo sem visão consolidada da propriedade ao longo dos ciclos

**Autor(a):** Pedro Henrique Ferreira Valim - 24.123.048-1  
**Persona(s) relacionada(s):** P01 (Jaime Carteiro, dono da fazenda)  
**Necessidade relacionada:** Acesso a dados confiáveis sobre os focos de infestação para orientar as ações de manejo (necessidade registrada na Entrega 3, persona P01)  
**Situação concreta da Entrega 1 relacionada:** seção 3.4 (H06: decidir onde aplicar o produto de controle é a atividade mais crítica), com apoio das seções 3.2 (A02 e A03: decidir onde e quando aplicar; acompanhar se o problema se espalha), 5.4 (F24: quem inspeciona não é quem decide) e 9.1 (H19: hoje não há registro visual organizado dos focos)  
**Hipóteses ainda presentes:** H04, H05, H06, H09, H21

### 1. Cenário inicial

Jaime é dono de uma fazenda de citros e cuida da parte administrativa e estratégica da propriedade. Ele conhece pouco a praga e depende do pragueiro para saber se há infestação e onde. A cada ciclo de inspeção, o pragueiro percorre os talhões e, ao final, avisa Jaime de forma verbal ou por mensagem, dizendo mais ou menos o que viu.

Jaime precisa decidir onde aplicar o produto de controle, em que ordem e com que urgência, e também quanto reservar de orçamento e mão de obra para isso. Mas o que chega até ele é uma impressão geral ("tem uns focos no fundo da fazenda"), sem um quadro do que está acontecendo em cada talhão. Ele não sabe se aquela área já teve problema em ciclos anteriores nem se a infestação está crescendo, estável ou diminuindo.

Como não sabe identificar a praga sozinho, Jaime não tem como conferir o que ouve. Se o pragueiro não pôde passar em alguma área, ou se passou rápido, ele não fica sabendo. No fim, planeja o manejo da propriedade com base em impressão, e não em dados.

### 2. Questões de refinamento

| # | Elemento | Questão em aberto | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Ambiente/contexto | Onde e sob que condições o responsável examina os resultados do ciclo? | Entrevista e observação do trabalho. |
| Q2 | Atores | Quem inspeciona, quem recebe os achados, quem recomenda e quem decide o manejo? | Entrevistas com responsável e inspetor. |
| Q3 | Objetivos | Qual decisão concreta precisa tomar ao receber o resultado? | Relato de decisão recente. |
| Q4 | Planejamento | Como escolhe quais talhões examinar primeiro e que informações busca antes de decidir? | Entrevista com exemplo concreto. |
| Q5 | Ações | Como recebe, registra e consulta hoje informações de inspeções anteriores? | Observação dos registros e entrevista. |
| Q6 | Eventos | O que muda seu plano quando uma área não é inspecionada ou surge um achado duvidoso? | Relato de caso e entrevista. |
| Q7 | Avaliação | Como verifica que a informação foi suficiente e que a decisão funcionou? | Entrevista e análise dos critérios usados no ciclo seguinte. |

### 3. Cenário refinado

Jaime representa o responsável pelo manejo de uma propriedade citrícola **[Q2 — hipótese de papel, não entrevista]**. Se as inspeções forem repassadas a ele, precisará decidir onde e quando agir **[Q3 — decisão e autoridade a confirmar]**. Ainda não sabemos se examina os resultados no escritório ou no campo, nem sob qual pressão de tempo **[Q1 — em aberto]**.

Ele pode receber o achado por conversa, mensagem ou registro, mas o canal, a qualidade da informação e a consulta a ciclos anteriores ainda precisam ser observados **[Q5 — em aberto]**. Se faltar cobertura de um talhão ou houver dúvida sobre um foco, pode precisar alterar a prioridade ou pedir nova inspeção **[Q4 e Q6 — hipóteses, não episódios registrados]**. Para planejar o manejo com confiança, precisa avaliar o que foi inspecionado e se a informação basta; como mede depois o resultado da decisão continua desconhecido **[Q7 — em aberto]**.

> **Nota de evidência:** o TCC sustenta que existe inspeção recorrente, mas não demonstra a rotina decisória particular de Jaime. Este cenário é uma hipótese de trabalho a investigar na Entrega 7; não há caso passado de Jaime registrado.

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Jaime (dono/gestor, P01); pragueiro (P02), fonte da informação; agrônomo consultor (P03), eventualmente consultado |
| Objetivo(s) | Planejar onde, em que ordem e com que orçamento aplicar o manejo, com base em dados confiáveis |
| Contexto | Escritório da propriedade, com visitas eventuais ao talhão; decisão a cada ciclo de cerca de 14 dias; informação chegando por terceiros |
| Recursos/informações | Relato verbal ou mensagem do pragueiro, memória de quem esteve em campo, conversas antigas |
| Ações | Receber o aviso do ciclo; decidir onde e quando aplicar; reservar orçamento e mão de obra; ir ao talhão quando fica inseguro |
| Problemas/rupturas | Ausência de visão por talhão e de histórico entre ciclos; impossibilidade de conferir o que ouve; dependência de poucos pragueiros; não saber o que foi inspecionado |
| Consequências | Priorização e orçamento baseados em impressão; não saber se a aplicação anterior funcionou; ciclos com cobertura reduzida sem que ele perceba |

### 5. Implicações para as próximas entregas

- Vale analisar, na modelagem de tarefas, "entender a situação geral da propriedade" como tarefa própria de P01, separada de "capturar a praga" (P02) e de "emitir parecer" (P03). Cada uma tem rupturas diferentes.
- É preciso levantar com um dono real quais decisões ele toma a partir da informação (onde aplicar, em que ordem, quando, orçamento) e que tipo de visão o ajudaria em cada uma, sem ainda desenhar telas.
- Vale checar se a comparação entre ciclos é uma necessidade real ou só uma hipótese da equipe, e qual intervalo de tempo faz sentido acompanhar.
- Convém investigar o que dá confiança ao Jaime num alerta, já que ele não sabe validar a praga sozinho. Isso conecta com o C02: ele precisa saber se "sem alerta" significa "inspecionado e limpo" ou "ninguém passou".
- Fica em aberto onde está a fronteira entre mostrar o dado e recomendar uma ação, já que isso pode invadir o papel do agrônomo (P03), tratado no C03.
- As hipóteses H04, H05, H06, H09 e H21 ficam diretamente reforçadas por este cenário e devem ser priorizadas na investigação de campo da Entrega 7.
---

## Cenário C02 — Inspeção manual de frutos com lupa, sob fadiga e sem registro do percurso

**Autor(a):** Lucas Tonoli Cabral Duarte - 24.123.032-5  
**Persona(s) relacionada(s):** P02 (Antônio Ferreira, trabalhador de campo / pragueiro)  
**Necessidade relacionada:** Confirmação clara e imediata se há ou não sinal de praga, sem depender de lupa ou de um especialista externo (necessidade registrada na Entrega 3, persona P02)  
**Situação concreta da Entrega 1 relacionada:** seção 4.5 (H08 — trabalhador cansado que passa rápido pelos últimos pés e deixa um foco passar), com apoio das seções 4.1 e 4.2 (F18, F19 — inspeção a pé, com lupa, cansativa e sem cobertura total)  
**Hipóteses ainda presentes:** H08, H09

### 1. Cenário inicial

Antônio é trabalhador de uma fazenda de citros e faz a inspeção de pragas nos pomares. No começo do dia, o dono da fazenda diz quais áreas ele deve percorrer. Antônio sai a pé entre as fileiras, escolhe alguns frutos em cada árvore e, com uma lupa de bolso, examina a casca de cada um à procura do ácaro.

O ácaro é minúsculo, tem a cor parecida com a da casca e se esconde nas irregularidades do fruto. Antônio precisa aproximar bem a lupa, girar o fruto e repetir isso em muitas árvores, com o sol forte batendo e pouco tempo por planta. Com o passar das horas, a vista cansa e a atenção cai. Às vezes ele vê um ponto escuro e não tem certeza se é o ácaro ou só uma marca da casca.

Quando acha algo suspeito, ele avisa o dono, mas não é ele quem decide o que fazer. Ao final do dia, como não há registro de quais árvores foram vistas, ele fica com a dúvida se deixou algum pé passar, principalmente os últimos do percurso.

### 2. Questões de refinamento

| # | Elemento | Questão ainda não respondida pelo cenário inicial | Fonte e situação |
|---|---|---|---|
| Q1 | Ambiente/contexto | Como variações de luz e deslocamento afetam a inspeção concreta em cada horário? | Observação de campo; aberta. |
| Q2 | Atores | Quem define a área, quem ajuda na dúvida e quem recebe o achado na prática? | Entrevista com inspetor e responsável; aberta. |
| Q3 | Objetivos | É suficiente localizar um sinal no fruto ou também demonstrar a cobertura da área? | Entrevista com inspetor; aberta. |
| Q4 | Planejamento | Como escolhe frutos e árvores sob restrição de tempo e decide o que fazer diante de um ponto suspeito? | Protocolo + observação; parcialmente aberta. |
| Q5 | Ações | Que passos executa no exame e como registra ou relata o achado? | Observação/entrevista; exame apoiado na literatura, relato aberto. |
| Q6 | Eventos | Que acontecimento interrompe ou altera seu plano, como sombra, chuva ou sinal suspeito? | Observação/relato de caso; aberta. |
| Q7 | Avaliação | Como sabe que examinou suficientemente os frutos, cobriu a área e comunicou o achado com clareza? | Entrevista/observação; aberta. |

### 3. Cenário refinado

Antônio representa um inspetor de citros **hipotético**, não uma pessoa entrevistada. No começo do trabalho, recebe uma área para examinar **[Q2: divisão de papéis a confirmar]**. Examina frutos com lupa, conforme o procedimento de inspeção da literatura, que descreve ampliação 10x, amostragem de frutos e caminhamento no talhão **[Q4, Q5: protocolo, não observação de Antônio]**. O sol, a sombra e a repetição do exame podem dificultar a observação **[Q1, Q6: restrições gerais cujo efeito real deve ser observado]**.

Ao perceber um ponto suspeito, precisa decidir se examina novamente ou busca outro tipo de apoio **[Q4, Q5: modo de decisão ainda aberto]**. Ainda não sabemos se ele também precisa comprovar cobertura, além de procurar sinais **[Q3]**, nem como registra ou comunica o achado, quem o recebe e que informação o destinatário utiliza **[Q2, Q5]**. No fim do trabalho, é necessário investigar como avalia se examinou o suficiente, cobriu a área solicitada e conseguiu comunicar a suspeita **[Q7]**. Uma mudança na iluminação ou novo achado pode modificar seu plano **[Q6: verificar em campo]**.

> **Estado do refinamento:** os trechos `[Qn]` rastreiam perguntas, mas as questões abertas não foram preenchidas com episódios inventados. Literatura sobre o procedimento não comprova como um inspetor específico pensa ou se comunica. Os pontos abertos devem orientar a Entrega 7.

### 4. Elementos extraídos

| Elemento formal | Evidência e lacuna |
|---|---|
| Ambiente/contexto | Pomar, deslocamento e luz variável; impacto concreto por horário ainda aberto [Q1]. |
| Atores | Inspetor e possível responsável pela área; divisão real de papéis e colega ainda não confirmados [Q2]. |
| Objetivos | Procurar sinais; necessidade de comprovar cobertura ainda aberta [Q3]. |
| Planejamento | Protocolo de amostragem conhecido; escolha real e decisão diante da dúvida não observadas [Q4]. |
| Ações | Exame com lupa documentado; registro e comunicação específicos não confirmados [Q5]. |
| Eventos | Mudança de luz ou achado suspeito podem alterar a tarefa; confirmar em campo [Q6]. |
| Avaliação | Critérios de suficiência do exame, cobertura e comunicação ainda não conhecidos [Q7]. |

### 5. Implicações para as próximas entregas

- Vale analisar, na modelagem de tarefas, a tarefa "decidir se o que vejo é praga" separada de "percorrer a rota" e de "avisar o dono". Cada uma tem rupturas diferentes.
- É preciso levantar com um pragueiro real quantos frutos e árvores ele inspeciona por dia, quanto tempo gasta por planta, como decide nas dúvidas e quanto a variação de luz atrapalha, sem ainda desenhar telas.
- É preciso investigar como o achado chega hoje ao dono (canal, informação enviada, atraso). Isso se conecta ao C03: as "fotos soltas sem contexto" que o Marcelo recebe nascem justamente dessa etapa.
- Vale checar se a falta de registro do percurso ([H09]) é uma dor real para o pragueiro ou só uma hipótese da equipe, e se o receio de ser responsabilizado aparece de fato nos relatos.
- As hipóteses H08 e H09 continuam em aberto neste cenário e devem ser priorizadas na investigação de campo da Entrega 7.

---

## Cenário C03 — Parecer técnico remoto sem contexto suficiente sobre o foco de infestação

**Autor(a):** Guilherme Morais Escudeiro - 24.123.005-1  
**Persona(s) relacionada(s):** P03 (Marcelo Fidalgo, agrônomo consultor da propriedade)  
**Necessidade relacionada:** Acesso a dados históricos e geolocalizados das inspeções, com detalhe técnico suficiente para embasar um parecer (necessidade registrada na Entrega 3, persona P03)  
**Situação concreta da Entrega 1 relacionada:** seção 4.3 (H07 — informações que o profissional precisa interpretar para decidir) e seção 2.2 (F08 — participação do agrônomo na definição do período de coleta do TCC, que não prova papel operacional)  
**Hipóteses ainda presentes:** H04, H07, H21

### 1. Cenário inicial

Marcelo é o agrônomo consultor de uma propriedade de citros, mas não está presente na fazenda no dia a dia, prestando atendimento também a outras propriedades. Certa manhã, o dono da fazenda liga para ele preocupado, dizendo que um dos trabalhadores encontrou "alguns frutos estranhos" durante a inspeção da plantação. Pouco depois, Marcelo recebe pelo celular algumas fotos soltas enviadas por mensagem, tiradas por diferentes trabalhadores em momentos diferentes do dia.

Nenhuma das fotos vem acompanhada de informação clara sobre em qual talhão foi tirada, a que distância das outras, ou se os frutos fotografados pertencem à mesma árvore ou a árvores distintas. Marcelo tenta reconstruir o cenário por telefone, perguntando ao dono onde exatamente cada trabalhador estava, mas as respostas são baseadas na memória de quem estava em campo horas antes, e nem sempre são precisas. Ele também não tem como comparar essas fotos com inspeções de semanas anteriores, porque não existe um registro histórico organizado, apenas mensagens soltas que se perdem na conversa.

Sem saber com certeza a extensão da área afetada, nem se o problema já havia aparecido antes naquele ponto da propriedade, Marcelo precisa decidir se recomenda a aplicação de um produto de controle, e onde. Ele sabe que recomendar a aplicação em uma área maior do que o necessário gera custo e impacto ambiental evitáveis, mas que recomendar pouco, ou no lugar errado, corre o risco de deixar a praga se espalhar sem controle.

### 2. Questões de refinamento

| # | Elemento | Questão (lacuna do cenário inicial) | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|---|
| Q1 | Eventos | Com que frequência Marcelo recebe relatos informais de campo (fotos soltas, ligações) e o que dispara cada pedido de parecer? | Define se essa é uma situação pontual ou recorrente, o que muda a prioridade do problema para o projeto | Entrevista com Marcelo (ou perfil equivalente de agrônomo consultor) |
| Q2 | Avaliação | Que informações Marcelo considera indispensáveis para julgar que tem contexto suficiente para um parecer confiável (localização, data, quantidade de frutos afetados, estágio)? | Revela exatamente qual informação falta hoje, sem supor o que "deveria" existir | Entrevista/roteiro técnico com o agrônomo |
| Q3 | Ações | Como Marcelo tenta suprir hoje a falta dessas informações (ligações repetidas, pedir novas fotos, visita presencial extra)? | Mostra o esforço e o atraso reais gerados pelo processo atual | Entrevista com Marcelo e com o dono da propriedade |
| Q4 | Ambiente/contexto | Em que condições Marcelo trabalha nesses momentos (deslocamento, canal usado, prazo, número de propriedades atendidas) e quanto tempo costuma passar entre a detecção em campo e o parecer? | Quantifica o atraso ligado a [H07]/[F20] e as pressões do ambiente remoto | Relato de caso passado, mesmo que informal (mensagens, agenda) |
| Q5 | Avaliação | Como ele percebe, depois, que uma recomendação foi adequada ou não (área maior ou menor que a necessária) e isso já aconteceu? | Evidencia a consequência concreta da ruptura; **a pergunta é se isso já aconteceu — não se supõe que sim** | Relato de caso passado com o dono/agrônomo |
| Q6 | Atores | Quem participa do parecer além de Marcelo (dono, gerente, outro agrônomo) e quem decide a execução? O papel de agrônomo consultor remoto existe nesta propriedade? | P03 é proto-persona; falta confirmar o papel (H04) | Entrevista com o dono e com o agrônomo |
| Q7 | Objetivos | O que Marcelo precisa entregar ao final (recomendação de produto, dose, área, período) e a quem? | O objetivo "parecer confiável" é amplo; falta o resultado concreto | Entrevista com o agrônomo |
| Q8 | Planejamento | Como Marcelo decide quando a informação recebida é suficiente e quando precisa pedir nova evidência ou visitar a propriedade? | Planejamento é a atividade mental de transformar o objetivo em ações; o cenário não a explora | Entrevista; relato de um caso em voz alta |

### 3. Cenário refinado

Marcelo é o agrônomo consultor de uma propriedade de citros. **[Q4 e Q6 — hipótese provisória (H): supomos que ele atenda também a outras propriedades; não sabemos se esse papel de consultor remoto existe nesta propriedade nem com que frequência isso ocorre (Q1).]** Certa manhã, o dono da fazenda liga para ele preocupado, dizendo que um dos trabalhadores encontrou "alguns frutos estranhos" durante a inspeção da plantação **[Q1 — em aberto: o que normalmente dispara esse contato]**. Pouco depois, Marcelo recebe pelo celular algumas fotos soltas enviadas por mensagem, tiradas por diferentes trabalhadores em momentos diferentes do dia.

**[Q2 — hipótese provisória (H07): para julgar que tem contexto suficiente, Marcelo poderia precisar saber onde cada foto foi tirada, quando, e se os frutos pertencem à mesma árvore ou a árvores distintas; quais informações ele de fato exige não foi levantado.]** Nenhuma dessas informações acompanha as fotos descritas no cenário. Ele tenta reconstruir o cenário por telefone, perguntando ao dono onde exatamente cada trabalhador estava, mas as respostas são baseadas na memória de quem estava em campo horas antes, e nem sempre são precisas. **[Q3 e Q8 — em aberto: não sabemos como ele supre a falta de informação nem como decide que é preciso mais evidência. Poderia pedir novas fotos ou visitar a propriedade; isso é hipótese.]** Ele também não tem como comparar essas fotos com inspeções de semanas anteriores, porque não existe um registro histórico organizado, apenas mensagens soltas que se perdem na conversa.

Sem saber com certeza a extensão da área afetada, nem se o problema já havia aparecido antes naquele ponto da propriedade, Marcelo precisa decidir se recomenda a aplicação de um produto de controle, e onde **[Q7 — em aberto: o que ele precisa entregar (produto, dose, área, período) e a quem]**. Ele sabe que recomendar a aplicação em uma área maior do que o necessário gera custo e impacto ambiental evitáveis, mas que recomendar pouco, ou no lugar errado, corre o risco de deixar a praga se espalhar sem controle **[Q5 — em aberto: não sabemos se recomendações equivocadas ou atrasadas já aconteceram com ele; a pergunta é investigar "isso já aconteceu?". Nenhum caso passado foi registrado.]**

> **Nota de rastreabilidade:** os casos concretos de "recomendação que levou à aplicação em área maior" e de "demora que permitiu que o foco se espalhasse", que constavam na versão anterior como ocorrências passadas, foram **removidos**: não houve relato real que os sustentasse. O cenário agora mantém essas possibilidades apenas como **perguntas em aberto** (Q5). Todo o cenário depende de P03 ser proto-persona e de H04, H07 e H21, ainda sem validação com agrônomo real; deve ser confirmado ou corrigido na Entrega 7.

### 4. Elementos extraídos

| Elemento | Evidência no cenário | Questão |
|---|---|---|
| Ambiente/contexto | Atendimento remoto, fora da propriedade, dependente de informação repassada por terceiros; condições e prazos em aberto | Q4 |
| Atores | Marcelo (P03, proto-persona), dono/gestor (P01), trabalhadores de campo (P02, fonte indireta das fotos); papéis a confirmar | Q6 |
| Objetivos | Emitir um parecer técnico confiável e recomendar a ação de manejo; resultado concreto em aberto | Q7 |
| Planejamento | Como decide se a informação é suficiente ou se pede nova evidência (em aberto) | Q8 |
| Ações | Receber fotos e relato informal; ligar para esclarecer; possivelmente pedir novas fotos ou visitar (hipótese) | Q3 |
| Eventos | Ligação do dono; recebimento de fotos soltas; frequência e gatilhos em aberto | Q1 |
| Avaliação | Como julga que tem contexto suficiente e se a recomendação foi adequada (em aberto) | Q2, Q5 |
| *(Complementar)* Problemas/rupturas | Ausência de localização, data e contexto junto às fotos; impossibilidade de comparar com inspeções anteriores; dependência da memória alheia | — |
| *(Complementar)* Consequências | Risco de recomendação de área maior ou menor que a necessária; risco de atraso na decisão (possibilidades, não casos registrados) | — |

### 5. Implicações para as próximas entregas

- Vale investigar, na modelagem de tarefas (Entrega 5), a tarefa "reunir contexto suficiente para emitir parecer" como uma tarefa própria de P03, distinta da tarefa de captura de P02.
- É preciso levantar, com um agrônomo real, quais metadados mínimos (local, data, sequência de fotos por árvore/talhão) tornariam um relato de campo suficiente para decisão remota, sem ainda desenhar telas.
- As hipóteses H04 (quem decide no dia a dia), H07 (que informação o profissional precisa) e H21 (quem acompanha a evolução do problema) são **investigadas** por este cenário e devem ser priorizadas na Entrega 7. C03 só deve alimentar tarefas do agrônomo depois de confirmado que esse papel e fluxo existem como descritos.
- Vale checar, na coleta, se existe atraso entre detecção e parecer e de quanto, sem pressupor; é consistente com a criticidade já apontada em [H06]/[F20] da Entrega 1, para dimensionar o impacto real do problema.

---

> Repita a estrutura acima para novos cenários, se necessário, com autoria individual.

## Checklist

- [x] Há um cenário completo por integrante.
- [x] Cada cenário tem título, ator, objetivo, contexto e problema.
- [x] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [x] O texto descreve a situação atual, sem antecipar a solução.
- [x] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela” (o TCC prevê interface; os cenários descrevem o problema atual).
- [x] Cada cenário tem ao menos uma questão por elemento característico.
- [x] A narrativa refinada referencia `[Qn]` e identifica hipóteses sem apresentá-las como observações.
- [x] Questões de refinamento acrescentam informação nova.
- [x] O refinamento mostra claramente o que foi adicionado/alterado.
- [x] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [x] Vínculos P01/C01, P02/C02 e P03/C03 registrados em `RASTREABILIDADE.md`.
