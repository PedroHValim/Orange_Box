# Entrega 12 — Planejamento da avaliação de usabilidade (DECIDE)

**Data:** 14/11/2026  
**Status:** 🟨 em andamento — partes de Pedro (P01) e Lucas (P02) preparadas; parte de Guilherme (P03) e consolidação da equipe pendentes.  
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

**Fluxo de P02 (Lucas Cabral — inspetor):** no perfil “Inspeção”, o participante consulta uma vistoria existente, registra uma nova vistoria de uma fruta de teste e verifica o registro no Histórico. A avaliação observa se ele encontra o registro, compreende o resultado mostrado e identifica a área ou a ausência de associação a um talhão. Não avalia se o modelo identificou corretamente um ácaro.

**Dados simulados no fluxo de P02:** a conta e as oito áreas da Fazenda Boa Esperança são demonstrativas. A vistoria anterior consultada em UT01 é um registro de exemplo. Em UT02, usa-se uma fruta ou imagem de teste, sem afirmar que há ácaros reais. A nova vistoria fica armazenada no iPhone do teste; ela não representa uma inspeção agronômica válida e não será enviada a uma propriedade.

| Planejado para P02 | No aplicativo | Consequência para a avaliação |
|---|---|---|
| Seguir um roteiro e identificar pontos pendentes de inspeção. | Há Mapa e Histórico, mas não há roteiro de visita nem lista de pontos pendentes. | A identificação de ponto pendente prevista em MU01 e a cobertura da rota não podem ser avaliadas nesta versão. |
| Fotografar, analisar e registrar uma vistoria. | A Câmera usa o modelo no iPhone; o registro depende de localização disponível e é salvo localmente. Uma detecção abaixo do limiar mostrado pode impedir a captura. | UT02 mede o registro de uma vistoria de teste, desde que o piloto confirme uma amostra e condições que permitam concluir a tarefa. A acurácia da detecção fica fora do escopo. |
| Entender resultado e localização antes de seguir. | O detalhe no Histórico mostra foto, contagem, confiança quando há detecção, data, coordenadas e talhão associado ou ainda não delimitado. | UT03 verifica se o participante interpreta o que foi registrado, sem inferir que “sem sinal confirmado” significa ausência de praga na área. |
| Guardar localmente e depois transmitir ao responsável, com estados de envio. | O aplicativo persiste registros no aparelho; não há fila de sincronização nem confirmação de repasse da inspeção. | Pode-se avaliar se o participante reconhece o registro local. Envio, recebimento e recuperação de falha de transmissão não são avaliáveis. |

**Fluxo de P03:** {{Guilherme}}

## A. Método DECIDE

