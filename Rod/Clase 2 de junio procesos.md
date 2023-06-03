## Cadenas ocultos de Markov
$$\lbrace Z_{n}\rbrace=estados~ocultos$$
$$\lbrace X_{n}\rbrace = estados ~(valores) ~observados$$

Los valores no observados tienen una dimensión $(n*n)$


y los valores observados tienen una dimension $(m *n)$ 

Este modelo se basa en tres pasos
1. Evaluación $P(Z_{n}, X_{1:n})$
2. Clasificación  lo que tengo son clases secuencias de estados ocultos
3. Entrenamientos $(datos\rightarrow \theta)$ 

Espacio de variables ocultas
$$\left.\begin{matrix} P(C_{1}\mid X_{1:T}) \\ P(C_{2}\mid X_{1:T} ) \\ \vdots  \\ P(C_{3}\mid X_{3:T}) \end{matrix}\right\rbrace\rightarrow clase~i $$  
### Forward
Defino alpha k
$$\alpha(k)=P(Z_{k},X_{1:k})=\sum\limits_{Z_{k-1}}P(Z_{b},Z_{k-1}, X_{1+k})$$
$$\alpha(k)=\sum\limits_{Z_k-1=1}P(X_{n}\mid Z_{n})P(Z_{k}\mid Z_{k-1})\alpha(k-1)$$
$$=\sum\limits_{Z_{k-1=1}}P(X_{k}\mid Z_{h},Z_{k-1},X_{1:h-1})$$
$$P(Z_{n},Z_{h-1},X_{1:k-1})$$
$$P(Z_{k\mid}Z_{k-1})$$
$$P(Z_{k}\mid Z_{h-1},X_{1:h-1})$$
$$P(Z_{p-1},X_{1:k-1})$$

paso numero uno defino
paso numero 2 desmarginalizar

$$\alpha(k)=P(Z_{n},X_{1:k})$$
$$\alpha(k)=\sum\limits_{Z_{k-1=1}}P(Z_{k},Z_{k-1},X_{1:k})$$
$$=\sum\limits_{Z_{k-1=1}}P(Z_{k},Z_{k-1},X_{k},X_{1:k-1})$$
$$=\sum\limits_{Z_{k-1=1}}P(X_{k}\mid Z_{k},Z_{k-1},X_{1:k-1})P(Z_{k},Z_{k-1},\cdot, Z_{1:k-1})$$
$$=\sum\limits_{Z_{k-1=1}}P(X_{k}\mid Z_{k})P(Z_{k}\mid Z_{k-1},X_{1:k-1})P(Z_{k-1},X_{1:k-1})$$
donde:
$$P(Z_{k}\mid Z_{k-1},X_{1:k-1})=P(Z_{n}\mid Z_{k-1})$$
reescribiendolo todo tenemos:
$$\alpha(k) = \sum\limits_{Z_{k}-1=1}P(X_{k}\mid Z_{n})P(Z_{k}\mid Z_{k-1})\alpha(k-1)$$

$$\alpha(1)=P(Z_{1},X_{1})P(Z_{1})P(X_{1}\mid Z_{1})$$

pelicula:
Con ganas de triunfar