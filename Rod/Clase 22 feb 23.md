Experimento: arrojar dos dados
Espacio muestral: $\Omega = \{(i,s):~i,s=1,2,\dots,6\}$

$P:P(\Omega)\rightarrow [0,1]$

$$\Omega = \begin{bmatrix} (1,1)&(1,2)&(1,3)&(1,4)&(1,5)&(1,6) \\ (2,1)&(2,2)&(2,3)&(2,4)&(2,5)&(2,6) \\ (3,1)&(3,2)&(3,3)&(3,4)&(3,5)&(3,6) \\ (4,1)&(4,2)&(4,3)&(4,4)&(4,5)&(4,6) \\ (5,1)&(5,2)&(5,3)&(5,4)&(5,5)&(5,6) \\ (6,1)&(6,2)&(6,3)&(6,4)&(6,5)&(6,6)\end{bmatrix}$$
cada uno es un evento elemental 

$X:\Omega\rightarrow \mathbb{R}$
$(i,j) \rightarrow i+j$

$$X=\begin{bmatrix} 2&3&4&5&6&7 \\ 3&4&5&6&7&8 \\  4&5&6&7&8&9 \\ 5&6&7&8&9&10  \\ 6&7&8&9&10&11 \\ 7&8&9&10&11&12\end{bmatrix}$$


Calculando la probabilidad de casos favorables / totales:
$P(1) = \frac{1}{6}$

En un caso de independencia:
$P(i, j) = P(i)~P(j) = \frac{1}{36}$

Calculamos la probabilidad de que x = k, será igual a la probabilidad de un conjunto de eventos elementales.
$P(x= k) = P(\{(i,j:~i+j =k\})$
$k = 2, 3, \dots, 12$

Para calcular la probabilidad de la variable aleatoria cuando vale 3:
$P(x=3) = P(\{(2,1), (1,2)\})=P(\{(2,1)\} U \{(1,2\}) =\frac{2}{36} = \frac{1}{36}+ \frac{1}{36}$


![[Pasted image 20230222123028.png]]

Da como resultado la función de distribución discreta: $P(X=X_{k})$ 

$V_{x} = \sum\limits_{k}(x_{k}-\mu_{k})^{2}~P(X=Xk)$ 
$\mu_{x}= \sum\limits_{k}X_{k}~P(X=x_{k})$  

## Variables aleatorias continuas
Toman valores directamente de los numeros reales, no se calcula la probabilidad de que tome valores puntuales, lo que se valora, es que caiga en un intervalo diferencial.

Se calcula por una función de densidad de probabilidad

$P(x\leq X\leq xdx) = F(x) dx$ 
$P(a\leq X \leq b) = \int_{a}^{b}F_{x}(x)dx$ 