## Entrenamiento y prueba
- El entrenamiento se suele dividir en dos conjuntos
- El modelo se ajusta con un conjunto distinto al de pruea
- De lo contrario no se realiza ninguna predicción

### Conjunto de entrenamiento
- El conjunto de entrenamiento es usado para *aprender* sobre las características que distinguen cada instancia de este conjunto
- Durante esta etapa se va relaizando ajustes para crear el modelo que mejor se dapate a los datos provistos
- Es importante que lasintancias includias en el conjunto de datos sean suficientes y diversas para que el modelo creado no muestre un sesgo 

### Problemas que presentan en el conjunto de entrenamiento 
- Training set pequeño -> Subajuste (underfiting). El no es capaz de encontrar un patrón que seguir para generar las predicciones
- Training set demasiado grande -> Sobreajuste (overfiting). El modelo se ajusta tanto a los datos de entrenamiento que no es capaz de predecir correctamente nuevas instancias
- El subajuste y el sobreajuste también se pueden presentar cuando las intancias del conjunto de entrenamiento no son muy diversas
- Training set desbalanceado

### Conjunto de pruebas 
- Este conjunto de datos se utiliza para verificar el rendimiento del modelo creado durante la etapa de entrenamiento
- Es importante que lasintacias del conjutno de pruebas no sean las mismas que las de lconjunto de entrenamiento
- El conjunto de pruebas no debe ser utilizado para relaizar eajustes al model oya que es sólo para verificar los resultados
- En caso de que los resutlados de esta etapa no sean los esperados se peudden volver a realizar ajustes en el model

### División del conjunto de datos en entrenamiento y pruebas
No existe un consenso generalizado sobre cómo realizar la divisón del conjunto de datos
Sin embarog , existen recomentaciones de buenas prácticas
1) Mazlar las intancias del conjutno de datos (suffle)
2) Seleccionar entre 50% a 90% de las intancias para el entrenamiento y con ellas crear un nuevo conjunto dedatos (conjunto de entrenamiento)
3) Seleccionar las instancias no seleeccionadas en el paso anterior y así crear un nuevo data set

### Generalización
- Durante el proceso de entrenamiento es importante asegurarse que el modelo creado tenga buena capacidad de generalización
- La generalización se reafiere a

### Validación cruzada
- Permite usar diferentes conjntos de datos para evaluar el rendimiento de un algoritmo de aprendizaje automático
- 
[[Aprendizaje Maquina]] 