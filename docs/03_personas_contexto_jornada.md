# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 09/09/2026  
**Status:** 🟩 concluído  
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Atenção a projetos técnicos

Em TCCs sem interface original, a persona pode representar um **profissional que se apropria da contribuição técnica**: DBA, analista, cientista de dados, administrador, pesquisador, técnico, operador, gestor ou especialista de domínio.

Não escolha um perfil apenas porque "parece combinar" com a tecnologia. Explique **qual objetivo esse perfil teria e qual parte da contribuição do TCC produziria valor para ele**. Se ainda for hipótese, mantenha como hipótese/proto-persona a validar.

Também considere papéis diferentes quando houver tarefas distintas, por exemplo:

- operador que executa análises;
- administrador que configura e gerencia permissões;
- especialista que interpreta resultados;
- gestor que consulta relatórios e decide;
- auditor que revisa histórico.

## Entradas da Entrega 1

Antes de criar personas, retome os tipos de usuários, características relevantes, objetivos e hipóteses registradas na Entrega 1. A persona **não deve transformar uma hipótese inicial em fato por meio de uma história fictícia**.

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| Inspetor de campo (pragueiro/trabalhador treinado) | H | [F07] descreve a inspeção por pessoa treinada; quem usaria o app é [H26] | Incorporar como P02 (hipótese). |
| Dono/gestor da fazenda | H | [H19], [H21] não confirmados | Incorporar como P01 (proto-persona). |
| Verificar os frutos em busca de sinais da praga | F | [F16] O trabalho descreve a inspeção como atividade recorrente | Incorporar. |
| Decidir onde e quando aplicar o produto de controle | H | [H04] Ainda não confirmado quem exatamente toma essa decisão no dia a dia | Incorporar como hipótese. |
| Acompanhar se o problema está se espalhando pela propriedade | H | [H05] Ainda não confirmado como esse acompanhamento é feito hoje | Incorporar como hipótese. |
| As pessoas da fazenda usam celular no dia a dia, mas não necessariamente têm prática com aplicativos técnicos | H | [H28] / [H20] (antes [F12], rebaixado na Entrega 1) | Incorporar como hipótese. |
| O trabalho de campo é feito ao ar livre, muitas vezes com pouco ou nenhum sinal de internet | F | [F13] | Incorporar. |
| Agrônomo da propriedade participa da definição do período de coleta de dados, junto à equipe | F | [F08] (fato do processo de pesquisa do TCC; **não** prova papel operacional no manejo) | Incorporar apenas como proto-persona. |

> **Aviso geral desta entrega:** persona organiza o que já aprendemos sobre usuários; **não cria fatos novos**. Nenhuma entrevista ou observação com pessoas da fazenda foi registrada no repositório até esta data. Por isso, **P01, P02 e P03 são proto-personas a validar** (Entregas 7 e 14). Informações de identidade (idade, trajetória, rotina) são **ilustrativas e hipotéticas**, incluídas apenas por alterarem decisões de interface, e estão marcadas como tal.

## 1. Personas

### Persona P01 — Jaime Carteiro

**Autor(a):** Pedro Henrique Ferreira Valim - 24.123.048-1  
**Tipo:** secundária *(proto-persona a validar)*  
**Base de evidências:** hipóteses da Entrega 1; não há entrevista ou observação rastreada com Jaime  
**Hipóteses da Entrega 1 relacionadas:** H04, H05, H21

<img src="../assets/03_personas/persona_01.jpeg" alt="Persona P01" width="220">

*Imagem ilustrativa gerada por IA (thispersondoesnotexist.com); não retrata uma pessoa real.*

