# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 19/08/2026
**Status:** 🟨 em andamento 
**Responsabilidade:** 1 solução consolidada por equipe

## Objetivo da atividade

Reinterpretar o tema do TCC sob a perspectiva de Interação Humano-Computador e construir um **entendimento comum entre os integrantes da equipe**.

A disciplina utiliza preferencialmente o tema do TCC para os exercícios de IHC. Isso vale tanto para TCCs que já preveem uma interface quanto para trabalhos cujo resultado principal é algoritmo, modelo, API, biblioteca, análise de dados, infraestrutura, estudo experimental ou outro artefato técnico.

> **Importante:** a interface projetada na disciplina é um artefato de aprendizagem de IHC. Ela **não se torna automaticamente uma obrigação do TCC**. Sua incorporação ao trabalho de conclusão depende de decisão da equipe e do orientador.

Antes de preencher, leia [`../GUIA_ESCOPO_IHC.md`](../GUIA_ESCOPO_IHC.md).

Nesta primeira semana a equipe **não deve começar desenhando telas**. Primeiro deverá compreender:

- o que o TCC realmente produz;
- quem poderia obter valor dessa contribuição;
- quais pessoas interagem, administram, configuram, interpretam ou são afetadas;
- o que essas pessoas precisam alcançar;
- como atividades relacionadas acontecem hoje;
- problemas, limitações e contexto;
- alternativas existentes;
- qual recorte de interação fará sentido para a disciplina.

Ao final desta entrega, a equipe deve diferenciar:

- **tema do TCC** × **escopo formal do TCC** × **escopo de IHC da disciplina**;
- **objetivo do projeto** × **objetivo do usuário**;
- **problema do usuário** × **solução tecnológica**;
- **fato conhecido** × **hipótese** × **lacuna de conhecimento**;
- **capacidade técnica** × **forma de uso dessa capacidade**;
- **funcionalidade** × **atividade/resultado que o usuário precisa alcançar**;
- **usuário direto** × **stakeholders**.

---

## Como classificar as respostas

Sempre que a resposta fizer uma afirmação sobre usuários, problemas, atividades, necessidades, contexto ou mercado, use:

- **[F] Fato conhecido** — existe evidência/fonte.
- **[H] Hipótese** — afirmação plausível que ainda precisa ser investigada.
- **[?] Não sabemos ainda** — lacuna relevante.

Quando usar `[F]`, informe a origem. Hipóteses prioritárias devem receber IDs (`H01`, `H02`...) e também ser registradas em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

> **Exemplo:** `[H] H01 — DBAs considerariam útil comparar automaticamente o plano atual de execução com uma recomendação produzida pelo algoritmo.`

Uma hipótese explicitada é melhor do que uma suposição escondida.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |
|---|---:|---|
| Lucas Tonoli Cabral Duarte | 24.123.032-5 | Cabral100 |
| Guilherme Morais Escudeiro | 24.123.005-1 | GMEscudeiro |
| Pedro Henrique Ferreira Valim | 24.123.048-1 | PedroHValim |

## 0.2 Título atual do TCC

Detecção Automatizada do Ácaro da Leprose na Citricultura via Redes Neurais Convolucionais em Dispositivos Móveis

## 0.3 Orientador(a)

Plinio Thomaz Aquino Junior

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [x] sistema/aplicação interativa;
- [x] algoritmo;
- [x] modelo de IA/ML/LLM;
- [x] biblioteca/API/framework;
- [x] análise de dataset;
- [x] estudo/benchmark/avaliação experimental;
- [x] infraestrutura/backend;
- [x] componente embarcado/IoT;
- [ ] outro: {{...}}.

**Descrição:** Utilizaremos visão computacional para a detecção do ácaro da leprose, a partir de um dataset desenvolvido pelo grupo com imagens do ácaro.

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [x] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [ ] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** Está previsto ter um sistema visual para que o usuário final possa marcar o ácaro a partir de um dispositivo mobile e poder utilizar o sistema de geolocalização ao marcar essa praga em campo.

> Esta resposta serve para separar o compromisso do TCC do projeto da disciplina. Mesmo quando a opção for **não**, a equipe irá definir uma interface para exercitar IHC.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

Detecção de ácaros da leprose em laranjas.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

