Un modelo de autoregresion de orden **p**, abreviado **AR(p)** tiene la forma:
$$X_{t}-\mu=\phi_{1}(X_{t-1}-\mu)+\phi_{2}(X_{t-1}-\mu)$$

Podemos escribit el modelo**$AR(p)$** en terminos del operador de diferenciación B como:
$$(1-\phi_{1}B-\phi_{2}B^{2}-\cdots-\phi_{p}B^{p})X_{t}=\phi(B)X_{t}=W_{t}$$
donde:
$$\phi(B)=1-\phi_{1}B^{1}-\phi_{2}-\cdots-\phi_{p}B^{p}$$
definido como el operador autoregresivo

### The AR(1) Model
Consideremos el AR(1). el modelo más sencillo de un modelo autoregresivo es cuando vale 1, se puede ver como: 
$$X_{t}=\phi X_{t-1}+W_{t})$$
Si iteramos haciaatras k veces obtenemos:
$$X_{t}=\phi X_{1}+W_{t}=\phi(\phi X_{t-2}+W_{t-1})+W_{t}$$
$$=\phi^{2}X_{t-2}+\phi W_{t-1}+W_{t-2}$$
$$\vdots$$
$$=\phi^{k} X_{t-k}+\sum\limits_{j=0}^{k-1}\phi W_{t-j}$$
This method suggests that, by continuing to iterate backward, and provided that $\mid\phi\mid<1$ and $sup_{t}~var(X_{t})<\infty$ we can represent an $AR(1)$ model as a linear process given by:
$$X_{t}=\sum\limits_{j=0}^{\infty}\phi W_{t-j}$$
wich is stationary.


