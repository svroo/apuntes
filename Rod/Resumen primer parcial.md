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

### Independencia de eventos

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
##### Tarea
Calcular la media y la desviación estandar del experimento de lanzar dos datos.
$\mu_{x}= \sum\limits_{k}P(X=k)k$ 
$\delta_{x}=\sum\limits_{n}^{delta}(\kappa - \mu_{x})^{2}p(x=n)$ 

Experimento: arrojar dos dados
Espacio muestral: $\Omega = \{(i,s):~i,s=1,2,\dots,6\}$
$P:P(\Omega)\rightarrow [0,1]$

$$\Omega = \begin{bmatrix} (1,1)&(1,2)&(1,3)&(1,4)&(1,5)&(1,6) \\ (2,1)&(2,2)&(2,3)&(2,4)&(2,5)&(2,6) \\ (3,1)&(3,2)&(3,3)&(3,4)&(3,5)&(3,6) \\ (4,1)&(4,2)&(4,3)&(4,4)&(4,5)&(4,6) \\ (5,1)&(5,2)&(5,3)&(5,4)&(5,5)&(5,6) \\ (6,1)&(6,2)&(6,3)&(6,4)&(6,5)&(6,6)\end{bmatrix}$$
cada uno es un evento elemental $X:\Omega\rightarrow \mathbb{R}$, $(i,j) \rightarrow i+j$

$$X=\begin{bmatrix} 2&3&4&5&6&7 \\ 3&4&5&6&7&8 \\  4&5&6&7&8&9 \\ 5&6&7&8&9&10  \\ 6&7&8&9&10&11 \\ 7&8&9&10&11&12\end{bmatrix}$$


