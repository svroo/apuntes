## Propiedades del promedio
Dado un conjunto de datos $\lbrace x_{i}\in\mathbb{R}: i=1,2,\dots,n\rbrace$ 
El mejor representante de estos datos respecto a la distancia cuadratica es su promedio.
Esto quiere decir:
$$\vec{x}=arg~max\sum\limits_{i=1}^{n}(x-x_{i})^{2}$$
se resuelve derivando, así como esta expresada arriba es una función g(x)
$$g(x)= \sum\limits_{i=1}^{n}(x-x_{i})^{2}$$
$$\frac{d}{dx}g(x)= \frac{d}{dx}\left(\sum\limits_{i=1}^{n} (x-x_{i})^{2}\right)=\sum\limits_{i=1}^{n} \frac{d}{dx}(x-x_{i})^{2}=\frac{\sum\limits_{i=1}^{n}(x-x_{i})} {2} = \frac{0}{2}=0$$
$$nx-\sum\limits_{i=1}^{n}x_i=\sum\limits_{i=1}^{n}x-\sum\limits_{i=1}^{n}x_{i}=0$$
$$x=\frac{1}{n}\sum\limits_{i=1}^{n}x_{i}$$
esto se usa para k medios, para usarlo y generar k clusters con k puntos.
serie, los años maravillosos

### Producto punto
Para ver de donde sale el producto punto podemos empezar viendolo desde un triangulo
![[Pasted image 20230504133731.png]]

$$(b_{1}-a_{1})^{2}+(b_{2}-a_{2})+(b_{3}-a_{3})=||b-a||^{2}=(||b||sen(\theta))^{2}+(||a||-||b|| cos(\theta))^{2}$$
$$=||b||^{2}sen^{2}(\theta)+(||a||^{2}||b||^{2}cos^{2}(\theta)-||a||~||b||~cos(\theta))$$
$$=||b||^{2}sen^{2}(\theta)+||b||^{2}cos^{2}(\theta)+||a||^{2}- 2||a||~||b|| cos(\theta)$$
$$=||b||^{2}(sen^{2}(\theta)+cos^{2}(\theta))+||a||^{2}-2||a||~||b||cos(\theta)=||a||^{2}+||b||^{2}-2||a||~||b|| cos(\theta)$$
y del otro lado quedaria:
$$b_{1}^{2}+2a_{1}b_{1}+b_{2}^{2}+a_{2}^{2}-2a_{1}b_{2}+b_{3}^{2}+a_{3}^{2}-2ab$$
$$||b||^{2}+||a||^{2}-2(a_{1}b_{1}+a_{2}b_{2}+a_{3}b_{3})$$
juntando todo queda:
$$a\dots b=a_{1}b_{1}+a_{2}b_{2}+a_{3}b_{3}=||a||~||b|| cos(\theta)$$
$$cos(\theta)=\frac{a.b}{||a||~||b||}$$
$$\theta=axos\left(\frac{a.b}{||a||~||b||}\right)$$
$$ab\iff a*b=0$$

Si tenemos una recta
![[Pasted image 20230504134759.png]]
$$\Delta y=m\Delta x, ~~\frac{\Delta y}{\Delta x}=m$$
$$y=mx+b$$
$$y_{1}=mx_{1}+b$$
$$y_{1}-y_{0}=(x_{1}-x_0)m$$
Despejando la m, obtenemos:
$$m=\frac{(y_{1}-y_{0})}{(x_{1}-x_{0})}$$
que es la formula de la pendiente
$$\Delta y=\Delta x~m$$
Siempre hay dos pendientes en un plano y la pendiente del eje z podemos calcularla como:
$$\Delta z=mx~\Delta x+w_{y}\Delta y$$
y si tenemos un hiperplano con n planos:
$$\Delta z=\sum\limits_{i=1}^{n}m_{i}~\Delta x_{i}$$
Si tenemos una función $f:\mathbb{R}^{n}\rightarrow\mathbb{R}$
$$f(x)=\sum\limits_{i=1}^{n}\frac{\partial f(x)}{\partial x_{i}}dx_{i}$$
$$df(x)=\Delta f(x)\cdot dx$$
$$=||\Delta f(x)||~||dx|| cos(\theta)$$
donde:
$$dx=\begin{bmatrix}dx_{1}   \\ 1 \\ 1 \\ dx_{n} \end{bmatrix}$$
$$\frac{\partial f}{\partial x}(x)=\Delta f(x)=\begin{bmatrix} \frac{\partial f(x)}{\partial x}  \\ \vdots \\  \frac{\partial f(x_{i})}{\partial x_{i}}\end{bmatrix}$$

pelicula el niño que domo al viento.