| Etapa | Aplicação no projeto |
|---|---|
| **D — Determine the goals** | **P01:** verificar, no aplicativo, o que é possível das metas MU10–MU16 da Entrega 8: concluir o fluxo sem ajuda, não confundir talhão não inspecionado com talhão sem praga, comparar com o período anterior, enviar o relatório a quem aplica e achar as tarefas fáceis. A seção B indica quais metas foram adaptadas e quais ficam não avaliadas. Além disso, observar como o gestor entende a ordem dos talhões (dado ou recomendação), ponto que segue em aberto desde a Entrega 5.<br><br>**P02 — Lucas Cabral:** verificar o que é possível das metas MU01–MU03: consultar uma vistoria, registrar outra sem ajuda, encontrá-la no Histórico, compreender seu resultado e sua condição de armazenamento, medir o tempo de registro e a facilidade percebida. A parte de MU01 referente a ponto pendente e o fluxo de envio planejado ficam **não avaliados** porque não existem nesta versão.<br><br>**P03:** {{Guilherme}} |
| **E — Explore the questions** | **P01:** as perguntas QA10–QA18 da seção B. As principais são: o gestor percebe o talhão que ninguém inspecionou? Encontra onde o problema mais cresceu? Consegue registrar uma aplicação e mandar a situação da fazenda a quem aplica?<br><br>**P02 — Lucas Cabral:** QA01–QA03 da seção B: o inspetor encontra e interpreta uma vistoria? Consegue registrar uma nova e reconhecê-la como salva **neste aparelho**? Quanto tempo leva e quão fácil considera as tarefas?<br><br>**P03:** {{Guilherme}} |
| **C — Choose the evaluation paradigm and techniques** | **P01:** teste de usabilidade com observação de usuários (conclusão, erros, tempo e compreensão), pergunta de facilidade após cada tarefa e inspeção heurística feita pela equipe antes do teste, para registrar problemas evidentes antes de ocupar o tempo dos participantes.<br><br>**P02 — Lucas Cabral:** teste de usabilidade individual com observação, registro de conclusão, tempo, erros e pedidos de ajuda em UT01–UT03; pergunta de facilidade após cada tarefa e perguntas curtas de compreensão do resultado. Antes das sessões, inspeção heurística do fluxo Câmera → Mapa → Histórico, especialmente mensagens sobre GPS, confiança, salvamento local e ausência de associação a talhão.<br><br>**P03:** {{Guilherme}} |
| **I — Identify the practical issues** | **P01:** três participantes planejados, recrutados por conveniência entre donos, gerentes ou administradores de propriedades de citros (seção C). Sessão individual e presencial de cerca de 30 minutos, conduzida por Pedro, com um colega anotando, em um iPhone da equipe com o aplicativo instalado. Um piloto com um colega valida instruções, preparação dos dados e tempo. Riscos: não conseguir gestores reais (usar substitutos e registrar a limitação); depender de um iPhone com iOS 17 ou superior e de um Mac para instalar o aplicativo; o mapa de satélite precisa de internet; os dados mudam durante a sessão e precisam ser restaurados entre participantes.<br><br>**P02 — Lucas Cabral:** três participantes planejados, mais um piloto fora da análise. Sessão individual de cerca de 20 a 30 minutos, conduzida por Lucas em iPhone físico com iOS 17 ou superior, aplicativo e modelo instalados, permissões de câmera e localização verificadas. Preparar previamente a fruta ou foto de teste, conferir GPS e conexão para o mapa, registrar o estado inicial e restaurar o aplicativo entre sessões. No piloto, verificar se a amostra permite registrar uma vistoria; se uma detecção de baixa confiança bloquear repetidamente a captura, anotar o impedimento e não inventar um resultado de UT02. Não testar com registros reais de propriedade.<br><br>**P03:** {{Guilherme}} |
| **D — Decide how to deal with ethical issues** | **P01:** mesmos cuidados da Entrega 7. Consentimento lido e confirmado antes de começar; participação voluntária, com direito de pular tarefas ou parar; sem áudio, vídeo ou fotos de pessoas; identificação só por código (G1, G2, G3); nenhum dado real da propriedade é pedido, pois os dados são de exemplo; o relatório exportado no teste não é enviado a ninguém de verdade; deixar claro que se avalia o aplicativo, e não a pessoa; apenas sínteses anônimas no repositório.<br><br>**P02 — Lucas Cabral:** explicar a finalidade e obter consentimento antes do teste; permitir recusa, pausa ou desistência sem justificativa. Usar códigos L1, L2 e L3. Não fotografar participantes, documentos, áreas reais ou coordenadas da propriedade; usar somente o aparelho e a amostra de teste. O registro pode conter foto e localização do teste, portanto deve ser apagado após a conferência e antes de reutilizar o aparelho. Anotar falas sem nome ou contato, restringir o acesso às notas da equipe e publicar apenas resultados anônimos. Esclarecer que o resultado do aplicativo é experimental e que a habilidade profissional do participante não está sendo julgada.<br><br>**P03:** {{Guilherme}} |
| **E — Evaluate, interpret and present the data** | **P01:** cada meta é comparada com o resultado e classificada como atingida, parcialmente atingida, não atingida ou não avaliada. Com três participantes, os resultados são apresentados em contagem de pessoas e mediana, sem porcentagens nem generalização. Observações e falas são agrupadas por tela do aplicativo e viram uma lista de problemas com gravidade (seção F).<br><br>**P02 — Lucas Cabral:** apresentar, por tarefa, quantos participantes concluíram sem ajuda, com ajuda ou não concluíram; a mediana dos tempos de UT02; as notas individuais e medianas de facilidade; e exemplos anônimos de interpretações corretas ou equivocadas. Comparar MU01–MU03 com os limites estabelecidos, identificando explicitamente os trechos não avaliáveis. Agrupar problemas por Câmera, Mapa, Histórico e detalhe do registro; não generalizar os achados para todos os inspetores a partir de três pessoas.<br><br>**P03:** {{Guilherme}} |

