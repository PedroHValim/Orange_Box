# Entrega 6 — Prototipação em papel

**Data:** 15/11/2026  
**Status:** 🟩 concluída — iteração formativa e revisão documentadas  
**Responsabilidade:** 1 solução integrada por equipe (Lucas Cabral, Guilherme e Pedro)

## Objetivo da atividade

Explorar a estrutura da interação em baixa fidelidade pelo ciclo **construir → simular → observar → revisar**. Os desenhos em papel registram a concepção inicial; as capturas do aplicativo registram a revisão realizada após os feedbacks. A avaliação descrita abaixo é formativa e não substitui o teste com participantes finais da Entrega 14.

## 1. Escopo do protótipo

### Funcionalidade — Lucas Cabral

**Funcionalidade:** inspecionar frutos com a câmera e consultar os achados da rota.  
**Persona:** P02 — Antônio Ferreira, trabalhador de campo/pragueiro.  
**Cenários/tarefas:** C02; T01 e T03 (inspecionar a rota e repassar achados); T02 (fotografar o fruto e interpretar o resultado).  
**Objetivo:** orientar a captura, mostrar o andamento da análise, comunicar o resultado e permitir retomar os registros da inspeção.

### Funcionalidade — Guilherme

**Funcionalidade:** examinar detecções e emitir parecer técnico.  
**Persona:** P03 — Marcelo Fidalgo, agrônomo consultor.  
**Cenários/tarefas:** C03; T07 (validar detecções), T06 (consultar histórico) e T05 (delimitar a área e emitir parecer).  
**Objetivo:** distinguir a indicação da IA da avaliação humana, conferir evidências e histórico e registrar a orientação técnica.

### Funcionalidade — Pedro

**Funcionalidade:** acompanhar talhões e decidir o manejo da fazenda.  
**Persona:** P01 — Jaime Carteiro, dono da fazenda.  
**Cenários/tarefas:** C01; T09 (revisar resultados), T08 (avaliar evolução) e T04 (planejar manejo).  
**Objetivo:** localizar talhões que exigem atenção, consultar informações resumidas e registrar ou encaminhar decisões.

## 1.1 Famílias de interface escolhidas

- **Lucas:** captura de imagem, acompanhamento da análise e resultado da inspeção.
- **Guilherme:** pedidos de parecer, mapa de detecções, detalhe, histórico e registro do parecer.
- **Pedro:** mapa com filtros e seleção de talhão, histórico e relatório para apoiar decisões.

Não foram incluídas telas de login, administração ou CRUD apenas para aumentar o número de telas.

## 2. Fluxos escolhidos

| Responsável | Fluxo | Tarefa/objetivo | Por que foi priorizado |
|---|---|---|---|
| Lucas | PF01 | Fotografar um fruto, acompanhar a análise e interpretar o resultado (T02). | A captura e a leitura do resultado afetam diretamente a qualidade do registro. |
| Lucas | PF02 | Retomar achados da inspeção e conferir a rota (T01/T03). | O trabalhador precisa localizar o que já foi registrado. |
| Guilherme | PF03 | Abrir uma detecção, examinar foto e histórico e validar ou pedir nova foto (T07/T06). | Evita tratar uma indicação automática como diagnóstico confirmado. |
| Guilherme | PF04 | Delimitar a área e emitir o parecer (T05). | Conecta a evidência à orientação enviada ao gestor. |
| Pedro | PF05 | Localizar talhões com ocorrências e examinar os resultados (T09). | Ajuda o gestor a decidir o que merece inspeção ou ação. |
| Pedro | PF06 | Consultar histórico e relatório antes de definir o manejo (T08/T04). | A decisão depende do contexto e da evolução, não de um ponto isolado. |

## 3. Telas e estados

Os códigos abaixo identificam estados da conversa. **Papel** indica o que foi fotografado no desenho inicial; **app revisado** indica a captura do aplicativo após a discussão. Estados previstos, mas não visíveis nas fotos, são explicitados como tal e não são apresentados como desenhos concluídos.

### Funcionalidade — Lucas Cabral

