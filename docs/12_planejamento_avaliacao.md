# Entrega 12 — Planejamento da avaliação de usabilidade (DECIDE)
 
**Data:** 14/11/2026  
**Status:** 🟨 em andamento — parte de Pedro (P01) preparada; partes de Lucas (P02) e Guilherme (P03) e consolidação da equipe pendentes.  
**Responsabilidade:** 1 solução por equipe
 
## Objetivo da atividade
 
Planejar a avaliação antes de executá-la, ligando perguntas de avaliação a métodos, participantes, tarefas, métricas, aspectos práticos, ética e forma de análise.
 
## O que está sendo avaliado
 
A avaliação investiga **a qualidade da interação**, e não a precisão, o desempenho ou a validade científica do modelo de detecção do TCC.
 
**Versão avaliada:** aplicativo CYF (Clean Your Farm) para iPhone, pasta `ios-native/` do repositório `Cabral100/App_Orange_Box`, na versão de 12/11/2026. A Entrega 11 (Figma) não foi feita porque o aplicativo já existe.
 
**Fluxo de P01 (gestor):** o perfil “Administrador” do aplicativo, com as abas Relatórios, Mapa e Histórico. Avalia-se se o gestor entende a situação da fazenda no período, percebe o que não foi inspecionado, compara com o período anterior, registra uma aplicação e envia o relatório a quem aplica. Não se avalia se a detecção está certa nem se a decisão de manejo é agronomicamente correta.
 
**Dados simulados no fluxo de P01:** a conta é demonstrativa e os dados são os de exemplo do próprio aplicativo (Fazenda Boa Esperança, 8 talhões, uma inspeção por talhão nos últimos dias, aplicações e armadilhas fictícias). O participante será informado disso antes de começar.
 
**Diferenças entre o planejado e o aplicativo:** as Entregas 6, 8, 9 e 10 descrevem um fluxo planejado para o gestor (telas G01–G08 e MoLIC M03). O aplicativo cobre parte dele de outra forma, e a tabela abaixo registra o que pode ser avaliado nesta versão.
 
| Planejado para P01 | No aplicativo | Consequência para a avaliação |
|---|---|---|
| Aviso e resumo do ciclo concluído. | Não há aviso de ciclo. A aba Relatórios mostra a situação por período (7, 14, 30 ou 90 dias). | As tarefas falam em “últimos dias”, e não em ciclo. |
| Cobertura que separa “inspecionado”, “não inspecionado” e “com focos”. | Não há tela de cobertura. Cada talhão mostra o número de inspeções e um rótulo; talhão sem inspeção e talhão inspecionado sem detecção recebem o mesmo rótulo, “Sem ocorrência”. | MU11 pode ser medida, e é o ponto de maior risco da avaliação. |
| Confiança em linguagem simples e posição do talhão (confiável, parecer do agrônomo ou reinspeção). | Não há registro de posição nem pedido de parecer ou de reinspeção. O Histórico mostra a foto de cada inspeção. | A parte de “registrar a posição” de MU10 não pode ser avaliada. |
| Evolução por ciclo, com a última aplicação marcada e aviso de cobertura incompleta. | Variação de cada talhão em relação ao período anterior de mesma duração; data, produto e alvo da última aplicação em seção separada. | MU12 é adaptada à variação entre períodos. MU13 fica não avaliada, pois os dados de exemplo não têm registros anteriores à aplicação. |
| Decisão do ciclo (onde, quando e com que urgência aplicar). | Não há registro de decisão. No Mapa, é possível registrar que um talhão foi pulverizado. | A decisão é substituída pelo registro da aplicação. |
| Repasse a quem aplica, com estados “registrada” e “repassada” e falha simulada. | Exportação do relatório em PDF e envio pelo compartilhamento do iPhone. Não há estado de repasse nem falha simulada. | MU15 é adaptada ao envio do relatório; a parte da falha não pode ser avaliada. |
 
**Fluxo de P02:** {{Lucas}}
 
**Fluxo de P03:** {{Guilherme}}
 
## A. Método DECIDE
 
