# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 01/11/2026  
**Revisão:** 22/11/2026  
**Status:** 🟩 concluído  
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
| Hipótese de contexto | Necessidade de o trabalhador consultar inspeções anteriores (H09/H22) e forma atual de controle do percurso de inspeção. | Investigar com I01 (perguntas 12 e 14, Entrega 7) antes de tratar histórico e rota como necessidades confirmadas de P02. |

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
| Hipótese de contexto | Rotina de ciclo, quem decide o manejo, uso de celular ou computador e uso atual de mapas pelo gestor (H05, H13/H14, H21). | Investigar com gestores reais (I03, Entrega 7, ainda não aplicado) antes de tratar como fato. O mapa é capacidade da plataforma, não necessidade confirmada: em U02 o participante usou o relatório e não abriu o mapa. |

Não foram medidos tempo de carregamento do mapa, tempo de exportação nem limite de registros. Esses valores não serão inventados.

### 1.3 Agrônomo — P03 — Guilherme

Mesma separação usada para P02 e P01. O aplicativo iOS não possui perfil de agrônomo. A plataforma prevista para P03 é uma aplicação web acessada pelo computador, pelo navegador. A versão considerada é o protótipo FA no Figma (Entrega 11), que tem dados fictícios e não está ligado a uma base de dados. Uma capacidade da plataforma não comprova que a funcionalidade correspondente exista.

| Categoria | Característica | Consequência para IHC |
|---|---|---|
| Capacidade técnica | Tela de computador maior que a do celular, com navegador. | Mostrar foto, local e detecções anteriores do ponto na mesma tela, sem trocar de tela para comparar (CTT T07). |
| Capacidade técnica | Exibição de imagens com ampliação. | Permitir examinar a foto em detalhe antes do veredito. |
| Capacidade técnica | Exibição de mapa do talhão com pontos georreferenciados. | Permitir localizar o ponto pelo espaço e delimitar a área de aplicação sobre o mapa. |
| Capacidade técnica | Armazenamento e consulta de registros por ponto e por período em servidor. | Viabilizar o histórico do ponto e a comparação com inspeções anteriores. |
| Capacidade técnica | Acesso remoto pela rede. | Permitir que o agrônomo analise os pedidos fora da propriedade. |
| Restrição da plataforma | Não há perfil de agrônomo no aplicativo iOS. | Avaliar o fluxo de P03 apenas no protótipo FA, sem atribuí-lo ao aplicativo. |
| Restrição da plataforma | Layout projetado para computador; uso em celular durante visitas não foi projetado. | Não generalizar os resultados para o uso móvel. |
| Restrição da plataforma | A aplicação web depende de conexão com o servidor para receber pedidos e enviar o parecer. | Comunicar carregamento, envio, sucesso e falha, com caminho de recuperação. |
| Restrição da versão | O protótipo FA simula o veredito, o pedido de nova foto, a área e o envio por links entre quadros e não guarda as escolhas. Só o ponto 3 abre a detecção, a área já vem desenhada e a falha de envio (FA07E) não está no caminho navegável. | Cliques sem efeito no protótipo não contam como erro do participante; metas dependentes dessas partes são adaptadas ou não avaliadas (Entrega 12). |
| Restrição da versão | A foto da detecção é uma ilustração, não uma foto real. | Não tirar conclusões sobre a leitura de fotos reais nem sobre a influência real da IA no julgamento. |
| Funcionalidade atual (protótipo FA) | Pedidos de parecer, mapa do talhão com situação dos pontos, detecção com foto ampliável e avaliação da IA, histórico do ponto, veredito (confirmar, rejeitar, pedir nova foto), área de aplicação, parecer e confirmação de envio. | São as partes avaliáveis nas Entregas 13 e 14, com dados fictícios. |
| Funcionalidade futura | Integração com os registros enviados por P02, validação de todos os pontos do talhão, desenho livre da área, falha e reenvio navegáveis e recebimento da nova foto pedida. | Não atribuir ao protótipo atual; metas que dependem delas ficam “não avaliadas”. |
| Papel do usuário | O agrônomo valida as detecções e emite o parecer; o resultado do modelo não é parecer agronômico, e o parecer não substitui o receituário agronômico. | Distinguir indicação da IA, veredito humano e parecer enviado. |
| Dependência do processo | O agrônomo só analisa o que foi fotografado e registrado em campo. | Oferecer saída quando a evidência for insuficiente (pedir nova foto) e indicar quando não há registro. |
| Contexto de uso | Análise a distância, no escritório, de pedidos de várias propriedades, algumas vezes por mês (T05). | Favorecer a retomada após intervalo: termos estáveis e pedidos agrupados. |
| Hipótese de contexto | Existência do papel de P03, dispositivos usados, uso atual de mapas digitais, estabilidade da conexão, volume real de registros e comunicação entre papéis (H04, H07, H21, H22). | Investigar com agrônomos reais (I02, Entrega 7, ainda não aplicada) antes de tratar como fato. |

Não foram medidos tempo de carregamento das fotos, tempo de envio do parecer nem limite de registros. Esses valores não serão inventados.

## 2. Princípios gerais do projeto

**Rótulos provisórios:** os termos usados nos princípios e nas telas (por exemplo, “sinal suspeito”, “não inspecionado”, “foco”, “pedir nova foto”) vêm dos signos das Entregas 9 e 10 e ainda não foram confrontados com o vocabulário espontâneo dos usuários. Permanecem provisórios até a análise de I01 (bloco 6) e I03 (item O9) da Entrega 7.

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

### 2.3 Princípios relacionados ao agrônomo — Guilherme

O contexto de P03 (análise a distância, dependente do que foi registrado em campo, com responsabilidade técnica pelo parecer) funciona como justificativa; os princípios abaixo são as regras que orientam o design. Os itens antes listados sem grupo nesta seção foram distribuídos aqui.

#### Princípios direcionados ao negócio

| Princípio | Justificativa | Decisão decorrente | Fonte |
|---|---|---|---|
| O parecer é responsabilidade do agrônomo. | Orientação de manejo exige julgamento profissional. | Não apresentar o resultado do modelo como parecer agronômico; informar que o parecer não substitui o receituário agronômico. | Cenário C03; HTA T05. |
| Só pontos validados por pessoa entram na área de aplicação. | A indicação do modelo não equivale a confirmação; incluir ponto não confirmado pode levar a aplicação em área errada (T05 crítica). | Usar como base da área apenas pontos confirmados; pendentes e rejeitados ficam fora. | CTT T07; HTA T05. |
| Pedir nova foto não é confirmar nem rejeitar. | A evidência insuficiente não permite veredito. | Manter o ponto como pendente até chegar nova evidência. | CTT T07; cenário C03. |
| Minimizar dados de pessoas e propriedades. | Fotos, mapas e pareceres podem identificar propriedades, trabalhadores e o profissional. | Mostrar apenas a identificação necessária à tarefa e limitar o acesso ao agrônomo responsável. | LGPD (Lei nº 13.709/2018); planejamento ético da Entrega 7. |
| Cobertura sem vigilância individual. | Informações da rota podem ser lidas como controle do trabalhador. | Mostrar pontos e datas por talhão, sem desempenho por pessoa. | Cenário C02; minimização de dados. |
| Registrar autoria e data do veredito e do parecer. | O parecer e os vereditos precisam ser atribuíveis quando questionados depois. | Guardar quem validou, quem emitiu o parecer e quando. | MoLIC M01 (Entrega 10). |

#### Princípios direcionados à interface

