Este método usa los ejes cordenados como direcciones de busqueda, consideramos $f:\mathbb{R}^{n}\rightarrow\mathbb{R}$, más especificamente $d_{1},\dots,d_{n}$ son las direcciones de busqueda desde $e_{i}=d_{i},~~i=1,\dots,n$ 

##### Algoritmo:
Inicialización: Escoja $\epsilon>0$, para su usado como criterio de paro por el algoritmo, y sea $d_{i},\dots,d_{n}$ la dirección coordenada. Escoja un punti inicial $X_{i}$ y sea $Y_{i}= x_{i}$, sea $K=j=1$, enseguida vaya al paso principal:
$$y_{1}=x_{1}$$
$$y_{2}= x_{1}+\lambda_{1} d_{1}$$
$$y_{3}= y_{2}+\lambda_{2}d_2$$
$$\vdots$$
$$x_{2}=y_{n}=y_{n-1}+\lambda_{n-1}+d_{n-1}$$

Paso principal
1. Sea $\lambda_j$ una solución óptima al problema de minimización $f(y_{j}+\lambda~d_{j})$  sujeto a $\lambda\in\mathbb{R}$, y sea $Y_{j+1}=j_{j}+\lambda_{j}d_{j}$ si $j<n$, reemplazamos j por $j+1$ y repita el paso 1
2. Consideramos $X_{k+n}$ si $\mid\mid~X_{k+1}-X_{k}\mid\mid<\epsilon$. De otra forma $Y_{1}=X_{k+1}$ sea $j=1$, reemplaze k por $k+1$ y vaya al paso 1

###### Nota:
En el algoritmo anterior se puede establecer un hallazgo de paso máximo.

### Algotimo de Hooke-Jackie

$$x_{1}=y_{1}$$
$$y_{2}= x_{1}+\lambda_{1} d_{1}$$
$$y_{3}= y_{2}+\lambda_{2}d_2$$
$$\vdots$$
$$x_{2}=y_{n}=y_{n-1}+\lambda_{n-1}+d_{n-1}$$
Con una d adicional

$$d=x_{2}-x_{1}$$
$$y_{1}=x_{2}+\lambda~d$$

##### Paso inicial
Esoja $\epsilon>0$ para ser usado como criterio de paro. Escoja un punto lineal $x_{1}$ y sea $y_{i}= x_{1}$, sea $k=j=1$. Vaya al paso 1.
1. Sea $\lambda_{j}$ una solución óptima al problema de minimización $f(y_{1}+\lambda~d_{j})$ sujeto a $\lambda\in\mathbb{R}$ y sea $y_{j+1}=y_{j}\lambda_{j}d_{j}$. Si $j<n$ reemplaze j por $u'+1$ y repita el paso 1. De otra forma si $j=n$ sea $x_{k+n}=y_{n+1}$ si $\mid\mid X_{k+1}-x_{k}\mid\mid<\epsilon$  preestableces un medio de otra forma vaya al, paso dos
2. Sea $d=x_{k+1}-X_{k}$ y sea $\hat{\lambda}$ una solución óptima al problema de minimización


### 8.6.1 Lema
Supongamos que $t\mathbb{R}^{n}\rightarrow\mathbb{R}$ es diferenciable en X y supongamos que $\forall~f(x)(x)\neq0$.Entonces habra que minimizar.

###### Demostación:
De la diferenciabilidad de t en x, se elije que:
$$F(x;d)=lim_{\lambda\rightarrow0^{t}} \frac{f(x+\lambda~d)-f(x)} {\lambda}=\Delta~f(x)^{t}d$$
$$\{x+\lambda~d\mid\lambda\in\mathbb{R}\}$$

luego el problemasereduce a minimizar $\Delta~f(x)^{t}d$ sujeto a $\mid\mid~d\mid\mid\leq1$. De la desigualdad de schwartz, para $\mid\mid d\mid\mid\leq1$ tenemos:

$$\mid\Delta f(x)^{t}.d\mid\leq\mid\mid\Delta f(x)\mid\mid~~\mid\mid d\mid\mid'$$

$$=-\Delta f(x)^{t}.d\leq\mid\mid\Delta f(x)\mid\mid~~\mid\mid d\mid\mid$$
$$=\Delta f(x)^{t}.d \geq -\mid\mid\Delta f(x)\mid\mid~\mid\mid d\mid\mid~\geq-\mid\mid\Delta f(x)\mid\mid$$

Observe que 
$$\overline{d}=\frac{\Delta f(x)}{\mid\mid\Delta f(x)\mid\mid}$$
luego
$$\Delta f(x)^{t}\overline{d}=\frac{-\mid\mid\Delta f(x)\mid\mid^{2}}{\mid\mid\Delta f(x)\mid\mid} = -\mid\mid\Delta f(x)\mid\mid$$
luego d es el vector
Luego el problema se reduce a minimizar $\Delta f(x)^{t}$

#### Paso inicial
Sea $\epsilon>0$, el número utilizado como criterio de paro. Escoja un punto inicial $x_{1},~sea~k=1$ vaya al paso principal.

##### Paso principal
Si$\mid\mid\Delta f(x_{u})\mid\mid<\epsilon$ pare de otra forma, sea $d_{k}=-\Delta f(x_{k})$ y sea $\lambda_k$ una solución óptima al problema de minimización.
$$f(x_{k}+\lambda d_{k})~~sujeto~a~\lambda\geq0$$
Sea $x_{k+1}=x_{k}+\lambda_{k}d_{k}$, reemplaze k por $k+1$ y repita el paso principal


## Método de Newton
Consideremos $f:\mathbb{R}^{n}\rightarrow\mathbb{R}$ y $q(x)$ la proximación de segundo orden de $f(x)$ en $x_{i}$, es decir 

$$q(x)=f(x_{k})+\Delta f(x_{k})^{t}(x-x_{k})+\frac{1}{2}(x-x_{k})^{t}H(x_{k})(x-x_{k})$$

Una condición necesaria para un minimo de q es que $\Delta q(x)=0$ o que $\Delta~f(x_{k})+H(x_{k})(x-x_{k})=0$ 

Asmiendo que la inversa de $H(x_{k})$ existe, el punto $x_{K+1}$, esta dado por:

$$x_{k+1}=x_{k}=H(x_{k}^{-1}\Delta~f(x_{k}))$$

###### Nota:
