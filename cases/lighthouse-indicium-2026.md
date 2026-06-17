# Lighthouse / Indicium 2026 — Analytics, SQL, previsão e recomendação

## Visão geral

Case técnico de Analytics e Ciência de Dados desenvolvido no contexto Lighthouse / Indicium 2026.

O projeto trabalha um cenário comercial com vendas, produtos e custos de importação, combinando análise exploratória, tratamento de dados, SQL, dados públicos de câmbio, previsão simples de demanda e recomendação de produtos.

Este estudo de caso apresenta uma visão pública do projeto, com foco nas competências técnicas demonstradas e sem exposição de dados restritos, enunciado integral ou detalhes sensíveis.

---

## Objetivo

Transformar dados operacionais em informação útil para tomada de decisão, avaliando qualidade dos dados, desempenho comercial, custos, risco de prejuízo, comportamento de clientes, sazonalidade e relações entre produtos.

---

## Principais frentes do notebook

### 1. Análise exploratória de vendas

- Leitura e inspeção da base de vendas.
- Avaliação de volume de linhas e colunas.
- Identificação de intervalo temporal.
- Análise da coluna de valor total.
- Verificação de nulos, tipos de dados e inconsistências de data.

### 2. SQL com DuckDB

- Uso de consultas SQL diretamente sobre DataFrames.
- Cálculo de métricas agregadas.
- Validação de resultados obtidos em Python.
- Criação de consultas para análise de vendas, clientes e calendário.

### 3. Limpeza e padronização de produtos

- Padronização de categorias.
- Conversão de valores para tipos numéricos.
- Remoção de duplicidades.
- Preparação de dados para cruzamento com vendas e custos.

### 4. Custos de importação e câmbio

- Leitura de dados de custo em moeda estrangeira.
- Conversão e validação de estrutura dos dados.
- Uso de cotação PTAX para conversão cambial.
- Associação temporal entre venda, custo vigente e câmbio aplicável.
- Cálculo de custo em BRL, prejuízo por transação e perda por produto.

### 5. Análise de clientes

- Cálculo de faturamento por cliente.
- Frequência de compras.
- Diversidade de categorias compradas.
- Ticket médio.
- Identificação de clientes de alto valor com diversidade de compra.
- Análise da categoria predominante entre clientes selecionados.

### 6. Dimensão de calendário

- Construção de tabela calendário via SQL.
- Cruzamento com vendas diárias.
- Inclusão de dias sem venda.
- Cálculo de média de vendas por dia da semana.

### 7. Previsão de demanda

- Seleção de produto específico para análise.
- Construção de série temporal diária.
- Inclusão de dias sem venda.
- Separação entre treino e teste.
- Baseline com média móvel de 7 dias.
- Previsão diária para janeiro de 2024.
- Avaliação com MAE.

### 8. Sistema de recomendação

- Construção de matriz usuário × produto.
- Cálculo de similaridade de cosseno entre produtos.
- Geração de ranking de produtos similares.
- Recomendação baseada em padrões de coocorrência de compra.

---

## Tecnologias e bibliotecas

- Python
- pandas
- NumPy
- DuckDB
- Matplotlib
- Requests
- scikit-learn
- Cosine Similarity
- API pública PTAX do Banco Central
- Google Colab / Jupyter Notebook

---

## Competências demonstradas

- Análise exploratória de dados
- Tratamento e padronização de dados
- SQL aplicado a analytics
- Modelagem de custos
- Integração com dado público externo
- Análise temporal
- Construção de dimensão calendário
- Forecasting baseline
- Métrica MAE
- Sistema de recomendação por similaridade
- Comunicação técnica de resultados
- Apoio à decisão com dados

---

## Resultados técnicos destacados

- Identificação de inconsistências de data na base bruta.
- Padronização de categorias de produtos.
- Cálculo de prejuízo por transação e por produto com base em custo, câmbio e receita.
- Identificação de produtos com maior perda financeira absoluta e relativa.
- Análise de clientes com maior ticket médio e diversidade de compra.
- Criação de tabela calendário para análise de dias com e sem venda.
- Construção de baseline de previsão de demanda com média móvel.
- Geração de ranking de produtos similares a partir de matriz de interação.

---

## Limitações

- O baseline de previsão por média móvel é simples e não captura bem produtos com vendas esparsas.
- A recomendação por similaridade considera coocorrência de compra e não substitui validação de negócio.
- O notebook depende de bases auxiliares externas que devem ser publicadas somente se houver autorização.
- A versão pública deve evitar exposição integral de enunciado, dados restritos ou respostas de processo seletivo.

---

## Enquadramento profissional

Este projeto reforça uma linha de atuação em Analytics e Ciência de Dados aplicada: transformar dados operacionais em rastreabilidade, previsibilidade e apoio à decisão.
