Nombre: Grace Proaño
El  trabajo tiene como finalidad seleccionar un modelo que sea capaz de identificar si un paciente tiene cancer o no. Para esto se utilizo el dataset Breast Cancer Wisconsin (Diagnostic). El  trabajo se ha desarrollado de la siguiente manera.
1. Importacion de Librerias: Las bibliotecas se han integrado progresivamente durante el desarrollo del código. Dentro de las principales bibliotecas se han utilizado numpy para manipulación de matrices, matplotlib y seaborn para visualización, y sklearn para generar los modelos de aprendizaje y sus respectivas metricas.
2. Lectura de archivos con extension .data y .names, para poder leerlos  primero revisaremos el contenido de cada uno de estos archivos para entender su estructura y formato, el archivo .name
contiene  informacion  sobre el conjunto de datos, el archivo .data  contiene valores separados por comas (csv). Para facilidad de manupilacion se transformo en un df de pandas
3. Se realiza una analisis exploratorio de datos  para proceder con la manipulacion, en este caso se verifica si tenemos datos outliers y/o NAN para proceder a limpiarlos, sin embargo no los hay. Se presenta un grafico para conocer la cantidad de la variable objetivo.
4. Se procede a realizar una matriz de correlacion para las caracteristicas del conjunto de datos y conocer si tenemos variables que tengan relacion , en este caso al aplicar la matriz se puede observar que tenemos variables que tienen  fuertes relaciones por lo que es util aplicar PCA , lo que nos permitira reducir la dimensionalidad  del conjunto de datos conservando una varianza del 95% de la varianza original.
En este caso se redujo de 30 caracteristicas originales a 10 principales  sin perder mucha informacion.Finalmente se crea un uevo dataframe con los datos a trabajar
5. A continuacion se realiza la division de datos de entrenamiento y validacion de manera aleatoria con el 20% de los datos para el conjunto de validacion y el resto para el entrenamiento.
6. Procedemos a aplicar 3 modelos de los cuales elegi regresion logistica ,SVM y KNN. Estos modelos fueron seleccionados ya que son ampliamente utilizados en aprendizaje supervisado.
7. Se fue variando manualmente varios hiperparametros de cada uno de los modelos , para de esta manera obtener el de mejor precision y rendimiento.
8. De los modelos empleados los que mejor accuracy  tuvieron  fue regresion logistica y SVM con un valor de 98.25%  a diferencia de KNN que tuvo 95.61% . Es importante mencionar que en el modelo de regresion logistica use una tecnica de scikit-learn  (GridSearch) que permite una optimizacion automatica de los hiperparametros , con el objetivo de encontrar la combinacion de parametros que resulte en el mejor rendimiento del modelo , el cual me dio el 99.12%. 
   