| Princípio | Justificativa | Decisão decorrente | Fonte |
|---|---|---|---|
| Distinguir indicação da IA e veredito humano. | O profissional pode aceitar automaticamente uma indicação da IA. | Identificar a origem de cada estado; permitir confirmar, rejeitar ou pedir nova foto. | Diretrizes de interação humano–IA (AMERSHI et al., 2019); CTT T07. |
| Tornar visível a situação dos pontos e do parecer. | O agrônomo precisa saber o que falta validar e se o parecer chegou ao gestor. | Mostrar pendente, confirmado e rejeitado no mapa; confirmar envio e indicar falha. | Heurística de Nielsen: visibilidade do estado do sistema. |
| Prevenir erros e indicar recuperação. | Pontos pendentes perto da área, campos inválidos e falha de envio podem gerar parecer errado ou perdido. | Avisar sobre pontos pendentes, validar campos e manter o parecer para reenvio após falha. | Heurísticas de Nielsen: prevenção de erros; ajudar a reconhecer, diagnosticar e recuperar erros. |
| Reconhecer em vez de lembrar. | Comparar a foto com inspeções anteriores exige ver as duas informações. | Mostrar foto, local e detecções anteriores do ponto na mesma tela. | Heurística de Nielsen: reconhecimento em vez de memorização; CTT T07. |
| Oferecer saída quando a evidência não basta. | A análise depende do que foi registrado em campo. | Permitir pedir nova foto ou encerrar a revisão sem concluir o parecer. | Heurística de Nielsen: controle e liberdade do usuário; cenário C03. |
| Não depender só de cor e garantir contraste. | Estados do mapa são lidos rapidamente e por pessoas com diferentes percepções de cor. | Usar símbolo, texto e cor (○ pendente, ● confirmado, × rejeitado) e verificar contraste. | WCAG 2.2 (1.4.1 Uso de cor; 1.4.3 Contraste). |
| Manter termos e cores consistentes entre os perfis. | O parecer e os pontos são vistos também por P01 e P02. | Usar a mesma semântica de cor e os signos das Entregas 9 e 10. | Heurística de Nielsen: consistência e padronização. |

**Referências:** NIELSEN, J. *10 Usability Heuristics for User Interface Design*, disponível em <https://www.nngroup.com/articles/ten-usability-heuristics/>; W3C. *WCAG 2.2*, disponível em <https://www.w3.org/TR/WCAG22/>; AMERSHI, S. et al. *Guidelines for Human-AI Interaction*. CHI 2019, disponível em <https://doi.org/10.1145/3290605.3300233>; BRASIL. *Lei nº 13.709/2018 (LGPD)*, disponível em <https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm>.

## 3. Metas de usabilidade

As metas são critérios planejados. A Entrega 12 registra quais podem ser avaliadas como escritas, quais precisam de adaptação e quais não são avaliáveis na versão disponível.

Não apresentar funcionalidade ausente como erro do participante.

### 3.1 Metas qualitativas

| Meta | Perfil/tarefa | Evidência desejada |
|---|---|---|
| Compreender o resultado sem atribuir certeza indevida à IA. | P02 / T02 — versão atual. | Explica que a indicação do modelo não é confirmação profissional e que ausência de sinal na foto não garante árvore livre. |
| Recuperar-se de captura inadequada. | P02 / T02 — versão atual. | Ajusta a captura em resposta às orientações; repetição ou resultado inconclusivo somente quando disponíveis. |
| Distinguir cobertura e envio. | P02 / T01/T03 — versão futura nas partes ausentes. | Identifica pontos pendentes e diferencia registro local de envio. Não avaliar esses estados no aplicativo quando ausentes. |
| Diferenciar detecção da IA e validação humana. | P03 / T07 — versão atual (protótipo FA). | Identifica o que depende do veredito do agrônomo. |
| Compreender o pedido de nova foto. | P03 / T07 — versão atual (protótipo FA); o recebimento da nova foto é futuro. | Entende que o ponto permanece pendente. |
| Compreender a situação do parecer. | P03 / T05 — versão atual parcial: confirmação de envio; a falha de envio é futura (FA07E fora do caminho navegável). | Identifica conclusão e falha de envio. |
| Avaliar suficiência do contexto. | P03 / T05/T06 — versão atual com dados fictícios; a suficiência com fotos reais depende de H07. | Consulta foto, local e histórico ou pede outra evidência. |
| Observar influência da IA no julgamento. | P03 / T07 — hipótese: a foto é ilustrativa, e o resultado na versão atual é apenas indício. | Explica quando consultou a indicação automática e como a usou. |
| Identificar estados sem depender só da cor. | P03 / T07 — versão atual (protótipo FA). | Diferencia pendente, confirmado e rejeitado por texto/símbolo. |
| Distinguir “sem focos” de “não inspecionado”. | P01 / T09 — versão atual: o talhão sem inspeção existe nos dados; o estado explícito ainda não. | Explica que ausência de inspeção não significa ausência de praga. |
| Compreender saídas diante de dúvida. | P01 / T09 — versão futura; depende de H21. | Distingue pedir parecer e pedir reinspeção, se essas ações existirem na versão. |
| Interpretar evolução entre ciclos. | P01 / T08 — versão atual parcial (comparação com o período anterior); evolução por ciclo e cobertura são futuras. | Identifica tendência e limites de cobertura quando disponíveis. |
| Observar influência do resultado automático na decisão. | P01 / T09/T04 — hipótese: na versão atual, as contagens do talhão vêm do modelo sem validação humana. | Explica de onde vêm os números do talhão e se os trataria como confirmação antes de decidir. |
| Interpretar ordenação como dado. | P01 / T04 — versão atual (talhões críticos em Relatórios). | Explica o significado da ordem da lista sem presumir recomendação automática. |
| Distinguir decisão registrada e repassada. | P01 / T04 — versão futura; depende de H21. | Identifica a situação real do repasse quando o fluxo existir. |

