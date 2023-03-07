## Medidas de dependecia

##### Varianza cruzada
Se define como:
$$\gamma ~xy(s,t)=cov(X_{s},Y_{T})=\mathbb{E}[(X_{s} -\mu_{xs})(Y_{T}-\mu_{xt})]$$

Mide para medir la varianza entre dos series de tiempo con distinto tiempo.

#### Correlación cruzada
va a estar en terminos de x y y de covarianza de x y covarianza de y
$$P_{xy}(s,t) =\frac{\gamma~xy (s,t)}{\sqrt{\gamma x(x-\mu)\gamma~Y(y-\mu)}}$$

#### Datos estacionarios
Nos sirve para hacer forecasting y los modelos asumen que estan estacionarios los datos

###### Datos estacionarios estricotos
En esta coleeccion de datos, tenemos qe todas las variables aleatorias son las mismas que si las aplicamos un shift al conjunto de variables aleatorias. Esto tiene que funcionar para cualquier tiempo.

Todas las variables son un muestreo de la misma distribuciondeprobabilidad con la misma media.

##### Estacionariedad debil, de segundo orden o amplio
Se va a tomar la definicion de estacionaridad fuerte, pero relajando las condiciones.

1. La media $\mu$ de la funcion es constande y no depende del tiempo
2. La varianza $\sigma_{x}$ es finita para todo el tiempo
3. La función de autocovarianza $\gamma(s,t)$ depende de s y y con la diferencia igual a uno $\mid s-t\mid$


##### Autocovarianza y autocorrelacion de una serie estacionaria
La funcion de autocovarianza de una serie de tiempo puedeser escrita como:
$$\gamma~(h)=cov(X_{t+h},X_{t})=\mathbb{E}[(X_{t+h}-\mu)(X_{t}-\mu)]$$

La funcion de autocorrelacion de una serie estacionaria puede ser escrita como:
$$p(h)=\frac{\gamma~(y+h,t)}{\sqrt{\gamma~(t+h,t+h)\gamma~(t,t)}}=\frac{\gamma(h)}{\gamma(0)}$$

#### Modelos estadisticos de estacionaridad
Excersises.
Contesta las siguientes preguntas.
1. ¿El ruido blanco es estacionario? La media es igual, la varianza es finita
2. ¿La caminata aleatoria con drift es estacionaria? No es estacionaria porque la media depende del tiempo


#### Trend stationarity
Es un un proceso estocastico si tiene una linea de tendencia baja puede ser removida, leaving a stationary process. Meaning the process can be expressed as: $y_{t}=f(t)+X_{t}$ 

Donde **f(t)** es una funcion $f:\mathbb{R}\rightarrow\mathbb{R}$ 

#### Estacionariadad por temporadas
Esta en termino de las distribuciones de probabilidad, donde $m\in\mathbb{Z}$ y $P\in\mathbb{N}$ es el periodo del proceso:
$$P_{r}(X_{t1},\cdots,X_{tn})=P_{r}(X_{t+p},\cdots,X_{t+p})$$

#### Importancia de los estimadores estacionarios


##### Estimacion del valor esperado.
Algunas veces no contamos con la funcion de distribucion y la unica informacion del conjunto son las muestras de la distribucion (o un conjunto de ejemplos con la misma media) despues lo estimamos usando la media que usaremos.

$$\hat{x}=\frac{1}{N}\sum\limits_{i=1}^{N}X_{i}$$

Aqui $\mathbb{E}[\hat{X}]=\mu$ y la desviacion estandar es el square root of $var(\hat{X})$ por que la estimacion puede ser verdadera donde la distribucion de probabilidad no es uniforme.

#### Estimacion de la varianz
puede ser comutada como:
$$s^{2}(X)=\frac{1}{N}$$

##### Función de auto covarianza
Puede ser definida como:
$$\hat{\gamma}(h)=\frac{1}{N}=\sum\limits_{t=1}^{N-h} (X_{t+h}-\hat{X})(X_{t}-\hat{X})$$

con $\hat{\gamma}=\hat{\gamma}(-h)~for~h=0,1,\cdots,N-1$ 
Esta funcion es simetrica, para h positiva como negativa, para evitar el sego tendriamso que dibidira entre $N-H-1$ o sollo entre $N-H$.

La funcion de autocovarianza $\gamma(h)$ es un proceso estacionario es definida no negativa ensuring that variances of linear combinations of the variates $X_{t}$ nunca sera negativa, entonces ,esta estimacion.

#### Calcular la autocorrelacion de manera sampleada
Puede ser definida como: 
$$\hat{p}(h)=\frac{\hat{\gamma(h)}}{\hat{\gamma}(0)}$$
se puede estimar todo siempre y cuando asumamos que los datos son estacionarios.

#### Large-Sample distribution of the ACF
Bajo las conidciones generales: si $X_{T}$ es ruido blanco para cada n large, el ejemplo ACF$\hat{p_{X}}(h)$ para $h=1,2,\cdots,H$ donde H es fixed but arbitrary es aproximada a la distribucion normal con media cero y lllllla desviacion estandar esta dada por:

$$\sigma_{\hat{p}x}=\frac{1}{\sqrt{N}}$$

Basado en los resultados previos, we obtain a rough method of assesing if peaks in $\hat{p}x$ son significantes para dterminar si estan fuera del intervalo $+-2\sigma_{\hat{p}x}$ 