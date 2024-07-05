# Previsão de Estoque Inteligente com Amazon SageMaker Canvas

## Introdução
Este projeto é um desafio da Digital Innovation One (DIO) com o objetivo de criar um modelo de Machine Learning no-code para previsão de estoque utilizando o Amazon SageMaker Canvas.

## Objetivo
Desenvolver um modelo de previsão de estoque utilizando séries temporais com o Amazon SageMaker Canvas.

## Dados
O conjunto de dados utilizado contém as seguintes colunas:
- **ID_PRODUTO**: Identificador do produto.
- **DIA**: Data.
- **FLAG_PROMOCAO**: Indicador de promoção (0 ou 1).
- **QUANTIDADE_ESTOQUE**: Quantidade em estoque.


###  Configuração do Modelo de Série Temporal
1. **Coluna de Identificação do Item (Item ID column)**: Selecione **ID_PRODUTO**.
2. **Coluna de Agrupamento (Group column)**:  vazio.
3. **Coluna de Carimbo de Tempo (Time stamp column)**: Selecionado **DIA**.
4. **Número de dias para prever (Days)**: 3 dias.

###  Avaliação do Modelo
1. Analise as métricas de desempenho:
    - **Avg. wQL (Average Weighted Quantile Loss)**: 0.668
    - **MAPE (Mean Absolute Percentage Error)**: 0.700
    - **WAPE (Weighted Absolute Percentage Error)**: 0.727
    - **RMSE (Root Mean Squared Error)**: 5.543
    - **MASE (Mean Absolute Scaled Error)**: 0.138



    - **Demanda Histórica**: Representada pela linha azul.
    - **Previsões P10, P50 e P90**: Representadas pelas linhas de diferentes cores, indicando diferentes níveis de confiança.

![image](https://github.com/DevRobertW/lab-aws-sagemaker-canvas-estoque/assets/149734892/96ec4504-b4d9-40ab-a81b-8654bc70b617)


## Resultados
- As métricas de desempenho indicam que o modelo tem um erro percentual médio de aproximadamente 70% (MAPE e WAPE).
- O valor de MASE é 0.138, sugerindo que o modelo é melhor do que um benchmark simples.

## Conclusão
O Amazon SageMaker Canvas demonstrou ser uma ferramenta funcional e eficiente para criar modelos de previsão de estoque de maneira rápida e sem a necessidade de codificação. No entanto, para obter previsões mais precisas e confiáveis, é necessário realizar ajustes adicionais nos dados e nos hiperparâmetros do modelo. Com essas melhorias, espera-se que o modelo atinja um desempenho superior, reduzindo os erros percentuais e fornecendo previsões de estoque mais precisas.
