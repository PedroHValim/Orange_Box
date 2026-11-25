# Matriz de rastreabilidade de IHC

**Atualização:** 22/11/2026.

A matriz registra como as hipóteses, necessidades, decisões de interação e resultados das avaliações se relacionam. Hipóteses ainda não investigadas permanecem abertas.

## 1. Derivação do escopo de IHC a partir do TCC

| Elemento | Registro da equipe | Evidência/justificativa | Estado |
|---|---|---|---|
| Tema do TCC | Detecção Automatizada do Ácaro da Leprose na Citricultura via Redes Neurais Convolucionais em Dispositivos Móveis | TCC | definido |
| Resultado técnico esperado | Sistema/modelo | TCC | definido |
| O TCC previa interface? | Sim | TCC | definido |
| Capacidade/contribuição central | Monitoramento com geolocalização de infestações e acesso à detecção de pragas | TCC | definido |
| Possíveis beneficiários/stakeholders | Inspetor de campo e responsável pelo manejo, como dono, gestor ou agrônomo | Entrega 1 revisada, seções 2.2 e 2.3 | hipótese H26 |
| Usuário escolhido para IHC | Inspetor de campo P02 como primário; P01 e P03 como secundárias/proto-personas | Atividade A01 documentada no TCC [F16], [F18]; papéis de P01/P03 não confirmados | proposta a validar |
| Objetivo principal do usuário | Inspetor: identificar sinal da praga e registrar ocorrência (H29). Responsável pelo manejo: compreender a distribuição para decidir (H21) | Entrega 1 revisada, seção 3.1 | hipótese |
| Contexto de uso adotado | Campo aberto, com pouca ou nenhuma internet [F13]. Sol forte, caminhada e pouco tempo por planta permanecem hipóteses (H30) | TCC; sem observação de campo registrada | parcialmente hipótese |
| Interface/recorte de IHC | Fluxo 1: captura → resultado → registro. Fluxo 2: mapa e decisão como hipótese condicionada a H21/H22 | Entrega 1 revisada, seção 7 | proposta revisada |
| Relação com o TCC | Interface prevista como parte do projeto | TCC | definido |
| Evidência de avaliação disponível | Sessões U01, U02 e U03 realizadas com participantes proxy | Entrega 14 | evidência limitada de interação |

> Preservar decisões anteriores e registrar a evidência que motivou cada mudança. Testes com participantes proxy não validam automaticamente os perfis profissionais ou o contexto de campo.

## 2. Registro de hipóteses e lacunas da Entrega 1

