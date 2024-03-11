### Propiedades básicas
Un programa lineal (PL) es un problema de optimización en el cual la función objetivo es lineal en las incógnitas y las restricciones consisten en ecuaciones lineales e inecuaciones lineales.

La forma exacta de ests restricciones puede variar de un problema a otro, pero como se muestra a continuación, cualquier programa lineal puede ser transformado a la siguiente forma estándar.

$$\begin{matrix}minimize&c_{1}x_{1}+c_{2}x_{2}+\cdots+c_{n}x_{n} \\ Subject~to&a_{11}x_{1}+a_{12}x_{2}+\cdots+a_{1n}x_{1}\leq b1 \\ &a_{21}x_{2}+a_{22}x_{2}+\cdots+a_{2n}x_{n}\leq b2 \\ &\vdots ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\vdots \\ &a_{m1}x_{1}+a_{m2}x_{2}+\cdots+a_{mn}x_{n}\leq b_{m} \\ and&x_{1}\geq 0,x_{2}\geq 0,\dots,x_{n}\geq0\end{matrix}$$


Donde los $b_{1},c_{i}$ y $a_{ij}$ son constantes reales fias
Los $x_{i}$ son números reales por determinar
Siempre asumimos que cada ecuación ha sido multiplicada por menos uno, si es necesario, de modo que cada $b_{i}$ sea mayor o igual a cero

En una notación vectorial más compacta, este problema estándar se convierte en:

$$\begin{matrix} minimize & c^{T}x \\ subject ~to&Ax = b~~and x\geq0\end{matrix}$$

Aquí x es un vector columna de n dimensiones

