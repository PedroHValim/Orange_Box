# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 19/08/2026
**Status:** 🟩 concluída
**Responsabilidade:** 1 solução consolidada por equipe

> **Nota sobre esta versão (revisada após feedback do professor):** a classificação `[F]`/`[H]`/`[?]` foi auditada item a item. Afirmações sobre comportamento de usuários, benefícios esperados e necessidades ainda não investigadas foram rebaixadas para hipótese (`[H]`), recebendo IDs novos a partir de `H23`; os IDs de fatos remanescentes foram mantidos (por isso há lacunas na sequência `F`). Para eliminar a colisão de identificadores, usamos prefixos distintos: **`F`** = fatos, **`H`** = hipóteses, **`A`** = atividades e **`FN`** = funcionalidades (antes `F01`–`F03` na seção 9.2). O ID `H01` do exemplo do enunciado (abaixo) é apenas ilustrativo.

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
- [x] outro: {{...}}.

**Descrição:** Utilizaremos visão computacional para a detecção do ácaro da leprose, a partir de um dataset desenvolvido pelo grupo com imagens do ácaro.

**Resultados efetivamente produzidos pelo TCC (marcados acima):** (1) o dataset de imagens do ácaro e sua análise; (2) o modelo de detecção treinado; (3) o estudo comparativo entre arquiteturas (YOLO26n, YOLO26s, YOLOv8n) e do protocolo de captura; (4) a aplicação móvel com detecção embarcada e geolocalização.

**Não marcados, por serem meios e não resultados:** algoritmo (o treinamento usa algoritmos existentes), biblioteca/API/framework (apenas utilizados), infraestrutura/backend (o processamento é local, no dispositivo) e componente embarcado/IoT (o smartphone é a plataforma de execução do modelo, o que não torna o TCC um projeto de IoT).

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [x] Sim, a interface já faz parte do TCC.
- [x] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [x] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** Está previsto ter um sistema visual para que o usuário final possa, a partir de um dispositivo mobile, capturar a imagem do fruto, obter a detecção do ácaro e utilizar o sistema de geolocalização para registrar o local da ocorrência em campo.

**Divisão de responsabilidade entre pessoa e sistema (a ser confirmada):** o TCC prevê detecção **automática** pela visão computacional; portanto, entendemos que a pessoa **captura** a imagem e o sistema **detecta e marca** o ácaro (a "marcação" da ocorrência é feita pelo sistema, não desenhada manualmente pelo usuário). Permanecem **em aberto** [?]: se a pessoa precisa confirmar ou corrigir a detecção, e se existe validação humana antes de uma ocorrência alimentar o mapa (ver H27).

> Esta resposta serve para separar o compromisso do TCC do projeto da disciplina. Mesmo quando a opção for **não**, a equipe irá definir uma interface para exercitar IHC.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

Detecção de ácaros da leprose em laranjas.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

**Problema humano / da atividade (domínio):**

- **[F01]** Dificuldade de detecção do ácaro da leprose em citros: praga muito pequena, inspeção visual com lupa, esforço e cobertura limitada da amostragem (fonte: TCC).

**Lacuna científica/técnica (necessária para viabilizar o TCC, mas não é um problema do usuário):**

- **[F02]** Não existir um dataset com ácaros de citros (fonte: TCC).

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

Nosso TCC permite detectar o ácaro da leprose através de visão computacional e prover um sistema de geolocalização para o usuário final.

## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

> Os itens abaixo são **benefícios esperados** da solução. Só poderão ser confirmados com evidência de uso; por isso são hipóteses, não fatos.

- **[H23]** Trabalhadores rurais sem a especialização de um "pragueiro" conseguiriam realizar a detecção com apoio do aplicativo.
- **[H24]** A detecção assistida exigiria menor esforço físico do que a inspeção manual com lupa.
- **[H25]** A geolocalização auxiliaria o gerenciamento de infestações em campo.
- **[H01]** Disponibilização do dataset do ácaro (contribuição técnica prevista no TCC).

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

