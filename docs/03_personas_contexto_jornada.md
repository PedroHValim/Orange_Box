# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 09/09/2026 
**Status:** 🟨 em andamento
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
| Pessoas que trabalham na fazenda | F | [F31] | incorporar |
| Dono/gestor da fazenda | F | [H19] | incorporar |
| Verificar os frutos em busca de sinais da praga | F | [F16] O trabalho descreve a inspeção como atividade recorrente | incorporar |
| Decidir onde e quando aplicar o produto de controle | F | [H04] Ainda não confirmado quem exatamente toma essa decisão no dia a dia | incorporar |
| Acompanhar se o problema está se espalhando pela propriedade | F | [H05] Ainda não confirmado como esse acompanhamento é feito hoje | incorporar |
| As pessoas da fazenda já usam celular no dia a dia, mas não necessariamente têm prática com aplicativos técnicos. | F | [F12] | incorporar |
| O trabalho de campo é feito ao ar livre, muitas vezes com pouco ou nenhum sinal de internet. | F | [F13] | incorporar |



## 1. Personas

### Persona P01, Jaime Carteiro

**Autor(a):** Pedro Henrique Ferreira Valim - 24.123.048-1
**Tipo:** primária  
**Base de evidências:** entrevista / observação   
**Hipóteses da Entrega 1 relacionadas:** {{H01, H02 ou —}}

![Persona P01](../assets/03_personas/persona_p01.svg)

| Campo | Descrição |
|---|---|
| contexto relevante | Pessoa com responsabilidade de gestão administrativa e estratégica da fazenda (dono, gerente etc.). |
| Ocupação/papel | Dono da Fazenda |
| Conhecimento do domínio | Administrativo |
| Experiência tecnológica | Pouco |
| Objetivos | Identificar os focos de infestação para embasar a tomada de decisão sobre manejo. |
| Necessidades | Ter acesso a dados confiáveis sobre os focos de infestação para orientar as ações de manejo. |
| Dores/frustrações | Dependência do profissional "pragueiro" para detecção e mapeamento de pragas. |
| Motivadores | Ganhar autonomia na detecção e no monitoramento de pragas, reduzindo a dependência de terceiros. |
| Restrições/acessibilidade | Baixo conhecimento técnico para identificar a praga por conta própria; depende da confiabilidade do sistema para validar os alertas recebidos. |
| Ambiente típico de uso | Escritório da propriedade, com visitas eventuais ao talhão para acompanhamento. |
| Comportamentos relevantes | Acompanha periodicamente as métricas e mapas do aplicativo para obter uma visão macro da propriedade e apoiar decisões estratégicas. |

**Decisões de design influenciadas por P01:**

- Interface com características 'clean' e objetivas.
- Diferentes visões de mapas e pontos de infestações.
- Menu lateral de métricas e dados mais especificados sobre os resultados obtidos em campo.

### Persona P02, Antônio Ferreira

**Autor(a):** Lucas Tonoli Cabral Duarte - 24.123.032-5  
**Tipo:** primária  
**Base de evidências:** hipótese (a validar em entrevista/observação de campo)  
**Hipóteses da Entrega 1 relacionadas:** H03, H09, H20

![Persona P02](../assets/03_personas/persona_p02.svg)

| Campo | Descrição |
|---|---|
| contexto relevante | Trabalhador rural que realiza a inspeção direta da plantação em busca de sinais da praga, sem formação técnica em agronomia. |
| Ocupação/papel | Trabalhador de campo / inspetor de pragas ("pragueiro") |
| Conhecimento do domínio | Alto conhecimento prático de campo (reconhece sinais visuais de praga por experiência), baixo conhecimento técnico/digital |
| Experiência tecnológica | Pouco |
| Objetivos | Verificar os frutos em busca de sinais da praga de forma rápida e confiável, sem depender de equipamento extra como lupa |
| Necessidades | Confirmação clara e imediata se há ou não sinal de praga; aplicativo funcionando mesmo sem internet |
| Dores/frustrações | Trabalho cansativo, repetitivo e demorado; sol forte; risco de deixar um foco de infestação passar despercebido no fim do dia |
| Motivadores | Realizar a inspeção corretamente sem se desgastar tanto; contribuir para evitar prejuízo na safra |
| Restrições/acessibilidade | Dificuldade de leitura extensa em tela pequena sob luz solar direta; pouca familiaridade com aplicativos técnicos |
| Ambiente típico de uso | A pé, entre as árvores, ao ar livre, sob sol forte, com pouco tempo disponível por planta e sem sinal de internet |
| Comportamentos relevantes | Tira a foto, olha o resultado na hora e segue para a próxima árvore; normalmente informa o achado, mas não é quem decide a ação a ser tomada |

**Decisões de design influenciadas por P02:**

- Botão de captura grande, de fácil acesso com uma mão, sem exigir múltiplos toques para tirar a foto.
- Resultado exibido com ícones/cores (ex.: sinal verde/vermelho) em vez de texto longo, para leitura rápida sob sol.
- Feedback em tempo real de enquadramento antes de tirar a foto, evitando capturas ruins.
- Funcionamento 100% offline, com sincronização automática quando houver conexão.
- Alto contraste visual para uso sob luz solar direta.
- Possível leitura em voz de instruções simples, para reduzir dependência de leitura em tela.
  
> Repita para P02, P03... Cada integrante deve produzir ao menos uma persona.

### Síntese das personas

