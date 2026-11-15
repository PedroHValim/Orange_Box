# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 02/09/2026  
**Status:** 🟩 concluído  
**Responsabilidade:** uma análise de interface por integrante e síntese comparativa da equipe.

## Objetivo da atividade

Investigar interfaces do domínio agrícola e padrões que possam apoiar tarefas reais do projeto, sem transformar características dos concorrentes automaticamente em requisitos.

## Entrada da Entrega 1 e público-alvo

O projeto considera dois fluxos cuja divisão entre pessoas ainda precisa ser confirmada:

- **Fluxo A — inspeção e captura:** trabalhador de campo/pragueiro registra imagens e interpreta a indicação da detecção.
- **Fluxo B — acompanhamento e decisão:** responsável pelo manejo consulta ocorrências, localização e evolução dos dados.

A hipótese **H26** investiga se os dois fluxos são realizados pela mesma pessoa ou por papéis distintos. FieldView e OneSoil são referências de representação espacial e consulta; Plantix é referência de captura e diagnóstico por imagem.

## 1. Interfaces analisadas

| ID | Interface | Tipo | Autor | Relação com o projeto |
|---|---|---|---|---|
| C01 | Climate FieldView | Análoga | Pedro Henrique Ferreira Valim | Mapas, filtros, indicadores e consulta de dados agrícolas. |
| C02 | Plantix | Direta/análoga | Guilherme Morais Escudeiro | Captura de foto e apresentação de diagnóstico automático. |
| C03 | OneSoil | Análoga | Lucas Tonoli Cabral Duarte — 24.123.032-5 | Mapa, pontos, notas e recuperação de registros por área. |

### C01 — Climate FieldView

**Autor:** Pedro Henrique Ferreira Valim  
**Fonte:** https://climate.com/pt-br.html

As capturas `Mapa_Marcacao.webp`, `visao_campo_driver_fieldview.webp` e `relatorio.webp` mostram mapas, pins, filtros, legendas e indicadores relacionados ao espaço agrícola. `drive_fieldview.jfif` apresenta principalmente o hardware e tem menor valor como evidência de interação.

A interface organiza um volume elevado de informações, mas a quantidade de controles e filtros também pode dificultar a leitura. A implicação para o projeto é investigar quais informações o responsável pelo manejo precisa consultar, sem copiar um painel completo por aparência.

### C02 — Plantix

**Autor:** Guilherme Morais Escudeiro  
**Fonte:** https://plantix.net/pt/

As telas de uso mostram uma câmera com orientação de enquadramento, mensagens de processamento e um resultado identificado como detecção automática. Há uma ação de confirmação antes de consultar o tratamento e um controle “Ouvir”.

A moldura e a mensagem mudam conforme o conteúdo enquadrado. Isso demonstra **feedback visual antes da captura**, mas as imagens não comprovam que o Plantix meça foco, distância ou iluminação. A necessidade de foco e distância adequados no nosso projeto vem do protocolo técnico de captura do TCC. A existência do botão “Ouvir” também não comprova que o nosso público precise de áudio; essa necessidade deve ser investigada.

### C03 — OneSoil

**Autor:** Lucas Tonoli Cabral Duarte — 24.123.032-5  
**Tipo:** interface agrícola análoga  
**Fonte:** https://onesoil.ai/pt/solutions/farmers  
**Data de acesso registrada:** 02/09/2026

A OneSoil utiliza mapas e dados espaciais para apoiar atividades agrícolas. A análise de Lucas observa **o que aparece nas imagens**, separando essa evidência de benefícios que ainda precisariam ser testados com pessoas.

| Evidência | O que aparece | Padrão de IHC | Relação com o projeto |
|---|---|---|---|
| `Mapa_OneSoil.jfif` | Delimitação de área e regiões diferenciadas visualmente. | Organização espacial por regiões. | Investigar se a divisão ajuda a pessoa a reconhecer o talhão pertinente. |
| `Mapeamento_OneSoil.jfif` | Mapa com variações espaciais usadas em outra tarefa agrícola. | Uso de cores e áreas para representar dados. | Não interpretar o mapa de produtividade como mapa de risco de ácaros. |
| `Interface_OneSoil.png` | Mapa, pins de notas, navegação inferior, busca, filtros, lista de notas e detalhe. | Relação entre registro, localização e recuperação posterior. | Investigar se o inspetor consegue reencontrar uma vistoria e reconhecer onde foi feita. |

