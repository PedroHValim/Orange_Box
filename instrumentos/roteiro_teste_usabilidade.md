# Roteiro de teste de usabilidade — CYF

**Versão planejada:** aplicativo iOS nativo (`ios-native/`), referência de 12/11/2026  
**Aplicador do fluxo P02:** Lucas Cabral  
**Participantes planejados para P02:** três, mais um piloto que não integra os resultados  
**Duração prevista por sessão P02:** 20 a 30 minutos

## 1. Antes da sessão

1. Conferir a versão instalada, o modelo de detecção e o funcionamento do iPhone físico com iOS 17 ou superior.
2. Entrar na conta demonstrativa do perfil **Inspeção**.
3. Conferir câmera, localização e carregamento do mapa. Não executar as tarefas no lugar do participante.
4. Confirmar que os registros demonstrativos estão disponíveis, inclusive o do **Talhão 05 · Experimental Sul**, usado em UT01.
5. Separar a fruta ou imagem de teste. No piloto, verificar se ela permite concluir UT02 sem depender da detecção de um ácaro real.
6. Registrar quantas vistorias existem antes da sessão e preparar a planilha de observação com o código L__.
7. Separar as instruções de UT01–UT03, sem mostrar ao participante os objetivos ocultos ou os critérios de sucesso.
8. Disponibilizar o termo de consentimento. **Não haverá gravação de tela, áudio ou vídeo.**

**Restauração entre sessões:** apagar a vistoria de teste criada, verificar o estado dos dados demonstrativos e restaurar o estado inicial do aplicativo pelo procedimento confirmado no piloto. Não reutilizar dados produzidos por outro participante.

## 2. Abertura padronizada

Ler ao participante:

> Obrigado por participar. Você realizará algumas tarefas no aplicativo CYF enquanto observamos se as informações e os caminhos de uso estão claros. Estamos avaliando o aplicativo, não seu desempenho. Você pode fazer perguntas, pular uma tarefa ou encerrar a participação a qualquer momento. Os dados exibidos sobre a fazenda são exemplos, e o resultado da análise é experimental. Hoje não estamos testando se o modelo identifica corretamente uma praga. Não faremos gravações; anotaremos apenas o necessário para analisar a interação, sem seu nome nos resultados. Antes de começar, você gostaria de esclarecer algo?

Obter o consentimento **antes** do pré-teste e das tarefas. Não explicar onde ficam os comandos. Se for solicitado que a pessoa comente o que está pensando, esclarecer que isso é opcional; não exigir fala contínua.

## 3. Perfil pré-teste — P02

Registrar apenas:

1. Você realiza ou já realizou inspeções de plantas ou frutos? Em qual cultura e há quanto tempo?
2. Como costuma registrar o que encontra nessas inspeções?
3. Que aparelho costuma utilizar para esse trabalho?
4. Você usa iPhone no dia a dia?

**Classificação do perfil:** ( ) inspetor de citros ( ) experiência próxima em inspeção vegetal ( ) participante substituto  
**Justificativa da classificação:** {{preencher após o pré-teste}}

Se a pessoa for substituta, registrar essa limitação na análise; não apresentá-la como inspetor de citros.

## 4. Tarefas

Aplicar UT01, UT02 e UT03 **nessa ordem**. Ler uma instrução por vez. As explicações da coluna central só podem esclarecer o contexto, sem indicar um caminho na interface.

