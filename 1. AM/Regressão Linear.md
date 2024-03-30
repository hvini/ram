Regressão Linear é um modelo matemático fundamental que descreve a relação entre variáveis. Utilizando conceitos estatísticos, ela prevê valores futuros. Amplamente empregada em Aprendizado de Máquina devido à sua simplicidade e eficácia, a Regressão Linear assume uma relação linear [[#^605abf]] entre as variáveis, sendo aplicável em modelos simples ou múltiplos.
$$
y = mx + c
$$

^605abf

### Simples
Na Regressão Linear Simples, estabelece-se a relação entre uma variável dependente e uma independente, permitindo uma representação gráfica bi-dimensional do relacionamento
![[regression-simple.png|600]]
### Múltipla
Na Regressão Linear Múltipla estabelece-se uma relação entre uma variável dependente e múltiplas independentes. No caso da Regressão Linear Múltipla, só é possível visualizar o relacionamento entre as variáveis quando se tem no máximo 3 variáveis, utilizando um plano tri-dimensional, acima disso, somente redimensionando ou de forma separada.
![[regression-multiple.png|600]]
Utilizando problemas do mundo real, é muito improvável que a reta obtida pela equação passe por todos os pontos, portanto, o objetivo final é encontrar a(s) reta(s) que minimizam o custo. A distância entre o ponto real e o ponto encontrado é conhecido como erro, quando somado o quadrado dos erros encontra-se o custo [[#^be7247]] da função. 
$$
J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} (h_{\theta}(x^{(i)}) - y^{(i)})^2
$$
^be7247

![[regression-error.jpg|600]]
A cada variação dos valores de coeficiente angular e linear na equação da reta [[#^605abf]], obtém-se uma nova reta e portanto um novo custo, entretanto, é muito custoso somente escolher valores aleatórios de coeficiente como método de minimização de custo, em vez disso, é comum utilizar algoritmos conhecidos para encontrar esses valores. Um algoritmo conhecido para minimização de custo é o Gradiente Descendente.
### Gradiente Descendente
O Gradiente Descendente é um algoritmo de otimização usado em modelos de aprendizado de máquina para minimizar uma função convexa. Ele ajusta os coeficientes iterativamente para alcançar o mínimo local da função, usando as derivadas do custo [[#^be7247]] em relação aos coeficientes para determinar a direção e magnitude dos ajustes necessários. O gradiente, um vetor que indica a direção de maior incremento de uma grandeza, é crucial no cálculo vetorial e determina como os coeficientes mudam em resposta aos erros. Quanto mais íngreme o gradiente, mais rápido é o aprendizado. Matematicamente, o gradiente é a derivada parcial em relação aos coeficientes [[#^4fce81]] e [[#^2a1473]].
$$
\frac{\partial J}{\partial \theta_0} = -\frac{2}{m} \sum_{i=1}^{m} (y^{(i)} - (\theta_1 x^{(i)} + \theta_0))
$$

^4fce81

$$
\frac{\partial J}{\partial \theta_1} = -\frac{2}{m} \sum_{i=1}^{m} x^{(i)}(y^{(i)} - (\theta_1 x^{(i)} + \theta_0))
$$

^2a1473

O algoritmo do Gradiente Descendente informa a próxima posição em sentido ao mínimo local. Inicialmente são definidos valores aleatórios para os coeficientes da função a ser minimizada e então o Gradiente Descendente move os valores passo a passo em sentido ao mínimo local. O passo a ser movido é definido por uma taxa de aprendizagem, onde, quanto maior a taxa maior é o salto e maior é a chance dos valores saltarem entre a função convexa e nunca atingirem o mínimo local e quanto menor o valor maior será o tempo para atingir o mínimo, ou seja, a taxa de aprendizagem nunca deve ser muito alta nem tão baixa.
![[gradient-descent-learning.webp||600]]
Para garantir que o Gradiente Descendente está funcionando corretamente pode-se exibir em um gráfico o custo a cada interação. Se o custo diminui a cada interação o Gradiente Descendente está funcionando corretamente.
![[gradient-descent-monitoring.webp||600]]