- **[F]** Dificuldade de detecção do ácaro da leprose em citros.
- **[F]** Não existir um dataset com ácaros de citros.

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

Nosso TCC permite detectar o ácaro da leprose através de visão computacional e prover um sistema de geolocalização para o usuário final.

## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

- **[F]** Trabalhadores rurais comuns poderão detectar as pragas sem necessariamente um "pragueiro" — especialista em detecção de pragas.
- **[F]** Menor esforço físico na detecção de pragas.
- **[F]** Auxílio no gerenciamento de infestações de pragas em campo com a geolocalização.
- **[H]** Disponibilização do dataset do ácaro.

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| Criação de um Dataset | Utilizar o dataset para a detecção do ácaro |
| Protocolo padronizado de captura óptica para alvos sub-milimétricos | Guia prático para o produtor escolher a combinação smartphone + lente macro adequada em campo |
| Comparação sistemática entre YOLO26n, YOLO26s e YOLOv8n | Orientar a escolha de arquiteturas leves em outras aplicações de Edge AI agrícola sem GPU dedicada |
| Exportação do modelo para TensorFlow Lite embarcado em smartphone (52 ms/imagem, offline) | Aplicativo de inspeção assistida por IA funcionando sem internet em áreas rurais |
| Sistema de mapeamento de focos e zonas de risco adjacentes através da geolocalização via metadados EXIF | Suporte à tomada de decisão para tratamento localizado em vez de pulverização uniforme do talhão, reduzindo custo e impacto ambiental |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

Se não houver interface prevista no TCC, escreva `NÃO SE APLICA AO ESCOPO ORIGINAL` e prossiga para 2.2.

**[F]** Essa interface final é destinada a **qualquer pessoa que atue na operação da fazenda** — não a um perfil único e especializado — já que o próprio TCC justifica a escolha do smartphone por sua alta capilaridade, baixo custo relativo e facilidade de operação pelo produtor rural no campo. Isso inclui, entre outros: pragueiros, donos/gestores da propriedade e trabalhadores rurais em geral.

## 2.2 Quem poderia usar, configurar, administrar, operar, interpretar ou tomar decisões a partir da contribuição técnica?

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Pessoas que trabalham na fazenda (pragueiros, dono/gestor da propriedade, trabalhadores rurais, etc.) | Usuários diretos do aplicativo final | Capturam imagens do fruto com a câmera do smartphone, visualizam detecções e o mapa de focos/zonas de risco, e usam essa informação para orientar o manejo (ex.: aplicação localizada de acaricida) | **[F]** O TCC justifica o uso do smartphone pela facilidade de operação em campo e cita o suporte à decisão sobre aplicação localizada de defensivos |
| Agrônomo da propriedade | Participa da definição do período de coleta de dados | Define, junto à equipe, o período de maior atividade populacional do ácaro para orientar a coleta em campo | **[F]** O TCC relata que o período de coleta foi definido em conjunto com o agrônomo responsável pela propriedade parceira |
| Equipe técnica/pesquisadores (autores) | Responsáveis pelo desenvolvimento do modelo e do pipeline | Treinam o modelo, ajustam hiperparâmetros, comparam arquiteturas (TCC 1 e TCC 2) | **[F]** Descrito nas etapas de treinamento e comparação de modelos ao longo do TCC |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Empresas e indústrias que compram a laranja/suco | Ganham ou perdem dependendo de quanto a safra é afetada pela praga | Não | **[F]** O trabalho menciona a importância econômica da citricultura para o país |
| Trabalhadores que aplicam o produto de controle no campo (quando não são os mesmos que usam o app) | Passam a aplicar o produto apenas em pontos específicos, em vez de na fazenda toda | Não | **[H13]** Consequência provável da aplicação localizada, ainda não confirmada com essas pessoas |
| Vizinhança/meio ambiente ao redor da propriedade | Recebe menos produto químico se a aplicação passar a ser localizada | Não | **[F]** O trabalho menciona redução do impacto ambiental como benefício esperado |
| Consumidor final da fruta/suco | Pode ser afetado indiretamente por preço ou disponibilidade do produto | Não | **[?]** Não é discutido no trabalho, é apenas um efeito possível de mercado |

## 2.4 Que características desses perfis podem influenciar a interação?