## B. Perguntas de avaliação

Os IDs de P01 acompanham as metas da Entrega 8 (QA10 corresponde a MU10, e assim por diante), para não colidir com as perguntas de P02 e P03. A última coluna diz se a meta vale como escrita, foi adaptada ao aplicativo ou fica não avaliada nesta versão. Os limites das metas adaptadas são os da Entrega 8 e serão revistos após o piloto.

| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| QA01 | O inspetor consegue consultar uma vistoria, registrar outra e encontrar o registro salvo sem ajuda? Entende o que ficou salvo e o que não foi transmitido? | Observação em UT01–UT03 e perguntas de compreensão. | Conclusão, ajuda e erros por participante; explicação sobre resultado, localização e armazenamento. | **MU01 adaptada:** 3 de 3 participantes concluem as tarefas avaliáveis sem ajuda. Identificar ponto pendente no roteiro e confirmar envio ficam **não avaliados**. |
| QA02 | Quanto tempo o inspetor leva para registrar uma vistoria de teste? | Cronometragem de UT02. | Tempo da Câmera pronta até o feedback de registro salvo, incluindo tentativas e correções; carga inicial do modelo anterior à tarefa não entra na medição. | **MU02:** mediana ≤ 60 segundos. Se a captura não puder ser concluída nas condições preparadas, registrar falha ou impedimento, sem atribuir tempo fictício. |
| QA03 | O inspetor considera fáceis o registro e a consulta do resultado? | Escala pós-tarefa de 1 a 7 e comentário aberto. | Nota após UT02 e UT03; mediana por tarefa; motivo da nota. | **MU03 adaptada:** mediana ≥ 5 em cada uma dessas tarefas. A satisfação com cobertura da rota e repasse não é avaliada. |
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

**Pontos a conferir na inspeção heurística de P02 (QA01–QA03),** levantados pela leitura do aplicativo e ainda não verificados em sessão com participante:

- A mensagem “Registro salvo neste aparelho” comunica armazenamento local, mas o fluxo planejado previa repasse posterior. Verificar se o inspetor supõe que alguém já recebeu a vistoria.
- O Histórico usa “Sem sinal confirmado”, enquanto o detalhe apresenta “Nenhuma praga confirmada”. Verificar se alguém interpreta essas expressões como garantia de que a fruta ou o talhão estão livres de praga.
- Após salvar, o aplicativo pode pedir a associação da vistoria a um talhão. Verificar se a pessoa entende a diferença entre **vistoria salva** e **vistoria associada a uma área**.
- Com localização indisponível ou confiança baixa, a captura pode não prosseguir. Verificar se a mensagem explica como recuperar a tarefa.

**Pontos a conferir na inspeção heurística (QA17),** levantados pela leitura do código e ainda não verificados no aparelho:

- O rótulo “Sem ocorrência” aparece tanto para talhão inspecionado sem detecção quanto para talhão sem nenhuma inspeção no período.
- A lista “Detecções por talhão” mostra só os quatro talhões com mais detecções; os demais, inclusive os sem inspeção, ficam ocultos até o gestor ampliar a lista.
- O Mapa conta apenas as detecções posteriores à última pulverização do talhão, e a aba Relatórios conta todas as do período. O mesmo talhão pode aparecer com números diferentes nas duas telas.

## C. Escopo e participantes

