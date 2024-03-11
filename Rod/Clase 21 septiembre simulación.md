<div aling='right'><h3>Clase 21 de septiembre del 2023</h3></div>
## Práctica Problema del viajero
- Como viajan las aves
- Distribución de hormigas
- Envios de paquetes
- Migración de las aves
### Pruebas de bondad de ajuste

También llamadas pruebas de aleatoridad. Las pruebas para números pseudoaletorios son pruebas estdísticas para decidir si una determinadda muestra o conjunto de datos responde a un patrón o se comportan de forma aleatoria.

Es importante asegurar que el generador usado busque una secuencia suficiente aleatoria, por ello es importante someter a estos generadores a dichas pruebas estadísticas.

Sim embargo este tipo de pruebas no son decisivas, debido a que un generador puede pasar una prueba estadística, pero si por ejemplo se cambia la semilla u otro segmento del ciclo, puede no pasar la misma prueba.

Hasta ahora se han presentado diversos algoritmos para construir un conjunto de números pseudoaleatorios. Sin embargo esto sólo es el primer paso, ya que este conjunto debe ser sometido a varias pruebas

- ¿De que forma se puede garantizar que tales números son realmente aleatorios \[entre 0 y 1\]?
- ¿Cuáles son las características que los identifican?
- ¿Cuáles son sus parámtreos?

La respuesta a estos cuestionamientos adquiere relevancia, dado que los número aleatorios serán utilizados en simulación para generar los valores de cualquier variable aleatoria.

##### Objetivos
- Conocer las pruebas estadísticas que deben aplicarse a un conjunto de números pseudo aleatorios antes de usarse para un modelo de simulación.
- Aplicar las pruebas estadísticas de uniformidad y de independencia a un conjunto ri de números pseudo aleatorios.
- Validar que el conjunto ri de números realmente está conformado por números aleatorios o no: a un nivel de confianza alfa $(\alpha)$ usando pruebas estadísticas

Hasta ahora hemos graficado las secuencias de núemros aleatorios para evaluar su aleatoriedad, sin embargo, el oo humano no es muy bueno discriminando aleatoriedad y las gráficas no escalan

Es por ello que resulta conveniente hacer pruebas estadísticas pra evaluar la calidad de los generadores.

Hay dos tipos de pruebas:
- **empíricas**
- **Teóricas**

El objetivo, en otras palabras, es validar que el conjunto ri realmente esta conformado por números aleatorios. Es importante mencionar que las pruebas que se mencionarán no son únicas.

## La prueba del promedio
Consiste en verificar que los números generados tengan una media estadíticamente igual a $\frac{1}{2}$, de esta manera, se analiza la siguiente hipótesis:
$$h_{0}=\mu = \frac{1}{2}$$
$$h_{1}:\mu \neq \frac{1}{2}$$

- Paso 1
Calcular la media de los n números generados.

- Paso 2
Calcular los límites inferior y superior de aceptación:
$$li_{x}= \frac{1}{2}-z_{\frac{a}{2}} \left(\frac{1}{12\sqrt{n}}\right), ~~~~ls_{x} = \frac{1}{2}+z_{ \frac{a}{2}} (\frac{}) $$


**Ejemplo**