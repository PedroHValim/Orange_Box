# Entrega 5 — Análise de tarefas: HTA, GOMS e CTT

**Data:** {{04/10/2026}}  
**Status:** 🟨 em andamento  
**Responsabilidade:** cada integrante modela pelo menos 1 HTA, 1 GOMS e 1 CTT. As três técnicas podem abordar a mesma funcionalidade ou funcionalidades distintas, conforme a orientação da disciplina.

## Objetivo da atividade

Modelar tarefas importantes sob perspectivas complementares: decomposição hierárquica (HTA), estrutura de metas/métodos/operações (GOMS) e relações temporais entre tarefas (CTT). O diagrama deve ser acompanhado de interpretação textual.

## Para projetos cujo TCC não previa interface

Modele **tarefas humanas relacionadas ao uso da contribuição técnica**, e não a implementação interna do algoritmo. Exemplos de boas tarefas para análise:

- investigar uma consulta de baixo desempenho;
- configurar uma análise e selecionar parâmetros;
- submeter um dataset e verificar sua validade;
- acompanhar uma execução demorada;
- comparar dois resultados/modelos;
- interpretar uma recomendação e decidir se a aceita;
- localizar uma execução anterior usando busca/filtros;
- gerar e compartilhar um relatório;
- administrar papéis/permissões quando isso for parte do trabalho real;
- revisar um alerta e registrar uma decisão.

Um CRUD pode gerar tarefas relevantes, mas “cadastrar usuário” só merece modelagem se tiver significado no domínio (papéis, validações, riscos, permissões, dependências).

## Seleção das tarefas

| ID | Tarefa | Persona/cenário de origem | Frequência/criticidade | Autor responsável |
|---|---|---|---|---|
| T01 | Inspecionar a rota do dia e repassar os achados (HTA) | P02 / C02 | Frequência alta: a inspeção se repete ao longo do ano, em ciclos de cerca de 14 dias [F16], [F17]. Criticidade alta: um foco que passa despercebido continua se espalhando [F20], [F25] | Lucas Tonoli Cabral Duarte - 24.123.032-5 |
| T02 | Verificar um fruto e encaminhar o resultado (GOMS) | P02 / C02 | Frequência muito alta: repetida a cada fruto de cada árvore da rota [F16], [F17]. Criticidade alta: é onde o foco é detectado ou passa despercebido [F19], [F20] | Lucas Tonoli Cabral Duarte - 24.123.032-5 |
| T03 | Inspecionar a rota do dia e repassar os achados (CTT) | P02 / C02 | Frequência alta e criticidade alta, como em T01 | Lucas Tonoli Cabral Duarte - 24.123.032-5 |

> Priorize tarefas necessárias para que o usuário alcance objetivos centrais. Não desperdice a modelagem em ações triviais isoladas, como “clicar em login”, se o objetivo relevante é maior. Da mesma forma, não modele o funcionamento interno do algoritmo como se fosse uma tarefa humana.

---

## HTA — T01 Inspecionar a rota do dia e repassar os achados

**Autor(a):** Lucas Tonoli Cabral Duarte - 24.123.032-5

### Descrição da tarefa

Antônio (P02) recebe do dono as áreas que deve percorrer, caminha entre as árvores, verifica de três a cinco frutos por árvore e precisa saber, para cada fruto, se há sinal de praga. Quando há sinal, o achado precisa chegar a quem decide [F24]. **Início:** Antônio recebe a rota do dia. **Conclusão esperada:** todas as áreas combinadas foram percorridas e os achados foram repassados, com a certeza de que chegaram. **Contexto:** campo aberto, sol forte, pouco tempo por planta, pouca ou nenhuma internet [F23]. A tarefa é descrita no nível do que P02 faz ao usar a contribuição do TCC (celular com detecção), sem desenhar telas. Parte da sequência vem de hipóteses ainda não validadas com um pragueiro real ([H08], [H09]) e será confirmada na Entrega 7.

### Diagrama

![HTA T01](../assets/05_tarefas/hta_t01.svg)

### Decomposição e planos

