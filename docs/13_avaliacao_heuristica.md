# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** 16/11/2026  
**Revisão documental:** 17/11/2026  
**Situação de Lucas:** ✅ inspeção e complementação documental concluídas para o aplicativo e os estados examinados.  
**Status geral:** 🟨 em andamento — parte de Lucas concluída; HC01 e HC02 consolidados por Lucas e Pedro; cobertura integral por avaliador e consolidação dos demais registros da equipe ainda não demonstradas.  
**Responsabilidade:** uma avaliação completa por integrante, sobre todas as telas e estados relevantes do projeto.

## Objetivo da atividade

Encontrar problemas de usabilidade por inspeção sistemática da interface com as **10 heurísticas de Nielsen**.

Cada avaliador realiza a inspeção individualmente. Depois, a equipe compara os registros, consolida duplicidades e define prioridades.

Somente problemas sustentados por evidência são registrados como violações. As matrizes de cobertura apresentam também heurísticas sem violação observada.

## 1. Heurísticas adotadas

1. Visibilidade do status do sistema.
2. Compatibilidade entre o sistema e o mundo real.
3. Controle e liberdade do usuário.
4. Consistência e padrões.
5. Prevenção de erros.
6. Reconhecimento em vez de memorização.
7. Flexibilidade e eficiência de uso.
8. Estética e design minimalista.
9. Ajudar usuários a reconhecer, diagnosticar e recuperar-se de erros.
10. Ajuda e documentação.

### Cobertura especial

Quando existentes, considerar:

- estados normais, vazios, de carregamento e de erro;
- filtros combinados e sem resultados;
- relatórios e exportação;
- Histórico e listas;
- edição, exclusão e validação;
- Acesso, Conta e permissões;
- confirmação de ações com consequências;
- mensagens, termos técnicos e ajuda;
- recuperação após falhas.

A inspeção avalia a comunicação da interface, não a precisão científica do modelo.

## 2. Escopo da inspeção

| Item | Definição |
|---|---|
| Versão de referência | Aplicativo CYF para iPhone, pasta `ios-native/` de <https://github.com/Cabral100/App_Orange_Box>, commit `a36785f`, de 12/11/2026. |
| Versão de Lucas | Aplicativo disponível durante a inspeção. Lucas confirmou Acesso, Conta, filtro do Histórico e comportamento sem GPS em 14/11/2026, na mesma versão que examinou. O registro anterior citava aproximadamente 15/11/2026, às 15h; essa data era uma estimativa. O hash exato da versão adicional não foi anotado. |
| Capturas adicionais | Documentam os estados enviados posteriormente. A data de envio das imagens não é tratada como data da inspeção. |
| Telas do aplicativo | Acesso F01, Câmera F02, Histórico F03, Mapa F04, Conta F05 e Relatórios F06. |
| Estados considerados | Ajuda da câmera, confirmação de captura, detalhe da inspeção, associação ao talhão, filtros, desenho manual, ausência de localização, relatório PDF e ações sobre registros, conforme cobertura individual. |
| Protótipo do agrônomo | Telas FA01–FA03 e FA05–FA07, incluindo estados alternativos. |
| Fluxos | M02 e M03 no aplicativo; M01 no Figma, pois o aplicativo não possui perfil de agrônomo. |
| Dispositivos | Aplicativo em iPhone; protótipo FA em computador. |
| Avaliadores | A01: Lucas Tonoli Cabral Duarte; A02: Guilherme Morais Escudeiro; A03: Pedro Henrique Ferreira Valim. |
| Limitações | Capturas não comprovam todos os comportamentos dinâmicos. Alguns achados de Pedro vieram do código. A inspeção de Guilherme concentrou-se no protótipo FA. Não há comprovação de que cada avaliador tenha inspecionado individualmente todos os produtos e estados do projeto. |

## 3. Procedimento individual

1. Percorrer os fluxos para conhecer a interface.
2. Examinar telas e estados aplicando H1–H10.
3. Registrar localização, condição, problema e evidência.
4. Justificar severidade pela frequência, impacto e persistência.
5. Formular recomendação relacionada à causa.
6. Explicitar estados não reproduzidos e limites da evidência.

### Severidade

| Grau | Interpretação |
|---:|---|
| 0 | Não constitui problema de usabilidade. |
| 1 | Problema cosmético. |
| 2 | Problema menor. |
| 3 | Problema maior, de alta prioridade. |
| 4 | Catástrofe de usabilidade; correção imperativa. |