| Item | Planejamento |
|---|---|
| Perfis | **P01:** dono, gerente ou administrador de propriedade de citros que participa da decisão de manejo de pragas.<br><br>**P02 — Lucas Cabral:** pessoa que realiza ou já realizou vistoria de frutas ou plantas em campo e registra ou comunica seus achados; corresponde ao perfil de inspetor do cenário C02.<br><br>**P03:** {{Guilherme}} |
| Critérios de inclusão/exclusão | **P01:** ter 18 anos ou mais e ter participado de alguma decisão de manejo de pragas em citros nos últimos 12 meses (mesmo critério da Entrega 7). Ficam de fora os integrantes da equipe e quem ajudou a desenvolver o aplicativo. Se não houver acesso a gestores reais, os substitutos serão identificados como tal e não serão apresentados como usuários do campo.<br><br>**P02 — Lucas Cabral:** ter 18 anos ou mais e experiência prática em inspeção de plantas ou frutos, preferencialmente em citros, nos últimos 12 meses. Excluir integrantes da equipe e pessoas que projetaram ou programaram o CYF. Se não houver três inspetores acessíveis, registrar separadamente quantos são participantes substitutos e qual experiência possuem; não apresentá-los como inspetores de citros.<br><br>**P03:** {{Guilherme}} |
| Nº de participantes | **P01:** três planejados (amostra da Entrega 8), mais um piloto que não entra nos resultados.<br><br>**P02 — Lucas Cabral:** três planejados para comparação com MU01–MU03, mais um piloto que não entra nos resultados.<br><br>**P03:** {{Guilherme}} |
| Ambiente | **P01:** presencial, no escritório da propriedade ou em local escolhido pelo participante, com internet para o mapa.<br><br>**P02 — Lucas Cabral:** sessão presencial em local seguro para manusear o iPhone e a amostra de teste. Registrar luminosidade, interrupções e disponibilidade de localização. O teste não exige acesso a uma propriedade real; isso limita conclusões sobre o uso no pomar.<br><br>**P03:** {{Guilherme}} |
| Dispositivo | **P01:** iPhone da equipe com iOS 17 ou superior. A Entrega 8 previa computador para o gestor; o uso no celular passa a ser um ponto a observar.<br><br>**P02 — Lucas Cabral:** iPhone físico da equipe com iOS 17 ou superior, câmera funcional, localização autorizada e modelo instalado. Conferir conexão para carregar o mapa; os registros e a inferência são locais.<br><br>**P03:** {{Guilherme}} |
| Protótipo/versão | **P01:** aplicativo CYF para iPhone (`ios-native/`), versão de 12/11/2026, perfil “Administrador”, com os dados de exemplo preparados conforme descrito abaixo.<br><br>**P02 — Lucas Cabral:** mesma versão, perfil demonstrativo “Inspeção”. Dados de exemplo para UT01 e amostra de teste preparada para UT02; registrar qualquer diferença da versão instalada antes de aplicar as tarefas.<br><br>**P03:** {{Guilherme}} |
| Teste piloto | **P01:** um colega que não participou do desenvolvimento, antes da primeira sessão. Validar se as instruções são entendidas sem explicação, se a preparação dos dados produz o talhão sem inspeção, como restaurar os dados entre participantes e se a sessão cabe em 30 minutos.<br><br>**P02 — Lucas Cabral:** um colega que não participou do desenvolvimento. Conferir a leitura das instruções, permissões, GPS, carregamento do modelo, resultado da amostra, início e fim da cronometragem, limpeza do registro criado e duração da sessão. Ajustar o **procedimento** após o piloto, registrando o ajuste; não mudar os limites das metas depois de iniciar a coleta.<br><br>**P03:** {{Guilherme}} |

**Preparação dos dados de P01:** antes de cada sessão, o avaliador entra como “Administrador” e, na aba Histórico, apaga a única inspeção de um talhão (proposta: Talhão 06 · Ribeirão). Assim a fazenda fica com 8 talhões, 7 inspecionados e 1 sem inspeção, e dois talhões aparecem como “Sem ocorrência”: o Talhão 05, inspecionado e sem detecção, e o Talhão 06, que ninguém inspecionou. O talhão com mais detecções é o Talhão 04 · Natal Oeste. Como o aplicativo guarda as alterações, os dados precisam voltar ao estado inicial entre participantes; a forma de fazer isso (por exemplo, reinstalar o aplicativo) será confirmada no piloto.