Calculando la probabilidad de casos favorables / totales: $P(1) = \frac{1}{6}$ en un caso de independencia:
$P(i, j) = P(i)~P(j) = \frac{1}{36}$. Calculamos la probabilidad de que x = k, será igual a la probabilidad de un conjunto de eventos elementales. $P(x= k) = P(\{(i,j:~i+j =k\})$ $k = 2, 3, \dots, 12$. Para calcular la probabilidad de la variable aleatoria cuando vale 3: $P(x=3) = P(\{(2,1), (1,2)\})=P(\{(2,1)\} U \{(1,2\}) =\frac{2}{36} = \frac{1}{36}+ \frac{1}{36}$

![[Pasted image 20230222123028.png|500x350]]

Da como resultado la función de distribución discreta: $P(X=X_{k})$ 
$V_{x} = \sum\limits_{k}(x_{k}-\mu_{k})^{2}~P(X=Xk)$ 
$\mu_{x}= \sum\limits_{k}X_{k}~P(X=x_{k})$  

## Variables aleatorias continuas
Toman valores directamente de los numeros reales, no se calcula la probabilidad de que tome valores puntuales, lo que se valora, es que caiga en un intervalo diferencial.Se calcula por una función de densidad de probabilidad

$P(x\leq X\leq xdx) = F(x) dx$ 
$P(a\leq X \leq b) = \int_{a}^{b}F_{x}(x)dx$ 

# Distribución de Bernouli

El problema es encontrar la probabilidad de que en n ensayos con dos posibles resultados, cada uno de ellos con probabilidad p y 1-p  ocurran k con probabilidad p. Supongamos que tenemos 3 ensayos. 
n = 3
k = 0, 1, 2, 3

Es igual a $\begin{pmatrix} 3 \\ 2\end{pmatrix} = \frac{3!}{(3-2)!~2!} = 3$ 
Ahora con n = 4 y k = 2

Es igual a: $\begin{pmatrix}4 \\ 2 \end{pmatrix} = \frac{4!}{(4-2)!~2!} = 6$

Como es un producto podemos verlos como: $P(x=k)= \begin{pmatrix}n \\ k\end{pmatrix}p^{k}(1-p)^{u-k}$ 
Para calcular la media tenemos que recordar el binomio de Newton: $(a+b)^{n} = \sum\limits_{k=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix} a^{u-k}b^{k}$ 

Problema: Calcula el promedio de una variable aleatoria de Bernulli con parametros $(n,p)$.

$$\mu_{x}= E[x] = \sum\limits_{k}k~P[x=k] = \sum\limits_{k=0}^{n} k~\begin{pmatrix}n \\ k\end{pmatrix}p^{k}(1-p)^{n-k} = \sum\limits k\frac{n!}{k!(n-k)!} p^{k}(1-p)^{n-k}$$
$$= P_{n}\sum\limits_{k=1}^{n}\frac{(n-1)!}{[(n-1)-(k-1)]!~(k-1)!}p^{{(k-1)}} (1-p) ^{([n-1]-[k-1])}$$

Se hace un cambio de variable $\ell = k-1$ cuando $n=1 ~~~\ell=0$
$$M_{x}=Pn\sum\limits_{n}\frac{(n-1)!}{([n-1]-\ell)*\ell}p^{\ell}(1-p)^{[(n-1)-\ell]}$$

Donde $\sum\limits_{n}\frac{(n-1)!}{([n-1]-\ell)*\ell}$ es igual a $\begin{pmatrix}n-1 \\ \ell\end{pmatrix}$ y tenemos que:
$$pn\sum\limits_{\ell=0}^{n-1} \begin{pmatrix}n-1 \\ \ell\end{pmatrix}p^{\ell}(1-p)^{(n-1)-\ell}=pn((1-p)+p)^{n-1}=pn$$


##### Ejercicio.
Calcular la varianza de una variable discreta de bernulli

# Variable continua

La variable aleatoria continua puede tomar un valor del intervalo de los reales, lo que podemos calcular es que la variable caiga en un intervalo diferencial, $P(x\leq X\leq x+dx) = f_{x}(x)dx = dF(x)$ la ultima función se llama funcion de distribución o función de distribución acumulada.

$$dF(x) = f_{x}(x)dx = \frac{dF(x)}{dx} = f_{x}(x)$$

$$P(a\leq X \leq) = \int_{a}^{b}dF(x) = \int_{a}^{b}f_{x}(x)dx$$ 
por tanto se puede calcular la probabilidad de $P(X\leq x) =\int_{-\infty}^{x}f_{x}(t)dt$ 
El evento seguro sería cuando la variable sea menor a infinito $P(X\leq\infty) = 1 =\int_{-\infty}^{\infty}f_{x}(x) dx$ 

###### Función distribución uniforme 
Entre cero y uno
Para: 
$$0\leq U\leq1 con~f_{u}(x)=\left\lbrace\begin{matrix} 1&0\leq X\leq 1 \\ 0&caso~contrario\end{matrix}\right.$$

$$\mu_{x}= \int_{-\infty}^{\infty}x~f_{x}(x)~dx$$ 
$$V_{x}=\int_{-\infty}^{\infty}(u-\mu_{x})^{2}f_{x}(x)~dx$$ 

Proposición. Sea $U$ una variable aleatoria y $f_{v}$ y $F_{v}$ una función de densidad de probabilidad y de distribución respectivamente. Entonces la variable aleatoria $V=F^{-1}(u)$ se distribuye como $f_{v}$ 

Lo que sees que: $P(u\leq x) =x$ para la función distribución uniforme
$$P(u\leq x) = \int_{0}^{x}1dt = [t]_{0}^{x}= x-0 = x$$
Pero $P(V\leq x)$ se puede escribir como:
Al querer evaluar V en cualquier valor lo podemos ver como:
$$P(V\leq x) = P(F^{1}(U)\leq X)$$
Como los de abajo son momentos podemos verlo de la siguiente forma
$$F^{1}(U)) \leq X\iff U\leq F(X)$$
Verlo así:
$$P(V\leq x) = P(F^{1}(U)\leq X) = P(u\leq F(x))=F(x)$$
queda como:
$$P(v\leq x)=F(X)=\int_{-\infty}^{x}f_{x}(t)dt$$

###### Ejercicio:
Integral
$$f_{x}=\lambda e^{-\lambda x}$$
calcular la integral y graficar el histograma

# Binomios

$(a+b) =1$
$(a+b)^{1} =a+b$
$(a+b)^{2}= (a+b) (a+b)$
	$\vdots$ 
$(a+b)^{n}=(a+b)^{n-1}(a+b)$ 

sustituyendo apoyandonos del triangulo de pascal es:
%%$(a+b)^{4}\sum\limits$%%
$(a+b)^{4}= a^{4}+4a^{3}b+6a^{2}b^{2}+4ab^{3}+b^{4}$


Definición: Un histograma es una función que asigna a cada elemento de una partición de un intervalo $[a,b]$ el número de miembros de un conjunto de datos que pertenecen a dicho elemento.

D: Conjunto de datos
$[a,b] = U_{i=1}J_{i},~~j_{i}\cap J_{j}=0$ 
$hisT:J_{i}\rightarrow n_{i}$

Proposicion.
Sean los datos D los valores una variable aleatoria X con función de densidad $f_{X}(x)$.
Entonces $F_{X}(x)=n_{i}$ donde n; es el número de datos que eprtenecen a un intervalo $J_{i}$ deuna partición, que contiene a X.

Prueba.
Sea $(J_{i})^{2}$ una partición uniforme del intervalo $[0,1]$ con $\mid J_{i}\mid=\frac{1}{N}$, (donde n es el número de muestras generadas), entonces la probabilidad  de que X caiga en $J_{i}$ es $P\left(a_{i}\leq X \leq b_{i}=O_{i}+\frac{1}{N} \right) =F(b_{i})-F(a_{i})$. Por otro lado $P(a_{i}\leq X\leq b_{i})=\frac{n_{i}}{N}$ 

$$F(b_{i})-F(a_{i}) = \frac {n_{i}} {N},~~~~\frac{[F(b_{i})-F(a_{i})]} {\frac{i}{N}=b_{i}-a_{i}}=n_{i}$$ 
$lim_{N\rightarrow\infty} \frac{F(b_{i})-F(a_{i})}{b_{i}-a_{i}}=F_{X}(a_{i})$ 

###### Varianza
$$var(X) = \mathbb{E} [X-\mathbb{E}(X)^{2}]=\mathbb{E}[x^{2}-2X\mathbb{E}[X]+\mathbb{E}[X]^{2}]$$
$$=\mathbb{E}[X^{2}]-2\mathbb{E}[X]\mathbb{E}[X]+\mathbb{E}[X]^{2}=\mathbb{E}[X^{2}]-\mathbb{E^2}[X]$$
$$Var(X)=\mathbb{E}[X^{2}]-\mathbb{E^{2}}[X]$$

$VAR(cX)=E[(cX-E[cX])^{2}]=\mathbb{E}[(cX-c\mathbb{E}[x])^{2}]= \mathbb{E} [(c(X-\mathbb{E}[X])^{2}=\mathbb{E}[c^{2}(X-\mathbb{E}[X])^{2}]$
$=c^{2}\mathbb{E}[(X-\mathbb{E} [X])^{2}]$

$Var(cX)=c^{2}Var(X)$

###### Definición
Si x,y son variables aletorias continuas con función de destribucion conjunta $f_{xy}(x,y)$ decimos que son independientes si obtiene que $f_{xy} (x,y)=f_{x}(x)f_{y}(y)$ 

Proposición si X,Y son variables aleatorias continuas independientes entonces>
$E[XY]=\mathbb{E}[X]\mathbb{E}[Y]$

Prueba.
$$\mathbb{E}[x,y]=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}(xy)f_{XY}(x,y)d_{x}d_{y}=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}(x,y)f_{X}(x)f_{Y}(y)d_{x}d_{y}$$
$$=\mathbb{E}[Y]\mathbb{E}[X]$$

$Cov(X,Y) =\mathbb{E}[(x-\mathbb{E}[x]) (y-\mathbb{E}[y])]=\mathbb{E}[xy-x\mathbb{E}[Y]-\mathbb{E}[X]Y+\mathbb{E}[X]\mathbb{E}[Y]]$
$=\mathbb{E}[xy]-\mathbb{E}[y]\mathbb{E}[x]-\mathbb{E}[Y]\mathbb{E}[x]+\mathbb{E}[y]$
$=\mathbb{E}[XY]+\mathbb{E}[x]\mathbb{E}[Y]-2\mathbb{E}[X]\mathbb{E}[Y]$

$\mathbb{E}[X]\mathbb{E}[Y]$

###### Proposicion
Si dos variables aleatorias continuas X,Y son independientes, entonces su $cov(x,y)=0$

$$var(X+Y)=var(x) ~var(y)$$

Prueba.
$$var(x+y) = \mathbb{E}[((x+y) - \mathbb{E}[x+y])^{2}] = E[X]+E[Y]$$
$$=E{(x-E[x])}^{2}+(y+E[y])^{2}+2(x-E[x])(y-E[y])$$
$$=E[(x-E[x])^{2}] +E[(y+E[y])^{2}]+2E[(x-E[x]) (y-E(x))] $$
$$=var(x+y)=var(x)+var(y)$$

Definicion.
Decimos que una variable aleatoria descreta es de Bernoulli si vale 1 cuando ocurre un evento conn probabilidad p y q con probabilidad (1-p) cunado no ocurre el evento.

Sea y una variable aleatoria discreta de Bernoulli entonces:
- $E[y] = P,~~var(y)=P(p-1)$ 
Prueba.
$\mathbb{E}[Y] = 1 P +0(1-P)= P$
$Var(Y) = \mathbb{E}[(\frac{y}{\mathbb{E}[Y])^{2}]=}P(1-p)^{2}+(1-p)(0.p)^{2}=p(1-p)^{2}+(1-p)p^{2}=(1-p)[p(1-p)+p^{2}]$
$=(1-p)[p-p^{2}+p^{2}]=p(1-p)$

Si X es una variable aleatoria binomial con probabilidad $\begin{pmatrix}n \\ k\end{pmatrix} p^{n}(1-p)^{n-k}$ para n ensayos. Entonces X se puede representar como la suma de n variables aleatorias de Bernoulli de pendientes $X=Y+y+\cdots+Y\rightarrow n~veces$
$\mathbb{E}[X]=\mathbb{E}[Y]+\cdots+\mathbb{E}[Y]=n\mathbb{E}[Y]=np$
$var[X]=var[y]+\cdots+var[Y]=np(p-1)$ 

### Distribución geométrica
$P(x=n)=(1-p)^{n-1}p$

n es el ensayo en que primera vez ocurre un eento con probabilidad p $\mathbb{E}[X]$

Serie geométrica $\mid\gamma\mid<1$
$$\sum\limits_{n=0}^{\infty}\gamma^{n},~~Sn=\sum\limits_{k=0}^{n}\gamma^{k}=1+\gamma ^{n}$$
$$\gamma Sn=r+r^{2}+\cdots+r^{n}+r^{n+1}$$
a la primera se resta con la segunda y slo queda libre el primero y el ultimo elemento
$$Sn (1-r)Sn - rSn=1-r^{n-1}=Sn=\frac{1-r^{n+1}}{1-r}$$
Esto es solo cuando r es menor a 1
$$S=lim\frac{1-r^{n+1}}{1-r}=\frac{1}{1-r}$$
Para calcular el valor esperado, como es discreta tenemos la formula:
$$\mathbb{E}[X]=\sum\limits_{n=1}^{\infty}np(1-p)^{n-1}=p\left(\sum\limits_{n=1}^{\infty}n(1-p)^{n-1}\right)$$
vamos a calcularlo usando el valor absoluto:
$$\frac{d}{dx}=\left(\sum\limits_{n=0}^{\infty}\frac{d}{dx}x^{n}\right)=\sum\limits_{n=0}^{\infty}nx^{n-1}$$
Segunda forma:
$$\frac{d}{dx}\left(\frac{1}{1-x}\right)=(-1)(1-x)^{2}\frac{d}{dx}(1-x)=(-1)\frac{1}{(1-x)^{2}})(-1)=\frac{1}{(1-x)^{2}}$$
sustituyendo en la primera tenemos:
$$\mathbb{E}[X]=\sum\limits_{n=1}^{\infty}np(1-p)^{n-1}=\mid p\left(\sum\limits_{n=1}^{\infty}n(1-p)^{n-1}\right)\mid =p\frac{1}{(1-(1-p))^{2}}=\frac{p}{p^{2}}=\frac{1}{p}$$