## Avaliador A01 — Lucas

**Autor:** Lucas Tonoli Cabral Duarte — 24.123.032-5.  
**Situação:** ✅ parte individual concluída para as seis telas do aplicativo e os estados descritos.

### Procedimento e cobertura

Lucas examinou:

- Acesso e seus controles disponíveis;
- Conta e suas ações disponíveis;
- câmera antes e depois da captura;
- orientação e ajuda da câmera;
- detalhe da inspeção;
- associação da foto ao talhão;
- filtros do Mapa e do Histórico;
- consulta e ações do Histórico: refazer foto, editar informações e excluir imagem;
- desenho manual de talhão;
- montagem, exportação, abertura e compartilhamento do PDF;
- mensagem apresentada quando a localização está indisponível.

A verificação complementar foi confirmada por Lucas como realizada em **14/11/2026**, na mesma versão do aplicativo.

Acesso e Conta foram examinados sem identificação de novas violações. Isso registra o resultado individual de Lucas e não invalida problemas encontrados por outros avaliadores nessas telas.

O PDF foi compartilhado com um funcionário de uma fazenda parceira, que gostou do relatório. O retorno foi informal e não substitui uma sessão sistemática com usuário.

### 4. Matriz de cobertura H1–H10

| Heurística | Telas/estados examinados | Violação? | IDs | Resultado |
|---|---|---|---|---|
| H1 — Status | Acesso, Conta, câmera, confirmação, Histórico, filtros e exportação | Não nos estados observados | — | Porcentagem e orientação visíveis; confirmação de captura; filtro informa quantidade de registros; PDF gerado e aberto. |
| H2 — Mundo real | Acesso, Conta, câmera, ajuda, detalhe e associação | Sim | A01-V01, A01-V02, A01-V04 | Termos de implementação, data em inglês e sigla EXIF sem explicação. |
| H3 — Controle | Acesso, Conta, câmera, associação, Histórico e desenho | Não nos estados observados | — | Retorno, opção “Depois”, ações sobre registros e controles “Desfazer”, “Cancelar” e “Concluir” no desenho. |
| H4 — Consistência | Acesso, Conta, filtros do Mapa/Histórico e relatório | Sim | A01-V03 | Filtros usam cores em vez de nomenclatura única para as situações. |
| H5 — Prevenção | Acesso, Conta, câmera e desenho | Não nos estados observados | — | Captura bloqueada abaixo de 85%; desenho orienta usar pelo menos três pontos. |
| H6 — Reconhecimento | Acesso, Conta, Mapa e Histórico | Não nos estados observados | — | Busca por nome, lista de talhões, períodos visíveis e registros disponíveis para consulta. |
| H7 — Eficiência | Acesso, Conta, câmera, filtros, Histórico e PDF | Não nos estados observados | — | Galeria, ações sobre registros, filtros por período/talhão e exportação. |
| H8 — Minimalismo | Acesso, Conta, câmera, filtros, Histórico e relatório | Não nos estados observados | — | Lucas não identificou excesso impeditivo; câmera mantém área central para enquadramento. |
| H9 — Recuperação | Acesso, Conta, orientação da câmera e ausência de GPS | Não nos estados observados | — | A câmera orienta ajuste da distância; sem localização, mensagem explica a necessidade de ativá-la. |
| H10 — Ajuda | Acesso, Conta, ajuda da câmera e desenho | Não nos estados observados | — | Ajuda explica captura e limiar; desenho informa como marcar os vértices. |

**Limite da matriz:** “nenhuma violação observada” se refere aos estados examinados e não comprova ausência de todas as falhas possíveis.

### 5. Declaração de violações ativas

