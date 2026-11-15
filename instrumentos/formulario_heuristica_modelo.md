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