| Campo | Descrição |
|---|---|
| Contexto relevante | Pessoa com responsabilidade de gestão administrativa e estratégica da fazenda (dono, gerente etc.). |
| Ocupação/papel | Dono da fazenda. |
| Conhecimento do domínio | Administrativo. |
| Experiência tecnológica | Pouca. |
| Objetivos | Identificar os focos de infestação para embasar a tomada de decisão sobre manejo. |
| Necessidades | Ter acesso a dados confiáveis sobre os focos de infestação para orientar as ações de manejo. |
| Dores/frustrações | Dependência do profissional "pragueiro" para detecção e mapeamento de pragas. |
| Motivadores | Ganhar autonomia na detecção e no monitoramento de pragas, reduzindo a dependência de terceiros. |
| Restrições/acessibilidade | Baixo conhecimento técnico para identificar a praga por conta própria; depende da confiabilidade do sistema para validar os alertas recebidos. |
| Ambiente típico de uso | Escritório da propriedade, com visitas eventuais ao talhão para acompanhamento. |
| Comportamentos relevantes | Acompanha periodicamente as métricas e mapas do aplicativo para obter uma visão macro da propriedade e apoiar decisões estratégicas. |

**Decisões de design influenciadas por P01:**

- Interface objetiva.
- Diferentes visões de mapas e pontos de infestações.
- Métricas e dados mais específicos sobre os resultados obtidos em campo.

Essas possibilidades dependem da confirmação das tarefas de P01 e não representam requisitos já validados.

### Persona P02 — Antônio Ferreira

**Autor(a):** Lucas Tonoli Cabral Duarte - 24.123.032-5  
**Tipo:** primária  
**Base de evidências:** proto-persona baseada em restrições do TCC e hipóteses de rotina; não há entrevista ou observação rastreada com Antônio  
**Hipóteses da Entrega 1 relacionadas:** H03, H09, H20

<img src="../assets/03_personas/persona_02.jpeg" alt="Persona P02" width="220">

*Imagem ilustrativa gerada por IA (thispersondoesnotexist.com); não retrata uma pessoa real.*

| Campo | Descrição |
|---|---|
| Identidade e trajetória *(hipótese ilustrativa)* | Antônio tem aproximadamente 38 anos e trabalha há cerca de dez anos em atividades de campo. Aprendeu a inspecionar frutos com colegas mais experientes. Idade e trajetória servem para discutir experiência prática e devem ser verificadas, não apresentadas como perfil observado. |
| Contexto relevante | Trabalhador rural que realiza inspeção na plantação; ausência de formação técnica em agronomia é hipótese a verificar. |
| Ocupação/papel | Trabalhador de campo / inspetor de pragas ("pragueiro"). |
| Conhecimento do domínio | Alto conhecimento prático de campo (reconhece sinais visuais de praga por experiência); seu conhecimento técnico e digital precisa ser investigado. |
| Experiência tecnológica | **[H20]** Hipótese de uso de câmera e mensagens no celular e pouca prática com aplicativos técnicos; perguntar ao público, sem presumir baixa habilidade individual. |
| Objetivos | Verificar os frutos em busca de sinais da praga de forma rápida e confiável, sem depender de equipamento extra como lupa. |
| Necessidades | Entender o que a análise da imagem indica, distinguir ausência de sinal na foto de ausência de praga na área e saber o que fazer na dúvida; trabalhar em locais com conexão instável. |
| Dores/frustrações | Trabalho cansativo, repetitivo e demorado; sol forte; risco hipotético de deixar um foco passar despercebido no fim do dia. |
| Motivadores | Realizar a inspeção corretamente sem se desgastar tanto; contribuir para evitar prejuízo na safra. |
| Restrições/acessibilidade | Possível dificuldade de leitura extensa em tela pequena sob luz solar direta; familiaridade com aplicativos técnicos a investigar. |
| Ambiente típico de uso | A pé, entre as árvores, ao ar livre, com pouco tempo disponível por planta e possibilidade de ficar sem sinal de internet. |
| Comportamentos relevantes | A sequência “tirar foto → consultar resultado → seguir” é a interação proposta, não uma rotina observada. O modo real de informar achados e a autoridade para decidir o manejo ainda precisam ser confirmados. |

**Necessidades e alternativas de design a validar para P02:**

- Em campo, precisa obter uma foto utilizável; alvo de captura acessível e feedback de enquadramento são alternativas a testar (RC01).
- Precisa interpretar sinal e incerteza; texto curto, ícones e contraste são alternativas, sem depender só de verde/vermelho.
- Inferência offline vem do TCC. Sincronização e confirmação de recebimento por outra pessoa são hipóteses distintas (H04/H21).
- Áudio é alternativa a investigar com usuários, não requisito concluído (RC03).

