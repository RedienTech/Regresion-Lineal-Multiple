## Regresion Lineal multiple

Este es un proyecto de ejecucion de un modelo de regresion lineal multiple, optimizando la funcion de costo a traves de dos metodos diferentes,
con el fin de explicar de forma concisa y practica el funcionamiento de estos modelos.

**Objetivos**
1. Desarrollar un modelo de regresion lineal utilizando como metodo de optimizacion a la ecuacion normal.
2. Desarrollar un modelo de regresion lineal utilizando como metodo de optimizacion al descenso del gradiente.
3. Evitar el uso de librerias que implementes estos algoritmos (No Scikit-Learn) Para abordar de una forma mas profunda su funcionamiento.

### Funcion normal

El metodo de optimizacion mediante la funcion normal proviene de una optimizacion a partir de la derivacion de la funcion de costo. Que en este caso sera el error medio cuadratico, una funcion de costo que se destaca por castigar los grandes errores.

![Error](https://latex.codecogs.com/svg.latex?%5Cfn_cm%20J%28%5Ctheta%29%20%3D%20%5Csum_%7Bi%3D1%7D%5E%7Bn%7D%28h%28x_%7Bi%7D%29%20-%20y_%7Bi%7D%29%5E2)

Esta funcion de costo dependera del vector de hiperparametros theta que representara a los coeficientes en la funcion hipotesis. La cual estara definida por la funcion:

![Hipotesis](https://latex.codecogs.com/svg.latex?%5Cfn_cm%20h%28x%29%3D%20X%5Ctheta%5E%7BT%7D)

Mediante la aplicacion del metodo de optimizacion basado en la primera derivada, se logra obtener mediante un proceso algebraico (Cuyo detalle no es el objetivo de este ejemplo) una expresion que determinara al vector de hiperparametros theta que minimize el valor de la funcion de costo, esta expresion estara representada en forma de operaciones vectoriales y en funcion de las matrices del conjunto de datos de entrenamiento X y Y.

![Ecuacion Normal](https://latex.codecogs.com/svg.latex?%5Ctheta%20%3D%20%28X%5E%7BT%7DX%29%5E%7B-1%7DX%5E%7BT%7DY)

Esta funcion expresada alrededor de los datos de entrenamiento, requiere que los datos sean previamente procesados realizando un pequeño ajuste a la matriz de entrada X. Una columna de unos, debe ser añadida al inicio de la Matriz X, esto con el objetivo de poder representar al termino independiente a partir de lamultiplicacion matricial. Quedando la matriz de datos X de la siguiente forma.

![Matriz X](https://latex.codecogs.com/svg.latex?X%20%3D%20%5Cbegin%7Bbmatrix%7D%201%20%26%20x_%7B11%7D%20%26%20x_%7B12%7D%20%26%20x_%7B13%7D%20%26%20...%20%26%20x_%7B1n%7D%5C%5C%201%20%26%20x_%7B21%7D%20%26%20x_%7B22%7D%20%26%20x_%7B23%7D%20%26%20...%20%26%20x_%7B2n%7D%20%5C%5C%201%20%26%20x_%7B31%7D%20%26%20x_%7B32%7D%20%26%20x_%7B33%7D%20%26%20...%20%26%20x_%7B3n%7D%5C%5C%20%3A%20%26%20%3A%20%26%20%3A%20%26%20%3A%20%26%20%3A%20%26%20%3A%5C%5C%201%20%26%20x_%7Bm1%7D%20%26%20x_%7Bm2%7D%20%26%20x_%7Bm3%7D%20%26%20...%20%26%20x_%7Bmn%7D%20%5Cend%7Bbmatrix%7D)

De esta forma los datos estaran preparados para mediante la utilizacion de la equacion normal, obtener los hiperparametros theta que minimizen la funcion de costo. Cabe resaltar que esta ecuacion normal, puede resultar mucho mas rapida que el descenso del gradiente (Del cual hablaremos mas tarde), sin embargo su principal limitacion se encuentra en el calculo de la inversa al principio de la ecuacion. Por lo cual al crecer esa matriz, la carga computacional se hace cada vez mas grande (En un factor de n al cubo), por lo cual en un ejemplo con muchos mas parametros, seria recomendable utilizar un metodo como el del descenso del gradiente (Un metodo iterativo).