| ID | H | Tela/estado | Problema | Evidência | Severidade | Justificativa | Recomendação |
|---|---|---|---|---|---:|---|---|
| A01-V01 | H2 | Câmera | “UltralyticsYOLO · Core ML pronto” comunica a implementação, sem traduzir o significado para a tarefa. | Figura 1 | 2 | Aparece na captura frequente; não impede a ação, mas pode ser incompreensível ao trabalhador. | Usar “Pronto para analisar” ou mensagem equivalente. |
| A01-V02 | H2 | Detalhe da inspeção | Data em inglês em interface portuguesa. | Figura 3 | 1 | Mudança de idioma dificulta leitura do registro. | Usar data e hora no padrão local. |
| A01-V03 | H4 | Filtros do Mapa e Histórico | “Verde”, “Amarelo” e “Vermelho” nomeiam situações, enquanto outras telas usam nomes de níveis. | Figuras 4 e 10 | 2 | Exige relacionar cores e significados e conciliar rótulos diferentes. | Adotar nomenclatura única e manter cores como apoio. |
| A01-V04 | H2 | Associação da foto à área | Mensagem usa “coordenadas GPS/EXIF” sem explicar EXIF ou a ação necessária. | Figura 6 | 2 | Termo técnico aparece durante associação do registro ao local. | Explicar que a localização da foto posicionou o mapa e orientar seleção da área. |

### Revisão de A01-V05

**Situação:** reclassificado; não contabilizado como violação ativa.

O registro anterior afirmava ausência de orientação ou recuperação sem GPS. A nova evidência mostra a mensagem:

> “Localização necessária. Ative a localização precisa para salvar a inspeção no ponto correto do mapa.”

Portanto, a alegação de ausência de orientação não se sustenta. A mensagem identifica a condição e informa uma ação de recuperação.

A captura do desenho manual comprova que é possível desenhar um talhão. Ela **não comprova que seja possível salvar uma inspeção sem GPS**.

A01-V05 é preservado neste histórico para documentar a revisão, sem renumerar os demais achados.

### Evidências fotográficas

#### Figura 1 — Câmera com detecção

Estado anterior à captura, com 57% e orientação de distância. Não representa inspeção salva abaixo de 85%.

![Câmera com detecção e mensagem técnica](../assets/13_heuristica/Camera_com_deteccao.jpeg)

#### Figura 2 — Confirmação de captura

Feedback de captura permitida e armazenamento no aparelho.

![Confirmação de captura](../assets/13_heuristica/Imagem_capturada.jpeg)

#### Figura 3 — Detalhe da inspeção

A data em inglês fundamenta A01-V02.

![Detalhe da inspeção](../assets/13_heuristica/Inspecao_Detalhes.jpeg)

#### Figura 4 — Filtros do Mapa

O campo “Situação” apresenta “Todas”, “Verde”, “Amarelo” e “Vermelho”.

![Filtros do Mapa](../assets/13_heuristica/Filtros_Mapa.jpeg)

#### Figura 5 — Configuração do relatório

Lucas gerou, abriu e compartilhou o PDF. A imagem documenta a configuração, não o conteúdo integral do arquivo exportado.

![Configuração do relatório](../assets/13_heuristica/Filtros_Realatorio.jpeg)

#### Figura 6 — Associação da foto à área

A mensagem apresenta a sigla EXIF sem explicação.

![Associação da foto à área](../assets/13_heuristica/mapa_selecionando.jpeg)

#### Figura 7 — Resultado e alteração do talhão

Controles permitem alterar a associação ou marcar o talhão no mapa.

![Resultado e alteração do talhão](../assets/13_heuristica/Resultado_e_alteracao_ft.jpeg)

#### Figura 8 — Localização desligada

A câmera informa que a localização precisa deve ser ativada para salvar a inspeção no ponto correto do mapa.

A imagem sustenta a revisão de A01-V05 e o registro de orientação de recuperação em H9. Não demonstra o comportamento de uma falha da imagem com GPS funcionando.

![Mensagem de localização necessária](../assets/13_heuristica/localizacao_desligada.jpeg)

#### Figura 9 — Desenho manual de talhão

O aplicativo apresenta vértices, quantidade de pontos e controles “Desfazer”, “Cancelar” e “Concluir”. A instrução solicita pelo menos três pontos.

Esta evidência comprova o desenho manual do talhão, não o salvamento de inspeção sem localização.

![Desenho manual do talhão](../assets/13_heuristica/desenho_talhao.jpeg)

#### Figura 10 — Filtro do Histórico

A tela “Refinar registros” apresenta:

- períodos Hoje, 7 dias, 14 dias e 30 dias;
- busca e seleção de talhão;
- situação Todas, Verde, Amarelo e Vermelho;
- ação “Limpar filtros”;
- quantidade de registros no controle “Ver 13”.

A imagem confirma o escopo de A01-V03 e HC02 no Histórico.

![Filtros do Histórico](../assets/13_heuristica/filtro_hist.png)

### Captura e estados de recuperação

