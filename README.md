# Final_test
Cancer data set

El objetivo de este codigo es observar la eficiencia de 3 modelos dentro del data set Breast Cancer, en primer lugar se carga algunas librerias, entre ellas la libreria OS, misma que nos permite seleccionar un directorio para trabajar

Para la carga de los datos se utilizo de la plaaforma Kaggle, misma en donde tambien se encuentra el data set a trabajar, misma que se encuentra en el siguiente link: https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

Una vez que se ha descargado el data set se ha trasladado el mismo y se ha realizado el reemplazo de las , con el parametro ~, ademas de que los titulos poseian "" mismos que tambien fueron reemplazados, cabe mencionar que al final de la primera fila existia una , extra, misma que se elimino.

Con el data set cargado se renombra a las columnas concave points_mean por concave_points_mean, concave points_se por concave_points_se y concave points_worst por concave_points_worst

Se genera diagramas de caja, con la finalidad de observar la distribucion de los datos, y se ha dividido el data set para observar las caracteristicas de los datos promedio, los datos se y los datos de casos con cancer de mama violentos.

Con respecto a la columna diagnostico se observa que existe un total de 569 datos de los cuales 357 son benignos y 212 malignos, luego de esto se ha calculado los valores Nan del data set indicando que no hay ningun valor nan dentro del data set

Luego se genera un describe con la finalidad de observar la distribucion de las variales

Se reemplaza el el M y B con Benigno y Maligno y se crea el data set X y y, en donde el Data set X contiene todas las variables numericas y el data set y que es una sola variable consta de datos de 0 y 1 indicando la presencia de cancer de mama o no.

Se elabora un scatter plot del data set con la finalidad de observar la distribucion de los datos, mismos que no poseen mucha dispersión por lo que viendo estas distribuciones se ha tomado la decision de tomar en consideracion modelos de aprendizaje supervisado, mismos que seran detallados a continuación

En primer lugar y tomando en consideración la bateria de modelos de aprendizaje supervisado que existen se tomo en consideracion una regresion logistica, misma que genero en una primera instancia un accuracy de 0.65 por ciento, valor que no se puede considerar como modelo final, tomando en consideracion la implicacion de la explicacion que se tiene por detras, toda vez que una cantidad fuerte de falsos positivos puede ser perjudicial para una persona que posee cancer pero no es diagnosticada y empieza su tratamiento.

Para mejorar este modelo y no descartarlo, ademas de que tomando en consideracion que la regresion logistica utiliza el calculo de los valores normalizados se utilizo de la normalizacion de las variables utilizando un escalado estandar, mismo que en aplicacion con el modelo antes mencionado genero como resultado un valor de 0.9736842105263158, que segun la matriz de confusion indica que dentro de los datos predecidos puede existir la posibilidad de que dos personas que tienen cancer pero son diagnosticadas como no portadoras de la enfermedad.

Posteriormente se evaluo como segunda opcion el modelo xgboost con una prediccion de de 3 falsos positivos y un acurracy de 0.956140350877193, el tercer modelo es random forest mismo que genero un resultado de 0.9473684210526315 como accuracy y un total de 4 falsos positivos.

Como modelo final se tomo en consideración la utilizacion de mecanismos de undersampling y oversampling, esto se realiza con la finalidad de obtener un data set mucho mas equilibrado que contenga una cantidad de datos importante para obtener una mejor lectura y prediccion del modelo, utilizando la tecnica del undersampling y smote tomek, situacion que en combinacion con el primer modelo genero un accuracy de 0.9824561403508771 con una matriz de confusion con un falso positivo, situacion que presenta una mejora del indicador, ademas de la prediccion del modelo.
