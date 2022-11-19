En la práctica se requiere resolver problemas que implican conjutnso de variables que están correlacionadas.
- El rendimiento de combustible esta realcionado con su volumen 
- El precio de una casa esta relacionado con el tamaño de su terreno

### Relacion no determinista
Ejemplo:
- Autos con motores del mismo volumen pueden tener distinto rendimiento de combustible
- Casas con la misma superficie de construcción distintos precios
Componente aleatorio relacionado no otras variables independientes o incluso elementos desconocidos.

<center> <h3> Pronóstico estimado o ajustado </h3></center> 
realcion lineal:
$$y = b_{0}+b_{1}x$$
$b_{0}= intersección$
$b_1 = pendiente$
$b_{0}$ y $b_{1}$ son los coeficientes de valores reales que el modelo debe aprender

### Error de estimación
Cada recta rde regresión que elijamos para modelar los datos tendrá asociada una suma del error respecto a la recta de regresión estimada: $$\sum_{i=1}^{n}= (y_{i}-\overline{y}_{i})^{2}$$
| Reducción de sólidos, x $(c/x)$ | Reducción de la demanda, y $(c/0)$|
| ---------------------------|---------------------------------------|
|3 | 5|
| 7 | 11|
| 11 | 21|
|15 | 16|
|18 | 16|
| 27| 28| 
|29|27|
|30|25|
|30|35|
|31|30|
|31|40|
|32|32|
|33|34|
|33|32|
|34|34|
|36|37|
|36|38|
|36|34|
|37|36|
|38|38|
|39|37|
|39|36|
|39|45|
|40|39|
|41|41|
|42|40|
|42|44|
|43|37|
|44|44|
|45|46|
|46|46|
|47|49|
|50|51|

- Encuentra los valores de $b_{0}$ y $b_{1}$ 
- ¿Cuál es la recta de regresión estimada $y_i$?

### Clase 10/11/22

Regresión Lineal

|Tamaño|precio|
|--|--|
| 60| 1.1|
| 70| 1.5|
|100|1|
|120|2|
|$\vdots$|$\vdots$ 

$Precio = b_{0} + b_{1}$ tamaño
$y(x)=b_{0}+b_{1}x$
$y(x)= b_{0}+b_{1}x$

La hipotesis sería $b=\begin{bmatrix} b_{0}\\b_{1}\end{bmatrix}$ 

$$h_{b}(x)=b_{}+b_{1}x$$
$$h(x) = b_{0}+b_{1}x$$
Se vuelve un problema de optimización ya que queremos minizar la suma de cuadrados y queda de la forma:
$$\sum_{i=1}^{m} \limits{e^{2}} = \sum_{i=1}^m\limits{y_{i}-\overline{y} _{i}}$$
$$\sum_{i=1}^{m} (y_{i}-b_{0}-b_{1}x_{i})^{2}$$
$$\frac{\partial}{\partial b_{0}} \sum_{i=1}^{m} (y_{i}-b_{0}-b_{1}x_{i})^{2}=0$$
$$\frac{\partial}{\partial b_{1}} \sum_{i=1}^{m} (y_{i}-b_{0}-b_{1}x_{i})^{2}=0$$
$$\frac{\partial}{\partial b_{0}} \sum_{i=1}^{m} (y_{i}-b_{0}-b_{1}x_{i})^{2}= 2 \sum_{i=1}^{m} (y_{i}-b_{0}-b_{1}x_{i}) * (-1) = -2 \sum_{i=1}^{m} (y_{i}-b_{0}-b_{1}x_{i}) \rightarrow 1$$
$$\frac{\partial}{\partial b_{1}} \sum_{i=1}^{m} (y_{i}-b_{0}-b_{1}x_{i})^{2}= 2 \sum_{i=1}^{m} (y_{i}-b_{0}-b_{1}x_{i}) * (x_{i}) = -2 \sum_{i=1}^{m} (y_{i}-b_{0}-b_{1}x_{i}) * (x_{i})\rightarrow 2$$


### Regrecion lineal mediante minimos cuadrados ordinarios (OLS)

<div align='right'><p>14/11/2022</p></div>

$$w_{o}= \frac{\sum_{i=1}^{n}y_{i}-w_{1}\sum_{i=1}^{n}x_{i}}{n} $$

- A pesar de su sencillez, este método es capaz de rosolver correctamente problemas de regresión lineal
- La desventaja de este método es que su costo computacional ($n^{3}$) no permite aplicarlo a conjntos de datos grandes que tengan muchas instancias y variables (características)
- También tiene dificultades cuando las variables independientes presentan multicolinealidad entre ellas, esto es que están correlacionadas
- Las variables indpendientes (características) deben tener correlación con la salida (target) pero no entre ellas.
#### Gradiente descendiente
w = cualquier punto en el espacio de parámetros

Mientras no converja hacer 
	Para cada $w_{i}$ en w hacer
	
	$$w_{i}=w_{i}-a \frac{\partial}{\partial w_{i}}f(w)$$

#### Derivacion de la funcion de pérdida
$$F(x) = \sum_{i=1}^{m} (h_{w}(x_{i})-y_{i}) ^ {2} ~~~~~~~~~ f(w) = \sum_{i=1}^{m}(w.x-y)^2$$
$$\frac{\partial }{\partial w} \sum_{i=1}^{m}(w*x-y)^{2}$$


#### Funcion de pérdida Error cuadrado medio

$$\frac{1}{m} \sum_{i=1}^{m}(w*x-y)^{2}$$

```python3
import matplotlib.pyplot as plt
import sys

def F(w,X,y):
	return (sum(w*x-y)**2 for x,y in zimp(X,y))

def dF(w,X,y):
	return (())
```



[[Aprendizaje Maquina]] 