# Cadenas de Markov
Investigar sobre Markov

#### Definición:
Una cadena de Markov es un proceso estocástico a tiempo discreto $X_{n},~n\in\{1,2,\dots\}$ que toma valores de estado discretos $s=\{0,1,2,\dots\}$. Con la propiedad que la probabilidad que: $p(xx_{n+1}=X_{n+1}\mid X=x_{0}, X_{1}=x_{1},\dots, X_{n-1}=x_{n-1},X_{n}=x_{n})=p(X_{n+1}=X_{n+1}\mid X_{n}=x_{n})$ (propiedad Markoviana) 

Como se calcula la probabilidad conjunta para una cadena de Markov: 
$$P(X_{n}=x_{n},X_{n-1}=X_{n-1},\dots,X_{1}=x_{1},X_{0}=x_{0})$$

Recordando que el calculo de probabilidad conjunta es igual a:
$$P(B\mid A)=\frac{P(A,B)}{P(A)}\rightarrow P(A,B) = P(B\mid A)P(A)$$

$P(X_{n}=x_{n},X_{n-1}=X_{n-1},\dots,X_{1}=x_{1},X_{0}=x_{0}) = P(X_{n}=x_{n}\mid X_{n-1}=x_{n-1},\dots,X_{0}=x_{0})P(X_{n-1}=x_{n-1},\dots X_{0}=x_{0})$
$=P(X_{n}=x_{n}\mid X_{n-1}=x_{n-1},\dots)P(X_{n-1}=x_{n-1}\mid X_{n-2}=x_{n-2},\dots)\cdots,P(X_{1}=x_{1}\mid X_{0}=x_{0})P(X_{0}=x_{0})$ 
$=[~\prod_{i=1}^{n}P(X_{i}=x_{i}\mid X_{i-1}=x_{i-i})~] P(X_{0})$ 

Probabilidad conjunta de una cadena de Markov
$$=\left[\prod_{i=1}^{n}P(X_{i}=x_{i}\mid X_{i-1}=x_{i-i})\right]  P(X_{0})$$

Tenemos algo llamado probabilidad inicial, para cada uno de los estados le vamos a llamar i, con la propiedad $\prod(x) = P(X_{0}=x),~x\in\S,\mid S\mid=n$ este es llamado como vector de probabilidades de valores de inicio en una cadena de Markov

Lo primero, defino $P(X_{n+1}=j\mid X_{n}=1)$ cuando depende de n, tengo una cadena de markov no estacionaria, cuando no depende de n tengo una cadena de markov estacionaria o de tiempo homogeneo y la puedo representar como $P_{ij}=P(X_{n+1}=j\mid X_{n}=i)$. Si tengo los estados finitos puedo ponerlos en una matriz:

$$\begin{matrix}0&\dots&\dots& \dots&n \\ 0&P_{00}&P_{01}&\dots&P_{0n} \\ \vdots &\vdots\\ \vdots&P_{n0}&P_{n1}&\dots&P_{nn}\end{matrix}$$

Una propiedad de esta matriz es:
$$\sum\limits_{j}^{i=0,1,\dots,n} P_{ij}=1$$
### Teorema de chapman-kolmogorov
(matrices de transición)

En una cadena de markov la probabilidad de llegar al estado J en n pasos a partir del estado i esta dado por:
$$P(X_{n}=J\mid X_{0}=1)~(n)=\sum\limits_{k=S}p(X_{n}=J\mid X_{r}=r)(n-r)~P(X_{r}=k \mid X_{0}=i)(r)$$

Prueba.
$$P(X_{n}=J\mid X_{0}=i)=\frac{P(X_{n}=jJ, X_{0}=i)}{P(X_{0}=i)} = \frac{1}{P(X_{0}=1)} \sum\limits_{R\in S} P(X_{n}=J,X_{r}=k, X_{0}=i)~\frac{P(X_{r}= k)}{P(X_{r}=k )}$$

Separamos la sumatoria en sus elementos independientes y el independiente:
$P(X_{n}=J, X_{r}=k)\rightarrow$ elementos dependientes
$P(X_{0}=i)\rightarrow$ Elementos independientes

y lo dividimos entre el ultimo termino de $P(X_{r}=k) / P(X_{r}=k)$ solo entre el dividendo
y el evento independiente lo unimos con el cociente de $P(X_{r}=k)$ y lo dividimos entre $\frac{1}{P(X_{0}=i)}$ quedando como resultado:

$$\sum\limits_{k\in S}P(X_{n}=J\mid X_{r}=k)P(X_{r}=k\mid X_{0}=i)$$

##### Corolario.
Si P es una matriz de transicion de una cadena de Markov entonces $P^{n}$ representa la probabilidad de n de un estado a otro con n pasos.

Prueba.
Caso base $n=1$ por definicion las entradas de P nos dan la probabilidad de pasos de un estado a otro en un paso.

Supongamos, de $P^{n-1}$ nos da la probabilidad de pasos del estado i al j en $(n-1)$ pasos/

$$P^{n}_{ij}=\sum\limits P_{ik}P_{kj}^{(n-1)}=\sum\limits_{K}p^{(n-1)} _{kj} p_{ik}=\sum\limits_{k}p(X_{i}=k\mid X_{0}=i)P(X_{n}=J\mid X_{i}=k)=P(X_{n}=J\mid X_{0}=i)$$
Por Chapman-Kolmogorov
