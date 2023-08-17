# reducao-dimensionalidade

Primeiramente, vamos ver como usar o algoritmo de componentes principais através do problema de classificação de atividade humana por dados de acelerômetro e giroscópio de celular na base HAR.

O contexto é o seguinte: esta base começa a ter um tamanho razoável para um hardware de computador pessoal: ela possui 7000 registros na base de treinamento e 3000 registros na base de testes, cada uma contendo 561 variáveis. Dessa forma, o processamento de um algoritmo nessa base pode levar um tempo razoável se considerarmos todas as variáveis - ainda considerando os diversos ajustes no algoritmo e uma eventual validação cruzada.

Assim, se quisermos ganhar agilidade, uma boa ideia é fazer redução de dimensionalidade - ou seja, trabalhar com um número menor de variáveis, com a menor perda de informação possível. Digamos que queremos limitar o nosso algoritmo a apenas 3 variáveis - é claro que vamos perder a informação das demais, mas será que não podemos minimizar essa perda construindo 3 novas variáveis através de combinações das 561?

Em poucas linhas, é esse o uso mais frequente da análise de componentes principais (PCA para principal component analysis): ela fornece novas variáveis chamadas de componentes principais, que são combinações lineares das 561 variáveis, e podem ser utilizadas em menor número de modo a minimizar a perda de informação. A técnica se baseia em álgebra linear, mas no momento vamos nos focar no uso, depois falamos um pouco sobre a mecânica.
