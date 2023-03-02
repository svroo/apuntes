<div align='right'>Tema opcional: Teoria de la generalización</div>
# Is learning Feasible?

La relación entre v and $\mu$ si usamos la desigualdad de Howffiding. Para un parametro de tamaño N.
$$P[[u-\mu] >\epsilon] \leq 2_{e}^{-2_{e}^{2}~N} = \frac{2}{e^{2\epsilon^{2}~N}}$$
Con forme N se aga pequeño se va a hacer más pequeño, la unica forma de hacer que la diferencia de u-$\mu$ lo que tengo que hacer es tomar más muestras
<div align='right'>
	<p>Solo funciona con estas dos condiciones</p>
	<ul>
		<li>Independencia en muestreo
		<li> Datos tengan la misma distribución
	</ul>
</div>

Las entradas $x_{i},\dots, x_{N}$ en el **dataset** son tomadas de manera independiente de acuerdo a la distribución **P** en **X** tenemos una muestra aleatoria de:

- Red marbles $percepton\leftarrow h(x_{n})\neq f(x_{n}) \rightarrow$ credito asignado. Todos los punto donde no se acerte serán las canicas rojas.
- Green marbles $h(x_{n}) = f(x_{n})$ si aquí se acierta serán canicas verdes.

En el contexto del problema crediticio, tenemos $P_{v}(|v-\mu|>\epsilon)$ donde v = muestras ó dataset $\rightarrow$ errores en dataset y f = real, población de estudio $\rightarrow$ Errores en general

- Consider the in-sample error
$$V \leftarrow E_{in}(h) =\frac{1}{N} \sum\limits_{n=1}^{N}[h(x_{n}) \neq f (x_{n})] \rightarrow[c] $$
Si c = True $\rightarrow$ 1
Si c = False $\rightarrow$ 0

and the out-of-sample error
$$\mu\leftarrow~E_{out}(h) = P[h(x_{n})\neq f(x_{n})]$$

appling the Goeffding bound in one hypotesis
$$P[[pv-\mu]>\epsilon] = P[[E_{in}- E_{out}] >\epsilon] \leq 2e^{-2e^{2}~N }$$

### Error y ruido 
ahora vamos a revisitar dos nociones en el problema de aprendizaje en orden a introducir en el mundo real.

##### Error de medidas
Un error mide la cantidad como cada hipotesis se aproxima a la funcion objetivo f. $error = E(h,f)$ donde h es el modelo y f = la funcion objetivo.

Mientras $E(h,f)$ esta basada enteramente en h y f.

#### Targets ruidosos
En muchas aplicaciones practicas, la data de donde aprendemos generalmente es no determinista la funcion objetivo. Inmediatamente nos genera un ruido en muchas formas donde la salida no esta determinada por la entrada.

Esta situación puede ser modelada con el mismo within the sema framework that we have, instead of y=f(x) we have a traget function.

### The general supervised learning Problem

![[Pasted image 20230223093948.png]]
