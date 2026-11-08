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

> **Método de refinamento (revisado — aplicado ao cenário C03, de Guilherme; C01 e C02 permanecem na versão original de seus autores).** O cenário C03 tem questões que cobrem os **sete elementos característicos** (ambiente/contexto, atores, objetivos, planejamento, ações, eventos, avaliação), com o elemento indicado em cada questão. Na narrativa refinada, cada trecho que responde a uma questão traz a referência `[Qn]`. Como **ainda não houve coleta com pessoas reais**, as respostas são classificadas: **[Lit]** (literatura/TCC), **[F]** (fato registrado) ou **[H]** (hipótese **provisória**, escrita no condicional, nunca como acontecimento já ocorrido). Questões sem resposta permanecem `[Qn — em aberto]` e viram perguntas para a coleta da Entrega 7. Não foram inventados casos passados.

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

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Como Jaime recebe hoje o resultado de cada ciclo de inspeção (conversa, mensagem, relatório) e com que nível de detalhe? | Mostra o que se perde entre quem inspeciona e quem decide, relacionado a [F24] | Entrevista com o dono da propriedade |
| Q2 | Que decisões ele toma a partir desse resultado (onde aplicar, em que ordem, quando, quanto comprar de produto, quantas pessoas alocar)? | Define o que o gestor realmente precisa enxergar, em vez de supor o que ele "deveria" querer | Entrevista com o dono; relato de uma decisão recente |
| Q3 | Ele consegue comparar o ciclo atual com os anteriores? Como sabe se a praga está avançando e se a última aplicação funcionou? | Revela se a falta de histórico é uma dor real, relacionado a [H05] e [H09] | Entrevista; observação de como guarda ou perde as informações |
| Q4 | Quantos pragueiros atendem a propriedade e o que acontece quando um deles não está disponível? | Dimensiona a dependência descrita na persona e o peso da escassez de pragueiros | Entrevista com o dono e com o pragueiro |
| Q5 | Como ele sabe quais talhões foram de fato inspecionados em um ciclo? | Mostra se ele consegue diferenciar "sem praga" de "ninguém passou", ligado ao C02 | Entrevista com o dono e com o pragueiro |

### 3. Cenário refinado

Jaime é dono de uma fazenda de citros e cuida da parte administrativa e estratégica da propriedade. Ele conhece pouco a praga e depende do pragueiro para saber se há infestação e onde. **[NOVO: a propriedade conta com poucos pragueiros disponíveis, e a inspeção se repete em ciclos de cerca de 14 dias.]** A cada ciclo de inspeção, o pragueiro percorre os talhões e, ao final, avisa Jaime **[NOVO: pessoalmente ou por mensagem no celular, e quase sempre de memória]**, dizendo mais ou menos o que viu.

Jaime precisa decidir onde aplicar o produto de controle, em que ordem e com que urgência, e também quanto reservar de orçamento e mão de obra para isso. **[NOVO: essa decisão é tomada a cada ciclo, geralmente no escritório da propriedade, e ele só vai ao talhão quando fica inseguro.]** Mas o que chega até ele é uma impressão geral ("tem uns focos no fundo da fazenda"), sem um quadro do que está acontecendo em cada talhão. Ele não sabe se aquela área já teve problema em ciclos anteriores nem se a infestação está crescendo, estável ou diminuindo. **[NOVO: ele guarda o histórico apenas na memória e em conversas antigas, e por isso também não consegue dizer se a última aplicação surtiu efeito.]**

Como não sabe identificar a praga sozinho, Jaime não tem como conferir o que ouve. Se o pragueiro não pôde passar em alguma área, ou se passou rápido, ele não fica sabendo. **[NOVO: quando o pragueiro está indisponível, o ciclo atrasa ou é feito com menos cobertura, e o Jaime só percebe isso depois.]** No fim, planeja o manejo da propriedade com base em impressão, e não em dados. **[NOVO: ele não consegue priorizar os talhões com segurança nem justificar para si mesmo quanto precisa gastar naquele ciclo.]**

