### Logistic regression
La tarea es tratar de predecir una probabilidad, solo producimos valores entre mas uno y menos uno. 

Lo que hacemos es definir un nuevo modelo, la salida esta en el rango de $[0,1]$. One choice that accomplishes this goal is te logistic regression model.
$$h(x) = \theta(w^{T}x)$$

Funcion sigmoide :
$$\theta(s)=\frac{e^{s}}{1+e^{s}}$$

En este caso el objetivo es una probabilidad que depende de la entrada x. Formalmente estamos tratando de aprender de la funcion objetivo.
$$f(x)=Pr[y =+1][x]$$

El error que vamos a usar entre nuestra hipotesis y nuestro erro, estara basada en la nocion de umbral.

### Gradiente decendente
Es una técnica pra minimizar una funcion que es dos veces diferenciable, como $E_{in}(w)$ en la regresion logistica.

Tenemos una analogia en fisica con el gradiente descendiente, si lo vemos como una pelota que va rodando colina abajo, ig the ball is placed on a hill, it will roll down, coming to rest at the bottom of a valley.

### Excersise
El gradiente descendiente es un algoritmo general para minimizar funciones dos veces diferencialbe. Podemos aplicarlo a la regresion logistica en el error de entrenamiento para retornar el peso para minimizar aproximadamente.

$$E_{in}=\frac{1}{N} \sum\limits_{n=1}^{N}ln(1+e^{-y})$$

# Evaluacion
Prácticas $\rightarrow$ 50%
Examen $\rightarrow$ 50%

Examen en equipo aleatorio y perminitiendo el uso de libro, duración una hora

Fecha examen : 27 - 31 marzo
Revision avances proyecto: 3 - 5 abril