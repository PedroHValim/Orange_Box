# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 01/11/2026  
**Revisão:** 16/11/2026  
**Status:** 🟩 concluída — plataforma, princípios e metas planejados; avaliação empírica nas Entregas 12–14 ainda em andamento.  
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e metas de usabilidade verificáveis, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| Contribuição técnica do TCC | Dataset, modelo de detecção do ácaro em imagens, processamento no dispositivo móvel e associação dos achados à localização. | O teste de IHC não substitui a avaliação da precisão, do desempenho ou da qualidade técnica do modelo. |
| Camada de interação — trabalhador (P02) | Rota do dia, orientação de captura, análise, resultado, registro do local, cobertura da rota e situação do envio (P01–P07 da Entrega 6). | Compreensão, conclusão da tarefa, tempo, erros, recuperação e facilidade percebida durante a inspeção. |
| Camada de interação — agrônomo (P03) | Pedidos de parecer e novas detecções, mapa do talhão, foto e histórico do ponto, veredito, delimitação da área, parecer e repasse ao gestor (A01–A03 e A05–A07 da Entrega 6; A04 foi retirada). | Compreensão, eficácia, eficiência, satisfação, erros e acessibilidade na análise técnica. |
| Camada de interação — gestor (P01) | Aviso de ciclo, resumo e cobertura do ciclo, talhões com focos, detalhe do talhão, posição registrada, evolução por ciclo, decisão e repasse a quem aplica (G01–G08 da Entrega 6). | Compreensão da cobertura e dos resultados, eficácia, tempo, erros e entendimento do repasse. |
| Integrações e dados simulados | Fotos, resultados da IA, localização, histórico, pedidos e repasses. | Resultados fictícios podem compor cenários de teste, desde que sejam apresentados como simulação. O teste avalia a interação, não a recomendação agronômica. |

**Fluxo de P02:** o modelo conceitual separa “salvo no celular” e “enviado ao gestor”. A versão do aplicativo da Entrega 11 não materializa todos os estados de rota e envio; essas partes de MU01 não poderão ser avaliadas nela, conforme o mapeamento da Entrega 12. A ausência de sinal em uma foto não comprova que a árvore esteja livre da praga.

**Fluxo de P03:** as telas A01–A07 identificam o fluxo conceitual. O aplicativo iOS não possui perfil de agrônomo; a Entrega 12 identifica separadamente o protótipo FA no Figma e quais metas MU04–MU09 podem ser observadas nele. Não presumir que atalhos, filtros ou avisos estejam implementados sem conferir a versão usada no teste.

**Fluxo de P01:** G01–G08 identificam estados do fluxo conceitual e da Entrega 6; o aplicativo iOS documentado na Entrega 11 cobre apenas parte deles. A Entrega 12 distingue metas MU10–MU16 avaliáveis, adaptadas e não avaliáveis na versão disponível. Evolução por ciclo, aviso de cobertura incompleta, registro de posição e repasse não devem ser atribuídos ao aplicativo quando não existirem.

## 1. Características da plataforma

A tabela reúne características da versão disponível e requisitos propostos. A coluna de consequências descreve necessidades de design; **não afirma que cada recurso já esteja implementado**.

