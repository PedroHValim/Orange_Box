# Entrega 9 — Modelo conceitual e design centrado na comunicação

**Data:** 01/11/2026<br>
**Status:** 🟨 em andamento — partes de Lucas e de Pedro preparadas; parte de Guilherme e consolidação da equipe pendentes.<br>
**Responsabilidade:** soluções individuais, com consolidação da equipe para mapa de objetivos e esquema de signos.

## Objetivo da atividade

Passar dos cenários de problema para uma concepção da interação, explicitando objetivos, tópicos de conversa, falas e signos compreensíveis aos usuários.

## Transformando resultados técnicos em conceitos compreensíveis

No fluxo do trabalhador, termos como “inferência”, “metadados EXIF” e “sincronização” serão comunicados como **analisando a foto**, **local do registro** e **situação do envio**. A interface distinguirá um sinal apontado pela IA de uma confirmação humana.

## 1. Cenários de interação

### CI01 — Revisão do ciclo e decisão do manejo por talhão

**Autor(a):** Pedro — 24.123.048-1<br>
**Origem:** cenário de problema C01, “Planejamento do manejo sem visão consolidada da propriedade ao longo dos ciclos”.

Jaime é dono de uma fazenda de citros e cuida da parte administrativa e estratégica da propriedade. Ele conhece pouco a praga e depende do pragueiro para saber se há infestação e onde. A propriedade conta com poucos pragueiros, e a inspeção se repete em ciclos de cerca de 14 dias. **Quando o ciclo termina, o sistema avisa Jaime no escritório e mostra um resumo com a data do ciclo, quantos talhões foram inspecionados e quantos têm focos. Ele não precisa esperar o relato do pragueiro.**

Antes, Jaime recebia uma impressão geral (“tem uns focos no fundo da fazenda”), sem um quadro do que aconteceu em cada talhão. **Agora ele abre a cobertura do ciclo, onde os talhões inspecionados, os não inspecionados e os que têm focos aparecem com texto, símbolo e cor. Um talhão “não inspecionado” nunca é apresentado como “sem focos”; se algum talhão ficou de fora, Jaime pode pedir nova inspeção sem sair da tela.** Se o pragueiro não pôde passar em alguma área, Jaime passa a saber disso na hora, e não depois.

Como não sabe identificar a praga sozinho, Jaime não tem como conferir o que vê. **Ao abrir um talhão com focos, encontra as fotos, o local e um grau de confiança em linguagem simples, sem números técnicos. O sistema não diz se a praga existe: Jaime decide em quem confiar e registra sua posição para o talhão, que pode ser “confiável”, “parecer do agrônomo” ou “reinspeção”. A dúvida não bloqueia a revisão; ele pode encerrá-la a qualquer momento, e as posições já registradas permanecem salvas.**

Jaime não sabia se a infestação estava crescendo, estável ou diminuindo, nem se a última aplicação funcionou. **Pela evolução do talhão, vê os ciclos mais recentes indicados como “avançando”, “estável” ou “recuando”, com a última aplicação marcada. Se algum ciclo comparado teve cobertura incompleta, o sistema avisa, para que ele não conclua que a praga recuou quando, na verdade, ninguém passou.**

No fim, Jaime planejava o manejo com base em impressão. **Agora registra a decisão do ciclo (onde e quando aplicar, e com que urgência) a partir das posições de cada talhão. O sistema ordena os talhões por gravidade e tendência, mas não recomenda produto, dose nem prioridade. A decisão aparece como “registrada” e só passa a “repassada” quando chega a quem aplica o produto; se o repasse falhar, a decisão continua salva e Jaime pode tentar de novo.**

Os trechos em **negrito** descrevem a interação proposta. Eles ainda precisam ser avaliados com usuários; não são observações de uso real. A tela de cada passo corresponde a G01–G08 da Entrega 6, ainda não desenhadas em papel nem simuladas.

