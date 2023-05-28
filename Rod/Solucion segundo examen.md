## Ley probabilidad total
$$P(A), \Omega=U_{i}B_{i},~A_{i}\cap B_{j}=\phi, i\neq s$$
$$A=A\cap \Omega$$
$$= A\cap (U_{i}B)$$
$$=U(A\cap B_{i})$$
$$=P(A)=P(U_{i}(A\cap B_{i}))=\sum\limits_iP(A\cap B)=\sum\limits_{i}P(A,B_{i})$$
donde:
$$\sum\limits_{i}P(A,B_{i}) = P(A\mid B_{i})P(B_{i})$$
y finalmente tenemos que;
$$P(A)=\sum\limits_{i} P(A\mid B_{i})P(B_{i})\rightarrow(Probabilidad ~total)$$

También vamos a usar la ley del valor esperado total
$$\mathbb{E}[Y]=\sum\limits_{j}y_{j}~P(Y=y)=\sum\limits_{j}y_{j}\sum\limits_{i}P(Y=y_{j}\mid X=x_{i})P(X=x_{i})$$
Escribimos el valor esperado en terminos de la probabilidad total
$$\mathbb{E}[Y]=\sum\limits_{i}P(Y=y_{j}\mid X=x)~P(X_{i}=x_{i})$$
$$\mathbb{E}[y]=\sum\limits_{i}P(X=x_{i})\sum\limits_{j}y_{j}~P(Y=y_{j}\mid X=x_{i})$$
Donde:
$$\sum\limits_{j}y_{j}~P(Y=y_{j}\mid X=x_{i})=\mathbb{E}[y\mid X=x_{i}]$$
y queda igual:
$$\mathbb{E}[Y]=\sum\limits_{i}\mathbb{E}[Y\mid X=x_{i}]P(X=x_{i})$$


### Primer problema
consiste el siguiente espacio de resultados:
|     | T   | H   |
| --- | --- | --- |
| T   | TT  | TH  |
| H   | HT  | HH  | 

Y definiremos nuestros 3 eventos:
$T= \frac{1}{2}$
$HT = \frac{1}{4}$
$HH= \frac{1}{4}$
$$\mathbb{E}[Y]=\mathbb{E}[y\mid T]~P(T)+\mathbb{E}[y\mid HT]~P(HT)+\mathbb{E}[y\mid HH]~P(HH)$$
$$=\mathbb{E}[y\mid T] \frac{1}{2}+\mathbb{E}[Y\mid HT] \frac{1}{4}+2 \left(\frac{1}{4}\right)$$
$$\mathbb{E}[Y\mid T]= 1+\mathbb{E}[Y]$$
$$\mathbb{E}[y\mid HT]=2+\mathbb{E}[Y]$$
$$\mathbb{E}[y]=(1+\mathbb{E}[y]) \frac{1}{2}+ (2+\mathbb{E}[y]) \frac{1}{4}+  \frac{1}{2}$$
$$=\frac{1}{2} + \frac{1}{2}\mathbb{E}[y]+ \frac{1}{2} + \frac{1}{4} \mathbb{E}[y]+ \frac{1}{2}$$
$$=\frac{3}{2} + \left( \frac{1}{2}  + \frac{1}{4}\right)\mathbb{E}[y]$$
$$= \frac{3}{2}+ \frac{3}{4}\mathbb{E}[y]$$
$$\left(1- \frac{3}{4}\right)\mathbb{E}[y]= \frac{3}{2}$$
$$\mathbb{E}[y]= \frac{3}{2} - \frac{1}{4}$$
$$\mathbb{E}[y]=6$$


## Segundo ejercicio
$$P(X_{2}=3\mid X_{0}=1)=P_{ij}^2$$
$$P(X_{2}=j\ \mid X_{0}=1)=\frac{P(X_{2}=J, X_{0}=i)}{P(X_{0}=i)}$$
$$(X_{2}=J, X_{0}=i)=U_{k}(X_{2}= J, X_{1}=P_{i}, X_{0}=1)$$
$$P(X_{2}=J, X_{0}=i)=\sum\limits_{j}P(X_{2}=J, X_{1}=k, X_{o}=i)=\sum\limits_{k}P(X_{1}=J, X_{i}=h)P(X_{1}=k, X_{u}=1)$$
no se pudo demostrar 💀

Prueba inducción matematica que $P(X_{n}=J\mid X_{0}=J)=P_{ij}^{n}$ con base $n=2$ 