| Característica | Trabalhador — P02 | Agrônomo — P03 | Gestor — P01 | Consequência para IHC |
|---|---|---|---|---|
| Software | Aplicativo CYF para iPhone no perfil Inspeção. | Fluxo proposto no protótipo FA em Figma; não há perfil de agrônomo no aplicativo iOS. | Aplicativo CYF para iPhone no perfil Administrador. | P02 precisa de captura curta; P03, de foto, localização e histórico organizados; P01, de resumo e talhões compreensíveis. |
| Hardware/dispositivos | iPhone com câmera e eventual lente macro. | Computador ou notebook para o protótipo FA; uso móvel durante visitas segue como hipótese. | iPhone na versão avaliável; outros dispositivos são hipótese. | Controles de captura adequados a P02, evidências ampliáveis para P03 e filtros legíveis para P01. |
| Capacidades previstas | Fotografar, analisar, apresentar resultado e registrar o ponto. | Examinar foto, local e histórico, validar detecções e emitir parecer. | Ver talhões, consultar resultados e apoiar a decisão de manejo. | Separar indicação da IA de confirmação humana e comunicar o significado dos resultados. |
| Restrições | Sol forte, deslocamento, pouco tempo por fruto e fotos sem nitidez. | Depende da qualidade das fotos enviadas e da possibilidade de examinar seu contexto. | Não valida a praga sozinho e depende do que foi registrado na inspeção. | Permitir refazer foto, pedir outra evidência quando necessário e explicar limites dos dados. |
| Conectividade | Pode faltar internet no pomar. | Fotos podem chegar depois da captura. | Dados podem depender do envio feito pelo campo. | Distinguir estados locais, envio e recebimento quando o fluxo os oferecer. |
| Segurança/privacidade | Fotos e localização podem revelar a atividade do trabalhador. | Fotos, mapas e pareceres podem identificar propriedades e o profissional. | Cobertura pode ser entendida como controle individual do trabalhador. | Limitar acesso e mostrar apenas identificação necessária à tarefa. |
| Volume/histórico | Inspeções se repetem em muitos pontos. | Pontos de vários talhões e períodos podem ser consultados. | Pode ser necessário comparar ciclos e talhões. | Oferecer consulta por local e período quando confirmada a necessidade. |
| Tempo de processamento | A análise ocorre durante a inspeção. | Fotos e pareceres podem exigir carregamento e envio. | Mapa e relatório podem demorar a carregar ou exportar. | Comunicar processamento, sucesso e falha com caminho de recuperação. |
| Papéis | Registra observações; não decide sozinho o manejo. | Analisa evidências e propõe orientação técnica. | Acompanha resultados e toma ou encaminha decisões de manejo. | Explicitar a autoria e o estado dos registros e distinguir os papéis. |

**Hipóteses de plataforma a confirmar:** dispositivos disponíveis na rotina, estabilidade da conexão, volume real de registros, comunicação entre papéis e necessidade de histórico. As capacidades propostas acima são requisitos de design, não prova de que estejam implementadas no aplicativo. A Entrega 12 confronta metas e versão avaliável.

## 2. Princípios gerais do projeto

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Contexto de uso — P02 | Inspeção a pé no pomar, sob sol e com conexão possivelmente instável. | Poucos passos, instruções curtas, captura e continuidade da tarefa. | Entregas 1, 3 e 5. |
| Contexto de uso — P03 | Análise a distância, dependente do que foi registrado em campo. | Organizar fotos, locais e histórico; oferecer saída quando a evidência for insuficiente. | Persona e cenário C03. |
| Contexto de uso — P01 | Revisão da situação da propriedade sem necessariamente reconhecer a praga. | Mostrar talhões e indicadores com significado claro e acesso à evidência. | Persona e cenário C01. |
| Prevenção e recuperação de erros | Foto inadequada, dúvida sobre o resultado e falhas de carregamento ou envio. | Permitir ajuste ou repetição e comunicar como recuperar a tarefa. | Entregas 5 e 6; heurísticas de Nielsen. |
| Privacidade e minimização | Fotos, locais e autoria podem identificar pessoas e propriedades. | Coletar apenas dados necessários e limitar o acesso. | LGPD, art. 6º. |
| Acessibilidade | Uso sob luz forte; mapas e estados que não devem depender só de cor. | Combinar texto, símbolo e cor; verificar contraste e tamanho dos controles. | WCAG 2.2. |
| Responsabilidade pelo parecer | Orientação de manejo exige julgamento profissional. | Não apresentar o resultado do modelo como parecer agronômico. | Requisitos do fluxo P03 e legislação aplicável. |
| Cobertura sem vigilância individual | Informações da rota podem ser interpretadas como controle do trabalhador. | Apresentar o necessário para cobertura da tarefa sem exposição desnecessária da pessoa. | Cenário C02; minimização de dados. |
| Dado e recomendação | Ordenação de talhões pode ser lida como recomendação de manejo. | Explicar o que o indicador mostra e preservar a decisão humana. | Cenário C01; tarefa T04. |
| Interação humano–IA | O profissional pode aceitar automaticamente uma indicação da IA. | Distinguir sinal do modelo e veredito humano; permitir revisar e rejeitar. | Amershi et al. (2019). |
| Visibilidade do estado | Usuários precisam saber se a análise, o registro ou a exportação terminaram. | Mostrar andamento, conclusão, falha e recuperação. | Heurísticas de Nielsen. |

## 3. Metas de usabilidade