### Diferenças relevantes — CI01

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Aviso e resumo do ciclo concluído. | Jaime não depender do relato do pragueiro para saber que o ciclo acabou. | C01; HTA T04, passo 1.1 (Entrega 5). |
| Cobertura que separa “inspecionado”, “não inspecionado” e “com focos”. | Evitar confundir “sem alerta” com “ninguém passou”. | C01, Q5; CTT T09; hipótese H09. |
| Fotos e confiança em linguagem simples, com saídas “parecer do agrônomo” e “reinspeção”. | Jaime não valida a praga; precisa decidir em quem confiar. | Persona P01; HTA T04, passo 2.3; CTT T09. |
| Evolução por ciclo com última aplicação marcada e aviso de cobertura incompleta. | Responder se a praga avança e se a aplicação funcionou, sem conclusão enganosa. | C01, Q3; GOMS T08 (regra de verificar a cobertura); hipóteses H05 e H09. |
| Ordenação por gravidade apresentada como dado, não como recomendação. | Não invadir o papel do agrônomo (P03). | HTA T04, passo 3.1; fronteira ainda em aberto. |
| Estados distintos para decisão “registrada” e “repassada”. | A decisão precisa chegar a quem aplica, que pode não usar o sistema. | C01; hipótese H02; protótipo G08 (Entrega 6). |

### CI02 — Inspeção dos frutos e repasse dos achados

**Autor(a):** Lucas — 24.123.032-5<br>
**Origem:** cenário de problema C02, “Inspeção manual de frutos com lupa, sob fadiga e sem registro do percurso”.

Antônio recebe do gestor as áreas que deve percorrer e caminha entre as árvores do pomar. **No celular, abre a rota do dia e vê o próximo ponto planejado e os pontos que já possuem registro.** Em cada árvore, escolhe os frutos para inspeção. **Ao abrir a câmera, recebe uma orientação curta sobre distância, iluminação e foco; se a imagem estiver inadequada, pode ajustá-la antes de fotografar.**

O ácaro é pequeno e pode ser confundido com marcas da casca. **Depois da foto, o aplicativo informa que está analisando a imagem no próprio celular, mesmo sem internet. O resultado aparece como “sinal suspeito”, “nenhum sinal nesta foto” ou “resultado inconclusivo”. Antônio pode ouvir o resultado e refazer a foto quando estiver em dúvida. A mensagem deixa claro que o resultado da IA não equivale à confirmação da praga.**

Quando encontra um sinal suspeito, Antônio precisa avisar quem decide o que fazer. **Ao salvar o achado, o aplicativo associa foto, data, hora e local disponível. Se o GPS não fornecer a posição, Antônio identifica talhão, linha e árvore manualmente; o registro fica marcado como “local manual, sem coordenadas”.** Ele continua a inspeção sem esperar conexão.

Ao final do percurso, Antônio costumava depender da memória para saber se deixou algum ponto passar. **Agora confere os pontos planejados com e sem registro. Se encerrar com pendências, a rota continua identificada como incompleta. Os achados ficam “salvos no celular” até que haja conexão; depois o aplicativo mostra “enviando” e “enviado ao gestor”, ou permite tentar novamente em caso de falha. “Enviado” não significa que o gestor já leu o registro.**

Os trechos em **negrito** descrevem a interação proposta. Eles ainda precisam ser avaliados com usuários; não são observações de uso real.

### Diferenças relevantes — CI02

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Rota com pontos planejados e registrados. | Reduzir a dúvida sobre locais esquecidos. | C02; HTA T01 e CTT T03 da Entrega 5. |
| Orientação de foco e possibilidade de refazer a foto. | Prevenir resultado baseado em imagem inadequada. | C02; GOMS T02; análise de interfaces da Entrega 2. |
| Resultado em linguagem curta, com alternativa inconclusiva. | Evitar que uma indicação da IA seja entendida como diagnóstico definitivo. | Dúvida do trabalhador em C02; GOMS T02. |
| Local automático ou identificação manual. | Evitar repasse baseado apenas na memória quando não houver GPS. | C02; HTA T01, etapa de comunicar o achado. |
| Estados distintos para salvo, enviando e enviado. | Permitir trabalhar offline e verificar se o repasse ocorreu. | Jornada de P02 da Entrega 3; CTT T03. |

### CI03 — {{título do cenário de Guilherme}}

**Autor(a):** Guilherme — {{matrícula}}<br>
**Origem:** cenário de problema C03.

{{Inserir cenário de interação. Marcar em negrito os trechos alterados em relação a C03.}}

## 2. Design centrado na comunicação

