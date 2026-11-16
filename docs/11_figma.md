# Entrega 11 — Protótipo no Figma

**Data:** 15/11/2026  
**Status:** 🟩 concluído  
**Responsabilidade:** 1 protótipo integrado por equipe cobrindo os fluxos MoLIC. Se a turma exigir divisão individual, identifique o responsável por cada fluxo/tela.

## Objetivo da atividade

Materializar o modelo de interação em um protótipo navegável, preservando a lógica dos objetivos, tópicos, signos, feedbacks, alternativas e recuperações definidos anteriormente.

## Protótipo adotado

Os perfis de inspeção e de administrador não têm protótipo no Figma: a interação foi materializada diretamente no aplicativo funcional **CYF — Clean Your Farm** para iPhone, que já existia quando esta entrega foi iniciada. As telas abaixo são capturas do aplicativo em execução, e é essa versão que será usada na inspeção e nos testes das Entregas 12 a 14. O fluxo do agrônomo (M01), que o aplicativo não tem, foi prototipado no Figma (telas FA).

## Link do Figma

**Protótipo (aplicativo):** não há protótipo no Figma; o protótipo é o aplicativo funcional.  
**Arquivo editável:** código-fonte em <https://github.com/Cabral100/App_Orange_Box>, pasta `ios-native/`.  
**Última verificação de permissão:** 14/11/2026 (repositório público).

**Protótipo do fluxo do agrônomo (M01, telas FA):** <https://www.figma.com/proto/gvxtwmmYvnJVONwUOHOMVD/Orange-Box>  
**Arquivo editável (FA):** <https://www.figma.com/design/gvxtwmmYvnJVONwUOHOMVD/Orange-Box>  
**Última verificação de permissão (FA):** 15/11/2026

> Teste o link em janela anônima. O avaliador deve conseguir abrir o protótipo sem solicitar permissão.

## Cobertura MoLIC → Figma

Para M02 e M03, a tabela relaciona o MoLIC às telas do aplicativo; as telas F01 a F06 têm captura nesta entrega. Para M01, a tabela relaciona o MoLIC às telas FA do Figma.

| MoLIC | Objetivo | Fluxo/telas no aplicativo | Estados de erro/recuperação | Responsável |
|---|---|---|---|---|
| M02 — Inspecionar a rota e repassar os achados | O01–O05 | `F01 → F02 → F03`, com consulta a `F04` e `F05` | Na câmera: confiança baixa, localização desativada e falha ao salvar a imagem, com mensagem e nova tentativa. Sem captura nesta entrega. | Lucas Cabral |
| M03 — Revisar o ciclo e decidir o manejo por talhão | O06–O11 | `F01 → F06 → F04 → F03`. A aba Relatórios (F06) só aparece no perfil administrador. | Não há estados de falha específicos do gestor no aplicativo. As diferenças em relação ao M03 estão registradas na Entrega 12. | Pedro |
| M01 — Validar detecções a distância e enviar o parecer ao gestor | O12–O19 | O aplicativo não tem perfil de agrônomo; telas web no Figma (ver “Fluxo do agrônomo”): `FA01 → FA02 → FA03 → FA02V (por ponto) → FA06 → FA07 → FA01C`; desvios `FA03 → FA05 → FA03` e `FA02 → FA05 → FA02`; pedir nova foto em `FA03` volta a `FA02N`; encerrar revisão em `FA02` volta a `FA01`; acesso a `FA01` e `FA05` em qualquer tela. | `FA01V, FA02R, FA02N, FA03E, FA05V, FA06E, FA07E` | Guilherme Morais Escudeiro |

## Catálogo de telas/estados

### F01 — Acesso ao campo

![F01](../assets/11_figma/f01_acesso.jpeg)

**Objetivo do usuário:** entrar no aplicativo escolhendo como vai usá-lo: “Inspeção” (câmera, mapa e histórico) ou “Administrador” (acesso completo e relatórios).  
**Signos principais:** função escolhida, usuário e senha da conta de teste, aviso “Conta de teste pronta para entrar” e aviso de demonstração offline.  
**Origem no MoLIC:** ponto de abertura de M02 (perfil de inspeção) e de M03 (perfil administrador).

### F02 — Câmera

![F02](../assets/11_figma/f02_camera.jpeg)