| Estado | Conteúdo e controles | Evidência |
|---|---|---|
| P01 | Início/rota de inspeção → abrir câmera. | Planejado no fluxo; não aparece na fotografia do papel. |
| P02 | Câmera: enquadrar o fruto; capturar → P03; voltar → inspeção. | Desenho em `Tela1-Tela2.jpeg`; câmera implementada em `Camera.jpeg`. |
| P03 | Análise: informar andamento e aguardar resultado → P04; voltar/cancelar → P02, se disponível. | A captura `Camera.jpeg` mostra o feedback de processamento; o estado completo não foi fotografado em papel. |
| P04 | Resultado da inspeção: examinar achado e dados associados; refazer captura → P02. | Desenho em `Tela1-Tela2.jpeg`; demais retornos dependem da implementação. |
| P05–P07 | Confirmação do registro, revisão da rota e situação do envio. | Caminhos previstos; não há fotografias desses estados em papel nesta entrega. |

**Caminho principal representado:** captura P02 → análise P03 → resultado P04. **Retorno relevante:** refazer uma foto inadequada. Não inferir que “sem sinal nesta foto” signifique ausência de pragas em toda a árvore ou no talhão. A captura do app exibe orientação para aproximar a câmera e um indicador de andamento da busca.

![Protótipo em papel — captura e resultado de Lucas](../assets/06_prototipos/Tela1-Tela2.jpeg)

![Revisão no aplicativo — câmera e feedback de análise](../assets/06_prototipos/Camera.jpeg)

### Funcionalidade — Guilherme

| Estado | Conteúdo e controles | Evidência |
|---|---|---|
| A01 | Lista de pedidos de parecer por fazenda; abrir pedido → A02. | `prototipo_fluxo_2-1.jpeg`. |
| A02 | Detecções no talhão e situação dos pontos; escolher ponto → A03; histórico → A05; área → A06. | `prototipo_fluxo_2-1.jpeg`. |
| A03 | Foto e contexto da detecção; aprovar, rejeitar ou pedir nova foto → A02. | `prototipo_fluxo_2-1.jpeg`. A porcentagem desenhada é uma indicação da IA, não confirmação agronômica. |
| A05 | Histórico de detecções; retornar → A02. | `prototipo_fluxo_2-2.jpeg`; captura revisada em `Historico.jpeg`. |
| A06 | Área de aplicação desenhada sobre o talhão; continuar → A07; voltar → A02. | `prototipo_fluxo_2-2.jpeg`. |
| A07 | Parecer com orientação, produto, dose e período; enviar → A01. | `prototipo_fluxo_2-2.jpeg`. |

**Caminho principal:** A01 → A02 → A03 → A02 → A06 → A07 → A01. **Alternativas:** A02 → A05 → A02 para consultar o histórico; em A03, pedir nova foto quando a evidência for insuficiente. O botão de pedir nova foto foi incorporado ao detalhe, e a situação do parecer retorna à lista de pedidos, sem telas separadas para essas ações.

**Formato dos desenhos:** as telas A01–A07 seguem o formato do aplicativo de celular (tela em retrato), porque nesta entrega o fluxo de P03 ainda era tratado como parte do app usado em campo. Com essa divisão, A02 (talhão), A03 (detecção) e A05 (histórico) ficam em telas separadas, e comparar a foto com o histórico exige trocar de tela, o que contraria o CTT T07 (Entrega 5), segundo o qual imagem, zoom e histórico precisam estar acessíveis na mesma tela. Por isso, na Entrega 11 o fluxo passa para o layout de computador (ver `RASTREABILIDADE.md`, Registro de mudanças de escopo, 22/10/2026).

![Protótipo em papel — pedidos, talhão e detecção](../assets/06_prototipos/prototipo_fluxo_2-1.jpeg)

![Protótipo em papel — área, parecer e histórico](../assets/06_prototipos/prototipo_fluxo_2-2.jpeg)

![Revisão no aplicativo — histórico e filtro temporal](../assets/06_prototipos/Historico.jpeg)

