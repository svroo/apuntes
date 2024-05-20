En las cruces ponemos la duración de las tareas, es decir los tiempos más cercanos o más lejanos de términos, la comprobación es la suma del inicio y fin, debe ser igual a cero.

Hacia atrás:
Tiempos tardíos (define ruta crítica)

se toma el más pequeño para empezar a llenar la parte de atras


Los nodos sin holgura serán la ruta critica.


#### Pasos a seguir (PERT)
1. Diagrama de Red
2. Determinar holguras
3. Ruta Critica


### Actividad
a) Dibujar el diagrama de red PDM.
b) Calcular la ruta critica, tiempos ASAP y ALAP de cada actividad.
c) Calcular las holguras totales y libres

| Actividad                                | ID. | Predecesor | Días |
| ---------------------------------------- | --- | ---------- | ---- |
| Identificar las necesidades del cliente. | A   | Ninguna    | 2    |
| Escribir y enviar propuesta              | B   | A          | 1    |
| Obtener aprobación                       | C   | B          | 1    |
| Desarrollar la consultoría               | D   | C          | 2    |
| Capacitación                             | E   | C          | 5    |
| Evaluación de resultados                 | F   | D,E        | 5    |
| Escribir reporte final                   | G   | F          | 1    |