**Objetivo do usuário:** enquadrar o fruto e obter uma foto analisável.  
**Signos principais:** orientação “Aponte e aproxime-se da praga”, moldura de enquadramento, barra de confiança (“Buscando 0%”), situação do modelo (“Core ML pronto”), botão de captura, galeria e flash.  
**Origem no MoLIC:** M02, cena S2 (preparar a foto) e processamento da análise; O02 e O03.

### F03 — Histórico

![F03](../assets/11_figma/f03_historico.jpeg)

**Objetivo do usuário:** conferir as inspeções já registradas, por dia e por talhão.  
**Signos principais:** período do filtro (“Últimos 14 dias”), quantidade de registros, talhão, número de ácaros detectados, data e hora, etiqueta “EXEMPLO” nos dados de demonstração e marcador de localização.  
**Origem no MoLIC:** M02, cenas S5 e S6 (confirmar o registro e conferir a rota); M03, cena S4 (avaliar o talhão pelas fotos).

### F04 — Mapa

![F04](../assets/11_figma/f04_mapa.jpeg)

**Objetivo do usuário:** ver a situação dos talhões na fazenda.  
**Signos principais:** “Total de pragas”, talhões desenhados sobre a imagem de satélite com cor por nível (verde e amarelo nesta captura), filtros, camada de satélite, ajuda e os botões “Desenhar” e “GeoJSON” para cadastrar talhões.  
**Origem no MoLIC:** M02, cena S6 (conferir a rota); M03, cena S3 (escolher o talhão).

### F05 — Conta

![F05](../assets/11_figma/f05_conta.jpeg)

**Objetivo do usuário:** conferir com qual perfil está usando o aplicativo e ver o resumo da fazenda.  
**Signos principais:** nome do usuário, “Perfil de inspeção”, resumo da fazenda (8 talhões, 8 inspeções e 64 pragas) e descrição do que o perfil permite fazer.  
**Origem no MoLIC:** apoio a M02 e M03; não corresponde a uma cena específica.

### F06 — Relatórios (perfil administrador)

![F06](../assets/11_figma/f06_relatorios.jpeg)

**Objetivo do usuário:** entender a situação da fazenda no período e decidir a próxima ação.  
**Signos principais:** filtro de talhões e período (“Todos os talhões · 30 dias”), “Detecções confirmadas” com a variação em relação ao período anterior, indicadores de talhões críticos, reentrada bloqueada e reinspeções vencidas, e o gráfico “Detecções por talhão”, seguido da lista de talhões com contagem.  
**Origem no MoLIC:** M03, cenas S1 (conhecer o ciclo), S3 (escolher o talhão) e S5 (acompanhar a evolução); O06, O07 e O09.

## Fluxo do agrônomo (M01) — telas FA

O aplicativo não tem perfil de agrônomo. O fluxo de M01 é proposto como aplicação web acessada pelo computador (ver Registro de mudanças de escopo, 22/10/2026), por dois motivos: o CTT T07 (Entrega 5) indica que foto, zoom e histórico precisam estar acessíveis na mesma tela, o que a tela de celular do protótipo em papel não permitia; e a hipótese de que P03 analisa os pedidos no escritório (Entrega 3; ainda não confirmada, pois P03 é proto-persona). O uso em celular durante visitas à propriedade continua como hipótese (Entrega 8). Para não colidir com as telas do aplicativo (F01–F06), as telas do agrônomo usam o prefixo **FA**, e os estados recebem uma letra após o número.

As telas FA foram produzidas no Figma a partir do MoLIC M01 e do protótipo em papel da Entrega 6 (A01 → FA01, A02 → FA02, A03 → FA03, A05 → FA05, A06 → FA06, A07 → FA07). Na passagem do papel (formato de celular) para o Figma (layout de computador), a navegação foi para um menu lateral fixo com “Pedidos de parecer” e “Histórico”, e FA03 passou a mostrar, junto da foto ampliável, as detecções anteriores do ponto, sem obrigar a trocar de tela para consultar o histórico. Os dados das telas são fictícios, e nenhuma funcionalidade técnica está integrada: o veredito, o pedido de nova foto, a delimitação da área e o envio do parecer são simulados por links entre quadros. A foto original é representada por uma ilustração no lugar da foto real, e as telas usam a fonte Inter. O fluxo depende das hipóteses H04, H07 e H22 e da questão Q7 do C03 (ver MoLIC M01); P03 é proto-persona.