Não foi possível salvar captura abaixo de 85%, pois o aplicativo bloqueia essa ação e informa o limiar.

As orientações de aproximação e afastamento ajudam a ajustar a captura. Lucas não reproduziu falha depois de seguir essas orientações.

Nos exemplos examinados, Lucas não identificou indicação maior ou igual a 85% que reconhecesse como algo diferente de ácaro. Isso não demonstra ausência de falsos positivos nem valida a precisão do detector.

Sem localização, a mensagem informa que é necessário ativar a localização precisa. O desenho manual do talhão é uma função separada e não elimina essa exigência para salvar a inspeção.

### 6. Boas práticas

| H | Exemplo | Evidência | Justificativa |
|---|---|---|---|
| H1 | Confirmação de captura e armazenamento. | Figura 2 | Comunica conclusão da ação. |
| H3 | Refazer foto, editar informações e excluir imagem; desfazer/cancelar desenho. | Inspeção relatada e Figura 9 | Permite rever registros e corrigir desenho. |
| H5 | Bloqueio abaixo de 85%; desenho exige pelo menos três pontos. | Figura 1, ajuda examinada e Figura 9 | Previne ações fora dos requisitos definidos. |
| H6 | Busca, períodos e lista de talhões. | Figuras 4 e 10 | Permite reconhecer opções sem memorizar códigos. |
| H7 | Galeria, filtros e configuração/exportação de PDF. | Figuras 1, 5 e 10 | Oferece alternativas de entrada, consulta e compartilhamento. |
| H8 | Área central dedicada ao enquadramento. | Figura 1 | Mantém foco na captura. |
| H9 | Mensagem solicita ativar localização precisa. | Figura 8 | Explica a condição e uma ação para prosseguir. |
| H10 | Ajuda explica uso e limiar; desenho orienta marcação. | Inspeção da ajuda e Figura 9 | Orientação contextual para a tarefa. |

### Síntese individual — Lucas

- **Parte individual concluída para o aplicativo e os estados descritos.**
- Quatro violações ativas: três de severidade 2 e uma de severidade 1.
- Três violações de H2 e uma de H4.
- A01-V05 reclassificado após evidência da orientação para ativar localização.
- Acesso e Conta examinados sem novas violações observadas por Lucas.
- Filtro do Histórico confirmado por relato e captura.
- HC01 e HC02 aprovados por Lucas e Pedro com severidade 2.
- PDF gerado e examinado; retorno do funcionário mantido como informal.
- Commit da versão adicional não anotado.
- Não há inspeção individual de Lucas das telas FA registrada neste documento.

## Avaliador A02 — Guilherme

**Autor:** Guilherme Morais Escudeiro — 24.123.005-1.

### Procedimento

Inspeção das telas FA01, FA01V, FA01C, FA02, FA02V, FA02R, FA02N, FA03, FA03A, FA03E, FA05, FA05V, FA06, FA06E, FA07 e FA07E.

O fluxo principal foi percorrido, incluindo Histórico, estados vazios e falhas. Depois, cada tela foi examinada com H1–H10.

Os dados e interações são simulados. Os pontos QA21 da Entrega 12 foram considerados. Os IDs V01–V13 desta seção pertencem a A02.

### 4. Matriz de cobertura

| H | Telas/estados | Violação? | IDs |
|---|---|---|---|
| H1 | FA01, FA01C, FA02, FA02V, FA02N | Sim | V01 |
| H2 | FA01, FA03, FA06, FA07 | Não | — |
| H3 | FA01C, FA02V, FA02R, FA03E, FA06, FA07E | Sim | V02, V03, V13 |
| H4 | FA02, FA02N, FA03, FA03E, FA05, FA06, FA07 | Sim | V04–V07 |
| H5 | FA02, FA06, FA07 | Sim | V08 |
| H6 | FA02, FA03, FA05, FA06 | Sim | V09 |
| H7 | FA02, FA03, FA05, FA06 | Sim | V10 |
| H8 | Todas as telas FA | Não | — |
| H9 | FA03E, FA05V, FA06E, FA07E | Sim | V11 |
| H10 | Todas as telas FA | Sim | V12 |

### 5. Declaração de violações

