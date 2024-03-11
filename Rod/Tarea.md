1. Dado el siguiente conjunto de datos, donde cada fila representa una observación de cuatro variables, calcule la media y la desviación estándar de cada variable:
$$data=\begin{bmatrix}\begin{bmatrix} 2, 4, 6,8\end{bmatrix}, \\ \begin{bmatrix}1,3,5,7\end{bmatrix}, \\ \begin{bmatrix} 0, 2, 4, 6\end{bmatrix}, \\ \begin{bmatrix}3,6,9,12\end{bmatrix} \\ \begin{bmatrix}2,5,8,11\end{bmatrix} \end{bmatrix}$$

Desarrollo:

Primera fila:
$$\mu = \begin{bmatrix} 2&4&6&8\end{bmatrix} = \frac{2 + 4+6+8}{4}=\frac{20}{4}=5$$
$$\sigma =\sqrt{\frac{\sum\limits(2-5)^{2} + (4-5)^{2}+(6-5)^{2}+(8-5)^{2}}{4}} = \sqrt{\frac{\sum\limits(-3)^{2} + (-1)^{2}+(1)^{2}+(3)^{2}}{4}} $$
$$=\sqrt{\frac{\sum\limits9 + 1+1+9} {4}} =\sqrt{\frac{20}{4}}=\sqrt{5}=2.2360$$

Segunda fila:
$$\mu=\begin{bmatrix} 1&3&5&7\end{bmatrix} = \frac{1+3+5+7}{4} = \frac{16}{4} = 4$$
$$\sigma = \sqrt{\frac{\sum\limits (1-4)^{2}+(3-4)^{2}+(5-4)^{2}+(7-5)^{2}}{4}}= \sqrt{\frac{\sum\limits (-3)^{2}+(-1)^{2}+(1)^{2}+(2)^{2}}{4}}$$

$$=\sqrt{\frac{\sum\limits 9+1+1+4}{4}} = \sqrt{\frac{20}{4}}=\sqrt{5} = 2.2360$$

Tercera fila:
$$\mu = \begin{bmatrix} 0&2&4&6\end{bmatrix} =\frac{0+2+4+6}{4} = \frac{12}{4} = 3$$
$$\sigma = \sqrt{\frac{(0-3)^{2}+(2-3)^{2}+(4-3)^{2}+(6-3)^{2}}{4}} = \sqrt{\frac{(-3)^{2}+(-1)^{2}+(1)^{2}+(3)^{2}}{4}}$$
$$=\sqrt{\frac{9+1+1+9}{4}} = \sqrt{\frac{20}{4}}=\sqrt{5} = 2.2360$$

Cuarta fila:

$$\mu = \begin{bmatrix}3&6&9&12\end{bmatrix} = \frac{3+6+9+12} {4} = \frac{30}{4} = 7.5$$
$$\sigma=\sqrt{\frac{(3-7.5)^{2}+(6-7.5)^{2}+(9-7.5)^{2}+(12-7.5)^{2}}{4}}= \sqrt{\frac{(-4.5)^{2}+(-1.5)^{2}+(1.5)^{2}+(4.5)^{2}}{4}}$$
$$=\sqrt{\frac{20.25+2.25+2.25+20.25}{4}} = \sqrt{\frac{45}{4}}  =\sqrt{11.25}=3.3541$$

Quinta fila:

$$\mu = \begin{bmatrix} 2&5&8&11\end{bmatrix} = \frac{2+5+8+11}{4} = \frac{26}{4} = 6.5$$
$$\sigma = \sqrt{\frac{(2-6.5)^{2}+(5-6.5)^{2}+(8-6.5)^{2}+(11-6.5)^{2}}{4}} = \sqrt{\frac{(-4.5)^{2}+(-1.5)^{2}+(1.5)^{2}+(4.5)^{2}}{4}}$$
$$=\sqrt{\frac{20.25+2.25+2.25+20.25}{4}}= \sqrt{\frac{45}{4}}=\sqrt{11.25} = 3.3541$$

2. Dada la matriz de correlación de cuatro variables, seleccione las variables que tienen una correlación positiva mayor a 0.7: 
$$Matrix~correlación=\begin{bmatrix} 1.0&0.6&0.8&0.3 \\ 0.6&1.0&0.4&0.1 \\ 0.8&0.4&1.0&0.6 \\ 0.3&0.1&0.6&1.0\end{bmatrix}$$

Las variables que tienen una correlación positiva mayor a 0.7 son:
- Variable 1 y Variable 3: Correlación de 0.8
- Variable 3 y Variable 1: Correlación de 0.8

Estas variables muestran una fuerte correlación positiva entre sí, lo que indica que tienden a aumentar o disminuir juntas.

3. Dados dos vectores "a" y "b" de longitud "n". Calcule el producto punto entre los vectores y la norma de cada uno.

El producto punto entre dos vectores “a” y “b” de longitud “n” se calcula sumando el producto de cada elemento correspondiente de los dos vectores. En otras palabras, si “a” y “b” son dos vectores de longitud “n”, entonces el producto punto se calcula como:

$$producto~punto = a[0]*b[0] + a[1]*b[1] + \cdots + a[n-1]*b[n-1]$$

La norma de un vector se calcula tomando la raíz cuadrada de la suma de los cuadrados de cada elemento del vector. Si “a” es un vector de longitud “n”, entonces la norma se calcula como:

$$norma~a = sqrt(a[0]^2 + a[1]^2 + \cdots + a[n-1]^2)$$