### FA01 — Pedidos de parecer

![FA01](../assets/11_figma/fa01_pedidos.png)

**Objetivo do usuário:** escolher o foco a avaliar entre os pedidos de parecer e as detecções novas (O13).  
**Signos principais:** pedido de parecer, propriedade, talhão, solicitante, pontos pendentes, situação do pedido (pendente ou concluído).  
**Origem no MoLIC:** M01/S1, ponto de abertura e retorno de P5.

#### FA01V — Nenhum pedido

![FA01V](../assets/11_figma/fa01_nenhum.png)

Estado vazio de S1: nenhum pedido de parecer nem detecção nova nas propriedades atendidas.

#### FA01C — Parecer enviado

![FA01C](../assets/11_figma/fa01_parecer.png)

Retorno de P5: mensagem “parecer enviado ao gestor” e o pedido marcado como “concluído” na lista (O19).

### FA02 — Mapa do talhão

![FA02](../assets/11_figma/fa02_mapa.png)

**Objetivo do usuário:** ver onde estão os pontos com detecção e quantos faltam validar (O13, O14).  
**Signos principais:** talhão, ponto, situação da validação (○ pendente, ● confirmado, × rejeitado, com legenda fixa), detecção anterior, contagem por situação; ações “emitir parecer”, “ver histórico do talhão” e “encerrar revisão”.  
**Origem no MoLIC:** M01/S2.

#### FA02V — Ponto validado

![FA02V](../assets/11_figma/fa02_ponto.png)

Retorno de P1: mensagem “ponto validado por você” e o próximo ponto pendente em destaque.

#### FA02R — Retorno à revisão

![FA02R](../assets/11_figma/fa02_retorno.png)

Revisão retomada depois de encerrada ou de troca de foco: vereditos já registrados mantidos e pontos ainda pendentes em destaque.

#### FA02N — Pedido de nova foto enviado

![FA02N](../assets/11_figma/fa02_pedido.png)

Retorno de P2: mensagem “pedido de nova foto enviado ao campo; o ponto continua pendente” (O16).

### FA03 — Detecção do ponto

![FA03](../assets/11_figma/fa03_deteccao.png)

**Objetivo do usuário:** decidir se confirma, rejeita ou pede nova foto (O14).  
**Signos principais:** foto original (ampliável; no protótipo, ilustração no lugar da foto), data e hora da captura, árvore, local do achado, detecções anteriores do ponto (até 3) com “ver histórico deste ponto”, detectado pela IA, avaliação da IA (recolhida), veredito (confirmar, rejeitar ou pedir nova foto), validado por, observação técnica (até 500 caracteres, com contador).  
**Origem no MoLIC:** M01/S3.

#### FA03A — Foto ampliada e avaliação da IA aberta

![FA03A](../assets/11_figma/fa03_foto.png)

Foto ampliada com a avaliação da IA aberta: intensidade do sinal em texto (“sinal forte” ou “sinal fraco”), região do fruto indicada e o aviso “indicação automática; a validação é sua”.

#### FA03E — Falha ao registrar

![FA03E](../assets/11_figma/fa03_falha.png)

Falha em P1 ou P2: “falha ao registrar o veredito” ou “falha ao enviar o pedido de nova foto”, com o veredito e a observação técnica mantidos para tentar de novo.

### FA05 — Histórico de detecções

![FA05](../assets/11_figma/fa05_historico.png)

**Objetivo do usuário:** comparar com inspeções anteriores do ponto ou do talhão (O15).  
**Signos principais:** histórico de detecções, período (padrão: últimas 8 semanas), local do filtro (ponto, talhão ou sem filtro, conforme a origem, sempre visível e removível), “abrir detecção”. Na tela, a coluna “Local” da tabela aparece cortada; o local completo fica visível no filtro ativo.  
**Origem no MoLIC:** M01/S5 e P3.

#### FA05V — Nenhuma detecção no período

![FA05V](../assets/11_figma/fa05_nenhuma.png)

Retorno de P3 sem resultados: “nenhuma detecção no período”, com sugestão de ampliar o período e os filtros mantidos.

### FA06 — Área de aplicação

![FA06](../assets/11_figma/fa06.png)