- **[F06]** O TCC justifica a escolha do smartphone por sua alta capilaridade, baixo custo relativo e suposta facilidade de operação pelo produtor rural no campo (fonte: TCC). Isso é uma **decisão formal do TCC** sobre o dispositivo, e não evidência de quem, de fato, usará a interface.
- **[H26]** Os perfis que poderiam interagir diretamente são pessoas diferentes, com atividades distintas: (a) quem **executa a inspeção** em campo (pragueiro ou trabalhador rural treinado) e (b) quem **acompanha e decide** o manejo (dono/gestor, possivelmente com o agrônomo). Não assumimos que "qualquer pessoa da fazenda" seja usuária direta; isso precisa ser investigado (ver seção 10).

## 2.2 Quem poderia usar, configurar, administrar, operar, interpretar ou tomar decisões a partir da contribuição técnica?

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| **Inspetor de campo** (pragueiro ou trabalhador rural que percorre a plantação) | Provável usuário direto da captura e do resultado da detecção | Percorre a plantação, observa os frutos (hoje com lupa) e, na solução, capturaria a imagem e veria o resultado | **[F07]** O TCC descreve a inspeção por pessoa treinada e justifica o smartphone para uso em campo. **[H26]** Se a mesma pessoa que inspeciona usaria o aplicativo ainda precisa ser confirmado |
| **Responsável pelo manejo** (dono/gestor; possivelmente agrônomo) | Possível usuário do acompanhamento espacial e decisor da intervenção | Interpretaria as ocorrências e decidiria se, onde e quando aplicar o produto | **[H04]/[H21]** Quem decide e quem usaria o mapa não foi confirmado |

**Atores do desenvolvimento do TCC (não são, por esse motivo, usuários ou stakeholders da interface):**

| Papel | Participação na pesquisa | Relação com a interface |
|---|---|---|
| Agrônomo da propriedade parceira | **[F08]** Definiu, com a equipe, o período de coleta de dados | Pode vir a ser stakeholder relevante da solução, mas isso depende do seu papel real no processo de inspeção/manejo — **[?]** a investigar |
| Equipe técnica/pesquisadores (autores) | **[F09]** Treinam e avaliam o modelo | Desenvolvedores; **não** são usuários da interface do projeto de IHC |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Trabalhadores que aplicam o produto de controle no campo (quando não são os mesmos que usam o app) | Passam a aplicar o produto apenas em pontos específicos, em vez de na fazenda toda | Não | **[H02]** Consequência provável da aplicação localizada, ainda não confirmada com essas pessoas |

> Stakeholders excessivamente indiretos (empresas compradoras, consumidor final, vizinhança/meio ambiente) foram **removidos da tabela** por não ajudarem a tomar decisões de IHC. Permanece como contexto apenas que o TCC cita a importância econômica da citricultura **[F10]** e a redução de impacto ambiental como benefício esperado **[F11]**.

## 2.4 Que características desses perfis podem influenciar a interação?

- **[H28]** As pessoas da fazenda usam celular no dia a dia, mas não necessariamente têm prática com aplicativos técnicos (a decompor em: que aplicativos usam, com que frequência, que tarefas fazem sem ajuda, que vocabulário conhecem — ver H20).
- **[F13]** O trabalho de campo é feito ao ar livre, muitas vezes com pouco ou nenhum sinal de internet (fonte: TCC).
- **[F14]** Quanto mais tempo demora para perceber o problema, maior o prejuízo (fonte: TCC).
- **[H03]** É provável que nem todos tenham o mesmo nível de leitura/familiaridade com tecnologia, então a interface precisa ser simples e visual.
- **[?]** Ainda não sabemos o nível real de conhecimento digital dessas pessoas nem se há alguma necessidade especial de acessibilidade.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

**Propósito organizacional (resultado desejado da atividade agrícola) — [F15]:** proteger a produção de laranja, evitando que a praga se espalhe e agindo antes que o prejuízo seja grande.