As metas de P01 foram classificadas na revisão de 20/11/2026. “Depende de H21” indica que, além de ausente na versão, a meta pressupõe que o gestor decide e repassa o manejo, hipótese ainda não confirmada com gestores reais. As metas de P03 foram classificadas na revisão de 22/11/2026; todas pressupõem que o agrônomo valida detecções e emite parecer a distância (H04, H07), hipótese ainda não confirmada com agrônomos reais.

### 3.2 Metas quantitativas

**Condições:** usar cenários e dados equivalentes por perfil, registrar ajuda separadamente e informar `n/N`. A Entrega 14 prevê três participantes no total da equipe, não três em cada perfil.

Uma observação isolada não permite generalização estatística.

| ID | Dimensão | Métrica | Tarefa/escopo | Meta proposta | Como medir |
|---|---|---|---|---|---|
| MU01 | Eficácia | Proporção que fotografa e salva um achado sem ajuda; identificação de ponto pendente registrada separadamente. | P02 / T01–T03; P01–P06 conceituais. | Todos os participantes P02 expostos à tarefa; informar `n/N`. Captura e salvamento são avaliáveis; ponto pendente da rota permanece futuro. | Registrar conclusão, erros e ajudas por etapa. Não declarar o fluxo conceitual completo como atendido pela conclusão parcial. |
| MU02 | Eficiência | Tempo da abertura da câmera à confirmação de registro. | P02 / T02 — versão atual. | Mediana ≤ 60 segundos quando houver mais de uma medição comparável; com uma pessoa, informar o tempo individual. | Cronômetro; registrar repetição da foto. |
| MU03 | Satisfação | Facilidade em escala de 1 a 7 após cada fluxo disponível. | P02 / PF01/PF02. | Nota ≥ 5 por participante; calcular mediana se houver amostra comparável. | Pergunta pós-tarefa. Se a escala não foi aplicada, registrar “não medida”, sem converter comentários em nota. |
| MU04 | Eficácia | Abrir pedido, validar pontos, delimitar área e enviar parecer. | P03 / T07/T05 — atual adaptada (validar o ponto 3, único que o protótipo FA abre); validação de todos os pontos é futura. | Todos os participantes P03 que executarem o fluxo; informar `n/N` e ajudas. | Conclusão e intervenções; adaptar ao número de pontos do FA. |
| MU05 | Prevenção de erro | Incluir pontos pendentes ou rejeitados na área. | P03 / T05 — atual adaptada (a área já vem desenhada no protótipo FA); desenho livre da área é futuro. | Zero inclusão indevida. | Conferir a área escolhida. |
| MU06 | Eficiência | Localizar detecção anterior do ponto. | P03 / T06 — versão atual. | Tempo ≤ 20 segundos por participante; relatar tempos individuais. | Cronômetro até a resposta. |
| MU07 | Eficiência | Tempo do fluxo completo para cinco pontos. | P03 / T07/T05 — versão futura. | Mediana ≤ 8 minutos somente numa versão com cinco pontos; não avaliável como escrita no FA atual, que usa um ponto. | Tempo registrado apenas como referência na versão atual. |
| MU08 | Compreensão | Proporção de participantes expostos à confirmação de envio que respondem corretamente se o parecer foi enviado (`n` corretas / `N` expostos); após falha simulada, contagem separada. | P03 / T05 — atual adaptada (confirmação de envio); compreensão após falha é futura (FA07E fora do caminho navegável). | `n/N = N/N`: todos os expostos respondem corretamente; registrar cada resposta errada. Não avaliável após falha na versão atual. | Resposta comparada à resposta conhecida do cenário. |
| MU09 | Satisfação | Facilidade em escala de 1 a 7. | P03 / T05–T07 — versão atual, nas tarefas disponíveis. | Nota ≥ 5 por participante; informar média somente com amostra comparável. | Pergunta pós-tarefa. |
| MU10 | Eficácia | Proporção que revê a situação do ciclo e registra posição e decisão sem ajuda. | P01 / T09/T04 — atual adaptada (ver situação, identificar o talhão sem inspeção, obter o relatório); posição e decisão são futuras. | Todos os participantes P01 que executarem o fluxo; informar `n/N` e ajudas. Registro de posição não é avaliável no app atual. | Conclusão e intervenções. |
| MU11 | Prevenção de erro | Número de participantes que tratam talhão não inspecionado como “sem focos”. | P01 / T09 — versão atual. | Zero ocorrência quando a diferença estiver visível no cenário. | Pergunta com resposta conhecida. |
| MU12 | Eficiência | Tempo para identificar a tendência do talhão entre ciclos. | P01 / T08 — atual adaptada (comparação com o período anterior). | Tempo ≤ 30 segundos por participante numa versão que apresente a evolução; registrar como não avaliável se ausente. | Cronômetro até a resposta. |
| MU13 | Compreensão | Proporção de participantes expostos à evolução e à última aplicação que respondem corretamente se os dados bastam para concluir sobre a aplicação (`n` corretas / `N` expostos). | P01 / T08 — versão futura. | `n/N = N/N`: todos os expostos respondem corretamente; registrar respostas erradas por tipo. Não avaliável na versão atual. | Resposta comparada à resposta conhecida do cenário. |
| MU14 | Eficiência | Tempo da revisão completa do ciclo. | P01 / T09/T04 — completa futura; tarefa adaptada na versão atual. | Mediana ≤ 10 minutos numa versão com o fluxo completo; na versão parcial, relatar apenas o tempo da tarefa adaptada. | Cronômetro. |
| MU15 | Compreensão | Proporção de participantes expostos ao estado de repasse que distinguem corretamente decisão registrada e repassada, inclusive após falha (`n` corretas / `N` expostos). | P01 / T04 — versão futura; depende de H21. | `n/N = N/N`; registrar cada confusão entre “registrada” e “repassada”. Não avaliável enquanto o repasse não existir. | Pergunta pós-tarefa com resposta conhecida. |
| MU16 | Satisfação | Facilidade em escala de 1 a 7. | P01 / T09/T08/T04 — versão atual, nas tarefas disponíveis. | Nota ≥ 5 por participante; informar média somente com amostra comparável. | Pergunta pós-tarefa. |

