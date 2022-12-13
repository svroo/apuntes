Definimos $0=(1,1,\dots,1)$ dimensión n
Definimos el vector de esperanzas = $(\mu_{1},\mu_{2},\dots,\mu_{n})$
Consideramos a los pesos $w_{1},\dots,w_{n}$ recordemos que estos pesos deben sumar 1
Por cada dos activos vamos a tener una covarianza, que esta representada por la matriz C: $C=(C_{ij})$ 
la matriz de covarianza del portafolio.
Donde:
$$C_{ij}=Cov(R_{i},R_{j})$$
Note que: 
$$C_{ii}=Var(R_{i})$$
y además puede ser demostrado que C es simetrica y semidefinida positiva (es decir que $\forall A,~AACA^{T}\geq0$) y supondremos que es invertible.

La ganancia esperada del portafolio:
$$M =MW^{t}=M\mu_{1}w_{1}+\dots+\mu_{n}w_{n}$$
y su riesgo:
$$\sigma^{2}=Var(w_{1}R_{1}+\cdots+w_{n}R_{n}) = WCW^{t}$$

Denotamos por f la finción que toma cada vector de pesos $(w_{1},\cdots, w_{n})$ plano riesgo- esperanza esdo de:
$$f(w_{1},\cdots,w_{n}) = (\sigma,\mu)$$
Trataremos de calculare m comportamiento de f de manera general.Consideramosu na linea parametrizada por el parametro t = $\ell(t)=a_{1}+tb_{1},\cdots, a_{n}+tb_{n} = At + B$
Si tomamos un punto de t: $\mu (\ell (t) ) = M(At + b) = MAt + MB$ la cual es una función lneal de t.

Ahora respecto al riesgo:
$$\sigma^{2}(\ell(t))= (At+B) C(At+B)^{t}=(At+B) C(A^{t}+B^{t})=(ACA^{t})t^{2}+ (BCA^{t}+ACB^{t})t+BCB^{t}$$
Podemos llamarla
$$= \gamma~t^{2}+\delta t+\epsilon$$

#### Teorema :
El portafolio de minimo riesgo es quel con peso: 
$$w=\frac{oC^{-1}}{OC^{-1}O^{t}}$$
#### Demostración Buscaremos minimizar:
$$\sigma^{2}=\sum\limits_{i,j=1}^{n}c_{ij}w_{i}w_{j}= WCW^{t}$$
Sujeto a la restriccion
$$OW^{t}=w_{1}+\cdots+w_{n}= 1$$
De acuerdo a la ténica de los mltiplicadores de Lagrangé.
Para esto tomamos la función a minimizar, sumandole la restricción:

$$g(w_{1},\dots, w_{n})=\sum\limits_{i,j=1}^{n}c_{i,j}w_{i}w_{j}+\alpha(1-(w_{1}+\dots+w_{n}))=0$$

$$ \frac{\partial g}{\partial w_{\ell}} =\frac{\partial}{\partial w_{\ell}}~~~\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}c_{ij}w_{i}w_{j}+\alpha(1-(w_{1}+\dots+w_{n}))$$

$$=\frac{\partial}{\partial~w_{\ell}}\sum\limits_{i=1~~i\neq\ell}^{n}\sum\limits_{j=1}^{n}c_{ij}w_{i}w_{j}+\frac{\partial}{\partial~w_{\ell}}\sum\limits_{j=1}^{n}c_{ij}w_{i}w_{j}\mid-1$$

$$\frac{\partial}{\partial~w_{\ell}}\sum\limits_{i=1~~i\neq\ell}^{n}\left[c_{ij}w_{i}w_{j}+ C_{i\ell}w_{i}w_{\ell} \right]=\frac{\partial}{\partial~w_{\ell}}\left[\sum\limits_{i=1~~i\neq\ell }^{n}\sum\limits_{j=1~~j\neq\ell}^{n}C_{ij}w_{i}w_{j}+\sum\limits_{i=1~~i\neq\ell}^{n}C_{i\ell}w_{i}w_{\ell}\right]=\sum\limits_{i=1~~i\neq\ell}c_{i\ell}w_{i} $$

<div align = 'right'><h4>07/12/2022</h4></div>
$$\frac{\partial}{\partial~w_{i}}g(\alpha,w_{i},\dots,w_{n})=\sum\limits_{i=1}^{n}c_{i\ell}w_{i}+\sum\limits _{j=1~~j\neq\ell} c_{j\ell}w_{j}+c_{\ell\ell}w_{\ell}-1$$
$$t $$
Ahora solo falta la parcial de g, queda de la siguiente manera:
$$\frac{\partial}{\partial~\alpha}g(\alpha,w_{i},\dots,-w_{n})=0~~~~2~ecuación$$
por definicion tenemos que $g(\alpha,w_{i},\dots,w_{n}) = \sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}(i,w_{i}w_{j}+\alpha(1-w_{i}\dots,-w_{n}))$
$$1)~\sum\limits_{i=1}^{n}c_{\ell~i}w_{i}=\frac{\alpha}{2}$$

$$(AB)^{t}_{ij}=(AB)_{ij}$$



como esto se cumple desde $\ell = 1,\dots, n$ se transforma a $CW^{t}= \frac{\alpha}{2}O^{t}$ y se puede despejar W de la siguiente forma:
$$WC^{t}=\frac{\alpha}{2}O$$
como supusimos que la c es invertible podemos despejar a W así:
$$3)~~W = \frac{\alpha}{2}OC^{t}$$
Despues:
$$OW^{t}=1$$
$$4)~~WO^{t}= 1$$
Sustituimos 3 en 4:
$$ \frac{\alpha OC^{-1}}{2}O^{t}= 1$$
$$5)~~\alpha = \frac{2}{OC^{-1}O^{t}}$$
Y obtenemos:
$$w=\frac{2}{OC^{-1}O^{t}}~~\frac{1}{2} OC^{-1}=\frac{OC^{-1}}{Oc^{-1}O^{t}}$$

#### Teorema:
Para una esperenza $\mu$ dada, el portafolio con riesgo minimo esta dado por la siguiente formula:
$$W= \left|\begin{matrix}M&MC^{-1} &O^{t}\\1 & OC^{-1} & O^{t} \end{matrix} \right|~MC^{-1}+ \left| \begin{matrix} MC^{-1}&M^{t}&\mu\\ OC^{-1}&M^{t}&1 \end{matrix}\right|$$
$$\left|  \begin{matrix} MC^{-1}M^{t} &MC^{-1}O^{t} \\ OC^{-1}M^{t}& OC^{-1}O^{t}\end{matrix} \right|$$
Dependiendo del número de variables es el número de multiplicadores que debemos usar. 

[[Matematicas avanzadas]] 