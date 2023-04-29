### Maquinas de soporte
Es un modelo lineal.

Para calcular la distancia de un punto al plano lo podemos ver como:
$$dist(x,h) =|u^{T}(x-x')| $$
vamos a considerar los puntos $x_{1},\cdots, x_{N}$ y el hiperplano $h=(b,w)$ qe satisface la condición de separacion $y_{n}=+-1$
$$|w^{T}x_{n}+b|=|y_{n}(w^{T}x_{n}+b)|=y_{n}(w^{T}x_{n}+b)$$
Entonces para la distancia del punto a h es:
$$dist(x_{n},h)=\frac{y_{n}(w^{T}x_{n}+b)}{||w||}$$
luego entonces, el punto más cercano al hiperpano tiene una distancia:
$$min_{n=1,\dots,N}dist(x_{n},h) =\frac{1}{||w||}min_{n=1,\dots,N}~y_{n}(w^{T}x_{n}+b)=\frac{1}{||w||}$$
