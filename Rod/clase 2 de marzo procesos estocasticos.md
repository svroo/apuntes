ver pelicula: talentos ocultos

Habilidades
1. Modelo
2. Programarlo
3. conceptos
4. sdf


x distancia del centro de la aguja a la linea paralela más cercana
$\theta$ ángulo que forma la agua con las lineas paralelas.

Rango de variabilidad de x:
$$x\in\left[0,\frac{t}{2}\right]$$

Rango de variabilidad de $\theta$:
$$\theta\in\left[0,\frac{\pi}{2}\right]$$

son variables que dependen del experimento.

Se puede gráficar su funcion de proabilidad, con base de $0~a~\frac{t}{2}$ y su altura de $\frac{2}{t}$ con una funcion de proabilidad de $f_{x}(x)=\frac{2}{T}$ 

La funcion de proabilidad para $\theta=f_{\theta}(\theta)=\frac{2}{\pi}$ con una distancia de $\frac{\pi}{2}$ y altura de $\frac{2}{\pi}$ 

Tenemos como condición para que la aguja cruce alguna linea paralela (hits), la condicion de corte es agarrar $\ell$ y proyectar verticalmente su imagen, usamos el seno para encontrar la proyección. La condición de cruce esta dado por: 
$$\frac{\ell~sen(\theta)}{2}$$
La condicion de cruza es:
$$x\leq\frac{\ell~sen(\theta)}{2}$$

Como tenemos dos ariables podemos calcular la funcion de densidad conunta de $x,\theta$ que es igual a la multiplicacion de ambas funciones.
$$f_{x\theta}(x,\theta) =\frac{4}{T\theta}$$

Proabilidad de que la agua cruze alguna linea paralela:

$$\int_{0}^{\frac{\pi}{2}}\int_{0}^{\frac{\ell}{2}sen(\theta)}\frac{4}{\pi T}~dx~d\theta$$

$$=\frac{4}{\pi t}\int_{0}^{\frac{\pi}{2}}\left( \int_{0}^{\frac{\ell}{2}sen(\theta)} dx\right)~~d\theta=\frac{4}{\pi~t}\int_{0}^{\frac{\pi}{2}}\frac{\ell}{2}sen(\theta)~d\theta=\frac{2\ell}{\pi~t}\left[-cos(\theta)\right]=\frac{2\ell}{\pi~t} =aprox~~\frac{h}{n}$$

despeando $\pi$ tenemos:
$$\pi=\frac{2\ell ~n}{h~t}=\frac{n}{h}$$

la condicion es que $0 <\ell \leq t$  


### Ejemplo 2
Se va a simular el lanzamiento de dardos, en un cuadrado de 2 x 2, osea con un area de 4, y un circulo con area $\pi$ se lanzan los dardos, usando numeros aleatorios que van desde -1 a 1,
$-1\leq x\leq 1$ 
$-1\leq y\leq 1$

vamos a comproar que si se acierta esta dado por:
$$\frac{\pi}{4} = \frac{na}{n}$$

Podemos despejar pi como
$$\pi=4\frac{na}{n}$$
```python 3
def pi_aprox(n):
	con = 0.0
	
	for i in range(n):
		x = 2 * random.random() - 1
		y = 2 * random.random() - 1
		if x*x + y*y < 1:
			con += 1.0
	return 4 * con / n
```
