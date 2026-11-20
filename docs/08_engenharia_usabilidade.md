# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 01/11/2026  
**Revisão:** 20/11/2026  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 solução por equipe.

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e metas de usabilidade verificáveis, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| Contribuição técnica do TCC | Dataset, modelo de detecção do ácaro em imagens, processamento no dispositivo móvel e associação dos achados à localização. | O teste de IHC não substitui a avaliação da precisão, do desempenho ou da qualidade técnica do modelo. |
| Camada de interação — trabalhador (P02) | Na versão atual: orientação de captura, análise, resultado e registro da inspeção. No modelo conceitual: rota do dia, cobertura e situação do envio, relacionadas a P01–P07 da Entrega 6. | Compreensão, conclusão da tarefa, tempo, erros, recuperação e facilidade percebida durante a inspeção. |
| Camada de interação — agrônomo (P03) | Pedidos de parecer e novas detecções, mapa do talhão, foto e histórico do ponto, veredito, delimitação da área, parecer e repasse ao gestor (A01–A03 e A05–A07 da Entrega 6; A04 foi retirada). | Compreensão, eficácia, eficiência, satisfação, erros e acessibilidade na análise técnica. |
| Camada de interação — gestor (P01) | Aviso de ciclo, resumo e cobertura do ciclo, talhões com focos, detalhe do talhão, posição registrada, evolução por ciclo, decisão e repasse a quem aplica (G01–G08 da Entrega 6). | Compreensão da cobertura e dos resultados, eficácia, tempo, erros e entendimento do repasse. |
| Integrações e dados simulados | Fotos, resultados da IA, localização, histórico, pedidos e repasses. | Resultados fictícios podem compor cenários de teste, desde que sejam apresentados como simulação. O teste avalia a interação, não a recomendação agronômica. |

**Fluxo de P02:** a avaliação atual considera captura, interpretação do resultado e confirmação do registro. O modelo conceitual também separa “salvo no celular” e “enviado ao gestor”, mas o aplicativo da Entrega 11 não materializa todos os estados de rota e envio. Essas partes permanecem como escopo futuro e não serão contabilizadas como sucesso ou falha na versão atual. A ausência de sinal em uma foto não comprova que a árvore esteja livre da praga.

**Fluxo de P03:** as telas A01–A07 identificam o fluxo conceitual. O aplicativo iOS não possui perfil de agrônomo; a Entrega 12 identifica separadamente o protótipo FA no Figma e quais metas MU04–MU09 podem ser observadas nele. Não presumir que atalhos, filtros ou avisos estejam implementados sem conferir a versão usada no teste.

**Fluxo de P01:** G01–G08 identificam estados do fluxo conceitual e da Entrega 6; o aplicativo iOS documentado na Entrega 11 cobre apenas parte deles. A Entrega 12 distingue metas MU10–MU16 avaliáveis, adaptadas e não avaliáveis na versão disponível. Evolução por ciclo, aviso de cobertura incompleta, registro de posição e repasse não devem ser atribuídos ao aplicativo quando não existirem.

## 1. Características da plataforma

### 1.1 Trabalhador — P02 — Lucas

Capacidades técnicas, restrições, funcionalidades e contexto são diferenciados abaixo. Uma capacidade do dispositivo não comprova que toda funcionalidade associada esteja implementada.

| Categoria | Característica | Consequência para IHC |
|---|---|---|
| Capacidade técnica | Câmera do iPhone para obtenção de imagens. | Orientar enquadramento, distância e estabilidade. |
| Capacidade técnica | Processamento do modelo no dispositivo. | Comunicar prontidão, processamento e resultado. |
| Capacidade técnica | Armazenamento local dos registros. | Confirmar o salvamento sem sugerir que houve envio a outra pessoa. |
| Capacidade técnica | Serviços de localização do aparelho. | Informar a necessidade de permissão e as limitações do posicionamento. |
| Restrição da plataforma | Versão avaliável para iPhone; funcionamento em outros dispositivos não foi demonstrado nesta avaliação. | Identificar dispositivo e versão utilizados, sem generalizar para outras plataformas. |
| Restrição da plataforma | Tela móvel com espaço limitado. | Priorizar informações essenciais e controles legíveis. |
| Restrição da plataforma | Captura e localização dependem das permissões e dos recursos disponíveis no aparelho. | Explicar bloqueios e oferecer recuperação quando suportada. |
| Limite de evidência | Não foi comprovado funcionamento integral de todos os fluxos sem conexão. | Não apresentar todo o aplicativo como funcional offline. |
| Regra da versão | A captura é bloqueada abaixo de 85%, conforme verificação relatada por Lucas. | Comunicar o limiar e orientar o ajuste da captura; o percentual não deve ser apresentado como garantia de acerto. |
| Funcionalidade atual | Fotografar, apresentar resultado e salvar a inspeção. | Permitir reconhecer conclusão e consultar o registro. |
| Funcionalidade futura | Rota completa, cobertura de pontos e confirmação de repasse entre papéis. | Manter essas partes separadas da avaliação do aplicativo atual. |
| Contexto de uso | Inspeção a pé, luz forte, deslocamento e repetição em muitos frutos. | Reduzir carga visual e etapas desnecessárias. |
| Hipótese de contexto | Conectividade instável e diferentes níveis de familiaridade com aplicativos. | Investigar com o público-alvo antes de tratar como condição confirmada. |

