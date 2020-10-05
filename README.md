# Kaggle Competition
![image](https://user-images.githubusercontent.com/69120593/95111267-8889d300-073f-11eb-8bba-a2c6a253c457.png)

## Propósito
Nuestro proyecto de esta semana consistía en obtener predicciones utilizando distintos algorítmos de Machine Learning.
A partir de una lista de diamantes, en las que se recogían una serie de características y sus precios, debíamos predecir el precio que obtendría otra larga lista de diamantes. Utilizando las métricas adecuadas, debíamos descubrir cual era el algoritmo más apropiado para el estudio, y explotarlo lo máximo posible.

## Material
Para este proyecto, se nos otorgaron documentos en formato csv, con los que proceder al trabajo. El primero, llamado train.csv, contenia el X_train y el y_train del estudio o lo que es lo mismo, numerizando ciertas columnas, y dejando de lado la columna "price", el dataset del documento representaba el conjunto de datos que el algorítmo debía tomar como referencia para después indicar a dicho algorítmo que los resultados de esos datos, serían los datos de la columna "price", nuestro y_train para el proyecto.  
El segundo csv, llamado predict.csv, contenia el conjunto de datos sobre los cuales debiamos hacer una prediccion. Era un dataset muy similar al de train.csv, pero con datos distintos y sin la columna "price". Este dataset lo interpretábamos como el X_test, faltándonos únicamente el y_test.

## Procedimiento
En primer lugar, importe ambos csv nombrandolos "train" y "predict" respectivamente. 
Posteriormente, procedí a preparar ambos datasets para el entrenamiento, convirtiendo las columnas alfabéticas a columnas numéricas, combinando dos herramientas: LabelEncoder() y fit_transform(). Del primer dataset, como ya he explicado antes, obtube el X_train(todas las columnas numéricas menos "price") y el y_train(columna "price"). Del segundo dataset, obtuve X_test(todas las columnas ya que price no aparece).
El siguiente paso, una vez preparados los datasets, es entrenar el model. Para ello, hay que importarlo, denominarlo de alguna manera (generalmente y en nuestro caso, la denomincacion es "model"), y posterirmente se entrena aplicando un "model.fit(X_train,y_train)". Con esto, lo que hemos conseguido es que el algoritmo entiendo cuales son los datos y sus consiguientes resultados. Una vez el algortimo ya sabe como interpretar los datos, este es aplicado a nuestro X_test de la siguiente manera: y_pred = model.predict(X_test). Asi obtenermos los resultados que pretendiamos en este proyecto.

## Exportación del DataFrame
Convertimos el y_pred en un DataFrame de Pandas, y mediante el codigo <DataFrame>.to_csv("<nombre>.csv"), exportamos este DataFrame al disco.
  
## Métricas
Después, y con el fin de conocer lo bien que funcionaba el algortimo aplicado a este estudio, he utilizado una serie de metricas que nos indican diversas informaciones:
 
### 

