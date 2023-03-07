## Training vs testing
Como estavamos viendo previamente, podemos estimar the out/of/sample error $E_{out}$ from the in-sample error$E_{in}$ 
- $E_{in}$ entrenamiento muestreo
- $E_{out}$ realidad, 

## The test set
Una alternativa es usar un test de test, que no van a ser usado en ninguna prueba para entrenar, este conjunto sale de dividir nuestro dataset en datos de entrenamiento y prueba.

### Other target types
Previamente hemos definido $E_{in}$ y $E_{out}$ basado en funcion binaria:
$$E_{in}(h)=\frac{1}{N} \sum\limits_{n=1}^{N}[(h(x_{n}) \neq f(x_{n}))]$$
$$E_{out}(h)=P[h(x)\neq f(x)]$$
donde h es la estimaicon y f nuestra funcion real

### Ejercicio
Para la funcion con objetivo binario, muestre que $P[h(x)\neq f(x)]$ puede ser escrito como un error cuadratico medio en los siguients casos:
- The convention used for the binary function is 0 or 1
- The conention used for the binary function is +- 1

Hint: the differene between both is just a scale

## The Bias-Variance Decomposition
nos ayuda de manera general a ver como se comporta un conjunto de datos. el error esta dado por:
$$E_{out}(g^{(D)}) =\mathbb{E}_{x}[g^{(D)}(x)-f(x)^{2}]$$

#### Excercise
Show that ir $H$ is closed under linear combination (any linear combination fo hypotheses in H is a iso a hypotesis in H), then $\overline{g}\in H$ 
