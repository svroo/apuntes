Comenzamos por definir la distribución de Poisson como:
$$P(X = k) = \frac{(\lambda^k * e^-\lambda)} {k!}$$
donde λ es la tasa media de ocurrencia de eventos en un intervalo dado, y k es el número de eventos que ocurren en ese intervalo.

Ahora, para encontrar el valor esperado de la distribución de Poisson, utilizamos la definición del valor esperado, que es:
$$\mathbb{E}(x)=\sum\limits_{n=0}^{\infty}(x * P(X = x))$$
donde la suma se realiza sobre todos los posibles valores de X.

Para simplificar esta expresión, podemos reemplazar P(X = x) con su definición, y luego agrupar términos similares para obtener:
$$\mathbb{E}(x)\sum\limits_{n=0}^{\infty}\left(k * \frac{(\lambda^{k} * e^{-\lambda})} {k!}\right)$$
A continuación, podemos utilizar la identidad matemática:
$$\sum\limits\left(k * \frac{(\lambda^{k} * e^{-\lambda})}{k!}\right) = \lambda * e^{-\lambda} * \sum\limits(k-1) * \left(\frac{\lambda^{k-1}} {(k-1)!}\right)$$