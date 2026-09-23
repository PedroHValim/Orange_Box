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

## Cenário C01 — {{título}}

**Autor(a):** {{nome — matrícula}}  
**Persona(s) relacionada(s):** {{P01}}  
**Necessidade relacionada:** {{R01}}  
**Situação concreta da Entrega 1 relacionada:** {{seção 4.4 / H01 / outra ou “nova situação justificada”}}  
**Hipóteses ainda presentes:** {{H01, H02 ou —}}

### 1. Cenário inicial

{{narrativa}}

### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | {{...}} | {{...}} | {{...}} |

### 3. Cenário refinado

Reescreva o cenário incorporando as respostas. Marque o conteúdo novo de forma consistente (por exemplo, `**[NOVO: ...]**`).

{{narrativa refinada}}

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | {{...}} |
| Objetivo(s) | {{...}} |
| Contexto | {{...}} |
| Recursos/informações | {{...}} |
| Ações | {{...}} |
| Problemas/rupturas | {{...}} |
| Consequências | {{...}} |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

> Repita para C02, C03... com autoria individual.

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
