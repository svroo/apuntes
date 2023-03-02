# Repositorio de libros
gen.lib.rus.ec

Programar en julia, python, r

# Procesos estocásticos
$E=P(A)$
$P:E \rightarrow [0,1]$
1. $P(0) =0,~P(A)=1,~P(B^{C}=1.P(B))$
2. $P(A~U~B) = P(A) + P(B),~~A\cap B$ 

1. Experimeto
2. Resultados
3. Espacio muestral (resultado de los experimentos)
4. Eventos con conjuntos en el espacio muestral





### Probabilidad condicional
$$P(R\mid S) = \frac{P(R\cap S)}{P(S)} = \frac{P(R,S)}{P(S)}$$
$$P(S\mid R) = \frac{P(R\cap S)}{P(R)}=\frac{P(R,S)}{P(R)}$$


si se despeja obtenemos:
$P(R,S) = P(R\mid S) P(S)$
$P(R,S) = P(S\mid R) P(R)$
$P(R\mid S) P(S) = P(S\mid R) ~P(R)$
$P(R\mid S) = P(S\mid R) ~\frac{P(R)}{P(S)}$ Regla de Bayes


### Idependencia de eventos

$P(R\cap S) = P(R\mid S)~P(S)$
$P(R,S) = P(R) P(S)$

Decimos que dos eventos son independientes cuando la probabilidad conjunta es diferente es el producto de sus probabilidades

## Variable aleatoria

Es una variable que viene del espacio muestral y toma un valor:
$X:\Omega \rightarrow \mathbb{R}$
Experimento de lanzar dados:
$\Omega = \{(i,j): ~ 1 \leq i,j \leq 6\}$ 
$(i,j) \rightarrow i+j$
$p(x=5) = p(\{(1,4), (3,2), (2,3), (4,1)\})$

Para calcular el valor de la variable aleatoria se tiene que contar el numero de casos favorables sobre el total de casos


# Tarea
Calcular la media y la desviación estandar del experimento de lanzar dos datos.

$\mu_{x}= \sum\limits_{k}P(X=k)k$ 
$\delta_{x}=\sum\limits_{n}^{delta}(\kappa - \mu_{x})^{2}p(x=n)$ 
