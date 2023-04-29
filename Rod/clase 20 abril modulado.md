## Determinar distancias
En orden para determinar que puntos de los datos estan más cerca. to a giben query point, the distance between.

#### Minkowski Distance
La distancia es un una manera generalizada de la distancia Euclididan y la distancia de Mangattan. El parametro, p, en la formula de abajo. allows for the creation of other distance metrics
$$\left(\sum\limits_{i=1}^{n}\mid x_{i}-y_{i}\mid^{p}\right)^\frac{1}{p}$$
### Distancia de Hamming
Esta tecnica es usado tipicamente con vectores boleanos o de caracteres, identificamos los puntos donde los vectores no concuerda. As a result it has also been referred to as the overlap metric
$$\sum_{i=1}^{n}[[x_{i}\neq y_{i}]]$$
$$[[False]]=1~~[[True]]==0$$
### Cosine Distance
Esta metrica de distancia es usado para calcular la similaridad entre dos vectores. Esta medida mide al angulo entre losdos vectores y determinar cualde los vectores apuntan a la mismadirección. Es usado aveces para medir la similaridad de documentos en el analisis de textos.
$$\frac{1}{||x||~||y||}\sum\limits_{i=1}^{n}x_{i}*y_{i}$$

### Definir k 
El valorde k en el algoritmo **KNN** define cuandos vecinos van a ser checado para determinar la clasificación de un punto en especifica. Por ejemplo si $k=1$ la instancia sera asignado a la misma clase que el vecino más cercano. Defining k can be a balancing act as differentes values can lead to overfiting or undefiting

Lower values of K can have hig variance, but low bias, and larger values of k may lead to high bias and lower variance.

