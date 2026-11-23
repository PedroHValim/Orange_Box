# Formulário de avaliação heurística — CYF

**Avaliador:** Lucas Cabral  
**Perfil/fluxo avaliado:** P02 — inspetor; consulta, registro e interpretação de vistorias  
**Versão planejada:** aplicativo iOS nativo (`ios-native/`), referência de 12/11/2026  
**Versão efetivamente examinada:** {{registrar versão instalada}}  
**Data da inspeção:** ____/____/________  
**Dispositivo/iOS:** {{modelo do iPhone e versão do iOS}}

**Telas a examinar:** Câmera, ajuda da Câmera, Mapa, associação da vistoria a um talhão, Histórico e detalhe da vistoria.

**Estados especiais a examinar:** modelo carregando; confiança baixa; ausência de detecção confirmada; registro salvo; localização indisponível; vistoria sem talhão associado; Histórico sem resultados no período; alteração da associação ao talhão; erro ao salvar, se reproduzível.

> Esta inspeção avalia a comunicação e o uso da interface. Não determina se o modelo identifica corretamente ácaros. Os dados da fazenda e as vistorias iniciais são demonstrativos.

## Procedimento

1. Registrar a versão, o aparelho, as permissões e as condições da inspeção.
2. Percorrer UT01, UT02 e UT03 da Entrega 12 no perfil demonstrativo **Inspeção**.
3. Examinar cada estado especial que puder ser reproduzido sem usar dados reais de propriedade.
4. Para cada possível problema, anotar a ação realizada, o que apareceu na tela e a consequência para a tarefa.
5. Relacionar cada problema a uma ou mais heurísticas, mas criar **um único ID para cada problema distinto**.
6. Atribuir severidade após considerar frequência provável, impacto na tarefa e possibilidade de recuperação.
7. Separar observações confirmadas no aparelho de hipóteses levantadas pela leitura do código.
8. Apagar a vistoria de teste criada durante a inspeção e restaurar os dados para os testes com participantes.

## Cobertura

Preencher **Violação?** somente após examinar o estado indicado. Usar `não examinado` quando a condição não puder ser reproduzida.

| H | Heurística | Fluxos/estados a examinar em P02 | Violação? | IDs dos problemas |
|---:|---|---|---|---|
| 1 | Visibilidade do status do sistema | Carregamento do modelo; análise pela Câmera; confirmação de salvamento; registro local; associação ao talhão. | {{sim / não / não examinado}} | {{...}} |
| 2 | Compatibilidade sistema–mundo real | Significado de “confiança”, “sem sinal confirmado”, “vistoria”, “talhão” e coordenadas para um inspetor. | {{sim / não / não examinado}} | {{...}} |
| 3 | Controle e liberdade do usuário | Voltar da Câmera; desistir da associação ao talhão; corrigir talhão associado; sair de filtros; apagar vistoria com confirmação. | {{sim / não / não examinado}} | {{...}} |
| 4 | Consistência e padrões | Comparar termos e estados mostrados na Câmera, no Histórico e no detalhe da vistoria. | {{sim / não / não examinado}} | {{...}} |
| 5 | Prevenção de erros | Captura com confiança baixa; exigência de localização; escolha de talhão; risco de interpretar ausência de detecção como ausência de praga. | {{sim / não / não examinado}} | {{...}} |
| 6 | Reconhecimento em vez de memorização | Identificação do registro recente; filtros do Histórico; indicação do talhão; distinção entre salvo e enviado. | {{sim / não / não examinado}} | {{...}} |
| 7 | Flexibilidade e eficiência de uso | Tempo e passos para fotografar, consultar a vistoria e localizar um registro anterior. | {{sim / não / não examinado}} | {{...}} |
| 8 | Estética e design minimalista | Legibilidade das mensagens sobrepostas à câmera; prioridade das informações no detalhe; leitura em ambiente iluminado. | {{sim / não / não examinado}} | {{...}} |
| 9 | Reconhecer, diagnosticar e recuperar erros | Mensagens e ações possíveis quando GPS, modelo, imagem ou salvamento falham. | {{sim / não / não examinado}} | {{...}} |
| 10 | Ajuda e documentação | Ajuda da Câmera e do Mapa; explicação do resultado, do limiar de confiança e da associação ao talhão. | {{sim / não / não examinado}} | {{...}} |

## Pontos de atenção para verificar

Os itens abaixo **não são violações confirmadas**. Foram identificados no planejamento e devem receber um ID na tabela de problemas somente se a inspeção encontrar evidência na interface.

