# Ley de espectativa total
El valor esperado de una variable se puede ver como el valor esperado de la variable dada otra
$$\mathbb{E} = \mathbb{E}[\mathbb{E}[Y\mid X]]$$

Prueba:
$$\mathbb{E}[y] = \int_{-\infty} ^{\infty} y~f_{y}(y)~dy$$

La funcion se puede escribir como una funcion marginal de probabilidad
$$f_{y}(y)=\int_{-\infty} ^{\infty}f_{xy}(x,y )dx $$

### Ley de la varianza total
La ley de la varianza total esta dado por:$Var(y)=\mathbb{E}[var(y\mid x)] + var(\mathbb{E}[y\mid x])$ 

**Prueba:**
$var(y)=\mathbb{E}[y^{2}]-\mathbb{E}[y^{2}],~\mathbb{E}[y^{2}] =var(y)+\mathbb{E}[y]^{2}$
$\mathbb{E}[y^{2}]=\mathbb{E}[\mathbb{E}[y^{2}\mid x]]$ $=\mathbb{E}[var(y\mid x)+ \mathbb{E} [y\mid x] ^{2}]=\mathbb{E}[var(y\mid x)]+\mathbb{E} [\mathbb{E}[y\mid x]^{2}]=var(y)=\mathbb{E}[var(y\mid x)]+\mathbb{E}[\mathbb{e}[y\mid x]^{2}]-\mathbb{E}[\mathbb{E}[y\mid x]]^{2}$ 
Donde: $\mathbb{E}[\mathbb{e}[y\mid x]^{2}]-\mathbb{E}[\mathbb{E}[y\mid x]]^{2}\rightarrow$ es $Var(\mathbb{E}[y\mid x])$  y por ende obtenemos $=\mathbb{E}[var(y\mid x)]+\mathbb{e}[var(y\mid x)]$

Si $s(t)$ es un proceso de Poisson compuesto $s(t)=\sum\limits_{i=1}^{n(t)}y_{i}$ desde $N(t)$ es un proceso de Poisson homogeneo y $y_{i}~(i=1,\dots, N(t))$ son variables aleatorias independientes entre si y v $N(t)$ ademas los $y_{i}$ son identicamentes distribuidos.
Se tiene que:
$a=\mathbb{E}[s(t)]=\mathbb{E}[N(t)]~\mathbb{E}[y_{i}]$
$b= var(s(t))=\mathbb{E}[N(t)]~\mathbb{E}[y_{i}]^{2}$ 

### Ley expecttiva total
$\mathbb{E}[s(t)]=\mathbb{E}[\mathbb{E}[s(t)\mid N(t)]]=\mathbb{E}\left[\mathbb{E}\left[\sum\limits_{i=1}^{N}y_{i}\mid N(t)\right]\right]=\mathbb{E}\left[\mathbb{E}\left[ \sum\limits_{i=1}^{n(t)} \mid N(t)\right] \right]=\mathbb{E}\left[ \sum\limits_{i=1}^{N(t)}\mathbb{E}\left[ y_{i}\mid N(t) \right] \right]=\mathbb{E}[N(t)~\mathbb{E}[y_{i}]]=\mathbb{E}[y_{i}]~\mathbb{E}[N(t)]$ 
#### Prueba b:
$$Var(S(t))=\mathbb{E}[var(s(t)\mid N(t))]+var(\mathbb{E}[s(t)\mid N(t)])$$
Donde:
$\mathbb{E}[var(s(t)\mid N(t))] = \mathbb{E}[N(t)var(y_i)]$
$var(\mathbb{E}[s(t)\mid N(t)]) = Var(n(t)\mathbb{E}[y_i])$ 
$\mathbb{E}[s(t)\mid N(t)]=N(t)\mathbb{E}(y_{i})$ 

Sustituyendo tenemos:
$$=var(y_{i})\mathbb{E}[N(t)]+\mathbb{E}[y_{i}]^{2}\mathbb{E}[N(t)]$$
$$=\mathbb{E}[N(t)](var(y_{i})+\mathbb{E}[y_{i}]^{2})\rightarrow\mathbb{E}[y_{i}^{2}]$$
$$Var(s(t))=\mathbb{E}[N\mid t] ~\mathbb{E}[y_{i}^{2}]=\lambda t~\mathbb{E}[y_{i}^{2}]$$

<div align='right'>Miercoles 29 marzo 2021</div>
# Proceso de Poisson Condicionales
Decimos que un proceso de conteo $N(t)\approx poiss(\Lambda)$ es condicional respecto a $\Lambda$ si $p(N(s+t)-N(s)=n\mid\Lambda=\lambda)=\frac{(\lambda t)^{n}}{n!}e^{-\lambda t}$, donde $\Lambda\approx f-x (\lambda)$. En este caso se dice que $\Lambda$ sea la tasa aleatoria de ocurrencia.

**Problema:** Calcular la media de $N(t)\approx Poiss(\Lambda), \Lambda\approx f_{x}(x)$ 
$$\mathbb{E}[N(s)]=\mathbb{E}[\mathbb{E}[N(s)\mid\Lambda]]=\mathbb{E}[\lambda t]=t\mathbb{E}[x]=t\mathbb{E}[\Lambda]$$
$$\mathbb{E}[N(s)]=t\mathbb{E}[\Lambda]$$

**Problema:** calcula la variana de $N(t)\approx Poiss(\Lambda), \Lambda\approx f_{n}(\lambda)$
$$Var(N(s))=var(\mathbb{E}[N(s)\mid\Lambda])+\mathbb{E}[var(N(s)\mid\Lambda)]=t^{2}var(\Lambda)+t\mathbb{E}[\:ambda]$$

Calculo de potencias de la exponencial $e^{x}$
$$e^{\left(\frac{y}{n}\right)}=e^{w} $$
$$\frac{e^{x+h}-e^{x}}{h}\mid_{x=0}=\frac{e^{n}-e^{0}}{h}=\frac{e^{n}-1}{h}=\frac{e^{w}-1}{w}=1$$
$$e^{x}=(e^{w})^{N}=(1+w)^{N}=\sum\limits_{k=0}^{N}\begin{pmatrix}n \\ k\end{pmatrix}w^{k}=\sum_{k=0}^{N}\begin{pmatrix}n\\ k\end{pmatrix}  \left(\frac{x}{n}\right)^{k}=\sum\limits_{k=0}^{N}1*\left(1-\frac{1}{N}\right)*\left(1 - \frac{2}{N}\right)\cdots$$
$$1\left(1 - \left(\frac{k-1}{N}\right)\right)=\sum\limits_{k=0}^{\infty}\frac{x^{k}}{k!}$$

Aproximar funcion en base a la series de taylor
$f(x)=f(x_{0})=f(x_{0})(x-x_{0})+a_{2}(x-x_{0})^{2}+a_{3}(x-x_{0})+\dots$ 
$f(x)=a_{u}+a_{1}(x-x_{0})+a_{2}(x-x_{0})^{2}+\dots$
$f(x) =2a_{2}(x-x_{0})+3a_{3}(x-x_{0})^{2}$
$f(x)=2a_{2}+3*2a_{3}(x-x_{0})+\dots$ 

$f(x)=\sum\limits_{k=0}^{\infty}\frac{f(x_{0})}{k!}-(x-x_{0})^{k}\rightarrow(e^{x})^{k}=e^{x}\mid_{x=0}=1$

$e^{x}=\sum\limits_{k=0}^{\infty}\frac{x^{k}}{k!}$ $a_{k}=\frac{f(k)(x_{0})}{k!}$ 

