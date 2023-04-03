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

