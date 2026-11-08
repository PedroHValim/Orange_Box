# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 01/11/2026  
**Status:** 🟨 em andamento 
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e metas de usabilidade verificáveis, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| Contribuição técnica do TCC | Dataset, modelo de detecção do ácaro em imagens, processamento no dispositivo móvel e associação dos achados à localização. | O teste de IHC não substitui a avaliação da precisão, do desempenho ou da qualidade técnica do modelo. |
| Camada de interação — trabalhador (P02)  | Rota do dia, orientação de captura, análise, resultado, registro do local, cobertura da rota e situação do envio (P01–P07 da Entrega 6). | Compreensão, conclusão da tarefa, tempo, erros, recuperação e facilidade percebida durante a inspeção. |
| Camada de interação — agrônomo (P03) | Pedidos de parecer e novas detecções, mapa do talhão, foto e histórico do ponto, veredito, delimitação da área, parecer e repasse ao gestor (A01–A07 da Entrega 6). | Compreensão, eficácia, eficiência, satisfação, erros e acessibilidade na análise técnica. |
| Camada de interação — gestor (P01) | Aviso de ciclo, resumo e cobertura do ciclo, talhões com focos, detalhe do talhão com fotos e confiança, posição registrada (confiável, parecer ou reinspeção), evolução por ciclo, decisão do ciclo e repasse a quem aplica (G01–G08 da Entrega 6). | Compreensão da cobertura e da confiança, eficácia, tempo, erros e compreensão do repasse na revisão do ciclo. |
| Integrações e dados simulados | Fotos, resultados da IA, localização, histórico, pedido de nova foto e envio dos registros ou do parecer. Para P01: cobertura por talhão, histórico dos ciclos, pedido de parecer ao agrônomo e de reinspeção ao trabalhador, e repasse da decisão a quem aplica. | Os resultados e as falhas podem ser apresentados por estados preparados no protótipo. O participante será informado de que são simulados. No fluxo de P01, cobertura, evolução e confiança serão dados fictícios com resposta conhecida; as falhas de repasse serão estados prontos. O teste avalia a interação, não a recomendação agronômica. |

**Fluxo de P02:** a captura, a análise e o salvamento serão simulados mesmo sem internet. “Salvo no celular” e “enviado ao gestor” são estados distintos. A ausência de sinal em uma foto não comprova que a árvore esteja livre da praga.

**Fluxo de P03:** as telas citadas seguem a numeração do protótipo em papel, mas descrevem o protótipo a ser avaliado no Figma (Entrega 11). O atalho “ver histórico deste ponto”, os filtros de período e local e o aviso sobre o receituário agronômico serão incluídos no Figma. As metas dependentes desses elementos valem para essa versão.

**Fluxo de P01:** as telas G01–G08 seguem a numeração do protótipo em papel (Entrega 6), com prefixo G para não se confundirem com as personas, e descrevem o protótipo a ser avaliado no Figma (Entrega 11). O desenho em papel e a simulação ainda estão pendentes, então valem como planejamento. A evolução por ciclo (G06), o aviso de cobertura incompleta e as metas que dependem deles (MU12 e MU13) só poderão ser verificados depois que essas telas forem desenhadas e testadas.

## 1. Características da plataforma

