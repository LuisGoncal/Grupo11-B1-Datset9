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

Formatação dos dados e metadados para análise. Descrição de dataset e caracterização de dados atribuídos com base no documento referente ao respetivo dataset. Vizualição de gráficos exploratórios de caracterísitcas principais de metadados, nomeadamente  o 'time'. Etapas de standardização e passos de preprocessamentos de dados, nomeadamente tratamento de valores nulos (missing values) e transposição de dados. Seleção de metadados com maior relevância para análise.

#### Etapa 2 - Redução de Dimensionalidade e Clustering de Dados

Nesta etapa, iniciou-se por realizar a filtração de dados e testes estatísticos univariados. De seguida foram aplicados tecnicas de reduçao de dimensionalidade, nomeadamente PCA no qual foram selecionado  *n_components*=0.9 para o qual foi obtido um valor de 86, que significa que é necessario 86 componetnes para explicar 90% da variabilidade. Posto isto foi realizado um *Agglomerative Clustering* de forma a organizar os dados relativos  ao 'time', onde os clusters mais semelhantes são agrupados em níveis mais altos da hierarquia, especificamente, o clustering hierárquico aglomerativo segue uma abordagem de baixo para cima, onde cada ponto de dados começa como um cluster individual e, em seguida, clusters adjacentes são sucessivamente combinados com base em sua similaridade, neste caso foram selecionados 4 clusters uma vez que existem 4 variaveis de tempo. Também foi necessário recorrer ao método de K-means com o objetivo de criar grupos onde os pontos estejam próximos dos centróides dos clusters, minimizando as distâncias entre eles. Para tal estes dois metodos foram aplicados a diferente dados, primeiro foram aplicados ao dados standardizados e os seguintes a uma seleção específica de genes diferencialmente expressos.


#### Etapa 3 - Modelos de Aprendizagem Máquina

Nesta última etapa utilizou-se a aprendizagem supervisionada de forma a avaliar o impacto do treino de resistência progressivo no músculo e comparar períodos temporais distintos, além de segmentar os dados para análises detalhadas em diferentes momentos.
Para tal os dados de treino e teste foram divididos em 70% e 30% respetivamente e examinou-se como a variável target está disposta nos conjuntos de treino e teste.
Após a divisão dos dados, implementou-se diversos modelos de aprendizagem máquina supervisionada, entre eles, Árvores de Decisão, Regressão Logística, SVM, NB, KNN.
Por fim realizou-se a análise de comportamento de modelos baseada em métricas de erro, nomeadamente accuracy e ROC, e aplicação de métodos de previsão de erro, cross-val-score. Ainda efetuou-se a análise e interpretaçao de resultados.






