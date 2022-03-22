# DeteccionFraude
Detección de fraude de tarjetas de crédito, ontiene características V1 a V28 que son los componentes principales obtenidos por PCA. Vamos a descuidar la característica de tiempo que no sirve para construir los modelos. Las funciones restantes son la función 'Monto' que contiene la cantidad total de dinero que se está transaccionando y la función 'Clase' que contiene si la transacción es un caso de fraude o no.



De 284807 muestras, solo hay 492 casos de fraude, lo que representa solo el 0.17 por ciento del total de muestras. Por lo tanto, podemos decir que los datos con los que estamos tratando son datos muy desequilibrados y deben manejarse con cuidado al modelar y evaluar.

Comenzando con el árbol de decisiones, hemos utilizado el algoritmo 'DecisionTreeClassifier' para construir el modelo. Dentro del algoritmo, hemos mencionado que 'max_depth' es '4', lo que significa que estamos permitiendo que el árbol se divida cuatro veces y que el 'criterio' sea 'entropía', que es más similar a 'max_depth' pero determina cuándo deja de partir el árbol. Finalmente, hemos ajustado y almacenado los valores predichos en la variable 'tree_yhat'

A continuación, se encuentran los K-Vecinos más cercanos (KNN). Hemos construido el modelo usando el algoritmo 'KNeighborsClassifier' y mencionamos que 'n_neighbors' es '5'. El valor de 'n_neighbors' se selecciona al azar.

Para la regresión logística, ya que mantuvimos el modelo de una manera más simplista utilizando el algoritmo 'LogisticRegression'.

Construimos el modelo Support Vector Machine usando el algoritmo 'SVC' y no mencionamos nada dentro del algoritmo ya que logramos usar el kernel predeterminado, que es el kernel 'rbf'. Después de eso, almacenamos los valores predichos en el 'svm_yhat' después de ajustar el modelo.

El siguiente modelo es el modelo de bosque aleatorio que construimos usando el algoritmo 'RandomForestClassifier' y mencionamos que 'max_depth' es 4, tal como lo hicimos para construir el modelo de árbol de decisión. Finalmente, ajustando y almacenando los valores en 'rf_yhat'.


