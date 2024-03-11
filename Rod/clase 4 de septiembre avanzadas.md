norma de un vector:

```python 3
def norma(arr):
	aux = 0
	for element in arr:
		aux += (element ** 2)
	return sqrt(aux)
```

![[Pasted image 20230904152656.png]]
Si el resultado es 0 es que son parecidos, si llegamos a 180 quiere decir que no se parecen en nada

Demostrar que:
- $(\alpha + \beta)A = \alpha A + \beta A$
para todos los casos

Investigar de que tamaño tienen que ser las matrices para poder multiplicarlas

Para multiplicar dos matrices, se debe cumplir una condición muy importante: el número de columnas de la primera matriz debe ser igual al número de filas de la segunda matriz. Por ejemplo, si tenemos una matriz A de tamaño m×n y una matriz B de tamaño n×p, entonces el producto AB estará definido y resultará en una matriz de tamaño m×p. En otras palabras, las dimensiones interiores deben coincidir para que la multiplicación sea posible.

