# Entrega 6 — Prototipação em papel

**Data:** 11/10/2026<br>
**Status:** 🟨 em andamento<br>
**Responsabilidade:** 1 solução integrada por equipe

## Objetivo da atividade

Explorar ideias de interação em baixa fidelidade, seguindo o ciclo **construir → simular → observar → revisar**.

## 1. Escopo do protótipo

### Funcionalidade — Lucas

**Funcionalidade:** inspeção de frutos e repasse dos achados.<br>
**Persona:** P02 — Antônio Ferreira, trabalhador de campo/pragueiro.<br>
**Cenários/tarefas cobertos:** C02; T01 e T03 — inspecionar a rota e repassar os achados; T02 — verificar um fruto e encaminhar o resultado.<br>
**Objetivos principais:** facilitar a captura da foto, apresentar resultados claros, registrar o local e conferir a cobertura da rota e o envio dos registros.

### Funcionalidade — Guilherme

**Funcionalidade:** {{...}}<br>
**Personas:** {{...}}<br>
**Cenários/tarefas cobertos:** {{...}}<br>
**Objetivos principais:** {{...}}

### Funcionalidade — Pedro

**Funcionalidade:** revisão do resultado do ciclo, avaliação da evolução dos talhões e registro da decisão de manejo.<br> 
**Persona:** P01 — Jaime Carteiro, dono da fazenda.<br> 
**Cenários/tarefas cobertos:** C01; T09 — revisar o resultado do ciclo e decidir se confia nele; T08 — avaliar a evolução de um talhão entre ciclos; T04 — planejar o manejo do ciclo (passos 1, 2, 3, 4 e 5).<br> 
**Objetivos principais:** conferir a cobertura do ciclo antes dos resultados, mostrar onde estão os focos e como evoluem, dar ao gestor evidência que ele consiga avaliar sem conhecimento técnico, permitir pedir parecer ou reinspeção e registrar a decisão do ciclo.

## 1.1 Possíveis famílias de interface

**Lucas:**

- **Entrada de dados:** captura da foto com orientação de foco.
- **Acompanhamento de execução:** análise da imagem e cancelamento.
- **Resultados:** sinal suspeito, ausência de sinal na foto ou resultado inconclusivo.
- **Acompanhamento da rota e envio:** pontos registrados, pendências e situação do repasse.

**Guilherme:** {{...}}

**Pedro:**

- **Visão geral:** resumo do ciclo e cobertura da propriedade por talhão.
- **Alertas/ocorrências:** aviso de ciclo concluído.
- **Resultados:** talhões com focos, em mapa e em lista ordenada.
- **Explicabilidade/detalhamento:** fotos, grau de confiança e local de cada talhão.
- **Histórico/comparação:** evolução do talhão entre ciclos e última aplicação.
- **Encaminhamento e registro:** pedido de parecer ou reinspeção, decisão do ciclo e repasse.

## 2. Fluxos escolhidos

| Responsável | Fluxo | Tarefa/objetivo | Por que foi priorizado |
|---|---|---|---|
| Lucas | PF01 | Fotografar o fruto, interpretar e registrar o resultado — T02. | Tarefa frequente, sujeita a erros de captura e interpretação. |
| Lucas | PF02 | Conferir a rota e o envio dos achados — T01/T03. | Reduz dúvidas sobre pontos esquecidos e registros não enviados. |
| Guilherme | {{...}} | {{...}} | {{...}} |
| Pedro | PF05 | Revisar o resultado do ciclo, conferir a cobertura e decidir se confia — T09 (e T04, passos 1 e 2.3). | Sem a cobertura, o gestor não diferencia "sem praga" de "ninguém passou" [H09], e ele não valida a praga sozinho. |
| Pedro | PF06 | Avaliar a evolução de um talhão e registrar a decisão do ciclo — T08 e T04 (passos 2.2, 3, 4 e 5). | Decidir onde aplicar é a atividade mais crítica do gestor [H06] e depende de saber se a praga avança e se a última aplicação funcionou. |

## 3. Telas e estados

**Desenho do protótipo em papel:** pendente. As telas abaixo representam o planejamento.

### Funcionalidade — Lucas

