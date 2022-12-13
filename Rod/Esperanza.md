Definición: Sea x una variable aleatoria en unespacio de probabilidad finito $(\Omega, P )$  donde $\Omega = \{w, \dots, \Omega_{n} \}$. El valor esperado de X data dado por:
$$E(X) = \sum_{i=1}^{n} x(w_{i}), p(w_{i})$$
Si al menos la imagen de X es finito $(X\mid \Omega)$ finito o numerable
$$E(X) = \sum_{y \in X(\Omega)} y P(x,y)$$
$$E: R_{w(\Omega)}\rightarrow R ~~es ~una~función~lineal$$
Pues 
$$E(aX+bY)=aEX+bEY$$
$\forall a,b\in \mathbb R$ Además si $F:\mathbb R\rightarrow \mathbb R$  función real valuada (medible) entonces $f_{0}X: \Omega \rightarrow  \mathbb R$ es tambien una variable aleatoria.
Y además 
$$E(f(x)) = \sum f(f) P(X=y) ~~~~y\in X(\Omega)$$

En nuestro curso asumiremos tales f medible salvo que se espeifique lo contrario.
Además, para $X$ y $Y$ V.A independiente. $E(xy) = E(x)F(y)$

### Varianza y desviación estandar
La vamos a utilizar como una medida de dispersión.
**Definición:** Sea X una variable aleatoria con valor esperado $\mu$. La varianza de X esta definida como:
$$\sigma_{x}^{2} = Var(X) = E((x-\mu)^ {2)}= \sum_{y~\in X(\Omega)} (y-\mu)^{2}p(X=y )~~~y\in X(\Omega)$$
y la desviación estandar $\sigma_{x}=\sqrt{Var(x)}$ 

##### Teorema

1. $Var(x) = E(x^{2}) - \mu^{2}$ 
2. $\forall a\in R$ 
$Var(ax)=a^{2}Var(x)$ = $E((a^{2}x-a \mu)^{2})= a^{2} E( (x-\mu )^{2})$
3. Si $X_{y}$ y $y$ son variables aleatorias independientes $Var(x+y) = Var(x) + Var(y)$
4. Si "c" es una constante entonces $Var(x+c) = Var(x)$

#### Estandarización

Sea X una variablea aleatoria con esperanza $\mu$ y desviación estandar $\sigma$, a $y=\frac{x-\mu}{\sigma}$ se le conoce como la estandarización de X.

Simplemente mete todos los datos entre (0,1)

#### Covarianza y correlación
Ahora decimos sobre la la relacion entre dos V.A dadas en un mismos espacio muestral

**Definición:** Si $X_{y}Y$ son B.A con medidas finitas entonces definimos la covarianza de $X_{y}Y$ como:
$$\sigma_{x,y}=Cov(x,y) = E((X-\mu_{x}) (y-\mu_{y}))$$

##### Teorema:

Sea X,y V.A con medidas finitas:
1. $Cov(x,y) = E(xy) - E(x)E(y)$
2. $Cov(x,y) = Cov(y,x)$
3. $Cov (x,x) = \sigma_{x}^{2}$
4. Si X es una constante, entonces $E(x,y) = 0$ 
5. La covarianza es lineal en sus dos coordenadas osea que es bilineal. Por ejemplo $Cov(a,x+by,z) = a~Cov(x,z)+b~Cov(y,z)$ 
6. Se tiene que $|Cov(x,y)| \leq \sigma_{x}~\sigma_{y}$ Ademas la igualdad se da si y sólo si existiera $a,b \in \mathbb R$  $y=ax+b$ o $X=ax+b$

**Definición:** Si $X_{y}$ y $Y$ son V.A con media finita y varianza no cero, entonces definimos el coeficiente de correlación:
$$P_{x,y}=\frac{Cov(x,y)}{\sigma_{x}\sigma_{y}}$$

Si $X,Y$ poseen medias finitas y varianzas no cero, el coeficiente de correlación de x, y  se define con el coeficiente de correlación:

$$-1 \leq P_{x,y}=\frac{Cov(x,y)}{\sigma_{x}\sigma_{y}} \leq 1$$

##### Teorema:
Si $X_{y},Y$ son V.A definidas en $\Omega$ con $a,b \in \mathbb R$ $Var(a~X+by) = a^{2}Var(x)+b^{2}Var(y)+2~ab~cov(x,y)$ 
Más en general si $x_{1},\dots,x_{n}$ son variables aleatorias sobre $\Omega$ y $a_{1},\dots, a_{n}$ son cortantes, entonces:

$$Var\left(\sum_{i=1}^{n}a_{i}x_{i}\right)= \sum_{i=1}^{n} \sum_{j=1}^{n}a_{i}a_{j}~Cov(x_{i},x_{j})$$
que sale de:
$$E([a_{x}+b_{y}-(a\mu_{x}+b\mu_{y})]^{2)}= E[a(x-\mu_{x}) + b(y-\mu_{y})]^{2}$$
$$E=(a^{2}(x-\mu_{x})^{2} +2a(x-\mu_{x}) b(y-\mu_{y}) +b^{2}(y-\mu_{y})^{2}) = a^{2}Var(x)+2ab~Cov(x,y) + b~Var(y)$$

Vemos que es lineal por lo que:

$$Var\left(\sum_{i=1}^{n} a_{i}x_{i} \right)= E\left[\left(\sum_{i=1}^{n} a_{i}\mu_{i}\right)\right]^{2}$$ $$E[(a_{i}x_{i})^{2}] = a_{i}^{2}E((x_{i}-\mu_{i})^{2})=Cov(x_{i},x_{i})$$
Supongamos valido el resultado para pvi $K = n$, ie
$$var\left(\sum_{i=1}^{n} a_{i}x_{i}\right)= \sum_{i=1}^{n}\sum_{j=1}^{n}a_{i}a_{j}~Cov(x_{i},x_{j})$$
para $k=n+1$

$$Var\left( \sum_{i)1}^{n+1} a_{i}x_{i} \right) = Var\left( \sum_{i=1}^{n} a_{i}x_{i}+a_{n+1}X_{n+1} \right)$$
$$=Var\left(\sum_{i=1}^{n}a_{i}X_{i} \right)= a^{2}_{n+1}Var(X_{n+1})= 2~a_{n+1}~Cov\left(\sum_{i=1}^{n}a_{i}x_{i},x_{n+1}\right)$$

$$=\sum_{i=1}^{n}\sum_{j=1}^{n} a_{i}~a_{j}~Cov(x_{i},x_{j})+a_{n+i}~a_{n+j}~Cov(X_{n+i},C_{n+j}) +2$$
$$=\sum_{i=1}^{n}a_{n+1}~a_{i}~Cov(X_{i},X_{n+1}) ~Var\left( \sum_{i=1}^{n} a_{i}x_{i} \right)$$
$$=\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}~a_{i}~a_{j}~Cov(x_{i},x_{j})~2~\sum\limits_{i=1}^{n+1}~a_{n+1}~a_{i}~Cov(x_{i},x_{n+1})+a_{an+1}~a_{n+1}~Cov(X_{n+1}, C_{n+1})$$