**Nome do cenário:** CI02 — inspeção dos frutos e repasse dos achados.

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| Iniciar a inspeção > escolher o próximo ponto | `U: Qual ponto devo inspecionar agora?` / `D: Próximo ponto: talhão, linha e árvore; estes pontos já têm registro e estes estão pendentes.` | Orientar a continuidade sem afirmar que todas as árvores do talhão foram examinadas. |
| Capturar o fruto > ajustar a imagem | `U: A foto está boa para analisar?` / `D: Ajuste a distância e o foco antes de fotografar.` | Prevenir captura inadequada. |
| Analisar a foto > aguardar | `U: O que está acontecendo?` / `D: Analisando a foto no celular.` | Informar o estado da tarefa sem depender da internet. |
| Entender o resultado > sinal suspeito | `U: É a praga?` / `D: Sinal suspeito nesta foto; precisa de confirmação.` | Comunicar a indicação da IA e seu limite. |
| > nenhum sinal na foto | `U: Posso considerar a árvore livre da praga?` / `D: Nenhum sinal nesta foto; isso não garante que toda a árvore esteja livre.` | Evitar uma conclusão além da imagem analisada. |
| > resultado inconclusivo | `U: E se eu não tiver certeza?` / `D: Não foi possível concluir. Refaça a foto ou salve para conferir depois.` | Permitir recuperação sem forçar uma decisão. |
| Registrar o achado > identificar o local | `U: Onde este fruto foi encontrado?` / `D: Local obtido por GPS; se não estiver disponível, informe talhão, linha e árvore.` | Manter o contexto do achado e indicar quando o local foi informado manualmente. |
| Repassar os achados > conferir o envio | `U: O gestor já recebeu?` / `D: Salvo no celular; aguardando conexão / enviando / enviado ao gestor / falha no envio.` | Diferenciar armazenamento local, envio e falha. |

**Convenção:** `U` = usuário; `D` = preposto do designer/sistema.

**Design centrado na comunicação — Pedro**

**Nome do cenário:** CI01 — revisão do ciclo e decisão do manejo por talhão.

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| Saber do ciclo > aviso e resumo | `U: O ciclo terminou?` / `D: Ciclo concluído em [data]: X talhões inspecionados, Y com focos.` | Dispensar o relato do pragueiro e informar o alcance do ciclo. |
| Conferir a cobertura > talhão não inspecionado | `U: Todos os talhões foram vistos?` / `D: Não inspecionado: talhão [nome]. Isso não significa que esteja livre da praga.` | Impedir que “não inspecionado” seja lido como “sem focos”. |
| > pedir nova inspeção | `U: E o que falta?` / `D: Pedir nova inspeção deste talhão?` | Dar uma saída sem sair da tela de cobertura. |
| Avaliar o talhão > evidência e confiança | `U: Posso confiar neste resultado?` / `D: Confiança [alta/média/baixa]. Veja as fotos e o local; o sistema não confirma a praga.` | Mostrar a evidência e o limite da indicação, em linguagem simples. |
| Registrar a posição > escolher a saída | `U: Eu não sei se é a praga.` / `D: Aceitar como confiável, pedir parecer do agrônomo ou pedir nova inspeção.` | Permitir a dúvida sem bloquear a revisão. |
| Acompanhar a evolução > ler a tendência | `U: A praga está se espalhando?` / `D: Neste talhão: avançando / estável / recuando. Última aplicação marcada no ciclo [data].` | Responder à pergunta do gestor com o histórico, sem exigir memória. |
| > cobertura incompleta | `U: Posso concluir que recuou?` / `D: Atenção: o ciclo [data] não cobriu todo o talhão. A comparação pode não ser confiável.` | Evitar conclusão enganosa na comparação. |
| Decidir o manejo > registrar a decisão | `U: Onde e quando aplico?` / `D: Talhões em ordem de gravidade. Escolha onde, quando e com que urgência aplicar.` | Apresentar dados sem recomendar produto, dose nem prioridade. |
| Repassar a decisão > conferir o repasse | `U: Quem vai aplicar já sabe?` / `D: Decisão registrada / repassada a [quem aplica] / falha no repasse: tentar novamente.` | Diferenciar registro, repasse e falha, mantendo a decisão salva. |

Os rótulos de confiança (“alta”, “média” e “baixa”) são uma proposta inicial, a testar com usuários.

