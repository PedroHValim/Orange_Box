# Entrega 9 — Modelo conceitual e design centrado na comunicação

**Data:** 01/11/2026<br>
**Status:** 🟨 em andamento — parte de Lucas preparada; consolidação da equipe pendente.<br>
**Responsabilidade:** soluções individuais, com consolidação da equipe para mapa de objetivos e esquema de signos.

## Objetivo da atividade

Passar dos cenários de problema para uma concepção da interação, explicitando objetivos, tópicos de conversa, falas e signos compreensíveis aos usuários.

## Transformando resultados técnicos em conceitos compreensíveis

No fluxo do trabalhador, termos como “inferência”, “metadados EXIF” e “sincronização” serão comunicados como **analisando a foto**, **local do registro** e **situação do envio**. A interface distinguirá um sinal apontado pela IA de uma confirmação humana.

## 1. Cenários de interação

### CI01 — {{título do cenário de Pedro}}

**Autor(a):** Pedro — {{matrícula}}<br>
**Origem:** cenário de problema C01.

{{Inserir cenário de interação. Marcar em negrito os trechos alterados em relação a C01.}}

### CI02 — Inspeção dos frutos e repasse dos achados

**Autor(a):** Lucas — 24.123.032-5<br>
**Origem:** cenário de problema C02, “Inspeção manual de frutos com lupa, sob fadiga e sem registro do percurso”.

Antônio recebe do gestor as áreas que deve percorrer e caminha entre as árvores do pomar. **No celular, abre a rota do dia e vê o próximo ponto planejado e os pontos que já possuem registro.** Em cada árvore, escolhe os frutos para inspeção. **Ao abrir a câmera, recebe uma orientação curta sobre distância, iluminação e foco; se a imagem estiver inadequada, pode ajustá-la antes de fotografar.**

O ácaro é pequeno e pode ser confundido com marcas da casca. **Depois da foto, o aplicativo informa que está analisando a imagem no próprio celular, mesmo sem internet. O resultado aparece como “sinal suspeito”, “nenhum sinal nesta foto” ou “resultado inconclusivo”. Antônio pode ouvir o resultado e refazer a foto quando estiver em dúvida. A mensagem deixa claro que o resultado da IA não equivale à confirmação da praga.**

Quando encontra um sinal suspeito, Antônio precisa avisar quem decide o que fazer. **Ao salvar o achado, o aplicativo associa foto, data, hora e local disponível. Se o GPS não fornecer a posição, Antônio identifica talhão, linha e árvore manualmente; o registro fica marcado como “local manual, sem coordenadas”.** Ele continua a inspeção sem esperar conexão.

Ao final do percurso, Antônio costumava depender da memória para saber se deixou algum ponto passar. **Agora confere os pontos planejados com e sem registro. Se encerrar com pendências, a rota continua identificada como incompleta. Os achados ficam “salvos no celular” até que haja conexão; depois o aplicativo mostra “enviando” e “enviado ao gestor”, ou permite tentar novamente em caso de falha. “Enviado” não significa que o gestor já leu o registro.**

Os trechos em **negrito** descrevem a interação proposta. Eles ainda precisam ser avaliados com usuários; não são observações de uso real.

### Diferenças relevantes — CI02

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Rota com pontos planejados e registrados. | Reduzir a dúvida sobre locais esquecidos. | C02; HTA T01 e CTT T03 da Entrega 5. |
| Orientação de foco e possibilidade de refazer a foto. | Prevenir resultado baseado em imagem inadequada. | C02; GOMS T02; análise de interfaces da Entrega 2. |
| Resultado em linguagem curta, com alternativa inconclusiva. | Evitar que uma indicação da IA seja entendida como diagnóstico definitivo. | Dúvida do trabalhador em C02; GOMS T02. |
| Local automático ou identificação manual. | Evitar repasse baseado apenas na memória quando não houver GPS. | C02; HTA T01, etapa de comunicar o achado. |
| Estados distintos para salvo, enviando e enviado. | Permitir trabalhar offline e verificar se o repasse ocorreu. | Jornada de P02 da Entrega 3; CTT T03. |

### CI03 — {{título do cenário de Guilherme}}

**Autor(a):** Guilherme — {{matrícula}}<br>
**Origem:** cenário de problema C03.

{{Inserir cenário de interação. Marcar em negrito os trechos alterados em relação a C03.}}

## 2. Design centrado na comunicação

