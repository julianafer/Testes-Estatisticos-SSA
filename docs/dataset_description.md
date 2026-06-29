# Caracterização do dataset analítico


| Característica             | Valor                                                                                                                                           |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nome**                   | `df_analytical`                                                                                                                                 |
| **Granularidade**          | Produto                                                                                                                                         |
| **Número de registros**    | 61.079 produtos                                                                                                                                 |
| **Número de atributos**    | 28 variáveis                                                                                                                                    |
| **Fonte dos dados**        | Dunnhumby – The Complete Journey                                                                                                                |
| **Tabelas utilizadas**     | `product`, `transaction_data`, `coupon`, `causal_data`                                                                         |
| **Tabelas não utilizadas** | `campaign_table`, `coupon_redempt`, `campaign_desc`, `hh_demographic`                                                                                            |
| **Objetivo**               | Servir como base analítica para análises exploratórias e experimentos de clusterização voltados ao estudo da alocação de espaço em prateleiras. |


O dataset analítico resultante é composto por 61.079 produtos, descritos por 28 atributos obtidos a partir da integração e transformação de múltiplas tabelas do conjunto de dados Dunnhumby – The Complete Journey. A base reúne informações cadastrais dos produtos, indicadores agregados de vendas, dados de campanhas promocionais e atributos derivados por meio da etapa de engenharia de atributos, constituindo um conjunto de dados estruturado e adequado para análises exploratórias e aplicação de técnicas de mineração de dados, em especial métodos de clusterização voltados ao estudo da alocação de espaço em prateleiras.

## Dicionário de dados


| Coluna                   | Tipo    | Exemplo                | Origem                     | Descrição                                                                                        |
| ------------------------ | ------- | ---------------------- | -------------------------- | ------------------------------------------------------------------------------------------------ |
| **PRODUCT_ID**           | int64   | `25671`                | `product`                  | Identificador único do produto. Chave primária do dataset analítico.                             |
| **MANUFACTURER**         | int64   | `69`                   | `product`                  | Identificador do fabricante responsável pelo produto.                                            |
| **DEPARTMENT**           | str     | `GROCERY`              | `product`                  | Departamento ao qual o produto pertence.                                                         |
| **BRAND**                | str     | `PRIVATE`              | `product`                  | Tipo de marca do produto (marca própria ou nacional).                                            |
| **COMMODITY_DESC**       | str     | `SOFT DRINKS`          | `product`                  | Categoria principal do produto.                                                                  |
| **SUB_COMMODITY_DESC**   | str     | `CARBONATED BEVERAGES` | `product`                  | Subcategoria do produto, fornecendo uma classificação mais específica.                           |
| **CURR_SIZE_OF_PRODUCT** | str     | `16 OZ`                | `product`                  | Representação original do tamanho do produto conforme disponibilizada no dataset.                |
| **SIZE_VALUE**           | float64 | `16.0`                 | *Feature Engineering*      | Valor numérico extraído da coluna `CURR_SIZE_OF_PRODUCT`.                                        |
| **SIZE_UNIT**            | str     | `OZ`                   | *Feature Engineering*      | Unidade de medida extraída e padronizada da coluna `CURR_SIZE_OF_PRODUCT`.                       |
| **TOTAL_UNITS**          | float64 | `12458`                | `transaction_data`         | Quantidade total de unidades vendidas do produto durante todo o período analisado.               |
| **TOTAL_REVENUE**        | float64 | `37842.65`             | `transaction_data`         | Receita total gerada pelo produto ao longo do período analisado.                                 |
| **AVG_SALES_VALUE**      | float64 | `3.49`                 | `transaction_data`         | Valor médio das vendas por transação do produto.                                                 |
| **AVG_QUANTITY**         | float64 | `1.87`                 | `transaction_data`         | Quantidade média de unidades vendidas por transação.                                             |
| **N_TRANSACTIONS**       | float64 | `6842`                 | `transaction_data`         | Número total de transações nas quais o produto esteve presente.                                  |
| **N_STORES**             | float64 | `92`                   | `transaction_data`         | Número de lojas distintas em que o produto foi comercializado.                                   |
| **FIRST_WEEK**           | float64 | `1`                    | `transaction_data`         | Primeira semana em que houve registro de venda do produto.                                       |
| **LAST_WEEK**            | float64 | `104`                  | `transaction_data`         | Última semana em que houve registro de venda do produto.                                         |
| **N_COUPONS**            | int64   | `3`                    | `coupon`                   | Quantidade de cupons associados ao produto.                                                      |
| **N_CAMPAIGNS**          | int64   | `2`                    | `coupon`  | Número de campanhas promocionais distintas nas quais o produto participou.                       |
| **HAS_COUPON**           | int64   | `1`                    | `coupon`                   | Indicador da existência de cupons associados ao produto (0 = não, 1 = sim).                      |
| **N_PROMOTION_WEEKS**    | int64   | `15`                   | `causal_data`              | Número de semanas em que o produto participou de ações promocionais.                             |
| **N_STORES_PROMOTION**   | int64   | `38`                   | `causal_data`              | Quantidade de lojas nas quais o produto participou de promoções.                                 |
| **DISPLAY_EVENTS**       | int64   | `21`                   | `causal_data`              | Quantidade de ocorrências de ações promocionais do tipo *display*.                               |
| **MAILER_EVENTS**        | int64   | `8`                    | `causal_data`              | Quantidade de ocorrências de campanhas promocionais via *mailer*.                                |
| **DISPLAY_TYPES**        | int64   | `3`                    | `causal_data`              | Número de tipos distintos de exposição promocional (*display*) utilizados para o produto.        |
| **MAILER_TYPES**         | int64   | `2`                    | `causal_data`              | Número de tipos distintos de campanhas via *mailer* associados ao produto.                       |
| **HAS_DISPLAY**          | int64   | `1`                    | `causal_data`              | Indicador da existência de pelo menos uma ação promocional do tipo *display* (0 = não, 1 = sim). |
| **HAS_MAILER**           | int64   | `0`                    | `causal_data`              | Indicador da existência de pelo menos uma campanha promocional via *mailer* (0 = não, 1 = sim).  |