| Etapa | Aplicação no projeto |
|---|---|
| **D — Determine the goals** | **P01:** verificar, no aplicativo, o que é possível das metas MU10–MU16 da Entrega 8: concluir o fluxo sem ajuda, não confundir talhão não inspecionado com talhão sem praga, comparar com o período anterior, enviar o relatório a quem aplica e achar as tarefas fáceis. A seção B indica quais metas foram adaptadas e quais ficam não avaliadas. Além disso, observar como o gestor entende a ordem dos talhões (dado ou recomendação), ponto que segue em aberto desde a Entrega 5.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| **E — Explore the questions** | **P01:** as perguntas QA10–QA18 da seção B. As principais são: o gestor percebe o talhão que ninguém inspecionou? Encontra onde o problema mais cresceu? Consegue registrar uma aplicação e mandar a situação da fazenda a quem aplica?<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| **C — Choose the evaluation paradigm and techniques** | **P01:** teste de usabilidade com observação de usuários (conclusão, erros, tempo e compreensão), pergunta de facilidade após cada tarefa e inspeção heurística feita pela equipe antes do teste, para registrar problemas evidentes antes de ocupar o tempo dos participantes.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| **I — Identify the practical issues** | **P01:** três participantes planejados, recrutados por conveniência entre donos, gerentes ou administradores de propriedades de citros (seção C). Sessão individual e presencial de cerca de 30 minutos, conduzida por Pedro, com um colega anotando, em um iPhone da equipe com o aplicativo instalado. Um piloto com um colega valida instruções, preparação dos dados e tempo. Riscos: não conseguir gestores reais (usar substitutos e registrar a limitação); depender de um iPhone com iOS 17 ou superior e de um Mac para instalar o aplicativo; o mapa de satélite precisa de internet; os dados mudam durante a sessão e precisam ser restaurados entre participantes.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| **D — Decide how to deal with ethical issues** | **P01:** mesmos cuidados da Entrega 7. Consentimento lido e confirmado antes de começar; participação voluntária, com direito de pular tarefas ou parar; sem áudio, vídeo ou fotos de pessoas; identificação só por código (G1, G2, G3); nenhum dado real da propriedade é pedido, pois os dados são de exemplo; o relatório exportado no teste não é enviado a ninguém de verdade; deixar claro que se avalia o aplicativo, e não a pessoa; apenas sínteses anônimas no repositório.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| **E — Evaluate, interpret and present the data** | **P01:** cada meta é comparada com o resultado e classificada como atingida, parcialmente atingida, não atingida ou não avaliada. Com três participantes, os resultados são apresentados em contagem de pessoas e mediana, sem porcentagens nem generalização. Observações e falas são agrupadas por tela do aplicativo e viram uma lista de problemas com gravidade (seção F).<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
 
## B. Perguntas de avaliação
 
Os IDs de P01 acompanham as metas da Entrega 8 (QA10 corresponde a MU10, e assim por diante), para não colidir com as perguntas de P02 e P03. A última coluna diz se a meta vale como escrita, foi adaptada ao aplicativo ou fica não avaliada nesta versão. Os limites das metas adaptadas são os da Entrega 8 e serão revistos após o piloto.
 
| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| {{QA01…}} | {{perguntas de Lucas — P02}} | {{...}} | {{...}} | {{MU01–MU03}} |
| {{QA04…}} | {{perguntas de Guilherme — P03}} | {{...}} | {{...}} | {{MU04–MU09}} |
| QA10 | O gestor conclui o fluxo sem ajuda: ver a situação, identificar o talhão não inspecionado, registrar uma aplicação e enviar o relatório? | Observação | Conclusão, pedidos de ajuda e erros em UT09 e UT04. | MU10 adaptada: todos concluem; no máximo um participante precisa de uma dica. O registro de posição por talhão não é avaliado. |
| QA11 | O gestor trata um talhão não inspecionado como livre da praga? | Observação e pergunta durante a tarefa | Resposta a “alguma área ficou sem ser vista?”, conferida com os dados preparados. | MU11: zero ocorrência. |
| QA12 | O gestor encontra rapidamente onde o problema mais cresceu em relação ao período anterior? | Observação | Tempo entre abrir a lista de talhões e apontar o talhão com maior aumento. | MU12 adaptada: mediana ≤ 30 segundos. |
| QA13 | O gestor consegue dizer se a última aplicação funcionou? | Pergunta pós-tarefa | Relato de onde procuraria essa resposta e do que sentiu falta. | MU13 não avaliada nesta versão; o relato é registrado como evidência qualitativa. |
| QA14 | O fluxo cabe em uma sessão curta? | Observação | Tempo total de UT09 + UT04 com os 8 talhões de exemplo. | MU14 adaptada: mediana ≤ 10 minutos. |
| QA15 | O gestor sabe se o relatório foi enviado a quem aplica? | Observação e pergunta pós-tarefa | Resposta a “quem vai aplicar já recebeu?” depois de UT04. | MU15 adaptada: todos os participantes. A recuperação após falha não é avaliada. |
| QA16 | O gestor considera as tarefas fáceis? | Pergunta pós-tarefa | Nota de 1 (muito difícil) a 7 (muito fácil) após cada tarefa. | MU16: média ≥ 5,5 em cada tarefa. |
| QA17 | O aplicativo mantém visível o que foi inspecionado e é consistente entre as telas? | Inspeção heurística | Violações de visibilidade do estado, consistência e reconhecimento em vez de memorização, com gravidade. | Problemas graves registrados antes do teste com usuários. |
| QA18 | O gestor lê a ordem dos talhões como dado ou como recomendação? | Observação e pergunta pós-tarefa | Relato do participante; sem métrica numérica. | Sem critério de aprovação: serve para decidir a fronteira entre dado e recomendação. |
 
**Pontos a conferir na inspeção heurística (QA17),** levantados pela leitura do código e ainda não verificados no aparelho:
 
- O rótulo “Sem ocorrência” aparece tanto para talhão inspecionado sem detecção quanto para talhão sem nenhuma inspeção no período.
- A lista “Detecções por talhão” mostra só os quatro talhões com mais detecções; os demais, inclusive os sem inspeção, ficam ocultos até o gestor ampliar a lista.
- O Mapa conta apenas as detecções posteriores à última pulverização do talhão, e a aba Relatórios conta todas as do período. O mesmo talhão pode aparecer com números diferentes nas duas telas.
## C. Escopo e participantes
 
| Item | Planejamento |
|---|---|
| Perfis | **P01:** dono, gerente ou administrador de propriedade de citros que participa da decisão de manejo de pragas.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| Critérios de inclusão/exclusão | **P01:** ter 18 anos ou mais e ter participado de alguma decisão de manejo de pragas em citros nos últimos 12 meses (mesmo critério da Entrega 7). Ficam de fora os integrantes da equipe e quem ajudou a desenvolver o aplicativo. Se não houver acesso a gestores reais, os substitutos serão identificados como tal e não serão apresentados como usuários do campo.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| Nº de participantes | **P01:** três planejados (amostra da Entrega 8), mais um piloto que não entra nos resultados.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| Ambiente | **P01:** presencial, no escritório da propriedade ou em local escolhido pelo participante, com internet para o mapa.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| Dispositivo | **P01:** iPhone da equipe com iOS 17 ou superior. A Entrega 8 previa computador para o gestor; o uso no celular passa a ser um ponto a observar.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| Protótipo/versão | **P01:** aplicativo CYF para iPhone (`ios-native/`), versão de 12/11/2026, perfil “Administrador”, com os dados de exemplo preparados conforme descrito abaixo.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
| Teste piloto | **P01:** um colega que não participou do desenvolvimento, antes da primeira sessão. Validar se as instruções são entendidas sem explicação, se a preparação dos dados produz o talhão sem inspeção, como restaurar os dados entre participantes e se a sessão cabe em 30 minutos.<br><br>**P02:** {{Lucas}}<br><br>**P03:** {{Guilherme}} |
 