Não foram fornecidas medições de memória, capacidade mínima de câmera ou limite técnico de processamento. Esses valores não serão inventados.

### 1.2 Gestor — P01 — Pedro

Mesma separação usada para P02. As versões consideradas são o aplicativo iOS no perfil Administrador (Entrega 11) e a versão web do mesmo repositório usada depois na sessão U02 (Entrega 14). Uma capacidade do dispositivo não comprova que a funcionalidade correspondente exista.

| Categoria | Característica | Consequência para IHC |
|---|---|---|
| Capacidade técnica | Exibição de mapa com camada de satélite e polígonos georreferenciados dos talhões. | Permitir localizar o talhão pelo espaço, sem depender apenas do nome. |
| Capacidade técnica | Armazenamento e consulta de registros por data e por talhão. | Viabilizar comparação entre períodos e acesso à evidência de cada número. |
| Capacidade técnica | Geração de gráficos e de arquivo exportável do relatório (PDF na versão web). | Comunicar processamento, conclusão e falha da exportação. |
| Capacidade técnica | Separação de acesso por perfil (Administrador e Inspeção). | Mostrar ao gestor apenas o que pertence à sua tarefa. |
| Restrição da plataforma | Tela de celular pequena para comparar vários talhões e períodos ao mesmo tempo. | Priorizar o resumo e permitir aprofundar por talhão, sem tabelas extensas. |
| Restrição da plataforma | Aplicativo nativo disponível só para iPhone; a versão web depende de conexão com o servidor. | Identificar a versão usada em cada avaliação e não generalizar para outros dispositivos. |
| Restrição da plataforma | O sistema só conhece o que foi registrado e enviado pela inspeção. | Indicar quando não há registro no período, em vez de exibir zero. |
| Funcionalidade atual | Mapa de talhões com contagem, relatório por período com variação em relação ao período anterior e talhões críticos, histórico de inspeções, exportação do relatório (web) e registro de pulverização (iOS). | São as partes avaliáveis nas Entregas 13 e 14. |
| Funcionalidade futura | Aviso e resumo do ciclo, estado “não inspecionado no período”, posição por talhão, pedido de parecer ou reinspeção, evolução por ciclo com aviso de cobertura incompleta, decisão e repasse (G01–G08). | Não atribuir ao aplicativo atual; metas que dependem delas ficam “não avaliadas”. |
| Papel do usuário | O gestor não valida a praga sozinho e decide ou encaminha o manejo. | Distinguir indicação automática, validação humana e decisão do gestor. |
| Contexto de uso | Revisão a cada ciclo de inspeção, fora do talhão, com intervalos entre usos. | Favorecer a retomada após intervalo: rótulos estáveis e resumo na entrada. |
| Hipótese de contexto | Rotina de ciclo, quem decide o manejo e uso de celular ou computador pelo gestor (H05, H21). | Investigar com gestores reais (I03, Entrega 7, ainda não aplicado) antes de tratar como fato. |

Não foram medidos tempo de carregamento do mapa, tempo de exportação nem limite de registros. Esses valores não serão inventados.

### 1.3 Agrônomo — P03 — conteúdo a revisar pelo responsável

A classificação abaixo preserva o conteúdo do perfil P03. Ainda precisa ser reorganizada pelo responsável para separar capacidades técnicas, restrições, funcionalidades e contexto, conforme o feedback.

