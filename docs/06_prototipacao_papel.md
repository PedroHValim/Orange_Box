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

**Funcionalidade:** validação remota das detecções da IA e emissão do parecer técnico sobre o foco.<br>
**Persona:** P03 — Marcelo Fidalgo, agrônomo consultor.<br>
**Cenários/tarefas cobertos:** C03; T07 — validar (confirmar/rejeitar) as detecções da IA; T06 — localizar no histórico as inspeções do talhão (método M3, a partir da detecção); T05 — emitir parecer técnico sobre o foco (passos 1 a 5).<br>
**Objetivos principais:** levar o alerta direto ao foco, reunir foto original, local, data e histórico do ponto na mesma tela, separar "sinal da IA" de "confirmação humana", permitir pedir nova foto ao campo e registrar um parecer vinculado aos pontos avaliados e repassado ao gestor.

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

**Guilherme:**

- **Alertas/ocorrências:** pedidos de parecer e detecções novas por propriedade atendida.
- **Resultados:** pontos com detecção do talhão em mapa, com situação de cada um (pendente, confirmado, rejeitado, aguardando nova foto).
- **Explicabilidade/detalhamento:** foto original ampliável, data, hora, árvore, localização e avaliação da IA.
- **Histórico/comparação:** detecções anteriores do mesmo ponto e do talhão, com filtro de período.
- **Encaminhamento e registro:** veredito por detecção, pedido de nova foto ao campo, área de aplicação, parecer e repasse ao gestor.

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
| Guilherme | PF03 | Validar as detecções do foco, consultando o histórico do ponto — T07 e T06 (M3). | Só focos confirmados por humano devem entrar no dimensionamento da área [H07]; hoje Marcelo recebe fotos soltas, sem local nem histórico (C03). |
| Guilherme | PF04 | Dimensionar a área, registrar o parecer e repassá-lo ao gestor — T05 (passos 3, 4 e 5). | O erro relatado no C03 (aplicar em área maior que a afetada) ocorre na delimitação da área, e o parecer hoje se perde em mensagens soltas. |
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
| A01 | Pedidos de parecer (vindos de G04) e detecções novas, agrupados por propriedade e talhão, com quantidade de pontos pendentes. | Abrir pedido → A02 (direto no talhão do foco); buscar no histórico → A05. |
| A02 | Mapa do talhão com os pontos com detecção, a situação de cada um (pendente, confirmado, rejeitado, aguardando nova foto) e marca nos pontos que já tiveram detecção antes. Contagem de pontos por situação. | Selecionar ponto → A03; ver histórico do talhão → A05; emitir parecer → A06; encerrar revisão → A01 (progresso salvo). |
| A03 | Detecção do ponto: foto original ampliável, data, hora, árvore, localização e, na mesma tela, as detecções anteriores do ponto. A avaliação da IA fica recolhida ("ver avaliação da IA") até Marcelo decidir abrir. Campo opcional de observação técnica. | Confirmar ou rejeitar → A02 (ponto marcado "validado por humano" e próximo pendente destacado); pedir nova foto → A04; ver histórico completo → A05; voltar → A02. |
| A04 | Pedido de nova foto: ponto e árvore já preenchidos, motivo (foto desfocada, outra face do fruto, frutos vizinhos) e prazo desejado. | Enviar → A02 (ponto "aguardando nova foto"; o pedido aparece na rota do trabalhador em P01); cancelar → A03. |
| A05 | Histórico de detecções em lista única, com filtros de período e talhão. Aberto a partir de A03 já filtrado pelo ponto (M3), de A02 pelo talhão (M1) ou de A01 sem filtro (M2). | Alterar filtros (permanece em A05); abrir detecção → A03; voltar → tela de origem. |
| A06 | Delimitação da área sobre o mapa, mostrando apenas os pontos confirmados; produto, dose e período em campos livres (o sistema só registra). Aviso quando ainda há pontos pendentes ou aguardando nova foto. | Continuar → A07; voltar → A02 para validar o restante. |
| A07 | Parecer: texto técnico, resumo da área, pontos vinculados listados automaticamente e destinatário (gestor). | Enviar → A08; voltar → A06. |
| A08 | Situação do parecer: "registrado" e "entregue ao gestor" mostrados separadamente. | Tentar novamente após falha; voltar → A01. |

**Caminho principal:** A01 → A02 → A03 → A02 (repete por ponto) → A06 → A07 → A08. Os desvios A03 → A05 → A03 (histórico, T06) e A03 → A04 → A02 (nova foto) cobrem as tarefas opcionais e a terceira saída do veredito no CTT T07.<br>
**Erros e retornos:** encerrar a revisão a qualquer momento mantém os vereditos já registrados; foto insuficiente leva ao pedido de nova foto em vez de forçar confirmar ou rejeitar; pontos pendentes não bloqueiam o parecer, mas geram aviso em A06; falha no envio mantém o parecer registrado para nova tentativa.

**Informações importantes:** distinguir "detectado pela IA" de "validado por humano" em todas as telas. Ocultar a avaliação da IA até Marcelo pedir é uma decisão a testar, por causa do possível viés de confirmação apontado no CTT T07.

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

**Situação:** pendente, após desenhar as telas.<br>
**Condutor:** Guilherme.<br>
**Participante:** a definir (pessoa que não participou da elaboração das telas).<br>
**Data da simulação:** a definir.

**Roteiro:** pedir que a pessoa, no papel de agrônomo consultor, abra o pedido de parecer recebido, diga quantos pontos do talhão ainda precisam ser avaliados, abra um ponto, diga se ele já teve detecção antes, decida entre confirmar, rejeitar ou pedir nova foto e explique por quê, peça uma nova foto de um ponto com imagem ruim, delimite a área de aplicação e envie o parecer ao gestor.

| Observação | Tela/ação | Evidência | Consequência para o design |
|---|---|---|---|
| A verificar: chegada direta ao foco. | A01/A02 — abrir o pedido e encontrar os pontos pendentes. | Registrar se a pessoa procura o talhão ou já reconhece os pontos pendentes no mapa. | Revisar o agrupamento dos alertas e as marcas de situação no mapa. |
| A verificar: uso do histórico na mesma tela. | A03 — dizer se o ponto já teve detecção. | Registrar se a pessoa usa o histórico da própria tela ou vai para A05. | Ajustar o destaque do histórico do ponto. |
| A verificar: momento de consultar a avaliação da IA. | A03 — veredito. | Registrar se a pessoa abre a avaliação da IA antes ou depois de decidir, e se sente falta dela. | Decidir se a avaliação da IA fica visível desde o início. |
| A verificar: diferença entre pendente e aguardando nova foto. | A02/A04 — pedir nova foto. | Registrar como a pessoa descreve o ponto após o pedido. | Revisar legendas e mensagens de estado. |
| A verificar: diferença entre registrado e entregue. | A08 — enviar o parecer. | Registrar se a pessoa sabe se o parecer chegou ao gestor. | Revisar mensagens de envio. |

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