### Funcionalidade — Pedro

| Estado | Conteúdo e controles | Evidência |
|---|---|---|
| G01 | Resumo da situação para decidir o que examinar; abrir mapa/relatório. | Parte do desenho em `Tela3.jpeg`; visão revisada em `Relatorio.jpeg`. |
| G02 | Conferir cobertura de inspeção; distinguir não inspecionado de sem ocorrência. | Planejado; não há fotografia própria do estado em papel. |
| G03 | Mapa de talhões: filtrar, escolher talhão e examinar ocorrências → G04. | Desenho parcial em `Tela3.jpeg`; mapa revisado em `Mapa.jpeg`. |
| G04 | Detalhe de ocorrência com contexto e encaminhamento para parecer/reinspeção. | Parte visível em `Tela3.jpeg`. |
| G05–G08 | Confirmação de posição, evolução, decisão e repasse. | Caminhos previstos; não há fotografias desses estados em papel nesta entrega. |

**Caminho principal previsto:** G01 → G02 → G03 → G04 → decisão. **Retornos relevantes:** voltar ao mapa, alterar filtros, pedir avaliação ou reinspeção quando os dados não bastarem. A captura revisada do mapa exibe os controles de **Filtros** e **Desenhar**; ela, isoladamente, não comprova a execução de uma pulverização. A tela de relatório resume detecções e reinspeções. Segundo o registro da equipe, as métricas de irrigação também estão disponíveis **na extração do relatório**, embora não estejam visíveis na captura da tela de resumo.

![Protótipo em papel — resultado e encaminhamento do gestor](../assets/06_prototipos/Tela3.jpeg)

![Revisão no aplicativo — mapa operacional com filtros](../assets/06_prototipos/Mapa.jpeg)

![Revisão no aplicativo — resumo do relatório](../assets/06_prototipos/Relatorio.jpeg)

## 4. Simulação / walkthrough formativo

**Participação relatada pela equipe:** Vitor, da fazenda parceira, examinou o aplicativo e comentou os fluxos do mapa e do relatório do perfil administrativo. Guilherme examinou as interfaces preparadas por Lucas e Pedro em 08/11/2026; Lucas e Pedro examinaram a interface de Guilherme em outro dia. Fora a data da avaliação de Guilherme, as datas individuais, o roteiro exato, a sequência de ações e eventuais falas literais não foram preservados; por isso, o registro abaixo contém apenas os comentários informados, sem atribuir falas ou tempos inventados. O contato com Vitor ocorreu **no aplicativo após os desenhos iniciais**; não equivale a afirmar que ele executou um walkthrough formal de todas as telas em papel.

| Observação relatada | Tela/ação | Evidência disponível | Consequência para o design |
|---|---|---|---|
| Vitor recomendou que os relatórios do administrador incluíssem métricas da fazenda, como pontos irrigados e momento de irrigar. | Relatórios do perfil administrativo. | Relato da equipe após apresentação do app a Vitor. A captura `Relatorio.jpeg` mostra o resumo; a equipe informa que os indicadores de irrigação aparecem na **extração**, não nessa tela. | Manter o resumo direto e disponibilizar as métricas detalhadas no relatório extraído. Conferir essa parte com participantes finais na Entrega 14. |
| Vitor recomendou um mapa com informação mais enxuta, filtros e ações objetivas sobre o talhão, inclusive marcar talhão para pulverização. | Mapa e seleção de talhões. | Relato da equipe; `Mapa.jpeg` mostra **Filtros**, polígonos e **Desenhar**. A imagem não demonstra, sozinha, o registro da pulverização. | Priorizar leitura do talhão, filtro e marcação; verificar em teste posterior se a ação de pulverização é encontrada e entendida. |
| Lucas e Pedro avaliaram os desenhos de Guilherme. | Fluxo de Guilherme (PF03/PF04). | Relato da equipe e fotografias dos desenhos. Não há notas individuais de hesitação, erro ou fala. | Registrar a revisão entre integrantes como feedback interno; não tratá-la como validação externa das personas. |