| ID | Instrução ao participante | O moderador pode esclarecer | O moderador não deve dizer |
|---|---|---|---|
| UT01 | “Você vai continuar uma vistoria. Descubra o que foi registrado anteriormente na área que eu indicar e explique o que esse registro permite concluir.” | Qual área foi indicada para o cenário de teste, se a pessoa não ouviu ou não compreendeu a referência. | Que deve abrir o Histórico, qual registro selecionar ou que “sem sinal confirmado” não prova ausência de praga na área. |
| UT02 | “Examine esta fruta de teste usando o aplicativo e deixe sua vistoria registrada para consulta posterior.” | Que a fruta/imagem é somente material de teste e que não se espera um diagnóstico real. | Que deve abrir a Câmera, pressionar determinado botão ou escolher uma opção específica de associação ao talhão. |
| UT03 | “Encontre a vistoria que você acabou de fazer. Mostre o resultado e diga se outra pessoa já recebeu esse registro.” | Que “outra pessoa” significa alguém fora do iPhone usado no teste. | Que deve abrir o Histórico ou responder que o aplicativo não confirma envio. |

**Para o aplicador, sem leitura ao participante:**

- **UT01:** verificar se encontra o registro indicado do Talhão 05, identifica ausência de detecção confirmada na vistoria e não conclui que todo o talhão está livre de praga.
- **UT02:** verificar se conclui o registro, percebe o feedback de salvamento local e distingue registro salvo de associação a um talhão. Medir o tempo da Câmera pronta até a confirmação de salvamento.
- **UT03:** verificar se encontra a vistoria recente, interpreta o resultado como informação experimental e não presume que o registro já foi enviado.

**Tarefas de Pedro (P01):** {{manter o roteiro UT09, UT08 e UT04 definido por Pedro na Entrega 12}}  
**Tarefas de Guilherme (P03):** {{preencher por Guilherme}}

## 5. Durante cada tarefa

O observador anota horário de início e fim, conclusão, erros, hesitações observáveis, comentários, pedidos de ajuda e intervenções. Não classificar silêncio, por si só, como dificuldade.

O aplicador não oferece dicas espontâneas. Pode oferecer uma dica somente após **dois pedidos de ajuda** ou aproximadamente **um minuto sem progresso**, registrando o momento e o conteúdo da intervenção. Problemas técnicos de câmera, modelo, GPS ou aparelho devem ser anotados separadamente das dificuldades de interação.

Se a captura ficar bloqueada por uma condição técnica ou pela amostra de teste, registrar o impedimento. Não declarar UT02 concluída nem atribuir um tempo de execução inventado. Após aproximadamente dois minutos sem possibilidade de prosseguir, seguir o procedimento de recuperação definido no piloto ou encerrar a tarefa como impedida.

Observar especialmente:

- compreensão das mensagens de confiança e de localização;
- diferença entre registro salvo no iPhone e registro enviado;
- diferença entre “sem sinal confirmado” e ausência de praga na área;
- percepção de que uma vistoria pode estar salva sem estar associada a um talhão;
- recuperação diante de mensagens de erro.

## 6. Pós-tarefa

Após **cada** tarefa, perguntar:

1. “Quão fácil foi realizar esta tarefa?”  
   **1 = muito difícil; 7 = muito fácil.**
2. “O que facilitou ou dificultou?”

Registrar a nota após UT01, UT02 e UT03. As medianas de **UT02 e UT03** serão comparadas com MU03. Não explicar previamente qual nota seria considerada satisfatória.

## 7. Encerramento

Fazer as perguntas sem indicar a resposta esperada:

1. “O que você entende pelo resultado mostrado nesta vistoria?”
2. “Onde esse registro está guardado?”
3. “Ele já foi enviado a alguém? O que no aplicativo lhe dá essa impressão?”
4. “Se precisasse voltar a um ponto ainda não visitado, como faria hoje?”
5. “Há algo que você mudaria para usar o aplicativo durante uma vistoria?”

Agradecer e lembrar como as anotações serão usadas. Completar a planilha com o código anônimo, registrar limitações de perfil e ambiente, apagar a vistoria criada e preparar o aparelho para a sessão seguinte.

## 8. Condições para a análise

Comparar os resultados de P02 com MU01–MU03 da Entrega 8, registrando as adaptações da Entrega 12. Não afirmar que foram avaliados roteiro de visita, pontos pendentes, cobertura da rota ou transmissão de vistorias: essas funções não estão presentes na versão testada.