As metas abaixo são critérios **planejados** para os fluxos conceituais. A Entrega 12 indica quais podem ser avaliadas como escritas, quais precisam de adaptação e quais não são avaliáveis na versão disponível. Não apresentar uma funcionalidade ausente como erro do participante.

### 3.1 Metas qualitativas

| Meta | Perfil/tarefa | Evidência desejada |
|---|---|---|
| Compreender o resultado sem atribuir certeza indevida à IA. | P02 / T02 | Explica que “sinal suspeito” não é confirmação profissional e que “nenhum sinal nesta foto” não garante árvore livre. |
| Recuperar-se de foto inadequada ou resultado inconclusivo. | P02 / T02 | Ajusta ou refaz a captura quando a versão permitir. |
| Distinguir cobertura e envio. | P02 / T01/T03 | Identifica pontos pendentes e diferencia registro local de envio, se esses estados estiverem disponíveis. |
| Diferenciar detecção da IA e validação humana. | P03 / T07 | Identifica o que depende do veredito do agrônomo. |
| Compreender o pedido de nova foto. | P03 / T07 | Entende que o ponto permanece pendente. |
| Compreender a situação do parecer. | P03 / T05 | Identifica conclusão e falha de envio. |
| Avaliar suficiência do contexto. | P03 / T05/T06 | Consulta foto, local e histórico ou pede outra evidência. |
| Observar influência da IA no julgamento. | P03 / T07 | Explica quando consultou a indicação automática e como a usou. |
| Identificar estados sem depender só da cor. | P03 / T07 | Diferencia pendente, confirmado e rejeitado por texto/símbolo. |
| Distinguir “sem focos” de “não inspecionado”. | P01 / T09 | Explica que ausência de inspeção não significa ausência de praga. |
| Compreender saídas diante de dúvida. | P01 / T09 | Distingue pedir parecer e pedir reinspeção, se essas ações existirem na versão. |
| Interpretar evolução entre ciclos. | P01 / T08 | Identifica tendência e limites de cobertura quando disponíveis. |
| Interpretar ordenação como dado. | P01 / T04 | Explica o significado da ordem da lista sem presumir recomendação automática. |
| Distinguir decisão registrada e repassada. | P01 / T04 | Identifica a situação real do repasse quando o fluxo existir. |

### 3.2 Metas quantitativas

**Condições:** usar cenários e dados equivalentes por perfil, registrar ajuda separadamente e informar `n/N` para cada meta. A Entrega 14 prevê **três participantes no total da equipe**, não três em cada perfil. Uma observação isolada não permite generalização estatística.

