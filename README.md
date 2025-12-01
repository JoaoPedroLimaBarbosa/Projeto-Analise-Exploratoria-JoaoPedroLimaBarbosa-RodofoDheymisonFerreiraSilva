#  README — Projeto de Análise Exploratória e Pré-Processamento dos Dados da Olist

---

##  Integrantes do Grupo
- **João Pedro Lima Barbosa**
- **Rodofo Dheymison Ferreira Silva**

---

##  Base de Dados Utilizada
Os dados utilizados fazem parte do **Brazilian E-Commerce Public Dataset by Olist**, disponível em:

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

Datasets utilizados:
- `olist_orders_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_products_dataset.csv`

---

##  Objetivo do Projeto
Este projeto tem como objetivo aplicar um processo completo de:

- Análise Exploratória de Dados (EDA)
- Tratamento e limpeza
- Normalização e codificação
- Criação de novos atributos (Feature Engineering)
- Construção de um dataset final pronto para análise

Focado em compreender o comportamento logístico e comercial do comércio eletrônico da Olist.

---

## � Descrição do Processo de Tratamento dos Dados

### 1. Análise Inicial
- Contagem de linhas e colunas  
- Visualização de amostras iniciais (head)  
- Verificação dos tipos de dados  
- Identificação de valores ausentes  
- Detecção de inconsistências e outliers  

---

### 2. Limpeza dos Dados
- Preenchimento de valores ausentes em datas, categorias e dimensões  
- Correção de inconsistências nos nomes das colunas  
- Padronização de textos (lowercase e remoção de espaços)  
- Remoção ou correção de categorias inválidas  
- Tratamento de outliers utilizando o método IQR (capping)  

---

### 3. Conversão e Padronização de Tipos
- Conversão de colunas de data para `datetime`  
- Padronização de IDs como `string`  
- Ajustes em tipos numéricos  

---

### 4. Codificação de Variáveis Categóricas
- **Label Encoding** → `product_category_name`  
- **One-Hot Encoding** → `order_status`  

---

### 5. Normalização
Aplicação de **MinMaxScaler** nas colunas:
- `price`
- `freight_value`

---

### 6. Feature Engineering
Criação de 7 novos atributos:

- `tempo_entrega`  
- `dias_processamento`  
- `atraso_entrega`  
- `valor_total_item`  
- `percentual_frete`  
- `volume_cm3`  
- `quantidade_itens_pedido`  

---

### 7. Seleção de Atributos
- Matriz de correlação  
- Análise de variância com `VarianceThreshold`  
- Identificação de atributos redundantes  

---

### 8. EDA — Análise Exploratória dos Dados
Gráficos incluídos no projeto:

- Distribuição de preços  
- Distribuição de frete  
- Categorias mais vendidas  
- Tempo de entrega  
- Atrasos de entrega  
- Volume dos produtos  
- Correlação entre variáveis  
- Evolução mensal de pedidos  

---

### 9. Exportação do Dataset Final
O dataset final tratado foi salvo como:

```
dataset_final_tratado.csv
```

---

##  Principais Desafios Encontrados
- Alto volume de valores ausentes em colunas importantes  
- Inconsistências de nomenclatura no dataset original  
- Grande número de categorias únicas para produtos  
- Outliers extremos em preço, frete e dimensões  
- Necessidade de unir três datasets em um único  
- Datas invertidas e atrasos negativos  
- Ajustes de padronização de tipos e categorias  

---

##  Principais Conclusões

- Frete e preço apresentam correlação importante, principalmente em itens volumosos  
- Tempo de entrega varia bastante, influenciando atrasos  
- Muitos pedidos são entregues antes do prazo  
- Categorias mais vendidas não são as mais caras  
- O volume do produto impacta diretamente o valor do frete  
- O ciclo compra → aprovação → envio → entrega mostra gargalos logísticos  
- O dataset final ficou totalmente limpo, padronizado e enriquecido com novas features  

---

