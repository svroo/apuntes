### Pre - procesamiento
El pre - procesamiento siempre tiene que ser diferente para cada conjunto de datos, para seleccionar de acuerdo a nuestro criterio el mejor procesamiento.

### Tipos de trasformaciones

Tipos de transformaciones que vamos aplicar a cada una de las columnas.

#### Centrado y escalado
Para centrar una caracteristica vamos a seleccionar todos los valores. Similar a escalar los datos, cada valor de las variables es dividido por su desviacion estandar 
$$\hat{x} = \frac{x-\mu_{x}}{\sigma}$$
Esto centra los valores en cero y un máximo de 3 desviaciones estandar.

#### Escalador min max
Su función es escalar los datos entre cero y uno, sin cambiar la distribción de los datos
$$\hat{x} = \frac{x-min(x)}{max(x)-min(x)}$$

### Resolve skewness
Busca corregir la asimetria de la distribución de los datos. La manera formal de describirla se define como el tercer momento:
$$\mathbb{E} \left[\left(\frac{x-\mu_{z}}{\sigma^{2}}\right)^{3}\right]$$
$$y=\left(\frac{x-\mu_{z}}{\sigma^{2}}\right)^{3}$$
$$=\sum\limits \frac{y*1}{n}=\frac{1}{N}\sum\limits_{i=1}^{N}y_{i}$$
Si el valor esta entre +2 y -2 la simetria no es tan intensa, si sale de estos valores se tendría que transfomrar.

Replacing the data with the log, square root, or inverse may help to remove the skew.

### Transormaciones a multiples caracteristicas.
#### Resolver los outliers
One data transformation taht can minize the problem is the spatial sign. This procedure projects the feature values onto a multidimensional sphere.

$$x_{i} =\frac{x_{i}}{\mid\mid x_{i} \mid\mid}=vector~unitario$$

Since the denominator is intended to measure the sqared distance to the center of the feature's distribtion, it is important to center and scale the variable data prior to using this transformation.

### Reducción de datos y reducción de caracteristicas
Estos metodos reducen los datos generando un conjunto más pequeño de las cracteristicas que capturen la mayoria de la informacion de las variables originales.

Para todas las tecnicas de reducción de datos tiene algunas funciones originales.

El metodo más común es PCA

##### PCA
VAmos a considerar una matriz $N~x~d$ con las column/wise zero empirical mean
$$x=\begin{bmatrix}\dots&x_{(1)}&\dots \\ \dots&x_{(2)}&\dots \\ &\vdots&  \\ \dots&x_{(N)}&\dots\end{bmatrix}$$

La transformacion es definida por un conjunto de tamañp k de d-dimensiones vectores de peso $w_{(j)}=(w_{1},w_{2},\dots,w_{d})_{(j)}$ that map each roe vector $x_{i}$ of x to a new vector of principal component scores $t_{(i)}=(t_{1},t_{2},\dots,t_{k})_{(i)}$ dado por:
$$t_{j(i)}=x_{i}*w_{j}~~~for~i =1,\cdots,N~~j=1,\cdots,k$$
La transformación es una ponderacion de las caracteristicas de la matriz.

##### First component
En order para maximizar la varianza, el primer vector de peso $w_{(i)}$ esta satisfecho por:
$$w_{(i)}=arg~max_{\mid\mid w\mid\mid=1}\left\lbrace\sum\limits_{i=1} ^{N}(t_{1})^{2}_{(i)} \right\rbrace=arg~max_{\mid\mid w\mid\mid=1}\left\lbrace\sum\limits_{i=1}^{N}(x_{(i)}*w)^{2}\right\rbrace=arg~max_{\mid\mid w\mid\mid=1}\{\mid\mid Xw\mid\mid^{2}\}$$
$$=arg~max_{\mid\mid w \mid\mid=1}\{w^{T}X^{T}Xw\}$$

Desde $w_{(i)}$ es definido como un vector unitario es equivalente:
$$w_{(i)}=argmax\left\lbrace\frac{w^{T}X^{T}Xw}{w^{T}w}\right\rbrace$$

La cantidad a ser maximisada puede ser reconocido como **Rayleigh quotient.** Un resultado estanda para una matriz positiva semidefinita 