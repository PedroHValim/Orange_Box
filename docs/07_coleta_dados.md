# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** 11/10/2026<br>
**Status:** 🟨 em andamento — planejamento de Lucas preparado; formulário online e coleta pendentes.

## Objetivo da atividade

Identificar necessidades e requisitos de IHC por meio de dados sobre usuários, tecnologia, conhecimento do domínio, tarefas, motivações e valores.

**Base:** material da aula de Barbosa e Silva (2010).

## Para escopos de IHC derivados de TCC técnico

O TCC já prevê uma interface. Mesmo assim, a coleta verificará se as tarefas, necessidades e condições atribuídas às personas correspondem à prática dos usuários.

Se não houver acesso ao público previsto, discutir alternativas com o docente e registrar as limitações. Participantes substitutos não serão apresentados como usuários reais do campo.

## Hipóteses e lacunas prioritárias herdadas da Entrega 1

| ID | Hipótese/lacuna | Evidência atual | Decisão que depende da resposta | Prioridade |
|---|---|---|---|---|
| H03/H20 | Os usuários possuem diferentes níveis de leitura e familiaridade com aplicativos técnicos. | Hipóteses utilizadas na persona P02, sem coleta direta. | Linguagem, instruções e necessidade de ajuda. | Alta |
| H08 | O cansaço pode prejudicar a atenção durante a inspeção. | Situação hipotética retomada no cenário C02. | Quantidade de etapas e apoio à continuidade da tarefa. | Alta |
| H09/H22 | Pode ser necessário registrar locais inspecionados e consultar inspeções anteriores. | Necessidades propostas, ainda não confirmadas. | Controle da rota e eventual histórico. | Alta |
| H21 | O dono/gestor acompanha a evolução do problema na propriedade. | Hipótese sobre a divisão de responsabilidades. | Destinatários e conteúdo do repasse. | Alta |

Experiência no domínio, vocabulário, motivações e preferências de aprendizagem também serão investigados, pois influenciam a compreensão e o uso da interface.

## Parte A — necessidades e requisitos de IHC

> **Responsabilidade:** solução individual por integrante.

### A01 — Lucas

**Autor(a):** Lucas — 24.123.032-5

#### Que dados coletar?

| Grupo da aula | Dado/informação | Hipótese/lacuna relacionada | Por que é necessário / decisão de design |
|---|---|---|---|
| O próprio usuário | Função, idioma de leitura e facilidade para compreender instruções. | H03 | Definir linguagem e quantidade de texto. |
| Relação com tecnologia | Acesso ao celular, aplicativos utilizados, autonomia e conexão em campo. | H20; condições de uso ainda pouco detalhadas. | Definir navegação, ajuda e funcionamento offline. |
| Conhecimento do domínio | Tempo de experiência, forma de aprendizagem e comportamento diante de dúvidas sobre a praga. | Lacuna complementar sobre o conhecimento prático de P02. | Definir explicações e comunicação da incerteza. |
| Conhecimento das tarefas | Frequência, controle da rota, erros, consequências, histórico e repasse dos achados. | H08/H09/H21/H22 | Organizar o fluxo, prevenir erros e apoiar o registro. |
| Motivações e valores | O que considera importante no trabalho, preferência de aprendizagem e condições para adotar uma ferramenta. | H03/H20; lacunas sobre aprendizagem e adoção. | Definir orientação inicial e prioridades da interface. |

Não serão solicitados sexo, renda ou identificação da propriedade, pois não há uma decisão de design definida que justifique esses dados neste recorte.

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Trabalhador de campo/pragueiro. | Ter 18 anos ou mais e ter realizado inspeção de pragas em citros nos últimos 12 meses. | Usuário da captura e do registro; corresponde à persona P02. |

**Amostra planejada:** 5 a 8 participantes por conveniência, buscando diferentes tempos de experiência quando possível.<br>
**Limitação:** levantamento exploratório, sem representatividade estatística.

**Quem utilizará o sistema?** Trabalhadores na captura; gestores e agrônomos na consulta dos resultados, conforme as personas propostas.

**Quem será afetado?** Trabalhadores da inspeção, responsáveis pelo manejo e gestores da propriedade.

**Quem decide os objetivos e funcionalidades?** A equipe do projeto e o orientador definem o escopo, considerando as necessidades levantadas com usuários e stakeholders.

**Quem definiu os processos apoiados?** Será investigado quem orienta a inspeção e o manejo na propriedade. A participação de gestores e agrônomos não será presumida como igual em todos os locais.

O questionário de Lucas coleta a perspectiva do trabalhador. Informações sobre outros papéis precisarão de confirmação com os próprios responsáveis.

#### Aspectos éticos

