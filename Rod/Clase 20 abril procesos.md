Si tenemos $(\Omega, F)$, donde f son los subconjuntos donde hay eventos y calculamos las probabilidades y $\Omega$ cerrada por intercecciones, donde hay algebra de borel.

Tenemos también el conjunto $(\Omega, F, P)$ donde P es nuestra función de probabilidad denotada como $P:F\rightarrow[0,1]\in \mathbb{R}$ y tenemos $\Omega$ cono el elemento más grande (espacio).
Denotado como:
$$p(\Omega)=1, P(0)=0, 0\leq P(A)\leq1, A\in F$$
![[Pasted image 20230424161839.png|350]]
Probabilidad como área de un circulo.

El área donde intercecta A y B es la probabilidad condicional $P(A|B)$:
$$P(A|B)=\frac{P(A|B)}{P(A)}=\frac{P(A,B)}{P(A)}$$
Donde la variable aleatoria $X$ la podemos ver como: $X:\Omega\rightarrow\mathbb{R}$ 

Si tengo un elemento de espacio muestral $w \in\Omega$ la variable aleatoria toma un valor $w_{X}, x_{w}$. Para el caso continuo lo podemos ver como:
$$P(a\leq X\leq b)=P(\{w:a\leq x(w)\leq b\})$$
En el caso continuo tenemos densidades de probabilidades:
$$P(x\leq X\leq x+dx)=f_{x}(x)dx$$
que la funcion es lo más cercano a una probabilidad puntual.
Para una probabilidad disjunta podemos tener
$$A\cap B=0, P(A\cup B)=P(A)+P(B)$$
como union infinita de eventos tenemos la formula:
$$P(a\leq X\leq b)=\int_{a}^{b}f_{X}(x)~dx$$
### Probabilidad acumulada función de distribución
La Función de Distribución Acumulativa (**CDF**) es la función de probabilidad de que una variable X tome un valor igual o menor que otra variable x. Con CDF, puede obtener una tabla que describe la distribución de probabilidad de las variables aleatorias. Descrita con la siguiente función.
$$F(x)=\int_{-\infty}^{\infty}f_{x}(t)~dt=P(X\leq x)$$
Si se deriva obtenemos:
$$\frac{dF(x)}{dx}=f_{x}(x)$$
Donde la variable aleatoria proviene de Omega
$$X:\Omega\rightarrow D\leq Z$$
$$f(x)=P(x=k)$$
y la función de probabilidad condicional la podemos ver:
$$f_{Y|X}(y|x)=\frac{F_{X|Y}(x,y)}{F_{X}(x)}$$
**Definición:** Sean X, Y variables aleatorias discretas definidas en el mismo espacio de probabilidades con función de probabilidad condicional $F_{Y|X}$.
La esperanza condicional de $Y$ dado $X=x$ esta dada por:
$$\mathbb{E}[Y|X]=\sum\limits_{y}y~f_{Y|X}(y|x)$$
$$f_{Y|X}(y|x) = \frac{f_{x|y}(x,y)}{f_{x}(x)}$$
Proposición:
$$\sum\limits_{y}f_{Y|X}(y|X=x)=1$$
Prueba:
$$\sum\limits_{y}\frac{f_{X|Y}(y,X=x)}{f_{X}(x)}=\frac{1}{f_{x}(x)}\sum\limits_{y}f_{X,Y}(y,X=x)$$
y ya que:
$$\sum\limits_{y}f_{X,Y}(y,X=x) = Funcion~marginal(f_{X}(X=x)=f_{x}(x))$$
obtenemos:
$$\frac{f_{x}(x)}{f_{x}(x)}=1$$