| Tela | Conteúdo previsto | Controles e mudanças de estado |
|---|---|---|
| P01 | Rota do dia e pontos pendentes. | Iniciar inspeção → P02; revisar rota → P06. |
| P02 | Câmera com orientação de foco. | Fotografar → P03; ajustar foto inadequada; voltar → P01. |
| P03 | Análise da imagem sem internet. | Exibir resultado → P04; cancelar → P02. |
| P04 | Resultado suspeito, sem sinal na foto ou inconclusivo. | Salvar → P05; refazer foto → P02. |
| P05 | Confirmação do registro salvo e identificação do local. | Próximo fruto/árvore → P02; revisar rota → P06. |
| P06 | Pontos registrados e pendentes da rota. | Retomar inspeção → P02; encerrar indicando pendências → P07. |
| P07 | Situação do envio ao gestor. | Enviar quando houver conexão; tentar novamente após falha; voltar → P06. |

**Caminho principal:** P01 → P02 → P03 → P04 → P05 → P06 → P07.

**Erros e retornos:** foto inadequada exige ajuste; resultado inconclusivo permite refazer; falta de GPS permite identificar o local manualmente; falha no envio mantém os registros salvos para nova tentativa.

**Informações importantes:** distinguir “salvo no celular” de “enviado”. Ausência de sinal na foto não significa que toda a árvore esteja livre da praga.

![Protótipo](../assets/06_prototipos/prototipo_fluxo_01.svg)

### Funcionalidade — Guilherme

| Tela/estado | Conteúdo previsto | Controles e mudanças de estado |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

**Caminho principal:** {{...}}<br>
**Erros e retornos:** {{...}}

![Protótipo](../assets/06_prototipos/prototipo_fluxo_02.svg)

### Funcionalidade — Pedro

| Tela/estado | Conteúdo previsto | Controles e mudanças de estado |
|---|---|---|
| G01 | Resumo do ciclo concluído: data, quantos talhões foram inspecionados e quantos têm focos. | Ver cobertura → G02. |
| G02 | Cobertura do ciclo: talhões inspecionados e não inspecionados, bem diferenciados de "sem focos". | Pedir nova inspeção dos talhões não cobertos (confirma e permanece em G02); continuar → G03. |
| G03 | Talhões com focos, em mapa e em lista ordenada por gravidade e tendência. | Selecionar talhão → G04; encerrar revisão → G07; voltar → G02. |
| G04 | Detalhe do talhão no ciclo: fotos, grau de confiança em linguagem simples (sem números técnicos), local e aviso se a cobertura do talhão foi incompleta. | Aceitar como confiável, marcar para parecer do agrônomo ou pedir reinspeção → G05; ver evolução → G06; voltar → G03. |
| G05 | Confirmação da posição registrada para o talhão (confiável, parecer pedido ou reinspeção pedida). | Próximo talhão → G03; encerrar revisão → G07. |
| G06 | Evolução do talhão por ciclo (avançando, estável ou recuando), com a última aplicação marcada. Avisa quando algum ciclo comparado teve cobertura incompleta. | Ver cobertura dos ciclos comparados → G02; voltar → G04. |
| G07 | Decisão do ciclo: talhões com a posição registrada e escolha de onde e quando aplicar, com urgência. | Registrar decisão → G08; voltar → G03. |
| G08 | Confirmação da decisão registrada e do repasse a quem aplica o produto. | Repassar; tentar novamente após falha. |

**Caminho principal:** G01 → G02 → G03 → G04 → G05 → G03 (próximo talhão) → G07 → G08. O desvio G04 → G06 → G04 corresponde à avaliação da evolução (T08).<br>
**Erros e retornos:** talhão sem inspeção permite pedir nova inspeção em G02 sem sair da tela; cobertura incompleta aparece em G04 e G06 e impede que a comparação pareça conclusiva; a dúvida do gestor leva a "parecer do agrônomo" ou "reinspeção", e não bloqueia o fluxo; encerrar a revisão a qualquer momento mantém as posições já registradas; falha no repasse mantém a decisão salva para nova tentativa.

![Protótipo](../assets/06_prototipos/prototipo_fluxo_03.svg)

## 4. Simulação / walkthrough

A simulação deverá envolver uma pessoa que não participou da elaboração das telas. Um colega pode participar desta iteração formativa, sem substituir os participantes finais da Entrega 14.

