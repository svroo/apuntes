# Números pseudoaleatorios y herramientas para su generación

El objetivo es generar sucesiones $\{u_{i}\}^{N}_{i=1}$ de números independientes ue se puedan considerar como observaciones de una distribución uniforme en el intervalo $[0,1]$ 

Los números completamente aleatorios (no determinísticos) son fáciles de imaginar conceptualmente, por ejemplo podemos imaginar lanzar una moneda, lanzar un dado o participar en una lotería.

En general los números aleatorio se basan en alguna fuente de aleatoriedad física que puede ser teóricamnete impredecible (cuántica) o prácticamente impredecible (caótica).

por ejemplo:
- *random.org* genera aleatoriedad a travésde ruido atmosférico
- *Ernie* usa ruido térmico en transistores y se utiliza en la lotería de bonos de reino unido
- *Rand corporation*


Los número pseudoaleatorios se generan de manera secuencial con un algoritmo determinístico, formalmente se define por:
- **Función de inicialización**. Recibe un número (la semilla) y pone al generado en us estado inicial
- **Función de transición** transforma el estado del generador
- **Función de salidas**. Tranforma el estado para producir un número fijo de bits $[0, 1]$


### ¿Cómo se generan los números seudoaletorios?
Se generan de manera secuencial con un algoritmo determinístico, formalmente se definen por ls funciones previamente señalados


## Algoritmo de cuadrados medios
En 1946 on Von Neuman sugirió usar las operaciones aritméticas de una computadora para generar secuencias de números pseudoaletorios

Sugirió el método *middle square*, para  generar secuencias de dígitos pseudoaleatorios de 4 digitos para arriba.

1. Se elige como **valor semilla** un número de más de 3 dígitos (t = cantidad de dígitos del varo semilla)
2. se eleva ese número al cuadrado
3. Al valor que resultó, seleccione los **t** dígitos de en medio (si se requiere, utilice un 0 como primer dígito)
4. Repetir desde el paso número 2 tomando éste nuevo número

