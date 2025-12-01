README — Projeto de Análise Exploratória e Pré-Processamento dos Dados da Olist
 Integrantes do Grupo
João Pedro Lima Barbosa
Rodofo Dheymison Ferreira Silva 

 Base de Dados Utilizada
Os dados utilizados fazem parte do Brazilian E-Commerce Public Dataset by Olist, disponível em:
 https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
Foram utilizados 3 datasets principais:
olist_orders_dataset.csv
olist_order_items_dataset.csv
olist_products_dataset.csv
 Objetivo do Projeto
O objetivo deste trabalho é realizar um processo completo de análise exploratória (EDA) e pré-processamento dos dados da Olist para:
entender padrões de vendas, frete e comportamento logístico;
analisar atrasos, tempos de entrega e características dos produtos;
tratar, limpar e padronizar os dados;
criar novas features relevantes;
consolidar um dataset final limpo, pronto para futuras análises ou modelos de machine learning.
Este projeto segue todas as etapas do ciclo de vida da ciência de dados aplicadas em um cenário real de e-commerce.
  Descrição do Processo de Tratamento dos Dados
O notebook do projeto realizou as seguintes etapas:
1. Análise Inicial
Contagem de linhas e colunas
Visualização de dados
Verificação de tipos
Identificação de nulos, inconsistências e outliers
2. Limpeza dos Dados
Preenchimento de valores ausentes (datas, categorias, dimensões)
Ajustes em colunas inconsistentes
Padronização de textos e categorias
Remoção/correção de categorias inválidas
Tratamento de outliers usando IQR (capping)
3. Conversão e Padronização de Tipos
Datas convertidas para datetime
IDs padronizados como string
Dimensões e atributos numéricos ajustados
4. Codificação de Variáveis Categóricas
Label Encoding → product_category_name
One-Hot Encoding → order_status
5. Normalização
Aplicado MinMaxScaler em:
price
freight_value
6. Feature Engineering
Foram criados 7 novos atributos:
tempo_entrega
dias_processamento
atraso_entrega
valor_total_item
percentual_frete
volume_cm3
quantidade_itens_pedido
7. Seleção de Atributos
Matriz de correlação
Análise de variância (VarianceThreshold)
Identificação de atributos redundantes
8. EDA — Análise Exploratória dos Dados
Gráficos gerados sobre:
preços
frete
categorias mais vendidas
tempo de entrega
atrasos
volume dos produtos
correlação
evolução mensal dos pedidos
9. Exportação do Dataset Final
O dataset consolidado foi salvo como:
dataset_final_tratado.csv
  Principais Desafios Encontrados
Durante o projeto, enfrentamos desafios como:
alto volume de valores ausentes em datas importantes;
inconsistências nos nomes das colunas do dataset original;
grande quantidade de categorias distintas para produtos;
presença de outliers extremos em preço, frete e dimensões;
necessidade de combinar três datasets diferentes por chaves distintas;
padronização de datas que estavam desformatadas ou faltando;
correção de atrasos negativos e datas invertidas.
Esses desafios exigiram múltiplas técnicas de tratamento e validação.
  Principais Conclusões
A análise permitiu identificar:
Frete e preço possuem correlação significativa, especialmente para produtos volumosos.
Existe grande variação no tempo real de entrega, impactando diretamente o atraso.
Atrasos acontecem, mas muitos pedidos são entregues antes do prazo estimado.
Algumas categorias dominam o volume de vendas, mas não necessariamente são as mais lucrativas.
O volume do produto influencia fortemente no valor do frete.
O ciclo de compra → aprovação → envio → entrega tem etapas críticas, especialmente na aprovação e na logística do transportador.
O dataset final está completamente limpo, padronizado e enriquecido com novas variáveis, pronto para ser utilizado em análises avançadas ou modelos preditivos.