| Característica | Agrônomo — P03 | Consequência para IHC |
|---|---|---|
| Software | Fluxo proposto no protótipo FA em Figma; não há perfil de agrônomo no aplicativo iOS. | P03 precisa de foto, localização e histórico organizados; P01, de resumo e talhões compreensíveis. |
| Hardware/dispositivos | Computador ou notebook para o protótipo FA; uso móvel durante visitas segue como hipótese. | Evidências ampliáveis para P03 e filtros legíveis para P01. |
| Capacidades previstas | Examinar foto, local e histórico, validar detecções e emitir parecer. | Separar indicação da IA de confirmação humana e comunicar o significado dos resultados. |
| Restrições | Depende da qualidade das fotos enviadas e da possibilidade de examinar seu contexto. | Pedir outra evidência quando necessário e explicar limites dos dados. |
| Conectividade | Fotos podem chegar depois da captura. | Distinguir estados locais, envio e recebimento quando o fluxo os oferecer. |
| Segurança/privacidade | Fotos, mapas e pareceres podem identificar propriedades e o profissional. | Limitar acesso e mostrar apenas identificação necessária à tarefa. |
| Volume/histórico | Pontos de vários talhões e períodos podem ser consultados. | Oferecer consulta por local e período quando confirmada a necessidade. |
| Tempo de processamento | Fotos e pareceres podem exigir carregamento e envio. | Comunicar processamento, sucesso e falha com caminho de recuperação. |
| Papéis | Analisa evidências e propõe orientação técnica. | Explicitar a autoria e o estado dos registros e distinguir os papéis. |

**Hipóteses a confirmar:** dispositivos disponíveis na rotina, estabilidade da conexão, volume real de registros, comunicação entre papéis e necessidade de histórico.

## 2. Princípios gerais do projeto

### 2.1 Princípios relacionados ao trabalhador — Lucas

#### Princípios direcionados ao negócio

| Princípio | Justificativa | Decisão decorrente |
|---|---|---|
| Minimizar a exposição de dados do trabalhador e da propriedade. | Fotos, localização e autoria podem identificar atividades e pessoas. | Registrar e apresentar apenas o necessário à inspeção, com acesso adequado. |
| Preservar os limites do resultado automático. | A indicação do modelo não equivale a diagnóstico profissional. | Não apresentar o percentual como certeza de identificação ou recomendação de manejo. |
| Diferenciar registro local de repasse. | Salvar no aparelho não comprova recebimento por outra pessoa. | Comunicar somente o estado efetivamente disponível na versão. |
| Não interpretar ausência de dados como ausência de praga. | Uma foto sem sinal e uma área não inspecionada têm significados diferentes. | Manter essa distinção no vocabulário e nos fluxos futuros de cobertura. |

#### Princípios direcionados à interface

| Princípio | Justificativa | Decisão decorrente |
|---|---|---|
| Permitir leitura rápida durante a inspeção. | Uso em campo e repetição da tarefa. | Instruções curtas, hierarquia clara e poucos elementos simultâneos. |
| Tornar visível a situação da captura e do registro. | O usuário precisa reconhecer quando pode fotografar e quando a imagem foi salva. | Mostrar orientação, processamento e confirmação. |
| Prevenir erros e indicar recuperação. | Captura inadequada ou permissões indisponíveis podem impedir a tarefa. | Explicar o motivo e a próxima ação possível. |
| Usar texto e símbolos além de cor. | Cores isoladas podem dificultar a interpretação. | Identificar estados com rótulos compreensíveis. |
| Manter termos e controles consistentes. | Consistência reduz esforço de aprendizagem. | Reutilizar os signos e objetivos das Entregas 9 e 10. |

### 2.2 Princípios relacionados ao gestor — Pedro

O contexto de P01 (revisão a cada ciclo, sem reconhecer a praga sozinho) funciona como justificativa; os princípios abaixo são as regras que orientam o design.

#### Princípios direcionados ao negócio

| Princípio | Justificativa | Decisão decorrente |
|---|---|---|
| A decisão de manejo pertence ao gestor (ou ao agrônomo, conforme H21). | O sistema não tem competência para recomendar produto, dose ou prioridade. | Apresentar e ordenar dados com critério explicado, sem recomendar o manejo. |
| Ausência de registro não é ausência de praga. | Um talhão não inspecionado no período não fornece evidência. | Tratar “não inspecionado” como estado próprio, separado de “sem ocorrência”. |
| Resultado automático não é confirmação. | A indicação do modelo não equivale a validação humana ou profissional. | Não chamar saídas do modelo de “confirmadas”; identificar a origem de cada número. |
| Cobertura por talhão, sem vigilância individual. | Informações da rota podem ser lidas como controle do trabalhador. | Mostrar o que foi coberto por talhão e período, não o desempenho por pessoa. |
| Registrar autoria e data das decisões. | Posição, decisão e repasse precisam ser atribuíveis quando questionados depois. | Guardar quem registrou e quando, nos fluxos futuros de posição e decisão. |
| Minimizar dados em relatórios exportados. | O arquivo pode circular fora do sistema. | Exportar apenas talhões, períodos e indicadores necessários. |

#### Princípios direcionados à interface