# Ejercicio:
Calcular la varianza

## Distribución de Poisson
$$p(x=n)=\frac{\lambda^{k}}{k!}e^{-\lambda}$$
Para resolverla necesitaremso un resultado de la exponencial, vamos a utilizar el resultado de la derivada de la exponencial, se va a calcular la derivada de:
$$\frac{d}{dx}e^{x}=\frac{e^{0}-e}{w}=1$$
si ponemos e a la 0 que llamaremos w, menos 1, da w
$$\frac{d}{dx}e^{x}=\frac{e^{0-w}-e}{w}=1,~~e^w-1=w$$
$$\frac{d}{dx}e^{x}=e^{x},~~~~e^{w}=1+w,(e^\frac{x}{N})^{N}=\left(1+\frac{x}{N}\right)^{2}$$
y esto lo podemos ver como un limite:
$$e^{x}=(1+\frac{x}{N})^{N}=lim_{n\rightarrow\infty}\left(1+\frac{x}{n}\right)^{n}$$
y asi es como vemos a e como una secuencia:
$$e=lim_{n\rightarrow\infty}\left(1+\frac{x}{n}\right)^{n}$$

aproximarlo en python

viendo esto con el binomio de newton, podemos ver:
$\frac{\lambda^{k}}{k!}e^{-k}$ $e^{x}=\mid e^{w\mid^{N}=(1+w)^{N}=\sum\limits_{k=0}^{N}\begin{pmatrix}N \\ k\end{pmatrix}}w^{k}=\sum\limits_{k=0}^{N}\begin{pmatrix}N \\ k\end{pmatrix} \begin{pmatrix}X \\ N\end{pmatrix}^{k}=\sum\limits_{k=0}^{N}\frac{N(N-1)\cdots (N-k +1)}{k!} \frac{x^{k}}{N^{k}}$
$e^{x}=\sum\limits_{k=0}^{N}\left[\frac{N}{N}\frac{N-1}{N}\dots\frac{(N-[k-1])}{N}\right]\left( \frac{x^{k}}{k!}\right)$
$\left[\frac{N}{N}\frac{N-1}{N}\dots\frac{(N-[k-1])}{N}\right]\rightarrow k~factores$ 
$e^{k}=\sum\limits_{k=0}^{N}(1-\frac{1}{N})\dots(1-\frac{h-1}{N})\frac{X^{h}}{n}=lim_{n\rightarrow\infty}\sum\limits_{k=0}^{n}(1-\frac{1}{k})\dots(1-\frac{k-1}{k})\frac{x^{k}}{k!}$
$e^{x}=\sum\limits_{k=0}^{\infty}\frac{x^{k}}{k!},~~e=\sum\limits_{k=0}^{\infty}\left(\frac{1}{n!}\right)$

Representado a e como una serie tenemos:
$\lambda=np$
$p<<1$

$$\begin{pmatrix}n \\ k\end{pmatrix}p^{k}(1-p)^{n-k}$$

$$\frac{n(n-1)\dots(n-k+1)}{k!}\left(\frac{\lambda}{n}\right)^{k}(1-\frac{\lambda}{n})^{n}\left(1-\frac{k}{n}\right)^{-k}$$

Viendolo de forma de limite tenemos:
$$lim_{n\rightarrow\infty}\left[\frac{n}{n}\left(1-\frac{1}{n}\right)\cdots\left(1-\frac{(n-1)}{n}\right)\left(\frac{\lambda^{k}}{k!}\right)\left(1+\frac{(-\lambda)}{n}\right)^{n}\left(1-\frac{\lambda}{n}\right)^{-k}\right]=\frac{\lambda^{k}}{n}e^{-\lambda}$$

$$P(x~ocurre~en~el~k-esimo~~ensayo)=\frac{\lambda^{k}}{k!}e^{-k}$$
$$\mathbb{E}[X]=\sum\limits_{k=1}^{\infty}k\frac{\lambda^{k}}{k!}e^{-\lambda}=e^{-\lambda}\sum\limits_{k=1}^{\infty}\frac{\lambda^{k}}{(k-1)!}$$
$$\mathbb{E}[X]=\lambda e^{-\lambda}\sum\limits_{k=1}^{\infty}\frac{\lambda^{k-1}}{(k-1)!}=\lambda e^{-k}\left(\sum\limits_{\ell=0}^{\infty}\frac{\ell ^{\ell}}{\ell!}\right)=\lambda$$