**Preparação dos dados de P02 — Lucas Cabral:** iniciar no perfil “Inspeção” com os registros demonstrativos disponíveis. Para UT01, usar o registro de exemplo do Talhão 05 · Experimental Sul, sem detecções confirmadas. Para UT02, preparar uma fruta ou imagem de teste e verificar no piloto se o aplicativo permite concluir uma captura sem exigir que apareça uma praga. Confirmar permissões e funcionamento da localização antes de cada sessão, sem abrir a tarefa pelo participante. Registrar o número de vistorias antes e depois, apagar a vistoria criada e restaurar o estado inicial para a próxima pessoa. Se o local do teste ficar fora dos talhões demonstrativos, a ausência de associação automática deve ser tratada como condição dos dados, não como erro do participante.

## D. Lista de tarefas de avaliação

Os IDs de P01 acompanham as tarefas da Entrega 5 (UT09 corresponde a T09, UT08 a T08 e UT04 a T04). As tarefas de P02 retomam T01–T03 **na parte que a versão instalada permite observar**. Cada participante recebe somente as tarefas do seu perfil, já dentro da respectiva conta demonstrativa.

| ID | Cenário neutro entregue ao usuário | Objetivo oculto da avaliação | Critério de sucesso | Tempo-limite (se houver) |
|---|---|---|---|---|
| UT01 | “Você vai continuar uma vistoria. Descubra o que foi registrado anteriormente na área que o avaliador indicar e explique o que esse registro permite concluir.” | T01; O01 e O03. Observar localização de registro anterior e distinção entre ausência de detecção na foto e ausência de praga na área. | Encontra a vistoria indicada, identifica que ela não tem detecção confirmada e não afirma que toda a área está livre de praga. | Sem limite rígido. |
| UT02 | “Examine esta fruta de teste usando o aplicativo e deixe sua vistoria registrada para consulta posterior.” | T02; O02 e O04. Observar captura, feedback de resultado, GPS, salvamento e tempo de MU02. | Conclui uma nova vistoria, reconhece a confirmação de salvamento no aparelho e consegue explicar se foi associada a uma área ou ficou sem associação. | Sem limite rígido; cronômetro conforme QA02. |
| UT03 | “Encontre a vistoria que você acabou de fazer. Mostre o resultado e diga se outra pessoa já recebeu esse registro.” | T03; O03–O05 na parte disponível. Observar busca no Histórico, interpretação do resultado e compreensão do estado local. | Encontra o registro mais recente, identifica seu resultado sem apresentá-lo como diagnóstico definitivo e reconhece que não há confirmação de envio a outra pessoa. | Sem limite rígido. |
| {{UT05…}} | {{tarefas de Guilherme — P03}} | {{...}} | {{...}} | {{...}} |
| UT09 | “Você é responsável por uma fazenda de citros. Nos últimos dias, a equipe passou olhando as laranjeiras. Descubra quais áreas preocupam mais e se alguma área ficou sem ser vista.” | T09; O06 e O07. Verificar se encontra o talhão com mais detecções e se distingue o talhão sem inspeção do talhão inspecionado sem detecção (MU11). | Aponta o Talhão 04 como o mais preocupante e o Talhão 06 como não inspecionado, sem tratá-lo como livre da praga, sem ajuda. | Sem limite rígido; contado no tempo total de MU14. |
| UT08 | “Compare a situação de agora com a de antes e diga em qual área o problema mais cresceu. Depois, descubra quando foi a última vez que trataram a área que o avaliador indicar e contra o quê.” | T08; O09. Verificar se encontra a variação por talhão (MU12) e a data e o alvo da última aplicação; colher o relato sobre se a aplicação funcionou (QA13). | Aponta o talhão com maior aumento e informa corretamente a data e o alvo da aplicação. | Sem limite rígido; registrar o tempo até a primeira resposta (MU12). |
| UT04 | “A área que mais preocupa foi tratada hoje. Deixe isso anotado no aplicativo e mande a situação da fazenda para a pessoa que cuida da aplicação.” | T04; O10 e O11. Verificar se registra a aplicação no talhão certo, se gera o relatório e chega ao envio (MU15) e se nota a mudança do número no mapa. | Registra a aplicação no Talhão 04 e chega à tela de envio do relatório, dizendo corretamente se ele foi enviado. | Sem limite rígido; contado no tempo total de MU14. |