| Princípio | Justificativa | Decisão decorrente |
|---|---|---|
| Tornar a cobertura visível antes do resultado. | O gestor precisa saber o que o ciclo cobriu para confiar nos números. | Mostrar inspecionados e não inspecionados com rótulo, não apenas com zero ou cor. |
| Um indicador, um nome e um critério. | O gestor compara números entre Mapa, Relatórios e Conta. | Rotular o período e a regra de cada contagem; não usar o mesmo nome para medidas diferentes. |
| Não depender só de cor e manter a semântica das cores. | Mapas e gráficos são lidos rapidamente e por pessoas com diferentes percepções de cor. | Usar rótulo, número ou legenda vinculada; reservar vermelho para alerta. |
| Explicar o critério da ordenação. | Uma lista ordenada influencia a prioridade mesmo sem recomendar. | Informar por que um talhão aparece primeiro. |
| Levar do número à evidência. | O gestor não valida a praga sozinho e precisa ver fotos e local. | Permitir abrir, a partir do talhão, as fotos, o local e as datas. |
| Facilitar a retomada após intervalos. | O uso ocorre a cada ciclo, não diariamente. | Manter navegação e termos estáveis e um resumo na entrada. |
| Comunicar processamento, sucesso e falha. | Exportar ou registrar sem retorno leva a repetir a ação ou a supor que foi feito. | Confirmar a conclusão e indicar a recuperação em caso de falha. |

### 2.3 Demais princípios — conteúdo preservado para revisão da equipe

A equipe ainda deverá organizar os itens abaixo em princípios de negócio e de interface. Descrições de contexto devem funcionar como justificativas, não como princípios por si mesmas.

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Contexto de uso — P03 | Análise a distância, dependente do que foi registrado em campo. | Organizar fotos, locais e histórico; oferecer saída quando a evidência for insuficiente. | Persona e cenário C03. |
| Prevenção e recuperação de erros | Foto inadequada, dúvida sobre o resultado e falhas de carregamento ou envio. | Permitir ajuste ou repetição e comunicar como recuperar a tarefa. | Entregas 5 e 6; heurísticas de Nielsen. |
| Privacidade e minimização | Fotos, locais e autoria podem identificar pessoas e propriedades. | Coletar apenas dados necessários e limitar o acesso. | Planejamento ético da Entrega 7. |
| Acessibilidade | Uso sob luz forte; mapas e estados que não devem depender só de cor. | Combinar texto, símbolo e cor; verificar contraste e tamanho dos controles. | Diretrizes de acessibilidade adotadas no projeto. |
| Responsabilidade pelo parecer | Orientação de manejo exige julgamento profissional. | Não apresentar o resultado do modelo como parecer agronômico. | Requisitos do fluxo P03. |
| Cobertura sem vigilância individual | Informações da rota podem ser interpretadas como controle do trabalhador. | Apresentar o necessário para cobertura sem exposição desnecessária da pessoa. | Cenário C02; minimização de dados. |
| Interação humano–IA | O profissional pode aceitar automaticamente uma indicação da IA. | Distinguir sinal do modelo e veredito humano; permitir revisar e rejeitar. | Diretrizes de interação humano–IA adotadas no projeto. |
| Visibilidade do estado | Usuários precisam saber se análise, registro ou exportação terminaram. | Mostrar andamento, conclusão, falha e recuperação. | Heurísticas de Nielsen. |

## 3. Metas de usabilidade

As metas são critérios planejados. A Entrega 12 registra quais podem ser avaliadas como escritas, quais precisam de adaptação e quais não são avaliáveis na versão disponível.

Não apresentar funcionalidade ausente como erro do participante.

### 3.1 Metas qualitativas

| Meta | Perfil/tarefa | Evidência desejada |
|---|---|---|
| Compreender o resultado sem atribuir certeza indevida à IA. | P02 / T02 — versão atual. | Explica que a indicação do modelo não é confirmação profissional e que ausência de sinal na foto não garante árvore livre. |
| Recuperar-se de captura inadequada. | P02 / T02 — versão atual. | Ajusta a captura em resposta às orientações; repetição ou resultado inconclusivo somente quando disponíveis. |
| Distinguir cobertura e envio. | P02 / T01/T03 — versão futura nas partes ausentes. | Identifica pontos pendentes e diferencia registro local de envio. Não avaliar esses estados no aplicativo quando ausentes. |
| Diferenciar detecção da IA e validação humana. | P03 / T07 | Identifica o que depende do veredito do agrônomo. |
| Compreender o pedido de nova foto. | P03 / T07 | Entende que o ponto permanece pendente. |
| Compreender a situação do parecer. | P03 / T05 | Identifica conclusão e falha de envio. |
| Avaliar suficiência do contexto. | P03 / T05/T06 | Consulta foto, local e histórico ou pede outra evidência. |
| Observar influência da IA no julgamento. | P03 / T07 | Explica quando consultou a indicação automática e como a usou. |
| Identificar estados sem depender só da cor. | P03 / T07 | Diferencia pendente, confirmado e rejeitado por texto/símbolo. |
| Distinguir “sem focos” de “não inspecionado”. | P01 / T09 — versão atual: o talhão sem inspeção existe nos dados; o estado explícito ainda não. | Explica que ausência de inspeção não significa ausência de praga. |
| Compreender saídas diante de dúvida. | P01 / T09 — versão futura; depende de H21. | Distingue pedir parecer e pedir reinspeção, se essas ações existirem na versão. |
| Interpretar evolução entre ciclos. | P01 / T08 — versão atual parcial (comparação com o período anterior); evolução por ciclo e cobertura são futuras. | Identifica tendência e limites de cobertura quando disponíveis. |
| Interpretar ordenação como dado. | P01 / T04 — versão atual (talhões críticos em Relatórios). | Explica o significado da ordem da lista sem presumir recomendação automática. |
| Distinguir decisão registrada e repassada. | P01 / T04 — versão futura; depende de H21. | Identifica a situação real do repasse quando o fluxo existir. |