- **Autonomia:** explicar o estudo, solicitar consentimento e permitir recusa, perguntas em branco ou desistência.
- **Não maleficência:** evitar constrangimento e exposição profissional; não aplicar durante atividades de risco nem diante do supervisor.
- **Beneficência:** buscar melhorias na inspeção, sem prometer benefícios individuais ou eficácia do aplicativo.
- **Justiça e equidade:** convidar pessoas com diferentes experiências e oferecer leitura assistida, sem excluir quem tem dificuldade digital.
- **Minimização e privacidade:** não solicitar nome, telefone, CPF, propriedade ou coordenadas; evitar identificação de colegas nos relatos.
- **Gravação:** não haverá áudio, vídeo ou fotografias dos participantes.
- **Consentimento:** registrar a concordância no formulário antes das perguntas; apresentar os cuidados ao docente antes da aplicação.
- **Armazenamento:** usar códigos R01, R02 etc. e manter respostas individuais em pasta restrita à equipe e ao docente.
- **Divulgação:** publicar apenas sínteses anônimas; não colocar respostas brutas no repositório público nem compartilhá-las com empregadores.
- **Descarte:** apagar os dados brutos até 30 dias após o encerramento da disciplina, mantendo apenas a síntese anônima.
- **Retirada:** enquanto existirem dados individuais, permitir a exclusão mediante o código do participante.

### A02 — Guilherme

**Autor(a):** Guilherme Morais Escudeiro — 24.123.005-1

#### Que dados coletar?

| Grupo da aula | Dado/informação | Hipótese/lacuna relacionada | Por que é necessário / decisão de design |
|---|---|---|---|
| O próprio usuário | Formação, tempo de atuação como consultor, quantidade de propriedades atendidas e se o atendimento é remoto, presencial ou misto. | H04; C03 Q1; persona P03 (atende várias propriedades, não está no campo). | Definir se a interface precisa agrupar alertas por propriedade (A01) e se o uso principal será no escritório ou em visita. |
| Relação com tecnologia | Dispositivos usados para trabalhar (computador, celular, tablet), ferramentas atuais (WhatsApp, e-mail, planilhas, sistemas de gestão agrícola), uso de mapas digitais e conexão no escritório e em visitas. | H20 (aplicada ao agrônomo); persona P03 (experiência tecnológica moderada). | Definir plataforma do fluxo do agrônomo (Entrega 8), densidade de informação por tela e se o mapa é um recurso familiar ou precisa de apoio. |
| Conhecimento do domínio | Sinais que usa para confirmar o ácaro e a leprose em uma foto, limitações de diagnóstico por imagem e quando exige ver o fruto pessoalmente. Opinião sobre usar um sinal automático (IA) como triagem. | H07; CTT T07 (confirmar, rejeitar ou pedir nova foto; possível viés de confirmação). | Definir o que a tela de detecção (A03) precisa mostrar, se o pedido de nova foto (botão em A03) basta sem informar motivo e se a avaliação da IA aparece antes ou depois do veredito. |
| Conhecimento das tarefas | Como recebe hoje os relatos de campo, frequência, informações mínimas para um parecer, como compara com inspeções anteriores, como delimita a área de aplicação, como registra e repassa a recomendação e quanto tempo passa entre o achado e o parecer. | H07, H21, H22; C03 Q1–Q5; HTA T05, GOMS T06 (SR1: o agrônomo sabe o nome/código do talhão?). | Confirmar a ordem do HTA T05, a regra de seleção do GOMS T06 (M1/M2/M3), os metadados mínimos da detecção e o conteúdo do parecer (A06/A07). |
| Motivações e valores | O que considera um parecer bem fundamentado, responsabilidade técnica pela recomendação, receios sobre decisões baseadas em IA e condições para confiar em dados enviados pelo campo. | H07; persona P03 (motivador: evitar aplicação incorreta ou desnecessária). | Definir como separar "detectado pela IA" de "validado por humano", que registro de autoria o parecer precisa ter e o que aumenta ou reduz a confiança no sistema. |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Engenheiro(a) agrônomo(a) ou técnico(a) agrícola que orienta o manejo de pragas em propriedades de citros. | Ter 18 anos ou mais e ter emitido ou orientado recomendação de manejo de pragas em citros nos últimos 12 meses. | Usuário da validação remota e do parecer; corresponde à persona P03. |