**Preparação dos dados de P01:** antes de cada sessão, o avaliador entra como “Administrador” e, na aba Histórico, apaga a única inspeção de um talhão (proposta: Talhão 06 · Ribeirão). Assim a fazenda fica com 8 talhões, 7 inspecionados e 1 sem inspeção, e dois talhões aparecem como “Sem ocorrência”: o Talhão 05, inspecionado e sem detecção, e o Talhão 06, que ninguém inspecionou. O talhão com mais detecções é o Talhão 04 · Natal Oeste. Como o aplicativo guarda as alterações, os dados precisam voltar ao estado inicial entre participantes; a forma de fazer isso (por exemplo, reinstalar o aplicativo) será confirmada no piloto.
 
## D. Lista de tarefas de avaliação
 
Os IDs de P01 acompanham as tarefas da Entrega 5 (UT09 corresponde a T09, UT08 a T08 e UT04 a T04). As tarefas são aplicadas nesta ordem, com o participante já dentro do perfil “Administrador”.
 
| ID | Cenário neutro entregue ao usuário | Objetivo oculto da avaliação | Critério de sucesso | Tempo-limite (se houver) |
|---|---|---|---|---|
| {{UT01…}} | {{tarefas de Lucas — P02}} | {{...}} | {{...}} | {{...}} |
| {{UT05…}} | {{tarefas de Guilherme — P03}} | {{...}} | {{...}} | {{...}} |
| UT09 | “Você é responsável por uma fazenda de citros. Nos últimos dias, a equipe passou olhando as laranjeiras. Descubra quais áreas preocupam mais e se alguma área ficou sem ser vista.” | T09; O06 e O07. Verificar se encontra o talhão com mais detecções e se distingue o talhão sem inspeção do talhão inspecionado sem detecção (MU11). | Aponta o Talhão 04 como o mais preocupante e o Talhão 06 como não inspecionado, sem tratá-lo como livre da praga, sem ajuda. | Sem limite rígido; contado no tempo total de MU14. |
| UT08 | “Compare a situação de agora com a de antes e diga em qual área o problema mais cresceu. Depois, descubra quando foi a última vez que trataram a área que o avaliador indicar e contra o quê.” | T08; O09. Verificar se encontra a variação por talhão (MU12) e a data e o alvo da última aplicação; colher o relato sobre se a aplicação funcionou (QA13). | Aponta o talhão com maior aumento e informa corretamente a data e o alvo da aplicação. | Sem limite rígido; registrar o tempo até a primeira resposta (MU12). |
| UT04 | “A área que mais preocupa foi tratada hoje. Deixe isso anotado no aplicativo e mande a situação da fazenda para a pessoa que cuida da aplicação.” | T04; O10 e O11. Verificar se registra a aplicação no talhão certo, se gera o relatório e chega ao envio (MU15) e se nota a mudança do número no mapa. | Registra a aplicação no Talhão 04 e chega à tela de envio do relatório, dizendo corretamente se ele foi enviado. | Sem limite rígido; contado no tempo total de MU14. |
 
A sessão é encerrada se UT09 e UT04 somarem 20 minutos, e a tarefa em andamento é registrada como não concluída.
 
> Uma boa instrução descreve o objetivo do participante sem dizer **onde clicar** ou usar o rótulo exato do controle que está sendo testado.
 
Por isso as instruções de P01 não usam “Relatórios”, “Histórico”, “filtros”, “talhão”, “inspeção”, “pulverização” nem “PDF”, que são rótulos do aplicativo.
 
## E. Instrumentos
 
- [Modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md)
- [Roteiro de teste](../instrumentos/roteiro_teste_usabilidade.md)
- [Planilha de observação](../instrumentos/planilha_observacao_modelo.md)
- [Formulário de avaliação heurística](../instrumentos/formulario_heuristica_modelo.md)
- **Questionário pré-teste (P01):** função na propriedade, tempo de participação nas decisões de manejo, número aproximado de talhões (em faixas), dispositivos que usa para acompanhar a propriedade e se usa iPhone no dia a dia. Sem nome, propriedade ou contato.
- **Questionário pós-tarefa (P01):** “Quão fácil foi realizar esta tarefa?”, de 1 (muito difícil) a 7 (muito fácil), aplicada após UT09, UT08 e UT04.
- **Perguntas pós-teste (P01):** “Alguma área ficou sem ser vista? Como você sabe?”; “A última aplicação funcionou? Onde você procuraria essa resposta?”; “Quem vai aplicar já recebeu a situação da fazenda?”; “Como você entendeu a ordem em que as áreas apareceram? Sentiu falta de uma sugestão do aplicativo?”.
- {{questionários de Lucas e de Guilherme}}
Os quatro modelos precisam ser adaptados ao fluxo de P01 antes da Entrega 13: o roteiro com as tarefas UT09, UT08 e UT04 e a planilha com uma linha por tela do aplicativo (Relatórios, Mapa, Histórico e detalhe do talhão).
 
