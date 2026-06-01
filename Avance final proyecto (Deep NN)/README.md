# Avance final (Deep NN)
Para este avance final se toma EfficientNetB0 como arquitectura base y se le añaden las siguientes capas: 

1. GlobalAveragePooling2D
2. Capa Dense (450 neuronas, activacion ReLU)
3. Capa Dropout (drop rate: 0.08789841674809465)
4. Capa Dense (50 neuronas, activacion ReLU)
5. Capa Dense de salida (4 neuronas, activacion Softmax)

En este avance se realiza el entrenamiento de la red neuronal en dos fases:

# Fase 1
En esta fase se realiza el entrenamiento unicamente de las capas que se añadieron a la arquitectura base de EfficienNetB0. Para esta fase se una tasa de aprendizaje de 0.0035896062216663705

# Fase 2
En esta fase se incluye dentro del entrenamiento a las ultimas dos capas de la arquitecura base de EfficienNetB0. Para esta fase se una tasa de aprendizaje de 3.385418278847751e-05

# Uso de Optuna
Varios de los hiperparametros del modelo fueron obtenidos haciendo uso de Optuna con el fin de encontrar los valores optimos que maximicen el rendimiento del modelo. Especificamente, se buscaron valores optimos de los siguientes hiper parametros:
1. Tasas de aprendizaje de ambas fases
2. Numero de neuronas de las capas Dense
3. Drop rate de la capa Dropout
4. NUmero de capas de tipo Dense y Dropout que se le agregaran al modelo
5. NUmero de capas de la arquitectura original que reentranaran en la fase 2

# Ejecucion del notebook
Se recomienda ejecutar este notebook usando jupyter notebook de forma local. Antes de ejecutar el notebook se debe usar el siguiente comando para instalar las librerias necesarias:

```code
pip install -r requirements.txt
```

Ademas, tambien sera necesario instalar jupyter notebook usando el siguiente comando:

```code
pip install jupyter lab
```

Una vez instalado, se usa el siguiente comando para abrir jupyter notebook (es necesario estar ubicado en la carpeta donde se encuentra el notebook): 

```code
jupyter lab
```

Eso abrira jupyter notebook y se podra ejecutar el notebook creado.