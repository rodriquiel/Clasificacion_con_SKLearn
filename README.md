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


