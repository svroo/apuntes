```python 3
u = np.random.norma(0,1,100)

b_0, b_1 = _ , _
x = np.linespace(0,5, 100)
y = np.exp(b_0 + b_1 * x + u)
delta_x = 1e-6

delta_y = b_0 + b_1 *(x+delta_x) - y

assert  delta_y.mean() == 100 * b_1 * delta_x
```

$$100 \cdot \frac{\Delta y}{y}  = 100 \cdot \beta_{1}x$$


<div align='right'><h3>08/09/2023</h3></div>

el cambio en el salario se verá reflejada en el cambio en la educación por $\beta_1$

$$\Delta wage=\beta_{1}\Delta e$$

si se despeja $\beta_{1}$:
$$\frac{\Delta w} {\Delta e} = \beta_{1}$$
que es lo mismo que se obtiene si sacamos la derivada.

La razón de cambio que quiero es:
$$\frac{\Delta w}{\Delta e}\approx \frac{\partial w}{\partial e}$$
resolviendo tenemos:
$$\frac{1}{w}~\frac{\partial w}{\partial e} = \beta_{1}$$
y vamos a decir que:
$$\frac{\Delta w}{\Delta e}\approx \frac{\partial w}{\partial e} \rightarrow \frac{1}{w}\frac{\Delta w}{\Delta e}\approx \beta_{1}$$
$$\frac{\Delta w}{w} \approx \beta_{1}\Delta e$$
al hacer esa operación  es lo mismo que hacer:
$$\frac{1}{100}=0.001 = 1\%$$
que es lo mismo que decir:
$$\%\Delta w \approx 100~ \beta_{1}~\Delta e$$

## Unbiasedness of ols
In the population mode, the dependant variable, **y**, is related to the independ variable:

$$y=\beta_{0}+\beta_{0}x+u$$

y queremos provar que los minimos cuadrados$(\beta_{0},\beta_{1})$

# modificación
Cambiar el muestreo de 2000 puntos por más puntos.

```python 3
def pop_random.sampling(n, b_0, b_1, ):
"""
n = numero de muestras
modelo = [b_1, b_0]
"""
u = np.random.normal(0, scale =1, size = n)
x = np.random.uniform(-3, 3, size = n)

y = m[0] + m[1] * x + u
return x, y
```



## Practica 2
```python 3
fitted.models = b_0, b_1 #arrays de numpy
vars = fitted.models.var(axis=0)


```