Esse propósito é amplo demais para orientar a interação. Os objetivos concretos, por papel, são:

| Papel | Objetivo que precisa alcançar na atividade | Status |
|---|---|---|
| Inspetor de campo | Saber se há sinal da praga no fruto que está inspecionando e registrar essa ocorrência | **[H29]** A confirmar na investigação |
| Responsável pelo manejo | Compreender onde estão as ocorrências para decidir se, onde e quando intervir | **[H21]** A confirmar na investigação |

"Usar a câmera", "ver o mapa" ou "usar IA" são **meios** de interação, não objetivos.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Verificar os frutos em busca de sinais da praga | Inspetor de campo (pragueiro/trabalhador treinado) | Alta — precisa ser repetida com frequência | **[F16]** O trabalho descreve a inspeção como atividade recorrente |
| A02 | Decidir onde e quando aplicar o produto de controle | Responsável pelo manejo (dono/gestor; agrônomo?) | Média — depende do resultado da inspeção | **[H04]** Ainda não confirmado quem exatamente toma essa decisão no dia a dia |
| A03 | Acompanhar se o problema está se espalhando pela propriedade | Responsável pelo manejo (a confirmar) | Contínua, ao longo do tempo | **[H05]** Ainda não confirmado como esse acompanhamento é feito hoje |

## 3.3 Qual atividade parece mais frequente? Por quê?

**[F17]** A verificação dos frutos (A01), porque precisa ser repetida várias vezes ao longo do ano para não deixar a praga passar despercebida.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

**[H06]** Decidir onde aplicar o produto de controle (A02) parece a mais crítica: se for mal feita, o produtor gasta dinheiro à toa em áreas sem problema ou deixa a praga se espalhar em áreas que precisavam de atenção.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje?

**Até encontrar a praga — [F18]:** hoje a verificação é feita por uma pessoa treinada, que percorre a plantação a pé e observa os frutos com uma lupa, sem apoio de tecnologia.

**Depois que a praga é encontrada — lacuna de conhecimento.** O TCC descreve a busca visual, mas não o que acontece em seguida. Todos os pontos abaixo são `[?]` e devem guiar a investigação (Entregas 3 e 7):

- [?] A ocorrência é anotada? Onde (papel, planilha, mapa, WhatsApp, memória, sistema agrícola)? Que informação é registrada?
- [?] Como a posição é identificada hoje (árvore, linha, talhão, área, outra referência do domínio)? Qual unidade faz sentido para a decisão?
- [?] A quem a ocorrência é comunicada e como? Há confirmação por outro profissional?
- [?] Quem reúne os resultados de diferentes inspeções e como são consolidados?
- [?] Quem decide a intervenção e com base em quais informações?

Enquanto essas respostas não existirem, a inspeção individual está bem justificada, mas o mapa e a decisão de manejo ainda são **hipótese de trabalho** (H21).

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

**[F19]** A praga é muito pequena e difícil de enxergar, o processo é cansativo e demorado, e não é possível checar todos os frutos, então parte da plantação fica sem cobertura.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

**[H07]** Provavelmente: se há sinais da praga, em quais pontos da plantação, com que intensidade e se a situação exige ação imediata ou pode esperar a próxima inspeção.

## 4.4 O que acontece quando a atividade falha ou o resultado é interpretado incorretamente?

**[F20]** A praga continua se espalhando sem ser percebida, atinge mais plantas e o prejuízo na safra aumenta.

## 4.5 Conte uma situação concreta.