## F. Plano de análise
 
Critérios definidos para o fluxo de P01. A equipe pode adotar os mesmos para P02 e P03 ou ajustá-los na consolidação.
 
- **Sucesso total, parcial e falha:** sucesso total é cumprir o critério da tarefa sem ajuda. Sucesso parcial é cumpri-lo com uma dica do avaliador ou depois de um erro que o próprio participante corrigiu. Falha é não cumprir o critério, desistir ou atingir o tempo de encerramento.
- **Erro:** ação ou conclusão que afasta o participante do objetivo, percebida ou não por ele. Em P01, tratar talhão não inspecionado como livre da praga, registrar a aplicação no talhão errado e dizer que o relatório foi enviado sem ter concluído o envio são erros críticos, mesmo que a tarefa termine.
- **Dúvida:** hesitação visível ou pergunta ao avaliador que o participante resolve sozinho.
- **Ajuda:** qualquer orientação do avaliador sobre o que fazer. O avaliador só ajuda depois de o participante pedir duas vezes ou ficar parado por cerca de um minuto, e cada ajuda é anotada com a tela em que ocorreu.
- **Abandono:** o participante declara que não consegue ou não quer continuar a tarefa.
- **Tempo:** cronômetro do fim da leitura da instrução até o participante declarar que terminou ou dar a resposta. Em MU12, da exibição da lista de talhões até a resposta. Carregamento do mapa não é contado.
- **Satisfação pós-tarefa:** escala de 1 a 7 após cada tarefa; apresenta-se a média por tarefa e as notas individuais.
- **Codificação de observações e falas:** cada anotação recebe a tela do aplicativo, o tipo (erro, dúvida, ajuda, comentário positivo ou sugestão) e o objetivo afetado (O06 a O11). Anotações repetidas entre participantes são agrupadas em um mesmo problema.
- **Priorização dos problemas:** gravidade de 0 a 4, considerando quantos participantes foram afetados, se o problema impede a tarefa e se leva a uma decisão errada de manejo. Problemas ligados a MU11 têm prioridade, por terem consequência fora do sistema.
- **Comparação com as metas:** uma tabela com MU10–MU16, a meta, o resultado obtido e a situação (atingida, parcialmente atingida, não atingida ou não avaliada), sem alterar os limites depois do teste. O que foi planejado e não existe no aplicativo é registrado como recomendação de projeto, e não como resultado.
## Checklist
 
- [ ] As seis etapas DECIDE foram contextualizadas, não apenas expandidas por sigla. — feito para P01; faltam P02 e P03.
- [ ] Perguntas de avaliação têm método e evidência correspondentes. — feito para P01; faltam P02 e P03.
- [x] O plano distingue avaliação de IHC de avaliação técnica/científica do TCC.
- [ ] Dados ou processamentos simulados no protótipo estão declarados. — feito para P01; faltam P02 e P03.
- [ ] Tarefas vêm de objetivos/cenários relevantes. — feito para P01; faltam P02 e P03.
- [ ] Critérios de sucesso foram definidos antes da coleta. — feito para P01; faltam P02 e P03.
- [ ] Questões práticas e éticas estão resolvidas. — faltam confirmar os participantes, o iPhone do teste e como restaurar os dados.
- [ ] Instrumentos estão prontos antes da Entrega 13/14. — modelos ainda precisam ser adaptados.
- [ ] Plano diz como dados serão analisados e apresentados. — feito para P01; faltam P02 e P03.
 
