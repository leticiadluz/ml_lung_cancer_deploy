# Previsão de Câncer de Pulmão com R

- O objetivo deste projeto é criar um modelo de machine learning utilizando o Tidymodels para prever o risco de câncer de pulmão. Este modelo pode ajudar as pessoas a entenderem melhor o risco de desenvolver câncer de pulmão com base em vários fatores, possibilitando a tomada de decisões apropriadas para a área saúde.
      
- Os dados foram coletados do [Kaggle](https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer/data)
  
- Para este projeto, utilizamos o Tidymodels, cuja principal função é fornecer uma interface coerente para todas as etapas do processo de modelagem, desde a preparação dos dados até a validação do modelo e a geração de previsões. O Tidymodels pode ser comparado ao pipeline do scikit-learn em Python, permitindo a criação de fluxos de trabalho com transformações, ajuste de hiperparâmetros e validação cruzada utilizando workflows e recipes.

- **Limitações:**  
         - **Tamanho do Conjunto de Dados:** O conjunto de dados utilizado é relativamente pequeno, contendo apenas 309 instâncias. Esse tamanho reduzido pode limitar a capacidade do modelo de generalizar para populações maiores e mais diversas.  
      - **Desbalanceamento dos Dados:** Os dados estavam extremamente desbalanceados, com 39 instâncias negativas para o desenvolvimento de câncer contra 270 instâncias positivas. Esse desbalanceamento pode levar a um viés no modelo, fazendo com que ele tenha dificuldade em identificar corretamente os casos negativos e, potencialmente, gerando um alto número de falsos positivos.  
      - **Falta de Fonte dos Dados:** Os dados no Kaggle não traziam a fonte da coleta, o que levanta preocupações sobre a validade e a representatividade dos dados.    
    
- **Pontos Positivos:**  
      - **Identificação de Risco:** Modelos de previsão podem identificar indivíduos com alto risco de desenvolver câncer de pulmão, permitindo intervenções preventivas e diagnósticos precoces, o que pode aumentar significativamente as chances de tratamento bem-sucedido.    
      - **Apoio ao Diagnóstico Médico:** O modelo pode ajudar os médicos a rastrear rapidamente os pacientes e identificar aqueles em alto risco que necessitam de exames adicionais. Isso pode ter um impacto significativo na intervenção precoce e no planejamento de tratamentos personalizados, melhorando os resultados de sobrevivência dos pacientes.    
      - **Eficiência no Tratamento:** Com a capacidade de identificar casos de alto risco, o modelo permite que os profissionais de saúde priorizem e direcionem recursos de maneira mais eficaz, promovendo uma gestão mais eficiente e focada na prevenção e tratamento do câncer de pulmão.    

## Conclusões sobre o Modelo Preditivo:    
- Foram desenvolvidos cinco modelos de machine learning para a previsão de câncer de pulmão. Os resultados foram:  
      - **Regressão Logística:** Sem levar em conta o desbalanceamento das classes, atingiu um recall de 0.61 nos dados de treino.    
      - **Random Forest:** Sem tratar o desbalanceamento das classes, alcançou um recall de 0.58. Com o método de case weights, resultou em um recall de 0.78.  
      - **K-Nearest Neighbors (KNN):** Utilizou técnicas de oversampling, com SMOTE obtendo um recall de 0.85 e ADASYN alcançando um recall de 0.90 nos dados de treino e teste.  

- **Esses resultados indicam que há espaço para melhorar ainda mais os modelos de machine learning, especialmente no que diz respeito ao recall. Um recall maior que 0.90 é extremamente importante para área da saúde, pois aumenta a capacidade do modelo de identificar corretamente a maioria dos casos positivos de câncer de pulmão, minimizando o risco de falsos negativos e possibilitando intervenções precoces e mais eficazes.**  

## Deploy  
- O segundo objetivo deste projeto era realizar o deploy do modelo para um serviço de nuvem utilizando a AWS, por meio das bibliotecas Vetiver e Plumber.
- **Vetiver:** Permite gerenciar e versionar modelos de machine learning de maneira eficiente, facilitando a integração e o deploy desses modelos em ambientes de produção. Gera um arquivo Docker, que é usado para criar uma imagem Docker.
- **Plumber:** Permite a criação de APIs RESTful em R, facilitando a exposição dos modelos de machine learning como serviços web.
- Com a API criada, o arquivo Docker gerado pela Vetiver pode ser hospedado no serviço ECS (Elastic Container Service) da AWS, permitindo que o modelo seja acessível de maneira escalável pela internet. Esse processo de deploy na nuvem garante que o modelo esteja disponível, possibilitando a realização de previsões e podendo ser integrado com outras aplicações e serviços.
- Para demonstrar a criação e funcionamento do contêiner no AWS ECS e da aplicação, fiz um vídeo detalhando o processo. O serviço não ficará ativo para evitar custos futuros.
- Para acessar o vídeo de demonstração clique [aqui](https://drive.google.com/drive/folders/1CjE35TrdnHBjZnJEEKLZ7MxsMdNOz_wU)
