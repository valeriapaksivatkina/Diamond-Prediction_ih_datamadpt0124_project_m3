# Diamond-Prediction_ih_datamadpt0124_project_m3 

Este repositorio contiene el código y los datos para la participación en la Diamond Price Prediction Challenge. Inspirada en el fascinante mundo de los diamantes, su valoración y los factores que influyen en sus precios de mercado, esta competencia requiere desarrollar un modelo predictivo que estime con precisión el precio de los diamantes basado en diversas características. 

# Métrica de Evaluación
La métrica de evaluación elegida para esta competencia es el RMSE (Root Mean Squared Error). 

# Datos
En esta sección se proporcionan los datos necesarios para entrenar el modelo y una descripción detallada de las características.

# Archivos
diamonds_train.db - El conjunto de entrenamiento

diamonds_test.csv - El conjunto de prueba

sample_submission.csv - Un archivo de muestra de envío en el formato correcto

# Características

price: Precio en USD

carat: Peso del diamante

cut: Calidad del corte (Fair, Good, Very Good, Premium, Ideal)

color: Color del diamante, desde J (peor) hasta D (mejor)

clarity: Medida de claridad del diamante (I1 (peor), SI2, SI1, VS2, VS1, VVS2, VVS1, IF (mejor))

x: Longitud en mm

y: Anchura en mm

z: Profundidad en mm

depth: Porcentaje de profundidad total

table: Anchura de la parte superior del diamante en relación con el punto más ancho

city: Ciudad donde se reporta la venta del diamante

id: Solo para archivos de prueba y de envío de muestra, ID para la identificación de la muestra de predicción


# Modelo e Hiperparámetros

El modelo utilizado es XGBRegressor con Dmatrices para manejar valores categóricos. Los mejores hiperparámetros identificados son los siguientes:

colsample_bytree: 0.9
learning_rate: 0.1
max_depth: 6
n_estimators: 100
subsample: 0.9


El proceso de ajuste involucró validación cruzada de 3 pliegues para cada uno de los 243 candidatos, sumando un total de 729 ajustes. El RMSE resultante para el mejor modelo fue 508.325.