**Quem utilizará o sistema?** O agrônomo consultor (P03) na validação das detecções e no parecer; o trabalhador de campo (P02) na captura e ao atender pedidos de nova foto; o dono/gestor (P01) ao receber o parecer e decidir o manejo.<br>
**Quem será afetado?** O dono/gestor, que paga pela aplicação e decide com base no parecer; os trabalhadores que aplicam o produto [H02]; o próprio agrônomo, que responde tecnicamente pela recomendação; e, indiretamente, o ambiente, pela quantidade de defensivo aplicada (C03).<br>
**Quem decide os objetivos e funcionalidades?** A equipe e o orientador definem o escopo da disciplina, a partir das necessidades levantadas. O agrônomo participa como fonte de requisitos sobre o que é suficiente para um parecer, mas não como decisor do escopo.<br>
**Quem definiu os processos apoiados?** Será investigado. A hipótese é que o protocolo de inspeção (intervalo de cerca de 14 dias, pontos amostrados) seja definido ou orientado pelo agrônomo junto ao dono [F08], [H04], e que a decisão final de aplicar seja do dono [F24]. A entrevista verifica essa divisão.

#### Aspectos éticos

- **Autonomia:** explicar objetivo, duração e uso dos dados antes de começar; pedir consentimento explícito; permitir que o participante pule perguntas, interrompa a qualquer momento ou peça a exclusão das respostas.
- **Não maleficência:** a entrevista pede relatos de recomendações que deram errado (C03 Q5), o que pode expor o profissional. Por isso: perguntar sobre situações, não sobre culpados; não pedir nome de clientes ou propriedades; deixar claro que o objetivo é entender o processo, não avaliar a competência técnica de quem responde.
- **Beneficência:** o participante pode receber, se quiser, a síntese anônima dos resultados. Não serão prometidos benefícios individuais nem acesso ao aplicativo.
- **Justiça e equidade:** oferecer a entrevista on-line ou presencial e em horário escolhido pelo participante, para não excluir quem tem agenda de campo.
- **Minimização e privacidade:** sem nome, e-mail ou telefone no registro de respostas; o contato para agendar fica separado das respostas e é apagado após a entrevista. Relatos que permitam identificar uma propriedade serão generalizados ("uma propriedade de médio porte").
- **Gravação:** gravação de áudio apenas se o participante autorizar à parte, só para conferir anotações. Sem autorização, o registro é feito por anotações do entrevistador no formulário. Não haverá vídeo nem fotos do participante.
- **Fotos de frutos:** se o participante mostrar imagens de casos reais, elas não serão copiadas nem publicadas; anota-se apenas o que ele descreveu.
- **Consentimento:** registrado na primeira seção do formulário de registro (aceite lido em voz alta e confirmado), antes de qualquer pergunta. Os cuidados serão apresentados ao docente antes da aplicação.
- **Armazenamento:** respostas identificadas por códigos E01, E02 etc., em pasta restrita à equipe e ao docente. Áudios, quando houver, ficam fora do repositório e são apagados assim que as anotações forem conferidas (até 7 dias após a entrevista).
- **Divulgação:** apenas sínteses anônimas no repositório público.
- **Descarte:** dados brutos apagados até 30 dias após o encerramento da disciplina, mantendo apenas a síntese anônima.
- **Retirada:** enquanto houver dados individuais, o participante pode pedir a exclusão informando o código recebido no fim da entrevista.

### A03 — Pedro

**Autor(a):** Pedro — {{matrícula}}

#### Que dados coletar?

| Grupo da aula | Dado/informação | Hipótese/lacuna relacionada | Por que é necessário / decisão de design |
|---|---|---|---|
| O próprio usuário | {{...}} | {{...}} | {{...}} |
| Relação com tecnologia | {{...}} | {{...}} | {{...}} |
| Conhecimento do domínio | {{...}} | {{...}} | {{...}} |
| Conhecimento das tarefas | {{...}} | {{...}} | {{...}} |
| Motivações e valores | {{...}} | {{...}} | {{...}} |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

**Quem utilizará o sistema?** {{...}}<br>
**Quem será afetado?** {{...}}<br>
**Quem decide os objetivos e funcionalidades?** {{...}}<br>
**Quem definiu os processos apoiados?** {{...}}

#### Aspectos éticos

{{Justificar e descrever consentimento, riscos, privacidade, gravação, armazenamento e descarte.}}

## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica diferente. Questionário deve estar entre as técnicas escolhidas.

### Instrumento I01 — Questionário

**Autor(a):** Lucas — 24.123.032-5<br>
**Técnica:** questionário com perguntas abertas e fechadas.<br>
**Ferramenta prevista:** Google Forms.<br>
**Link:** {{inserir após criar o formulário}}<br>
**Objetivo:** investigar os cinco grupos de dados da aula no contexto da inspeção de citros.<br>
**Público:** trabalhadores de campo/pragueiros.<br>
**Duração estimada:** 20 a 25 minutos.

**Justificativa da técnica:** permite aplicar as mesmas perguntas aos participantes e comparar respostas. As perguntas abertas complementam as alternativas, mas não substituem a profundidade de entrevistas ou observações.

#### Procedimento padronizado de aplicação