| Característica | Fluxo do trabalhador — P02 | Fluxo do agrônomo — P03 | Fluxo do gestor — P01 | Consequência para IHC |
|---|---|---|---|---|
| Software | Aplicativo móvel de inspeção previsto no TCC. | Aplicação web proposta para uso no escritório; hipótese a confirmar na Entrega 7. | Mesma aplicação web de P03, com conta de gestor vinculada à propriedade; hipótese a confirmar na Entrega 7. | P02 precisa de fluxo curto de captura; P03 precisa de lista, mapa e histórico organizados. Para P01: padrões web conhecidos e a mesma conta de P03, pois a persona tem pouca experiência tecnológica. |
| Hardware/dispositivos | Smartphone com câmera e eventual lente macro, conforme o equipamento de captura. | Computador ou notebook; uso em tablet ou celular durante visitas é hipótese. | Computador ou notebook no escritório; celular ou tablet em visitas ao talhão (hipótese). | Botão de captura grande para P02; foto e contexto ampliáveis para P03. Para P01: resumo e cobertura na primeira tela, sem rolagem; mapa e lista em abas nas telas menores. |
| Capacidades | Fotografar, analisar, apresentar resultado e registrar o ponto. | Tela ampla para mostrar mapa do talhão e foto ampliada lado a lado (o CTT T07 indica foto, local e histórico em paralelo); teclado para redigir o parecer; acesso a várias propriedades na mesma conta. | Ver cobertura do ciclo, talhões com focos, fotos com confiança, evolução por ciclo e registrar a posição e a decisão. | Mostrar o resultado da IA separado da confirmação humana. Para P01: mostrar a cobertura antes dos resultados e a evolução a um toque do talhão. |
| Restrições | Sol forte, deslocamento, pouco tempo por fruto e fotos que podem sair sem nitidez. | Depende de conexão para carregar mapa e fotos em resolução original; uso em tela pequena (visitas) prejudica a comparação de foto e mapa; o agrônomo depende da qualidade e do contexto das fotos enviadas pelo campo e não pode refazê-las. | O gestor não valida a praga e depende do que P02 registra; a cobertura só existe se o percurso for registrado. | P02 pode ajustar ou refazer a foto; P03 pode pedir outra foto quando a informação for insuficiente. Para P01: oferecer “parecer do agrônomo” e “reinspeção” e sinalizar cobertura incompleta; o sistema não sugere produto, dose nem prioridade. |
| Conectividade/latência | A conexão pode faltar no pomar; os registros aguardam sincronização. | As fotos podem chegar horas após a captura, quando P02 recuperar conexão. | Escritório com internet estável (hipótese); os resultados só chegam após a sincronização de P02. | Exibir estados de salvamento e envio para P02; mostrar a P03 horários de captura e sincronização. Para P01: mostrar data do ciclo e da última sincronização, e distinguir “sem focos” de “ainda não chegou”. |
| Segurança/privacidade | Foto e localização podem revelar dados da propriedade e a atividade do trabalhador. | Mapa, fotos e parecer podem identificar a propriedade e o profissional responsável. | A cobertura por talhão pode ser lida como controle do trabalhador; a decisão identifica o gestor. | Informar a finalidade do registro, limitar acesso e mostrar a autoria necessária ao parecer. Para P01: mostrar cobertura por talhão e ciclo, sem o percurso individual nem o nome do trabalhador; autoria da decisão visível. |
| Volume de dados/histórico | Inspeções se repetem em muitas árvores e em diferentes dias. | Há pontos de diferentes talhões e ciclos a consultar. | Ciclos de cerca de 14 dias e dezenas de talhões por propriedade (hipótese). | P02 distingue registrados e pendentes; P03 acessa histórico com filtros por local e período. Para P01: evolução com os ciclos mais recentes por padrão (proposta: 6) e comparação com o ciclo anterior em um toque. |
| Tempo de processamento | O resultado precisa aparecer durante a inspeção; o tempo real depende do dispositivo. | A detecção já chega processada; mapa, fotos e envio do parecer podem demorar. | O resultado chega processado; o que demora é carregar mapa e fotos e repassar a decisão. | Mostrar estados de análise e carregamento, com recuperação após falhas. Para P01: “registrada” e “repassada” como estados separados, com nova tentativa sem perder a decisão. |
| Papéis/permissões | P02 registra e repassa achados; não decide sozinho o manejo. | P03 valida e emite parecer; P01 solicita ou recebe a recomendação. | Revisa o ciclo, registra a posição e a decisão, pede parecer a P03 e reinspeção a P02; quem aplica pode não usar o sistema. | Explicitar destinatário, estado do repasse e diferença entre detecção e veredito. Não há tela administrativa neste recorte. Para P01: só o gestor registra a decisão; o repasse a quem aplica é explícito e não exige conta (hipótese). |

**Hipóteses de plataforma a confirmar:** dispositivos disponíveis, estabilidade da conexão, volume real de registros, forma de comunicação entre papéis e necessidade de histórico. As características propostas não devem ser apresentadas como fatos observados com usuários.

