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

<div align='right'><h4>14/12/2022</h4></div>
1. $xk$ 
2. dk
3. $\lambda K$
4. $x_{\lambda~k}=x_{\mu}+\lambda_{\mu}dk$ 

Se van a realizar algoritmos de busqueda lineal de la forma:
$min~f(x) \rightarrow f:~\mathbb{R}^{n} \rightarrow \mathbb{R}$ $x\in C$ 

Investigar que es una matriz cuasiconvexa

#### Teorema 8.1.1
Sea $\theta:\mathbb{R}\rightarrow \mathbb{R}$ una función cuasiconvexa sobre el intervalo $[a,b]$, Sea $\lambda,~\mu t[a,b]$ tal que $\lambda<\mu$. Si $\theta(\lambda)>\theta(\mu)$; entonces $\theta(Z)\geq \theta(\mu)~~\forall~z\in[a,\lambda]$. Si $\theta(\lambda)\leq\theta(\mu)$ entonces $\theta(Z)\leq\theta(\lambda)~\forall~Z\in(\mu,b]$.

El resultado anterior (8.1.1) da lugar al método de busqueda uniforme. Consideramos los puntos:
$$t_{i}= a+i\frac{b-a}{n},~~i=0,\dots,n$$
a la que llamaremos $\hat{\lambda}=min~\theta(t_{i})$  

### Busqueda dicotómica
Consideramos $\theta : \mathbb {R} \rightarrow \mathbb{R}$ la función a minimizar sobre el intervalo $[a,b]$. Supongamos que $\theta$ es estrictamente cuasiconvexa consideramos dos puntos $\lambda_{i}$ y $\mu_{i}$ en virtud de el nuevo intervalo de incertidumbre es $[a_{i},\mu_{i}]$ si $\theta(\lambda_{i})<\theta(\mu_{i})$ y si $\theta(lambda_{i})>\theta(\mu_{i})$ entonces el nuevo intervalo de incertidumbre es $[\lambda_{i}, b_{i}]$. Sin embargo no sabemos a priori la colocación de $\lambda_{i},\mu_{i}$, pero se puede demostrar que dicha colocación debe ser simétrica respecto del origen.

#### Algoritmo de busqueda dicotomica.
Inicialización, Escoje una constante $2~\epsilon>0$ y defina la longitud de incertidumbre final como $\ell>0$. Sea $[a,b_{i}]$ el intervalo inicial de incertidumbre, sea $k=1$, vaya al paso principal

##### Paso principal
1. Si $b_{k}-a_{k} < \ell$ para el punto mínimo cae en el intervalo $[a_{ki}, b_{k}]$. De otra forma, considere $\lambda_{k}$ y $\mu_{k}$ definida como sigue:
$$\lambda_{k}=\frac{a_{b}+b_{k}}{z} - \epsilon,~~~\mu_{k}=\frac{a_{k}+b_{k}}{z} + \epsilon$$
2. Si $\theta(\lambda_{k})<\theta(\mu_{k})$, sea $a_{k+1}=a_{k}$ y $b_{k+1}=\mu_{k}$ De otra forma $a_{k+1}=\lambda_{x}$ y $b_{k+1}=b_{k}$. Reemplaze k por $k+1$ 
**Nota:** La longitud del intervalo de incertidumbre en el paso $k+1$ es:
$$b_{k+1}-a_{k+1} = \frac{1}{2^{k}}(b_{i}-a_{i}) + 2~\epsilon(1-\frac{1}{2^{k}})$$
entonces quedaria de la siguiente manera:
$$\frac{b-a}{2}$$ 
### Método de la sección dorada
Para comparar los métodos de busqueda lineal utilizaremos el siguiente radio:

$$r(\nu) =\frac{longitud~del~intervalo~de~incertidumbre~después~de~\nu~observaciones}{longitud~del~intervalo~de~incertidumbre~antes~de~tomar~las~observaciones}$$

En la iteración general k del método, consideramos el intervalo de incertidumbre como $[a_{n},b_{k}]$. Utilizamos nuevamente el terorema 8.1.1, el nuevo intervalo de incertidumbre $[a_{k+1},b_{k+1}]$ esta dado por $[\lambda_{k},~b_{k}]$ si $\theta(\lambda_{k})>\theta(\mu_{k})$ y $[a_{k},~\mu_{k}]$ si $\theta(\lambda_{k})\leq\theta(\mu_{k})$. Los puntos $\lambda_{k}$ y $\mu_{k}$ son seleccionados de la siguiente forma.