1. Criar o formulário online com o conteúdo abaixo, sem solicitar nome, e-mail ou login. Testar as perguntas e o encerramento para quem não consentir ou não atender aos critérios.
2. Combinar um momento adequado, atribuir um código ao formulário e apresentar objetivos, duração, riscos e cuidados com os dados.
3. Solicitar consentimento e verificar os critérios de inclusão. Sem consentimento ou elegibilidade, encerrar e não utilizar as respostas.
4. Aplicar as perguntas na ordem, permitindo que sejam puladas. Na leitura assistida, ler exatamente o texto e as opções, sem sugerir respostas; registrar a modalidade.
5. Encerrar agradecendo e informar o código para eventual retirada. Remover identificadores dos relatos e armazenar os dados em pasta restrita.

**Importância do protocolo:** padroniza a aplicação entre integrantes e reduz diferenças causadas pela maneira de explicar ou perguntar.

#### Instrumento

**Código:** {{R01...}}<br>
**Data:** {{...}}<br>
**Aplicador:** {{...}}<br>
**Modalidade:** ( ) Autopreenchimento ( ) Leitura assistida

**Apresentação:**

“Somos estudantes e queremos compreender como acontece a inspeção de pragas em citros. A participação é voluntária e dura aproximadamente 20 a 25 minutos. Não haverá gravação nem solicitação do seu nome ou da propriedade. Você pode pular perguntas ou parar a qualquer momento. Relatos podem causar desconforto; não identifique colegas ou empregadores. As respostas individuais ficarão restritas à equipe e ao docente. Serão divulgadas apenas sínteses anônimas. Não há benefício direto garantido. Os dados brutos serão apagados até 30 dias após o encerramento da disciplina; até lá, você poderá solicitar a retirada pelo código do formulário.”

**Consentimento:** concorda em participar?<br>
( ) Sim<br>
( ) Não — encerrar.

**Triagem:**

- Tem 18 anos ou mais? ( ) Sim ( ) Não
- Inspecionou pragas em citros nos últimos 12 meses? ( ) Sim ( ) Não

Se alguma resposta for “Não”, agradecer e encerrar.

### Bloco 1 — O próprio usuário

**1. Qual é sua função no trabalho de inspeção?**

Resposta: __________________________________

**2. Em qual idioma prefere ler instruções?**

Resposta: __________________________________

**3. Como considera a leitura de instruções no celular?**

( ) Muito fácil<br>
( ) Fácil<br>
( ) Nem fácil nem difícil<br>
( ) Difícil<br>
( ) Muito difícil<br>
( ) Não utilizo/não sei avaliar

### Bloco 2 — Relação com tecnologia

**4. Qual é seu acesso a um celular para o trabalho?**

( ) Uso um celular individual.<br>
( ) Uso um celular compartilhado.<br>
( ) Não tenho acesso.<br>
( ) Outra situação: __________

**5. Quais aplicativos costuma utilizar e para quê?**

Resposta: __________________________________<br>
( ) Não utilizo aplicativos.

**6. Ao realizar uma tarefa nova no celular, com que frequência precisa de ajuda?**

( ) Nunca<br>
( ) Raramente<br>
( ) Às vezes<br>
( ) Frequentemente<br>
( ) Sempre<br>
( ) Não utilizo celular.

**7. Como é o acesso à internet durante a inspeção?**

( ) Disponível na maior parte do percurso.<br>
( ) Disponível somente em alguns pontos.<br>
( ) Raramente disponível.<br>
( ) Não há acesso.<br>
( ) Não sei/não utilizo.

### Bloco 3 — Conhecimento do domínio

**8. Há quanto tempo realiza inspeções de pragas?**

( ) Menos de 1 ano<br>
( ) De 1 a 5 anos<br>
( ) Mais de 5 anos

**9. Como aprendeu a identificar sinais de pragas? Marque as opções aplicáveis.**

[ ] Curso ou treinamento.<br>
[ ] Orientação de colegas.<br>
[ ] Experiência prática.<br>
[ ] Materiais de consulta.<br>
[ ] Outra forma: __________

**10. O que costuma fazer quando não tem certeza se encontrou uma praga?**

Resposta: __________________________________

### Bloco 4 — Conhecimento das tarefas

**11. Com que frequência realiza inspeções e qual é o volume aproximado de um dia típico?**

Frequência: __________<br>
Árvores por dia: __________<br>
Frutos por árvore: __________<br>
( ) Não sei estimar o volume.

**12. Como controla os locais já inspecionados e os que ainda faltam?**

Resposta: __________________________________<br>
( ) Não faço esse controle.

**13. Lembra de alguma dificuldade ou erro durante a inspeção nos últimos três meses?**

