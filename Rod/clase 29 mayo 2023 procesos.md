## Aplicaciones de los procesos estocasticos
Quería saber cuanta información cabe a través de un canal, se dio cuenta que la información es la inversa del evento seguro:
$$I_{0}= \frac{1}{P_{0}}$$
$$I_{e}=log\left(\frac{1}{P_{e}}\right)$$
esta formulase usaba en física anteriormente y es conocida como la entropía.

$$A=\lbrace a_{1},\cdots,a_n\rbrace$$
$$\mathbb{E}[a]=\sum\limits_{i}I_{i}P_{i}=\sum\limits_{i}\left(log \frac{1}{P_{1}}\right)P_{i}=\sum\limits_{i}P_{i}logP_{i}$$

### Machine Learning
$b = (b_{1},\cdots, b_{n})$ donde $b=$ descripción y los demás son los atributos


# PCA
Es para reducir dimensiones, podemos verlo como:
$$\mathbb{E}[(x-\mu_{x}) (y-\mu_{})], \mathbb{E}[X*Y],~\mathbb{E}[X]=\mu_{x}\rightarrow\mathbb{E}[X]=0, X'=X-\mu_{x} $$
cuando su varianza es cero decimos que son ortogonales

Prueba de lo ultimo:
$$\mathbb{E}[X']=\mathbb{E}[x-\mu_{x}]=\mathbb{E}[x]-\mathbb{E}[\mu_{x}]=\mu_{x}-\mu_{x}=0$$

## Algoritmo PCA
1. Calculas los promedio de cada atributo $X_{i}$ y se restan para obtener atributos con media cero
2. Se calcula la matriz de covarianza
3. Se obtiene los vectores propios de la matriz de covarianza y se ordena de mayor a menor
4. Se usan los k vectores propios que corresponden a los primeros k valores propios para formar la matriz de transformación

### Proyecto final
1. Nombre
2. Problema a resolver
3. Objetivo general
4. Objetivos específicos
5. Aportaciones (valor agregado del trabajo).
6. Estado del arte.

- Fundamentos
- Solución propuesta
- resultados y conclusiones