1. La longitud del nuevo intervalo de incertidumbre $b_{k+1}-a_{k+1}$ no depende del resultado de la k-ésima iteración, esto es, si$\theta(\lambda_{k})>\theta(\mu_{k})$ o $\theta(\lambda_{k})\leq\theta(\mu_{k})$. Por tanto debemos tener $b_{k}-\lambda_{k}=\mu_{k}-a_{k}$ 
2. Asi $\lambda_{k+1}$ y $\mu_{k+z}$ son seleccionadas con el proposito de que en una nueva iteración $\lambda_{k+1}$ coincida con $\mu_{k}$ o $\mu_{k+1}$ concida con $\lambda_{k}$. Si esto puede ser realizado, entonces durante la iteración $k+1$ solo una observacion extra es nesesaria.

#### Caso 1.
$\theta(\lambda_{k})>\theta(\mu_{k})$. En este caso $a_{k+1}= \lambda_{k}$ y $b_{k+1}=b_{k}$. Para satisfacer que $\mu_{k}=\lambda_{k+1}=a_{n+1}+(1-\alpha)(b_{k+1}-a_{k+1}) = \lambda_{k} + (1-\alpha)(b_{k}-\lambda_{k})$ 

8.1 : $\lambda_{k}=a_{k}+(1-\alpha)(b_{k}-a_{k})$ 
8.2 : $\mu_{k}= a_{k}+\alpha(b_{k}-a_{k})$

Sustituyendo las expresiones de $\lambda_{k}$ y $\mu_{k}$ de 8.1 y 8.2:

$$a_{k}+\alpha (b_{k}-a_{k})=a_{k}+(1-\alpha) (b_k-a_{k}) + (1-\alpha) (b_{k}-a_{k}-(1-\alpha)(b_{k}-a_{k}))$$

$$=(1-\alpha)[(b_{k}-a_{k})+(b_{k}-a_{k})-(1-\alpha)(b_{k}-a_{k})] = (1-\alpha)[(b_{k}-a_{k})(1+\alpha )]$$

$$\alpha=1-\alpha^{2}\rightarrow \alpha^{2}+\alpha-1 = 0~~luego~~\alpha=0.618$$

De manera analoga en el caso 2 se obtiene la misma ecucación para $\alpha$ 

#### Algoritmo de sección dorada
**Inicialización:** Escoja una longitud admisible en el intervalo $\{a_{1},~b_{1} \}$ el intervalo de incertidumbre inciial y sea $\lambda_{i}=a_{i}+(1-\alpha)(b_{i}-a_{i})$ y $\mu_{i}= a_{i}+\alpha(b_{i}a_{i})$, donde $\alpha = 0.618$. Entre $\theta(\lambda_{i})$ y $\theta(\mu_{i})$, sea $k=1$ vaya al paso principal


###### Paso principal
1. Si $b_{k}-a_{k}<\ell$ pare, la solución optima cae en eintervalo $[{a_{k},b_{k}}]$. De otra forma, si $\theta(\lambda_{k})>\theta(\mu_{k})$ vaya al paso 2; y si $\theta(\lambda_{k})\leq\theta(\mu_{k})$ vaya al paso 3
2. Sea $a_{k+1}=\lambda_{k}$ y $b_{k+1}=b_{k}$ y además.. $\lambda_{k+1}= \mu_{k}$ y $\mu_{k+1}=a_{k+1}+\alpha(b_{k+1}-a_{k+1})$. Evalues $\theta(\mu_{k+1})$ vaya al paso 4
3. Sea $a_{k+1}= a_{k}$ y $b_{k+1}=\mu_{k}$, con $\mu_{k+1} = \lambda_{k}$ y sea $\lambda_{k+1}= a_{k+1}+(1-\alpha)(b_{k+1}-a_{k+1})$. Evalue $\theta(\lambda_{k+1})$ y vaya al paso 4.
4. Reemplace k por $k+1$ y vaya al paso 1.

|Minimize|$\lambda^{2}+2\lambda$|
|---|--|
| |$-3\leq\lambda\leq5$|
(pagina 351)

[[Matematicas avanzadas]] 