| ID | Afirmação/dúvida inicial | Tipo | Por que importa | Como/onde investigar | Evidência obtida | Estado atual | Impacto no projeto |
|---|---|---|---|---|---|---|---|
| H01 | Disponibilização do dataset do ácaro | H | Contribuição técnica prevista | TCC | TCC | aberta | Fora do escopo de IHC |
| H02 | Quem aplica o produto pode não ser quem usa o aplicativo | H | Define o repasse da decisão | Entrega 7 | Sem coleta específica registrada | aberta | Repasse explícito em G08, a validar |
| H03 | Usuários podem ter diferentes níveis de leitura e familiaridade tecnológica | H | Define simplicidade e apresentação | Entrega 7 | U01 elogiou legibilidade, mas é estudante de Computação e proxy | aberta | Não generalizar a avaliação positiva para trabalhadores com outros perfis |
| H05 | Como o acompanhamento da disseminação é feito atualmente | ? | Justifica comparação entre ciclos | Entrega 7 | Sem coleta específica registrada | aberta | Comparação temporal ainda depende de investigação |
| H06 | Decidir onde aplicar é a atividade mais crítica | H | Prioriza T04/T08 | Entrega 7 | Sem coleta com perfil profissional registrada | aberta | Prioridade ainda não confirmada |
| H09 | Necessidade de histórico e rastreabilidade das inspeções | H | Justifica consulta de registros e cobertura da rota | Entregas 7 e 14 | U01 localizou inspeção com ajuda; sugeriu melhorias no histórico | parcialmente investigada | Revisar acesso ao histórico; necessidade profissional ainda não validada |
| H20 | Usuários têm pouca familiaridade com aplicativos técnicos | H | Orienta simplicidade | Entregas 3 e 7 | U01 não tinha experiência agrícola, mas cursa Computação | aberta | U01 não representa baixa familiaridade tecnológica |
| H21 | Dono/gestor acompanha a evolução e usaria o mapa | H | Justifica Fluxo 2 | Entregas 3, 7 e 14 | U02 (proxy, versão web) acompanhou a evolução pelo relatório e não abriu o mapa | aberta | Mapa permanece hipótese de trabalho; relatório usado como principal fonte em U02 |
| H23–H25 | Detecção sem pragueiro, menor esforço e auxílio da geolocalização à gestão | H | Benefícios dependem do uso | Entrega 14 e investigação de campo | U01 concluiu captura, mas não houve avaliação desses benefícios | aberta | Não afirmar redução de esforço ou substituição de profissional |
| H26 | Inspetor e responsável pelo manejo são pessoas/papéis diferentes | H | Define personas | Entrega 7 | Sem coleta específica registrada | aberta | P01/P02/P03 permanecem propostas |
| H27 | Pode ser necessária confirmação humana; falsos positivos e negativos têm consequências diferentes | H | Define divisão entre pessoa e IA | Entregas 7 e 14 | U03 apresentou dúvida sobre autoria do veredito; interpretação de U01 não foi registrada | parcialmente investigada | Explicitar autoria e separar resultado automático de validação humana |
| H28 | Usuários utilizam celular sem prática com aplicativos técnicos | H | Orienta interação inicial | Entrega 7 | Não investigada com público correspondente | aberta | Evitar generalização com base em U01 |
| H29/H30 | Objetivo do inspetor e condições de campo: sol, caminhada e pouco tempo | H | Define contexto | Entrega 7 e observação em campo | U01 foi testado na FEI; comentou positivamente sobre textos grandes | aberta | Sessão não valida uso real em campo |
| H31–H33 | Processamento, alertas e interface mais simples | H | Evita requisitos sem evidência | Entregas 7 e 14 | U01 acompanhou orientação de distância e capturou sem ajuda; avaliou interface como didática | parcialmente investigada | Manter orientação; verificar com perfil representativo |
| [?] | O que acontece após encontrar a praga: registro, comunicação, consolidação e decisão | ? | Justifica mapa e decisão de manejo | Entregas 3, 4 e 7 | Sem investigação do processo profissional registrada | aberta | Fluxos de repasse permanecem propostas |
| H04 | Quem decide onde e quando aplicar: gestor ou agrônomo | ? | Define destinatário do parecer e papel de P03 | Entrega 7, instrumento I02 | I02 não aplicada; C03 e HTA T05 assumem recomendação do agrônomo e decisão do dono | aberta | Se a decisão couber ao agrônomo, revisar o destinatário do repasse |
| H07 | O profissional precisa de localização, intensidade e urgência da ocorrência | H | Define conteúdo mínimo para validação remota | Entrega 7, instrumento I02 | Necessidades propostas em P03 e C03; sem coleta com agrônomo | aberta | Foto, data, hora, localização e histórico em FA03 |
| H22 | Necessidade de histórico das inspeções para o agrônomo | H | Justifica comparação temporal | Entregas 5, 7 e 14 | U03 consultou três ocorrências corretamente em 64 s, mas é proxy | parcialmente investigada | Consulta demonstrada; necessidade profissional ainda não validada |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos

| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação/signos | MoLIC | Tela(s) | Heurística/problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | Registro geolocalizado das inspeções, associado aos talhões | Saber o que foi inspecionado e onde há detecções para decidir o manejo | P01; teste com proxy | C01 | O06/O07; T09 | [CTT T09](docs/05_analise_tarefas.md) | CI01; cobertura do talhão, situação do talhão no ciclo e confiança do resultado | M03 S1/S2/S3 | F06 Relatórios e F04 Mapa; versão web | HC20 (A03-V03; problema potencial de código, pendente de reprodução no iOS); AU04 | UT09 → U02, 17/11/2026: apontou os Talhões 04 e 02 como piores; não identificou o talhão sem inspeção | Distinguir “não inspecionado no período” de “sem ocorrência”; não calcular variação sem inspeção; testar novamente |
| R02 | Contagem de detecções por talhão ao longo dos períodos | Acompanhar a evolução e levar a situação a quem decide ou aplica | P01 → P03; teste com proxy | C01 | O09/O10/O11; T08/T04 | [GOMS T08 e HTA T04](docs/05_analise_tarefas.md) | CI01; tendência do talhão, decisão do ciclo e situação do repasse | M03 S5/S7/S8 | F06 Relatórios: Visão do período e exportação; versão web | HC18 (A03-V01; contagens diferentes entre telas no aplicativo iOS) | UT08/UT04 → U02, 17/11/2026: apontou 04 e 02 como maiores aumentos; gerou o relatório em PDF | Manter a comparação entre períodos e a exportação; registrar a resposta sobre redução em novo teste |
| R03 | Detecção por foto com geolocalização | Localizar as detecções a partir dos relatos de campo | P03 | C03 | O13/T05, passos 1 e 2.1 | [HTA T05](docs/05_analise_tarefas.md) | CI03; pedido de parecer, propriedade, talhão, solicitante, pontos pendentes e situação | M01 S1/S2 | FA01, FA01V, FA02 | AU02, observado na avaliação com usuário | UT07 → U03, 16/11/2026: pedido correto escolhido por eliminação entre dois pedidos de Jaime | Mostrar as árvores ou pontos de cada pedido; ligar os dois pedidos no protótipo e retestar UT07 |
| R04 | Resultado da detecção automática por foto | Separar indicação da IA de confirmação humana | P03 | C03 | O14/T07 | [CTT T07](docs/05_analise_tarefas.md) | CI03; avaliação da IA, veredito, validado por e observação técnica | M01 S2/S3/P1 | FA02, FA02V, FA02R, FA03, FA03A, FA03E | HC08, HC09, HC14, HC15, HC16 e HC17 (A02-V04, V05, V10, V11, V12 e V13); AU01 | UT07 → U03: confirmou ponto 3 sem abrir avaliação da IA; QA19 parcialmente observada por UT06 | Manter distinção entre IA e veredito humano. Correções da inspeção não aplicadas antes do teste, conforme QA21. Explicitar autoria no histórico |
| R05 | Registro geolocalizado ao longo dos ciclos | Comparar as detecções atuais com inspeções anteriores | P03 | C03 | O15/T06 | [GOMS T06](docs/05_analise_tarefas.md) | CI03; histórico, período, local e detecções anteriores | M01 S5/P3/acesso ubíquo | FA03, FA05, FA05V | HC09 e HC13 (A02-V05 e V09); AU01 | UT06 → U03: resposta correta em 64 s; QA06 não atingida; dúvida sobre autor do veredito | Mostrar quem decidiu e separar avaliação da IA em FA03/FA05 |
| R06 | Captura de foto em campo | Solicitar nova imagem quando a foto é insuficiente | P03; P02 recebe pedido | C03 | O16/T07, saída de nova foto | [CTT T07](docs/05_analise_tarefas.md) | CI03; pedido de nova foto | M01 S3/P2; entrada na rota em M02 | FA03, FA02N | HC10 (A02-V06) | UT05/pós-teste → U03: compreendeu que L5-11 aguarda nova foto | Manter pedido vinculado ao ponto; situação continua pendente até nova avaliação |
| R07 | Mapa dos pontos detectados | Dimensionar área de aplicação | P03 | C03 | O17/T05, passos 3 e 4 | [HTA T05](docs/05_analise_tarefas.md) | CI03; área, pontos confirmados, produto, dose e período | M01 S6/P4 | FA06, FA06E | HC07, HC11 e HC12 (A02-V03, V07 e V08) | UT05 → U03: citou pontos 2, 3 e 5; QA05 atingida | Delimitar área com pontos confirmados; avisar pendências sem bloquear; produto e dose são registrados, não prescritos pelo sistema |
| R08 | Registro das detecções e vereditos vinculados | Encaminhar orientação ao gestor com contexto | P03 → P01 | C03 | O18/O19/T05, passo 5 | [HTA T05](docs/05_analise_tarefas.md) | CI03; parecer, pontos, destinatário e situação do pedido | M01 S7/P5/S1 | FA07, FA07E, FA01C | HC05, HC06 e HC15 (A02-V01, V02 e V11) | UT05 → U03: reconheceu envio pelo aviso verde; QA08 atingida | Vincular pontos ao parecer e preservar texto em falha. Esclarecer diferença entre envio concluído e pontos pendentes |
| R09 | Detecção da praga por imagem no dispositivo móvel | Fotografar seguindo orientações da câmera | P02; teste com proxy | C02 | O02/O03; T02 | [Análise de tarefas](docs/05_analise_tarefas.md) | CI02; foto, confiança, orientação de distância e resultado | M02 | F02; câmera do aplicativo | Nenhuma dificuldade de captura observada na sessão U01 | UT02 → U01, 14/11/2026: capturou sem ajuda; estimativa retrospectiva de 20 s a 1 min, não cronometrada | Manter orientação de aproximação/afastamento. Compreensão da diferença entre IA e confirmação humana não foi registrada |
| R10 | Armazenamento de inspeções com resultado, data e localização | Reencontrar uma inspeção anterior | P02; teste com proxy | C02 | O04; T01/T03 | [Análise de tarefas](docs/05_analise_tarefas.md) | CI02; histórico, inspeção, talhão, data e resultado | M02 | F03; histórico do aplicativo | AU03 — dificuldade inicial para encontrar a funcionalidade | UT01 → U01, 14/11/2026: encontrou com ajuda; estimativa retrospectiva de 2–3 min, não cronometrada | Revisar acesso ao histórico; avaliar refazer foto, editar informações e excluir imagem; verificar melhorias em novo teste |