| ID | H | Tela/estado | Problema | Evidência | Severidade | Justificativa | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H1 | FA01C | Pedido aparece concluído com ponto aguardando nova foto, sem ação para reabrir. | ![V01](../assets/13_heuristica/a02_v01.png) | 3 | Ponto pode permanecer sem avaliação após envio do parecer. | Separar situação do parecer e do pedido; manter acesso e aviso da nova foto. |
| V02 | H3 | FA01C | Parecer enviado não pode ser aberto, revisto ou complementado. | ![V02](../assets/13_heuristica/a02_v02.png) | 2 | Correções precisam ocorrer fora do sistema. | Permitir consulta e envio de correção ou complemento. |
| V03 | H3 | FA06 | Desenho sem desfazer vértice, mover ponto ou limpar área. | ![V03](../assets/13_heuristica/a02_v03.png) | 2 | Clique errado dificulta corrigir área calculada. | Incluir desfazer, limpar e ajuste de vértices. |
| V04 | H4 | FA03/FA03E | “Confirmar” recebe destaque antes da seleção; estilo selecionado fica mais claro. | ![V04](../assets/13_heuristica/a02_v04.png) | 2 | Pode confundir seleção e influenciar confirmação. | Mesmo peso inicial e estilo único de seleção. |
| V05 | H4 | FA03/FA05 | Avaliação da IA recolhida no ponto atual, mas aberta no Histórico. | ![V05](../assets/13_heuristica/a02_v05.png) | 2 | Regra de apresentação inconsistente. | Adotar regra única conforme estado da validação. |
| V06 | H4 | FA02N | Nova foto pedida usa símbolo de pendência e não aparece separada no contador. | ![V06](../assets/13_heuristica/a02_v06.png) | 2 | Usuário pode tentar avaliar ponto sem foto disponível. | Símbolo, legenda e contador próprios. |
| V07 | H4 | FA06 | Dois retornos ao mesmo local usam rótulos diferentes. | ![V07](../assets/13_heuristica/a02_v07.png) | 1 | Destino do retorno pode ser interpretado incorretamente. | Padronizar rótulo ou manter um controle. |
| V08 | H5 | FA02 | “Emitir parecer” ativo sem ponto confirmado, levando ao erro posterior. | ![V08](../assets/13_heuristica/a02_v08.png) | 2 | Destaca caminho ainda inviável. | Desativar e explicar necessidade de confirmar um ponto. |
| V09 | H6 | FA05 | Coluna de local cortada. | ![V09](../assets/13_heuristica/a02_v09.png) | 2 | Sem filtro, registros não se distinguem adequadamente. | Ampliar coluna ou quebrar texto em linhas. |
| V10 | H7 | FA03 | Sequência “Ponto 3 de 5” sem próximo/anterior. | ![V10](../assets/13_heuristica/a02_v10.png) | 2 | Requer voltar ao mapa a cada ponto. | Oferecer próximo pendente e anterior. |
| V11 | H9 | FA03E/FA07E | Falhas pedem nova tentativa, sem causa ou alternativa persistente. | ![V11](../assets/13_heuristica/a02_v11.png) | 2 | Repetir ação pode não resolver. | Explicar causa e recuperação, preservando dados. |
| V12 | H10 | FA03A/FA03/FA05 | “Sinal forte/fraco” sem explicação. | ![V12](../assets/13_heuristica/a02_v12.png) | 2 | Pode atribuir peso indevido ao modelo. | Explicar termos e responsabilidade da validação humana. |
| V13 | H3 | FA02V/FA02 | Veredito não pode ser desfeito ou alterado. | ![V13](../assets/13_heuristica/a02_v13.png) | 3 | Erro de confirmação ou rejeição altera área e não tem correção. | Desfazer e reabrir ponto até envio, com autoria registrada. |

### 6. Boas práticas

| H | Exemplo | Evidência | Justificativa |
|---|---|---|---|
| H2 | Identificação de árvore, dose e aviso sobre receituário em linguagem do domínio. | ![FA03](../assets/11_figma/fa03_deteccao.png) ![FA07](../assets/11_figma/fa07_parecer.png) | Relaciona informações à atividade do agrônomo. |
| H8 | Pedidos mostram informações necessárias à escolha, com uma ação por linha. | ![FA01](../assets/11_figma/fa01_pedidos.png) | Detalhes ficam para etapas posteriores. |

### Síntese individual — Guilherme