( ) Sim ( ) Não ( ) Não lembro

Se sim:<br>
O que aconteceu? __________<br>
Quais foram as consequências? __________<br>
Como a situação foi resolvida? __________

**14. Nos últimos três meses, precisou consultar uma inspeção anterior?**

( ) Sim ( ) Não ( ) Não lembro

Se sim:<br>
Para quê? __________<br>
Quais informações procurou? __________<br>
Conseguiu encontrá-las? __________

**15. Quando encontra algo suspeito, como faz o repasse?**

Para qual função/profissional informa? __________<br>
Qual meio utiliza? __________<br>
Como identifica o local do achado? __________<br>
Como sabe que a informação chegou? __________

Não informar nomes de pessoas ou da propriedade.

**16. Quem acompanha a evolução dos achados e quem decide as ações?**

Função de quem acompanha: __________<br>
Função de quem decide: __________<br>
( ) Não sei.

**17. Imagine que um aplicativo apresente as mensagens abaixo. O que cada uma significa para você e o que faria em seguida?**

- “Sinal suspeito”: __________________________
- “Nenhum sinal nesta foto”: _________________
- “Resultado inconclusivo”: __________________

### Bloco 5 — Motivações e valores

**18. O que considera mais importante para realizar bem seu trabalho de inspeção?**

Resposta: __________________________________

**19. Como prefere aprender a usar uma ferramenta nova? Marque as opções aplicáveis.**

[ ] Explicação de outra pessoa.<br>
[ ] Demonstração prática.<br>
[ ] Instruções escritas.<br>
[ ] Vídeo ou áudio.<br>
[ ] Experimentando a ferramenta.<br>
[ ] Outra forma: __________

**20. O que levaria você a utilizar ou deixar de utilizar uma nova ferramenta de inspeção?**

Resposta: __________________________________

**Comentário adicional opcional:** __________________________

#### Como os dados serão analisados

- Contar as respostas fechadas, informando o total válido e as perguntas não respondidas.
- Agrupar respostas abertas pelos cinco grupos da aula.
- Identificar vocabulário recorrente, dificuldades, necessidades e divergências.
- Relacionar cada achado a uma decisão de interface.
- Tratar preferências de aprendizagem como preferências relatadas, não como capacidades fixas.
- Registrar a amostra alcançada e suas limitações, sem generalizar para todos os trabalhadores.

| Hipótese/lacuna | Perguntas | Decisão de design relacionada |
|---|---|---|
| H03/H20 | 2–7, 17 e 19 | Linguagem, ajuda, navegação e orientação inicial. |
| H08 | 11 e 13 | Redução de esforço e apoio à continuidade da inspeção. |
| H09/H22 | 12 e 14 | Controle da cobertura e necessidade de histórico. |
| H21 | 15 e 16 | Responsabilidades e repasse dos achados. |
| Conhecimento do domínio | 8–10 | Explicações e alternativas diante de dúvidas. |
| Motivações e valores | 18–20 | Prioridades de uso e barreiras à adoção. |

Relatos podem apoiar ou contrariar hipóteses, mas não comprovam relações de causa. Por exemplo, o questionário não demonstra sozinho que o cansaço causa perda de focos.

### Instrumento I02 — Entrevista semiestruturada

**Autor(a):** Guilherme Morais Escudeiro — 24.123.005-1<br>
**Técnica:** entrevista semiestruturada individual, com roteiro fixo de perguntas e aprofundamentos opcionais.<br>
**Ferramenta:** Google Meet (ou presencial) para a conversa; Google Forms como formulário de registro, preenchido pelo entrevistador durante a entrevista, com o consentimento na primeira seção.<br>
**Link, quando aplicável:** pendente — inserir após criar o formulário de registro.<br>
**Objetivo:** entender como o agrônomo consultor recebe relatos de campo, decide se há foco, compara com inspeções anteriores, dimensiona a área e repassa a recomendação, e quais informações e garantias precisaria para confiar em uma detecção feita por IA.<br>
**Público:** agrônomos(as) e técnicos(as) agrícolas que orientam o manejo de pragas em citros (perfil P03).<br>
**Justificativa da técnica:** o público é pequeno, especializado e com agenda de campo, o que torna um questionário com muitas respostas pouco viável. As dúvidas do C03 (Q1–Q5) pedem relatos de casos concretos e explicações de raciocínio técnico ("como você decide a área?"), que só aparecem com perguntas de aprofundamento. A entrevista complementa o questionário de Lucas, que cobre o trabalhador de campo, e permite cruzar as duas visões sobre o repasse dos achados (H21).

#### Procedimento padronizado de aplicação