### 3.1 Registro complementar — avaliação conduzida por Lucas

**Participante:** U01, 21 anos, estudante de Ciência da Computação, sem experiência em inspeção agrícola; proxy, fora da equipe.  
**Sessão:** 14/11/2026, às 14h40, presencialmente na FEI, sem interferências relatadas.  
**Dispositivo:** iPhone 16 Pro Max, GPS funcionando; iOS mais recente disponível no aparelho na data, sem número/build anotado.  
**Versão do aplicativo:** disponível na data, sem hash registrado.  
**Consentimento:** verbal; não há termo assinado ou arquivo separado.  
**Registro:** anotações, sem gravação.

| Item | Evidência disponível | Interpretação e limite |
|---|---|---|
| Captura | U01 fotografou sem ajuda e acompanhou a orientação de distância | Indício de compreensão da orientação operacional da câmera, sem comprovar compreensão completa do resultado |
| Restrição de captura | Aplicativo exige confiança maior ou igual a 85%; abaixo disso orienta ajustar a captura | Restrição preventiva; não contabilizada automaticamente como erro do participante |
| Tempo de UT02 (captura) | Intervalo relatado de 20 s a 1 min; o valor pontual de 40 s não é adotado | Estimativa retrospectiva, não medida por cronômetro |
| Histórico | U01 inicialmente não encontrou a funcionalidade e precisou de ajuda | Sucesso parcial; AU03 |
| Tempo de UT01 (consulta anterior) | Intervalo relatado de 2–3 min; o valor pontual de 2 min 30 s não é adotado | Estimativa retrospectiva, não medida por cronômetro |
| Clareza visual | Comentou que a interface era didática, os campos e botões eram perceptíveis e os textos grandes favoreciam leitura | Opinião positiva de um proxy, em ambiente de faculdade; não comprova legibilidade no campo |
| Satisfação | Comentário qualitativo positivo | Não houve nota numérica |
| Interpretação da IA | Não foi anotada explicação sobre IA versus confirmação humana | Compreensão não verificada |
| Sugestões | Refazer foto, editar informações e excluir imagem pelo histórico | Propostas a avaliar; não equivalem a falhas comprovadas de todas essas funções |
| Armazenamento | Local e prazo de descarte originais não informados | Política posterior registrada na Entrega 14, Passo 3; não publicar dados identificáveis |

**Limitação:** os valores aproximados não devem ser usados como tempos cronometrados ou como comprovação de metas quantitativas. A ausência de experiência agrícola impede generalização para trabalhadores de campo.

## 4. Rastreabilidade de padrões de interface

| ID da tela/fluxo | Padrão de interface | Objetivo/tarefa que justifica | Informação/ação principal | Evidência de necessidade | Artefatos relacionados |
|---|---|---|---|---|---|
| F01 | dashboard | T09/T08/T04; O06–O10 | Situação do período por talhão, comparação com o período anterior e exportação | U02 encontrou os piores talhões e gerou o relatório; não identificou o talhão sem inspeção (AU04) | C01/M03, R01, R02 |
| F02 | captura e feedback da análise | T02; O02/O03 | Foto, confiança, orientação de distância e resultado | U01 concluiu captura sem ajuda; interpretação completa não registrada | C02, CI02, M02, R09 |
| F03 | histórico de inspeções | T01/T03; O04 | Localizar registro por talhão, data e resultado | U01 precisou de ajuda para encontrar a funcionalidade; AU03 | C02, CI02, M02, R10 |
| FA01 | alertas/ocorrências | T05, passo 1 | Pedidos e detecções por propriedade/talhão | Necessidade profissional ainda hipotética; U03 revelou ambiguidade entre pedidos | C03, CI03, M01 S1, AU02 |
| FA03 | detalhamento e explicabilidade | T07 | Foto, metadados, histórico, avaliação automática e veredito | H07; CTT T07; autoria do veredito questionada por U03 | C03, CI03, M01 S3, AU01 |
| FA05 | histórico com filtros | T06 | Lista com período e local | H22; GOMS T06; U03 consultou ocorrências corretamente, acima do tempo-meta | C03, CI03, M01 S5, AU01 |
| FA06/FA07 | encaminhamento e registro | T05, passos 4 e 5 | Área, parecer e repasse ao gestor | H04 e risco de dimensionamento ainda hipotéticos; U03 compreendeu área e envio no protótipo | C03, CI03, M01 S6/S7 |

