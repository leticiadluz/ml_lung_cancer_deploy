# Previsão de Câncer de Pulmão com R

- O objetivo deste projeto é criar um modelo de machine learning utilizando o Tidymodels para prever o risco de câncer de pulmão.
- Este modelo pode ajudar as pessoas a entenderem melhor o risco de desenvolver câncer de pulmão com base em vários fatores,
- possibilitando a tomada de decisões apropriadas para a área saúde.
      
- Os dados foram coletados do Kaggle: https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer/data
  
- Para este projeto, utilizamos o Tidymodels, cuja principal função é fornecer uma interface coerente para todas as etapas do processo de modelagem,
- desde a preparação dos dados até a validação do modelo e a geração de previsões. O Tidymodels pode ser comparado ao pipeline do scikit-learn em Python, permitindo a criação de fluxos
- de trabalho com transformações, ajuste de hiperparâmetros e validação cruzada utilizando workflows e recipes.

- **Limitações:**
   - Tamanho do Conjunto de Dados: O conjunto de dados utilizado é relativamente pequeno, contendo apenas 309 instâncias.
   - Esse tamanho reduzido pode limitar a capacidade do modelo de generalizar para populações maiores e mais diversas.
Desbalanceamento dos Dados: Os dados estavam extremamente desbalanceados, com 39 instâncias negativas para o desenvolvimento de câncer contra 270 instâncias positivas. Esse desbalanceamento pode levar a um viés no modelo, fazendo com que ele tenha dificuldade em identificar corretamente os casos negativos e, potencialmente, gerando um alto número de falsos positivos.
