## Binomio de Newton extendido 
El binomio de Newton es una fórmula general para expandir la potencia n-ésima de un binomio, resultando dicho desarrollo en un polinomio o bien en una serie infinita de potencias. Así mismo, se lo denomina teorema del binomio.
$$a_{0},a_{1},\dots\rightarrow Naturales$$
$$f:\mathbb{Z}\rightarrow\mathbb{R}$$
$$a(n)=a_{n}=f(n),~~n\rightarrow a_{n}$$
a mapea a $f(n)$ 
Estas secuencias demuestran secuencias de probabilidades y se puede ver como polinomio. Tenemos la función generatriz como:
$$A(x)=\sum\limits_{n=0}^{\infty}a_{k}x^{k}$$
Como nos interesa la suma aplicamos un limite
$$lim_{x\rightarrow 1} A(x)\sum\limits_{n=0}^{\infty}a_{k}$$
Calcular la media es aplicar la derivada
$$A'(x)=\sum\limits_{n=0}^{\infty}a_{k}b_{k}$$
Donde:
a = probabilidad
b = valores de la variable aleatoria

Media $(\mu)$
$$lim_{x\rightarrow 1}A'(x)=\mathbb{E}[x]$$
Calcular la probabilidad de retorno de una cmainata simple.
Secuencias de probabilidades de interes {familias}
Caminata simple como modelo financiero para retorno de inversión

### Teoria del binomio generalizado a partir de una función de Taylor
$$F(x)=(a+x)^{n}$$
Considere las derivadas, calcular k derivadas:
$$\frac{d^{k}}{d_{x}^{k}}(a+x)^{n}\mid_{x=0}= n(n-1)\dots(n(k-1))x^{n-k}$$

De forma más particular:
$$\frac{d^3}{dk^{3}}(ax)^{5}=\frac{d}{dx}\left(\frac{d}{dx}\left(\frac{d}{dx}(ax)^{5}\right)\right)$$
$$=n(n-1)(n-(k-1)(axx)^{n-k})$$
$$\frac {d^{n}}{dx}(a+x)^{x}=n(n-1)\dots(n-(n-1))a^{n-n}=n!$$
$$\frac{d^{n+1}}{dx^{n+1}}=\frac{d}{dx}\left(\frac{d^{n}}{dx^{n}}(a+x)^{n}\right)=0$$
$$f\left(x\right)=\sum\limits_{k=0}^{\infty}\frac{(a+x)^{k}}{k!} \mid_{x=0}$$
$$=\sum\limits_{k=0}^{n}=\left(\frac{n(n-1)\dots(n-(k-n))}{k!}\right)a^{n-k}x^{k}$$
$$(a+b)^{n}=\sum\limits_{k=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix}a^{n-k}b^{k}$$

### Teorema Binomio de Newton generalizado
Cuando k es igual a n, nunca k alcanza a n cuando n es una fracción o un numero negativo, $n=\alpha$ 
$$(a+x)^{\alpha}=\sum\limits_{k=0}^{\infty}\frac{\alpha(\alpha -1)\dots(\alpha -(\alpha -1))}{k!}a^{\alpha-k}x^{k}$$
$$(a+x)^{\alpha}=\sum\limits_{k=0}^{\infty}\begin{pmatrix}\alpha \\ k\end{pmatrix} a^{\alpha-k}~x^{k}$$
$$(a+x)^{\alpha}=\sum\limits_{k=0}^{\infty}\begin{pmatrix}\alpha \\ k\end{pmatrix} a^{\alpha-k}~b^{k}$$

Calcular
$$\begin{pmatrix}2n \\ n\end{pmatrix} \frac{(2n)!}{(2n-n)!~n!}=\frac{(2n)!}{n!~n!}=\frac{(2n)(2n-1)\dots 4, 3, 2, 1}{(n! ~n!)}$$
Se divide en pares y nones
$$\frac{\prod_{k=0}^{n-1}(2n-2k)\prod_{k=1}^{n}(2n-(2k-1))}{n! ~n!}$$
$$\frac{\left[\frac{2^{n}\prod_{k=0}^{n-1}(n-k)}{n!} \right] \left[2^{n}\prod_{k=1}^{n}(n-(k-1))\right]} {n!~n!}$$
$$\begin{pmatrix}2n \\ n\end{pmatrix}=\frac{2^{4}}{2^{n}}2^{n}2^{n}\prod_{k=1}^{n}\frac{(2n-(2k-1))}{2}=4^{n}\prod_{k=1}^{n}\left(n-\left(k-\frac{1}{2}\right)\right)$$