Idade, trajetória, dificuldade com aplicativos e hábitos de Antônio são hipóteses de uma proto-persona, não resultados de coleta.

### Persona P03 — Marcelo Fidalgo

**Autor(a):** Guilherme Morais Escudeiro - 24.123.005-1  
**Tipo:** secundária *(proto-persona a validar)*  
**Base de evidências:** **fato** apenas de que um agrônomo participou da definição do período de coleta do TCC [F08]. Todo o restante (consultor remoto, recebe fotos soltas, valida focos, consulta histórico, recomenda produto/dose/período, depende dos dados do aplicativo) é **hipótese** não confirmada. Confirmar se esse papel existe no fluxo da propriedade e quais informações utiliza.  
**Hipóteses da Entrega 1 relacionadas:** H04, H07

<img src="../assets/03_personas/persona_03.jpeg" alt="Persona P03" width="220">

*Imagem ilustrativa gerada por IA (thispersondoesnotexist.com); não retrata uma pessoa real.*

| Campo | Descrição |
|---|---|
| Contexto relevante | Profissional de agronomia que poderia prestar consultoria técnica à propriedade; a atuação remota contínua é hipótese. |
| Identidade *(ilustrativa, hipótese)* | Cerca de 45 anos; engenheiro agrônomo com mais de 15 anos de atuação em citricultura; atende várias propriedades, com visitas pontuais; comunica-se por e-mail, planilhas e mensagens. Detalhes biográficos são hipóteses mantidas por afetarem o tipo de detalhe técnico e o canal de comunicação (H04, H07). |
| Ocupação/papel | Agrônomo consultor da propriedade *(papel operacional a confirmar)*. |
| Conhecimento do domínio | Alto conhecimento técnico/científico sobre pragas, fitossanidade e manejo de citros. |
| Experiência tecnológica | Uso de e-mail, planilhas e relatórios técnicos é uma hipótese de trabalho; verificar com profissionais reais. |
| Objetivos | Possivelmente validar tecnicamente focos de infestação e recomendar manejo adequado (produto, dose e período de aplicação). |
| Necessidades | Se atuar remotamente, poderá precisar de dados históricos e localizados das inspeções, com detalhe técnico suficiente para um parecer. |
| Dores/frustrações | **[H]** Poderia receber informações informais e incompletas do campo (relatos verbais e fotos sem contexto), dificultando diagnóstico e comparação. |
| Motivadores | Emitir recomendações embasadas, evitando aplicação incorreta ou desnecessária de defensivos. |
| Restrições/acessibilidade | Sua presença na propriedade, canais de trabalho e dependência dos dados do aplicativo não foram confirmados. |
| Ambiente típico de uso | Escritório ou propriedade, eventualmente consultando dados recebidos da equipe de campo *(hipótese)*. |
| Comportamentos relevantes | Consulta de histórico e distribuição espacial antes de emitir parecer é uma tarefa candidata, não comportamento observado. |

**Decisões de design influenciadas por P03 — candidatas a investigar:**

- Histórico de inspeções com filtro por período e localização (H22).
- Metadados de cada detecção (data, localização, imagem original) para eventual parecer remoto (H07).
- Diferenciação entre "sinal detectado pela IA" e "confirmação humana" (H27).

### Síntese das personas

P02 é o perfil priorizado para o fluxo de captura em campo. P01 pode atuar no acompanhamento e decisão, e P03 pode interpretar tecnicamente os dados. **A existência e a divisão exata desses papéis ainda precisam ser confirmadas.**

**Classificação:** interagir diretamente com o aplicativo não basta para definir uma persona primária. Foram considerados o foco prioritário do design, o objetivo atendido, as restrições de uso e a necessidade de decisões de interação próprias.

- **P02 — primária:** o fluxo de inspeção é o foco inicial e exige decisões específicas para o contexto de campo.
- **P01 — secundária:** acompanhamento e decisão dependem da validação do Fluxo B e de H21.
- **P03 — secundária / proto-persona:** a existência do papel operacional descrito não foi confirmada.