# Ejercicio calcular varianza de poisson
$$Var = \mathbb{E}(x^{2})- [\mathbb{E} (x)]^{2}$$
Encontraremos:
$$\mathbb{E}(x^{2})=\sum\limits_{k=0}^{\infty}k^{2}p(x=k)$$
Utilizaremos la formula de la exponencial:
$$$ \mathbb{E}[x^{2}]=\sum\limits_{k=0}^{\infty}k^{2}p(x=k)$$

$$=\sum\limits_{k=0}^{\infty} k(k-1)+k*p(x=k)=\sum\limits_{k=0}^{\infty}k(k-1)p(x=k)+\sum\limits_{k=0}^{\infty}k*p(x=k)$$
$$=\lambda*\sum\limits_{k=2}^{\infty} \left[\frac{(e^{-\lambda} \lambda^{k-2})} {(k-2)!}\right] +\lambda=\lambda*e^{-\lambda} \lambda^{2} \sum\limits_{k=0}^{\infty}\left[\frac{(\lambda^{k-2})}{(k-2)!} \right]+\lambda=\lambda^{2}+\lambda$$
Entonces tenemos:
$$Var(x)=\lambda^{2}+\lambda -[\lambda^{2}]=\lambda$$


ver pelicula: talentos ocultos

Habilidades
1. Modelo
2. Programarlo
3. conceptos
4. sdf


x distancia del centro de la aguja a la linea paralela más cercana
$\theta$ ángulo que forma la agua con las lineas paralelas.

Rango de variabilidad de x:
$$x\in\left[0,\frac{t}{2}\right]$$

Rango de variabilidad de $\theta$:
$$\theta\in\left[0,\frac{\pi}{2}\right]$$

son variables que dependen del experimento.

Se puede gráficar su funcion de proabilidad, con base de $0~a~\frac{t}{2}$ y su altura de $\frac{2}{t}$ con una funcion de proabilidad de $f_{x}(x)=\frac{2}{T}$ 

La funcion de proabilidad para $\theta=f_{\theta}(\theta)=\frac{2}{\pi}$ con una distancia de $\frac{\pi}{2}$ y altura de $\frac{2}{\pi}$ 

Tenemos como condición para que la aguja cruce alguna linea paralela (hits), la condicion de corte es agarrar $\ell$ y proyectar verticalmente su imagen, usamos el seno para encontrar la proyección. La condición de cruce esta dado por: 
$$\frac{\ell~sen(\theta)}{2}$$
La condicion de cruza es:
$$x\leq\frac{\ell~sen(\theta)}{2}$$

Como tenemos dos ariables podemos calcular la funcion de densidad conunta de $x,\theta$ que es igual a la multiplicacion de ambas funciones.
$$f_{x\theta}(x,\theta) =\frac{4}{T\theta}$$

Proabilidad de que la agua cruze alguna linea paralela:

$$\int_{0}^{\frac{\pi}{2}}\int_{0}^{\frac{\ell}{2}sen(\theta)}\frac{4}{\pi T}~dx~d\theta$$

$$=\frac{4}{\pi t}\int_{0}^{\frac{\pi}{2}}\left( \int_{0}^{\frac{\ell}{2}sen(\theta)} dx\right)~~d\theta=\frac{4}{\pi~t}\int_{0}^{\frac{\pi}{2}}\frac{\ell}{2}sen(\theta)~d\theta=\frac{2\ell}{\pi~t}\left[-cos(\theta)\right]=\frac{2\ell}{\pi~t} =aprox~~\frac{h}{n}$$

despeando $\pi$ tenemos:
$$\pi=\frac{2\ell ~n}{h~t}=\frac{n}{h}$$

la condicion es que $0 <\ell \leq t$  


### Ejemplo 2
Se va a simular el lanzamiento de dardos, en un cuadrado de 2 x 2, osea con un area de 4, y un circulo con area $\pi$ se lanzan los dardos, usando numeros aleatorios que van desde -1 a 1,
$-1\leq x\leq 1$ 
$-1\leq y\leq 1$

vamos a comproar que si se acierta esta dado por:
$$\frac{\pi}{4} = \frac{na}{n}$$

Podemos despejar pi como
$$\pi=4\frac{na}{n}$$

## Desigualdad de Markov

Si X es una variable aleatoria con función de densidad de probabilidad $F()$ entonces:
$$P(X\geq a)<\frac{\mathbb{E}[X]}{a} ~~~~(a<0)$$

Prueba:
$$\mathbb{E}[X] = \int_{-\infty}^{\infty} xf(x)~dx=\int_{-\infty}^axf(x)~dx+\int_{a}^{\infty}xf(x)~dx$$
si la integral evaluada de infinito a a es positivo, se lo restamos a la otra integral.

$$\int_{a}^{\infty}xf(x)~dx\leq\mathbb{E}[X]$$
En la integral se cumple que a es menor que x, si se integra, queda:
$$a\int_{a}^{\infty}f(x)~dx\leq \int_{a}^{\infty}xf(x)~dx\leq\mathbb{E}[X]$$
Esto es lo mismo que verlo como si multiplicaramos a por la función
$$\int_{a}^{\infty}af(x)\leq\int_{a}^{\infty}xf(x)~dv$$
# Ley de los grandes numeros
### Ley debil y fuerte de los grandes numeros

#### Desigualdad de Chebyshev
En probabilidad, la **desigualdad** **de** **Chebyshov** (también escrito de **Chebychev**) es un resultado que ofrece una cota inferior a la probabilidad de que el valor de una variable aleatoria con varianza finita esté a una cierta distancia de su esperanza matemática.

Prueba:
$$\mathbb{E}\left[ \frac{(x-\mu)^{2}}{\sigma^{2}}\right]=\frac{1}{\sigma^{2}}\mathbb{E}[(x-\mu)^{2}]=\frac{\sigma^{2}}{\sigma^{2}}=1$$
$$p\left( \frac{(x-\mu)^{2}}{\sigma^{2}} \mid k^{2}\right)<\frac{1}{k^{2}},~p\left( \sqrt{ (x-\mu)^{2}} > \sqrt{(k\sigma^{2})}\right)$$

$$p(\mid x-\mu\mid~\geq~ k~\sigma)\leq \frac{1}{k^{2}}\rightarrow Desigualdad~de~Chebyshev$$

Sea $x_{1},x_{2},\dots,$ una secuencia de variables aleatorias independientes, con media $\mu$ y varianza, con la misma distribuciom media $\mu$ y varianza $\sigma^{2}$
$$P\left( \mid\frac{x_{1}+\dots+x_{n}}{n}-\mu\mid\right)>\epsilon\rightarrow 0~~~cuando~n\rightarrow\infty$$
#### Ley fuerte de los grnades numeros
Con prabilidad 1
$$lim_{n\rightarrow\infty} \frac{x_{1}+\dots +n}{n} =\mu$$