| ID | Objetivo/operação | Plano/ordem | Problema ou decisão de design observada |
|---|---|---|---|
| 0 | Inspecionar a rota do dia e repassar os achados | 1 > 2 (repetir por árvore) > 3 | Quem inspeciona nem sempre decide [F24]: a tarefa só se completa quando o achado chega a quem decide |
| 1.2 | Deixar o celular pronto para fotografar | — | Pouca familiaridade com aplicativos técnicos [H20]: preparação mínima, sem atrasar a rota |
| 2.1 | Escolher os frutos da árvore | 3 a 5 frutos; ramos internos se não houver frutos adequados | Decisão do próprio pragueiro, que precisa lembrar quais árvores já cobriu [H09] |
| 2.2.1 | Posicionar o celular sobre o fruto | — | Sem a lupa, é preciso manter a distância certa com uma só mão, andando e sob sol forte [F23] |
| 2.2.2 | Conferir enquadramento e foco | Repetir 2.2.1–2.2.2 até ficar adequado | Principal ponto de erro: foto ruim leva a resultado ruim. Decisão: avisar sobre o enquadramento antes da captura |
| 2.2.3 | Acionar a captura | — | Fadiga e pouco tempo por planta [F19]: o mínimo de gestos possível |
| 2.3.1 | Aguardar o resultado | — | Sem internet [F13]: o resultado precisa vir sem depender de conexão e sem espera longa |
| 2.3.2 | Ler a indicação de sinal ou não sinal | — | Leitura sob luz solar direta em tela pequena [H03]: indicação curta e visual |
| 2.3.3 | Avaliar se confia no resultado | — | Antônio já tem dúvida entre ácaro e marca da casca (C02, Q2): decidir como o resultado comunica incerteza |
| 2.4.2 | Reconfirmar: refazer a captura ou pedir a um colega | Se a dúvida persistir após refazer, chamar colega | Custa tempo em campo: precisa ser rápido e não punir o erro |
| 2.4.3 | Avisar o dono e garantir o registro do local | Só quando há sinal | Hoje a foto e o aviso saem sem local preciso (C02, Q3; C03): o local não pode depender da memória nem de esforço extra |
| 3.1 | Conferir se cobriu as áreas combinadas | — | Hoje não há registro do percurso, e fica a dúvida "deixei passar um pé?" [H08], [H09] |
| 3.2 | Enviar os registros quando houver conexão | Condicionado à conexão | O envio não pode bloquear o trabalho nem exigir ação em campo |
| 3.3 | Confirmar que o envio ocorreu | — | Dúvida "será que chegou lá?" (jornada de P02, etapa 6): status de envio visível |

**Verificação do HTA:**

- O objetivo 0 representa uma meta do usuário? **Sim:** inspecionar e repassar com confiança, não "usar o app".
- As subtarefas são necessárias e suficientes? **Sim:** ficaram de fora a decisão de manejo (A02, do dono e do agrônomo) e o funcionamento interno da detecção.
- Os **planos** indicam ordem, alternativa, repetição ou condição? **Sim:** ordem (1 > 2 > 3), repetição (por fruto e por árvore), condição (2.4, 3.2) e alternativa (2.4.1, 2.4.2, 2.4.3).
- A decomposição parou em nível útil para projeto de interação? **Sim:** parou em posicionar, conferir, acionar, ler e decidir, sem descer a toques de tela.

---

## GOMS — T02 Verificar um fruto e encaminhar o resultado

**Autor(a):** Lucas Tonoli Cabral Duarte - 24.123.032-5

O modelo cobre o ciclo repetido a cada fruto (subtarefas 2.2 a 2.4 do HTA T01), onde estão as alternativas de execução e as decisões do usuário.

### Goal

`G0: Verificar um fruto e encaminhar corretamente o resultado`

- `G1: Obter uma imagem utilizável do fruto`
- `G2: Interpretar o resultado`
- `G3: Encaminhar o resultado`

### Métodos, operadores e regras de seleção

- **Method M1 (G1, captura direta):**
  - Operators: perceber o fruto e a luz; posicionar o celular sobre o fruto; perceber o feedback de enquadramento; acionar a captura.
- **Method M2 (G1, captura com ajuste):**
  - Operators: perceber que o enquadramento ou a luz está inadequado (reflexo, sombra, desfoque); ajustar ângulo ou distância, ou fazer sombra com o corpo ou a mão; perceber o feedback de enquadramento; acionar a captura.
- **Method M3 (G2, leitura direta):**
  - Operators: aguardar o resultado; perceber a indicação; decidir que confia nela.
- **Method M4 (G2, reconfirmação):**
  - Operators: perceber a dúvida; repetir G1 ou chamar um colega e mostrar o fruto e a tela; comparar com o que o colega vê; decidir.
- **Method M5 (G3, seguir adiante):**
  - Operators: decidir que não há sinal; deslocar-se até o próximo fruto ou árvore.
- **Method M6 (G3, avisar o dono):**
  - Operators: decidir que há sinal; avisar o dono (pessoalmente ou por mensagem); conferir que o local ficou registrado; seguir adiante.
- **Selection Rule SR1 (G1):** usar M1 quando o feedback indica enquadramento adequado de primeira; usar M2 quando há reflexo, sombra ou desfoque.
- **Selection Rule SR2 (G2):** usar M3 quando o resultado é claro e coerente com o que Antônio vê no fruto; usar M4 quando o resultado contradiz sua percepção ou ele fica em dúvida. *Hipótese a validar: refazer a captura uma ou duas vezes antes de chamar um colega.*
- **Selection Rule SR3 (G3):** usar M5 quando não há sinal; usar M6 quando há sinal confirmado.

