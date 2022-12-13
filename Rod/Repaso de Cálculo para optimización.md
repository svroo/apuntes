Libreria a usar: **sympy**

#### Gradiente, Jacobiano y Hessiano.
Calcular la derivada parcial de una función que depende de varias variables (v.a (con respecto a)) una variable, corresponde a calcular la derivada de la función respecto a esa variable asumiendo las demas constantes. Esto es;

$$\frac{\partial~f(x)}{\partial~x_{i}} = lim~\frac{f(x+he_{i}) - f(x)}{h}~~~~h\rightarrow0$$

El operador gradiente
$$f(x)=\begin{bmatrix} \frac{\partial f(x)}{\partial~x_{1}} \\ \frac{\partial~f(x)}{\partial~\partial~x_{2}}\\ \vdots \\ \frac{\partial~f(x)}{\partial~x_{n}} \end{bmatrix}$$

#### La matriz Jacobiana
$$J_{f}=^{def} \begin{bmatrix} \frac{\partial~f(x)}{\partial~x_{i}},& \frac{\partial~f(x)}{\partial~x_{2}}, &\dots, & \frac{\partial~f(x)}{\partial~ x_{n}} \end{bmatrix}$$
y por ultimo la matriz Hessiana:

$$H_{f}= J\{\Delta~f \} = J\{J_{f}^{T}\} = \begin{bmatrix}  \frac{\partial^{2}f}{\partial~x_{1}^{2}} & \frac{\partial^{2}}{2x_{1}\partial~x_{2}} &\dots&\frac{\partial^{2f}}{\partial~x_{i}~\partial~x_{n}} \\ \frac{\partial^{2}}{\partial~x_{2}\partial~x_{1}} & & &\vdots \\ \vdots & & &\vdots \\ \frac{\partial^{2}f}{\partial~x_{n}\partial x_{1}}&\dots&\dots & \frac{\partial^{2}f}{\partial~x_{n}\partial~x_{i}} \end{bmatrix} = \begin{bmatrix} \frac{\partial~f}{\partial~x_{i}\partial~x_{j}} \end{bmatrix}^{2}~~i,j=1$$

$x_{i}^{3}+(x_{1}-x_{2})^{2}= f(x_{1},x_{2})$ 

#### Optimización Convexa
Definición Un conjunto $\Omega\in\mathbb R^{n}$ es un conjunto convexo si:
$$\alpha~x+(1-\alpha) yf~\Omega$$
$$\forall~x_{1}~y~t\Omega~y~\forall~\alpha\in~[0,1]$$
##### Definición:
$f:\Omega\rightarrow\mathbb{R}$ es una función convexa si $\forall~\alpha\in~(0,1)$ y $\forall~x_{1}~y~t~\Omega$:
$$\alpha~f(x)+(1-\alpha)~f(y)\geq~f(\alpha~x+(1-\alpha)~y)$$

##### Definición:
Se bice que una funcion f tiene un punto mínimo (máximo) global en S. Si existe $um~\vec{x}^{*}\in~S$ que $f(\vec{x}^{*})\leq f(\vec{x})~\forall~\vec{x}\in S$ $\mid$ $f(\vec{x}^{*})\geq f(\vec{x})~\forall~\vec{x}\in S$ 

##### Definición:
Se dice que f tiene un mínimo (máximo) local en S sí existe $\delta>0$.
$f(\vec{x})\geq~f(\vec{x}^{*})~\forall\vec{x}\in\forall\delta(\vec{x}^{*})$  $\mid$ $f(\vec{x})\leq~f(\vec{x}^{*})~\forall\vec{x}\in\forall\delta(\vec{x}^{*})$ 

Diremos que f admite un punto extremo en S, si f tiene un mínimo o un máximo local en S.

#### Condiciones de primer orden
###### Definición:
Supongamos que f es diferenciable en S, un abierto de $\mathbb{R}^{n}$, diremos que f admite un punto crítico en $\vec{x}^{*}$ en S. Si:
$$\frac{\partial~f(\vec{x}^{*})}{\partial~x_{j}} = 0~~~\forall j=1,\dots,n$$
###### Teorema:
Supongamos que f es continuamente diferenciable con S, un abierto de $\mathbb{R}^{n}$, y que tienen un punto extremo en $\vec{x}^{*}~\in~S~\rightarrow\frac{\partial~f(\vec{x}^{*})}{\partial~x_{j}} = 0~~~~~\forall~j=1,\dots,n$ 

###### Definición:
Una matriz H es positiva definida ($H\in\mathbb{R}^{n}$)($H\in M_{nxn}(\mathbb{R})$) es postivia semidefinida si sucede lo siguiente:
$$\vec{x}^{t}~H\vec{x}\geq0~~~~~\forall~\vec{x}\in\mathbb{R}^{n}$$
y analogamente negativa semidefinida si:
$$\vec{x}^{t}~~H~\vec{x}\leq 0~~~~~\forall~\vec{x}\in\mathbb{R}^{n}$$

###### Teorema:
Sea $f:S\leq\mathbb{R}^{n}\rightarrow \mathbb{R},S$ abierto y $f\in \zeta^{2}(S)$. Si $\vec{x}^{*}$ es un punto crítica de f en S y si el Hebiano de f evaluado en $\vec{x}^{*}$ $(H_{t}(\vec{x}^{*}))$ es positiva definida entonces f tiene un mínimo local en $\vec{x}^{*}$. Por otra parte si $H_{t}~(\vec{x}^{*})$ es negativo definido $\vec{x}^{*}$ es máximo local.
