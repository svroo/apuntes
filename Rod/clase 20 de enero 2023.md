Método de evaluación, practicas y/o examenes.


### Probabilidad y Estadistica.

#### ¿Que son las series de tiempo?
Es una forma especifica de analizar una secuencia de datos coleccionados en un intervalo de tiempo
El analisis puede mostrarnos como las variables cambian sobre en tiempo. Por ejemplo:
- Stock Market $\leftarrow$ 1 day
- weater 

##### Caracteristicas de las series de tiempo
- Correlacion entre cada uno de los puntos
- Análisis del dominio de tiempo
- Análisis del dominio de la frecuencia.

### ¿Que es una serie de tiempo?
Puede ser definida como una coleccion de variables aleatorias indexadas acore al valor obtenido en el tiempo. $(x_{1}, x_{2}, x_{3}\dots, x_{N})$ 

### Modelos estádisticos para series de tiempo
El objetivo primario del analisis de las series de tiempo es desarrollar modelos matemáticos que dan descripcicones del fenomeno.

### Modelo del ruido blanco
Hace referencia a variables aleatorios que no estan relacionadas entre ellas, con media 0 y finitas variaciones $\sigma^{2}_w$. La serie detiempo generada desde la incorrelacion de las variables es usada como un modelo de ruido y es llamado ruido blanco.

$$w_{t} i-i-dN(0,\sigma^{2}_{w})$$ 
#### Medias moviles y filtrado
El segundo modelo estadistico es medias moviles. Es usuada usualmente para suavisar las series de tiempo.
$$Y_{t}=\frac{X_{1}+X_{2}+\dots+X_n}{n}$$

### Autoregresiones
El siguiente modelo estadistico es la autoregresion. Si queremos expresar un valora futuro en termino del pasado este modelo es la opción.
$$X_{t}= \phi_{1} X_{t-1}+\phi _{2}X_{t-2}+\dots+\phi_{p}X_{t-p} +W_{t}$$

### Caminata aleatoria con drift
El modelo para análizar la tendencia de la caminata aleatoria esta dado por:

$$X_{t}= \delta + X_{t-1}+W_{t}$$

para $t=1,2,\dots$ con una condicion inicial $X_{0}=0$. La constante $\delta$ es llamada **the drift**, y cuando $\delta = 0$ es llamado una caminata aleatoria simple. Puede ser escrita como:

$$X_{t} = \delta t + \sum_{j=1} ^{t}W_{t}$$

### Señal en ruido
Many realistic models for generating time series assume an underlying signal with some consistent peridoic variation.

$$X_{t}=Acos(2~\pi~\omega~t) +W_{t}$$
$$\omega = \frac{1}{\# pasos~de~tiempo~x~~ciclo}$$