### Funcionalidade — Lucas

**Situação:** pendente, após desenhar as telas.<br>
**Condutor:** Lucas.<br>
**Participante:** {{...}}<br>
**Data da simulação:** {{...}}

**Roteiro:** pedir que a pessoa fotografe um fruto, interprete o resultado, salve sem internet, confira a rota e verifique o envio quando a conexão retornar.

| Observação | Tela/ação | Evidência | Consequência para o design |
|---|---|---|---|
| A verificar: compreensão da captura. | P02 — fotografar ou ajustar a imagem. | Registrar dúvidas e pedidos de ajuda. | Revisar instruções conforme observado. |
| A verificar: interpretação do resultado. | P04 — salvar ou refazer. | Registrar como a pessoa explica o resultado. | Ajustar mensagens que causarem confusão. |
| A verificar: compreensão das pendências. | P06/P07 — conferir rota e envio. | Registrar se distingue pendente, salvo e enviado. | Revisar legendas e mensagens de estado. |

As observações reais serão preenchidas após a simulação.

### Funcionalidade — Guilherme

**Situação:** {{...}}<br>
**Condutor:** {{...}}<br>
**Participante:** {{...}}<br>
**Data da simulação:** {{...}}<br>
**Roteiro:** {{...}}

| Observação | Tela/ação | Evidência | Consequência para o design |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

### Funcionalidade — Pedro

**Situação:** pendente, após desenhar as telas.<br>
**Condutor:** Pedro.<br>
**Participante:** a definir (pessoa que não participou da elaboração das telas).<br>
**Data da simulação:** a definir.

**Roteiro:** pedir que a pessoa, no papel de dono da fazenda, abra o resumo do ciclo, diga quais talhões não foram inspecionados, escolha um talhão com foco, explique se confia no resultado e por quê, compare com o ciclo anterior, registre a posição do talhão e a decisão do ciclo e repasse a decisão.

| Observação | Tela/ação | Evidência | Consequência para o design |
|---|---|---|---|
| A verificar: diferença entre "sem focos" e "não inspecionado". | G01/G02 — conferir a cobertura. | Registrar como a pessoa descreve um talhão sem inspeção. | Revisar rótulos, cores e textos da cobertura. |
| A verificar: compreensão da confiança do resultado. | G04 — decidir se confia. | Registrar o que a pessoa usa para decidir (fotos, grau de confiança, local). | Ajustar a forma de mostrar evidência e confiança. |
| A verificar: leitura da evolução entre ciclos. | G06 — avaliar tendência e última aplicação. | Registrar se a pessoa conclui "avançando", "estável" ou "recuando" e se nota a cobertura incompleta. | Revisar a forma de mostrar a comparação e o aviso de cobertura. |
| A verificar: diferença entre registrada e repassada. | G08 — registrar e repassar. | Registrar se a pessoa sabe se a decisão chegou a quem aplica. | Revisar legendas e mensagens de estado. |

## 5. Alterações após a simulação

### Funcionalidade — Lucas

**Pendente:** preencher após o teste, relacionando cada alteração a uma dificuldade realmente observada.

| Antes | Problema | Depois | Justificativa |
|---|---|---|---|
| {{Elemento da versão testada}} | {{Dificuldade observada}} | {{Alteração realizada}} | {{Evidência que motivou a revisão}} |

### Funcionalidade — Guilherme

| Antes | Problema | Depois | Justificativa |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

### Funcionalidade — Pedro

| Antes | Problema | Depois | Justificativa |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

## Checklist

**Situação referente ao planejamento da parte de Lucas. A consolidação da equipe permanece pendente.**

- [x] O escopo planejado do protótipo cobre tarefas relevantes da Entrega 5.
- [x] Cada tela/estado planejado pode ser justificado por uma tarefa, decisão ou informação necessária.
- [x] O projeto não criou dashboard/CRUD/login apenas para parecer “completo”.
- [x] Telas/estados estão numerados e têm caminhos de navegação indicados na documentação.
- [ ] Há pelo menos uma simulação/walkthrough documentado.
- [ ] Críticas não foram apenas listadas: geraram decisão de revisão.
- [ ] O protótipo em papel foi elaborado e permanece em baixa fidelidade; detalhes visuais não mascaram problemas de fluxo.
