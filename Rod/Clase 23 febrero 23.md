# Libro
Time series analysis and it's applications with R examples

# Measures of Dependence
Una completa descripción de una serie de tiempo, es una coleccion de variables aleatorias con puntos arbitrarios de tiempo $t_{1}, t_{2,}\cdots, t_{n}$ for cada posible entero positivo n, is provided by the joint distribution fuction, evaluated as the probability that the values of the series are jointly less than the n constants $c_{1}, c_{2}, \cdots, c_{n}$ it is.

$$F_{t_{1},\cdots, t_{n}}(c_{1},\cdots,c_{n})=Pr(X_{1}\leq c_{1},\cdots, X_{n}\leq c_{n})$$

Although the joint distribution fuction describes the data completely, it is an unwieldy tool for displaying and analyzing time series data. 

## El valor esperado
El valor esperado de una vareable aleatoria con un numero finito de salidas. En el caso de 

$$\mu X_{1}= \mathbb{E}[X_{t}] = \int_{x=-\infty}^{\infty}$$

### Valor esperado para algunos modelos estadisticos
Ejercicio.
Asume que el ruido blanco $W_{1}$ ~ $N(0,\sigma_{w})$ y despues compute:
1. El valor esperado de medias mobiles esta definido por:
$$V_{t}= \frac{1}{3}(W_{t-1}+W_{t}+W_{t+1})$$
Se resolveria:
$$\mathbb{E}[V_{t}] = \int_{v=-\infty}^{\infty}v~f(v_{t}< v)~dv$$
Reemplazando con la función, quedaria:

$$\mathbb{E}[V_{t}]=E\left[ \frac{1}{3}W_{t-1} + \frac{1}{3}W_{t} +\frac{1}{3}W_{t+1}\right]$$

sin integral quedaría:

$$\mathbb{E}[V_{t}] = \mathbb{E} \left[\delta t+\sum\limits_{\delta=1}^{j}w_{j}\right]$$
$$=\mathbb{E} [\delta t] +E\left[ \sum\limits_{j=1} ^{t}W_{t}\right]$$
$$\delta t+\sum\limits_{\delta=1}^{t}\mathbb{E}[W_{j}]\rightarrow ~se~hace~0$$

### Autocovarianza
The autocovariance function measures the lineal dependence between two point on the same series observed at different times, and it is defined as:
$$\gamma x(s,t)=\gamma x(t,s) = cov(X_{s},X_{t})=\mathbb{E}[(X_{s}-\mu_{s})(X_{t}-\mu_{t})]$$
Se remplaza como el valor esperado de la varianza:
$$\mathbb{E[(X_{t}-\mu_{t})^{2}]}$$

##### Ejercicio 
Asuma que todo ruido blanco $W_{i}$~$N(0,\sigma_w)$ 
1. Compute la autocovarianza del modelo del ruido blanco

$$Cov(W_{s},W_{t}) = \mathbb{E}[W_{s}* W_{t}]=\int_{w_{s}=-\infty}^{\infty}\int_{w_{t}=-\infty}^{\infty}(W_{s}=w_{s})~(W_{t}=w_{t}) ~N(0,\sigma_{ws})~N(0,\sigma_{wt})dw$$
$$=\mathbb{E}[W_{s}]~\mathbb{E}[W_{t}]=0$$
Como el valor esperado del ruido blanco es 0, entonces 0 * 0 = 0

2. Comprueba la igualdad escrita debajo the la autocoracianza de las medias mobiles:
$$Cov=(V_{s},V_{t}) = cov\left(\frac{1}{3}(W_{s-1}+W_{s}+W_{s+1}),\frac{~1}{3} (W_{t-1}+W_{t}+W_{t+1}) \right) =\left\lbrace\begin{matrix}\frac{3}{9} \sigma^{2}w& s=t  \\ \frac{2}{9}\sigma^{2}w&\mid s-t\mid =1 \\ \frac{1}{9}\sigma^{2}w&\mid s-t\mid = 2 \\ 0&\mid s-t\mid >2\end{matrix}\right.$$

$$\mathbb{E} \left[\left(\frac{1}{3}W_{s-1}+\frac{1}{3}W_{s}+\frac{1}{3}W_{s+1} \right) \left( \frac{1}{3}W_{t-1}+\frac{1}{3}W_{t}+ \frac{1}{3}W_{t+1}\right) \right]$$
se multiplican cada uno de los elementos por el otro.

## Autocorrelación
La función de autoocorrelacion mide la prediccion lineal de las series de tiempo t, dicho $X_{t}$, usando una sola valiable de tiempo s, digamos $X_{s}$ y esta definida como:

$$-1 \leq P_{x}(s,t)=\frac{\gamma X(s,t)}{\sqrt{\gamma X(s,s) \gamma X (t,t)}} \leq 1$$

Utilizando la desigualdad de Cauchy-Schwarz establece que dadas dos variables aleatorias, X y Y, con una probabilidad common, entonces:
$$\mid\mathbb{E}\mid XY\mid\mid \leq\sqrt{ \mathbb{E} [X^{2}] \mathbb{E} [Y^{2}]} $$
$$=P(s,t) = $$