1. **Preparação:** criar o formulário de registro no Google Forms com as seções abaixo, sem campos de nome, e-mail ou login. Fazer uma entrevista piloto com um colega para ajustar tempo e redação. Agendar com o participante, enviando antes o texto de apresentação, e atribuir um código (E01, E02...).
2. **Apresentação e consentimento:** ler o texto de apresentação, pedir o consentimento e, à parte, a autorização de gravação de áudio. Verificar os critérios de inclusão. Sem consentimento ou elegibilidade, encerrar sem registrar respostas.
3. **Aplicação:** seguir os blocos na ordem. Fazer sempre a pergunta principal com o texto do roteiro; usar os aprofundamentos apenas quando a resposta não cobrir o ponto, sem sugerir respostas nem citar a solução da equipe antes do Bloco 6. Pedir exemplos de casos reais ("a última vez que..."), não opiniões gerais. Registrar no formulário, com as palavras do participante sempre que possível.
4. **Encerramento:** perguntar se há algo não abordado, agradecer, informar o código para eventual retirada e oferecer o envio da síntese anônima.
5. **Armazenamento e anonimização:** em até 48 horas, revisar as anotações, remover nomes de pessoas, clientes e propriedades, e conferir com o áudio (se houver), apagando-o em seguida. Guardar as respostas em pasta restrita à equipe e ao docente.


#### Instrumento

**Código:** E__<br>
**Data:** ____<br>
**Entrevistador:** ____<br>
**Modalidade:** ( ) On-line ( ) Presencial<br>
**Gravação de áudio autorizada:** ( ) Sim ( ) Não

**Apresentação:**

"Somos estudantes da FEI e estamos estudando como agrônomos e técnicos acompanham o ácaro-da-leprose em citros, para projetar uma ferramenta de apoio. Queremos entender o seu processo de trabalho; não estamos avaliando o seu conhecimento técnico. A conversa leva cerca de 30 a 40 minutos. Não vamos registrar seu nome nem o nome das propriedades que você atende, e pedimos que não cite nomes de clientes ou colegas. Você pode pular perguntas ou parar a qualquer momento. Só gravamos o áudio se você autorizar, e ele será apagado depois de conferirmos as anotações. As respostas ficam restritas à equipe e ao docente; publicamos apenas um resumo anônimo. Os dados individuais serão apagados até 30 dias após o fim da disciplina, e até lá você pode pedir a exclusão pelo código desta entrevista."

**Consentimento:** concorda em participar? ( ) Sim ( ) Não — encerrar.<br>
**Gravação:** autoriza a gravação apenas de áudio? ( ) Sim ( ) Não — seguir só com anotações.

**Triagem:**

- Tem 18 anos ou mais? ( ) Sim ( ) Não
- Emitiu ou orientou alguma recomendação de manejo de pragas em citros nos últimos 12 meses? ( ) Sim ( ) Não

Se alguma resposta for "Não", agradecer e encerrar.

##### Bloco 1 — O próprio usuário

**1. Qual é a sua formação e há quanto tempo trabalha com citros?**<br>
Formação: ( ) Agronomia ( ) Técnico agrícola ( ) Outra: ____<br>
Tempo com citros: ( ) Menos de 2 anos ( ) 2 a 5 anos ( ) 6 a 10 anos ( ) Mais de 10 anos

**2. Quantas propriedades você acompanha hoje e como é esse acompanhamento?**<br>
Quantidade aproximada: ____<br>
( ) Principalmente a distância ( ) Principalmente em visitas ( ) Misto<br>
*Aprofundamento:* com que frequência visita cada propriedade?

##### Bloco 2 — Relação com tecnologia

**3. Que equipamentos e ferramentas você usa para acompanhar as propriedades?**<br>
[ ] Computador [ ] Celular [ ] Tablet<br>
[ ] WhatsApp ou outro mensageiro [ ] E-mail [ ] Planilhas [ ] Sistema de gestão agrícola [ ] Mapas/imagens de satélite [ ] Outro: ____<br>
*Aprofundamento:* em qual equipamento você costuma analisar fotos enviadas pelo campo? Por quê?

**4. Você já usa mapas digitais da propriedade (talhões, pontos) no seu trabalho?**<br>
( ) Sim, com frequência ( ) Às vezes ( ) Não<br>
*Aprofundamento:* se sim, para quê? Se não, como localiza um talhão ou um ponto?

##### Bloco 3 — Conhecimento das tarefas (processo atual)

**5. Pense na última vez em que recebeu um relato de possível ácaro ou leprose. Como a informação chegou até você?**<br>
Quem avisou (função): ____<br>
Meio: ____<br>
O que veio junto (fotos, local, data, quantidade): ____<br>
*Aprofundamento:* isso é comum? Com que frequência acontece por mês?