- **[F]** As pessoas da fazenda já usam celular no dia a dia, mas não necessariamente têm prática com aplicativos técnicos.
- **[F]** O trabalho de campo é feito ao ar livre, muitas vezes com pouco ou nenhum sinal de internet.
- **[F]** Existe urgência: quanto mais tempo demora para perceber o problema, maior o prejuízo.
- **[H02]** É provável que nem todos tenham o mesmo nível de leitura/familiaridade com tecnologia, então a interface precisa ser simples e visual.
- **[?]** Ainda não sabemos o nível real de conhecimento digital dessas pessoas nem se há alguma necessidade especial de acessibilidade.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

**[F]** Proteger a produção de laranja, evitando que a praga se espalhe, gastando menos com produtos de controle e agindo antes que o prejuízo seja grande.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Verificar os frutos em busca de sinais da praga | Pessoas que trabalham na fazenda | Alta — precisa ser repetida com frequência | **[F]** O trabalho descreve a inspeção como atividade recorrente |
| A02 | Decidir onde e quando aplicar o produto de controle | Dono/gestor da fazenda | Média — depende do resultado da inspeção | **[H06]** Ainda não confirmado quem exatamente toma essa decisão no dia a dia |
| A03 | Acompanhar se o problema está se espalhando pela propriedade | Dono/gestor da fazenda | Contínua, ao longo do tempo | **[H08]** Ainda não confirmado como esse acompanhamento é feito hoje |

## 3.3 Qual atividade parece mais frequente? Por quê?

**[F]** A verificação dos frutos (A01), porque precisa ser repetida várias vezes ao longo do ano para não deixar a praga passar despercebida.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

**[H06]** Decidir onde aplicar o produto de controle (A02) parece a mais crítica: se for mal feita, o produtor gasta dinheiro à toa em áreas sem problema ou deixa a praga se espalhar em áreas que precisavam de atenção.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje?

**[F]** Hoje a verificação é feita por uma pessoa treinada, que percorre a plantação a pé e observa os frutos com uma lupa, sem apoio de tecnologia.

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

**[F]** A praga é muito pequena e difícil de enxergar, o processo é cansativo e demorado, e não é possível checar todos os frutos, então parte da plantação fica sem cobertura.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

**[H18]** Provavelmente: se há sinais da praga, em quais pontos da plantação, com que intensidade e se a situação exige ação imediata ou pode esperar a próxima inspeção.

## 4.4 O que acontece quando a atividade falha ou o resultado é interpretado incorretamente?

**[F]** A praga continua se espalhando sem ser percebida, atinge mais plantas e o prejuízo na safra aumenta.

## 4.5 Conte uma situação concreta.

**[H19]** Um trabalhador percorre a plantação em um dia de sol forte, verificando fruto por fruto com uma lupa. Depois de algumas horas, cansado, ele passa mais rápido pelos últimos pés de laranja. Um foco pequeno da praga passa despercebido nessa área e, semanas depois, quando é notado, já afetou várias árvores vizinhas, gerando perda de produção que poderia ter sido evitada com uma detecção mais cedo.

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Descrição do processo manual no trabalho | Mostra que a inspeção hoje depende inteiramente de uma pessoa treinada e de uma lupa | Não traz relatos diretos de trabalhadores ou donos de fazenda |
| Dados sobre erro de amostragem citados no trabalho | Mostra que o método manual pode errar bastante quando não é bem aplicado | Vem de uma fonte do setor, não de teste direto com os usuários do nosso projeto |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

**[F]** No meio da plantação, durante a inspeção dos frutos, ao ar livre.

## 5.2 Em quais dispositivos/equipamentos?

**[F]** Smartphone com câmera.

## 5.3 Existem condições físicas relevantes?

**[F]** Sol forte, calor, pouca ou nenhuma internet, pessoa caminhando entre as árvores, pouco tempo disponível por planta.

## 5.4 Existem fatores sociais ou organizacionais?

**[F]** Não necessariamente quem faz a inspeção no campo é quem decide o que fazer com o resultado (ex.: trabalhador informa, dono/gestor decide), confirmado pelo estudo em campo.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

**[H21]** Sim, provavelmente: saber onde já foi inspecionado e onde já houve problema antes ajuda a acompanhar a evolução ao longo do tempo, mas isso não foi confirmado com os usuários.

