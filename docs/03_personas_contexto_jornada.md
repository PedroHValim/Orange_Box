# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 09/09/2026 
**Status:** 🟨 em andamento
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Atenção a projetos técnicos

Em TCCs sem interface original, a persona pode representar um **profissional que se apropria da contribuição técnica**: DBA, analista, cientista de dados, administrador, pesquisador, técnico, operador, gestor ou especialista de domínio.

Não escolha um perfil apenas porque “parece combinar” com a tecnologia. Explique **qual objetivo esse perfil teria e qual parte da contribuição do TCC produziria valor para ele**. Se ainda for hipótese, mantenha como hipótese/proto-persona a validar.

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

### Persona P01 — Jaime Carteiro

**Autor(a):** Pedro Henrique Ferreira Valim - 24.123.048-1
**Tipo:** primária  
**Base de evidências:** entrevista / observação   
**Hipóteses da Entrega 1 relacionadas:** {{H01, H02 ou —}}

![Persona P01](../assets/03_personas/persona_p01.svg)

| Campo | Descrição |
|---|---|
| contexto relevante | Figura com responsabilidade de gestão em uma fazenda (Dono/Gerentes/etc). |
| Ocupação/papel | Dono da Fazenda |
| Conhecimento do domínio | Administrativo |
| Experiência tecnológica | Pouco |
| Objetivos | Entender pontos de infestações para tomadas de decisões |
| Necessidades | Obter dados que reflitam pontos de infestações de praga |
| Dores/frustrações | Dependência do profissional 'pragueiro' para detecção e mapeamento de pragas.  |
| Motivadores | Falta de autonomia na detecção de pragas e monitoramento de pontos de infestações. |
| Restrições/acessibilidade | Falta de conhecimento para identificação de praga aumentada quando falamos de um software que não enfrenta dificuldades 'humanas'. |
| Ambiente típico de uso | Fazenda e escritório |
| Comportamentos relevantes | Administrar e observar as métricas apontadas pelo aplicativo, gerando insights de níveis macro. |

**Decisões de design influenciadas por P01:**

- Interface com características 'clean' e objetivas.
- Diferentes visões de mapas e pontos de infestações.
- Menu lateral de métricas e dados mais especificados sobre os resultados obtidos em campo.

> Repita para P02, P03... Cada integrante deve produzir ao menos uma persona.

### Síntese das personas

Explique diferenças entre os perfis e qual persona é prioritária. Evite personas duplicadas que só mudam nome/foto.

## 2. Mapa de empatia — equipe

**Persona escolhida:** {{P01}}  
**Justificativa:** {{por que esse perfil é relevante}}

![Mapa de empatia](../assets/03_personas/mapa_empatia.svg)

Documente também em texto: o que vê; ouve; diz/faz; pensa/sente; dores; ganhos. Diferencie **evidência** de **hipótese**.

## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | {{...}} | {{...}} |
| Tarefas | {{...}} | {{...}} |
| Equipamentos | {{...}} | {{...}} |
| Ambiente físico | {{...}} | {{...}} |
| Ambiente social/organizacional | {{...}} | {{...}} |
| Papéis/permissões/governança | {{...}} | {{...}} |
| Volume de dados/histórico | {{...}} | {{...}} |

## 4. Jornada do usuário — equipe

**Persona:** {{P01}}  
**Objetivo da jornada:** {{...}}  
**Início e fim da jornada:** {{...}}

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

> A jornada pode incluir etapas **antes, durante e depois** do uso do produto. Não transforme a jornada em lista de telas.

## Síntese

Quais necessidades e objetivos devem obrigatoriamente aparecer nos cenários e nas tarefas seguintes?

## Checklist

- [ ] Existe pelo menos uma persona por integrante.
- [ ] As personas não são apenas diferenças demográficas superficiais.
- [ ] Está claro o que é dado real e o que é hipótese/proto-persona.
- [ ] A persona não “validou por ficção” uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência.
- [ ] Objetivos e dores têm consequência para o design.
- [ ] Contexto de uso está coerente com a Entrega 1.
- [ ] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica.
- [ ] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes.
- [ ] Jornada possui etapas, dores e oportunidades e não é apenas wireflow.
- [ ] IDs das personas foram adicionados à rastreabilidade.
