# Análise de Dados Olist – ETL, Limpeza e EDA

Este repositório apresenta o processo completo de tratamento e análise dos dados da Olist, contemplando etapas de ETL, limpeza, criação de variáveis e análise exploratória.

## Estrutura do Projeto

- Notebook principal (.ipynb) com todas as etapas sequenciais
- Arquivos de dados utilizados (opcional)
- Dataset final tratado exportado como CSV ou ZIP

## Etapas Realizadas

### 1. Importação e Análise Inicial
- Carregamento dos três datasets da Olist  
- Verificação de dimensões, tipos e valores ausentes  
- Identificação de duplicatas e inconsistências  

### 2. Tratamento dos Dados
- Preenchimento de valores ausentes
- Padronização de textos e categorias
- Tratamento de outliers utilizando o método IQR
- Ajustes de consistência nos datasets

### 3. Codificação e Normalização
- Label Encoding para categorias com muitas classes
- One-Hot Encoding para variáveis com poucas categorias
- Normalização MinMax para variáveis numéricas

### 4. Merge dos Datasets e Feature Engineering
Criação de variáveis adicionais, entre elas:
- tempo_entrega  
- dias_processamento  
- atraso_entrega  
- volume_cm3  
- valor_total_item  
- percentual_frete  
- quantidade_itens_pedido  

### 5. Análise Exploratória (EDA)
Inclui:
- Distribuições de preço, frete e tempo de entrega
- Categorias mais vendidas
- Matriz de correlação
- Evolução mensal de pedidos

### 6. Conclusões Gerais
O processo resultou em um dataset limpo, consolidado e adequado para análises avançadas ou uso em modelos preditivos. Foram identificados padrões relevantes em relação a prazos, fretes, categorias e sazonalidade.

## Tecnologias Utilizadas

- Python  
- Pandas, NumPy  
- Scikit-Learn  
- Matplotlib, Seaborn  
- Jupyter Notebook

## Arquivo Final
O dataset final tratado foi exportado como:
dataset_final_tratado.csv

