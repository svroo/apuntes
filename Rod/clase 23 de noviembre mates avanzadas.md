### Ejemplo 6.4 (268)
Consiere el siguiente problema 

|Minimize | $-2x_{1}+x_{2}-x_{3}$|
|--|--|
|Sujeto a;| $x_{1}+x_{2}+x_{3}\leq6$ |
| |$-x_{1}+2x_{2}\geq 4$|
| |$x_{1},x_{2},x_{3}\geq0$|

con el vector $c=(-2,1,-1 )$ y $c_{2}=1\iff-1$ 
Con la siguiente tabla

| |z|$x_{1}$| $x_{2}$| $x_{3}$| $x_4$|$x_{5}$|RHS|
|-|-|-|-|-|-|-|-|
|Z| 1|0|1|-3|-2|1|-12|
|$x_{1}$|0|1|1|1|1|0|6|
|$x_{5}$|0|0|3|1|1|1|10|
Supongamos que intercambiamos $c_{2} = 1\iff -3$, como $x_{2}$ no es basica $z_{j}-c'_{j} = (z_{j}-c_{j}) + (c_{j}-c'_{j})$

Al realizar el cambio pedido, obtenemos la siguiente entrada

| |z|$x_{1}$| $x_{2}$| $x_{3}$| $x_4$|$x_{5}$|RHS|
|-|-|-|-|-|-|-|-|
|Z| 1|0|1|-1|-2|1|-12|
|$x_{1}$|0|1|1|1|1|0|6|
|$x_{5}$|0|0|3|1|1|1|10|
A partir de este punto se continua con el metodo simplex, ahora modifiquemos $c_{1}= 2 \iff 0$, en este caso, la modificacion se hace a todo el renglón 0, vea la formula:

$$z'_{j} -c_{j}= (z_{j}-c_{j}) + (C'_{Bi}-C_{Bi})yij$$

| |z|$x_{1}$| $x_{2}$| $x_{3}$| $x_4$|$x_{5}$|RHS|
|-|-|-|-|-|-|-|-|
|Z| 1|0|1|-3|-2|1|-12|
|$x_{1}$|0|1|1|1|1|0|6|
|$x_{5}$|0|0|3|1|1|1|10|

Quedan los calculos de la siguiente manera:
$Z'_{j}-c_{j} = 0+(0-(-2)) = 2$
Para toda variable que no hemos cambiado aplicamos la siguietne formula:
$$z'_{j} -c_{j} + c_{j}-c'_{j} = 2+-2 + 0 = 0 = z'_{j} -c'_{j}$$
$$z'_{j} - c_{2} = (-3)+(0-(-2)) 1 = -3+2=-1$$ 
Ahora con $x_{3}$
$$z'_{3}-c_{3} = (-1)+(0-(-2)) 1 = (-1)+2=1$$
y ahora con $x_{4}$
$$z'_{4}-c_{4}= (-2)+2(1) = 0$$
ahora con $x_{5}$
$$z_{5}-c_{5}= 0+(0-(-2)) 0 = 0$$
este es el performance nuevo, la parte básica del vector c primo, por el vector b barra, el calculo:
$$C'_{B}B^{-1}b=C_{B}B^{-1}b+(C_{Bi}-C_{B})\overline{b}_{i} = -12 + 2 * 6 = 0$$
Y la tabla queda de la siguiente manera

| |z|$x_{1}$| $x_{2}$| $x_{3}$| $x_4$|$x_{5}$|RHS|
|-|-|-|-|-|-|-|-|
|Z| 1|0|-1|0|0|0|0|
|$x_{1}$|0|1|1|1|1|0|6|
|$x_{5}$|0|0|3|1|1|1|10|

Toca análizar que pasa con el vector b

### Cambios en el vector del lado derecho (b)
Si el vector b es reemplazado por $b'$, entonces $B^{-1}b$ será reemplazado por $B^{-1}$:
$$\begin{bmatrix}1 & z_{1}-c_{1}&z_{2}-c_{2} &\dots & z_m-c_{m} & z\\ \theta & y_{1}&y_{2} & \dots & y_{n} & \overline{b}\end{bmatrix}$$
Y la única dificultad que podemos encontrar es que $B^{-1}b' \ngeq 0$, en tal caso se continua con el método dual-Simplex. Si $B^{-1}b' \geq 0$ la solución se mantiene óptima.

#### Ejemplo 
En la tabla óptima inicial del ejemplo anterior reemplace:
$b' = \begin{pmatrix} 3 \\4 \end{pmatrix}$ luego $\overline{b} = B^{-1}b' = \begin{bmatrix}1 & 0 \\ 1 & 1\end{bmatrix} \begin{bmatrix}3\\4\end{bmatrix} = \begin{pmatrix} -3\\7\end{pmatrix}$ la nueva solución óptima es $x_{1}= -3, x_{2}= 7$

#### Cambios en la matriz de restricción A

**Caso 1 :** Cambios en columnas **No** básicas
Supongamos que la columna no básica $a_{}$, se modifica por $a'_{j}$. Entonces la a columna actualizada de la tabla "óptima" es $B^{-1}a'_{j}$ y $z'_{k} - c_{k} = C_{B}B^{-1}a_{j}-c_{j}$