**Consistência de identificadores:** F02 e F03 são registrados conforme seu uso na Entrega 14: câmera e histórico. As linhas genéricas anteriores que os descreviam como “histórico com filtros” e “administração/CRUD” eram campos de modelo sem conteúdo específico. Caso outro artefato utilize esses códigos com significado diferente, alinhar a nomenclatura antes da consolidação.

## 5. Registro de mudanças de escopo e decisões

| Data | O que mudou | Evidência/feedback que motivou | Artefatos afetados | Responsável |
|---|---|---|---|---|
| 22/10/2026 | Fluxo do agrônomo proposto como aplicação web no computador | CTT T07 exige foto, zoom e histórico simultâneos; hipótese de análise no escritório | Entregas 6, 8 e 11 | Guilherme |
| 08/11/2026 | Inspetor P02 passa a ser prioritário; P01/P03 secundárias; mapa e manejo tratados como hipóteses; fatos rebaixados e modelos corrigidos | Feedback do professor | Entregas 1 a 6 | Equipe |
| 10/11/2026 | Piloto do aplicativo com os pais de Lucas, aproximadamente às 10h20, por cerca de 10 minutos | Execução de captura, marcação de talhão e extração de relatório | Entregas 12 e 14 | Lucas |
| Após o piloto de 10/11/2026 | Inclusão de métricas no relatório e simplificação visual do mapa e da câmera | Relato de Lucas sobre as alterações realizadas | Aplicativo; Entregas 6, 11 e 14, conforme versão | Equipe; piloto conduzido por Lucas |
| 14/11/2026 | Registro da sessão final U01 como avaliação com proxy | Estudante de Computação sem experiência agrícola; captura sem ajuda e consulta ao histórico com ajuda | Entrega 14; R09/R10 | Lucas |
| 14/11/2026 | Decisão de revisar o histórico e avaliar refazer foto, editar informações e excluir imagem | Dificuldade de U01 em localizar inspeção e sugestões pós-teste | Histórico do aplicativo; M02; F03; AU03 | Lucas |
| 15/11/2026 | Protótipo FA mantido sem correções da inspeção para comparação no teste | Comparar inspeção e comportamento observado | Entregas 12, 13 e 14 | Guilherme |
| 16/11/2026 | Piloto FA ajustou explicação do controle e o registro de horários | Dificuldade de entendimento em UT05 durante o piloto | Roteiro P03; Entregas 12 e 14 | Guilherme |
| 16/11/2026 | Sessão U03 identificou dúvidas sobre autoria do veredito e distinção dos pedidos | UT06/UT07; AU01/AU02 | FA01, FA03, FA05; M01; Entrega 14 | Guilherme |
| 17/11/2026 | Inclusão de U01 e U03 nesta matriz, com limitações explícitas | Resultados disponíveis na Entrega 14 | R03–R10; hipóteses relacionadas; matriz | Equipe |
| 17/11/2026 | Sessão U02 feita na versão web, com dados fictícios, por falta de acesso ao aplicativo iOS no aparelho do participante | Proxy não percebeu o talhão sem inspeção (AU04); localizou os piores talhões e gerou o relatório | Entregas 12 e 14; R01, R02; F01; M03 S2 | Pedro |
| 20/11/2026 | Revisão da parte de Pedro após o feedback: “gravidade” substituída por “ordem dos talhões”; O06–O11 classificados; cobertura do M03 declarada parcial; emendas de P01 (versão web, um participante, gravação, sem piloto) registradas na Entrega 12; achados só de código de A03 separados como pendentes de reprodução; tarefa de U02 renomeada de UT03 para UT09. Revisão posterior às avaliações; não altera o que foi planejado antes delas. | Feedback do professor às Entregas 8 a 14 | Entregas 8–14; instrumentos; R01 | Pedro |
| 22/11/2026 | Revisão da parte de Guilherme na Entrega 9 após o feedback: CI03 abstraído (sem rótulos, estados e dados fictícios do protótipo); episódio passado de aplicação em área maior retirado, voltando a ser possibilidade a investigar (Q5 do C03); hipóteses de P03 explicitadas; O12 final, O14/O15/O17/O18 instrumentais diretos e O13/O16/O19 indiretos; restrições de P03 dependentes de hipóteses marcadas como decisão provisória; semântica da avaliação da IA precisada | Feedback da Entrega 9 (itens 5–8, 11–16, 23 e 25) | Entrega 9 (CI03, DCC, mapa, SVG integrado, signos); Entrega 10 deve reutilizar os títulos revisados de O12–O19 | Guilherme |
| 22/11/2026 | Vocabulário da equipe: “foco” passa a designar só região com pontos confirmados pelo agrônomo; detecções sem veredito humano são “detecções em avaliação”; em P01, “com focos/sem focos” passa a “com detecções/sem detecções”. “Confiança do resultado” (P01, por talhão) e “avaliação da IA” (P03, por foto) mantidos como signos distintos com a mesma origem (pontuação do modelo) | Feedback da Entrega 9 (itens 24 e 25) | Entrega 9 (vocabulário, signos de P01 e P03); R01, R03 e R05; Entrega 10 deve usar os mesmos termos | Equipe |
| 22/11/2026 | Revisão da parte de Guilherme na Entrega 10 após o feedback: M01 com objetivos O12–O19 classificados; signos com os nomes da Entrega 9 no texto e no SVG; S1 passa a “Saber o que aguarda avaliação”, sem usar “foco” antes do veredito; ação “ampliar foto” retirada de dentro de S3; hipóteses de P03 e decisões provisórias explicitadas | Feedback da Entrega 10 (itens 7, 25, 26 e 31) e da Entrega 9 | Entrega 10 (M01, consolidação); `molic_m01.svg` | Guilherme |
| 22/11/2026 | Revisão da parte de Guilherme na Entrega 11 após o feedback: tabela de cobertura usa o nome do M01; FA01 e FA02R conferidos com as cenas do M01 revisado, sem “foco” antes do veredito (subtítulo de FA01 registrado como divergência, captura mantida); signo foto do fruto identificado no rótulo “Foto original”; decisões provisórias de P03 marcadas em FA05–FA07; FA07E declarado fora do caminho navegável (recuperação da falha no envio não testável); ambiguidade de autoria do veredito (AU01) registrada para a próxima versão | Feedback da Entrega 11 (itens 18, 20, 21 e 32) e das Entregas 9 e 10 | Entrega 11 (cobertura M01, FA01–FA07, checklist) | Guilherme |
| 22/11/2026 | Revisão da equipe na Entrega 11: cobertura do M02 verificada cena por cena e declarada parcial (S2 coberta, S5 parcial, demais cenas, processamentos e encerramentos sem captura); origem de F02–F04 ajustada; significado da porcentagem da câmera (“Buscando 0%”) registrado como ponto a corrigir e a avaliar | Feedback da Entrega 11 (itens 3–6, 24 e 32) | Entrega 11 (cobertura M02, F02–F04, pontos observados, checklist) | Equipe |
| 22/11/2026 | Revisão da equipe na Entrega 10: M03 passa a usar “talhões com detecções” em vez de “talhões com focos” (DOT e SVG regenerado) e “confiança do resultado” em S4; M02 passa a indicar o SVG como fonte editável, sem notas de publicação; `molic_m02.png` antigo removido | Vocabulário da equipe de 22/11/2026; feedback da Entrega 10 (item 26) | Entrega 10 (M02, M03); `molic_m03.dot`, `molic_m03.svg` | Equipe |
| 22/11/2026 | Revisão da parte de Guilherme na Entrega 12 após o feedback: procedimento de inspeção de A02 (independência, H1–H10, severidade, consolidação e versionamento) no documento principal; seção I com emendas e execução de P03 (plano de 15/11, inspeção e decisão de QA21 anteriores a U03, correção de links, piloto, U03 sem observador, aceite verbal); leitura individual de QA04, QA06, QA08 e QA09; limitações de confiabilidade e validade de P03. Revisão posterior às avaliações; não altera o que foi planejado antes delas. | Feedback da Entrega 12 (itens 2, 3, 5, 6, 8, 10, 11, 15, 16, 24 e 27) | Entrega 12; roteiro, termo e formulário heurístico de P03 | Guilherme |
| 22/11/2026 | Revisão da equipe na Entrega 12: bloco “Avaliação heurística da equipe” (A01–A03, divisão de escopo por fluxo, independência, consolidação); “com focos” → “com detecções” na tabela de P01; nota de MU03 lida individualmente no roteiro de P02; contato institucional, prazo de descarte e forma de aceite preenchidos no termo de P02; código L1 relacionado a U01 no termo; checklist revisto e Entrega 12 marcada como concluída, com critérios anteriores à coleta (P01/P02) e piloto de P01 mantidos como não atendidos | Feedback da Entrega 12 (itens 3, 5, 10 e 23) e vocabulário da Entrega 9 | Entrega 12; roteiro e termo de consentimento | Equipe |
| 22/11/2026 | Revisão da parte de Guilherme na Entrega 13 após o feedback: versão inspecionada do protótipo FA (commit `ed4dbdc`, 15/11) e correção de links posterior registradas; limite de cobertura de A02 (só FA, aplicativo não inspecionado; FA inspecionado por um único avaliador); FA07E examinado só como quadro desenhado; matriz limitada aos estados observados; severidades de A02 declaradas individuais e HC05–HC17 sem reavaliação coletiva; V01 relacionado também a H4; capturas mantidas | Feedback da Entrega 13 (itens 1, 2, 3, 9, 16, 17, 20 e 36); feedback da Entrega 12 (versionamento entre inspeção e teste) | Entrega 13 (A02, consolidação HC05–HC17 e conclusão) | Guilherme |
| 22/11/2026 | Revisão da parte de Guilherme na Entrega 14 após o feedback: U03 registrado como conhecido do moderador (possível viés); pré-teste declarado não aplicado; leitura do termo P03, aceite verbal sem assinatura e termo ajustado depois da sessão; local das anotações originais (fora do repositório); pensar em voz alta pedido oralmente, sem texto no roteiro; limitações de U03 reunidas; AU01 e AU02 com recomendações revistas (AU02 com evidência parcial e reteste com os dois pedidos ligados); capturas de FA01 e FA03 da versão testada em `assets/14_testes`; roteiro P03 com lista pré-sessão, pensar em voz alta, pré-teste para substituto, pós-teste completo e frase de UT05 sem campos de FA06 para novas sessões. Revisão posterior à sessão; não altera o que foi executado. | Feedback da Entrega 14 (itens 2, 4, 6, 10, 12, 13, 15, 23, 24 e 29) | Entrega 14 (Passos 2–6, U03, AU01, AU02, conclusão); roteiro, sessão U03 e piloto P03; R03 | Guilherme |
| 22/11/2026 | Revisão da equipe na Entrega 14: fluxograma exportado com as oito etapas do modelo (`assets/14_testes/fluxograma_avaliacao.dot` e `.svg`); tarefa de U02 passa a UT09 em todo o relatório; comparação com a heurística usa os IDs HC da consolidação corrigida da Entrega 13, com HC20 tratado como hipótese de código pendente de reprodução no iOS; coluna de gravidade identificada como prioridade da equipe, distinta da severidade de Nielsen; matriz R01, R02 e R04–R08 com os IDs HC; IDs de Lucas propagados (R09 = UT02 captura, R10 = UT01 consulta), sem os valores pontuais estimados; roteiro P02 com o mesmo texto de pensar em voz alta de P01 e P03 para novas sessões | Feedback da Entrega 14 (itens 7, 13, 26 e 29) e da Entrega 13 (item 15) | Entrega 14 (seções A, B, C, E, F, G e checklist); matriz R01–R10; roteiro P02 | Equipe |
| 24/11/2026 | Reavaliação coletiva das severidades da Entrega 13: notas individuais 0–4 dos três avaliadores para os 35 HC (não às cegas) e reunião remota com Lucas, Guilherme e Pedro; 27 notas iguais confirmadas por unanimidade e 8 divergências decididas por consenso (HC05 → 3; HC09, HC15, HC19 e HC23 → 1; HC24, HC27 e HC35 → 2); todos os itens considerados violação; HC04 em H2, HC15 em H9, HC16 em H10; HC22 e HC38 mantidos separados. Contagem final: severidade 3: 5, 2: 18, 1: 12 | Feedback da Entrega 13 (itens 3, 4 e síntese 5–6) | Entrega 13 (7.4, 7.6, seção 8, conclusão, checklist); `instrumentos/reavaliacao_severidades_e13.md` | Equipe |