## 2. Princípios gerais do projeto

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte | Link de referência |
|---|---|---|---|---|
| Contexto de uso — P02 | Inspeção a pé no pomar, sob sol e com conexão instável. | Poucos passos, instruções curtas, controle da rota e continuidade offline. | Entregas 1, 3 e 5 | — (artefatos internos) |
| Contexto de uso — P03 | Análise à distância, dependente do que o campo registrou. | Organizar pedidos por propriedade e talhão; permitir abrir diretamente a foto e o contexto do ponto. | Personas e cenário C03 | — (artefatos internos) |
| Contexto de uso — P01 | Decisão no escritório, a cada ciclo, com poucos pragueiros disponíveis e sem conhecer a praga. | Resumo e cobertura do ciclo na primeira tela; entrada direta no talhão com problema; vocabulário igual ao do campo (talhão, foco, ciclo). | Entregas 1 e 5; cenário C01 | — (artefatos internos) |
| Prevenção e recuperação de erros | Foto inadequada, dúvida sobre o resultado, falta de GPS e falhas de envio ou carregamento. | Permitir refazer a foto, registrar local manualmente, pedir nova foto e tentar reenviar sem perder dados. | Entregas 5 e 6 | https://www.nngroup.com/articles/ten-usability-heuristics/ |
| Privacidade e minimização | Localização, fotos e autoria podem identificar pessoas e propriedades. | Registrar apenas os dados necessários; informar a finalidade; limitar acesso às propriedades e pessoas envolvidas. | LGPD, art. 6º | https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm |
| Acessibilidade | Uso sob luz forte em P02; estados do mapa que não devem depender só de cor em P03. Em P01, “inspecionado”, “não inspecionado” e “com focos” não podem depender só da cor. | Combinar texto, símbolos e cor; buscar contraste mínimo de 4,5:1 para texto comum e tamanho adequado para os controles. Cobertura e tendência por cor, símbolo e texto; contraste de 3:1 para símbolos do mapa. | WCAG 2.2: 1.4.1, 1.4.3 e 2.5.8; 1.4.11 (P01) | https://www.w3.org/TR/WCAG22/ |
| Responsabilidade pelo parecer | A recomendação de manejo é uma decisão técnica do profissional habilitado. | O sistema registra o parecer; não sugere automaticamente produto ou dose. Informar que o parecer na interface não substitui o receituário agronômico aplicável. | Requisito do fluxo P03; Lei nº 14.785/2023 (agrotóxicos e receituário agronômico) | https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2023/lei/l14785.htm |
| Cobertura sem vigilância do trabalhador | A cobertura por talhão pode ser lida como controle de P02. | Mostrar cobertura por talhão e ciclo, sem o percurso individual nem o nome do trabalhador; registrar só quem decidiu. | LGPD, art. 6º; cenário C02 | https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm |
| Dado e recomendação (P01) | A ordenação por gravidade pode ser lida como sugestão de manejo, papel do agrônomo. | A ordem é dado, não recomendação; o sistema registra a decisão do gestor e não sugere produto, dose nem prioridade. A fronteira segue em aberto (HTA T04, passo 3.1). | Requisito do fluxo P01; legislação pertinente ao receituário | https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2023/lei/l14785.htm |
| Princípios de interação (ISO 9241-110) — P03 | O agrônomo compara foto, local e histórico antes de decidir; um veredito ou parecer errado tem custo no manejo. | Adequação à tarefa: foto, local e detecções anteriores na mesma tela da detecção. Tolerância a erros: veredito alterável até o envio e texto do parecer mantido após falha. Autodescrição: situação da validação e do pedido sempre visível. | ISO 9241-110:2020 | https://www.iso.org/standard/75258.html |
| Interação humano-IA e viés de automação — P03 | O agrônomo pode aceitar a indicação da IA sem examinar a foto. | A avaliação da IA aparece como “sinal forte/fraco” e região indicada, só depois da foto; deixar claro o que a IA faz e que a validação é humana; permitir rejeitar facilmente a indicação. | Amershi et al. (2019), *Guidelines for Human-AI Interaction*, diretrizes G1, G2 e G9; Parasuraman e Manzey (2010) | https://doi.org/10.1145/3290605.3300233 |
| Visibilidade do estado e reconhecimento (Nielsen) | Hoje o gestor decide pela memória e por relatos soltos, sem ver o que foi inspecionado nem se a decisão foi repassada. | Cobertura do ciclo e estados “registrada” e “repassada” sempre visíveis; ciclos anteriores na própria tela de evolução. | Nielsen (1994); cenário C01 | https://www.nngroup.com/articles/ten-usability-heuristics/ |