**Objetivo do usuário:** delimitar a área com os pontos confirmados e informar produto, dose e período (O17).  
**Signos principais:** pontos confirmados (só eles aparecem como base), aviso de pontos pendentes (não bloqueia), lista dos pontos confirmados na área (marcável, alternativa ao desenho), área de aplicação (em ha, calculada pelo desenho), produto, dose, período de aplicação; “‹ Voltar” e “Voltar ao mapa do talhão” levam a FA02 para validar o restante, e “Continuar” leva a FA07.  
**Origem no MoLIC:** M01/S6 e P4.

#### FA06E — Área ou campos inválidos

![FA06E](../assets/11_figma/fa06e.png)

Retorno de P4: “nenhum ponto confirmado na área” ou “produto, dose ou período vazios”, com o que já foi preenchido mantido. Na tela, o aviso diz em texto quais campos estão vazios (produto e dose), e esses campos aparecem com borda vermelha.

### FA07 — Parecer técnico

![FA07](../assets/11_figma/fa07_parecer.png)

**Objetivo do usuário:** escrever e enviar o parecer ao gestor (O18).  
**Signos principais:** parecer técnico, área de aplicação, pontos vinculados, destinatário do parecer, aviso “o parecer não substitui o receituário agronômico”, “voltar” (para FA06, sem perder o texto) e “enviar”.  
**Origem no MoLIC:** M01/S7 e P5.

#### FA07E — Falha no envio

![FA07E](../assets/11_figma/fa07_falha.png)

Falha em P5: “falha no envio; parecer mantido para reenviar”. O pedido continua “pendente” em FA01 até o envio dar certo. Este estado foi desenhado, mas não está ligado ao caminho navegável do protótipo: “Enviar ao gestor” leva direto a FA01C (ver Entrega 12, seção “Diferenças entre o planejado e o protótipo FA”).

> FA04 (pedir nova foto) e FA08 (situação do parecer) foram retiradas, assim como A04 e A08 no protótipo em papel (Entrega 6): o pedido de nova foto é um botão em FA03, e a situação do parecer aparece em FA01.


## Sistema visual e consistência

| Elemento | Regra adotada | Justificativa |
|---|---|---|
| Tipografia | Fonte do sistema do iPhone, com títulos grandes e em peso forte e rótulos de seção pequenos, em maiúsculas. | Leitura rápida em campo, sob luz forte, e hierarquia clara entre título e conteúdo. |
| Cores | Verde escuro como cor principal, fundo claro, laranja para detecções e ações de destaque; verde, amarelo e vermelho para o nível de cada talhão. | Contraste alto sobre fundo claro e semântica de nível igual no mapa e nos relatórios. |
| Componentes | Cartões brancos com cantos arredondados, botões em formato de pílula e barra inferior com as mesmas abas em todas as telas. | Consistência: o mesmo componente se comporta do mesmo modo em qualquer tela. |
| Feedback | Barra de confiança e mensagem de orientação na câmera, aviso de conta pronta no acesso e etiqueta “EXEMPLO” nos dados de demonstração. | Manter visível o estado do sistema e separar dado de demonstração de dado real. |
| Telas FA (web) | Mesmas cores e cartões do aplicativo, em layout de computador e fonte Inter; menu lateral fixo com “Pedidos de parecer” e “Histórico”; situação da validação sempre com símbolo, texto e cor (○ pendente, ● confirmado, × rejeitado). | Acesso ubíquo de M01 a S1 e S5; mesma semântica de cor dos outros fluxos; situação legível sem depender da cor. |
| Feedback (FA) | Mensagem no topo após cada processamento (P1 a P5), em verde para sucesso e vermelho para falha, sempre com texto; em falha, os dados digitados permanecem na tela. | Cada retorno e ruptura de M01 tem feedback e recuperação, sem perder o trabalho feito. |

## Verificação de acessibilidade básica

Verificação feita apenas pelas capturas, sem teste com tecnologias assistivas.

- **Tamanho de alvo:** o botão de captura, os botões de entrada e as abas inferiores são grandes e ficam na área do polegar.
- **Contraste:** texto escuro sobre fundo claro nas telas de acesso, histórico e conta. Os rótulos sobre a imagem da câmera e do mapa usam fundo escuro ou verde próprio.
- **Informação além da cor:** no Histórico, a contagem aparece em texto. No Mapa, o nível dos talhões aparece nesta captura só pela cor da borda e do preenchimento, sem número nem rótulo visível em cada talhão. É um ponto a conferir na inspeção heurística.
- **A verificar:** leitor de tela (VoiceOver), ampliação de texto e uso sob sol forte.