- A mensagem “Registro salvo neste aparelho” deixa claro que outra pessoa ainda não recebeu a vistoria?
- “Sem sinal confirmado” no Histórico e “Nenhuma praga confirmada” no detalhe transmitem a mesma ideia? Alguma expressão pode sugerir, indevidamente, que toda a área está livre de praga?
- Após a captura, fica clara a diferença entre **vistoria salva** e **vistoria associada a um talhão**?
- Ao faltar localização ou ao surgir confiança baixa, a mensagem indica uma ação possível para continuar?
- Ao abrir o Histórico sem resultados para o período selecionado, a pessoa entende que pode mudar o período?
- As orientações permanecem legíveis quando a câmera é usada sob luz forte?

## Problemas encontrados

Criar uma linha por problema confirmado. Em **Evidência**, registrar o texto exibido, a sequência de ações e, se permitido pela equipe, uma captura **somente da interface**, sem pessoas nem dados reais. Não preencher esta tabela com resultados presumidos.

| ID | H | Tela/estado | Ação/condição | Problema observado | Consequência para a tarefa | Evidência | Severidade 0–4 | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---|---|---:|---|---|
| V01 | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |
| V02 | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

## Escala de severidade

| Nota | Significado |
|---:|---|
| 0 | Não foi confirmada uma violação; registrar apenas como observação, se útil. |
| 1 | Problema superficial, com pouco efeito sobre a tarefa. |
| 2 | Problema moderado: causa dúvida ou atraso, mas há recuperação clara. |
| 3 | Problema grave: dificulta bastante ou impede uma tarefa importante. |
| 4 | Problema crítico: pode levar a uma conclusão perigosa, como tratar “sem detecção” como ausência de praga ou considerar uma vistoria local como enviada. |

A nota deve ser justificada pela **consequência observada ou plausível na tarefa**, e não somente pela aparência da tela.

## Síntese após a inspeção

**Estados efetivamente examinados:** {{...}}  
**Estados que não puderam ser reproduzidos e motivo:** {{...}}  
**Quantidade de problemas por severidade:** 0: {{...}} · 1: {{...}} · 2: {{...}} · 3: {{...}} · 4: {{...}}  
**Problemas a corrigir antes do teste com participantes:** {{IDs e justificativa, se houver}}  
**Problemas a observar durante UT01–UT03:** {{IDs, se houver}}  
**Limitações da inspeção:** {{por exemplo, ausência de GPS, modelo indisponível ou teste fora do pomar}}

> A inspeção heurística não substitui o teste com participantes. Atualizar este formulário com evidências reais antes de marcar sua execução como concluída na Entrega 12.

---

# Formulário de avaliação heurística — P03, fluxo do agrônomo (telas FA)

**Avaliador:** Guilherme Morais Escudeiro  
**Perfil/fluxo avaliado:** P03 — agrônomo; validação a distância, área de aplicação e parecer (MoLIC M01)  
**Versão planejada:** protótipo no Figma, telas FA01–FA07 (Entrega 11)  
**Versão efetivamente examinada:** Figma, versão de ____/____/________  
**Data da inspeção:** ____/____/________  
**Computador/navegador:** ____

**Telas a examinar:** FA01 (pedidos de parecer), FA02 (mapa do talhão), FA03 (detecção do ponto), FA05 (histórico), FA06 (área de aplicação), FA07 (parecer técnico).

**Estados a examinar:** FA01V (nenhum pedido), FA01C (parecer enviado), FA02V (ponto validado), FA02R (retorno à revisão), FA02N (nova foto pedida), FA03A (foto ampliada e avaliação da IA), FA03E (falha ao registrar), FA05V (nenhuma detecção), FA06E (área ou campos inválidos), FA07E (falha no envio).

> Esta inspeção avalia a comunicação e o uso da interface. Não determina se a IA identifica corretamente o ácaro nem se o parecer é agronomicamente correto. Todos os dados do protótipo são fictícios.

## Procedimento

1. Registrar a versão do arquivo e o navegador.
2. Percorrer UT06, UT07 e UT05 da Entrega 12 no modo de apresentação.
3. Examinar os estados acima pelo modo de apresentação ou, quando não estiverem ligados no caminho do protótipo, diretamente no arquivo, anotando de qual forma cada um foi examinado.
4. Para cada possível problema, anotar a tela, o que aparece e a consequência para a tarefa do agrônomo.
5. Criar **um único ID para cada problema distinto** (`A02-V01`, `A02-V02`...), relacionado a uma ou mais heurísticas.
6. Atribuir severidade considerando frequência provável, impacto na tarefa e recuperação.
7. Separar limitações do protótipo (quadros sem ligação, figura no lugar da foto) de problemas de design.

## Cobertura