**Avaliação de Guilherme sobre os fluxos de Lucas e Pedro (08/11/2026).** Guilherme percorreu os desenhos em papel tentando cumprir as tarefas de cada fluxo (PF01/PF02: fotografar um fruto e interpretar o resultado; PF05/PF06: localizar talhões e examinar resultados), sem explicação prévia dos autores.

| Observação relatada | Tela/ação | Evidência disponível | Consequência para o design |
|---|---|---|---|
| Guilherme não identificou qual dos botões inferiores fazia a captura: os três são ícones sem rótulo (galeria, lupa e “i”). | P02 — câmera (`Tela1-Tela2.jpeg`, tela da esquerda). | Relato de Guilherme. | Destacar o botão de captura (maior e centralizado) e dar rótulo aos demais. |
| Não soube dizer se a barra “90%” no topo da câmera indicava o andamento da análise ou a confiança da detecção; a tela de resultado mostra outro valor (“97%”). | P02/P03 — câmera. | Relato de Guilherme. | Dar rótulo à barra e não usar dois números parecidos com significados diferentes. |
| O rótulo “ÁCARO” aparece sobre o fruto durante o enquadramento, antes da captura, e foi lido por Guilherme como resultado já definido. | P02 — câmera. | Relato de Guilherme. | Mostrar a indicação só depois da análise e como indicação (“possível ácaro”), não como constatação. |
| “Leprose Macho Adulto” mistura a doença (leprose) com o vetor (ácaro) e indica sexo e fase que o modelo do TCC não necessariamente classifica. | P04 — resultado (`Tela1-Tela2.jpeg`, tela da direita). | Relato de Guilherme. | Usar o termo que corresponde ao resultado do modelo (“sinal de ácaro-da-leprose”) e retirar o que ele não informa. |
| Guilherme não conseguiu diferenciar talhão inspecionado de talhão limpo: as marcas ✓ e as hachuras no mapa não têm legenda. | G03 — mapa (`Tela3.jpeg`). | Relato de Guilherme. | Incluir legenda e estados distintos (não inspecionado, inspecionado sem ácaro, com ácaro), com texto e símbolo. |
| No histórico do talhão, “poucos ácaros” não permite comparar inspeções; Guilherme sugeriu mostrar a quantidade detectada. | G04 — cartão de resultados (`Tela3.jpeg`). | Relato de Guilherme. | Exibir o número de ácaros detectados em cada registro. |
| O detalhe do talhão só oferece “Pedir inspeção”. Guilherme sugeriu reorganizar esse menu para incluir “pedir parecer ao agrônomo”, que é a entrada do fluxo de P03 (pedido de parecer em A01). | G04 — detalhe do talhão (`Tela3.jpeg`). | Relato de Guilherme; ligação com PF03. | Incluir a ação “pedir parecer ao agrônomo” no detalhe do talhão, ao lado de “pedir inspeção”, ligando o fluxo do gestor ao do agrônomo. |

**Análise crítica da avaliação de Guilherme:** Guilherme integra a equipe e conhece as personas, os cenários e o vocabulário do projeto; por isso, não substitui um participante do perfil de P02 ou P01. Rótulos que ele compreendeu sem dificuldade — por exemplo, “97% de assertividade” lido como certeza, “Limpo” lido como talhão livre da praga em toda a área ou “Talhão T5 Q19” sem saber o que é “Q19” — podem confundir um trabalhador ou um gestor. Além disso, só os estados desenhados foram percorridos: rota (P01), confirmação e envio (P05–P07), resumo do ciclo (G01) e posição, evolução, decisão e repasse (G05–G08) não estavam em papel e não foram avaliados. Esses pontos permanecem como perguntas para a Entrega 14.

**Limite da evidência:** estes registros documentam a iteração formativa informada pela equipe. Não permitem medir sucesso, tempo ou dificuldades por tarefa nem comprovar testes de todos os estados previstos. A avaliação com usuários representativos e o roteiro de observação devem ser aprofundados na Entrega 14.

## 5. Alterações após o feedback