**6. Para dar um parecer em que você confia, quais informações são indispensáveis? E quais ajudam, mas não são obrigatórias?**<br>
Indispensáveis: ____<br>
Desejáveis: ____<br>
*Aprofundamento:* o que costuma faltar? O que faz quando falta?

**7. Quando a informação não é suficiente, o que você faz?**<br>
[ ] Ligo para quem está na propriedade [ ] Peço novas fotos [ ] Agendo visita [ ] Decido com o que tenho [ ] Outro: ____<br>
*Aprofundamento:* quanto tempo isso costuma atrasar o parecer? Quando você pede uma nova foto, o que pede exatamente (outro ângulo, outro fruto, frutos vizinhos)?

**8. Você compara o caso atual com inspeções anteriores do mesmo local? Como?**<br>
( ) Sim, sempre ( ) Às vezes ( ) Não<br>
Onde busca: ____<br>
*Aprofundamento:* você costuma lembrar o nome ou código dos talhões de cada propriedade, ou se orienta por outra referência (mapa, nome popular, ponto de referência)?

**9. Como você decide o tamanho da área em que recomenda a aplicação?**<br>
Resposta: ____<br>
*Aprofundamento:* já aconteceu de a área recomendada se mostrar maior ou menor do que o necessário? O que levou a isso e qual foi a consequência?

**10. Como sua recomendação é registrada e chega a quem decide e a quem aplica?**<br>
Meio: ____<br>
Quem recebe (função): ____<br>
Como sabe que foi recebida e seguida: ____<br>
*Aprofundamento:* você guarda um histórico das recomendações que fez? Como?

**11. Quem decide de fato se e onde aplicar: você, o dono ou outra pessoa?**<br>
Resposta: ____<br>
*Aprofundamento:* quem define o protocolo de inspeção (intervalo, pontos amostrados)?

##### Bloco 4 — Conhecimento do domínio

**12. Por uma foto, o que permite afirmar que há ácaro ou leprose? O que só é possível confirmar vendo o fruto?**<br>
Visível em foto: ____<br>
Só presencialmente: ____

**13. Quais erros de identificação são mais comuns (confusão com outra praga, doença ou dano)?**<br>
Resposta: ____

##### Bloco 5 — Motivações e valores

**14. O que, para você, torna um parecer técnico bem fundamentado?**<br>
Resposta: ____

**15. Imagine que um sistema indique automaticamente "possível ácaro" em uma foto. Em que situações você confiaria nessa indicação, e em quais não confiaria?**<br>
Confiaria quando: ____<br>
Não confiaria quando: ____<br>
*Aprofundamento:* você preferiria ver a avaliação do sistema antes ou depois de olhar a foto? Por quê?

**16. Que responsabilidade você sente ao assinar uma recomendação baseada em fotos enviadas por outras pessoas?**<br>
Resposta: ____

##### Bloco 6 — Reação a conceitos (aplicar por último)

Mostrar ao participante, nesta ordem, a lista abaixo sem explicar a solução da equipe:

> Foto original do fruto · Data e hora da foto · Localização no mapa (talhão e ponto) · Identificação da árvore · Fotos anteriores do mesmo ponto · Indicação do sistema ("possível ácaro") · Grau de confiança do sistema · Observação de quem tirou a foto · Quantidade de pontos com sinal no talhão

**17. Destas informações, quais você usaria para validar um caso? Ordene as cinco mais importantes.**<br>
1. ____ 2. ____ 3. ____ 4. ____ 5. ____<br>
Alguma informação está faltando? ____

**18. Ao terminar a análise de um caso, o que você precisaria conseguir fazer em seguida?**<br>
Resposta: ____

**Comentário adicional opcional:** ____

**Encerramento:** "Obrigado pela participação. O código desta entrevista é E__. Se quiser retirar suas respostas, basta informar esse código à equipe até 30 dias após o fim da disciplina."

#### Como os dados serão analisados

- Revisar as anotações e organizar as respostas por bloco em uma tabela por participante (E01, E02...).
- Fazer uma análise temática simples: marcar trechos com códigos ligados aos cinco grupos da aula e às hipóteses (H04, H07, H21, H22), e agrupar códigos repetidos entre participantes.
- Para a pergunta 17, contar quantas vezes cada informação aparece entre as cinco mais importantes, apenas como indicação de prioridade (amostra pequena).
- Registrar divergências entre participantes, sem forçar consenso, e comparar com o que os trabalhadores relatam no questionário de Lucas (perguntas 15 e 16) sobre o repasse dos achados.
- Ligar cada achado a uma decisão de design e a uma tela do protótipo (A01–A03 e A05–A07), e marcar no `RASTREABILIDADE.md` se a hipótese ficou sustentada, refutada, refinada ou aberta.

