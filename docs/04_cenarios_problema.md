# Entrega 4 — Cenários de análise/problema

**Data:** 23/09/2026  
**Status:** 🟨 em andamento  
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
**Situação concreta da Entrega 1 relacionada:** seção 4.3 (H07 — informações que o profissional precisa interpretar para decidir) e seção 2.2 (F08 — participação do agrônomo na definição do período de coleta)  
**Hipóteses ainda presentes:** H04, H07, H21

### 1. Cenário inicial

Marcelo é o agrônomo consultor de uma propriedade de citros, mas não está presente na fazenda no dia a dia, prestando atendimento também a outras propriedades. Certa manhã, o dono da fazenda liga para ele preocupado, dizendo que um dos trabalhadores encontrou "alguns frutos estranhos" durante a inspeção da plantação. Pouco depois, Marcelo recebe pelo celular algumas fotos soltas enviadas por mensagem, tiradas por diferentes trabalhadores em momentos diferentes do dia.

Nenhuma das fotos vem acompanhada de informação clara sobre em qual talhão foi tirada, a que distância das outras, ou se os frutos fotografados pertencem à mesma árvore ou a árvores distintas. Marcelo tenta reconstruir o cenário por telefone, perguntando ao dono onde exatamente cada trabalhador estava, mas as respostas são baseadas na memória de quem estava em campo horas antes, e nem sempre são precisas. Ele também não tem como comparar essas fotos com inspeções de semanas anteriores, porque não existe um registro histórico organizado, apenas mensagens soltas que se perdem na conversa.

Sem saber com certeza a extensão da área afetada, nem se o problema já havia aparecido antes naquele ponto da propriedade, Marcelo precisa decidir se recomenda a aplicação de um produto de controle, e onde. Ele sabe que recomendar a aplicação em uma área maior do que o necessário gera custo e impacto ambiental evitáveis, mas que recomendar pouco, ou no lugar errado, corre o risco de deixar a praga se espalhar sem controle.

### 2. Questões de refinamento

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Com que frequência Marcelo recebe relatos informais de campo (fotos soltas, ligações) para emitir um parecer? | Define se essa é uma situação pontual ou recorrente, o que muda a prioridade do problema para o projeto | Entrevista com Marcelo (ou perfil equivalente de agrônomo consultor) |
| Q2 | Quais informações mínimas Marcelo considera indispensáveis para um parecer confiável (ex.: localização exata, data, quantidade de frutos afetados, estágio da infestação)? | Revela exatamente qual informação falta hoje, sem supor o que "deveria" existir | Entrevista/roteiro técnico com o agrônomo |
| Q3 | Como Marcelo tenta suprir hoje a falta dessas informações (ligações repetidas, pedir novas fotos, visita presencial extra)? | Mostra o esforço e o atraso reais gerados pelo processo atual, sem os quais o cenário fica genérico | Entrevista com Marcelo e com o dono da propriedade |
| Q4 | Quanto tempo, em média, passa entre a detecção do foco em campo e o parecer técnico de Marcelo? | Quantifica o atraso ligado a [H07]/[F20] (a praga continua se espalhando enquanto não há decisão) | Relato de caso passado, mesmo que informal (WhatsApp, agenda) |
| Q5 | O que acontece quando Marcelo decide com informação incompleta e a recomendação se mostra equivocada depois (área maior/menor do que a necessária)? | Evidencia a consequência concreta da ruptura, reforçando por que o cenário é crítico e não apenas incômodo | Relato de caso passado com o dono/agrônomo |

### 3. Cenário refinado

Marcelo é o agrônomo consultor de uma propriedade de citros. **[NOVO: ele atende a mais de uma propriedade e costuma revisar relatos de campo dessa forma pelo menos algumas vezes por mês, geralmente quando o dono percebe algo fora do padrão durante a rotina da fazenda.]** Certa manhã, o dono da fazenda liga para ele preocupado, dizendo que um dos trabalhadores encontrou "alguns frutos estranhos" durante a inspeção da plantação. Pouco depois, Marcelo recebe pelo celular algumas fotos soltas enviadas por mensagem, tiradas por diferentes trabalhadores em momentos diferentes do dia.