| ID | Dimensão | Métrica | Tarefa/escopo | Meta proposta | Como medir |
|---|---|---|---|---|---|
| MU01 | Eficácia | Fotografar, salvar um achado e identificar ponto pendente sem ajuda. | P02 / T01–T03; P01–P06. | Todos os participantes P02 que executarem a tarefa; informar `n/N`. A parte do ponto pendente não é avaliável no app atual. | Conclusão, erros e ajudas. |
| MU02 | Eficiência | Tempo da abertura da câmera à confirmação de registro. | P02 / T02. | Mediana ≤ 60 segundos quando houver mais de uma medição comparável; com uma pessoa, informar o tempo individual. | Cronômetro; registrar repetição da foto. |
| MU03 | Satisfação | Facilidade em escala de 1 a 7 após cada fluxo. | P02 / PF01/PF02. | Nota ≥ 5 por participante; calcular mediana se houver amostra comparável. | Pergunta pós-tarefa. |
| MU04 | Eficácia | Abrir pedido, validar pontos, delimitar área e enviar parecer. | P03 / T07/T05. | Todos os participantes P03 que executarem o fluxo; informar `n/N` e ajudas. | Conclusão e intervenções; adaptar ao número de pontos do FA. |
| MU05 | Prevenção de erro | Incluir pontos pendentes ou rejeitados na área. | P03 / T05. | Zero inclusão indevida. | Conferir a área escolhida. |
| MU06 | Eficiência | Localizar detecção anterior do ponto. | P03 / T06. | Tempo ≤ 20 segundos por participante; relatar tempos individuais. | Cronômetro até a resposta. |
| MU07 | Eficiência | Tempo do fluxo completo para cinco pontos. | P03 / T07/T05. | Mediana ≤ 8 minutos somente numa versão com cinco pontos; não avaliável como escrita no FA atual, que usa um ponto. | Tempo registrado apenas como referência na versão atual. |
| MU08 | Compreensão | Identificar se o parecer foi enviado, inclusive após falha simulada. | P03 / T05. | Todos os participantes expostos ao estado; informar `n/N`. | Pergunta e observação. |
| MU09 | Satisfação | Facilidade em escala de 1 a 7. | P03 / T05–T07. | Nota ≥ 5 por participante; informar média somente com amostra comparável. | Pergunta pós-tarefa. |
| MU10 | Eficácia | Rever situação do ciclo e registrar posição e decisão. | P01 / T09/T04. | Todos os participantes P01 que executarem o fluxo; informar `n/N` e ajudas. Registro de posição não é avaliável no app atual. | Conclusão e intervenções. |
| MU11 | Prevenção de erro | Tratar talhão não inspecionado como “sem focos”. | P01 / T09. | Zero ocorrência quando a diferença estiver visível no cenário. | Pergunta com resposta conhecida. |
| MU12 | Eficiência | Identificar tendência do talhão entre ciclos. | P01 / T08. | Tempo ≤ 30 segundos por participante numa versão que apresente a evolução; registrar como não avaliável se ausente. | Cronômetro até a resposta. |
| MU13 | Compreensão | Dizer se a última aplicação funcionou com base em dados suficientes. | P01 / T08. | Todos os participantes expostos aos dados; não avaliável na versão atual se a informação não existir. | Resposta comparada ao cenário. |
| MU14 | Eficiência | Tempo da revisão completa do ciclo. | P01 / T09/T04. | Mediana ≤ 10 minutos numa versão com o fluxo completo; na versão parcial, relatar apenas o tempo da tarefa adaptada. | Cronômetro. |
| MU15 | Compreensão | Diferenciar decisão registrada e repassada, inclusive após falha. | P01 / T04. | Todos os participantes expostos ao estado; não avaliável se o repasse não existir. | Pergunta pós-tarefa. |
| MU16 | Satisfação | Facilidade em escala de 1 a 7. | P01 / T09/T08/T04. | Nota ≥ 5 por participante; informar média somente com amostra comparável. | Pergunta pós-tarefa. |

**Critério de interpretação:** registrar também conclusão por tentativa e erro, ajudas e comentários. “Terminou a tarefa” não demonstra, sozinho, que a interação foi clara. Não alterar os limites depois do início da coleta para fazer a meta parecer atingida.

### 3.3 Priorização das metas

Os percentuais abaixo são **pesos de prioridade do projeto**, não resultados dos testes. Todas as metas MU01–MU16 participam da soma.

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

O peso não deve ser interpretado como taxa de sucesso. Metas não avaliáveis na versão disponível mantêm sua prioridade de projeto, mas recebem o resultado **“não avaliada”** na Entrega 14.

## 4. Como o ciclo será iterado

1. **Entrega 7:** confrontar hipóteses sobre rotina, tecnologia, histórico e responsabilidades com os dados que eventualmente forem coletados. Instrumento preparado não é evidência de participante.
2. **Entrega 6:** registrar os feedbacks da iteração formativa, revisões feitas no aplicativo e estados de papel que não foram materializados.
3. **Entrega 11:** identificar as telas do aplicativo para P01/P02 e do Figma para P03 sem declarar cobertura de conversas ausentes.
4. **Entrega 12:** mapear cada meta às tarefas avaliáveis e indicar explicitamente adaptações e partes não avaliáveis.
5. **Entregas 13 e 14:** confrontar problemas identificados por inspeção com comportamentos observados nas sessões; medir somente metas a que os participantes foram expostos.
6. **Após a avaliação:** relacionar evidência, problema, decisão de revisão e meta afetada na rastreabilidade.

## Checklist

- [x] Capacidades e restrições têm impacto de IHC explicitado.
- [x] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [x] Resultados e processamento de demonstração foram diferenciados de evidência de desempenho técnico.
- [x] Metas avaliam a interação, sem substituir métricas técnicas do TCC.
- [x] Princípios estão contextualizados para os perfis e as tarefas.
- [x] Metas quantitativas têm medida, tarefa e público definidos.
- [x] Eficácia, eficiência e satisfação foram consideradas.
- [x] Metas poderão ser verificadas nas Entregas 12–14: a Entrega 12 mapeia MU01–MU16 e registra as partes adaptadas ou não avaliáveis. Os resultados das sessões da Entrega 14 ainda estão pendentes.