A sessão de P01 é encerrada se UT09 e UT04 somarem 20 minutos, e a tarefa em andamento é registrada como não concluída. Em P02, se uma tarefa ficar parada por aproximadamente dois minutos por falha técnica, o aplicador registra o impedimento, oferece a recuperação prevista no roteiro e decide no piloto se é possível continuar; o tempo e a ajuda não são ocultados.

> Uma boa instrução descreve o objetivo do participante sem dizer **onde clicar** ou usar o rótulo exato do controle que está sendo testado.

Por isso as instruções de P01 não usam “Relatórios”, “Histórico”, “filtros”, “talhão”, “inspeção”, “pulverização” nem “PDF”, que são rótulos do aplicativo. As instruções de P02 também não indicam “Câmera”, “Mapa”, “Histórico” ou o botão a pressionar.

## E. Instrumentos

- [Modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md)
- [Roteiro de teste](../instrumentos/roteiro_teste_usabilidade.md)
- [Planilha de observação](../instrumentos/planilha_observacao_modelo.md)
- [Formulário de avaliação heurística](../instrumentos/formulario_heuristica_modelo.md)
- **Questionário pré-teste (P01):** função na propriedade, tempo de participação nas decisões de manejo, número aproximado de talhões (em faixas), dispositivos que usa para acompanhar a propriedade e se usa iPhone no dia a dia. Sem nome, propriedade ou contato.
- **Questionário pós-tarefa (P01):** “Quão fácil foi realizar esta tarefa?”, de 1 (muito difícil) a 7 (muito fácil), aplicada após UT09, UT08 e UT04.
- **Perguntas pós-teste (P01):** “Alguma área ficou sem ser vista? Como você sabe?”; “A última aplicação funcionou? Onde você procuraria essa resposta?”; “Quem vai aplicar já recebeu a situação da fazenda?”; “Como você entendeu a ordem em que as áreas apareceram? Sentiu falta de uma sugestão do aplicativo?”.
- **Questionário pré-teste (P02 — Lucas Cabral):** “Você realiza ou já realizou inspeções de plantas ou frutos? Em qual cultura e há quanto tempo?”; “Como costuma registrar o que encontra?”; “Que aparelho costuma usar nesse trabalho?”; “Usa iPhone no dia a dia?”. Não pedir nome da propriedade, endereço nem coordenadas.
- **Registro de observação (P02 — Lucas Cabral):** código L1–L3, UT01–UT03, início e fim de UT02, conclusão sem ajuda/com ajuda/não conclusão, erros, dúvidas, mensagens percebidas, interpretação do resultado, associação ao talhão e entendimento de salvamento local. Para dificuldade técnica, registrar o estado do modelo, GPS e amostra, sem atribuir automaticamente a falha ao participante.
- **Pergunta pós-tarefa (P02 — Lucas Cabral):** após UT01, UT02 e UT03: “Quão fácil foi realizar esta tarefa?”, de 1 (muito difícil) a 7 (muito fácil); “O que facilitou ou dificultou?”.
- **Perguntas pós-teste (P02 — Lucas Cabral):** “O que você entende pelo resultado mostrado nesta vistoria?”; “Onde esse registro está guardado?”; “Ele já foi enviado a alguém? O que no aplicativo lhe dá essa impressão?”; “Se precisasse voltar a um ponto ainda não visitado, como faria hoje?”.
- **Instrumentos de P03:** {{questionários e registros de Guilherme}}.

Os quatro modelos vinculados acima ainda precisam ser adaptados antes da Entrega 13: o roteiro deve trazer as tarefas e perguntas de cada perfil; a planilha deve identificar participante, tarefa, tempo, ajuda, erro, interpretação e tela. **Ter as perguntas de Lucas descritas aqui não significa que os arquivos dos modelos já foram alterados.**

## F. Plano de análise

Os critérios abaixo são definidos antes da coleta. Cada perfil terá seus resultados apresentados separadamente, porque as tarefas e limitações da versão são diferentes.

