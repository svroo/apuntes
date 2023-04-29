# Calculo del área mediante determinantes
$$b=(b_{1},b_{2})$$
$$a=(a_{1},a_{2})$$
![[Pasted image 20230428131143.png]]

$$a U B=||a||~||b||~cos(\theta)$$
$$cos(\theta)=\frac{a*b}{||a||~||b||}$$

Calculo del area:
$$A^{2}=(||a||~||b||~sen(\theta))^{2}=||a||^{2}sen(\theta)=(a_{1}^{2}+a_{2}^{2})(b_{1}^{2}+b_{2}^{2})(1-cos^{2}(\theta))$$
$$=||a||^{2}||b||^{2}\left(1-\frac{(a*b)^{2}}{||a||^{2}||b||^{2}}\right)=||a||^{2}||b||^{2}-(a*b)^{2}$$
$$=a^{2}_{1}b_{1}^{2}+a_{1}^{2}+b_{1}^{2}+a_{2}^{2}b_{1}^{2}+a_{2}^{2}b_{2^2}-(a_{1}b_{1}+a_{2}^{2}b_{2}^{2})$$
$$=a_{1^2}b_{2}^{2}+a_{1^{2}+}b_{2}^{2}=2a_{1}b_{1}a_{2}b_{2}=(a_1b_{2}-a_{2}b_{1})^{2}$$
ya que el area tiene que tener un valor positivo se tiene que sacar el absoluto siempre.

### Transformacion del elemento de área en cordenadas polares
Si tenemos un eje $z=\mathbb{R}^{2}$ y tenemos que para las cordenadas en dos dimensiones lo podemos ver como:
$$z=\mathbb{R}^{2}=x^{2}+y^{2}$$
y las polares como:
$$\theta=aTan\left(\frac{y}{x}\right)$$
lo primero que vamos a hacer es definir la semi derivada de $\theta$: 
$$d_{\theta}=\frac{\partial\theta}{\partial x}d_{x}+\frac{\partial\theta}{\partial y}d_{y}$$
$$d_{z}=\frac{\partial z}{\partial x}dx+\frac{\partial z}{\partial y}d_{y}$$
si lo vemos como forma matricial obtenemos:
$$\begin{bmatrix}d_\theta \\ d_{z}\end{bmatrix}=\begin{bmatrix}\frac{\partial\theta}{\partial x}&\frac{\partial\theta}{\partial y} \\ \frac{\partial z}{\partial x}&\frac{\partial z}{\partial y}\end{bmatrix}\begin{bmatrix}d_{x} \\  d_{y}\end{bmatrix}$$

si resolvemos, podemos obtener:
$$\frac{\partial \theta}{\partial x}=\frac{1}{1+\left(\frac{y}{x}\right)} =y*\left(\frac{1}{x^{2}}\right)=\frac{-y}{x^{2}+y^{2}}=\frac{-y}{z}$$
$$\frac{\partial\theta}{\partial y}=\frac{1}{1+\left(\frac{x}{y}\right)^2}\frac{1}{x}\frac{x}{x}=\frac{x}{x^{2}+y^2}=\frac{x}{z}$$
$$\frac{\partial z}{\partial x}=2x$$
$$\frac{\partial z}{2 y}=2y$$

Obtenemos la siguiente matriz sustituyendo los valores obtenidos
$$\begin{bmatrix}\frac{\partial\theta}{\partial x}&\frac{\partial\theta}{\partial y} \\ \frac{\partial z}{\partial x}&\frac{\partial z}{\partial y}\end{bmatrix}=\begin{bmatrix}\frac{-y}{z}&\frac{x}{z} \\ 2x&2y \end{bmatrix}=B$$
$$||B||=\frac{-2y}{z} - \frac{2x^{2}}{z}  =-\left(\frac{2}{z}\right)(x^{2}+y^{2}) =-2$$
$$abs(|B|)=2$$

Si queremos obtener el area de una sarea lo podemos ver como:
$$|(dx_{1},dy_{2})|=d_{x}d_{y}|(e_1,e_2)|=-d_{x}d_{y}$$
$$abs(|(Bd_{x}e_{1},Bd_{y}e_{2})|)=abs(d_{x}d_{y}|(Be_{1},Be_{2})|)$$
$$=abs(d_{x}d_y|(B_{1},B_{2})|)=abs(d_{x}d_{y}|B|)$$
$$=d_{x}d_{y}abs(|B|)$$

Con $d=0$ y $\beta=1$

$$B=(B_{1},B_{2})$$
$$Be_{1}=(B_{1},B_{2})=\begin{pmatrix}\alpha  \\ \beta\end{pmatrix}=\alpha B_{1}+\beta B_{2}=B_{1}$$
$$d_{\theta}d_{z}=2d_{x}d_{y}$$
$$d_{x}d_{y}=\frac{1}{2}d_{\theta}d_{z}$$


## Método para generar variables aleatorias normales
Tenemos que X,Y de distribuyen de manera gaussiana con intervalo (0,1) independientes
$$x\approx \frac{1}{\sqrt{2\pi}}e^{\frac{x^{2}}{2}},~~y\approx\frac{1}{\sqrt{2\pi}}e^{\frac{x^{2}}{2}}$$

$$f_{x,y}(x,y) = \frac{1}{2\pi}e^{\frac{x^{2}+y^{2}}{2}}$$
Si convertimos esto a coordenadas polares tenemos que:
$$z=x^{2}+y^{2}$$
$$\theta=aTan\left(\frac{y}{x}\right)$$
$$\frac{1}{2\pi}e^{\frac{x^{2}+y^{2}}{2}}d_{x}d_{y}=\frac{1}{2\pi}\left(e^{\frac{-z}{2}} \frac{1}{2}\right)d_{\theta}d_{z}$$
Donde:
$$\frac{1}{2\pi}\left(e^{\frac{-z}{2}} \frac{1}{2}\right)d_{\theta}d_{z}=f_{\theta}(\theta,z)=\begin{bmatrix} -z(t) \\ \frac{1}{2}e\end{bmatrix}\begin{bmatrix} \frac{\pi }{2\pi} \end{bmatrix}$$