> **Nota de rastreabilidade:** o ponto de que quem inspeciona não é quem decide vem de [F24], que é fato. Os demais trechos **[NOVO]** são **hipóteses plausíveis**, construídas a partir da persona P01 e das hipóteses [H04], [H05], [H06], [H09] e [H21] da Entrega 1. Elas ainda **não foram validadas com um dono de fazenda real** e devem ser confirmadas ou corrigidas na investigação de campo da Entrega 7.

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

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Quantas árvores e quantos frutos Antônio inspeciona por dia, e quanto tempo gasta em cada planta? | O cenário fala em "muitas árvores" e "pouco tempo", mas sem números não dá para dimensionar o esforço nem o peso da fadiga descrita em [F19] | Entrevista/observação com pragueiro; protocolo de inspeção do Fundecitrus |
| Q2 | Como Antônio decide se um ponto escuro na casca é o ácaro ou outra coisa? O que ele faz quando fica em dúvida? | Mostra onde nasce o erro de julgamento, que o cenário só sugere | Entrevista com pragueiro; observação de uma rota de inspeção |
| Q3 | Como e com que informação ele avisa o dono de um achado (conversa, mensagem, foto)? | Define o que se perde entre quem encontra e quem decide, relacionado a [F24] | Entrevista com pragueiro e com o dono da propriedade |
| Q4 | Como ele controla quais árvores já foram inspecionadas? Existe algum registro do percurso? | Revela se a dúvida "deixei passar um pé?" tem causa concreta, ligada a [H08]/[H09] | Entrevista com pragueiro; observação |
| Q5 | O que acontece quando ele acha um foco, ou quando um foco passa despercebido e só aparece depois? | Mostra a consequência real da ruptura e quem arca com ela, relacionado a [F20]/[F25] | Relato de caso passado com pragueiro e dono |

### 3. Cenário refinado

Antônio é trabalhador de uma fazenda de citros e faz a inspeção de pragas nos pomares. No começo do dia, o dono da fazenda diz quais áreas ele deve percorrer. **[NOVO: a inspeção se repete ao longo do ano, em ciclos de cerca de 14 dias.]** Antônio sai a pé entre as fileiras, **[NOVO: caminhando pelo talhão em zigue-zague e, nas áreas que o dono indicou, escolhe de três a cinco frutos por árvore inspecionada]** e, com uma lupa de bolso **[NOVO: de aumento 10x, segura o fruto com uma mão e a lupa com a outra, examinando a superfície inteira e girando o fruto para não deixar nenhuma parte sem ver. Quando não há frutos no ponto adequado, ele olha os ramos mais internos, nos primeiros 30 cm a partir da ponta.]**

O ácaro é minúsculo, tem a cor parecida com a da casca e se esconde nas irregularidades do fruto. Antônio precisa aproximar bem a lupa, girar o fruto e repetir isso em muitas árvores, com o sol forte batendo e pouco tempo por planta. Com o passar das horas, a vista cansa e a atenção cai. **[NOVO: a luz muda ao longo do dia, entre sol direto e sombra das copas, e isso atrapalha a visão pela lupa.]** Às vezes ele vê um ponto escuro e não tem certeza se é o ácaro ou só uma marca da casca. **[NOVO: nessas horas ele costuma repetir o exame no mesmo fruto, chamar um colega mais experiente para olhar ou, se ainda tem dúvida, tirar uma foto com o celular para mostrar depois ao dono. A foto geralmente sai sem indicar de qual árvore ou talhão veio.]**

Quando acha algo suspeito, ele avisa o dono, **[NOVO: pessoalmente ou por mensagem no celular, dizendo mais ou menos onde estava, de memória,]** mas não é ele quem decide o que fazer. Ao final do dia, como não há registro de quais árvores foram vistas, ele fica com a dúvida se deixou algum pé passar, principalmente os últimos do percurso. **[NOVO: ele só tem a própria memória e o que combinou com o dono para saber onde passou. Se um foco passa despercebido e aparece depois, a falha tende a recair sobre quem inspecionou aquela área, o que aumenta o receio de errar.]**