| Antes | Problema apontado | Depois | Justificativa e limite da evidência |
|---|---|---|---|
| Desenhos iniciais e discussão do mapa com muitos detalhes possíveis por talhão. | Vitor pediu informações mais enxutas, filtro e foco em marcar/agir sobre o talhão. | Revisão diretamente no app: `Mapa.jpeg` mostra mapa operacional, **Filtros** e **Desenhar**. | A captura comprova a presença dos controles e a organização geral. O fluxo completo de marcação/pulverização precisa ser verificado em uso. |
| Discussão inicial de relatórios sem as métricas operacionais citadas por Vitor. | Necessidade de pontos irrigados e indicação de quando irrigar. | `Relatorio.jpeg` mostra o resumo para decisão; segundo a equipe, as métricas de irrigação constam **na extração do relatório**. | Mantém a visualização resumida e concentra detalhes na exportação. A captura disponível não comprova o conteúdo exportado; incluir amostra da extração se o docente exigir evidência visual. |
| Consulta às detecções do talhão apresentada no desenho em papel. | Necessidade de recuperar ocorrências em contexto temporal. | `Historico.jpeg` registra a tela implementada, com período selecionável e lista de registros. | A revisão torna a consulta visível; a efetividade do filtro ainda depende de teste com usuário. |
| Câmera e resultado esboçados em papel. | Necessidade de orientar a captura e comunicar que a análise está em andamento. | `Camera.jpeg` mostra orientação para aproximar a câmera e indicador de busca. | Dá feedback durante a operação; a compreensão do resultado ainda deverá ser observada. |
| Câmera em papel com três ícones sem rótulo e barra “90%” sem rótulo. | Botão de captura não identificado e barra ambígua, observados na avaliação de Guilherme. | `Camera.jpeg`: botão de captura central e destacado, “Galeria” e “Flash” com rótulo e barra rotulada “Buscando”. | A versão do app resolve a identificação do botão de captura. Ainda é preciso observar com participantes se “Buscando 0%” é entendido como andamento ou como confiança. |
| “Poucos ácaros” no histórico do talhão em papel. | Quantidade vaga, que não permite comparar inspeções, observada na avaliação de Guilherme. | `Historico.jpeg`: cada registro mostra “N ácaro(s) detectado(s)”. | Atende à observação. |

As decisões acima resultam dos comentários relatados e da revisão que a equipe implementou **no código do aplicativo**, não de uma segunda versão desenhada em papel. Das observações de Guilherme sobre os fluxos de Lucas e Pedro, permanecem sem revisão comprovada: a indicação “ÁCARO” antes da captura e o termo “Leprose Macho Adulto” (não aparecem nas capturas), a legenda que diferencia talhão inspecionado de talhão limpo (`Mapa.jpeg` mostra filtros, mas não a legenda) e a ação “pedir parecer ao agrônomo” no detalhe do talhão (o aplicativo não tem o fluxo do agrônomo; ver Entrega 11, telas FA).

## Checklist

- [x] Os desenhos e a revisão no app cobrem partes relevantes das tarefas da Entrega 5.
- [x] Cada tela/estado fotografado está associado a uma tarefa, decisão ou informação necessária.
- [x] Não foram criados login, CRUD ou dashboard apenas para parecer “completo”.
- [x] Estados fotografados estão identificados na documentação, com caminhos e retornos descritos; os estados apenas planejados estão explicitamente diferenciados.
- [x] Há registro de uma avaliação formativa com Vitor e de avaliação cruzada entre integrantes, com a limitação da ausência de protocolo detalhado declarada.
- [x] O feedback relatado gerou decisões de revisão, documentadas com as quatro capturas do aplicativo.
- [x] Os desenhos iniciais permanecem em baixa fidelidade e suas limitações não são mascaradas pelas capturas da implementação.

**Limitações remanescentes:** não há fotografia em papel de todos os estados inicialmente previstos, protocolo de observação individual ou captura do relatório exportado. Esses materiais não são presumidos como existentes; se forem exigidos para avaliação da disciplina, deverão ser anexados como evidência adicional.