**Nome do cenário:** CI02 — inspeção dos frutos e repasse dos achados.

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| Iniciar a inspeção > escolher o próximo ponto | `U: Qual ponto devo inspecionar agora?` / `D: Próximo ponto: talhão, linha e árvore; estes pontos já têm registro e estes estão pendentes.` | Orientar a continuidade sem afirmar que todas as árvores do talhão foram examinadas. |
| Capturar o fruto > ajustar a imagem | `U: A foto está boa para analisar?` / `D: Ajuste a distância e o foco antes de fotografar.` | Prevenir captura inadequada. |
| Analisar a foto > aguardar | `U: O que está acontecendo?` / `D: Analisando a foto no celular.` | Informar o estado da tarefa sem depender da internet. |
| Entender o resultado > sinal suspeito | `U: É a praga?` / `D: Sinal suspeito nesta foto; precisa de confirmação.` | Comunicar a indicação da IA e seu limite. |
| > nenhum sinal na foto | `U: Posso considerar a árvore livre da praga?` / `D: Nenhum sinal nesta foto; isso não garante que toda a árvore esteja livre.` | Evitar uma conclusão além da imagem analisada. |
| > resultado inconclusivo | `U: E se eu não tiver certeza?` / `D: Não foi possível concluir. Refaça a foto ou salve para conferir depois.` | Permitir recuperação sem forçar uma decisão. |
| Registrar o achado > identificar o local | `U: Onde este fruto foi encontrado?` / `D: Local obtido por GPS; se não estiver disponível, informe talhão, linha e árvore.` | Manter o contexto do achado e indicar quando o local foi informado manualmente. |
| Repassar os achados > conferir o envio | `U: O gestor já recebeu?` / `D: Salvo no celular; aguardando conexão / enviando / enviado ao gestor / falha no envio.` | Diferenciar armazenamento local, envio e falha. |

**Convenção:** `U` = usuário; `D` = preposto do designer/sistema.

**Design centrado na comunicação — Pedro:** {{inserir tópicos, falas e signos de CI01}}.

**Design centrado na comunicação — Guilherme:** {{inserir tópicos, falas e signos de CI03}}.

## 3. Mapa de objetivos

### Mapa individual — Lucas

**Objetivo principal:** inspecionar a rota e repassar os achados com confiança.

- **O01 — Inspecionar os pontos da rota**
  - Identificar o próximo ponto planejado.
  - Distinguir pontos com registro de pontos pendentes.
- **O02 — Obter uma foto analisável**
  - Ajustar enquadramento e foco.
  - Fotografar ou refazer a captura.
- **O03 — Entender o resultado da foto**
  - Distinguir suspeita, ausência de sinal na foto e resultado inconclusivo.
  - Decidir entre seguir, refazer ou guardar para conferência.
- **O04 — Registrar o achado e seu local**
  - Salvar foto, resultado, data e hora.
  - Usar o local obtido ou identificar o ponto manualmente.
- **O05 — Confirmar o repasse dos registros**
  - Verificar pendências da rota.
  - Distinguir registro salvo de registro enviado.
  - Recuperar-se de falha no envio.

**Mapa individual — Pedro:** {{inserir mapa e IDs sem repetir os objetivos acima}}.

**Mapa individual — Guilherme:** {{inserir mapa e IDs sem repetir os objetivos acima}}.

**Mapa consolidado da equipe:** pendente. Ao reunir os três mapas, verificar se termos como “achado”, “detecção”, “foco” e “ponto” estão sendo usados para conceitos diferentes antes de unir objetivos.

![Mapa consolidado](../assets/09_modelo_conceitual/mapa_objetivos.svg)

### Dicionário de objetivos

| ID | Objetivo | Persona(s) | Cenário(s) | Prioridade |
|---|---|---|---|---|
| O01 | Inspecionar os pontos da rota. | P02 | CI02 | Alta |
| O02 | Obter uma foto analisável. | P02 | CI02 | Alta |
| O03 | Entender o resultado da foto. | P02 | CI02 | Alta |
| O04 | Registrar o achado e seu local. | P02 | CI02 | Alta |
| O05 | Confirmar o repasse dos registros. | P02 | CI02 | Alta |
| {{ID}} | {{objetivo de Pedro}} | {{...}} | CI01 | {{...}} |
| {{ID}} | {{objetivo de Guilherme}} | {{...}} | CI03 | {{...}} |

**Numeração:** O01–O05 identificam o mapa de Lucas nesta versão. A equipe deve conferir e fixar os IDs no mapa consolidado antes de reutilizá-los na Entrega 10.

## 4. Esquema conceitual de signos

A tabela abaixo já reúne os signos do fluxo de Lucas. Pedro e Guilherme devem acrescentar seus signos **nesta mesma tabela**, reaproveitando as linhas existentes quando se tratar do mesmo conceito.