> **Nota de rastreabilidade:** os trechos **[NOVO]** se apoiam em duas fontes. O protocolo de inspeção (lupa 10x, três a cinco frutos por planta, caminhamento em zigue-zague, ramos nos primeiros 30 cm, ciclo de cerca de 14 dias, variação de luz e fadiga ocular) vem da literatura já citada no TCC (Fundecitrus; Bassanezi, 2019) e é coerente com [F16], [F18] e [F19] da Entrega 1. Já o comportamento de Antônio nas dúvidas (repetir o exame, chamar colega, foto sem local, aviso de memória, cobrança por foco perdido) e a ausência de registro do percurso são **hipóteses plausíveis**, construídas a partir de [H08], [H09] e do mapa de empatia da Entrega 3 (itens marcados como hipótese). Elas ainda **não foram validadas com um pragueiro real** e devem ser confirmadas ou corrigidas na investigação de campo da Entrega 7.

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Antônio (trabalhador de campo/pragueiro, P02); dono/gestor da propriedade (P01), que orienta a rota e recebe os achados; colegas de campo, consultados nas dúvidas |
| Objetivo(s) | Verificar os frutos em busca de sinais da praga e avisar quem decide, sem deixar nenhum foco passar |
| Contexto | Pomar a céu aberto, sol forte, deslocamento a pé entre árvores, pouco tempo por planta, rotina repetida ao longo do ano, comunicação com o dono por conversa ou mensagem |
| Recursos/informações | Lupa de bolso 10x, orientação do dono sobre a rota, memória do percurso, celular usado para fotos e mensagens |
| Ações | Percorrer o talhão; escolher frutos; examinar a casca com a lupa; repetir o exame ou chamar colega em caso de dúvida; fotografar; avisar o dono |
| Problemas/rupturas | Ácaro pequeno e camuflado; fadiga visual; luz variável; dúvida entre ácaro e marca da casca; foto e aviso sem localização precisa; nenhum registro de onde já passou |
| Consequências | Foco que passa despercebido no fim do percurso; informação imprecisa chegando a quem decide; receio de ser responsabilizado; inspeção menos confiável do que o protocolo prevê |

### 5. Implicações para as próximas entregas

- Vale analisar, na modelagem de tarefas, a tarefa "decidir se o que vejo é praga" separada de "percorrer a rota" e de "avisar o dono". Cada uma tem rupturas diferentes.
- É preciso levantar com um pragueiro real quantos frutos e árvores ele inspeciona por dia, quanto tempo gasta por planta, como decide nas dúvidas e quanto a variação de luz atrapalha, sem ainda desenhar telas.
- É preciso investigar como o achado chega hoje ao dono (canal, informação enviada, atraso). Isso se conecta ao C03: as "fotos soltas sem contexto" que o Marcelo recebe nascem justamente dessa etapa.
- Vale checar se a falta de registro do percurso ([H09]) é uma dor real para o pragueiro ou só uma hipótese da equipe, e se o receio de ser responsabilizado aparece de fato nos relatos.
- As hipóteses H08 e H09 ficam diretamente reforçadas por este cenário e devem ser priorizadas na investigação de campo da Entrega 7.

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

> **Nota de rastreabilidade (revisada):** os casos concretos de "recomendação que levou à aplicação em área maior" e de "demora que permitiu que o foco se espalhasse", que constavam na versão anterior como ocorrências passadas, foram **removidos**: não houve relato real que os sustentasse. O cenário agora mantém essas possibilidades apenas como **perguntas em aberto** (Q5). Todo o cenário depende de P03 ser proto-persona e de H04, H07 e H21, ainda sem validação com agrônomo real; deve ser confirmado ou corrigido na Entrega 7.

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
- [x] Cada cenário tem ao menos uma questão por elemento característico (ambiente, atores, objetivos, planejamento, ações, eventos, avaliação), com o elemento indicado.
- [x] A narrativa refinada referencia `[Qn]` nos trechos correspondentes e não apresenta hipóteses como acontecimentos já ocorridos.
- [x] Questões de refinamento acrescentam informação nova.
- [x] O refinamento mostra claramente o que foi adicionado/alterado.
- [x] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [x] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade (`RASTREABILIDADE.md`, seção 6, atualizada nesta revisão).
