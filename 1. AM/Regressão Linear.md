Regressão Linear é um modelo matemático que descreve a relação entre duas ou mais variáveis. A regressão Linear utiliza conceitos estatísticos para prever um valor no futuro. Por ser um modelo simples e rápido, os modelos de Regressão Linear são bastante utilizados em Aprendizado de Máquina. A base da Regressão Linear é a equação da reta, então, é esperado que as variáveis possuam uma relação linear. Dependendo do análise pode-se utilizar o modelo de Regressão Linear simples ou múltiplo.
### Simples
A Regressão Linear simples busca estabelecer uma relação entre uma variável dependente e outra independente.
![[regression-simple.png|700]]
### Múltipla
A Regressão Linear Múltipla busca estabelecer uma relação entre uma variável dependente e múltiplas independentes.
![[regression-multiple.png|700]]


Na Regressão Linear simples é possível visualizar as variáveis de forma gráfica em um plano bi-dimensional, já no caso da múltipla, só é possível visualizar, quando temos no máximo 3 variáveis, acima disso só é possível analisar redimensionando ou de forma separada.
Utilizando problemas do mundo real, é muito improvável que a reta obtida pela equação passe por todos os pontos, portanto, o objetivo final é encontrar a ou as retas que possuem o menor custo. A distância entre o ponto real e o ponto encontrado é conhecido como erro, quando somado o quadrado dos erros encontra-se o custo da reta.
![[regression-error.jpg|700]]
A cada variação dos valores de coeficiente angular e linear na equação da reta, obtém-se uma nova reta e portanto um novo custo, entretanto, é muito custoso somente escolher valores aleatórios de coeficiente como método de minimização de custo, em vez disso, é comum utilizar algoritmos conhecidos para encontrar esses valores. Um algoritmo conhecido para minimização de custo é o Gradiente Descendente.
### Gradiente Descendente
