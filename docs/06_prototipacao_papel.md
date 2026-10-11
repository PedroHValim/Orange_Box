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

**Funcionalidade:** {{...}}<br>
**Personas:** {{...}}<br>
**Cenários/tarefas cobertos:** {{...}}<br>
**Objetivos principais:** {{...}}

## 1.1 Possíveis famílias de interface

**Lucas:**

- **Entrada de dados:** captura da foto com orientação de foco.
- **Acompanhamento de execução:** análise da imagem e cancelamento.
- **Resultados:** sinal suspeito, ausência de sinal na foto ou resultado inconclusivo.
- **Acompanhamento da rota e envio:** pontos registrados, pendências e situação do repasse.

**Guilherme:** {{...}}

**Pedro:** {{...}}

## 2. Fluxos escolhidos

| Responsável | Fluxo | Tarefa/objetivo | Por que foi priorizado |
|---|---|---|---|
| Lucas | PF01 | Fotografar o fruto, interpretar e registrar o resultado — T02. | Tarefa frequente, sujeita a erros de captura e interpretação. |
| Lucas | PF02 | Conferir a rota e o envio dos achados — T01/T03. | Reduz dúvidas sobre pontos esquecidos e registros não enviados. |
| Guilherme | {{...}} | {{...}} | {{...}} |
| Pedro | {{...}} | {{...}} | {{...}} |

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
| {{...}} | {{...}} | {{...}} |

**Caminho principal:** {{...}}<br>
**Erros e retornos:** {{...}}

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

**Situação:** {{...}}<br>
**Condutor:** {{...}}<br>
**Participante:** {{...}}<br>
**Data da simulação:** {{...}}<br>
**Roteiro:** {{...}}

| Observação | Tela/ação | Evidência | Consequência para o design |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

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
