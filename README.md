# Bioinformatica


### Descrição e caracterização do dataset

O objetivo do estudo é a análise de amostras de biópsia do músculo vasto lateral de adultos jovens (cerca de 24 anos) e idosos (cerca de 84 anos) antes e depois de 12 semanas de treino de resistência progressivo (extensões bilaterais de joelho, 3x10 reps, 3 vezes por semana, ou seja, 36 sessões). Os resultados fornecem informações sobre a adaptação molecular do músculo esquelético jovem e idosos ao treino de resistência.

Foram incluídos 28 indivíduos na investigação: Os jovens adultos eram 8 homens e 8 mulheres, os idosos eram 6 homens e 6 mulheres. As amostras foram retiradas antes da primeira sessão, 4h depois da primeira sessão, antes da última sessão e 4h depois da última sessão, resultando num total de 4 biópsias por indivíduo.

Quanto aos metadados, verifica-se que possuem 5 variáveis: a amostra, a categoria de idade do indivíduo (young ou old), o tipo de amostra retirada (antes da primeira sessão, 4hr depois da primeira sessão, antes da última sessão ou 4h depois da última sessão), o sexo do indivíduo e os valores para aquele determinado indivíduo.

### Informaçao do Dataset

Dataset 9: GDS5218

https://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS5218

Ficheiros:
• Dados: gds5218.csv
• Meta Dados: meta-gds5218.csv


### Metodologia

#### Etapa 1 - Exploração do Dataset Pela Análise de Dados e Metadados

Formatação dos dados e metadados para análise. Descrição de dataset e caracterização de dados atribuídos com base no documento referente ao respetivo dataset. Vizualição de gráficos exploratórios de caracterísitcas principais de metadados, nomeadamente 'time' e 'age'. Etapas de standardização e passos de preprocessamentos de dados, nomeadamente tratamento de valores nulos (missing values) e transposição de dados. Seleção de metadados com maior relevância para análise.

#### Etapa 2 - Redução de Dimensionalidade e Clustering de Dados

Nesta etapa, iniciou-se por realizar a filtração de dados e testes estatísticos univariados. De seguida foram aplicados tecnicas de reduçao de dimensionalidade, nomeadamente PCA no qual foram selecionado  \textit{n_components}=0.9


Filtração de dados e testes estatísticos univariados. Aplicaçao de técnicas de redução de dimensionalidade (PCA, t-SNE) e métodos de clustering (Hierárquico, k-Means). Análise e interpretação de resultados.

#### Etapa 3 - Modelos de Aprendizagem Máquina

Desenvolvimento e aplicação de algoritmos de aprendizagem máquina supervisionada (Árvores de Decisão, Regressão Logística, SVM, NB, KNN). Análise de comportamento de modelos baseada em métricas de erro (accuracy, ROC) e aplicação de métodos de previsão de erro (cross-val-score). Análise e interpretaçao de resultados.