A equipe concentra inicialmente o design em P02, sem descartar os outros objetivos.

## 2. Mapa de empatia — equipe

**Persona escolhida:** P02, Antônio Ferreira  
**Legenda de evidência:** 🟦 **Fato** sustentado pelo TCC · 🟨 **Hipótese** inferida, não observada. A **tabela textual abaixo é o mapa de referência**; a imagem é ilustrativa.  
**Justificativa:** P02 executaria a captura e consultaria o resultado em campo, fluxo principal do escopo de IHC.

![Mapa de empatia — P02, Antônio Ferreira](../assets/03_personas/mapa_de_empatia.png)

| Dimensão | Descrição | Status |
|---|---|---|
| O que vê | 🟦 Frutos pequenos, com sinais de praga difíceis de enxergar a olho nu [F19]; plantação a céu aberto [F21]; falta de sinal de internet [F13]. 🟨 Sol forte incidindo sobre a plantação [H30]; colegas reconhecendo a praga "no olho"; propriedades vizinhas com prejuízo; celular usado para fotos e mensagens, não para aplicativos técnicos [H28]. | Fato: [F19], [F21], [F13]. Hipótese: restante. |
| O que ouve | 🟨 Orientação do dono/gestor sobre quais áreas priorizar; comentários de colegas sobre trechos percorridos ou focos; conversas e mensagens sobre pragas e perdas em outras propriedades. | Hipótese. |
| O que diz/faz | 🟦 Percorre a plantação a pé verificando frutos com lupa [F18]; smartphone com câmera é o dispositivo previsto [F22]. 🟨 Fotografaria frutos suspeitos e informaria achados a um responsável [H04]. | Fato: [F18], [F22]. Hipótese: restante. |
| O que pensa/sente | 🟦 O processo manual é cansativo e demorado e deixa parte da plantação sem cobertura [F19]. 🟨 Pode questionar se deixou uma árvore sem examinar, sentir cansaço ou preocupar-se com a interpretação do resultado [H08]. **Sentimentos são hipóteses, não conhecimento sobre trabalhadores reais.** | Fato: [F19]. Hipótese: restante. |
| Dores | 🟦 Trabalho cansativo e demorado [F19]; falta de internet [F13]; um erro pode agravar o prejuízo [F25]. 🟨 Risco de erro por fadiga [H08] e dificuldade com aplicativos técnicos [H03/H20]. | Fato: [F19], [F13], [F25]. Hipótese: restante. |
| Ganhos | 🟦 Agir cedo reduz prejuízo [F14]. 🟨 Resultado imediato sem lupa [H23], menor esforço [H24] e segurança de ter concluído e comunicado o percurso. | Fato: [F14]. Hipótese: restante. |

## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | P02 no fluxo de captura; P01 e P03 como perfis secundários a validar. | Diferenciar interação operacional rápida de eventual consulta gerencial ou técnica. |
| Tarefas | A01: verificar frutos (P02); A02: decidir manejo (P01, papel a confirmar); A03: acompanhar disseminação (P01/P03, necessidade a confirmar). | Priorizar o fluxo de captura; investigar antes de fixar mapa, histórico ou parecer. |
| Equipamentos | Smartphone com câmera, eventualmente lente macro acoplada. | Considerar captura e leitura em tela pequena e variações entre dispositivos. |
| Ambiente físico | Campo aberto, deslocamento entre árvores, variação de luz e pouco tempo por planta [F21], [F23]. Solo irregular, galhos, mãos sujas/suadas e efeito concreto do sol na tela são hipóteses a observar. | Testar contraste, legibilidade, controles e enquadramento em condições próximas às reais. |
| Ambiente social/organizacional | **[H04]** Pode existir separação entre quem inspeciona e quem decide. Rota orientada pelo gestor e troca de informação entre colegas não foram observadas. | Investigar destinatário, canal e conteúdo do repasse. |
| Papéis/permissões | Não foi confirmado se haverá perfis formais ou login distintos. | Não criar administração de usuários sem necessidade demonstrada. |
| Dados/histórico | Inspeções são recorrentes [F16]; necessidade de histórico e cobertura registrada é hipótese (H09/H22). | Verificar quais registros precisam ser guardados e recuperados. |

