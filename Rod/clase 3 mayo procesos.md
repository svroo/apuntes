**Defiición:** Se dice que dos eventos A y B son equivalentes si la ocurrencia de A implica B y viceversa.
**Proposición** Si los eventos A y B son equivalentes entones $P(A)=P(B)$ 

**Ejemplo:** En un experimento de arrojar una moneda en evento $A=\lbrace~cae~aguila\rbrace$ es equivalente al evento $B=\lbrace~no~cae~sol\rbrace$ 

**Ejemplo:** Si G es una función creciente en $\mathbb{R}~(G:\mathbb{R}\rightarrow\mathbb{R})$ entonces el evento $A=\lbrace X\leq x\rbrace$ es equivalente a $B=\lbrace G(X)\leq G(x)\rbrace$  donde X es una variable aleatoria.
Son funciónes equivalentes y se les puede aplicar la inversa si son funciones uno a uno.
si en A multiplicamos por G() y en B multiplicamos por $G(x)^{-1}$

Corulario.
$$P(\lbrace X\leq x\rbrace)=P(\lbrace G(X)\leq G(x)\rbrace)$$
# Método de la función inversa para generar números aleatorios.
Supongamos que tenemos una función de densidad de probabilidad $f_{x}(x)$ y queremos generar números aleatorios $X\sim f_{x}(x)$. Vamos a usar un resultado que dice, ese resultado debe ajustarse a la aproximación de la función.
$$P(X\leq x)=P(F^{-1}(X) \leq F^{-1}(x))=P(U \leq u)=\int_{-0}^{u} 1 dt=[t]_{0}^{u}=u$$
Vamos a agarrar un intervalo de 0 a 1 de una función uniformemente distribuida y vamos a mapearla usando la función de densidad
$$F(x) = \int_{-\infty}^{x}f_{X}(t)dt ~~~~F^{-1}$$
Vamos a probar que bajo un mapeo de esta naturaleza vamos a obtener el numero aleatorio.
$$\int_{-\infty}^{x}f_{x}(t)dt=F(x)=P(U\leq F(x))=P(F^{-1}(U)\leq F^{-1}(x))=P(X\leq x)=\int_{-\infty}^{x}f_{x}(t)dt$$
**Ejemplo:** Distribución exponencial 
Sabemos ue se distribuye:
$$X\sim \lambda e^{-\lambda x}$$
Lo que tenemos que obtener es el funcion de distribución acumulada:
$$F(x) = \int_{0}^{x}\lambda e^{-\lambda t} dt=\lambda\int_{0}^{x}e^{-\lambda t}dt=\lambda\left[\frac{-1}{x}e^{-\lambda t}\right]_{0}^{x}$$
$$=-[e^{-\lambda t}]_{0}^{x}=1-e^{-\lambda x}$$
como final obtenemos:
$$F(x)=1-e^{-\lambda x}=u, ~~e^{-\lambda y}=1-u$$
$$x=\frac{1}{\lambda}lim(1-u) ^{\lambda x}=ln(1-u)$$

```python 3
import numpy as np
import matplotlib.pyplot as plt

# Creamos las vatiables
u = np.random.rand(1000)
# print(u > 0)
x = -np.log(u)
x_menos = -np.log(1 - u)

# Graficamos
fig, (ax, ax1, ax2) = plt.subplots(ncols=3)
ax.hist(x, "auto")
ax.set_title("Grafica de x")
ax1.hist(u, "auto")
ax1.set_title("Grafica u")
ax2.hist(x_menos, "auto")
ax2.set_title("Grafica de log(1-u)")
plt.show()
```