| Grupo | Signo | Origem | Observações/semântica | Tipo de conteúdo | Restrição | Valor padrão | Prevenção | Recuperação |
|---|---|---|---|---|---|---|---|---|
| Rota | Ponto planejado | Domínio/gestor | Local indicado para inspeção; não significa que foi visitado. | Talhão, linha e árvore | Deve identificar o ponto na rota. | Próximo pendente | Mostrar identificador do ponto. | Voltar à rota e selecionar outro ponto. |
| Rota | Situação do ponto | Sistema | “Com registro” ou “pendente”; não indica ausência de praga. | Estado | Não confundir com resultado da foto. | Pendente | Exibir texto e símbolo além de cor. | Abrir o ponto e conferir registros. |
| Captura | Foto do fruto | Usuário | Imagem que será analisada. | Imagem | Deve ter qualidade suficiente para análise. | Nenhuma | Orientar foco, distância e iluminação. | Ajustar ou refazer a foto. |
| Captura | Qualidade da foto | Sistema | Indica possível problema de foco ou enquadramento. | Estado/mensagem | Não equivale ao resultado da análise. | Aguardando captura | Avisar antes de fotografar. | Reposicionar e tentar novamente. |
| Análise | Situação da análise | Sistema | “Analisando”, “concluída” ou “falhou”. | Estado/mensagem | Informar quando não houver conclusão. | Aguardando foto | Mostrar progresso textual. | Cancelar ou tentar novamente. |
| Resultado | Resultado da foto | Sistema | “Sinal suspeito”, “nenhum sinal nesta foto” ou “inconclusivo”. É indicação da IA, não validação humana. | Texto e símbolo | Vinculado à foto analisada. | Nenhum | Explicar o alcance de cada mensagem. | Refazer a foto ou guardar para conferência. |
| Registro | Data e hora da captura | Sistema | Momento em que a foto foi obtida, distinto do horário de envio. | Data e hora | Associadas ao registro. | Captura atual | Mostrar no resumo. | Corrigir por nova captura se o registro estiver incorreto. |
| Registro | Local do achado | Sistema ou usuário | Posição obtida por GPS ou identificação manual do ponto. | Coordenadas ou talhão/linha/árvore | Indicar a origem do local. | Tentar GPS | Mostrar se o local foi obtido. | Informar local manualmente se faltar GPS. |
| Registro | Situação do registro | Sistema | “Salvo no celular”; ainda não significa que o gestor o recebeu. | Estado/mensagem | Registro deve permanecer acessível. | Não salvo | Confirmar o salvamento. | Tentar salvar novamente sem descartar a foto. |
| Repasse | Destinatário | Domínio | Papel que receberá os achados, como o gestor da propriedade. | Função | Deve estar definido para o repasse. | Gestor da rota, se previamente definido | Mostrar a função no resumo. | Corrigir o destinatário antes do envio, conforme regras da equipe. |
| Repasse | Situação do envio | Sistema | “Aguardando conexão”, “enviando”, “enviado” ou “falha”; enviado não significa lido. | Estado/mensagem | Separada da situação do registro local. | Aguardando, se offline | Mostrar texto e quantidade pendente. | Tentar novamente mantendo os dados salvos. |
| {{grupo}} | {{signo de Pedro}} | {{usuário/sistema/domínio}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |
| {{grupo}} | {{signo de Guilherme}} | {{usuário/sistema/domínio}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

**GPS:** sistema de posicionamento utilizado quando há localização disponível. Um local informado manualmente não será apresentado como coordenada obtida automaticamente.

## Síntese

**Lucas:** os diagramas MoLIC deverão contemplar O01–O05 e as conversas sobre selecionar ponto, ajustar e capturar a foto, aguardar a análise, interpretar cada tipo de resultado, registrar o local e verificar o envio. Devem incluir os retornos para foto inadequada, resultado inconclusivo, GPS indisponível e falha no envio.

**Pedro:** {{objetivos, tópicos e signos que devem aparecer no MoLIC}}.

**Guilherme:** {{objetivos, tópicos e signos que devem aparecer no MoLIC}}.

Após a consolidação, a equipe deverá fixar um vocabulário e reutilizar os mesmos nomes de objetivos e signos na Entrega 10.

## Checklist

- [x] O cenário CI02 mostra alterações em relação ao cenário de problema C02.
- [ ] Cada solução individual identifica autor e cenário de origem — faltam Pedro e Guilherme.
- [x] Tópicos, falas e signos da parte de Lucas são coerentes com seus objetivos.
- [ ] Mapas individuais foram consolidados.
- [ ] O esquema de signos da equipe está completo em uma tabela única e sem duplicações.
- [ ] Nomes de objetivos e signos foram fixados pela equipe para a Entrega 10.
- [x] Os signos de Lucas representam conceitos compreensíveis ao trabalhador, e não apenas estruturas internas do código.
- [x] As telas propostas para Lucas correspondem a objetivos e signos identificados.
- [x] A interface comunica o significado e os limites do resultado técnico para a tarefa de Lucas.