**Hierarquia de MU10–MU16:** as medidas essenciais do gestor na versão atual são MU11 (não confundir ausência de inspeção com ausência de praga) e MU10 adaptada, porque um erro nelas leva a decisão de manejo sem dados. MU12, MU14 e MU16 são complementares: orientam ajustes, mas não decidem sozinhas se o fluxo atende. MU13 e MU15 são metas de versão futura e não entram no resultado da versão atual. Esta revisão acrescentou a classificação e a forma de contagem; os limites originais foram mantidos.

**Hierarquia de MU04–MU09:** as medidas essenciais do agrônomo na versão atual são MU05 (não incluir ponto não confirmado na área), MU04 adaptada e MU08 adaptada, porque um erro nelas leva a aplicação em área errada ou a supor que o gestor recebeu um parecer que não chegou (T05 é tarefa crítica na Entrega 5). MU06 e MU09 são complementares: orientam ajustes, mas não decidem sozinhas se o fluxo atende. MU07 e a parte de MU08 após falha são metas de versão futura e não entram no resultado da versão atual. Esta revisão acrescentou a classificação e a forma de contagem; os limites originais foram mantidos.

**Interpretação de MU01–MU03:** captura e salvamento constituem as medidas essenciais do trabalhador na versão atual. Tempo e facilidade complementam a análise. Cobertura da rota e envio não serão incluídos no resultado quando ausentes.