## 4. Jornada do usuário — equipe

**Persona:** P02, Antônio Ferreira  
**Objetivo:** inspecionar frutos e compreender/encaminhar os achados.  
**Recorte:** inicia antes da interface, passa pelo uso em campo e termina após o percurso. Rota, sincronização e confirmação de recebimento são **alternativas hipotéticas**; captura e inferência offline são apoiadas pelo TCC.

| Etapa | Situação/ação | Objetivo | Pensamento/emoção *(hipótese, salvo indicação)* | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| A — antes | Começa um ciclo; recebe uma área a verificar, caso essa organização se confirme. | Saber o que inspecionar. | “Preciso cobrir a área.” | Inspeção manual cansativa e cobertura limitada. | Mostrar a área combinada, se houver rota formal. | F18, F19, H04 |
| 0 | Recebe orientação inicial para utilizar a solução. | Aprender sem atrasar o trabalho. | Dúvida sobre o uso de novo aplicativo. | Familiaridade digital não conhecida. | Primeiro uso curto e visual, a testar. | H03, H20, H28 |
| 1 | Entra no pomar e inicia o percurso. | Começar a inspeção. | Atenção ao trabalho e ao tempo disponível. | Percurso extenso. | Indicar continuidade, se a necessidade de rota for confirmada. | F21, H09 |
| 2 | Posiciona o smartphone sobre o fruto. | Obter imagem utilizável. | “A foto está adequada?” | Foco e distância exigidos pelo alvo pequeno. | Apoio ao enquadramento; feedback dinâmico a validar. | F22, RC01 |
| 3 | Aguarda a análise no dispositivo. | Conhecer a indicação. | Dúvida durante a espera. | Conexão pode faltar. | Processamento offline e estado compreensível. | F13, RC04 |
| 4 | Lê o resultado. | Decidir se continua ou reconfirma. | Alívio ou dúvida conforme a indicação. | Texto técnico ou resultado ambíguo. | Texto curto, ícone e explicação de incerteza, a testar. | H03, RC02 |
| 5 | Passa ao próximo fruto/árvore ou repete a captura. | Prosseguir sem perder cobertura. | Possível cansaço. | Repetição e risco hipotético de pular pontos. | Poucos passos entre resultado e próxima captura. | F18, F19, H08 |
| 6 | Se houver repasse digital, aguarda o envio quando existir conexão. | Informar o achado. | “Foi recebido?” | Registro local pode ser confundido com envio. | Estados separados de “salvo” e “enviado”, a validar. | H04, RC04 |
| B — depois | Encerra o percurso e verifica o que ficou registrado ou pendente. | Evitar dúvida e retrabalho. | Segurança se conseguir reconhecer o trabalho concluído. | Cobertura e recebimento ainda não conhecidos. | Resumo e pendências, se necessidades confirmadas. | H04, H08, H21 |

## Síntese

- Captura, orientação para obter imagem utilizável e indicação no próprio dispositivo devem alimentar o cenário e os modelos de tarefas da Entrega 5.
- Repasse entre P02, P01 e P03, histórico, cobertura de rota e sincronização continuam hipóteses a investigar.
- O primeiro uso e a comunicação não punitiva de uma foto inadequada são alternativas para prototipação.
- H03, H09 e H21 permanecem abertas e orientam a coleta da Entrega 7.

## Checklist

- [x] Existe uma persona por integrante.
- [x] As personas possuem objetivos, tarefas e restrições relevantes para o design.
- [x] Fatos, hipóteses e proto-personas foram distinguidos.
- [x] A história fictícia não foi utilizada para validar hipóteses.
- [x] Objetivos e dores têm consequências para a interação.
- [x] O contexto é coerente com a Entrega 1.
- [x] A relação das personas com a contribuição técnica foi explicitada.
- [x] P02 foi priorizada com justificativa.
- [x] A jornada inclui antes, durante e depois, com dores e oportunidades.
- [x] P01, P02, P03 e seus vínculos foram registrados em `../RASTREABILIDADE.md`.