## Distribución Gaussiana (normal)
$$e^{-x^{2}}$$
Es una distribución proporcionada.
$$e^{-x^{2}}=\frac{1}{e^{x^{2}}}$$
Podemos agregar un $-\alpha$ a la x para extender la curva.

Integrando, tenemos:
$$\int_{-\infty}^{\infty}e^{-x^{2}}dx=2\int_{0}^{\infty} e^{-x^{2}}dx,~~~~~I=\int_{0}^{\infty}e^{-x^{2}}dx$$

$$I^{2}=\left(\int_{0}^{\infty}e^{-x^{2}}dx\right)=\left(\int_{0}^{\infty}e^{-y^{2}}dy\right)=\int_{0}^{\infty}\int_{0}^{\infty} e^{-x^{2}+y^{2}}dxdy$$

Donde: $y^{2}=x^{2}+y^{2}$

Insertar imagen

$$I^{2}=\int_{r=0}^{\infty}\int_{\theta=0}^{\frac{\pi}{2}}e^{-r^{2}}~r~d\theta dr=\int_{0}^{\infty}r\left(\int_{\theta}^{\frac{\pi}{2}}e^{r^{2}}d\theta \right)dr=\int_{\theta}^{\infty}e^{-r^{2}}r\left(\int_{0}^{\infty}d\theta\right)dr$$

$$2I=2\left(\frac{\sqrt{\pi}}{2}\right)=\sqrt{\pi}$$

Si hacemos:
$$\frac{1}{\sqrt{\pi}}\int_{-\infty}^{\infty}e^{-x^{2}}dx =1$$
y como al integral da uno podemos ver como si es una función de probabilidad


$$\int_{-\infty}^{\infty}\left(\frac{e^{-x^{2}}}{\sqrt{\pi}}dx\right)=1$$

Desplazandola y escalandola tenemos:
$$\frac{(x-\mu)^2}{2\pi^{2}}$$


Sea X una variable aleatria discreta con distribución geometrica
$P(x=n)=(1-p)^{n-1}p$ 
$\mathbb{E} [x]=\frac{1}{p}$
$var(x)=\mathbb{E}[(x-\mathbb{E}[x])^{2}]=\mathbb{E}[x^{2}]-\mathbb{E}[x]^{2}$ 

Generación de números aleatorios uniformemente distribuidos (mediante una secuancia congruencial periodica)

$x_{0}=semilla$
$x_{n+1}=ax_{u}+b~mod~w$

Revisar el libro de Donal knut, revisar las condiciones de divicibilidad The art of programing

$$\frac{1}{\sqrt{\pi}} \int_{-\infty}^{\infty}e^{-u^{2}}du = 1$$

Vamos a integrar la siguiente funcion dado lo que conocemos aunteriormente y lo vamos a probar en la distribucion gaussiana
$$\frac{1}{\Delta\sqrt{2\pi}}\int_{-\infty}^{\infty}e^\frac{-(x-\mu)^{2}}{2\sigma^{2}}dx$$

Dada una distribución Gaussiana:
$$\frac{1}{\sigma~2\sqrt\pi}=$$

# Procesos Estocásticos
Definición de un proceso estocástico es una familia de variables aleatorias $\{N_{t}:t\in T.X_{t}\in S\}$. Donde T es un conjunto de indices y S conjunto de estados

#### Definición de Caminata aleatoria
Caminata aleatoria (simple) es un proceso aestocastico discreto $T(z_{t},s\leq z)$ 
$$P(X_{n}=J\mid X_{n-1} =i)=\left\lbrace\begin {matrix} p,&j=i+1\\ q, & J=i-1 \\ 0, & en~caso~contrario\end{matrix} \right.$$

$X_{n}= x_{0}+\epsilon_{1}+\dots+\epsilon_{n}$ son variables de Bernoulli y calculamos su valor esperado como:
$\mathbb{E}[X_{n}]=\mathbb{E}\left[x_{0}+\sum\limits_{i=1}^{n}\epsilon_{1}\right] =\mathbb{E}[x_{0}]+\sum\limits_{i=1}^{n}\mathbb{E}[\epsilon_{i}]] = x_{0}+ \sum\limits_{i=1}^{n}\mathbb{E}[\epsilon_{1}]$ y obtenemos:
$\mathbb{E}[\epsilon_{i}]=1*p+(-1)*q=p-q~~~(i=1,2,\dots,n)$
$\mathbb{E}[X_{n}]=n(p-q)$
$var(X_{n})=\sum\limits_{i=1}^{n} var(\epsilon_{i})$
$var(\epsilon_{i}) =\mathbb{E}[\epsilon_{i}^{2}]-\mathbb{E}[\epsilon_{i}]^{2}$
$\mathbb{E}[\epsilon_{i}^{2}]=1^{2}*p+(-1)^{2}q=p+q=1$
$\mathbb{E}[\epsilon_{i}] ^{2}=p-q$
$var=1-(p-1)^{2}~~~~q=1-p$
$=1-(2p-1)^{2}=1-(4p^{2}-4p+1)=1-4p^{2}+4p-1=4p-4p^{2}=4p(1-p)$
$var=4npq$

La variable $X_{n}$ se puede escribir como pasos a la derecha menos pasos a la izquierda.
$X_{}=R_{n}-L_{n}~~ y~n=R_{n}+L_{n}$
$X_{n}+ n =2R_{n}\sum\limits_{i=1}^{n}\epsilon_{i}$

La suma de n variables Bernulli se distribuye como una Binomial con parametro p y n

$$R_{n}=\frac{x_{n}+n}{2}=\frac{1}{2}(y_{n}+n)+\frac{1}{2}\sum\limits_{i=1}^{n}(\epsilon_{i}+1)=\sum\limits_{i=1}^{n}\left(\frac{\epsilon_{i}+1}{2} \right)$$

$$$$
$$P(X_{n}=x \mid X_{0}=0 )=P\left(R_{n}=\frac{x=2}{2}\right)=\begin{pmatrix}n \\ \frac{x+2}{2}\end{pmatrix} p^{{\frac{x+2}{2}}} q^{(n-\frac{k+2}{2})} n-\left[\frac{x+2}{2} \right]=$$
$$=n-\frac{x}{2}-\frac{n}{2}=\frac{n}{2}-\frac{x}{2}=\frac{n-x}{2}$$

$$P(X_{n}=x\mid X_{0}=0)=\begin{pmatrix}n\\\frac{n+x}{2}\end{pmatrix}p^{\frac{n+x}{2}}q^{\frac{n-x}{2}}$$

Modificar probabilidad python

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

## Predictor de clima
Matriz estocastica
$$0~~~1$$
$$\begin{matrix}0 \\ 1\end{matrix}\begin{pmatrix}0.80&0.20 \\ 0.25& 0.75\end{pmatrix}$$

codigo en python

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


