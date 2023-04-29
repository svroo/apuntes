# Valor esperado condicional (variable aleatoria)
**Definción:** Sea X,Y variables aleatorias definidas en el mismo espacio de probabilidad $((\Omega, F, P))$ con función de probabilidad condicional $f_{Y|X}$ 
La esperanza condiciona lesta dada de Y dado X es una función de X y esta dada por:
$$g(x)=\mathbb{E}[Y|X]$$
Propiedades:
$$a.\mathbb{E}[g(x)h(x)]=\mathbb{E}[yh(x)],h:\mathbb{R}\rightarrow\mathbb{R}$$
$$b. \mathbb{E}[X,Y|X=x]=x\mathbb{E}[Y|X=x]$$
$$c. si~H:\mathbb{R}\rightarrow\mathbb{R}$$
$$\mathbb{E}[Y|H(x)]=\mathbb{E}[Y|X]$$

##### Demostraciones
$$a. \mathbb{E}[g(x)h(x)]=\sum\limits_{x}g(x)h(x)f_{X}(x)$$
donde:
$$g(x)\rightarrow\mathbb{E}[Y|X]\rightarrow\sum\limits_{y}y~f_{Y|X}(x,y)$$
Sustituimos:
$$=\sum\limits_{x,y}yh(x)~f_{x,y}(x,n)=\mathbb{E}[yh(x)]$$

$$b. \mathbb{E}[XY|X=x]=x\mathbb{E}[Y|X=x]$$
para evitar la doble sumatoria hacemos un cambio de variable de la siguiente forma:
$$x=0$$
$$z=xy$$
$$y=\frac{z}{x}$$
