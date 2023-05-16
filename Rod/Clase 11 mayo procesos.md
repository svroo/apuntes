## Distribución Geometrica
$P(x=n, ~ocurre~el~primer~exito)=(1-p)^{n-1}p$ Donce p es la probabilidad de exito
$P(z=n,~numero~de~fracasos~antes~del~primer~exito)=(1-p)^{n}p$ 
Hay que observar bien que se pide, si el numero de fracasos antes del exito  o solo la probabilidad de exito.

$$\mathbb{E}[x]=\sum\limits_{n=1}^{\infty}n~P(X=n)=\sum\limits_{n=1}^{\infty}n[(1-p)^{n-1}p]=$$
$$=\sum\limits_{n=1}^{\infty}\left(\sum\limits_{k=1}^{n}1\right)[(1-p)^{n-1}p]$$
El núcleo de la suma es la multiplicación de 1 por $(1-p)^{n-1}p$ 
$$\sum\limits_{k=0}^{\infty}\sum\limits_{n=k+1}^{\infty}(1-p)^{n-1}p=\sum\limits_{k}p\left(\sum\limits_{n}(1-p)^{n-1}\right)$$
$$\left(\sum\limits_{n}(1-p)^{n-1}\right) = \frac{(1-p)^{k+1}}{(1-(1-p))}=\frac{(1-p)^{k+1}}{p}$$
sustituyendo:
$$=\sum\limits_{k=0}^{\infty}(1-p)^{k+1}=\frac{1}{p}$$
$$S_{N}=\sum\limits_{n=m}^{N}q^{n}=q^{n}+q^{n+1}+\cdots+q^{N}$$
$$qS_{N}=q^{n+1}+\cdots+q^{N}+q^{N+1}$$
$$=S_{n}-qS_{n}=q^{m}-q^{N+1}$$

$$X=Z+1$$
$$Z=X-1$$
$$\mathbb{E}[Z] =\mathbb{E}[X-1]$$
$$=\mathbb{E}[X]-\mathbb{E}[1]$$
$$\mathbb{E}[Z]=\mathbb{E}[X] =1$$
$$\frac{1}{p}-1=\frac{1}{p}- \frac{p}{p}=  \left(\frac{1-p}{p}\right)$$