As metas de P01 foram classificadas na revisão de 20/11/2026. “Depende de H21” indica que, além de ausente na versão, a meta pressupõe que o gestor decide e repassa o manejo, hipótese ainda não confirmada com gestores reais. As metas de P03 ainda precisam da mesma classificação.

### 3.2 Metas quantitativas

**Condições:** usar cenários e dados equivalentes por perfil, registrar ajuda separadamente e informar `n/N`. A Entrega 14 prevê três participantes no total da equipe, não três em cada perfil.

Uma observação isolada não permite generalização estatística.

| ID | Dimensão | Métrica | Tarefa/escopo | Meta proposta | Como medir |
|---|---|---|---|---|---|
| MU01 | Eficácia | Proporção que fotografa e salva um achado sem ajuda; identificação de ponto pendente registrada separadamente. | P02 / T01–T03; P01–P06 conceituais. | Todos os participantes P02 expostos à tarefa; informar `n/N`. Captura e salvamento são avaliáveis; ponto pendente da rota permanece futuro. | Registrar conclusão, erros e ajudas por etapa. Não declarar o fluxo conceitual completo como atendido pela conclusão parcial. |
| MU02 | Eficiência | Tempo da abertura da câmera à confirmação de registro. | P02 / T02 — versão atual. | Mediana ≤ 60 segundos quando houver mais de uma medição comparável; com uma pessoa, informar o tempo individual. | Cronômetro; registrar repetição da foto. |
| MU03 | Satisfação | Facilidade em escala de 1 a 7 após cada fluxo disponível. | P02 / PF01/PF02. | Nota ≥ 5 por participante; calcular mediana se houver amostra comparável. | Pergunta pós-tarefa. Se a escala não foi aplicada, registrar “não medida”, sem converter comentários em nota. |
| MU04 | Eficácia | Abrir pedido, validar pontos, delimitar área e enviar parecer. | P03 / T07/T05. | Todos os participantes P03 que executarem o fluxo; informar `n/N` e ajudas. | Conclusão e intervenções; adaptar ao número de pontos do FA. |
| MU05 | Prevenção de erro | Incluir pontos pendentes ou rejeitados na área. | P03 / T05. | Zero inclusão indevida. | Conferir a área escolhida. |
| MU06 | Eficiência | Localizar detecção anterior do ponto. | P03 / T06. | Tempo ≤ 20 segundos por participante; relatar tempos individuais. | Cronômetro até a resposta. |
| MU07 | Eficiência | Tempo do fluxo completo para cinco pontos. | P03 / T07/T05. | Mediana ≤ 8 minutos somente numa versão com cinco pontos; não avaliável como escrita no FA atual, que usa um ponto. | Tempo registrado apenas como referência na versão atual. |
| MU08 | Compreensão | Identificar se o parecer foi enviado, inclusive após falha simulada. | P03 / T05. | Todos os participantes expostos ao estado; informar `n/N`. | Pergunta e observação. |
| MU09 | Satisfação | Facilidade em escala de 1 a 7. | P03 / T05–T07. | Nota ≥ 5 por participante; informar média somente com amostra comparável. | Pergunta pós-tarefa. |
| MU10 | Eficácia | Proporção que revê a situação do ciclo e registra posição e decisão sem ajuda. | P01 / T09/T04 — atual adaptada (ver situação, identificar o talhão sem inspeção, obter o relatório); posição e decisão são futuras. | Todos os participantes P01 que executarem o fluxo; informar `n/N` e ajudas. Registro de posição não é avaliável no app atual. | Conclusão e intervenções. |
| MU11 | Prevenção de erro | Número de participantes que tratam talhão não inspecionado como “sem focos”. | P01 / T09 — versão atual. | Zero ocorrência quando a diferença estiver visível no cenário. | Pergunta com resposta conhecida. |
| MU12 | Eficiência | Tempo para identificar a tendência do talhão entre ciclos. | P01 / T08 — atual adaptada (comparação com o período anterior). | Tempo ≤ 30 segundos por participante numa versão que apresente a evolução; registrar como não avaliável se ausente. | Cronômetro até a resposta. |
| MU13 | Compreensão | Proporção de participantes expostos à evolução e à última aplicação que respondem corretamente se os dados bastam para concluir sobre a aplicação (`n` corretas / `N` expostos). | P01 / T08 — versão futura. | `n/N = N/N`: todos os expostos respondem corretamente; registrar respostas erradas por tipo. Não avaliável na versão atual. | Resposta comparada à resposta conhecida do cenário. |
| MU14 | Eficiência | Tempo da revisão completa do ciclo. | P01 / T09/T04 — completa futura; tarefa adaptada na versão atual. | Mediana ≤ 10 minutos numa versão com o fluxo completo; na versão parcial, relatar apenas o tempo da tarefa adaptada. | Cronômetro. |
| MU15 | Compreensão | Proporção de participantes expostos ao estado de repasse que distinguem corretamente decisão registrada e repassada, inclusive após falha (`n` corretas / `N` expostos). | P01 / T04 — versão futura; depende de H21. | `n/N = N/N`; registrar cada confusão entre “registrada” e “repassada”. Não avaliável enquanto o repasse não existir. | Pergunta pós-tarefa com resposta conhecida. |
| MU16 | Satisfação | Facilidade em escala de 1 a 7. | P01 / T09/T08/T04 — versão atual, nas tarefas disponíveis. | Nota ≥ 5 por participante; informar média somente com amostra comparável. | Pergunta pós-tarefa. |