| H | Heurística | Fluxos/estados a examinar em P03 | Violação? | IDs dos problemas |
|---:|---|---|---|---|
| 1 | Visibilidade do status do sistema | Situação de cada ponto (○ ● ×) e contagem em FA02; retorno após veredito (FA02V) e após pedir nova foto (FA02N); situação do pedido em FA01 após o envio (FA01C). | sim / não / não examinado | |
| 2 | Compatibilidade sistema–mundo real | Termos “pedido de parecer”, “veredito”, “detectado pela IA”, “validado por”, “sinal forte/fraco”, “área de aplicação” para um agrônomo. | sim / não / não examinado | |
| 3 | Controle e liberdade do usuário | “Voltar ao mapa do talhão”, “Encerrar revisão”, “Voltar à área de aplicação”, “Voltar e validar o restante”, acesso a pedidos e histórico pelo menu. | sim / não / não examinado | |
| 4 | Consistência e padrões | Mesmos símbolos e cores de situação em FA01, FA02, FA03, FA05 e FA06; mesma posição dos botões de voltar. | sim / não / não examinado | |
| 5 | Prevenção de erros | Aviso de pontos pendentes em FA06 (não bloqueia); só pontos confirmados como base da área; aviso do receituário em FA07. | sim / não / não examinado | |
| 6 | Reconhecimento em vez de memorização | Detecções anteriores na própria FA03; filtro do histórico visível em FA05; resumo do parecer em FA07. | sim / não / não examinado | |
| 7 | Flexibilidade e eficiência de uso | Atalho “Ver histórico deste ponto”; próximo ponto pendente em destaque; histórico pelo menu (busca sem filtro). | sim / não / não examinado | |
| 8 | Estética e design minimalista | Densidade de informação em FA03 e FA07; avaliação da IA recolhida; legibilidade das tabelas de FA01 e FA05. | sim / não / não examinado | |
| 9 | Reconhecer, diagnosticar e recuperar erros | FA03E, FA06E e FA07E: texto do erro, campo indicado e dados mantidos. | sim / não / não examinado | |
| 10 | Ajuda e documentação | Legenda fixa em FA02; subtítulos de cada tela; explicação do veredito em FA03. | sim / não / não examinado | |

## Pontos de atenção para verificar

Os itens abaixo **não são violações confirmadas**; vêm do planejamento (Entrega 12, QA21) e só recebem ID se a inspeção encontrar evidência.

- O aviso de pontos pendentes em FA06 não bloqueia o avanço. Fica claro que esses pontos ficam fora da área?
- A situação do parecer aparece só na lista de pedidos (FA01). Fica claro, após o envio, que o pedido passou a “concluído”?
- A avaliação da IA fica recolhida em FA03. Quem quer consultá-la a encontra?
- A delimitação da área depende do mouse. Há alternativa por teclado (marcar os pontos em lista)?
- A situação dos pontos é legível sem depender da cor (símbolo e texto)?

## Problemas encontrados

| ID | H | Tela/estado | Ação/condição | Problema observado | Consequência para a tarefa | Evidência | Severidade 0–4 | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---|---|---:|---|---|
| A02-V01 | | | | | | | | | |

Escala de severidade: a mesma do formulário de P02 acima. Para P03, nota 4 inclui levar o agrônomo a considerar ponto não confirmado dentro da área ou a supor que um parecer não enviado chegou ao gestor.

## Síntese após a inspeção

**Estados examinados no modo de apresentação / só no arquivo:** ____  
**Quantidade de problemas por severidade:** 0: __ · 1: __ · 2: __ · 3: __ · 4: __  
**Problemas a corrigir antes do teste ou mantidos para comparação, com justificativa:** ____  
**Problemas a observar durante UT06, UT07 e UT05:** ____  
**Limitações da inspeção:** protótipo com quadros prontos, figura no lugar da foto, avaliador que participou do projeto das telas.

> A inspeção heurística não substitui o teste com participantes.

---

# Formulário de avaliação heurística — P01, fluxo do gestor (perfil Administrador)

> Seção acrescentada na revisão de 20/11/2026, depois da inspeção de A03 registrada na Entrega 13. Documenta o escopo e o procedimento para a reinspeção; não comprova que estava formalizada antes da execução.

**Avaliador:** Pedro Henrique Ferreira Valim (A03)  
**Perfil/fluxo avaliado:** P01 — gestor; revisão do período, comparação entre períodos e envio do relatório (MoLIC M03)  
**Versão planejada:** aplicativo iOS nativo (`ios-native/`), commit `a36785f` (12/11/2026), perfil Administrador  
**Versão efetivamente examinada:** ____  
**Data da inspeção:** ____/____/________  
**Dispositivo/iOS:** ____