## 5.6 Um erro pode produzir consequência relevante? Qual?

**[F]** Sim: não perceber a praga a tempo, ou agir no lugar errado, pode fazer o problema se espalhar e aumentar o prejuízo na safra.

---

# 6. Entendendo mercado e alternativas existentes

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Inspeção visual com lupa | Pessoa treinada na fazenda | Encontrar sinais da praga nos frutos | **[F]** Descrito como o método atual no trabalho |

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

**[?]** Ainda não foi levantado no trabalho; existem de forma geral aplicativos de identificação de pragas e doenças em plantas por foto, mas não é confirmado se algum é voltado para essa praga específica.

## 6.3 Quais interfaces profissionais esse público já conhece?

**[H22]** Provavelmente aplicativos simples do dia a dia, como câmera do celular, mensagens e aplicativos de previsão do tempo — ainda não confirmado.

## 6.4 O que essas soluções parecem fazer bem?

**[H23]** São simples e já fazem parte da rotina dessas pessoas.

## 6.5 O que parecem fazer mal, dificultar ou não atender?

**[H24]** Não são feitas para esse problema específico e não ajudam a decidir onde agir dentro da fazenda.

## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

**[H25]** Fotos, mapas simples, alertas e ícones grandes e fáceis de entender.

---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Caminho escolhido

**Caminho A — TCC já possui interface.** O trabalho já prevê um aplicativo com câmera que detecta a praga e mostra o resultado, além de um mapa com os pontos de risco na propriedade. Esse fluxo (capturar foto → ver resultado → ver mapa) é o recorte relevante para a disciplina.

## 7.2 Qual perfil será priorizado no projeto de IHC?

Pessoas que trabalham na fazenda de forma geral (pragueiros, dono/gestor, trabalhadores rurais).

**Por que esse perfil foi escolhido?** Porque são elas que vão realmente segurar o celular, tirar a foto e usar o resultado no dia a dia.

## 7.3 Qual objetivo desse usuário será priorizado?

Conseguir saber, de forma rápida e simples, se há sinal da praga no fruto e onde estão os pontos de atenção na propriedade.

## 7.4 Que interface será explorada na disciplina?

> Para fins da disciplina de IHC, será projetada uma interface que permita a **pessoas que trabalham na fazenda** utilizar **a câmera com detecção automática da praga e o mapa de pontos de risco** para **agir a tempo e no lugar certo**, no contexto de **inspeção da plantação em campo, muitas vezes sem internet e com pouco tempo disponível**.

## 7.5 Qual é a relação dessa interface com o TCC?

- [x] Já fazia parte do TCC.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | talvez | Ver rapidamente a situação geral da fazenda | **[H26]** |
| Configuração/parametrização | não | Não há necessidade clara identificada até agora | — |
| Entrada/upload/seleção de dados | sim | Capturar a foto do fruto para análise | **[F]** |
| Acompanhamento de processamento | sim | Saber que a foto está sendo analisada | **[F]** |
| Relatório/resultados | sim | Mostrar se foi encontrada a praga e onde | **[F]** |
| Histórico com busca/filtros | talvez | Ver inspeções e ocorrências anteriores | **[H21]** |
| Comparação de resultados | não | Não identificado como necessidade nesta etapa | — |
| Explicabilidade/detalhamento | talvez | Entender por que o app marcou aquele ponto | **[H27]** |
| Administração/configurações globais | não | Fora do foco do usuário de campo | — |
| CRUD de entidade do domínio | não | Não identificado como necessidade nesta etapa | — |
| Auditoria/logs | talvez | Registrar onde e quando cada inspeção ocorreu | **[H21]** |
| Alertas/ocorrências | sim | Avisar sobre pontos de risco na propriedade | **[F]** |
| Ajuda/documentação | talvez | Orientar quem não está acostumado com o app | **[H14]** |

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Identificar a praga de forma mais rápida e simples que a inspeção manual | A inspeção manual é lenta, cansativa e pode falhar | Pessoas que trabalham na fazenda | **[F]** |
| Saber onde estão os pontos de risco na propriedade | Hoje não há registro visual organizado dos focos | Dono/gestor da fazenda | **[H16]** |

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | Tirar uma foto do fruto com a câmera | Saber se há sinal da praga | alta |
| F02 | Ver o resultado da análise de forma simples | Decidir se precisa agir | alta |
| F03 | Ver os pontos de risco em um mapa da propriedade | Priorizar onde agir | média |