**[H08]** Um trabalhador percorre a plantação em um dia de sol forte, verificando fruto por fruto com uma lupa. Depois de algumas horas, cansado, ele passa mais rápido pelos últimos pés de laranja. Um foco pequeno da praga passa despercebido nessa área e, semanas depois, quando é notado, já afetou várias árvores vizinhas, gerando perda de produção que poderia ter sido evitada com uma detecção mais cedo.

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Descrição do processo manual no trabalho | Mostra que a inspeção hoje depende inteiramente de uma pessoa treinada e de uma lupa | Não traz relatos diretos de trabalhadores ou donos de fazenda |
| Dados sobre erro de amostragem citados no trabalho | Mostra que o método manual pode errar bastante quando não é bem aplicado | Vem de uma fonte do setor, não de teste direto com os usuários do nosso projeto |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

**[F21]** No meio da plantação, durante a inspeção dos frutos, ao ar livre.

## 5.2 Em quais dispositivos/equipamentos?

**[F22]** Smartphone com câmera.

## 5.3 Existem condições físicas relevantes?

- **[F23a]** Ambiente ao ar livre e pouca ou nenhuma internet (fonte: TCC).
- **[H30]** Sol forte, calor, pessoa caminhando entre as árvores e pouco tempo disponível por planta são condições prováveis de interação, mas ainda não foram observadas.
- **[?]** Condições reais de captura: iluminação, posição do fruto, movimentação, uso de lente macro, manipulação simultânea do celular.

## 5.4 Existem fatores sociais ou organizacionais?

**[H04]** Não necessariamente quem faz a inspeção no campo é quem decide o que fazer com o resultado (ex.: trabalhador informa, dono/gestor decide). Não há evidência direta na documentação do TCC; precisa ser confirmado com pessoas da fazenda.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

**[H09]** Sim, provavelmente: saber onde já foi inspecionado e onde já houve problema antes ajuda a acompanhar a evolução ao longo do tempo, mas isso não foi confirmado com os usuários.

## 5.6 Um erro pode produzir consequência relevante? Qual?

**[F25]** Sim: não perceber a praga a tempo, ou agir no lugar errado, pode fazer o problema se espalhar e aumentar o prejuízo na safra.

---

# 6. Entendendo mercado e alternativas existentes

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Inspeção visual com lupa | Pessoa treinada na fazenda | Encontrar sinais da praga nos frutos | **[F26]** Descrito como o método atual no trabalho |

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

**[?]** Ainda não foi levantado no trabalho; existem de forma geral aplicativos de identificação de pragas e doenças em plantas por foto, mas não é confirmado se algum é voltado para essa praga específica.

## 6.3 Quais interfaces profissionais esse público já conhece?

**[H10]** Provavelmente aplicativos simples do dia a dia, como câmera do celular, mensagens e aplicativos de previsão do tempo — ainda não confirmado.

## 6.4 O que essas soluções parecem fazer bem?

**[H11]** São simples e já fazem parte da rotina dessas pessoas.

## 6.5 O que parecem fazer mal, dificultar ou não atender?

**[H12]** Não são feitas para esse problema específico e não ajudam a decidir onde agir dentro da fazenda.

## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

**[H13]** Fotos, mapas simples, alertas e ícones grandes e fáceis de entender.

---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Caminho escolhido

**Caminho A — TCC já possui interface.** O trabalho já prevê um aplicativo com câmera que detecta a praga e mostra o resultado, além de geolocalização/mapeamento dos focos. Para a disciplina, o recorte é organizado em dois fluxos distintos:

- **Fluxo 1 — Inspeção (recorte principal, melhor fundamentado):** capturar foto → ver resultado da detecção → registrar a ocorrência.
- **Fluxo 2 — Acompanhamento espacial e decisão (hipótese de trabalho, não solução congelada):** consultar a distribuição das ocorrências para decidir onde agir. Será mantido apenas na medida em que a investigação (H21, H22) demonstrar quem o usa e para qual decisão. A capacidade técnica de gerar um mapa não é, por si, evidência de que o usuário precise dele.

## 7.2 Qual perfil será priorizado no projeto de IHC?

**Inspetor de campo** — a pessoa que percorre a plantação e inspeciona os frutos (pragueiro ou trabalhador rural treinado para a atividade).