Definición: Un estado $i\in S$ es recurrente si la probabilidad de que regrese a i es uno es decir, si $P(X_{n}= 0~para~n\geq1\mid X_{0}= i)=1$, si $n=0$ $P(X_{0}= i\mid X_{0}=i)=1$ se dice que el estado es absorbente.

Definición: Un estado es transitorio si la probabilidad anterior es estrictamente menor que 1. Esto quiere decir que la cadena puede regresar o no al estado 2.

Definicion: Se dice que el estado j es accesible desde el estado i, si existe un entero $n\geq 0$ tal que $P_{ij}(n)> 0$ esto se escribe $i\rightarrow J$. Si ademas $J\rightarrow i$, i y j son con comunicantes $i \iff J$.

Nota: La comunicación es una relación de equivalencia, es decir se puede particionar el espacio de estados en clases comunicantes.

```mermaid
flowchart LR
i --> J
j --> i

```

conjunto como union de clases 

Definición: Una cadena de Markiv es irreducible si y solo si sus estados forman una sola clase comunicante, ejemplo de clase comunicante:
$$\begin{pmatrix}P_{11}&P_{12} \\ P_{21}& P_{22}\end{pmatrix}$$

Definición: Un estado $i \in S$ de una cadena de Markov se llama de absorción si es imposible salir de el. Es decir $P_{ii}= 1$.
Una cadena de markov es absorvente si tiene al menos un estado absorvente y si  de cada estado es posible ir al estado absorbente


## Ejemplo en r
``` r
install.packages("diagram") 
install.packages("expm") 
install.packages("markovchain")

tm.name<- matrix(c(p11.value, p12.value, . . . , pnn.value), nrow=n.value, ncol=n.value, byrow=TRUE)
tr.tm.name<- t(tm.name)

library(diagram) 
plotmat(tr.tm.name, )

library(markovchain) 
dtmc.name<- new("markovchain", transitionMatrix=tm.name, states=c("state1.name", "state2.name",...))
```

## Distribución multinomial
$\mid S\mid=k$, n ensayos $s=\{1,2,\dots,k\}$

De variables:
$X_{1}+X_{2}+\dots+X_{k}=n,P_{1}+\dots+P_{k}=1$

La variable aleatoria x la podemos ver como: $X=X_{1}+\dots+X_{R}$ y la suma de probabilidades como: $P_{i}=P(X =i)(i=1,2,\dots,k)$ y$P(X_{1})=x_{i}~X_{2}=x_{2},~~X_{k}=x_{k}=\frac{n!}{X_{1}!\dots x_{k}}~~P_{1}^{x_{1}\dots}P_{k}^{x_{k}}$ 
$(a+b)^{n}=\sum\limits_{n=0}^{0}\begin{pmatrix}u \\ k\end{pmatrix}a^{u-k}b^{k}=\sum\limits_{n=0}^{n}\frac{n!}{k!(n-k)!}$ donde: $X_{1}= n*k, x_{2}= k~~~x_{1}+x_{2}= (n-k)+k=n$ y $a=P_{1},b=P_{2},~~~P_{1}+P_{2}=1$ entonces tenemos que para calcular dos variables, tenemos:
$$=\sum\limits_{0\leq x_{1},x_{2}\leq n}\frac{n!}{x_{1}!x_{2}!}a^{x_{1}}, b^{x_{2}}, 1=\sum\limits_{3\leq x_{1},x_{2}\leq n}\frac{n}{x_{1}! x_{2}!} p_{1}p_{2}$$

Para tres casos:
$$(ab + c)^{n}=(a+(b+c))^{n}=\sum\limits_{\ell\leq0} ^{n}\begin{pmatrix}n \\ k\end{pmatrix}q^{n-k}(b+c)^{k}\sum\limits_{k=0}^{n}\begin{pmatrix}n\\ k\end{pmatrix}a^{n-k} \left(\sum\limits_{\ell=0}^{k} \begin{pmatrix} k \\ \ell\end{pmatrix}b^{k-\ell}c^{\ell} \right)$$

$$=\sum\limits_{n=0}^{n}\sum\limits_{\ell=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix}\begin{pmatrix}k \\ \ell\end{pmatrix} a^{n-k}b^{k-\ell}c^{\ell}$$
Donde:
$$\begin{pmatrix}n \\ k\end{pmatrix}\begin{pmatrix}k \\ \ell\end{pmatrix} = \frac{n!}{k!(n-k)!}\frac{k!}{\ell!(k-\ell)!}$$
$x_{1}= n-k$ $x_{2}=k-\ell$ $x_{3}= \ell$ $x_{1}+x_{2}+x_{3}=n$

$$\sum\limits_{0\leq x_{1},x_{2}, x_{3}\leq 4} \frac{n!}{x_{1}! x_{2}! x_{3}!}$$

### Proceso de Poisson
**Definicion:** Un proceso estocástico $\{N(t), t\geq0\}$ es llamado de conteo si $N(t)$ es el numero total de cuentos ocurridos al tiempo t.

Un proceso de conteo se dice que tiene incrementos independientes, si el número de eventos que ocurre en intervalos sin traslape son independientes

![[Pasted image 20230401141537.png]]

Un proceso de conteo $\{N(t), t\geq 0\}$ tiene incrementos estacoinarios si la distribución del numero de eventos ocurren en cada intervalo temporal, dependen solo de la longitud del intervalo.

En otras palabras $N(t_{s}) - N(s)$ tienen la misma distribución que $N(t)-N(0)$, es decir esta distribución depende únicamente de t no de S.

Un proceso estocástico de conteo es llamado de Poisson si:
1. No ocurren eventos al tiempo 0, $N(0)=0$
2. Tiene incrementos independientes
3. Tienen incrementos estacionarios
4. $P(N(t)=n)=\frac{(\lambda t)^{n}}{n!} e^{-\lambda t} \rightarrow$ Poisson homogeneo o estacionario

Se usa, ocurrencia, tiempo de espera, tiempo entre ocurrencia $N(t)\approx Poiss(\lambda)$ El tiempo de espera $\rightarrow$ d.gamma. Tiempo de interarrivo $\rightarrow$ d

**Definición:** el tiempo de arribo es el tiempo entre la ocurrencia de dos eventos, es decir: 

![[Pasted image 20230401142259.png]]

y el tiempo que pasa desde que empieza a correr hasta que pasa en $T_{1}$ 

![[Pasted image 20230401142516.png]]

Tiempo de espera como distribución gamma

**Definición:** El tiempo de espera $S_{n}$ hasta la ocurrencia del n-esímo evento es: $S_{n}=T_{1}+T_{2}+\cdots +T_{n}$ 

**Preposición:** Los tiempos de interarribo $t_{n},n=1, 2, \dots,$ son variables aleatorias independites experimentalmente distribuidas $T_{n}\approx exp(\lambda),~f_{x}(t)=\lambda e^{-\lambda t}$ 