> Não chame qualquer passo de “método”. Em GOMS, métodos são sequências alternativas capazes de atingir uma meta; regras de seleção explicam quando escolher entre eles.

**Interpretação:** o custo se concentra em M2 e M4, os caminhos em que Antônio perde tempo e atenção justamente quando está cansado e com pouco tempo por planta. Isso indica que o feedback de enquadramento (reduz o uso de M2) e a forma de comunicar incerteza (reduz idas e vindas em M4) são decisões de interação prioritárias. M6 mostra que o registro do local precisa acontecer sem esforço extra, ligando este modelo ao problema do C03. Não foram estimados tempos (KLM), apenas a estrutura de metas, métodos e regras.

---

## CTT — T03 Inspecionar a rota do dia e repassar os achados

**Autor(a):** Lucas Tonoli Cabral Duarte - 24.123.032-5

### Descrição

O modelo mostra a relação temporal entre as tarefas de Antônio e as do sistema ao longo da rota: preparar, inspecionar árvore a árvore, verificar cada fruto e repassar os achados. O diagrama está em dois níveis para ficar legível.

### Diagrama

![CTT T03](../assets/05_tarefas/ctt_t03.svg)


### Legenda e relações temporais usadas

| Operador/relação | Significado no diagrama | Exemplo no modelo |
|---|---|---|
| `>>` (habilitação) | A tarefa seguinte só começa quando a anterior termina | Analisar a imagem `>>` Exibir o resultado `>>` Interpretar o resultado |
| `[]` (escolha) | Apenas uma das alternativas é executada | Seguir adiante `[]` Reconfirmar `[]` Avisar o dono, conforme o resultado |
| `*` (iteração) | A tarefa se repete até a condição de parada | Inspecionar árvore (para cada árvore da rota); Verificar fruto (3 a 5 frutos por árvore) |
| `\|[]\|` (concorrência com troca de informação) | As tarefas acontecem ao mesmo tempo e uma alimenta a outra | Posicionar o celular `\|[]\|` Mostrar feedback de enquadramento |

**Tipos de tarefa (formato do nó):** hexágono = abstrata; retângulo = usuário; arredondado = sistema; estádio = interação.

Identifique, quando aplicável, tarefas de usuário, sistema, interação e tarefas abstratas. Verifique se concorrência, escolha, habilitação, desabilitação e repetição estão representadas corretamente segundo a notação adotada em aula.

**Interpretação:** três pontos merecem atenção no projeto de interação. Primeiro, posicionar o celular e receber o feedback de enquadramento acontecem juntos, e só depois a captura é habilitada. É aqui que se decide se a foto sai boa. Segundo, depois do resultado, Antônio escolhe entre seguir, reconfirmar ou avisar o dono, e essa escolha depende da leitura rápida e da confiança no resultado. Terceiro, o envio dos registros só ocorre se houver conexão, então a tarefa precisa fechar sem ele e Antônio só confirma o envio depois. Não há tarefa do dono ou do agrônomo neste modelo: elas aparecem nas tarefas de P01 e P03. O operador de desabilitação não se aplicou a esta tarefa.

---

## Síntese da equipe

Quais problemas de interação, oportunidades e requisitos apareceram a partir das modelagens? Quais tarefas irão para o protótipo e para o teste de usabilidade?

**Contribuição do Lucas (P02):**

- **Problemas de interação:** foto ruim por enquadramento sem apoio (2.2.2), dúvida sobre o resultado e como comunicá-la (2.3.3, 2.4.2), local do achado dependente da memória (2.4.3), dúvida sobre cobertura da rota e sobre o envio (3.1, 3.3).
- **Requisitos que emergiram:** feedback de enquadramento antes da captura; leitura rápida do resultado sob sol; funcionamento sem internet; registro automático do local; indicação clara de cobertura e de status de envio.
- **Para o protótipo e o teste de usabilidade:** o ciclo "Verificar fruto" (captura, resultado, encaminhamento) e o fechamento do percurso (cobertura e envio). A síntese final da equipe deve juntar isto com as tarefas de P01 e P03.

## Checklist

- [ ] Cada integrante produziu ao menos 1 HTA, 1 GOMS e 1 CTT.
- [ ] Cada artefato identifica autor e tarefa.
- [ ] Diagramas são legíveis e possuem fonte editável quando possível.
- [ ] HTA contém planos, não apenas árvore de tópicos.
- [ ] GOMS distingue Goals, Operators, Methods e Selection Rules.
- [ ] CTT usa operadores temporais e tipos de tarefa coerentes.
- [ ] Há texto explicando cada diagrama.
- [ ] Tarefas estão ligadas a cenários/personas na rastreabilidade.
- [ ] Em TCC técnico, as tarefas descrevem o que a pessoa faz com a contribuição/resultados, não passos internos do código.
- [ ] CRUDs, relatórios, filtros e atividades administrativas foram escolhidos por relevância ao objetivo do usuário.
