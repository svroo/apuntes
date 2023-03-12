## El modelo lineal
Vamos a tener tres problemas principalmente, el problema de clasificacion, el problema de regresion y el problema de la probabildda estimada.

### Clasificacion lineal
El modelo lineal para clasificar los datos, vamos ausar un hipotesis, donde h tiene la forma:
$$h(x)=sign(w^{T}x)$$
Donde w va a ser un vector de pesos y la x las caracteristicas que al meterlo a la funcion nos va a dar si es menos uno o uno.

para alguna columna de vector $w\in\mathbb{R}^{d+1}$ donde d es la dmension de la entrada de espacio.

El mayor problema es que solo funciona para datos que si pueden ser separados linealmente.

Los datos que no son linealmente seprables puede ser a causa de los outlieers o el ruido, para encontrar la hipotesis que minimisa el $E_{in}$ necesitamos resolver el problmea de optimizacion combinatoria:

$$min~E_in(w)=min_{w\in\mathbb{R}^{d+1}} \frac{1}{N}\sum\limits_{n=1}^N[sign(w^{T}x_{n}\neq y_{n})$$

La dificultad en resolver este problema arises from the discrete nature of both sign(**) and [**]

# The pocket Algorithm

1. Set the pocket weight vector $\hat{w}$ to $w(0)$ of PLA
2. For $t=0,\cdots,T-1$ do
	1. Run PLA for one update to obtein $w(t+1)$
	2. Evaluate $E_in(w(t+1))$
	3. If $w(t+1)$ is better than $\hat{w}$ in terms of $E_{in}$ set $\hat{w}$ to
3. Finish