**Telas a examinar:** Acesso (perfil Administrador), Relatórios, Mapa, detalhe do talhão, Histórico e Conta.

**Estados a examinar:** talhão sem inspeção no período; talhão inspecionado sem ocorrência; variação sem dados no período anterior; lista de talhões recolhida e expandida; filtros combinados e sem resultados; registro de pulverização e sua confirmação; exportação do relatório (processamento, sucesso e cancelamento); mensagens de erro e retorno existentes.

> Esta inspeção avalia a comunicação e o uso da interface. Não determina se o modelo identifica corretamente ácaros nem se a decisão de manejo é correta. Os dados da fazenda são demonstrativos.

## Procedimento

1. Registrar versão, aparelho e condições da inspeção.
2. Percorrer UT09, UT08 e UT04 da Entrega 12 no perfil Administrador.
3. Preparar o talhão sem inspeção (Entrega 12, “Preparação dos dados de P01”) e examinar cada estado acima.
4. Para cada possível problema, anotar a ação, o que apareceu na tela e a consequência para a tarefa do gestor, com **captura da tela**.
5. Criar um único ID por problema distinto (`A03-Vxx`), relacionado a uma ou mais heurísticas.
6. Atribuir severidade considerando frequência provável, impacto e recuperação.
7. Comportamento visto só no código vai para “Problemas potenciais pendentes de reprodução”, sem severidade final e fora da contagem, até ser reproduzido e capturado.
8. Restaurar os dados demonstrativos ao final.

## Cobertura

| H | Heurística | Fluxos/estados a examinar em P01 | Violação? | IDs dos problemas |
|---:|---|---|---|---|
| 1 | Visibilidade do status do sistema | Talhão sem inspeção versus sem ocorrência; retorno após registrar pulverização e após exportar. | sim / não nos estados observados / não examinado | |
| 2 | Compatibilidade sistema–mundo real | “Detecções confirmadas”, “pragas”, “Sem ocorrência”, “reentrada”, nomes técnicos. | sim / não nos estados observados / não examinado | |
| 3 | Controle e liberdade do usuário | Desfazer pulverização registrada; cancelar exportação; voltar do detalhe do talhão. | sim / não nos estados observados / não examinado | |
| 4 | Consistência e padrões | Mesmos números em Mapa, Conta e Relatórios; mesma semântica de cor no mapa e no gráfico; nomes dos filtros. | sim / não nos estados observados / não examinado | |
| 5 | Prevenção de erros | Registro de pulverização com um toque; variação calculada sem dados anteriores. | sim / não nos estados observados / não examinado | |
| 6 | Reconhecimento em vez de memorização | Identificação dos talhões no mapa em diferentes zooms; lista de talhões recolhida. | sim / não nos estados observados / não examinado | |
| 7 | Flexibilidade e eficiência de uso | Filtros por período e talhão; atalhos entre relatório, mapa e histórico. | sim / não nos estados observados / não examinado | |
| 8 | Estética e design minimalista | Controles de cadastro (Desenhar, GeoJSON) junto da informação gerencial. | sim / não nos estados observados / não examinado | |
| 9 | Reconhecer, diagnosticar e recuperar erros | Falhas de exportação, de carregamento do mapa e de gravação. | sim / não nos estados observados / não examinado | |
| 10 | Ajuda e documentação | Explicação dos indicadores, da variação e dos critérios de contagem. | sim / não nos estados observados / não examinado | |

## Problemas encontrados

| ID | H | Tela/estado | Ação/condição | Problema observado | Consequência para a tarefa | Evidência (captura) | Severidade 0–4 | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---|---|---:|---|---|
| A03-V01 | | | | | | | | | |

## Problemas potenciais pendentes de reprodução

| ID | H provisória | Local no código | Comportamento esperado | O que falta para confirmar |
|---|---|---|---|---|
| | | | | captura, estado, heurística e severidade |

Escala de severidade: a mesma do formulário de P02 acima. Para P01, nota 3 ou 4 inclui levar o gestor a tratar talhão não inspecionado como livre da praga ou a decidir com números divergentes sem saber o critério.

## Síntese após a inspeção

**Estados examinados / não examinados:** ____  
**Quantidade de violações por severidade:** 0: __ · 1: __ · 2: __ · 3: __ · 4: __  
**Problemas potenciais pendentes de reprodução:** ____  
**Problemas a observar durante UT09, UT08 e UT04:** ____  
**Limitações da inspeção:** avaliador participou do projeto; protótipo FA fora do escopo de A03.

> A inspeção heurística não substitui o teste com participantes.