**Hierarquia de MU10–MU16:** as medidas essenciais do gestor na versão atual são MU11 (não confundir ausência de inspeção com ausência de praga) e MU10 adaptada, porque um erro nelas leva a decisão de manejo sem dados. MU12, MU14 e MU16 são complementares: orientam ajustes, mas não decidem sozinhas se o fluxo atende. MU13 e MU15 são metas de versão futura e não entram no resultado da versão atual. Esta revisão acrescentou a classificação e a forma de contagem; os limites originais foram mantidos.

**Interpretação de MU01–MU03:** captura e salvamento constituem as medidas essenciais do trabalhador na versão atual. Tempo e facilidade complementam a análise. Cobertura da rota e envio não serão incluídos no resultado quando ausentes.

Tempos estimados posteriormente devem permanecer identificados como estimativas. Comentários positivos não substituem a escala de satisfação.

**Critério geral:** registrar também tentativa e erro, ajudas e comentários. Terminar a tarefa não demonstra, sozinho, clareza da interação. Não alterar os limites depois da coleta para fazer a meta parecer atingida.

### 3.3 Priorização das metas específicas — conteúdo anterior preservado

A tabela abaixo registra a prioridade interna das metas específicas. Ela não substitui a priorização dos cinco atributos de Nielsen solicitada pela disciplina.

| Meta | Peso | Justificativa |
|---|---:|---|
| MU01 — conclusão do fluxo de P02 | 10% | Evitar perda de achados e confusão na rota. |
| MU02 — tempo da captura | 5% | Tarefa repetida em muitos frutos. |
| MU03 — facilidade percebida por P02 | 4% | Apoia a continuidade do uso. |
| MU04 — conclusão do fluxo de P03 | 10% | Integra validação e parecer. |
| MU05 — erro na área delimitada | 10% | Pode afetar diretamente o manejo. |
| MU06 — acesso ao histórico | 5% | Informação necessária à análise. |
| MU07 — tempo do fluxo de P03 | 4% | Esforço da sessão completa. |
| MU08 — compreensão do envio | 6% | Evita conclusão falsa do parecer. |
| MU09 — facilidade percebida por P03 | 4% | Identifica dificuldade técnica. |
| MU10 — conclusão do fluxo de P01 | 10% | Integra cobertura, avaliação e decisão. |
| MU11 — não confundir não inspecionado com sem focos | 10% | Evita decidir com base em ausência de dados. |
| MU12 — tempo de leitura da evolução | 5% | Mede acesso à tendência. |
| MU13 — compreensão da última aplicação | 5% | Evita conclusão equivocada sobre manejo. |
| MU14 — tempo do fluxo de P01 | 4% | Esforço da revisão completa. |
| MU15 — compreensão do repasse | 5% | Distingue decisão registrada de recebida. |
| MU16 — facilidade percebida por P01 | 3% | Identifica dificuldade na revisão. |
| **Total** | **100%** | **MU01–MU16 incluídas.** |