## 3. Metas de usabilidade

As metas serão avaliadas no contexto das tarefas. Seus limites são **propostas iniciais**, a revisar após um piloto, sem alterar retroativamente os critérios de um teste já realizado.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| Entender o resultado sem atribuir certeza indevida à IA. | P02 / T02 | O participante explica que “sinal suspeito” requer confirmação e que “nenhum sinal nesta foto” não garante árvore livre. | Evita interpretação incorreta durante a inspeção. |
| Recuperar-se de foto inadequada ou resultado inconclusivo. | P02 / T02 | O participante ajusta ou refaz a captura e continua na mesma rota. | O enquadramento é um ponto crítico da tarefa. |
| Distinguir cobertura e situação do envio. | P02 / T01 e T03 | O participante aponta o que falta inspecionar e explica se o registro está salvo ou já foi enviado. | Quem registra nem sempre é quem recebe e decide. |
| Compreender a diferença entre “detectado pela IA” e “validado por humano”. | P03 / T07 | O participante explica que o ponto confirmado passou pela avaliação humana e o pendente ainda não. | A distinção sustenta o parecer técnico. |
| Compreender o pedido de nova foto. | P03 / T07 | O participante entende que o ponto permanece pendente enquanto aguarda a nova foto. | Evita pedidos duplicados ou decisão sem dados suficientes. |
| Compreender a situação do parecer. | P03 / T05 | O participante identifica se o parecer foi enviado e o que fazer diante de falha. | O repasse ao gestor precisa ser explícito. |
| Avaliar se o contexto é suficiente. | P03 / T05 e T06 | O participante usa foto, local e histórico ou pede nova foto quando necessário. | Responde à dificuldade de decidir com fotos soltas e sem contexto. |
| Perceber se o resultado da IA interfere no julgamento. | P03 / T07 | O participante relata quando consultou a avaliação da IA e como a utilizou. | Permite revisar a ordem de apresentação das informações. |
| Distinguir a situação dos pontos no mapa sem depender só da cor. | P03 / T07 (A02) | O participante identifica pendentes, confirmados e rejeitados pelo símbolo e pela legenda, inclusive em versão do protótipo em escala de cinza. | Cobre a acessibilidade declarada para P03 (WCAG 1.4.1 e 1.4.11). |
| Distinguir “sem focos” de “não inspecionado”. | P01 / T09 (G01–G03) | O participante aponta os talhões não inspecionados e explica que talhão sem inspeção não significa talhão livre da praga. | Erro central do C01 e hipótese H09. |
| Compreender as saídas diante de um resultado duvidoso. | P01 / T09 (G04, G05) | O participante escolhe entre “parecer do agrônomo” e “reinspeção” e explica a diferença. | O gestor não valida a praga sozinho. |
| Interpretar a evolução entre ciclos. | P01 / T08 (G06) | O participante diz se o talhão avança, está estável ou recua, se a aplicação parece ter funcionado e se notou o aviso de cobertura incompleta. | Decide se o gestor reaplica o produto. |
| Perceber a ordenação por gravidade como dado, não como recomendação. | P01 / T04 (G03) | Relato de como entendeu a ordem da lista e se sentiu falta de uma sugestão do sistema. | Fronteira entre dado e recomendação em aberto. |
| Compreender a situação da decisão registrada. | P01 / T04 (G07, G08) | O participante diz se a decisão está só registrada ou já repassada a quem aplica e o que fazer diante de falha. | Quem aplica pode não ser quem usa o sistema (H02). |

### 3.2 Metas quantitativas