**[NOVO: para emitir um parecer em que confia, Marcelo precisaria minimamente saber onde cada foto foi tirada dentro da propriedade, em que data e horário, e se os frutos fotografados pertencem à mesma árvore ou a árvores distintas (nenhuma dessas informações acompanha as fotos que recebe.)]** Ele tenta reconstruir o cenário por telefone, perguntando ao dono onde exatamente cada trabalhador estava, mas as respostas são baseadas na memória de quem estava em campo horas antes, e nem sempre são precisas. **[NOVO: quando a resposta não é suficiente, ele chega a pedir que um trabalhador volte ao local para tirar novas fotos, ou, em casos mais sérios, agenda uma visita presencial extra à propriedade, o que pode levar mais de um dia para acontecer.]** Ele também não tem como comparar essas fotos com inspeções de semanas anteriores, porque não existe um registro histórico organizado, apenas mensagens soltas que se perdem na conversa.

Sem saber com certeza a extensão da área afetada, nem se o problema já havia aparecido antes naquele ponto da propriedade, Marcelo precisa decidir se recomenda a aplicação de um produto de controle, e onde. **[NOVO: em uma ocasião anterior relatada pelo dono, uma recomendação baseada em informação incompleta levou à aplicação do produto em uma área maior do que a realmente afetada, gerando gasto desnecessário; em outra, a demora para reunir informação suficiente atrasou a decisão em alguns dias, tempo em que o foco identificado se espalhou para árvores vizinhas.]** Ele sabe que recomendar a aplicação em uma área maior do que o necessário gera custo e impacto ambiental evitáveis, mas que recomendar pouco, ou no lugar errado, corre o risco de deixar a praga se espalhar sem controle.

> **Nota de rastreabilidade:** as respostas incorporadas acima (Q1–Q5) são **hipóteses plausíveis**, construídas a partir das dores já registradas para P03 na Entrega 3 e das hipóteses [H04], [H07] e [H21] da Entrega 1. Elas ainda **não foram validadas com um agrônomo real** e devem ser confirmadas ou corrigidas na investigação de campo da Entrega 7.

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Marcelo (agrônomo consultor, P03), dono/gestor da propriedade (P01), trabalhadores de campo (P02, fonte indireta das fotos) |
| Objetivo(s) | Emitir um parecer técnico confiável sobre o foco de infestação e recomendar a ação de manejo adequada |
| Contexto | Atendimento remoto, fora da propriedade, dependente de informação repassada por terceiros |
| Recursos/informações | Fotos soltas enviadas por mensagem, relatos verbais do dono por telefone, memória dos trabalhadores sobre onde estiveram |
| Ações | Receber fotos e relato informal; ligar para esclarecer detalhes; pedir novas fotos ou agendar visita presencial quando a informação não é suficiente |
| Problemas/rupturas | Ausência de localização, data e contexto junto às fotos; impossibilidade de comparar com inspeções anteriores; dependência da memória alheia |
| Consequências | Recomendação de área de aplicação maior ou menor do que a necessária; atraso de dias na decisão, tempo em que o foco pode se espalhar |

### 5. Implicações para as próximas entregas

- Vale investigar, na modelagem de tarefas (Entrega 5), a tarefa "reunir contexto suficiente para emitir parecer" como uma tarefa própria de P03, distinta da tarefa de captura de P02.
- É preciso levantar, com um agrônomo real, quais metadados mínimos (local, data, sequência de fotos por árvore/talhão) tornariam um relato de campo suficiente para decisão remota, sem ainda desenhar telas.
- As hipóteses H04 (quem decide no dia a dia), H07 (que informação o profissional precisa) e H21 (quem acompanha a evolução do problema) ficam diretamente reforçadas por este cenário e devem ser priorizadas na investigação de campo da Entrega 7.
- Vale checar se o atraso relatado (dias entre detecção e parecer) é consistente com a criticidade já apontada em [H06]/[F20] da Entrega 1, para dimensionar o impacto real do problema.

---

> Repita a estrutura acima para novos cenários, se necessário, com autoria individual.

## Checklist

- [ ] Há um cenário completo por integrante.
- [ ] Cada cenário tem título, ator, objetivo, contexto e problema.
- [ ] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [ ] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [ ] Questões de refinamento acrescentam informação nova.
- [ ] O refinamento mostra claramente o que foi adicionado/alterado.
- [ ] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [ ] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.