**Design centrado na comunicação — Guilherme:** {{inserir tópicos, falas e signos de CI03}}.

## 3. Mapa de objetivos

### Mapa individual — Lucas

**Objetivo principal:** inspecionar a rota e repassar os achados com confiança.

- **O01 — Inspecionar os pontos da rota**
  - Identificar o próximo ponto planejado.
  - Distinguir pontos com registro de pontos pendentes.
- **O02 — Obter uma foto analisável**
  - Ajustar enquadramento e foco.
  - Fotografar ou refazer a captura.
- **O03 — Entender o resultado da foto**
  - Distinguir suspeita, ausência de sinal na foto e resultado inconclusivo.
  - Decidir entre seguir, refazer ou guardar para conferência.
- **O04 — Registrar o achado e seu local**
  - Salvar foto, resultado, data e hora.
  - Usar o local obtido ou identificar o ponto manualmente.
- **O05 — Confirmar o repasse dos registros**
  - Verificar pendências da rota.
  - Distinguir registro salvo de registro enviado.
  - Recuperar-se de falha no envio.

### Mapa individual — Pedro

**Objetivo principal:** decidir o manejo do ciclo com base em dados confiáveis sobre cada talhão.

- **O06 — Saber o que o ciclo cobriu**
  - Receber o aviso e o resumo do ciclo.
  - Distinguir talhão sem focos de talhão não inspecionado.
  - Pedir nova inspeção dos talhões não cobertos.
- **O07 — Avaliar o resultado de um talhão**
  - Ver fotos, local e confiança.
  - Decidir em quem confiar, sem validar a praga.
- **O08 — Registrar a posição de cada talhão**
  - Aceitar como confiável.
  - Pedir parecer do agrônomo ou reinspeção.
- **O09 — Acompanhar a evolução do talhão**
  - Ler a tendência entre ciclos.
  - Ver a última aplicação e o aviso de cobertura incompleta.
- **O10 — Decidir o manejo do ciclo**
  - Escolher onde, quando e com que urgência aplicar.
  - Usar a ordem por gravidade como dado, não como recomendação.
- **O11 — Confirmar o repasse da decisão**
  - Distinguir decisão registrada de repassada.
  - Recuperar-se de falha no repasse.

**Mapa individual — Guilherme:** {{inserir mapa e IDs sem repetir os objetivos acima}}.

**Mapa consolidado da equipe:** pendente. Ao reunir os três mapas, verificar se termos como “achado”, “detecção”, “foco” e “ponto” estão sendo usados para conceitos diferentes antes de unir objetivos.

![Mapa consolidado](../assets/09_modelo_conceitual/mapa_objetivos.svg)

### Dicionário de objetivos

| ID | Objetivo | Persona(s) | Cenário(s) | Prioridade |
|---|---|---|---|---|
| O01 | Inspecionar os pontos da rota. | P02 | CI02 | Alta |
| O02 | Obter uma foto analisável. | P02 | CI02 | Alta |
| O03 | Entender o resultado da foto. | P02 | CI02 | Alta |
| O04 | Registrar o achado e seu local. | P02 | CI02 | Alta |
| O05 | Confirmar o repasse dos registros. | P02 | CI02 | Alta |
| O06 | Saber o que o ciclo cobriu. | P01 | CI01 | Alta |
| O07 | Avaliar o resultado de um talhão. | P01 | CI01 | Alta |
| O08 | Registrar a posição de cada talhão. | P01 | CI01 | Alta |
| O09 | Acompanhar a evolução do talhão. | P01 | CI01 | Alta |
| O10 | Decidir o manejo do ciclo. | P01 | CI01 | Alta |
| O11 | Confirmar o repasse da decisão. | P01 | CI01 | Alta |
| {{ID}} | {{objetivo de Guilherme}} | {{...}} | CI03 | {{...}} |

**Numeração:** O01–O05 identificam o mapa de Lucas e O06–O11, o de Pedro, nesta versão. A equipe deve conferir e fixar os IDs no mapa consolidado antes de reutilizá-los na Entrega 10.

## 4. Esquema conceitual de signos

A tabela abaixo já reúne os signos do fluxo de Lucas e de Pedro. Guilherme deve acrescentar os seus **nesta mesma tabela**, reaproveitando as linhas existentes quando se tratar do mesmo conceito.