**Condições para MU01–MU03:** participantes do perfil P02; cenário e resultados simulados iguais para todos; amostra inicialmente planejada de três participantes. Registrar separadamente qualquer ajuda fornecida pelo avaliador.

| ID | Dimensão | Métrica | Tarefa/escopo | Meta proposta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | Eficácia | Participantes que fotografam, salvam um achado e identificam um ponto pendente sem ajuda. | P02 / T01–T03; P01 → P06 | 3 de 3 participantes planejados. | Observação de conclusão, erros e pedidos de ajuda. | Reúne captura, registro e controle da rota. |
| MU02 | Eficiência | Tempo da abertura da câmera até a confirmação de registro salvo no celular. | P02 / T02; P02 → P05 | Mediana ≤ 60 segundos. | Cronômetro; incluir ajustes e repetição da foto, excluindo espera artificial de processamento. | O ciclo é repetido muitas vezes. |
| MU03 | Satisfação | Facilidade percebida em escala de 1 (muito difícil) a 7 (muito fácil), após cada fluxo. | P02 / PF01 e PF02 | Mediana ≥ 5 em cada fluxo. | Pergunta pós-tarefa aplicada separadamente. | Uma tarefa concluída ainda pode ter sido difícil. |
| MU04 | Eficácia | Conclusão sem ajuda do fluxo: abrir pedido, validar cinco pontos, delimitar área e enviar parecer. | P03 / T07 + T05; A01 → A07 | Todos concluem; no máximo um participante precisa de uma dica. | Teste observado, registrando ajuda e conclusão. | Fluxo central de P03. |
| MU05 | Eficácia: erro | Pontos pendentes ou rejeitados incluídos indevidamente na área de aplicação. | P03 / T05, passo 4.1; A06 | Zero ocorrência. | Conferir a delimitação ao final da tarefa. | Evita dimensionar uma área maior com base em pontos não confirmados. |
| MU06 | Eficiência | Tempo para responder “este ponto já teve detecção antes?” a partir da tela da detecção. | P03 / T06, método M3; A03 | Mediana ≤ 20 segundos. | Cronômetro da exibição de A03 até a resposta. | Verifica se o histórico do ponto está acessível. |
| MU07 | Eficiência | Tempo total do fluxo para um talhão com cinco pontos pendentes. | P03 / T07 + T05; A01 → A07 | Mediana ≤ 8 minutos. | Cronômetro do início até a confirmação de envio. | O fluxo deve caber em uma sessão curta de trabalho. |
| MU08 | Eficácia: compreensão | Participantes que identificam corretamente a situação do parecer, inclusive após falha simulada. | P03 / T05; A07 e A01 | Todos os participantes. | Observação e pergunta pós-tarefa. | Um parecer não enviado não pode parecer concluído. |
| MU09 | Satisfação | Nota de facilidade, de 1 a 7, após cada tarefa. | P03 / T05, T06 e T07 | Média ≥ 5,5 em cada tarefa. | Pergunta pós-tarefa. | Permite comparar a dificuldade percebida nas tarefas técnicas. |
| MU10 | Eficácia | Conclusão sem ajuda do fluxo: abrir o resumo, identificar o talhão não inspecionado, revisar um talhão com foco, registrar a posição e a decisão do ciclo. | P01 / T09 + T04; G01 → G08 | Todos concluem; no máximo um participante precisa de uma dica. | Teste observado, registrando ajuda e conclusão. | Fluxo central de P01. |
| MU11 | Eficácia: erro | Talhões não inspecionados tratados como “sem focos” ao ler o resumo do ciclo. | P01 / T09; G01–G03 | Zero ocorrência. | Pergunta durante o teste e conferência com o cenário preparado. | Erro central do C01. |
| MU12 | Eficiência | Tempo para dizer se um talhão avança, está estável ou recua em relação ao ciclo anterior, a partir da lista de talhões com focos. | P01 / T08; G03 → G06 | Mediana ≤ 30 segundos. | Cronômetro da exibição de G03 até a resposta. | Tempo alto indica evolução pouco visível. |
| MU13 | Eficácia: compreensão | Participantes que dizem corretamente se a última aplicação funcionou no talhão indicado. | P01 / T08; G06 | Todos os participantes. | Pergunta pós-tarefa, com cenário de resposta conhecida. | Resposta errada leva a gasto desnecessário ou a foco que se espalha. |
| MU14 | Eficiência | Tempo total do fluxo para uma propriedade com 8 talhões, 3 com focos e 1 não inspecionado. | P01 / T09 + T04; G01 → G08 | Mediana ≤ 10 minutos. | Cronômetro do início até a confirmação do repasse. | A revisão do ciclo deve caber em uma sessão curta. |
| MU15 | Eficácia: compreensão | Participantes que identificam se a decisão está registrada e repassada, inclusive após falha simulada. | P01 / T04, passo 5.2; G08 | Todos os participantes. | Observação e pergunta pós-tarefa. | Decisão que não chega a quem aplica não gera manejo. |
| MU16 | Satisfação | Nota de facilidade, de 1 a 7, após cada tarefa. | P01 / T09, T08 e T04 | Média ≥ 5,5 em cada tarefa. | Pergunta pós-tarefa. | Mesma escala de MU09. |