Tempos estimados posteriormente devem permanecer identificados como estimativas. Comentários positivos não substituem a escala de satisfação.

**Critério geral:** registrar também tentativa e erro, ajudas e comentários. Terminar a tarefa não demonstra, sozinho, clareza da interação. Não alterar os limites depois da coleta para fazer a meta parecer atingida.

### 3.3 Priorização dos cinco atributos de usabilidade de Nielsen

Esta é a priorização solicitada na atividade. Usa exclusivamente os cinco atributos de Nielsen: facilidade de aprendizado, facilidade de memorização, eficiência, baixa taxa de erros e satisfação positiva do usuário. Cada integrante propôs os pesos para o seu perfil, e a seção 3.3.4 consolida a prioridade da equipe.

#### 3.3.1 Contribuição de Lucas — trabalhador P02

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

#### 3.3.2 Contribuição de Pedro — gestor P01

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


#### 3.3.3 Contribuição de Guilherme — agrônomo P03

Para o agrônomo P03, a prioridade proposta considera os cinco atributos exigidos, sem substituir a consolidação da equipe.

| Atributo | Peso proposto para P03 | Justificativa |
|---|---:|---|
| Baixa taxa de erros | 35% | Confirmar uma detecção errada ou incluir ponto pendente ou rejeitado na área leva a aplicação em área errada; T05 é tarefa crítica (Entrega 5). |
| Facilidade de memorização | 25% | O parecer é emitido algumas vezes por mês (T05); o agrônomo precisa reencontrar o caminho e o significado dos estados sem reaprender. |
| Eficiência | 15% | A validação se repete a cada detecção positiva (T07), mas o julgamento técnico importa mais que o tempo. |
| Facilidade de aprendizado | 15% | O agrônomo tem alto conhecimento do domínio; o que precisa aprender é a interface, não a praga. |
| Satisfação positiva do usuário | 10% | Indica esforço percebido e apoia a adoção, mas não substitui a validação correta. |
| **Total** | **100%** | |

A memorização é um objetivo de design. Não será apresentada como medida sem uma avaliação de retorno após intervalo.

#### 3.3.4 Priorização consolidada da equipe

A consolidação usa a média simples dos pesos dos três perfis, arredondada para somar 100%.

| Atributo | P02 | P01 | P03 | Equipe | Ordem |
|---|---:|---:|---:|---:|---:|
| Baixa taxa de erros | 30% | 30% | 35% | 32% | 1º |
| Facilidade de memorização | 10% | 30% | 25% | 22% | 2º |
| Eficiência | 30% | 10% | 15% | 18% | 3º |
| Facilidade de aprendizado | 20% | 20% | 15% | 18% | 3º |
| Satisfação positiva do usuário | 10% | 10% | 10% | 10% | 5º |
| **Total** | **100%** | **100%** | **100%** | **100%** | |