P01 decide com base em dados agregados, no escritório, pouco exposto ao campo, P02 coleta a informação direto na plantação, sob sol, sem internet. São papéis complementares, não sobrepostos. A persona prioritária é P02, pois é quem realiza a interação de captura e recebe o resultado, fluxo definido como escopo de IHC na Entrega 1. P01 permanece como usuário secundário, do mapa e relatório.

## 2. Mapa de empatia — equipe

**Persona escolhida:** {{P01}}  
**Justificativa:** {{por que esse perfil é relevante}}

![Mapa de empatia](../assets/03_personas/mapa_empatia.svg)

Documente também em texto: o que vê; ouve; diz/faz; pensa/sente; dores; ganhos. Diferencie **evidência** de **hipótese**.

## 3. Contexto de uso, consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | P02 (trabalhador de campo/pragueiro) como usuário primário do fluxo de captura, P01 (dono/gestor) como usuário do mapa/relatório. | Interface precisa comportar dois níveis de uso, operacional e rápido em campo, e analítico em consulta no escritório. |
| Tarefas | A01, verificar frutos em busca de sinais da praga (P02), A02, decidir onde/quando aplicar controle (P01), A03, acompanhar disseminação do problema (P01). | Fluxo de captura precisa ser curto e direto, fluxo de mapa precisa sustentar comparação ao longo do tempo. |
| Equipamentos | Smartphone com câmera, eventualmente com lente macro acoplada. | Botões grandes e alcançáveis com uma mão, app deve tolerar variação de hardware entre dispositivos. |
| Ambiente físico | Campo aberto, sol forte, calor, deslocamento constante entre árvores, pouco tempo por planta. | Alto contraste, textos curtos, pouca dependência de leitura extensa. |
| Ambiente social/organizacional | Quem inspeciona nem sempre é quem decide a ação, há uma etapa de comunicação entre P02 e P01. | App precisa deixar claro o repasse da informação, como alerta visível para o gestor, sem exigir decisão do trabalhador de campo. |
| Papéis/permissões/governança | Ainda não confirmado se haverá diferenciação formal de perfil/login entre trabalhador e gestor. | Lacuna a investigar nas próximas entregas, relacionada a H21. |
| Volume de dados/histórico | Inspeções são recorrentes ao longo do ano, necessidade de histórico ainda é hipótese. | Justifica prototipar uma versão simples de histórico/mapa acumulado, relacionado a H09. |

---

## 4. Jornada do usuário, equipe

**Persona:** P02, Antônio Ferreira  
**Objetivo da jornada:** Inspecionar os frutos da propriedade e reportar, de forma confiável, se há sinais da praga em cada ponto percorrido.  
**Início e fim da jornada:** Começa ao chegar na propriedade para iniciar a rota de inspeção do dia, termina ao encerrar o percurso e sincronizar os dados quando há conexão.

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | Chega à propriedade e inicia o percurso de inspeção entre as árvores | Começar a rota do dia | Disposição no início, rotina já conhecida | Percurso longo pela frente, calor já presente | Indicar de forma simples por onde continuar, se houver histórico de rota | F21, H09 |
| 2 | Posiciona o smartphone sobre o fruto para capturar a imagem | Obter uma foto de qualidade suficiente para a detecção | Concentração, incerteza sobre o enquadramento | Dificuldade de manter distância/foco adequados sem apoio de lupa | Feedback visual em tempo real de enquadramento e distância antes da captura | F22, RC01, Entrega 2 |
| 3 | Aguarda o resultado da análise diretamente no app | Saber se há sinal da praga naquele ponto | Ansiedade breve pela resposta | Falta de internet poderia impedir o resultado | Processamento offline, resposta em poucos segundos | F13, RC04, Entrega 2 |
| 4 | Vê o resultado indicado na tela | Confirmar se precisa agir ou seguir em frente | Alívio ou atenção, conforme o resultado | Texto técnico demais poderia confundir | Resultado com ícone ou cor de leitura rápida | H03, RC02, Entrega 2 |
| 5 | Segue para a próxima árvore repetindo o processo | Cobrir o máximo de pontos possível no tempo disponível | Cansaço crescente ao longo do dia | Fadiga aumenta risco de pular pontos ou apressar a captura | Fluxo com o mínimo de toques entre foto e resultado | F18, F19, H08 |
| 6 | Ao final do percurso, ou quando há sinal, o app sincroniza os dados com o servidor central | Repassar os achados para quem decide | Sensação de dever cumprido | Não saber se a sincronização realmente ocorreu | Indicação clara de status de sincronização | F24, RC04, Entrega 2 |

---

## Síntese

- O fluxo de captura, feedback de enquadramento, resultado imediato e sincronização posterior precisa aparecer nos cenários e no modelo de tarefas da Entrega 5.
- O repasse de informação entre P02 e P01, já que quem inspeciona nem sempre decide, deve virar um requisito explícito de fluxo, não só de tela.
- As hipóteses H03, H09 e H21 seguem em aberto e devem orientar a investigação da Entrega 7.

## Checklist

- [x] Existe pelo menos uma persona por integrante.
- [x] As personas não são apenas diferenças demográficas superficiais.
- [x] Está claro o que é dado real e o que é hipótese/proto-persona.
- [x] A persona não "validou por ficção" uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência.
- [x] Objetivos e dores têm consequência para o design.
- [x] Contexto de uso está coerente com a Entrega 1.
- [x] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica.
- [ ] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes.
- [x] Jornada possui etapas, dores e oportunidades e não é apenas wireflow.
- [ ] IDs das personas foram adicionados à rastreabilidade.