| Hipótese/lacuna | Perguntas | Decisão de design relacionada |
|---|---|---|
| H04 (quem decide no dia a dia) | 2, 11 | Destinatário do parecer e papel do agrônomo no fluxo (A07). |
| H07 (informação necessária para decidir) | 5, 6, 12, 17 | Conteúdo mínimo da tela de detecção (A03) e metadados gravados na captura. |
| H21 (quem acompanha a evolução) | 10, 11 | Repasse do parecer ao gestor e situação do pedido na lista (A01). |
| H22 (necessidade de histórico) | 8, 10 | Decidir se o histórico precisa aparecer na tela da detecção (A03) ou se basta o histórico do talhão (A05). |
| C03 Q1 e Q4 (frequência e atraso) | 5, 7 | Prioridade do fluxo do agrônomo e criticidade de T05 na Entrega 8. |
| C03 Q2 e Q3 (informação mínima e como supre a falta) | 6, 7 | Pedido de nova foto (A03) e alternativa de visita. |
| C03 Q5 (consequência de decidir mal) | 9 | Delimitação da área só com pontos confirmados (A06). |
| GOMS T06, regra SR1 | 4, 8 | Se o histórico deve permitir busca por nome do talhão (M2) ou priorizar o mapa (M1) e o atalho a partir da detecção (M3). |
| CTT T07, viés de confirmação | 15 | Mostrar a avaliação da IA antes ou depois do veredito (A03). |
| Plataforma do fluxo do agrônomo | 3 | Computador, tablet ou celular (Entrega 8). |

Relatos de poucos especialistas indicam práticas e necessidades plausíveis, mas não representam todos os agrônomos. Quando um único participante relatar algo, o achado fica como indício, não como fato.

### Instrumento I03 — {{nome da técnica}}

**Autor(a):** Pedro — {{matrícula}}<br>
**Técnica:** {{diferente do questionário e da técnica de Guilherme}}<br>
**Ferramenta:** {{...}}<br>
**Link, quando aplicável:** {{...}}<br>
**Objetivo:** {{...}}<br>
**Público:** {{...}}<br>
**Justificativa da técnica:** {{...}}

#### Procedimento padronizado de aplicação

1. {{preparação}}
2. {{apresentação/consentimento}}
3. {{aplicação}}
4. {{encerramento}}
5. {{armazenamento/anonimização}}

#### Instrumento

{{Inserir o conteúdo completo. Se escolher entrevista, utilizar também uma ferramenta online, conforme a aula.}}

#### Como os dados serão analisados

{{...}}

## Síntese

**Lucas:** o questionário investiga os cinco grupos da aula e pretende reduzir dúvidas sobre compreensão, autonomia digital, experiência, rotina e adoção da ferramenta.

Após a análise, H03, H08, H09, H20, H21 e H22 poderão receber evidências favoráveis, contrárias ou que exijam refinamento. Evidência insuficiente manterá a hipótese em aberto.

**Guilherme:** a entrevista semiestruturada investiga os cinco grupos da aula para o agrônomo consultor (P03) e pretende confirmar ou corrigir as respostas hipotéticas do C03 (Q1–Q5), a ordem do HTA T05, a regra de seleção do GOMS T06 e o momento de mostrar a avaliação da IA no CTT T07. Após a análise, H04, H07, H21 e H22 poderão receber evidências favoráveis, contrárias ou que exijam refinamento. **Pendente:** criar o formulário de registro, recrutar os participantes, aplicar as entrevistas e preencher os resultados.

**Pedro:** {{...}}

A síntese integrada dependerá dos instrumentos dos três integrantes. Após a coleta e a análise, atualizar `RASTREABILIDADE.md` com evidências, limitações e decisões de design.

## Checklist

**Marcações referentes à parte preparada por Lucas. Os requisitos coletivos permanecem pendentes.**

- [x] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas.
- [x] A coleta investiga a plausibilidade do usuário, tarefa e contexto adotados.
- [x] Perguntas investigam necessidades sem pressupor dashboard, CRUD, filtros ou relatórios.
- [x] Cada dado a coletar responde uma dúvida concreta ou justifica outra necessidade de informação.
- [x] Parte A identifica dados e perfis de coleta de forma específica.
- [x] Os cinco grupos de dados apresentados na aula foram contemplados.
- [x] Aspectos éticos são contextualizados para o projeto.
- [ ] Há uma técnica completa por integrante e técnicas distintas.
- [x] Questionário está incluído entre as técnicas.
- [ ] Cada instrumento possui objetivo, público, procedimento e conteúdo integral.
- [x] O instrumento de Lucas contém perguntas sem indução intencional e evita dados identificadores desnecessários.
- [x] Está claro como os dados de Lucas serão analisados e usados no design.
- [ ] O questionário foi criado e conferido na ferramenta online, com link inserido.
