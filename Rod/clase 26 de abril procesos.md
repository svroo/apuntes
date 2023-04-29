# Estrategia de  apuestas en Juegos sucesivos
**Definición:** Puedo apostar tipicamente a un evento que se va a estar repitiendo muchas veces. Un juego sucesivo es una secuencia de jugadas, donde en cada jugada hay una puesta y se puede ganar o perder la apuesta.

Vamos a usar la martingala como estrategia de apuesta.
Consideramos una variable aleatoria $Z_{1},Z_{2},\dots,Z_{i}$ que representa con probabilidad $P(Z_{i}=1)$ con triunfo y con $(1-p)(Z_{i}=-1)$ una perdida. Entonces $Z_{0}$ representa la fortuna inicial

**Definición:** Una estrategia de apuesta es una sucesión (o secuencia) de funciones $\xi_{n}=n, 1,2\dots$ donde si:
$$\xi_{n+1}=\{Z_{o}\}x\{-1,1\}^{n}\rightarrow[0,\infty)$$
Mapea una secuencia de $Z_{0}\dots, Z_{n}$ aplicando la función nos da $Z_{0},\dots,Z_{n}\rightarrow a\in([0,\infty))\in\mathbb{R}$ 
$$\xi_{n+1}=g(Z_{0},Z_{1}\dots,Z_{n})$$
Ejemplos de estrategia de apuestas
$$1.\xi_{n+1}(Z_{0},Z_{1},\dots,Z_{n})=\left\lbrace\begin{matrix}c~si~S_{n}\geq c \\ 0~si~S_{n}< c \end{matrix}\right.$$
$$2.\xi_{n+1}(Z_{0},Z_{1},\dots,Z_{n})=\alpha S_{u},0<d<1, n=0,1,2,\dots$$
$$S_{n+1}=S_{n}+Z_{n+1}\xi_{n+1}(Z_{0},\dots,Z_n)$$
si es desde el paso 0
$$S_{n+1}=Z_{0}+\sum\limits_{i=1}^{n+1}Z_{i}\xi_{i}(Z_{0},\dots,Z_{i-i})$$
$$3.\xi_{n+1}(Z_{n})$$
se fija una ganacia c $\xi_{n+1}=2^{n}C$
**Nota:** Si en el juego n-esimo se apuesta $c2^{n}$ y se gana se obtiene una ganancia global (fortuna) de C
**Nota:** T variable aleatoria que representa el número de jugadas para obtener el primer triunfo $P(T<\infty)=1$, se distribuye de forma geometrica $T\approx Geo(P)~~ P(T=k)(1-p)^{k-1}p$.

<div align='right'><p>27/04/2023</p></div>
# Fortuna acumulada hasta la jugada n
$$S_{n+1}=S_{n}+Z_{n+1}\xi_{n+1}(Z_{0},\dots,Z_{n}), ~~~S_{n+1}=S_{0}+\sum\limits_{i=1}^{n+1}Z_{i}\xi_{i}(Z_{0},\dots,Z_{i-1})~~P(Z_{n}=1)P~para~n\in\mathbb{N}$$
El valor esperado lo tenemos como:
$$\mathbb{E}[Z_{n+1}]=1*p+(-1)(1-p)=p+p-1=2p-1$$

**Proposición:** Sea $\lbrace\xi:n=1,2,\dots\rbrace$ una estrategia de apuesta arbitraria y $S_{n}$ la fortuna acumulada hasta el juego n
$$a.Si,p=\frac{1}{2},entonces~\mathbb{E}[S_{n+1}|S_{n},\dots,S_{0}]=S_{n}$$
$$b. Si, ~p\geq \frac{1}{2}~entonces~\mathbb{E}[S_{n+1}|s_{n},\dots, S_{0}]\geq S_{n}$$
$$c. Si~p\leq\frac{1}{2},~entonces~~\mathbb{E}[S_{n+1}|S_{n},\dots,S_{0}]\leq S_{n}$$

Dado que:
$$1.\mathbb{E}[C_{i}Y_{i}+\cdots+C_{n}Y_{n}|X]=c_{i}\mathbb{E}[X_{i}|x]+\cdots+C_{n}\mathbb{E}[X_{n} |X]$$
$$2. \mathbb{E}[Y|X]=\mathbb{E}[Y|H(X)]$$
$$3.\mathbb{E}[h(x)Y|X]=h(x)\mathbb{E}[Y|X]$$
$$4.\mathbb{E}[Y|X]=\mathbb{E}[Y],~~X~~independiente~~de ~~Y$$

**Demostración:**
$$\mathbb{E}[S_{n+1}|S_{n},\dots,S_{0}]=\mathbb{E}[S_{n+1}+Z_{n+1}\xi_{n+1}(Z_{0},\dots,Z_{n})|Z_{n},\dots,Z_{0}]$$
$$=\mathbb{E}[S_{n}|Z_{n},\dots,Z_{0}]+\mathbb{E}[Z_{n+1}\xi_{n+1}(Z_{=},\dots,Z_{n})|Z_{n},\dots,Z_{0}]$$
$$=\mathbb{E}[S_{n}]+\xi_{n+1}(Z_{0},\dots,Z_{n})\mathbb{E}[Z_{n+1}|Z_{n},\dots,Z_{0}]$$
$$=S_{n}+\xi_{n+1}(Z_{0},\dots,Z_{n})\mathbb{E}[Z_{n+1}]=S_{n}+\xi_{n+1}(Z_{0},\dots,Z_{n})(2-1)$$
$$\mathbb{E}[S_{n+1}|S_{n},\dots,S_{0}]=S_{n}+\xi_{n+1}(Z_{0},\dots,Z_{n})(2p-1)$$

y dado eso quedan probadas los tres puntos anteriores.

**Definición:** Sea X,Y $X=\lbrace X_{n}:n=0,1,2,\dots,\rbrace~~Y=\lbrace Y_{n}:~n=0,1,2,\dots\rbrace$ procesos estocasticos discretos, decimos que Y es una martingala respecto a X, si para todo $n$ 
$$\mathbb{E}[|Y_{n}|]<\infty,~\mathbb{E}[Y_{n+1}|X_{n},\dots,X_{0}]=Y_{n}$$
va a ser su martingala si
$$\mathbb{E}[Y_{n+1}|X_{n},\dots,X_{0}]\geq(Y~es~sub~martigala~respecto~de~X)$$
$$\mathbb{E}[Y_{n+1}|X_{n},\dots,X_{0}]\leq(Y~es~super~martigala~respecto~de~X)$$