## 6. Personas, cenários, tarefas e protótipos — Entregas 3 a 6

Cadeia: **necessidade → persona → cenário → tarefa → modelo de tarefa → fluxo → tela/estado → avaliação → decisão**.

As personas permanecem propostas enquanto não houver investigação suficiente com os perfis correspondentes. Sessões com proxy não confirmam automaticamente o cenário profissional.

| Persona | Tipo/estado | Hipóteses relacionadas | Cenário | Tarefas/modelos | Fluxo | Telas | Situação |
|---|---|---|---|---|---|---|---|
| P02 — inspetor de campo | Primária; perfil a validar com público correspondente | H03, H09, H20, H27–H30 | C02 | T01/T02/T03; modelos na Entrega 5 | PF01/PF02; M02 | Câmera e histórico do aplicativo; F02/F03 | U01 avaliado em 14/11/2026, mas é proxy sem experiência agrícola; captura concluída sem ajuda e consulta ao histórico com ajuda |
| P01 — gestor | Secundária/proto-persona | H04, H06, H21, H26 | C01 | T04/T08/T09, conforme Entrega 5 | M03 | Mapa e relatório | U02 avaliado em 17/11/2026, mas é proxy sem experiência agrícola, na versão web; encontrou os piores talhões e gerou o relatório, mas não percebeu o talhão sem inspeção |
| P03 — Marcelo Fidalgo | Secundária/proto-persona; somente F08 registrado como fato | H04, H07, H21, H22 | C03 | T05 HTA; T06 GOMS; T07 CTT | PF03/PF04; M01 | A01–A03 e A05–A07 em papel; FA01–FA07 e estados no Figma | Papel avaliado por Lucas/Pedro sem notas individuais; inspeção A02 registrada; I02 não aplicada; U03 testado em 16/11/2026 com proxy, sem validar o perfil agronômico |

