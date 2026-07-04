# Data Analysis Project: Bike Buyers Dashboard

Este repositório contém um projeto completo de análise de dados desenvolvido no Microsoft Excel. O objetivo principal é analisar o perfil demográfico e socioeconômico dos clientes para identificar os principais fatores que influenciam a compra de bicicletas.

## Estrutura do Projeto e Compreensão de cada Aba

O arquivo está estruturado em quatro abas principais, representando o ciclo completo de um projeto de análise de dados: **Dados Brutos (Raw Data) ➔ Limpeza de Dados (Data Cleaning) ➔ Agregação (Pivot Tables) ➔ Visualização (Dashboard)**.

### 1. "bike_buyers" (Dados Brutos)
Esta aba contém o conjunto de dados original sem nenhuma modificação. É o ponto de partida do projeto.
* Contém abreviações e valores brutos que dificultam a leitura imediata e a plotagem de gráficos claros (ex: "M" e "S" para estado civil; "M" e "F" para gênero).
* Contém os campos principais como `ID`, `Marital Status`, `Gender`, `Income`, `Children`, `Education`, `Occupation`, `Home Owner`, `Cars`, `Commute Distance`, `Region`, `Age`, `Purchased Bike`.

### 2. "Working Sheet" (Limpeza e Transformação de Dados)
Esta é a aba de processamento técnico, onde os dados foram padronizados para garantir maior clareza e permitir segmentações mais inteligentes.
* **Estado Civil (`Marital Status`):** Substituição de `M` por `Married` (Casado) e `S` por `Single` (Solteiro).
* **Gênero (`Gender`):** Substituição de `F` por `Female` (Feminino) e `M` por `Male` (Masculino).
* **Nova Variável (`Age Brackets`):** Utilização de fórmulas lógicas (`SE`/`IF`) para agrupar a idade dos clientes em três faixas etárias:
  * Adolescent (Adolescentes/Jovens)
  * Middle Age (Meia-idade)
  * Old (Idosos)
* **Objetivo:** Preparar a base para que as Tabelas Dinâmicas gerassem rótulos limpos e fáceis de interpretar no Dashboard.

### 3. "Pivot Table" (Análise e Agregação de Dados)
Essa é uma aba intermediária onde os dados transformados da `Working Sheet` foram sumarizados para responder a perguntas de negócio específicas.

**Análises Identificadas:**
* **Média Salarial por Gênero e Compra:** Serviu para comparar se o nível de renda média impacta na decisão de compra entre homens e mulheres.
* **Distância de Deslocamento (`Commute Distance`):** Quantidade de bicicletas compradas com base na distância diária percorrida pelo cliente até o trabalho.
* **Faixa Etária (`Age Brackets`):** Análise do volume de compras concentrado em cada ciclo de vida (Adolescente, Meia-idade, Idoso) para perceber qual faixa etária compra mais ou compra menos.

### 4. "Dashboard" (Apresentação Visual e Insights)
Aqui é a aba final do projeto. Um painel interativo construído para tomadores de decisão poderem analisar os resultados, conectando os gráficos dinâmicos gerados a partir da aba anterior.
* Nesta aba foram usados elementos visuais como gráficos de colunas e linhas que ilustram as tendências de compra.
* Inclui *Slicers* (Segmentadores de Dados) por Região, Educação e Ocupação, permitindo filtrar todo o painel de forma dinâmica com apenas um clique.

---

## Principais Insights Obtidos

1. **Impacto da Renda:** Clientes que efetivamente compraram bicicletas possuem, em média, uma renda salarial superior àqueles que não compraram, indicando que o poder aquisitivo é um forte indicador de conversão.
2. **Efeito da Distância de Deslocamento:** O maior volume de compras concentra-se em clientes que moram muito perto do trabalho (0-1 milhas), sugerindo o uso da bicicleta para locomoção diária rápida ou lazer de curta distância.
3. **Público-Alvo por Idade:** A categoria de *Middle Age* (Meia-idade) representa a esmagadora maioria das compras efetuadas, sendo o público mais estratégico para campanhas de marketing direcionadas.

---

## Aspectos Técnicos

### Tecnologias e Ferramentas Utilizadas
Para esse projeto foi usado o **Microsoft Excel**:
* Fórmulas de Texto e Lógicas (`IF`, substituições).
* Ferramentas de Limpeza de Dados (Remover duplicadas, formatação).
* Tabelas Dinâmicas (*Pivot Tables*).