| Grupo | Signo | Origem | Observações/semântica | Tipo de conteúdo | Restrição | Valor padrão | Prevenção | Recuperação |
|---|---|---|---|---|---|---|---|---|
| Rota | Ponto planejado | Domínio/gestor | Local indicado para inspeção; não significa que foi visitado. | Talhão, linha e árvore | Deve identificar o ponto na rota. | Próximo pendente | Mostrar identificador do ponto. | Voltar à rota e selecionar outro ponto. |
| Rota | Situação do ponto | Sistema | “Com registro” ou “pendente”; não indica ausência de praga. | Estado | Não confundir com resultado da foto. | Pendente | Exibir texto e símbolo além de cor. | Abrir o ponto e conferir registros. |
| Captura | Foto do fruto | Usuário | Imagem que será analisada. | Imagem | Deve ter qualidade suficiente para análise. | Nenhuma | Orientar foco, distância e iluminação. | Ajustar ou refazer a foto. |
| Captura | Qualidade da foto | Sistema | Indica possível problema de foco ou enquadramento. | Estado/mensagem | Não equivale ao resultado da análise. | Aguardando captura | Avisar antes de fotografar. | Reposicionar e tentar novamente. |
| Análise | Situação da análise | Sistema | “Analisando”, “concluída” ou “falhou”. | Estado/mensagem | Informar quando não houver conclusão. | Aguardando foto | Mostrar progresso textual. | Cancelar ou tentar novamente. |
| Resultado | Resultado da foto | Sistema | “Sinal suspeito”, “nenhum sinal nesta foto” ou “inconclusivo”. É indicação da IA, não validação humana. | Texto e símbolo | Vinculado à foto analisada. | Nenhum | Explicar o alcance de cada mensagem. | Refazer a foto ou guardar para conferência. |
| Registro | Data e hora da captura | Sistema | Momento em que a foto foi obtida, distinto do horário de envio. | Data e hora | Associadas ao registro. | Captura atual | Mostrar no resumo. | Corrigir por nova captura se o registro estiver incorreto. |
| Registro | Local do achado | Sistema ou usuário | Posição obtida por GPS ou identificação manual do ponto. | Coordenadas ou talhão/linha/árvore | Indicar a origem do local. | Tentar GPS | Mostrar se o local foi obtido. | Informar local manualmente se faltar GPS. |
| Registro | Situação do registro | Sistema | “Salvo no celular”; ainda não significa que o gestor o recebeu. | Estado/mensagem | Registro deve permanecer acessível. | Não salvo | Confirmar o salvamento. | Tentar salvar novamente sem descartar a foto. |
| Repasse | Destinatário | Domínio | Papel que receberá os achados, como o gestor da propriedade. | Função | Deve estar definido para o repasse. | Gestor da rota, se previamente definido | Mostrar a função no resumo. | Corrigir o destinatário antes do envio, conforme regras da equipe. |
| Repasse | Situação do envio | Sistema | “Aguardando conexão”, “enviando”, “enviado” ou “falha”; enviado não significa lido. | Estado/mensagem | Separada da situação do registro local. | Aguardando, se offline | Mostrar texto e quantidade pendente. | Tentar novamente mantendo os dados salvos. |
| Ciclo | Aviso de ciclo concluído | Sistema | Informa que a inspeção terminou, com data; não garante que todos os talhões foram inspecionados. | Estado/mensagem e data | Associado ao ciclo. | Nenhum | Exibir junto ao resumo da cobertura. | Reabrir o resumo do ciclo. |
| Cobertura | Cobertura do talhão | Sistema | “Inspecionado”, “não inspecionado” ou “cobertura incompleta”; não indica ausência de praga. | Estado | Não confundir com “sem focos”. | Não inspecionado, até haver registro | Texto e símbolo além de cor; frase explicando o limite. | Pedir nova inspeção do talhão. |
| Resultado | Situação do talhão no ciclo | Sistema | “Com focos”, “sem focos nesta inspeção” ou “não inspecionado”. | Estado | “Sem focos” só vale para talhão inspecionado. | Não inspecionado | Separar visualmente os três estados. | Abrir o talhão e conferir a cobertura. |
| Resultado | Confiança do resultado | Sistema | Indicação em linguagem simples de quão confiável é a detecção; não é validação humana. | Texto (alta/média/baixa, proposta) | Sem números técnicos; vinculada às fotos. | Nenhum | Mostrar com as fotos e o local. | Marcar para parecer do agrônomo ou pedir reinspeção. |
| Decisão | Posição do talhão | Usuário | Escolha do gestor: “confiável”, “parecer do agrônomo” ou “reinspeção”; não valida a praga. | Estado escolhido | Uma posição por talhão e ciclo. | Sem posição | Mostrar as três saídas com texto claro. | Alterar a posição antes de registrar a decisão. |
| Evolução | Tendência do talhão | Sistema | “Avançando”, “estável” ou “recuando” entre ciclos. | Estado e ciclos comparados | Avisar se algum ciclo comparado teve cobertura incompleta. | Sem comparação, se faltar ciclo | Texto e símbolo além de cor. | Ver a cobertura dos ciclos comparados. |
| Evolução | Última aplicação | Usuário/domínio | Marca no histórico o ciclo em que houve aplicação. | Data/ciclo | Não indica produto nem dose. | Nenhuma | Marcar na própria linha do tempo. | Corrigir o registro, conforme regras da equipe. |
| Decisão | Decisão do ciclo | Usuário | Onde, quando e com que urgência aplicar; não é recomendação do sistema. | Talhões, data e urgência | Só o gestor a registra; mostrar autoria e data. | Nenhuma | Ordenar por gravidade como dado, sem sugerir ação. | Voltar e alterar antes de repassar. |
| Repasse | Situação do repasse | Sistema | “Registrada”, “repassada” ou “falha”; repassada não significa que foi aplicada. | Estado/mensagem | Separada do registro da decisão; o destinatário pode não usar o sistema. | Registrada | Mostrar o estado e o destinatário. | Tentar novamente mantendo a decisão salva. |
| {{grupo}} | {{signo de Guilherme}} | {{usuário/sistema/domínio}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

**GPS:** sistema de posicionamento utilizado quando há localização disponível. Um local informado manualmente não será apresentado como coordenada obtida automaticamente.

## Síntese

**Lucas:** os diagramas MoLIC deverão contemplar O01–O05 e as conversas sobre selecionar ponto, ajustar e capturar a foto, aguardar a análise, interpretar cada tipo de resultado, registrar o local e verificar o envio. Devem incluir os retornos para foto inadequada, resultado inconclusivo, GPS indisponível e falha no envio.

**Pedro:** os diagramas MoLIC deverão contemplar O06–O11 e as conversas sobre receber o resumo do ciclo, conferir a cobertura, avaliar evidência e confiança, registrar a posição do talhão, ler a evolução, registrar a decisão do ciclo e conferir o repasse. Devem incluir os retornos para talhão não inspecionado (pedir nova inspeção), dúvida sobre o resultado (parecer do agrônomo ou reinspeção), cobertura incompleta na comparação e falha no repasse. Os signos “cobertura do talhão”, “confiança do resultado”, “posição do talhão”, “tendência do talhão” e “situação do repasse” devem manter os mesmos nomes. “Destinatário” e “situação do envio” de Lucas descrevem o repasse do trabalhador ao gestor; o repasse do gestor a quem aplica é outro signo, e a equipe deve conferir se os nomes não se confundem.

**Guilherme:** {{objetivos, tópicos e signos que devem aparecer no MoLIC}}.

Após a consolidação, a equipe deverá fixar um vocabulário e reutilizar os mesmos nomes de objetivos e signos na Entrega 10.

## Checklist

- [x] O cenário CI02 mostra alterações em relação ao cenário de problema C02.
- [ ] Cada solução individual identifica autor e cenário de origem — falta Guilherme.
- [x] Tópicos, falas e signos das partes de Lucas e de Pedro são coerentes com seus objetivos.
- [ ] Mapas individuais foram consolidados.
- [ ] O esquema de signos da equipe está completo em uma tabela única e sem duplicações.
- [ ] Nomes de objetivos e signos foram fixados pela equipe para a Entrega 10.
- [x] Os signos de Lucas representam conceitos compreensíveis ao trabalhador, e não apenas estruturas internas do código.
- [x] As telas propostas para Lucas correspondem a objetivos e signos identificados.
- [x] A interface comunica o significado e os limites do resultado técnico para a tarefa de Lucas.
