### Preposición.
En una caminata al azar simple $\{x(n), n= 0, 1, 2\}$ la probabilidad de cero evento retorno es: $1-\mid p-q\mid$
$$(a+b)^{\alpha}=\sum\limits_{k=0}^{\infty}\begin{pmatrix}\alpha\ \\ k\end{pmatrix}a^{\alpha-k}b^{k}$$
$$\begin{pmatrix}\alpha \\ k\end{pmatrix}=\frac{\alpha(\alpha-1)\dots(\alpha-(k-1))}{k}$$
$$\begin{pmatrix}2n \\ n\end{pmatrix}(-4)^{n}\begin{pmatrix}\frac{1}{2} \\ n\end{pmatrix}$$
En la caminata simple vamos a tener:
$Pn=$ probabilidad de estar en el origen en el paso n
$fn=$ probabilidad de regreso por primera vez al origen
$p_{0}=1$ $f0=0$ la ecuación que describe el suceso esta dado por: $p_{n}=\sum_{h=0}^{\infty}fkp_{n-k}$ 
$$A(t)=\sum\limits_{n=0}^{\infty}an~t^{n}$$
Saber los coeficientes
La probabilidad de retorno al origen es:
$$\sum\limits_{n=0}^{\infty}fn$$
$$Gt=\sum\limits_{k=0}^{\infty}fx~t^{k},~~lim_{t\rightarrow 1}G(t)=\sum\limits_{n=0}^{\infty}fk$$
Si n es impar no es la probabilidad de estar en el origen y $n<0$
$$t^{n}Pn =\left(\sum\limits_{k=0}^{\infty}fk~Pn-k\right)t^{n}$$
$$\sum\limits_{n=1}^{\alpha}t^{n}Pn =\sum\limits_{n=1}^{\infty}t^{n}\left(\sum\limits_{k=0}^{\infty}fk~P_{n-k}\right)$$
$$\sum\limits_{n=1}^{\infty}Pn t^{n}=\sum\limits_{n=1}^{\infty}\sum\limits_{k=0}^{\infty}t^{n}Pk~Pn-k~t^{k}t^{-k}=\sum\limits_{n=1}^{\infty}\sum\limits_{k=0}^{n}fk~Pn-k ~t^{n-k}t^{k}$$
$$=\sum\limits_{k}^{\infty}\sum\limits_{k=0}^{\infty}[fn~t^{k}~pn-k t^{n-k}] =\left(\sum\limits_{k=0}^{\infty}fk-t^{k}\right)\left(\sum\limits_{n=k}^{\infty}Pn~t^{n-k}\right)$$
cambio de variable $\ell=n-k$ 
$$=\sum\limits_{\ell=0}^{\infty}P_{\ell}~t^{\ell}$$
$$\sum\limits_{n=0}^{\infty}P_{n}t^{n}=1$$
$$\sum\limits_{n=0}^{\infty}P_{n}t^{n}+1 =\sum\limits_{\ell=0}^{\infty}P_{\ell}t^{\ell}-1$$
$$\sum\limits_{n=0}^{\infty}P_{n}t^{n}-1 =G(t)\left(\sum\limits_{n=0}^{\infty}P_{n}t^{n}\right)$$
Vamos a suponer n par:
$$P2n =\begin{pmatrix}2n \\ n\end{pmatrix}p^{n} q^{n}$$
que lo anterior es igual a:
$$(-4)^{n}\begin{pmatrix}-\frac{1}{2} \\ n\end{pmatrix}p^{n}q^{n}$$
$$\sum\limits_{n=0}^{\infty}P2nt^{2n}=\sum\limits_{n=0}^{\infty}\begin{pmatrix}-\frac{1}{2} \\ n\end{pmatrix}(-4)^{n}p^{n}q^{n}t^{2n}=\sum\limits_{n=0}^{\infty}\begin{pmatrix}-\frac{1}{2} \\ n\end{pmatrix}(-4pqt^{2})^{n}t^{2n}$$
Usando el binomio de Newton extendido:
$$(1-4pqt^{2})^{\frac{-1}{2}}=\sum\limits_{n=0}^{\infty}\begin{pmatrix}-\frac{1}{2} \\ n\end{pmatrix}(-4pqt^{2})^{n}$$
$$(1-4pqt^{2})^{-\frac{1}{2}}-1=G(t)(1-4pq)^{-\frac{1}{2}}$$
$$lim_{t\rightarrow 1}1-(1-4pqt^{2})^{\frac{1}{2}}=lim_{t\rightarrow 1}G(t) $$
$$\sum\limits_{k=0}^{k}fk=1-(4p1)^{\frac{1}{2}}=1-\sqrt{(p-q)^{2}} =1-\mid p-q\mid$$
Este resultado se da ya que:
$$=(1-4pq)^{\frac{1}{2}}=(1/4p(1-p))=1-4p-4p^{2}=(2p-1)^{2}=(2p-(p+q))=(pq)^{2}$$