- **Sucesso total, parcial e falha:** sucesso total é cumprir o critério da tarefa sem ajuda. Sucesso parcial é cumpri-lo com uma dica do avaliador ou depois de um erro que o próprio participante corrigiu. Falha é não cumprir o critério, desistir ou atingir o tempo de encerramento.
- **Erro:** ação ou conclusão que afasta o participante do objetivo, percebida ou não por ele. Em P01, tratar talhão não inspecionado como livre da praga, registrar a aplicação no talhão errado e dizer que o relatório foi enviado sem ter concluído o envio são erros críticos. Em P02, também são críticos concluir que “sem sinal confirmado” prova ausência de praga em todo o talhão ou afirmar que a vistoria foi enviada apenas porque está salva no iPhone.
- **Dúvida:** hesitação visível ou pergunta ao avaliador que o participante resolve sozinho.
- **Ajuda:** orientação do avaliador sobre o que fazer. Em P01, o avaliador só ajuda depois de dois pedidos ou de cerca de um minuto parado. P02 segue essa regra, distinguindo dica de interação de intervenção técnica para corrigir permissão, GPS ou funcionamento do aparelho. Toda intervenção é anotada.
- **Abandono:** o participante declara que não consegue ou não quer continuar a tarefa.
- **Tempo:** cronômetro do fim da leitura da instrução até o participante declarar que terminou ou dar a resposta. Em MU12, da exibição da lista de talhões até a resposta; carregamento do mapa não é contado. Em MU02, da Câmera pronta até a confirmação do registro salvo; tentativas e correções durante a tarefa são incluídas, mas a preparação inicial do aparelho e do modelo ocorre antes dela.
- **Satisfação pós-tarefa:** escala de 1 a 7. Para P01, apresentar média por tarefa e notas individuais; para P02, mediana por tarefa e notas individuais, conforme MU03.
- **Codificação de observações e falas:** cada anotação recebe a tela, o tipo (erro, dúvida, ajuda, comentário positivo ou sugestão) e o objetivo afetado. P01 usa O06–O11; P02 usa O01–O05. Anotações repetidas são agrupadas em um mesmo problema.
- **Priorização dos problemas:** gravidade de 0 a 4, considerando quantos participantes foram afetados, se o problema impede a tarefa e se induz uma conclusão equivocada no trabalho. Confundir área não inspecionada com área livre da praga (P01) ou registro local com registro enviado (P02) recebe atenção especial.
- **Comparação com as metas:** apresentar uma tabela por perfil com meta, resultado e situação: atingida, parcialmente atingida, não atingida ou não avaliada. P01 compara MU10–MU16; P02 compara MU01–MU03 apenas nas partes observáveis. Não alterar os limites após começar a coleta nem apresentar função inexistente como falha de desempenho do participante.
- **Apresentação:** com três participantes por perfil, informar contagens, tempos individuais e mediana, sem generalização estatística. Relatar limitações da amostra, do ambiente de teste e das funções ausentes; transformar os problemas observados em propostas de revisão para a entrega seguinte.

## Checklist

- [ ] As seis etapas DECIDE foram contextualizadas, não apenas expandidas por sigla. — feito para P01 e P02; falta P03.
- [ ] Perguntas de avaliação têm método e evidência correspondentes. — feito para P01 e P02; falta P03.
- [x] O plano distingue avaliação de IHC de avaliação técnica/científica do TCC.
- [ ] Dados ou processamentos simulados no protótipo estão declarados. — feito para P01 e P02; falta P03 e conferir a preparação no piloto.
- [ ] Tarefas vêm de objetivos/cenários relevantes. — feito para P01 e P02; falta P03.
- [ ] Critérios de sucesso foram definidos antes da coleta. — feito para P01 e P02; falta P03.
- [ ] Questões práticas e éticas estão resolvidas. — ainda é preciso confirmar participantes, iPhone, permissões, amostra de teste e restauração dos dados.
- [ ] Instrumentos estão prontos antes da Entrega 13/14. — os modelos vinculados ainda precisam ser adaptados.
- [ ] Plano diz como dados serão analisados e apresentados. — feito para P01 e P02; falta P03.