- Treze problemas: dois de severidade 3, dez de severidade 2 e um de severidade 1.
- H4: quatro; H3: três; H1, H5, H6, H7, H9 e H10: um cada.
- H2 e H8 sem violação observada.
- Prioridades: V01, V13, V04 e V05.
- Estados intermediários e avaliação automática não seguem a mesma regra em todo o fluxo.
- QA21: aviso de pendentes aparece em FA06/FA07; situação do parecer gerou V01/V02; avaliação recolhida gerou V05; foco por teclado não conferido nas capturas.
- Inspeção baseada nas telas FA, com conferência no Figma da impossibilidade de reabrir ponto validado.
- O desenho manual mostrado na Figura 9 pertence ao aplicativo e não elimina V03 do protótipo FA.

## Avaliador A03 — Pedro

**Autor:** Pedro Henrique Ferreira Valim — 24.123.048-1.

### Procedimento

Inspeção das seis capturas da Entrega 11 e leitura do código, aplicando H1–H10.

Os registros `[código]` têm evidência de implementação, não necessariamente confirmação de comportamento no aparelho.

V09 foi confirmado visualmente no Mapa e no Histórico pelas capturas de Lucas. V12 tem confirmação parcial. V03, V10, V11 e V14 permanecem sem confirmação no iPhone.

O documento de origem registra V03 como observado na versão web no teste com usuário, com referência a AU04 da Entrega 14. Essa relação deve ser conferida na consolidação final da Entrega 14.

### 4. Matriz de cobertura

| H | Telas/fluxos | Violação? | IDs |
|---|---|---|---|
| H1 | Relatórios, detalhe do talhão, câmera | Sim | V03, V04, V11 |
| H2 | Acesso, câmera, relatórios, Mapa | Sim | V05, V06, V07, V16 |
| H3 | Câmera, desenho, exclusões | Sim | V13 |
| H4 | Mapa, Conta, relatórios, filtros | Sim | V01, V08, V09 |
| H5 | Talhão, exclusões, Acesso | Sim | V10 |
| H6 | Mapa, Histórico, relatórios | Sim | V02 |
| H7 | Câmera, associação e filtros | Sim | V12 |
| H8 | Todas as capturas | Não | — |
| H9 | Câmera, Acesso, Mapa | Sim | V14 |
| H10 | Câmera, Mapa, relatórios | Sim | V15 |

### 5. Declaração de violações

