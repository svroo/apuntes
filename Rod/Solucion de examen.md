1. $X, Y$ son variables dependientes con función de probabilidad conjunta:
$$f_{X,Y}(X,Y) =\left\lbrace\begin{matrix} 3y&0<x<y\leq1 \\  0,&c.c.\end{matrix}\right.$$
a. Econtrar la densidad condicional de Y dado $X=x$ 
b. Encontrar la densidad condicional de X dado $Y=y$

Encontrar la región donde se encuentra la densidad.
![[Pasted image 20230518130918.png]]

$$f_{y\mid x}(x,y)=\frac{f_{X,Y}(x,y)}{f_{X}(X)}, f_{X}(x)=\int_{x}^{1}f_{XY}(x,y) dy=\int_{x}^{1}3y~dy$$

$$3y=\int_{x}^{1}y~dy=3y\left[\frac{y^{2}}{2}\right]_{x}^{1}=\frac{3}{2}(1-x^{2})$$
$$=\frac{3y}{\frac{3}{2}(1-x^{2})}=\frac{2y}{(1-x^{2})}$$
Inciso b.
$$f_{XY}(XY)=\frac{f_{XY}(xy)}{f_{Y}(y)}$$
$$f_{Y}(y)=\int_{0}^{y}f_{XY}(xy)dx=\int_{0}^{y}3y
~dx=3y\int_{0}^{y}dx$$
$$=3y[x]_{0}^{y}=3y(y)=3y^{2}$$
$$\frac{3y}{3y}=\frac{1}{y}$$
## Ejercicio 2
Encontrar $F^{-1}(.)$ para muestrear numero aleatorios.
![[Pasted image 20230518134208.png]]
$$F(x)=\int_{-\infty}^{\infty}f(t)~dt =\int_{0}^{x}f(t)~dt$$

Con la función
$$F(x)=\left\lbrace \begin{matrix}  \frac{1}{2}&0\leq x\leq 1 \\ &1<x\leq 2\end{matrix}\right.$$
Area bajo la curva
$$F(x)=\frac{1}{2} +\int_{1}^{x}(2-t)~dt= \frac{1}{2}+2\int_{1}^{x}dt-\int_{1}^{x}t~dt$$
$$=\frac{1}{2}+2 [t]_{1}^{x}-\left[\frac{t}{2}\right]_{1}^{x}=\frac{1}{2}+2(x-1) - \frac{1}{2}(x^{2}-1)= \frac{1}{2}+2x-2- \frac{1}{2}x^{2}+ \frac{1}{2}$$
$$=\left(\frac{-1}{2}x^{2}+2x-1\right)= \frac{1}{2}(x^{2}-4x+2)=(x-2)^{2}-2= - \frac{1}{2}(x-2)^{2}+1$$

$$u=\frac{1}{2}x^{2},~~ x^{2}=2u,~~~u=\sqrt{2u}$$
Resultado
$$\left\lbrace \begin{matrix} \sqrt{2u}&0\leq u\leq \frac{1}{2}  \\ 2-\sqrt{2(1-u)} & \frac{1}{2}< u \leq 1\end{matrix} \right.$$