**Por que esse perfil foi escolhido?** Pela **atividade** que será estudada (inspeção, A01), que é a mais frequente **[F17]** e a mais bem documentada **[F18]**–**[F19]**, e não apenas por ser quem segura o celular. O **responsável pelo manejo** (dono/gestor/agrônomo) permanece como **perfil secundário**, a ser diferenciado do inspetor e investigado a partir da atividade A02/A03; não será fundido ao inspetor em uma única persona.

## 7.3 Qual objetivo desse usuário será priorizado?

**Objetivo prioritário (inspetor de campo):** conseguir saber, durante a inspeção, se há sinal da praga no fruto e registrar a ocorrência (H29).

**Objetivo do perfil secundário (responsável pelo manejo), a investigar:** compreender a distribuição das ocorrências para priorizar uma ação (H21). Os dois objetivos pertencem a papéis possivelmente distintos e não são reunidos numa única frase.

## 7.4 Que interface será explorada na disciplina?

> Para fins da disciplina de IHC, será projetada uma interface que permita ao **inspetor de campo** utilizar **a câmera com detecção automática da praga** para **saber se há sinal da praga no fruto e registrar a ocorrência**, no contexto de **inspeção da plantação em campo, com pouca ou nenhuma internet**; a visualização espacial das ocorrências para o responsável pelo manejo será explorada como hipótese de trabalho, condicionada à investigação de H21 e H22.

## 7.5 Qual é a relação dessa interface com o TCC?

- [x] Já fazia parte do TCC.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | talvez | Ver rapidamente a situação geral da fazenda | **[H14]** |
| Configuração/parametrização | não | Não há necessidade clara identificada até agora | — |
| Entrada/upload/seleção de dados | sim | Capturar a foto do fruto para análise | **[F27]** |
| Acompanhamento de processamento | talvez | Saber que a foto está sendo analisada; o TCC informa processamento muito rápido (52 ms), então pode bastar feedback imediato da ação, sem etapa específica de espera | **[H31]** |
| Relatório/resultados | sim | Mostrar se foi encontrada a praga e onde | **[F29]** (resultado da detecção é parte do que o TCC produz) |
| Histórico com busca/filtros | talvez | Ver inspeções e ocorrências anteriores | **[H15]** |
| Comparação de resultados | não | Não identificado como necessidade nesta etapa | — |
| Explicabilidade/detalhamento | talvez | Entender por que o app marcou aquele ponto | **[H16]** |
| Administração/configurações globais | não | Fora do foco do usuário de campo | — |
| CRUD de entidade do domínio | não | Não identificado como necessidade nesta etapa | — |
| Auditoria/logs | talvez | Registrar onde e quando cada inspeção ocorreu | **[H17]** |
| Alertas/ocorrências | talvez | Avisar sobre pontos de risco na propriedade; necessidade ainda não demonstrada (o mapa pode existir sem alertas) | **[H32]** |
| Ajuda/documentação | talvez | Orientar quem não está acostumado com o app | **[H18]** |

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Identificar a praga de forma mais rápida e simples que a inspeção manual | A inspeção manual é lenta, cansativa e pode falhar | Pessoas que trabalham na fazenda | **[H33]** (benefício esperado; "mais simples" é resultado de qualidade de uso, a ser avaliado) |
| Saber onde estão os pontos de risco na propriedade | Hoje não há registro visual organizado dos focos | Dono/gestor da fazenda | **[H19]** |

## 9.2 Que ações o usuário deverá conseguir realizar?

> Os IDs de funcionalidades usam o prefixo **`FN`**, distinto dos fatos (`F`), hipóteses (`H`) e atividades (`A`).

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| FN01 | Tirar uma foto do fruto com a câmera | Saber se há sinal da praga | alta |
| FN02 | Ver o resultado da análise de forma simples | Decidir se precisa agir | alta |
| FN03 | Ver as ocorrências em um mapa da propriedade (hipótese de trabalho, depende de H21/H22) | Priorizar onde agir | média |