| ID | H | Tela/estado | Problema | Evidência | Severidade | Justificativa | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H4 | Mapa, Conta e Relatórios | Contagens diferentes sem explicar que Mapa considera detecções posteriores à última pulverização. | ![V01](../assets/13_heuristica/v01.jpeg) | 3 | Gestor recebe números distintos sem conhecer a regra. | Unificar contagem ou explicitar período e critério. |
| V02 | H6 | Mapa | Polígonos sem nome/contagem visíveis no zoom capturado; acesso depende do rótulo. | ![V02](../assets/13_heuristica/v02.jpeg) | 3 | Exige memória e pode impedir abertura do talhão. | Exibir identificação e permitir tocar no polígono; conferir outros níveis de zoom. |
| V03 | H1 | Relatórios [código] | Talhão não inspecionado recebe indicação semelhante a inspecionado sem ocorrência; lista inicial limitada. | `DashboardView.swift`; referência a AU04 da Entrega 14 na versão web. | 3 | Ausência de dado pode ser entendida como ausência de praga. | Distinguir “Não inspecionado no período” de “Sem ocorrência”. |
| V04 | H1 | Relatórios | Variação positiva exibida sem dados no período anterior. | ![V04](../assets/13_heuristica/v04.jpeg) | 2 | Pode sugerir crescimento sem base comparativa. | Mostrar “Sem dados no período anterior”. |
| V05 | H2 | Relatórios e ajuda | “Detecções confirmadas” nomeia saída do modelo com confiança alta. | ![V05](../assets/13_heuristica/v05.jpeg) | 3 | Pode ser confundida com confirmação profissional. | Identificar resultado do modelo e separar validação humana. |
| V06 | H2 | Acesso | “Continuar com Google” entra em conta de teste pelo código, sem autenticação Google real. | ![V06](../assets/13_heuristica/v06.jpeg) | 2 | Promete comportamento diferente do implementado. | Rotular como demonstração ou implementar autenticação real. |
| V07 | H2 | Câmera | “UltralyticsYOLO · Core ML pronto” usa termos de implementação. | ![V07](../assets/13_heuristica/v07.jpeg) | 2 | Usuário pode não compreender se deve agir. | Usar “Pronto para analisar”. |
| V08 | H4 | Gráfico do relatório | Cores identificam talhões, mas também significam severidade em outras telas; gráfico sem legenda. | ![V08](../assets/13_heuristica/v08.jpeg) | 2 | Vermelho pode ser interpretado como crítico. | Usar paleta adequada e legenda. |
| V09 | H4 | Filtros do Mapa e Histórico | Cores no filtro diferem dos nomes usados nos relatórios e na legenda do Mapa. | ![Mapa](../assets/13_heuristica/Filtros_Mapa.jpeg) ![Histórico](../assets/13_heuristica/filtro_hist.png) | 2 | Exige traduzir cores para situações. | Padronizar rótulos, mantendo cor como apoio. |
| V10 | H5 | Registrar pulverização [código] | Um toque registra aplicação, muda contagem e datas sem confirmação ou desfazer. | `MapView.swift`; não confirmado no aparelho. | 3 | Toque acidental pode alterar indicação de manejo. | Confirmar talhão/data, permitir data real e desfazer. |
| V11 | H1 | Salvar nome/leitura/pulverização [código] | Gravações sem mensagem de confirmação. | `MapView.swift`; não confirmado no aparelho. | 2 | Usuário pode repetir ação sem saber se salvou. | Feedback curto após gravação. |
| V12 | H7 | Após foto [código] | Saída da câmera para associação de área pode interromper capturas sucessivas. | ![Área](../assets/13_heuristica/mapa_selecionando.jpeg) Pergunta confirmada fora de talhão; caso dentro de talhão não confirmado. | 3 | Pode adicionar passos repetidos à inspeção. | Associar quando possível e perguntar apenas quando necessário; confirmar comportamento no aparelho. |
| V13 | H3 | Câmera | Retorno leva ao Histórico, independentemente da origem, segundo código. | ![V13](../assets/13_heuristica/v13.jpeg) | 1 | Impõe navegação adicional, sem perda de dados. | Voltar à origem ou manter navegação disponível. |
| V14 | H9 | Falha de captura [código] | Mensagem de localização também usada quando falha a captura da imagem. | `CameraView.swift`; falha da imagem não reproduzida no aparelho. | 2 | Recuperação sugerida pode não corresponder à causa. | Separar verificações e mensagens. |
| V15 | H10 | Relatórios | Sem ajuda para indicadores e limites. | ![V15](../assets/13_heuristica/v15.jpeg) | 2 | Indicadores podem não ser compreendidos. | Ajuda contextual com definições e limites. |
| V16 | H2 | Mapa demonstrativo | Talhões de exemplo sobre área urbana. | ![V16](../assets/13_heuristica/v02.jpeg) | 1 | Prejudica coerência da demonstração e dos testes. | Reposicionar exemplos em área agrícola. |

### Observações sobre as novas evidências

A Figura 9 mostra nomes e contagens no zoom apresentado. Isso delimita V02: a ausência de rótulos não pode ser generalizada para todos os níveis de zoom.

A Figura 8 confirma a mensagem quando falta localização. Não confirma que a mesma mensagem apareça em uma falha da imagem com localização disponível; por isso V14 permanece identificado como achado de código.

A ausência de violação identificada por Lucas em Acesso e Conta não apaga automaticamente V06 ou V01 de Pedro. São resultados individuais, com métodos e evidências diferentes.

### 6. Boas práticas

| H | Exemplo | Evidência | Justificativa |
|---|---|---|---|
| H8 | Câmera concentra enquadramento, orientação, confiança e controles; indicadores ficam no relatório. | ![Câmera](../assets/11_figma/f02_camera.jpeg) | Mantém informações relacionadas à tarefa atual. |

### Síntese individual — Pedro

- Dezesseis problemas: seis de severidade 3, oito de severidade 2 e dois de severidade 1.
- H2: quatro; H1 e H4: três cada; H3, H5, H6, H7, H9 e H10: um cada.
- Prioridades: V01, V03, V05, V10, V02 e V12.
- Padrões principais: ausência de dados confundida com zero e saída automática apresentada como confirmação.
- V09 confirmado por capturas do Mapa e Histórico.
- V12 parcialmente confirmado.
- V03, V10, V11 e V14 permanecem sem confirmação no aparelho.
- A referência de V03 ao teste web deve permanecer coerente com a Entrega 14 final.

## 7. Consolidação da equipe