O peso não representa taxa de sucesso. Metas não avaliáveis recebem “não avaliada” na Entrega 14.

### 3.4 Contribuição de Lucas à priorização de Nielsen

Para o trabalhador P02, a prioridade proposta considera os cinco atributos exigidos, sem substituir a consolidação da equipe.

| Atributo | Peso proposto para P02 | Justificativa |
|---|---:|---|
| Baixa taxa de erros | 30% | Evitar captura inadequada, perda de registro e interpretação do percentual como certeza. |
| Eficiência | 30% | A inspeção repete a mesma atividade em muitos frutos. |
| Facilidade de aprendizado | 20% | O trabalhador precisa reconhecer rapidamente como capturar e interpretar as orientações. |
| Satisfação positiva do usuário | 10% | A facilidade percebida ajuda a identificar esforço e frustração. |
| Facilidade de memorização | 10% | Controles consistentes favorecem a retomada da tarefa após interrupções. |
| **Total** | **100%** | |

A facilidade de memorização é um objetivo de design. Não será apresentada como medida empiricamente sem uma avaliação de retorno após intervalo.

**Consolidação pendente:** Pedro e Guilherme deverão acrescentar a perspectiva dos seus perfis e consolidar a prioridade geral dos cinco atributos. Essa consolidação não poderá ser substituída pelos pesos de MU01–MU16.

### 3.5 Contribuição de Pedro à priorização de Nielsen

Para o gestor P01, a prioridade proposta considera os cinco atributos exigidos, sem substituir a consolidação da equipe.

| Atributo | Peso proposto para P01 | Justificativa |
|---|---:|---|
| Baixa taxa de erros | 30% | Ler “não inspecionado” como “sem praga” ou um número automático como confirmado leva a uma decisão de manejo errada. |
| Facilidade de memorização | 30% | O gestor usa o sistema a cada ciclo, com intervalos; precisa reencontrar o caminho sem reaprender. |
| Facilidade de aprendizado | 20% | O gestor conhece pouco a praga e não é usuário técnico; a primeira revisão deve ser compreensível sem treinamento. |
| Eficiência | 10% | A revisão não é repetida dezenas de vezes por dia; tempo importa menos que interpretação correta. |
| Satisfação positiva do usuário | 10% | Indica esforço percebido e apoia a adoção, mas não substitui a interpretação correta. |
| **Total** | **100%** | |

A memorização é um objetivo de design. Não será apresentada como medida sem uma avaliação de retorno após intervalo.

Falta a contribuição de P03 e a consolidação dos três perfis.

## 4. Ciclo de vida

### 4.1 Contribuição de Lucas — Ciclo de Vida da Engenharia de Usabilidade

O fluxo do trabalhador é relacionado ao modelo teórico solicitado no feedback.

| Etapa | Aplicação ao fluxo de P02 | Artefatos relacionados |
|---|---|---|
| Análise de requisitos | Investigar o trabalhador, suas tarefas e tecnologia; definir capacidades, restrições, princípios e metas. | Entregas 3, 5, 7 e 8. |
| Nível 1 — projeto essencial | Examinar como a captura digital altera o trabalho; definir conceitos e conversas; explorar maquetes e revisar sua estrutura. | Entregas 6, 9 e 10. |
| Nível 2 — padrões de telas e diálogos | Definir padrões de captura, resultado e confirmação; materializar o protótipo e planejar testes mais realistas. | Entregas 11 e 12. |
| Nível 3 — projeto detalhado | Integrar os detalhes disponíveis, permissões, bloqueios e recuperação; inspecionar e observar a interação. | Entregas 13 e 14. |
| Instalação e uso | Acompanhar dificuldades em uso continuado e orientar correções e novas versões. | Etapa futura; não apresentada como concluída. |

O ciclo não é linear. Uma dificuldade observada na câmera pode exigir revisão da mensagem, do padrão de interação ou do próprio requisito. Após a mudança, a interação deve ser novamente avaliada.

As metas originais permanecem identificadas. A reorganização desta revisão não será apresentada como planejamento que já existia antes das avaliações anteriores.

### 4.2 Contribuição de Pedro — Ciclo de Vida da Engenharia de Usabilidade

O fluxo do gestor é relacionado ao mesmo modelo teórico.