**Aprendizado:** mapa e lista oferecem duas formas de localizar um registro. Pins e detalhes preservam a relação entre a nota e a área. Isso é uma referência concreta para estudar como um achado de campo poderia ser recuperado.

**Limite da evidência:** uma captura estática não comprova rapidez, facilidade de uso, legibilidade sob sol, GPS em tempo real nem funcionamento offline. Depoimentos promocionais da plataforma não substituem observação dos usuários do projeto.

**Decisão para o projeto:** considerar a associação entre ocorrência e local como alternativa de design, condicionada à confirmação de que o usuário precisa registrar e recuperar ocorrências por área. A interface de inspeção não precisa receber mapas de produtividade ou controles de taxa variável só porque eles existem na OneSoil.

## 2. Interfaces familiares como referências potenciais

| Interface | Padrão observado | Limite |
|---|---|---|
| WhatsApp | Foto, áudio e estado de envio de mensagens. | O uso específico desses recursos pelo inspetor ainda é hipótese. |
| Google Maps/Waze | Mapa, pin, localização e navegação. | Não comprova que o público usa mapas dentro dos talhões. |
| Aplicativo de previsão do tempo | Ícones e informação resumida. | Não justifica criar alertas sem tarefa correspondente. |

## 3. Síntese comparativa

| Critério | FieldView | Plantix | OneSoil | Encaminhamento |
|---|---|---|---|---|
| Tarefa central | Consulta de dados agrícolas. | Captura e indicação automática. | Consulta espacial e notas. | Definir a interface a partir das tarefas de captura e de decisão. |
| Organização | Mapas, camadas, filtros e indicadores. | Câmera, feedback e resultado. | Mapa, pins, lista, busca e detalhe. | Priorizar o fluxo curto de captura; investigar se histórico e mapa são necessários. |
| Risco | Densidade visual elevada. | Resultado automático confundido com confirmação humana. | Representação espacial copiada para uma tarefa diferente. | Testar compreensão e evitar informação sem significado para a decisão. |

## 4. Recomendações derivadas

| ID | Recomendação e origem | Status |
|---|---|---|
| RC01 | Investigar orientação de captura. Plantix mostra feedback antes da foto; exigências de foco e distância vêm do TCC. | Candidata a validar. |
| RC02 | Testar contraste, tamanho dos controles e leitura sob luz de campo. | Candidata a validar. |
| RC03 | Investigar se leitura em áudio ajuda o inspetor; o Plantix mostra a ação “Ouvir”. | Hipótese, não requisito. |
| RC04 | Manter a inferência offline prevista no TCC; investigar separadamente eventual sincronização posterior. | Offline: decisão técnica existente. Sincronização: hipótese. |
| RC05 | Considerar pontos, regiões, cores e camadas quando a tarefa e os dados justificarem. | Candidata a validar. |
| RC06 | Evitar excesso de informação em mapas e filtros. | Diretriz para verificar nos protótipos. |
| RC07 | Informar a finalidade da coleta e do compartilhamento da localização. | Diretriz de transparência. |

Os vínculos de RC01–RC07 com as hipóteses, personas e tarefas constam em `../RASTREABILIDADE.md`.

## Checklist

- [x] Uma interface principal foi analisada por integrante.
- [x] Prints foram relacionados a observações específicas de IHC.
- [x] Tela de uso, material promocional e evidência contextual foram distinguidos.
- [x] A análise de OneSoil identifica o que é visível e o que ainda é inferência.
- [x] A síntese compara as interfaces por critérios comuns.
- [x] Recomendações distinguem observação, decisão técnica e hipótese.
- [x] Os aprendizados foram vinculados à rastreabilidade.