| Item | Estado |
|---|---|
| Walkthrough da Entrega 6 | Formativo: comentários de Vitor e avaliação cruzada. Guilherme avaliou fluxos de Lucas/Pedro em 08/11/2026, com sete observações. Avaliação de PF03/PF04 por Lucas/Pedro sem notas individuais |
| Alterações após simulação da Entrega 6 | Registradas no aplicativo. Botão de captura e contagem de ácaros atendidos nas evidências `Camera.jpeg` e `Historico.jpeg`; demais itens devem ser conferidos nos artefatos |
| Cenários C01–C03 | Hipóteses e perguntas continuam explícitas; avaliações proxy não equivalem a validação profissional |
| Padrões da Entrega 2 | RC01 candidata; RC02 candidata; RC03 hipótese; RC04 reforça decisão do TCC; RC05 reformulada; RC06 e RC07 diretrizes |
| Piloto de Lucas | Pais de Lucas, 10/11/2026, cerca de 10 minutos; não conta na amostra final |
| U01 | Sessão final em 14/11/2026; proxy; resultados e limites registrados |
| U03 | Sessão final em 16/11/2026; proxy; resultados e limites registrados |
| U02 | Sessão final em 17/11/2026; proxy; versão web com dados fictícios; resultados e limites registrados |
| Consolidação da Entrega 14 | Concluída em 17/11/2026: quatro achados priorizados (AU04, AU01, AU03 e AU02), todos observados uma vez em participantes proxy |

