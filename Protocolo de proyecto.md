1. Título
2. Objetivo
	1. Lo que quiero resolver
3. Planteamiento del problema
	1. Reto técnico
4. Descripción de las fuentes de los datos
	1. Practica 2
5. Arquitectura de datos
	1. Modelo tentativo
		1. Constelacion
		2. Copo de nieve
		3. Estrella
6. Fases de procesamiento de datos
```mermaid
flowchart LR
id1[selección de datos] --> B{ETL} 
B --> id2[Cargar la arquitectura de datos] 
B --> id4[Limpieza ligera]
```
Noviembre
```mermaid
flowchart TD
B{Exploracion de datos} -->limpieza --> lattice --> id2[cubos de datos]
B --> id3[mapas, Gráficas, Nubes de palabras]
id3 --> id4[Descripcion, Clasificación, Prediccion, Modelo de ML]
id4 --> Objetivo
```
Diciembre

7. Plan de trabajo
