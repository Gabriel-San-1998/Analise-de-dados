Este projeto tem como objetivo explorar um conjunto de dados de diamantes, identificar padrões relevantes e aplicar modelos de Machine Learning para prever o preço com base em características físicas e qualitativas.



Etapas do Projeto

1. Análise Exploratória de Dados (EDA)

  Foram realizadas análises iniciais para entender a distribuição dos dados e as relações entre variáveis:
  
    Visualização da distribuição de preços
    Relação entre peso (carat) e preço
    Análise de correlação entre variáveis

2. Relação entre peso e preço
   
  Principais insights:

    Forte relação positiva entre carat e price
    Quanto maior o diamante, maior tende a ser o preço
    Existe dispersão crescente → outros fatores também influenciam o preço

3. Correlação entre variáveis

  Principais insights:

    carat possui forte correlação com price (~0.92)
    Dimensões físicas (x, y, z) também têm alta correlação com o preço
    Variáveis como cut, color e clarity possuem menor correlação linear
    Alta correlação entre x, y e z (possível multicolinearidade)

4. Pré-processamento
    Conversão de variáveis categóricas (cut, color, clarity) para valores numéricos
    Normalização dos dados com preprocessing.scale
    Embaralhamento dos dados para evitar viés
    Separação entre variáveis independentes (X) e alvo (y)

5. Modelagem

  Foram testados modelos de regressão utilizando Support Vector Machines (SVR):

    Modelo 1: SVR com kernel linear
    R² ≈ 0.87
    Boa performance geral
    Problema: previsão de valores negativos (não faz sentido no contexto)
    
    Modelo 2: SVR com kernel RBF
    R² inferior ao modelo linear
    Porém:
    Não gera valores negativos
    Melhor comportamento para relações não lineares

6. Reflexões e Aprendizados
   
    O preço dos diamantes é fortemente influenciado pelo tamanho (carat)
   
    Relações não são totalmente lineares → modelos mais complexos podem ser necessários
   
    Correlação não implica causalidade, mas ajuda a identificar variáveis relevantes
   
