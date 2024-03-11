Propiedad de uniformidad:
# Prueba de kolmogorov-Smirnov

consta de cinco pasos:
1. Generar 'n' números pseudoaleatorios uniformes
2. Ordenar dichos números en orden ascendente
3. Calcular la distribución cumulada de los números generados a través de la siguiente expresión:
$$F_{n}(x)= \frac{i}{n}$$
Donde:
$i\rightarrow$ Posición de $X_{i}$ (ordenado)
$n\rightarrow$ Cantidad números pseudoaletorios

4. Calcular el estadístico kolmogorov-Smirnov del modo siguiente:
$$D_{n}=max\mid F_{n}(x_i)-x_{i}\mid$$
5. Si $Dn < D_{ain}\rightarrow$ se acepta la $H_{0}$ 

### Ejemplo
Sea una muestra de 10 números pseudoaleatorios:
0.36, 0.82, 0.54, 0.39, 0.76, 0.94, 0.72, 0.65, 0.03, 0.18
Con $\alpha =5\%$ 
0.03, 0.18, 0.36, 0.39, 0.54, 0.65, 0.72, 0.76, 0.82, 0.94
