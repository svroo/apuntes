Tipos de clasificaciones
- Clasificación binaria
- Clasificación multiclase
- Clasificacion multietiqueta

### Metricas de optimización
Durante la fase de aprendizaje podemos usarlas para optimiza nuestro modelo, la metrica que utilizaremos depende el modelo que vayamos a utilizar y también si la metrica es apropiada para la tarea.

- **Entropia:** Mide la incertidumbre en la información
- **Kullback-Leibier divergence:** Usada para medir la distancia entre dos distribuciónes de probabilidad
- **Entropia cruzada:** Una mezcla de la divergencia KLy la entropia
- **Gini coefficient:** Mide la desigualdad en la población 
- **Mean squared error:** Mide la distancia entre dos puntos.

Metricas de evaluación
Sensitivity (recall):
$$Sensivit=\frac{TP}{TP+FN}$$

Specifity:
$$specifity=\frac{TN}{TN+FP}$$

Precision:
$$Precision=\frac{TP}{TP+FP}$$
$F_{1}$ score:
$$F_{1}=\frac{2}{\frac{1}{Precision}+\frac{1}{Recall}}=2\frac{Precision*Recall}{Precision + Recall}$$

Acuracy:
$$Acuracy =\frac{TP+TN}{TN+TP+FP+FN}$$

# KNN 
Es un algoritmo no parametrico de aprendizaje supervisado.
