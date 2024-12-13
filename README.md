# Sobre o dataset de critérios de classificação para concessão de empréstimos



O dataset Loan Approval Classification  Dataset (https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data?select=loan_data.csv) aborda a possibilidade de prever o status de aprovação de empréstimos com base em características demográficas (gênero, escolaridade, idade, renda), financeiras (ex: empréstimos prévios, se o indivíduo é proprietário ou não de imóvel) e específicas (ex: escore de crédito, percentual de renda comprometida com o empréstimo).


Este dataset possui 45.000 linhas e 14 atributos. Este conjunto de dados permite a classificação binária para concessão de empréstimo, levando em consideração o atributo categórico loan_status (status de aprovação do empréstimo), onde: 1 => aprovado; 0 => rejeitado.


Este projeto consiste em comparar as métricas de diferentes algoritmos de classificação binária, com aprendizado supervisionado. As métricas consideradas são: acurácia, precisão, recall, área da curva AUC-ROC, F1_score, a quantidade de falsos positivos e falsos negativos. Este MVP considerou os seguintes algoritmos: a) RandomForest; b) Árvore C 4.5; c) CART; d) KNN com 5 vizinhos; e) KNN com 3 vizinhos; f) Regressão Logística; g) Naive Bayes e h) Support Vector Machine (SVM).
O propósito deste trabalho consiste em auxiliar as instituições financeiras a reduzirem os riscos nos processos de concessão de empréstimo.


## URL do dataset no Github ##

O dataset foi copiado para a seguinte URL do Github: 
https://raw.githubusercontent.com/Andrea68A/Puc_Ciencia_Dados/refs/heads/MVP_Machine_Learning/loan_data.csv



## Link para o Google Colab ##



https://colab.research.google.com/github/Andrea68A/Puc_Ciencia_Dados/blob/MVP_Machine_Learning/MVP_dataset_emprestimo_Andrea.ipynb





