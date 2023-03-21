# Distribución estacionaria o final de una cadena de Markov

Hay dos probabilidades importantes para las cadenas de markov

$lim_{n\rightarrow\infty}~P(X_{n}=J) =\pi_{J}$ (Distribucion estacionario)

Vamos a escribirla como una probabilidad conjunta para calcular la marginal a partir de la conjunta, en este caso la vamos a escribir como una marginal a partir de la conjunta:
$$P(X_{n+1}=J)=\sum\limits_{i ~\in~S}P(X_{n+1}=5, X_{N}= i)$$

y ahora la marginal la escribimos como el producto de la condicional:
$$P(X_{n+1}=J)=\sum\limits_{i ~\in~S}P(X_{n+1}=5, X_{N}= i)=\sum\limits_{i~\in~S}P(X_{n+1}=J\mid X_{n}=1)P(X_{n}=1)$$

Donde $P(X_{n+1}=J\mid X_{n}=1)$ es la entrada ij de una cadena de markov  y llegamos a:
$$P(X_{n+1}=J)=\sum\limits_{i~\in~S}P_{ij}P(X_{n}=1)$$
después se tima el limite de los extremos, queda como:
$$\pi_{J}=lim_{n\rightarrow\infty}~~ P(X_{n+1}=J)=\sum\limits_{i~\in~S}p_{ij}~lim_{n\rightarrow 6}~p(X_{n}=i)$$
y esto es equivalente a:
$$\pi_{J}=\sum\limits_{i~\in~S} P_{IJ}\pi_{i},~~~~~~\pi=\pi P$$ 
viendolo de forma matricial tenemos:
$$\begin{pmatrix} \pi_{i},\dots,\pi_{n}\end{pmatrix}\begin{pmatrix}P_{11}&P_{12}&\dots&P_{nn} \\ P_{21}& P_{22}&\dots&P_{2n} \\ \vdots&\vdots& &\vdots \\ P_{n1}&P_{n2}& &P_{nn} \end{pmatrix}=\begin{pmatrix}\pi_{1},\pi_{2},\dots,\pi_{3},\dots,\pi_{4} \end{pmatrix}$$

### Libro a utilizar: Stochastic Processes with R an introduction
autora Olga Korosteleva

## Ejercicio
Vamos a considerar una matriz de probabilidad de la siguiente forma:
$$\begin{bmatrix}\pi_{1},\pi_{2},\pi_{3},\end{bmatrix}=\begin{bmatrix}\pi_{1},\pi_{2},\pi_{3},\end{bmatrix} \begin{bmatrix}0.7&0.1&0.2 \\ 0.0&0.6&0.4 \\ 0.5&0.2&0.3\end{bmatrix}$$

Al realizar la multiplicaciones correspondientes tenemos lo siguiente:
$0.7\pi_{1}+0.0\pi_2+0.5\pi_{3}=\pi_{1}$
$0.1\pi_{1}+0.6\pi_{2}+0.2\pi_{3}=\pi_{2}$
$0.2\pi_{1}+0.4\pi_{2}+0.3\pi_{3}=\pi_{3}$

La solución va a ser el valor de la cadena de markov estacionaria, conocemos que $\pi_{1}+\pi_{2}+\pi_{3}=1$ 
Se resuelve el sisitema de ecuaciones despejando primero $\pi_{3}$, luego $\pi_{2}$ y por ulitmo en la suma de los pi igual a uno se sustituyen los valores previos para obtener el valor de cada uno

$\pi_{3}=0.6\pi_{1}$
$\pi_{2}=0.55\pi_{1}$

Valores propios
$\pi1=0.4651$
$\pi_{2}=0.2258$
$\pi_{3}=0.2790$


