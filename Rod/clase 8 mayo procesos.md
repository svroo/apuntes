# Método de aceptación y rechazo para generar variables aleatorias.
Tenemos una forma de generar una variable aleatoria $y\sim g$  y se desea generar una variable aleatoria $X\sim F$ 
## Algoritmo
(se pide $f(x)\leq Mg(x)$)
1. Se genera y de acuerdo a $Y\sim g$ y con valor u respecto a $U\sim U(0,1)$ (Nota. Y y U son independientes)
2. Se $u\leq\frac{f(u)}{Mg(y)}$  para $M>1$ entonces $X=Y$ en caso contrario continua en el paso 1.

$$h(u,y)=1\cdot g(y)=g(y)$$
### Demostración 
$$P(X\leq x)$$
queremos demostrar que mediante la integral es una funcion de densidad, lo podemos escribir como:
$$P(X\leq x)= P\left(Y\leq x\mid U\leq \frac{f(y)}{Mg(y)}\right)$$
lo podemos ver como un cociente de probabilidad, (la y minuscula es la que muestreamos en el algoritmo):
$$=\frac{P\left(Y\leq x, U\leq\frac{f(y)}{Mg(y)}\right)} {P\left(U\leq \frac{f(y)}{mg(y)}\right)}$$
Primero calculamos:
$$P\left(Y\leq y,U<\frac{f(y)}{Mg(y)}\right)=\int\int h(y,y)~d_{u}d_y=\int_{-\infty}^{y=x}\left(\int_{0}^{\frac{f(x)}{Mg(x)}}g(y)~d_{u}\right)d_{y}$$
Sacamos la g(y):
$$\int_{-\infty}^{y=x} g(y)\left(\int_{0}^{\frac{f(x)}{Mg(x)}}~d_{u}\right)d_{y}=\int_{-\infty}^{x}[u]_{0}^{\frac{f(x)}{Mg(x)}} g(y) d_{y}=\int_{-\infty}^{x}\left({\frac{f(x)}{Mg(x)}}\right)g(y)d_{y}x$$
$$=\frac{1}{M}\int_{-\infty}^{x}f(n)d_{y}=\frac{1}{M}F(x)$$
$$P\left(U\leq \frac{f(x)}{Mg(x)}\right)=\int\int g(u,y)d_{x}d_{y}=\int_{-\infty}^{\infty}g(x)\left(\int_{0}^{\frac{f(x)}{Mg(x)}}du\right)d_{x}=\frac{1}{M}\int_{-\infty}^{\infty}f(y)d_{y}=\frac{1}{M}$$
Si:
$$\int_{-\infty}^{\infty}f(y)d_{y}$$
da uno, entonces solo nos queda 
$$\frac{1}{M}$$