**Prueba:** 
$$P(t_{1}>t) =P(N(t)=0)=P(N(t)=0)=\frac{(\lambda t)^{n}}{n!}e^{-\lambda t}\mid_{n=0}=e^{-\lambda t}$$
$$1-p (t_{q}\leq t)=P(t_{1}>t)=e^{-\lambda t}=1-\int_{e}^{t}f_{x}(x)dx$$
$$(-\lambda e^{-\lambda t}=-f_{x}(t))-1$$
$$f_{x}(t) = \lambda e^{-\lambda t}$$

Ahora probamos esto para un tiempo igual a dos.
$$P(T_{2}> t) = \int_{0}^{\infty}P(t_{2}> t\mid t_{1}=S)\lambda~e ^{-\lambda t}~d_{s} ~~~~(Donde ~e^{-\lambda t}se~usa~para~marginalizar)$$
$$P(t_{2}>t)=\int_{0}^{\infty}P(N(t+s) - N(S)=0\mid N(s)=1)\lambda ~e^{-\lambda s}d_s$$
$$P(T_{2}> t)=e^{-\lambda t}$$
$$t_{2}\approx exp(\lambda)=\int_{0}^{\infty}P(N(t)=0)~\lambda e^{-\lambda s}d_{s}=e^{-\lambda t}\int\lambda e^{-\lambda}d_{s}=e ~\lambda^{t}$$
<div align='right'><p>23/03/2021</div>
## Tasa de ocurrencia de eventos
$N_{x}[S,S_{t}d_{s}]$ 
$lim_{sd\rightarrow 0} N_{x}[S, S-t d_{s}]\in \{0,1\}$ 

##### Tasa media de ocurrencia
$\mathbb{E}[N_{\lambda}(s,t)]=(t-s)\lambda$ 

Si tenemos N espacios de tiempo, podemos ver la distribución como poison como un conjunto de eventos Bernulli, y podemos expresarlo matematicamente como:

$$P(N_{\lambda}[t, t+\Delta]=1)\approx\lambda\Delta$$
$$P(N_{\lambda}[S,T]=n) = (\lambda\Delta)^{n}(1-\lambda\Delta)^{M-n}$$
y esta lo podemos ver de una forma binomial, como:

$$\begin{pmatrix}M \\ n\end{pmatrix}=\frac{M!}{n!(M-n)!}=(\lambda\Delta)N(1-\lambda\Delta)^{n}$$
y tenemos a $\Delta$ que es igual a:
$$\Delta = \frac{t-s}{M},~M=\frac{t-s}{\Delta}$$
y por ende tenemos:
$$(1-\lambda\Delta)~m(1-\lambda\Delta)^{-n}$$

y podemos ver lo anterior y generalizandolo para n factores como:
$$\frac{M(M-1)\cdots(M-n+1)}{m}\frac{[\lambda(t-s)]^{n}}{n!} \left(1-\frac{\lambda(t-s)}{M} \right)^{M}(1-\lambda\Delta)^{-n}$$
$$=\left(q-\frac{1}{m}\right)\left(1-\frac{2}{M}\right)\cdots\left(t-\frac{n!}{m!}\right)\frac{[\lambda(t-s)]}{m}\left(1-\frac{\lambda(t-s)}{m}\right)^{m}(1-\lambda\Delta)^{-n}=\frac{[\lambda(t-s)]^{n}}{n!}e^{-[\lambda(t-s)]}$$

y asi llegamos a la distribución de Poisson a partir de la supocicion de n eventos de bernulli

Sumpongamos: $\lambda(t)$
$$\int_{s}^{t}xd_{x}=\lambda(t-s)$$
$$M(t)=\int_{S}^{t}\lambda(x)dx$$
$$N_{x}(t)[s,t]=\frac{M(t)^{n}}{n!}e^-\mu(t)$$
$$e^{x}=\sum\limits_{n=0}^{\infty}\frac{x^{n}}{n!}=1+x+\frac{x^{2}}{2! }+\cdots~~~~w=\frac{x}{N}$$
$$e^{w}=1+w$$
$$e^{x}=(e^{w})^{N}=(1+w)^{N}=\left(1+\frac{x}{N}\right)^{N}$$
$$e^{x}=lim\left(1+\frac{x}{n}\right)^{n}$$
$$e=e^{1}=lim_{n\rightarrow\infty}\left(1+\frac{1}{n}\right)^{n}$$
$$P(N_{\lambda}(t)=n)\frac{(\lambda t)^{n}}{n!}e^{-\lambda t}~~~~Donde~k=n-1$$
$$=e^{-\lambda t}\sum\limits_{n=1}^{\infty}(\lambda t)\frac{(\lambda t)^{n-1}}{(n-1)!}=\lambda t~e^{-\lambda t}\left(\sum\limits_{n=0}^{\infty}\frac{(\lambda t)^{k}}{k!}\right)$$
y obtenemos que el valor esperado es: $\mathbb{E}=-\lambda t$ 

# Ley de espectativa total
El valor esperado de una variable se puede ver como el valor esperado de la variable dada otra
$$\mathbb{E} = \mathbb{E}[\mathbb{E}[Y\mid X]]$$

Prueba:
$$\mathbb{E}[y] = \int_{-\infty} ^{\infty} y~f_{y}(y)~dy$$

La funcion se puede escribir como una funcion marginal de probabilidad
$$f_{y}(y)=\int_{-\infty} ^{\infty}f_{xy}(x,y )dx $$

### Ley de la varianza total
La ley de la varianza total esta dado por:$Var(y)=\mathbb{E}[var(y\mid x)] + var(\mathbb{E}[y\mid x])$ 

**Prueba:**
$var(y)=\mathbb{E}[y^{2}]-\mathbb{E}[y^{2}],~\mathbb{E}[y^{2}] =var(y)+\mathbb{E}[y]^{2}$
$\mathbb{E}[y^{2}]=\mathbb{E}[\mathbb{E}[y^{2}\mid x]]$ $=\mathbb{E}[var(y\mid x)+ \mathbb{E} [y\mid x] ^{2}]=\mathbb{E}[var(y\mid x)]+\mathbb{E} [\mathbb{E}[y\mid x]^{2}]=var(y)=\mathbb{E}[var(y\mid x)]+\mathbb{E}[\mathbb{e}[y\mid x]^{2}]-\mathbb{E}[\mathbb{E}[y\mid x]]^{2}$ 
Donde: $\mathbb{E}[\mathbb{e}[y\mid x]^{2}]-\mathbb{E}[\mathbb{E}[y\mid x]]^{2}\rightarrow$ es $Var(\mathbb{E}[y\mid x])$  y por ende obtenemos $=\mathbb{E}[var(y\mid x)]+\mathbb{e}[var(y\mid x)]$

