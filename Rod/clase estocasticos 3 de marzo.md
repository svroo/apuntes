## Desigualdad de Markov

Si X es una variable aleatoria con función de densidad de probabilidad $F()$ entonces:
$$P(X\geq a)<\frac{\mathbb{E}[X]}{a} ~~~~(a<0)$$

Prueba 
$$\mathbb{E}[X] = \int_{-\infty}^{\infty} xf(x)~dx=\int_{-\infty}^axf(x)~dx+\int_{a}^{\infty}xf(x)~dx$$
si la integral evaluada de infinito a a es positivo, se lo restamos a la otra integral.

$$\int_{a}^{\infty}xf(x)~dx\leq\mathbb{E}[X]$$
En la integral se cumple que a es menor que x, si se integra, queda:
$$a\int_{a}^{\infty}f(x)~dx\leq \int_{a}^{\infty}xf(x)~dx\leq\mathbb{E}[X]$$
Esto es lo mismo que verlo como si multiplicaramos a por la función
$$\int_{a}^{\infty}af(x)\leq\int_{a}^{\infty}xf(x)~dv$$

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