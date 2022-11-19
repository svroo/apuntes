- Percepciones iniciales ...
	- Uno de los objetivos principales y difíciles en estadística, es **determinar** cuándo dos elementos son parecidos y cuándo no.
	- Resolver adecuadamente esta cuestión es la base de diversos procedimientos y algoritmos, desde la generación de __hipótesis__ hasta métodos de __clasificación__.
	- Entonces para ello, podemos usar la palabra ambigua **elementos**, porque a veces nos interesa comparar magnitudes escalares (**números**), pero otras veces queremos comparar obsevaciones multivariantes(**vectores**)
	- Incluso podemos necesitar saber si dos funciones se **parecen** o elementos más complicados, como imágenes, fotografías, documentos, twwets
- La idea básica se consideran los siguietes:
Formula:
$$d_{m(X,u)}= \sqrt{(X-\mu)^{T}\sum{-1}(x - \overline{x})}$$
En el caso de tener observaciones escalares en lugar de vextores, si $\overline{x}$ es la media muestrar y **s** es la desviación típica muestral, la expresión anterior es simplemente la observación estandarizada en **valor absoluto:
$$d_{M} (x,\overline{x}) = \sqrt{\frac{(x,\overline{x})^{2}}{s^{2}}} = \frac{|x-\overline{x}|}{s}$$
- Definición:
	- Es una funcion que permite determinar la **distancia** entre **dos individuos** definidos por **p variables**, en donde se consideran la **matriz** de **covarianzas** de las variables que definen a los componentes de cada individuo
- Caracteristicas
	- Su utilidad radica en que es una forma de determinar la **similitud** entre dos **variable aleatorias multidimencionales**
	- Se utiliza con variables alearorias que tienen la misma **distribución** de **probabilidad**
	- Debe cumplir con 3 propiedades para ser una distancia: 
		1) **Semipositividad**
		2) **Simetria**
		3) **desigualdad tringular**
		$$d(a,b) \geq 0~\forall~a,b\in$$

- Sea $M_{nxp}$ una matriz de datos, en donde la distancai cradrática en tre los individuos i y j de denota por $d_{M}(i,j)$ que es el valor resultante de aplicar el producto matricial:
$$d^{2}_{M}(i,j) = (x^{(i)}-x^{(j)})\sum\limits^{-1}(x^{(i)}-x^{(j)})^{T}$$
Siendo $\sum\limits$ la matriz de covarianzas muestrales $\sum\limits_{ij} = cov(x_{i},x_{j}),~i=1,\dots,p;~j=1,\dots,p$ siempre y cuando dicha matriz sea no singular (matriz inversa)

## Ejemplo
Ejemplo , considére la matriz de datos formada por 6 individuos y 4 variables:
## Examen 8 de noviembre