Si $s(t)$ es un proceso de Poisson compuesto $s(t)=\sum\limits_{i=1}^{n(t)}y_{i}$ desde $N(t)$ es un proceso de Poisson homogeneo y $y_{i}~(i=1,\dots, N(t))$ son variables aleatorias independientes entre si y v $N(t)$ ademas los $y_{i}$ son identicamentes distribuidos.
Se tiene que:
$a=\mathbb{E}[s(t)]=\mathbb{E}[N(t)]~\mathbb{E}[y_{i}]$
$b= var(s(t))=\mathbb{E}[N(t)]~\mathbb{E}[y_{i}]^{2}$ 

### Ley expecttiva total
$\mathbb{E}[s(t)]=\mathbb{E}[\mathbb{E}[s(t)\mid N(t)]]=\mathbb{E}\left[\mathbb{E}\left[\sum\limits_{i=1}^{N}y_{i}\mid N(t)\right]\right]=\mathbb{E}\left[\mathbb{E}\left[ \sum\limits_{i=1}^{n(t)} \mid N(t)\right] \right]=\mathbb{E}\left[ \sum\limits_{i=1}^{N(t)}\mathbb{E}\left[ y_{i}\mid N(t) \right] \right]=\mathbb{E}[N(t)~\mathbb{E}[y_{i}]]=\mathbb{E}[y_{i}]~\mathbb{E}[N(t)]$ 
#### Prueba b:
$$Var(S(t))=\mathbb{E}[var(s(t)\mid N(t))]+var(\mathbb{E}[s(t)\mid N(t)])$$
Donde:
$\mathbb{E}[var(s(t)\mid N(t))] = \mathbb{E}[N(t)var(y_i)]$
$var(\mathbb{E}[s(t)\mid N(t)]) = Var(n(t)\mathbb{E}[y_i])$ 
$\mathbb{E}[s(t)\mid N(t)]=N(t)\mathbb{E}(y_{i})$ 

Sustituyendo tenemos:
$$=var(y_{i})\mathbb{E}[N(t)]+\mathbb{E}[y_{i}]^{2}\mathbb{E}[N(t)]$$
$$=\mathbb{E}[N(t)](var(y_{i})+\mathbb{E}[y_{i}]^{2})\rightarrow\mathbb{E}[y_{i}^{2}]$$
$$Var(s(t))=\mathbb{E}[N\mid t] ~\mathbb{E}[y_{i}^{2}]=\lambda t~\mathbb{E}[y_{i}^{2}]$$

<div align='right'>Miercoles 29 marzo 2021</div>
# Proceso de Poisson Condicionales
Decimos que un proceso de conteo $N(t)\approx poiss(\Lambda)$ es condicional respecto a $\Lambda$ si $p(N(s+t)-N(s)=n\mid\Lambda=\lambda)=\frac{(\lambda t)^{n}}{n!}e^{-\lambda t}$, donde $\Lambda\approx f-x (\lambda)$. En este caso se dice que $\Lambda$ sea la tasa aleatoria de ocurrencia.

**Problema:** Calcular la media de $N(t)\approx Poiss(\Lambda), \Lambda\approx f_{x}(x)$ 
$$\mathbb{E}[N(s)]=\mathbb{E}[\mathbb{E}[N(s)\mid\Lambda]]=\mathbb{E}[\lambda t]=t\mathbb{E}[x]=t\mathbb{E}[\Lambda]$$
$$\mathbb{E}[N(s)]=t\mathbb{E}[\Lambda]$$

**Problema:** calcula la variana de $N(t)\approx Poiss(\Lambda), \Lambda\approx f_{n}(\lambda)$
$$Var(N(s))=var(\mathbb{E}[N(s)\mid\Lambda])+\mathbb{E}[var(N(s)\mid\Lambda)]=t^{2}var(\Lambda)+t\mathbb{E}[\:ambda]$$

Calculo de potencias de la exponencial $e^{x}$
$$e^{\left(\frac{y}{n}\right)}=e^{w} $$
$$\frac{e^{x+h}-e^{x}}{h}\mid_{x=0}=\frac{e^{n}-e^{0}}{h}=\frac{e^{n}-1}{h}=\frac{e^{w}-1}{w}=1$$
$$e^{x}=(e^{w})^{N}=(1+w)^{N}=\sum\limits_{k=0}^{N}\begin{pmatrix}n \\ k\end{pmatrix}w^{k}=\sum_{k=0}^{N}\begin{pmatrix}n\\ k\end{pmatrix}  \left(\frac{x}{n}\right)^{k}=\sum\limits_{k=0}^{N}1*\left(1-\frac{1}{N}\right)*\left(1 - \frac{2}{N}\right)\cdots$$
$$1\left(1 - \left(\frac{k-1}{N}\right)\right)=\sum\limits_{k=0}^{\infty}\frac{x^{k}}{k!}$$

Aproximar funcion en base a la series de taylor
$f(x)=f(x_{0})=f(x_{0})(x-x_{0})+a_{2}(x-x_{0})^{2}+a_{3}(x-x_{0})+\dots$ 
$f(x)=a_{u}+a_{1}(x-x_{0})+a_{2}(x-x_{0})^{2}+\dots$
$f(x) =2a_{2}(x-x_{0})+3a_{3}(x-x_{0})^{2}$
$f(x)=2a_{2}+3*2a_{3}(x-x_{0})+\dots$ 

$f(x)=\sum\limits_{k=0}^{\infty}\frac{f(x_{0})}{k!}-(x-x_{0})^{k}\rightarrow(e^{x})^{k}=e^{x}\mid_{x=0}=1$

$e^{x}=\sum\limits_{k=0}^{\infty}\frac{x^{k}}{k!}$ $a_{k}=\frac{f(k)(x_{0})}{k!}$ 

# Proceso de Nacimiento y muerte
Es una cadena de Markov continua $\{x(t), t,0\}$, Nacimiento:
$$P(x_{T+T}=n+1 \mid X_{T}=n)=\int_{0}^{t}\lambda ne^{-\lambda n t}dt$$
$$P(X_{T+T}=n-1\mid X_{T}=n)=\int_{0}^{t}\mu~ n~e^{-\mu~nt}dt\rightarrow muerte$$
La matriz de transicion tiene las siguietnes caracteristicas:
$$\begin{matrix} &0&1&2&3 &\dots\\ 0&0&1&0&0&\dots \\ 1&\frac{\lambda_{1}}{\lambda_{1}+\mu}&0&\frac{\lambda_{1}}{\lambda_{1}+\mu}&0&\dots \\ 2&0& \frac{\lambda_{2}}{\lambda_{2}+\mu}&0 &\frac{\lambda_{2}}{\lambda_{2}+\mu}&\dots \\ 3&0&0&\dots&\dots&\dots \\ \vdots&\vdots&\vdots&\vdots&\vdots&\vdots \end{matrix}$$

$p_{n}n+1 =\frac{\lambda_{n}}{\lambda_{n}+\mu_{n}}$
$P_{n},n-1=\frac{\mu_{n}}{\lambda_{u}+\mu_{u}}$