| Etapa | Aplicação ao fluxo de P01 | Artefatos relacionados |
|---|---|---|
| Análise de requisitos | Perfil do gestor (proto-persona), tarefas T04, T08 e T09, capacidades e restrições, princípios e metas MU10–MU16. O Estudo de Campo I03 foi planejado para confirmar quem decide o manejo, mas ainda não foi aplicado. | Entregas 3, 5, 7 e 8. |
| Nível 1 — projeto essencial | Rever como o gestor passa a ver cobertura, evidência e evolução por talhão; definir conceitos e conversas (CI01, DCC, signos, M03); explorar a maquete G01–G08. | Entregas 6, 9 e 10. |
| Nível 2 — padrões de telas e diálogos | Definir padrões de resumo, mapa, relatório e estados; materializar no perfil Administrador do aplicativo e planejar a avaliação. | Entregas 11 e 12. |
| Nível 3 — projeto detalhado | Integrar detalhes, estados de falha e exportação; inspecionar (A03) e observar o uso (U02). | Entregas 13 e 14. |
| Instalação e uso | Acompanhar gestores reais ao longo de vários ciclos e orientar correções e novas versões. | Etapa futura; não apresentada como concluída. |

O ciclo não é linear. Um problema de interpretação da cobertura retorna ao signo (Entrega 9), à cena S2 do M03 (Entrega 10) e ao padrão de tela (Entrega 11), e deve ser avaliado de novo pela meta MU11. Se o Estudo de Campo mostrar que o gestor não decide o manejo (H21), o retorno é à análise de requisitos e à própria persona.

As metas originais de P01 permanecem identificadas. A reorganização desta revisão não será apresentada como planejamento que já existia antes das avaliações.

### 4.3 Relação anterior entre entregas — preservada para consolidação

A relação abaixo indica o uso dos artefatos, mas não substitui a descrição do ciclo teórico para os demais perfis.

1. **Entrega 7:** confrontar hipóteses sobre rotina, tecnologia, histórico e responsabilidades com os dados que forem coletados. Instrumento preparado não é evidência de participante.
2. **Entrega 6:** registrar feedbacks da iteração formativa, revisões feitas e estados não materializados.
3. **Entrega 11:** identificar as telas do aplicativo para P01/P02 e do Figma para P03, sem declarar cobertura de conversas ausentes.
4. **Entrega 12:** mapear cada meta às tarefas avaliáveis e indicar adaptações e partes não avaliáveis.
5. **Entregas 13 e 14:** confrontar problemas de inspeção com comportamentos observados; medir somente metas às quais os participantes foram expostos.
6. **Após a avaliação:** relacionar evidência, problema, revisão e meta afetada na rastreabilidade.

## 5. Correções ainda necessárias

| Responsável | Correção |
|---|---|
| Guilherme | Separar capacidades, restrições, funcionalidades e contexto de P03; reorganizar seus princípios em negócio e interface; classificar suas metas entre atuais, futuras e hipóteses; explicitar a proporção de respostas corretas em MU08 e hierarquizar as medidas. |
| Pedro | Concluído na revisão de 20/11/2026: seções 1.2, 2.2, 3.1, 3.2 (MU10–MU16), 3.5 e 4.2. |
| Equipe | Consolidar a priorização dos cinco atributos de Nielsen e a aplicação do Ciclo de Vida da Engenharia de Usabilidade aos três perfis. |

As metas e os limites originais dos colegas foram preservados para que os responsáveis realizem essas correções.

## Checklist

- [x] Está claro o limite entre contribuição técnica do TCC e camada interativa.
- [x] Resultados simulados estão diferenciados de evidência de desempenho técnico.
- [x] Metas avaliam a interação, sem substituir métricas técnicas do TCC.
- [x] Capacidades, restrições, funcionalidades e contexto de P02 foram separados.
- [x] Capacidades, restrições, funcionalidades e contexto de P01 foram separados.
- [ ] A mesma separação foi concluída para P03.
- [x] Princípios de P02 estão separados em negócio e interface.
- [x] Princípios de P01 estão separados em negócio e interface.
- [ ] Os princípios de P03 foram reorganizados nos dois grupos.
- [x] Metas qualitativas e quantitativas estão separadas.
- [x] MU01–MU03 distinguem o escopo atual das partes futuras.
- [x] MU10–MU16 e as metas qualitativas de P01 distinguem versão atual, futura e hipótese, com hierarquia.
- [ ] A classificação de escopo e a hierarquia das metas de P03 foram concluídas.
- [x] MU13 e MU15 apresentam explicitamente a variável quantitativa de compreensão.
- [ ] MU08 apresenta explicitamente a variável quantitativa de compreensão.
- [x] As contribuições de P02 e P01 à priorização dos cinco atributos de Nielsen estão documentadas.
- [ ] A priorização dos cinco atributos foi consolidada para a equipe.
- [x] Os fluxos de P02 e P01 foram relacionados ao Ciclo de Vida da Engenharia de Usabilidade.
- [ ] A aplicação do ciclo foi consolidada para os três perfis.
- [x] A revisão distingue metas planejadas de evidências coletadas posteriormente.
- [x] A Entrega 12 permanece como referência para adaptações e partes não avaliáveis.