**Telas FA (web, WCAG 2.2).** Verificação feita no Figma, sem teste com tecnologias assistivas.

- **Contraste (1.4.3):** textos e botões ficam entre 5,1:1 e 6,6:1 (cinza sobre fundo claro, verde, âmbar, vermelho e branco sobre verde). Exceção: o laranja das detecções (“com detecção anterior”, “Região indicada pela IA” e o rótulo da área de aplicação) tem 3,1:1 com o branco e não atinge 4,5:1. É um ponto a corrigir na próxima versão; foi mantido na versão usada no teste da Entrega 14, que é a mesma inspecionada na Entrega 13 (decisão de 15/11/2026, registrada em `RASTREABILIDADE.md`).
- **Uso da cor (1.4.1):** a situação da validação e a situação do pedido aparecem com símbolo e texto, além da cor.
- **Texto alternativo (1.1.1):** a foto traz uma legenda com data, hora e árvore (“Foto original · 14/11/2026 09:35 · Árvore L3-27”), que serve de base para o texto alternativo na implementação.
- **Teclado e foco (2.1.1, 2.4.7):** veredito, enviar e os filtros do histórico têm ordem de foco definida e foco visível. A delimitação da área sobre o mapa depende do mouse; a alternativa por teclado é marcar os pontos confirmados na lista de FA06. Os controles seguem a ordem de leitura da tela; o estado de foco visível não foi desenhado no Figma e fica para a próxima versão, pois o teste da Entrega 14 é feito com mouse.
- **Tamanho de alvo (2.5.8):** botões e pontos do mapa com pelo menos 24 × 24 px.
- **Identificação de erros (3.3.1):** FA03E, FA06E e FA07E dizem em texto o que falhou; em FA06E, o aviso nomeia os campos vazios, e eles aparecem com borda vermelha.

## Pontos observados nas capturas

- O Mapa mostra “Total de pragas: 25”, enquanto a Conta mostra “64 pragas” e a aba Relatórios mostra “64 detecções confirmadas” para a mesma fazenda. Pela leitura do código, o Mapa conta apenas as detecções posteriores à última pulverização de cada talhão. A diferença deve ser avaliada na inspeção heurística (Entrega 12, QA17).
- A foto do perfil não aparece na tela Conta (círculo vazio).
- Na aba Relatórios, as cores do gráfico “Detecções por talhão” (azul, verde, vermelho, roxo e outras) identificam talhões, e não o nível de cada um. O vermelho do gráfico pode ser lido como talhão crítico, embora o indicador mostre zero talhões críticos.

## Checklist

- [x] Link do Figma está acessível. — protótipo do agrônomo (telas FA) no Figma; telas do aplicativo no repositório público.
- [x] Há screenshots representativos no repositório.
- [x] Todos os MoLIC relevantes estão cobertos. — M02 e M03 pelas telas do aplicativo; M01 pelas telas FA01–FA07 e seus estados no Figma.
- [x] Estados de erro, feedback e recuperação foram prototipados. — no aplicativo e nas telas FA (FA02V, FA02N, FA03E, FA05V, FA06E, FA07E).
- [x] Terminologia/signos são consistentes com Entrega 9.
- [x] Componentes equivalentes se comportam de forma consistente.
- [x] Fluxos críticos são clicáveis do início ao fim. — aplicativo funcional e caminho principal das telas FA ligado no protótipo do Figma; o estado de falha no envio (FA07E) está desenhado, mas fora do caminho navegável.
- [x] O protótipo está pronto para inspeção e testes, sem “links mortos” nas tarefas avaliadas.
- [x] Dashboards, relatórios, históricos, filtros, administração e CRUDs presentes possuem justificativa rastreável.
- [x] Estados de vazio, processamento, erro e recuperação foram considerados quando pertinentes.
- [x] Resultados técnicos são apresentados de forma interpretável para o perfil de usuário.
- [x] A equipe distingue no protótipo o que é interação simulada e o que é funcionalidade técnica realmente integrada, quando necessário. — conta de teste e dados marcados como “EXEMPLO” no aplicativo; nas telas FA, dados fictícios e interações simuladas por links entre quadros.