**Condições para MU10–MU16:** participantes do perfil P01; cenário e resultados fictícios iguais para todos, com resposta conhecida; amostra inicialmente planejada de três participantes. Registrar separadamente qualquer ajuda do avaliador.

**Critério de conclusão:** o avaliador deverá registrar também os casos em que a pessoa termina a tarefa por tentativa e erro ou com ajuda. A conclusão isolada não demonstra que a interação foi clara.

### 3.3 Priorização das metas

Se o professor solicitar porcentagens que somem 100%, elas representarão **peso de prioridade**, não resultado medido.

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| MU01 — conclusão do fluxo de P02 | 20% | Evitar perda de achados e confusão na rota. |
| MU02 — tempo da captura | 10% | Tarefa repetida em muitos frutos. |
| MU03 — facilidade percebida por P02 | 5% | Ajuda a avaliar a continuidade do uso. |
| MU04 — conclusão do fluxo de P03 | 20% | Integra validação e parecer. |
| MU05 — erro na área delimitada | 15% | Erro com consequência relevante no manejo. |
| MU06 — acesso ao histórico | 10% | Informação necessária à análise do ponto. |
| MU07 — tempo do fluxo de P03 | 10% | Mede o esforço da sessão completa. |
| MU08 — compreensão do envio | 5% | Evita parecer de conclusão falsa. |
| MU09 — facilidade percebida por P03 | 5% | Identifica dificuldades nas tarefas técnicas. |
| **Total** | **100%** | **Distribuição proposta para a solução integrada.** |

## 4. Como o ciclo será iterado

1. **Após a Entrega 7:** revisar hipóteses sobre familiaridade digital, rotina de inspeção, controle da rota, necessidade de histórico e responsabilidades de cada perfil.
2. **Após o protótipo em papel e o walkthrough:** corrigir mensagens e caminhos em que as pessoas hesitarem, errarem ou não entenderem o resultado e o envio.
3. **Na Entrega 11:** integrar os fluxos de P01, P02 e P03 ao protótipo avaliável, mantendo explícitos os estados simulados.
4. **Nas Entregas 12–14:** aplicar tarefas equivalentes aos perfis correspondentes, medir MU01–MU16 e registrar também erros e comentários.
5. **Após cada avaliação:** relacionar problema observado, evidência, alteração realizada e meta afetada. Revisitar protótipo, descrições das tarefas e metas quando os dados justificarem.

## Checklist

- [x] Capacidades e restrições têm impacto de IHC explicitado.
- [x] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [x] Resultados e processamento simulados no protótipo foram explicitados.
- [x] Metas de usabilidade avaliam a interação, sem substituir métricas técnicas do TCC.
- [x] Normas e princípios estão contextualizados.
- [x] Metas quantitativas são mensuráveis e associadas a tarefas e públicos.
- [x] Eficácia, eficiência e satisfação foram consideradas.
- [ ] Metas verificadas nas Entregas 12–14 — avaliação ainda pendente.
