# Clasificacion con SciKit Learn

## Proyecto creado por Ezequiel Rodriguez en base a curso de Alura "Machine Learning: clasificacion con SKLearn"

### Proyecto destinado a trabajar mediante el uso de distintas bases de datos sobre diferentes topicos, a traves del lenguaje Python. El principal objetivo es mostrar el funcionamiento de algoritmos de clasificacion en base a distintos procesos como el uso muestras, el entrenamiento de modelos, la prueba de los mismos, la medicion de la tasa de acierto y la optimizacion del proceso mediante el uso de Support Vector Machines, árboles de decisión y dummy classifiers.

### Conocimientos aplicados:
* Trabajar con dataframes
* Limpiar y tratar datos faltantes
* Crear diferentes agrupamientos para aplicar estadistica descriptiva
* Analisis sobre graficos generados mediante librearias
* Modelado de sistemas lineales y no lineales para comparar resultados
* Utilizacion de dummy classifiers y arboles de decision e interpretacion de los mismos

### Uso de Python Pandas, Numpy, Matplotlib, Seaborn, SciKit Learn, Graphviz y Jupyter

## Resultados obtenidos

### Comparacion entre modelado con sistemas lineales y no lineales

### Se toma una base de datos a partir de datos recopilados a partir de proyectos de web desing, donde se tiene la condicion de no-finalizacion (1: no finalizado, 0: finalizado), las horas esperadas de trabajo y el precio cobrado. Luego de cambiar la logica de la columna 'no_finalizado' para que sea mas intuitiva (1: finalizado, 0: no finalizado), se desarrolla e implementa un modelo para determinar si el proyecto será finalizado o no en base a comparar el precio a pagar por el desarrollo con las horas esperadas de trabajo.

### En el siguente grafico, se puede observar que a medida que la cantidad de horas de trabajo esperadas aumentan, si el precio aumenta tambien los proyectos son finalizados, mientras que si el precio se mantiene en un valor bajo, los proyectos no son finalizados.

![0](https://user-images.githubusercontent.com/111917955/230812889-1c53a6ea-19b1-4a26-9f8c-5516161727f5.png)

### En primera instacia, se aplica un modelo lineal, y se establece una Baseline para saber si el modelo es bueno. En el siguente grafico, la recta verde representa el limite de la decision (decision boundary), y para este caso su interpretacion es que todo los puntos que se encuentran sobre ella seran tomados como finalizados y todos los que estan por debajo seran tomados como no finalizados. Observando donde se encuentran los puntos correspondientes a no finalizado y finalizado se puede concluir que el limite es pesimo para el caso.

![1](https://user-images.githubusercontent.com/111917955/230813980-7ce99611-5ad5-4af3-9fea-ad40c6d8db38.png)

### En segunda instancia, se aplica un modelo no lineal a partir de una Support Vector Machine (SVC), donde primero se procede a estandarizar los datos para que tengan la misma cantidad de ceros con la finalidad de que el SVC pueda estimar y graficar de buena manera (se toma la media y se divide por el desvío típico en ambas variables). Se puede observar en este caso que utilizando un estimador no lineal para el calculo del limite de la decision (recta verde) se llegó a un mejor resultado que en el caso anterior, quedando los puntos en su mayoria con su respectivo color de decision tomada por el modelo desarrollado para saber que proyectos seran finalizados y cuales no.

![2](https://user-images.githubusercontent.com/111917955/230813494-e3b4b842-0c48-4d85-b26a-dce23d7470bf.png)

### Dummy classifiers y Arboles de decision

### Para este caso, se utiliza una base de datos sobre datos de automoviles como su millaje por año, el año del modelo, el precio y si fue vendido. Se busca crear un modelo para estimar si un automovil con ciertos atributos será vendido o no. Antes de realizar el modelaje, se realiza un tratamiento sobre los datos para poder trabajar de mejor manera con los mismos.

### Al ver los resultados de las baselines en base a los calsificadores Dummy utilizados se puede concluir que dependiendo del tipo de estrategia al momento de instanciar nuestro DummyClassifier, se tiene una baseline mejor o peor. Cuando se selecciona una baseline la idea es quedarse con una baseline que tenga sentido, entonces 'most_frequent', que tiene un valor más alto seria la adecuada, y este es el valor del clasificador (58%) se debe superar de buena manera. En este caso, se superó en aproximadamente 18%. Entonces se puede concluir que hubo una superación bastante grande y que el modelo es bueno. La contra con la que cuenta este tipo de clasificador es que no tiene ningun grafico para detallar de manera visual lo calculado.

### Se aplica entonces otro clasificador denominado 'Arbol de decision', el cual se aplica por medio de un modelo con datos escalados. Luego de entrenar al modelo con 7500 elementos y se utilizar de prueba 2500 elementos, la tasa de acierto fue de: 78.04 %. Por ultimo, por medio de la libreria 'graphviz' se puede ver la vista del arbol en forma de grafo.

### Arbol de decision con datos escalados

![arbol de decision1](https://user-images.githubusercontent.com/111917955/231894968-c3c2f5c6-1b33-4f06-83f9-ad4f026d0bc1.png)

### Por ultimo, se realiza el modelo pero con datos sin escalar o estandarizar, obteniendo el siguiente grafico

![arbol2](https://user-images.githubusercontent.com/111917955/231895143-d4dc4a36-90e8-461a-a022-82045e3655ab.png)

### Class = Si significa que se vende y Class = No significa que no se vende, y a mayor oscuridad del color, mayor probabilidad de que lo resultado en Class suceda. Se puede ver que para este modelo, la 'edad' del auto no cobra relevancia a la hora de devolver un resultado en base a una consulta