## 7. Síntese das evidências e decisões atuais

| Evidência | O que permite concluir | O que não permite concluir | Decisão |
|---|---|---|---|
| U01 capturou sem ajuda | Conseguiu operar a captura naquela sessão | Precisão do algoritmo ou desempenho de trabalhadores agrícolas | Manter orientação; testar com perfil representativo |
| U01 seguiu aviso de distância | Orientação operacional foi acompanhada | Compreensão integral da porcentagem ou da IA | Explicar significado da confiança e registrar compreensão em avaliação posterior |
| U01 precisou de ajuda no histórico | Houve dificuldade de descoberta naquela sessão | Que todos os usuários terão a mesma dificuldade | Revisar acesso; AU03 |
| U01 elogiou textos e controles | Percepção positiva de clareza visual | Legibilidade sob sol, caminhando ou em condições reais de campo | Preservar clareza e investigar contexto real |
| U03 consultou histórico corretamente em 64 s | Conseguiu recuperar informações no protótipo | Atendimento da meta de 20 s | QA06 não atingida |
| U03 questionou autoria do veredito | Ambiguidade entre decisão humana e automática | Frequência do problema na população | Explicitar autoria; AU01 |
| U03 escolheu pedido por eliminação | Ambiguidade na distinção dos pedidos | Desempenho com todos os pedidos funcionais | Diferenciar pedidos e testar; AU02 |
| U03 reconheceu área e envio | Compreensão desses estados simulados | Implementação no aplicativo ou validade agronômica | Preservar feedback e investigar com especialista |
| U02 não percebeu o talhão sem inspeção | O rótulo “Sem ocorrência” não distinguiu ausência de inspeção naquela sessão | Que gestores reais cometeriam o mesmo erro, ou que o participante leu o talhão como livre da praga | Distinguir “não inspecionado no período”; AU04 |
| U02 usou só o relatório | O relatório bastou para as três tarefas naquela sessão | Que o mapa é dispensável para gestores | Manter H21 aberta |

## Como usar

- Manter identificadores estáveis e coerentes entre entregas.
- Citar hipóteses quando a necessidade ainda não tiver evidência.
- Distinguir observação, opinião, inferência e decisão.
- Identificar participantes proxy e limitações.
- Não substituir tempo estimado por tempo cronometrado.
- Não registrar ausência de problema como prova de inexistência.
- Preservar histórico de mudanças e hipóteses refutadas.
- Atualizar a matriz após U02 e após implementar ou testar melhorias.
- Registrar local de armazenamento e prazo de descarte das anotações de U01 na Entrega 14.