### 7.1 Achados consolidados por Lucas e Pedro

Lucas confirmou que ele e Pedro concordaram com a unificação dos dois pares, mantendo severidade 2 para ambos.

Os registros individuais são preservados para rastrear autoria e evidências.

| ID | Registros individuais | H | Problema consolidado | Escopo | Severidade final do par | Decisão | Responsáveis |
|---|---|---|---|---|---:|---|---|
| HC01 | A01-V01 + V07/A03 | H2 | Câmera comunica prontidão com nomes técnicos da implementação. | Câmera do aplicativo. | 2 | Usar mensagens relacionadas à tarefa, como “Pronto para analisar”. | Lucas e Pedro. |
| HC02 | A01-V03 + V09/A03 | H4 | Filtros nomeiam situações pelas cores, divergindo dos demais rótulos do aplicativo. | Mapa e Histórico, ambos documentados. | 2 | Padronizar os nomes em filtros, Mapa e relatórios, mantendo cores como apoio. | Lucas e Pedro. |

**Situação:** HC01 e HC02 consolidados e aprovados pelos dois avaliadores envolvidos.

### 7.2 Registro reclassificado

| Registro | Situação anterior | Evidência adicional | Decisão |
|---|---|---|---|
| A01-V05 | Ausência de orientação de recuperação sem GPS. | Figura 8 informa necessidade de ativar localização precisa. | Retirar da lista de violações ativas; manter histórico da revisão e registrar boa prática de H9. |

O desenho manual mostrado na Figura 9 é registrado separadamente. Não é apresentado como prova de salvamento da inspeção sem GPS.

### 7.3 Demais registros

Os demais achados permanecem com seus IDs individuais até a revisão final da equipe.

Problemas em produtos diferentes não são automaticamente duplicidades. O aplicativo e as telas FA podem exigir soluções diferentes.

### 7.4 Contagem atualizada

- Lucas: 4 violações ativas.
- Guilherme: 13 violações.
- Pedro: 16 violações.
- Total bruto ativo: 33 registros.
- Dois pares consolidados: HC01 e HC02.
- Total após unificar somente esses pares: 31 registros.
- A01-V05 permanece apenas no histórico, fora da contagem ativa.

A classificação dos 31 registros como total final da equipe depende de revisar os demais casos e delimitar os achados baseados somente no código.

## 8. Síntese e plano de melhoria

### Prioridades

| Prioridade | Problemas | Ação | Responsável pelo acompanhamento |
|---|---|---|---|
| Alta | A03-V01, V03 e V05 | Esclarecer contagens, ausência de dados e resultado automático. | Pedro/equipe. |
| Alta | A03-V10 | Verificar e prevenir registro acidental de pulverização. | Pedro/equipe. |
| Alta | A02-V01 e V13 | Manter acesso a pendências e permitir corrigir veredito. | Guilherme/equipe. |
| Alta | A03-V02 e V12 | Conferir identificação por zoom e interrupções nas capturas. | Pedro/equipe. |
| Média | HC01 | Traduzir mensagem técnica da câmera. | Lucas e Pedro. |
| Média | HC02 | Padronizar nomes nos filtros, Mapa e relatórios. | Lucas e Pedro. |
| Média | A01-V04 | Explicar associação da foto sem a sigla EXIF. | Lucas/equipe. |
| Menor | A01-V02 | Localizar data e hora para português. | Lucas/equipe. |

A severidade não indica que a correção já foi implementada.

## Checklist — equipe

- [ ] Cada integrante realizou inspeção completa de todo o escopo exigido.
- [ ] Todas as telas e estados relevantes possuem cobertura individual demonstrada.
- [ ] Cobertura integral de estados dinâmicos e de falha confirmada.
- [x] A inspeção avalia a interface, não o mérito científico do algoritmo.
- [x] H1–H10 aparecem nas matrizes individuais.
- [x] Não foi criada uma violação obrigatória para cada heurística.
- [x] Registros possuem localização, contexto e evidência visual ou de código, com limitações explícitas.
- [ ] Todos os comportamentos registrados no código foram confirmados no aparelho.
- [x] Severidades individuais possuem justificativas.
- [x] Recomendações indicam correção ou redução do impacto.
- [x] HC01 e HC02 consolidados e aprovados por Lucas e Pedro.
- [ ] Revisão dos demais registros e consolidação final da equipe concluídas.
