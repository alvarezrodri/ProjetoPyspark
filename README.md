# 📊 Análise de Despesas Públicas com PySpark

## 📊 Dashboard 

Acesse o dashboard aqui:
https://lookerstudio.google.com/s/oXlOoKeAbeI

## 🎯 Objetivo

Este projeto tem como objetivo construir um pipeline completo de dados para análise de despesas públicas utilizando **PySpark**, cobrindo desde a ingestão até a visualização e aplicação de modelos de machine learning.

A solução foi desenvolvida para:

- Processar grandes volumes de dados de forma distribuída
- Realizar limpeza e padronização de dados brutos
- Explorar padrões de gastos governamentais
- Preparar dados para modelagem preditiva
- Identificar comportamentos semelhantes de despesas
- Prever valores de gastos com modelos de regressão
- Reduzir a dimensionalidade dos dados mantendo sua variabilidade
- Criar dashboards interativos para análise visual dos dados

O projeto simula um cenário real de dados, integrando **engenharia de dados, análise exploratória, machine learning e visualização de dados**.

---

## ⚙️ Tecnologias Utilizadas

- Python
- PySpark
- Spark MLlib
- Looker Studio (visualização de dados)

---

## 🔄 Pipeline de Dados

### 1. Ingestão de Dados
- Leitura de arquivos CSV
- Separador `;`
- Inferência automática de schema

### 2. Seleção e Padronização
- Seleção de colunas relevantes
- Renomeação de colunas para padrão consistente

### 3. Tratamento de Dados
- Conversão de valores monetários (string → float)
- Tratamento de valores nulos
- Padronização de variáveis categóricas

### 4. Manipulação de Datas
- Conversão para formato de data
- Extração de ano e mês

### 5. Análise Exploratória
- Contagem de órgãos distintos
- Ranking de gastos por:
  - Órgão
  - Unidade gestora
  - Tipo de despesa

### 6. Preparação para Machine Learning
- Codificação de variáveis categóricas (`StringIndexer`)
- Criação de vetor de features (`VectorAssembler`)
- Normalização dos dados (`MinMaxScaler`)

---

## 🤖 Modelos de Machine Learning

### 🔹 KMeans (Clusterização)
- Agrupamento em 5 clusters
- Identificação de padrões de comportamento de gastos

### 🔹 Random Forest (Regressão)
- Previsão do valor pago
- Avaliação do modelo com RMSE

### 🔹 PCA (Redução de Dimensionalidade)
- Redução do número de variáveis
- Preservação da variância dos dados

---

## 📊 Visualização de Dados (Looker Studio)

Os dados processados foram utilizados para construção de um dashboard interativo no **Looker Studio**, permitindo uma análise visual mais intuitiva dos gastos públicos.

### Principais visualizações:

- 💰 Indicadores principais:
  - Valor total pago (R$ 1,17 tri)
  - Valor total empenhado
  - Valor total liquidado

- 📊 Gráfico de barras:
  - Comparação de gastos por ministério
  - Destaque para o Ministério da Fazenda como maior responsável pelos gastos

- 📉 Gráfico horizontal:
  - Comparação entre valores empenhados e liquidados

- 🍩 Gráfico de distribuição:
  - Participação percentual dos principais ministérios nos gastos totais

Essas visualizações permitem identificar rapidamente:
- Concentração de gastos
- Principais áreas de investimento público
- Diferenças entre valores empenhados e pagos

---

## 💾 Saída dos Dados

- Exportação em formato **Parquet**
- Otimizado para processamento distribuído e integração com ferramentas de BI

---

## 📌 Conclusão

Este projeto demonstra a construção de um pipeline completo de dados em larga escala, integrando múltiplas etapas essenciais:

- Engenharia de dados para tratamento e estruturação de dados brutos
- Análise exploratória para geração de insights relevantes
- Aplicação de machine learning para:
  - Identificação de padrões ocultos (clusterização)
  - Previsão de despesas (regressão)
- Redução da complexidade dos dados com PCA
- Visualização interativa com Looker Studio para apoio à tomada de decisão

Na prática, a solução mostra como transformar dados públicos em informações estratégicas, podendo ser aplicada em:

- Monitoramento e controle de gastos públicos  
- Auditoria e detecção de anomalias  
- Planejamento orçamentário  
- Suporte à tomada de decisão baseada em dados  

Além disso, o uso combinado de **PySpark + Looker Studio** evidencia um fluxo moderno de dados, unindo processamento em larga escala com visualização acessível e interativa.

---

## 🚀 Possíveis Melhorias

- Implementação de validação cruzada (Cross Validation)
- Ajuste de hiperparâmetros
- Criação de pipelines com `Pipeline` do Spark ML
- Integração com Data Warehouse
- Publicação do dashboard online

