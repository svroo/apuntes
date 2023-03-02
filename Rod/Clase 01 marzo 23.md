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

# Ejercicio calcular varianza de puason

