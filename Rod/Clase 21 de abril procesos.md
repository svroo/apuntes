**Definición:** Sea X,Y variables aleatorias discretas en el mismo espacio de probabilidad con función de probabilidad condicional $f(Y|X)$, entonces la esperanza condicional de y dado $X=x$ esta dada por:
$$\mathbb{E}[Y|X=x]=\sum\limits_{y}y~f_{Y|X}(y|x)$$
La esperanza condicional (restringida a $X=x$) satisface:
$$a)\mathbb{E}[(c_{1}X_{1}+\cdots+c_{n}X_{n})|Y=y]=\sum\limits_{i=1}^{n}c_{i}[x_{i}|Y=y]$$
$$b)\mathbb{E}[h(X)|X=x]=h(x), h:\mathbb{R}\rightarrow\mathbb{R}$$
$$c) \mathbb{E}[Y|X=x]=\mathbb{E}[Y] si~X~son~independientes$$
Demostración
a. Por inducción:
$$\mathbb{E}[c_{i}X_{i}|Y=y]=\int_{-\infty}^{\infty}ax_{i}f_{x_{i}|y}(x,y)dx$$
$$=c_{i}\int_{-\infty} ^{\infty}x_{i}f_{x_{i} |y}(xy)d_{x_{i}}=c_{i}\mathbb{E}[X_{i}|Y=y]~Caso~base$$
Supongamos que el enunciado es valido para n por demostración entonces tambien vale para $n+1$.
$$\mathbb{E}[C_{i}X_{i}+\cdots+C_{n}X_{n}+C_{n+1}X_{n+1}][Y=y]=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}[C_{i}x_{i}+\cdots+C_{n}X_{n}+C_{n+1}X_{n+1}]$$
donde las integrales son $n+1$
$$=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}(C_{i}X_{i}+\cdots+C_{n}X_{n}+C_{n+1}X_{n+1})f_{C_{i}X_{i}+\cdots+C_{n}X_{n}+C_{n+1}X_{n+1}|y}(X_{i},\dots,X_{n},X_{n+1}|y)dx,.,dxn,dxn+1$$
$$=\int_{-\infty}^{\infty}\dots\int_{-\infty}^{\infty}C_{n+1}X_{n+1}f_{(X_{i},\dots,X_{n},X_{n+1})}y(x_{i},\dots,x_{n},x_{n+1}|y)dx_{i},\dots dx_{n},dx_{n+1} $$
$$+\int_{-\infty}^{\infty}\dots\int_{-\infty}^{\infty}(C_{i}X_{i}+\cdots +C_{n}X_{n})f_{X_{i},\dots,X_{n},X_{n+1}|y} (x_{i},x_{n},x_{n+1})dx_{1}\dots dx_{n+1}$$
$$=\int_{-\infty}^{\infty}\cdots\int_{-\infty}^{\infty}C_{n+1}X_{n+1}+dx_{n+1}\int_{-\infty}^{\infty}\cdots\int_{-\infty}^{\infty}f_{(x_{i},\dots,X_{n},X_{n+1})} (x_{i},\dots,x_{n},x_{n+1}|y)dx,dx_{n}$$
y podemos ver que:
$$\int_{-\infty}^{\infty}\cdots\int_{-\infty}^{\infty}f_{(x_{i},\dots,X_{n},X_{n+1})} (x_{i},\dots,x_{n},x_{n+1}|y)dx,dx_{n}$$
es la funcion de probabilidad marginal con lo que de un lado de la suma sustituimos esa función y queda:
$$=C_{n+1} \int_{-\infty}^{\infty}f_{X_{n+1}|y}(x_{n+1}, y)dx_{n+1}=C_{n+1}\mathbb{E}[X_{n+1}|Y=y]$$
y del otro lado de la suma tenemos:
$$+\int_{-\infty}^{\infty}\cdots\int_{-\infty}^{\infty}(C_{i}X_{i}+\cdots+C_{n}X_{n})\int_{-\infty}^{\infty}f_{(X_{i},\dots,X_{n},X_{n+1})|Y} (x_{i},\dots,x_{n},x_{n+1})dx_{n+1}$$
y podemos ver:
$$\int_{-\infty}^{\infty}f_{(X_{i},\dots,X_{n},X_{n+1})|Y} (x_{i},\dots,x_{n},x_{n+1})dx_{n+1}$$
como: 
$$f_{(X_{i},\dots, X_{n})|Y}(x_{i},\dots,x_{n}|y)$$
sustituyendo tenemos:
$$+\int_{-\infty}^{\infty}\cdots\int_{-\infty}^{\infty}(C_{i}X_{i}+\cdots+C_{n}X_{n})f_{x_{i},\dots,x_{n}|Y}(x_{i},\dots,x_{n}|y)dx_{i}\dots,dx_{n}$$
y lo de arriba lo podemos ver como:
$$\mathbb{E}[(C_{i}X_{i}+\cdots+C_{n}X_{n+1})|Y=y]=\sum\limits_{i=1}^{n}C_{i}\mathbb{E}[X_{i}|Y=y]$$
Resumen:
$$\mathbb{E}[(C_{i}X_{i}+\cdots+C_{n}X_{n+1})|Y=y]=C_{n+1}\mathbb{E}[X_{n+1}|Y=y ]+\sum\limits_{i=1}^{n}C_{i}\mathbb{E}[X_{i}|Y=y]=\sum\limits_{i=1}^{n+1}C_{i}\mathbb{E}[X_{i}|Y=y]$$
$$b.\mathbb{E}(h(x)[X=x])=\sum\limits_{y}G(x)=h(x)$$
hacemos un cambio de variable $y=h(x)$
Prueba.
$$\mathbb{E}[h(x)|X=x]=\sum\limits_{y}y~f_{Y|X}~(y|x)=\sum\limits_{y}h(x)~f_{y|x}(y|x)=h(x)\sum\limits_{y}f_{y|x}(y|x)=h(x)$$
y como:
$$\sum\limits_{y}f_{y|x}(y|x) = 1$$
entonces queda $h(x)$

$$c. \mathbb{E}[Y|X=x]=\mathbb{E}[Y]$$
si X,Y son independientes.
Prueba
$$\mathbb{E}[Y|X=x]=\sum\limits_{y}y~f_{y|x}(y,x)=\sum\limits_{y}f_{y}~(y,x)=\mathbb{E}[y]$$