**Interpretação:** baixa taxa de erros é a prioridade nos três perfis, porque nos três o erro de interpretação (percentual como certeza, “não inspecionado” como “sem praga”, ponto não confirmado na área) leva a decisão de manejo errada. Memorização vem em segundo porque gestor e agrônomo usam o sistema com intervalos. Eficiência pesa mais para o trabalhador, que repete a captura em muitos frutos; a média esconde essa diferença, e por isso os pesos por perfil continuam valendo para o fluxo de cada um.

**Consequência para a avaliação:** as metas de prevenção de erro (MU05 e MU11) e as metas de compreensão que evitam interpretação errada recebem atenção prioritária; metas de tempo e de satisfação são complementares. Esta priorização foi feita na revisão de 22/11/2026, depois das avaliações das Entregas 13 e 14. Ela não orientou aquelas avaliações e será aplicada nas próximas iterações.

### 3.4 Prioridade das metas específicas do projeto (complementar)

A tabela abaixo registra a prioridade interna das metas específicas. Ela não substitui a priorização dos cinco atributos de Nielsen (seção 3.3) e foi mantida como ferramenta interna.

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

### 4.3 Contribuição de Guilherme — Ciclo de Vida da Engenharia de Usabilidade

O fluxo do agrônomo é relacionado ao mesmo modelo teórico.

| Etapa | Aplicação ao fluxo de P03 | Artefatos relacionados |
|---|---|---|
| Análise de requisitos | Perfil do agrônomo (proto-persona P03), cenário C03, tarefas T05, T06 e T07 (HTA, GOMS e CTT), capacidades e restrições, princípios e metas MU04–MU09. A entrevista I02 foi planejada para confirmar o papel do agrônomo, mas ainda não foi aplicada. | Entregas 3, 4, 5, 7 e 8. |
| Nível 1 — projeto essencial | Reengenharia do trabalho: fotos soltas e relatos informais passam a chegar como pedidos de parecer com foto, local e histórico; a IA indica, o agrônomo valida, e só pontos confirmados entram na área. Definir conceitos e conversas (signos, MoLIC M01) e explorar a maquete A01–A07 em papel. | Entregas 6, 9 e 10. |
| Nível 2 — padrões de telas e diálogos | Definir padrões de layout de computador, menu lateral, situação dos pontos com símbolo, texto e cor e mesma semântica de cor dos outros perfis; materializar no protótipo FA no Figma, que dialoga com o usuário sem estar ligado a uma base de dados; planejar a avaliação. | Entregas 11 e 12. |
| Nível 3 — projeto detalhado | Integrar estados não essenciais (nenhum pedido, falha ao registrar, nenhuma detecção no período, campos inválidos, falha no envio); inspecionar as telas FA e observar o uso (U03). Etapa parcial: o protótipo não é o sistema final, e a falha de envio não está no caminho navegável. | Entregas 13 e 14. |
| Instalação e uso | Acompanhar agrônomos reais emitindo pareceres em vários ciclos e orientar correções e novas versões. | Etapa futura; não apresentada como concluída. |

O ciclo não é linear. Na passagem do papel ao Figma, as telas A04 (pedir nova foto) e A08 (situação do parecer) foram retiradas e incorporadas a outras telas, e o formato de celular deu lugar ao de computador para manter foto e histórico na mesma tela. Um problema de compreensão do ponto com nova foto pedida retorna ao signo (Entrega 9), à conversa de M01 (Entrega 10) e ao padrão de estado (Entrega 11), e deve ser avaliado de novo. Se a entrevista I02 mostrar que o agrônomo não emite parecer a distância (H04, H07), o retorno é à análise de requisitos e à própria persona.

As metas originais de P03 permanecem identificadas. A reorganização desta revisão não será apresentada como planejamento que já existia antes das avaliações.

### 4.4 Ciclo de Vida da Engenharia de Usabilidade — consolidação da equipe

O projeto adota o Ciclo de Vida da Engenharia de Usabilidade (Mayhew, apresentado em Barbosa e Silva, 2010). Os níveis 1 a 3 são repetidos para cada grupo de funcionalidades essenciais; no projeto, cada perfil (P02, P01 e P03) corresponde a um grupo, e por isso os perfis estão em etapas diferentes.