## 9.3 Tecnologias/restrições já definidas no TCC

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Aplicativo precisa funcionar sem internet | Falta de sinal no campo | Interface não pode depender de conexão em tempo real |
| Resultado precisa aparecer rápido, quase na hora | Facilitar decisão em campo | Necessário feedback visual imediato, sem espera longa |

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H14 | As pessoas da fazenda têm pouca familiaridade com aplicativos técnicos | Define o quanto a interface precisa ser simples | Entrega 3/7 |
| H16 | O dono/gestor é quem acompanha a evolução do problema na propriedade | Define quem realmente usaria o mapa de risco | Entrega 3/7 |
| H21 | Existe necessidade de guardar histórico das inspeções | Pode justificar uma tela de histórico | Entrega 5/7 |

Registrar em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | Um sistema que detecta automaticamente a praga por foto e mostra onde estão os pontos de risco na propriedade |
| O TCC já previa interface? | Sim, um aplicativo com câmera e um mapa |
| Quem é o usuário prioritário de IHC? | Pessoas que trabalham na fazenda (pragueiros, dono/gestor, trabalhadores rurais) |
| O que ele precisa alcançar? | Saber rápido se há praga e onde agir |
| Qual problema/atividade será estudado? | A inspeção dos frutos e a decisão de onde agir |
| Como isso acontece hoje? | De forma manual, com lupa e sem apoio de tecnologia |
| Qual é o contexto de uso? | Campo aberto, sol, pouca internet, pouco tempo por planta |
| Que interface/recorte será explorado? | Captura da foto, resultado da detecção e mapa de pontos de risco |
| Como a interface se relaciona ao TCC? | Já fazia parte do TCC |
| Quais pontos ainda são hipóteses? | H14, H16, H21 |

### Delimitação

**Dentro do escopo de IHC:** captura da foto, exibição do resultado e visualização do mapa de risco
**Fora do escopo de IHC:** treinamento do modelo, comparação entre arquiteturas, infraestrutura de servidor
**Dentro do escopo formal do TCC:** todo o pipeline de detecção, dataset e geolocalização
**Interface da disciplina será implementada no TCC?** não definido

---

# 12. Como esta entrega alimenta as próximas

- **Entrega 2:** verifica mercado, concorrentes e interfaces profissionais representativas.
- **Entrega 3:** detalha perfis e contexto.
- **Entrega 4:** aprofunda situações problemáticas.
- **Entrega 5:** modela tarefas centrais.
- **Entrega 6:** experimenta alternativas em baixa fidelidade.
- **Entrega 7:** investiga hipóteses com dados.
- **Entrega 8:** define restrições e metas de usabilidade.
- **Entregas 9–11:** transformam o recorte em modelo de interação e protótipo.
- **Entregas 12–14:** avaliam a interface construída na disciplina.

---

# 13. Relação com INOVA e comunicação do projeto

1. **Problema/atividade humana:** Hoje, encontrar uma praga muito pequena na plantação de laranja depende de inspeção manual, lenta e sujeita a falhas.
2. **Contribuição técnica do TCC:** Um sistema que usa a câmera do celular e inteligência artificial para detectar a praga automaticamente e marcar onde estão os pontos de risco.
3. **Como uma pessoa poderia utilizar essa contribuição:** Tirando uma foto do fruto com o celular e vendo na hora, em um mapa simples, se e onde precisa agir na propriedade.

---

# Checklist de qualidade

- [ ] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [ ] A equipe declarou se o TCC já previa interface.
- [ ] Se não previa, foi derivado um usuário plausível e um objetivo de uso.
- [ ] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [ ] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [ ] Usuários diretos e stakeholders foram diferenciados.
- [ ] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [ ] Objetivo do usuário não foi confundido com objetivo do projeto.
- [ ] Processo/problema atual foi descrito antes da solução.
- [ ] Existe situação concreta de uso/problema.
- [ ] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [ ] Mercado/alternativas existentes foram levantados inicialmente.
- [ ] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [ ] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [ ] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.
- [ ] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [ ] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [ ] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.