El número $z_{i}$ es: $C_{B}B^{-1}a_{i} = z_{i}$ Si el indice i no es la columna que hemos modificada, entonces esta intacata, entonces todas las entradas del vector 0 que no se han movido son iguales a cero.
$$\begin{bmatrix}1 & z_{1}-c_{1}&z_{2}-c_{2} & z_{i}-c_{i} & z_m-c_{m} & z\\ \theta & y_{1}&y_{2} & y_{i} & y_{n} & \overline{b}\end{bmatrix}$$
Lo unico que se ha movido son las filas con subindice i y se actualiza de la siguiente manera:
$$\begin{bmatrix}1 & z_{1}-c_{1}&z_{2}-c_{2} & z_{i}-c_{i} & z_m-c_{m} & z\\ \theta & y_{1}&y_{2} & B^{-1}a'_{j} & y_{n} & \overline{b}\end{bmatrix}$$
El único problema que existiria es que fuera mayor a cero, en ese caso se continua con el método simplex.

**Caso 2:** Cambios en columnas básicas
Supongamos que una columna básica $a_{j}$ es modificada a $a'_{j}$, en este caso se debe comenzar a resolver desde cero
$$a_{1}, a_{2},\dots,a_{j},\dots, a_{m}~~a_{j}\iff a'_{j}$$
tenemos que identificar si siguen siendo lineal mente independiete, lo podemos realizar con la siguietne formula:
$$a'_{j}=\sum_{i=1}^{m} \lambda_{i}a_{i} = \sum_{i=1}^{m}\lambda_{i}a_{i}+\lambda_{j}a_{j}$$
Si es cero no es linealmente independiente, si es cero si es lineal mente independiente

#### Añadir una nueva actividad
Supongamos que una nueva actividad $x_{n+1}$ con costo unitario y columna de consumo $a_{n+1}$ 
Primero calculamos, $Z_{n+1} - C_{n+1}$ si este numero es negativo entonces $X*_{n+1}=0$, y la solución actual es óptima, si $z_{n+1} - c_{n+1}>0$ entonces $x_{n+1}$ entra a la base y se continua el metodo simplex.


Considere nuevamente la primera tabla óptima del primer ejemplo, y una nueva actividad $X_{6}\geq 0$ con $C_{6}=1$ y $a_{6}0\begin{pmatrix}-1\\2\end{pmatrix}$ calculemos primero, $z_{6}-a_{6}$ y a $y_{6}$ :
$$z_{6}-c_{6}= (-2,0)\begin{pmatrix}-1\\2\end{pmatrix} -1 = 0$$
$$y_{6}= B^{-1}a_{6} = \begin{bmatrix} 1 & 0 \\1 &1\end{bmatrix} \begin{bmatrix}-1\\2\end{bmatrix} = \begin{bmatrix}-1\\1\end{bmatrix}$$
Queda la siguiente tabla

| |z|$x_{1}$| $x_{2}$| $x_{3}$| $x_4$|$x_{5}$|$x_6$|RHS|
|-|-|-|-|-|-|-|-|--|
|Z| 1|0|-3|-1|-2|0|1|-12|
|$x_{1}$|0|1|1|1|1|0|-1|6|
|$x_{5}$|0|0|3|1|1|1|1|10|
y se tiene que continuar con el metodo simplex

<div align='right'><p> 24/11/2022</div>

##### Añadir una nueva restricción
Supongamos que una nueva restricción es añadida al problema. Si la solución optima $x^{*}$ satisface esta nueva restricción entonces esta se mantiene óptima.
$$X^{*} = min f(x)~~~~ x\in C$$
En todo caso, esto solo limita el conjunto de solución, podemos verlo como:
$$min f(x)~~~~ X \in C \cap C'$$
Si no se cumple se tiene que implementar el método dual simplex, para encontrar una nueva solución óptima.

Supongamos que B es la base óptima obtenida antes de añadir:
$$a^{m+1}x\geq b_{m+1}$$
$$a_{m+1}x_{1}+a_{m+1}2x_{2}+\dots+a_{m+1}, nx_{n}\leq b_{m+1}$$
$$1) ~z+(C_{B}B^{-1} N-C_{N})XN = C_{B}B^{-1}b $$
$$2)~~X_{B}+B^{-1}NX_{N}= B^{-1}b$$
y la última restricción se puede reescribir como:
$$3)~~ a^{m+1}_{B}  X_{B } + a_{N}^{m+1} X_{N}+X_{n+1} = b_{m+1}$$
Lo que se hace es multiplicar (2) por $a_{B}^{m+1}$ y obtenemos: $a_{B}^{^{m+y}}X_{B}+ a_{B}^{m+1}B^{-1}NX_{N}$ multiplicamos esto por la segunda ecuación 4) $a_{B}^{^{m+y}}X_{B}+ a_{B}^{m+1}B^{-1}NX_{N} = a_{B}^{m+1}B^{-1}b$ ahora se resta la tercera ecuación menos la cuarta.
$$(a_{N}^{m+1} - a_{B}^{m+1}B^{-1}N) X_{N}+X_{m+1} = b_{m+1}- a_{B}^{m+1}B^{-1}b \geq 0$$
Estas ecuaciónes nos dan una solución básica del nuevo sistema, si es positivo se termina, si no se continua el dúal simplex. La única posible violación a la optimalidad es el signo de $X_{n+1} = b_{m+1}-a_{B}^{m+1}B^{-1}b$  si $b_{m+1}-a_{B}^{m+1}B^{-1}b \geq 0$ entonces la nueva solución permanece óptima, en otro caso, se continua con el método dual simplex. 

![[Pasted image 20221124085836.png]]

Apliquemos la reesticcion: $-x_{1}+2x_{3}\geq 2$ 

![[Pasted image 20221124091225.png]]
[[Matematicas avanzadas]]