| Etapa | O que o projeto realizou | Onde o projeto está |
|---|---|---|
| Análise de requisitos | Proto-personas P01–P03, cenários, tarefas (HTA, GOMS, CTT), análise da concorrência, capacidades e restrições, princípios de negócio e de interface, metas qualitativas e quantitativas e priorização de Nielsen (Entregas 1 a 5, 7 e 8). | Feita com base em hipóteses: os instrumentos da Entrega 7 não foram aplicados a usuários reais. |
| Nível 1 — projeto essencial | Reengenharia do trabalho de captura, validação e decisão; modelo conceitual e MoLIC; maquetes em papel com avaliação formativa (Entregas 6, 9 e 10). | Concluído para os três perfis. |
| Nível 2 — padrões de telas e diálogos | Padrões de telas e cores; aplicativo iOS (P02 e P01) e protótipo FA (P03); planejamento da avaliação (Entregas 11 e 12). | Concluído para os três perfis, com partes futuras identificadas. |
| Nível 3 — projeto detalhado | Estados não essenciais e de falha; avaliação heurística e observação de usuários (Entregas 13 e 14). | Parcial: P02 e P01 avaliados no aplicativo, P03 no protótipo; nem todos os estados existem nas versões avaliadas. |
| Instalação e uso | Feedback após uso continuado, correções e novos releases. | Não iniciada. |

**Retorno das avaliações:** cada problema encontrado nas Entregas 13 e 14 é registrado na `RASTREABILIDADE.md` com a etapa a que retorna: à análise de requisitos (se refuta uma hipótese sobre usuário, tarefa ou papel), ao modelo conceitual (se o signo ou a conversa foi mal compreendido), aos padrões de telas (se o problema se repete entre telas) ou ao projeto detalhado (se é um estado ou mensagem isolada). Após a mudança, a meta afetada é avaliada de novo. Os resultados posteriores são comparados com as metas definidas antes da coleta, sem alterar os limites.

## Checklist

- [x] Está claro o limite entre contribuição técnica do TCC e camada interativa.
- [x] Resultados simulados estão diferenciados de evidência de desempenho técnico.
- [x] Metas avaliam a interação, sem substituir métricas técnicas do TCC.
- [x] Capacidades, restrições, funcionalidades e contexto de P02 foram separados.
- [x] Capacidades, restrições, funcionalidades e contexto de P01 foram separados.
- [x] A mesma separação foi concluída para P03.
- [x] Princípios de P02 estão separados em negócio e interface.
- [x] Princípios de P01 estão separados em negócio e interface.
- [x] Os princípios de P03 foram reorganizados nos dois grupos.
- [x] Descrições de contexto aparecem como justificativa, não como princípio.
- [x] Metas qualitativas e quantitativas estão separadas.
- [x] MU01–MU03 distinguem o escopo atual das partes futuras.
- [x] MU10–MU16 e as metas qualitativas de P01 distinguem versão atual, futura e hipótese, com hierarquia.
- [x] MU04–MU09 e as metas qualitativas de P03 distinguem versão atual, futura e hipótese, com hierarquia.
- [x] MU08, MU13 e MU15 apresentam explicitamente a variável quantitativa de compreensão.
- [x] A priorização usa exclusivamente os cinco atributos de Nielsen e vem antes da prioridade de MU01–MU16.
- [x] As contribuições dos três perfis à priorização de Nielsen estão documentadas.
- [x] A priorização consolidada dos cinco atributos foi validada pela equipe.
- [x] O ciclo de vida é descrito pelo Ciclo de Vida da Engenharia de Usabilidade, e não por sequência de entregas.
- [x] Os fluxos de P02, P01 e P03 foram relacionados ao ciclo.
- [x] A consolidação do ciclo para os três perfis foi validada pela equipe.
- [x] A revisão distingue metas planejadas de evidências coletadas posteriormente.
- [x] A Entrega 12 permanece como referência para adaptações e partes não avaliáveis.
- [x] Uso atual de mapas, histórico para P02, controle do percurso e vocabulário dos rótulos estão identificados como hipóteses abertas.