## 9.3 Tecnologias/restrições já definidas no TCC

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Aplicativo precisa funcionar sem internet | Falta de sinal no campo | Interface não pode depender de conexão em tempo real |
| Resultado precisa aparecer rápido, quase na hora | Facilitar decisão em campo | Necessário feedback visual imediato, sem espera longa |

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H20 | As pessoas da fazenda têm pouca familiaridade com aplicativos técnicos (decompor: quais apps usam, frequência, tarefas sem ajuda, vocabulário, dificuldades) | Define o quanto a interface precisa ser simples | Entrega 3/7 |
| H21 | O dono/gestor é quem acompanha a evolução do problema na propriedade e usaria o mapa | Define quem realmente usaria o mapa; pode ser interação distinta da captura | Entrega 3/7 |
| H22 | Existe necessidade de guardar histórico das inspeções (quem consulta, para qual decisão, período, detalhe) | Pode justificar uma tela de histórico | Entrega 5/7 |
| H26 | Inspetor de campo e responsável pelo manejo são pessoas/papéis diferentes | Define usuário prioritário e personas | Entrega 3/7 |
| H27 | Pode ser necessário confirmação/correção humana da detecção antes de a ocorrência alimentar o mapa; falsos positivos e negativos têm consequências distintas | Define divisão pessoa × IA e a confiança no resultado | Entrega 4/5/7 |
| [?] | O que acontece depois que a praga é encontrada (registro, comunicação, consolidação, decisão, unidade espacial) | Justifica (ou não) o mapa e o fluxo de decisão | Entrega 3/4/7 |

Registrar em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | Um sistema que detecta automaticamente a praga por foto e registra a localização das ocorrências (mapeamento) |
| O TCC já previa interface? | Sim, um aplicativo com câmera e um mapa |
| Quem é o usuário prioritário de IHC? | Inspetor de campo (pragueiro/trabalhador treinado); responsável pelo manejo como perfil secundário a investigar |
| O que ele precisa alcançar? | Saber, durante a inspeção, se há sinal da praga no fruto e registrar a ocorrência |
| Qual problema/atividade será estudado? | A inspeção dos frutos (A01); decisão de manejo (A02/A03) como hipótese a investigar |
| Como isso acontece hoje? | De forma manual, com lupa e sem apoio de tecnologia |
| Qual é o contexto de uso? | Campo aberto, sol, pouca internet, pouco tempo por planta |
| Que interface/recorte será explorado? | Captura da foto e resultado da detecção (principal); mapa de ocorrências como hipótese de trabalho |
| Como a interface se relaciona ao TCC? | Já fazia parte do TCC |
| Quais pontos ainda são hipóteses? | H20, H21, H22, H26, H27 e o processo pós-detecção |

### Delimitação

**Dentro do escopo de IHC:** captura da foto e exibição do resultado (principal); visualização espacial das ocorrências (condicionada a H21/H22)
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
2. **Contribuição técnica do TCC:** Um sistema que usa a câmera do celular e inteligência artificial para detectar a praga automaticamente e registrar onde ocorreu.
3. **Como uma pessoa poderia utilizar essa contribuição:** Tirando uma foto do fruto com o celular e vendo na hora o resultado da detecção; a visualização das ocorrências em mapa é uma possibilidade ainda em investigação.

---

# Checklist de qualidade

- [x] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [x] A equipe declarou se o TCC já previa interface.
- [x] Se não previa, foi derivado um usuário plausível e um objetivo de uso.
- [x] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [x] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [x] Usuários diretos e stakeholders foram diferenciados.
- [x] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [x] Objetivo do usuário não foi confundido com objetivo do projeto.
- [x] Processo/problema atual foi descrito antes da solução.
- [x] Existe situação concreta de uso/problema.
- [x] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [x] Mercado/alternativas existentes foram levantados inicialmente.
- [x] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [x] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [x] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.
- [x] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [x] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [x] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.
