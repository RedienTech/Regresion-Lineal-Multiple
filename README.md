## Regresion Lineal multiple

Este es un proyecto de ejecucion de un modelo de regresion lineal multiple, optimizando la funcion de costo a traves de dos metodos diferentes,
con el fin de explicar de forma concisa y practica el funcionamiento de estos modelos.

**Objetivos**
1. Desarrollar un modelo de regresion lineal utilizando como metodo de optimizacion a la ecuacion normal.
2. Desarrollar un modelo de regresion lineal utilizando como metodo de optimizacion al descenso del gradiente.
3. Evitar el uso de librerias que implementes estos algoritmos (No Scikit-Learn) Para abordar de una forma mas profunda su funcionamiento.

### Funcion normal

El metodo de optimizacion mediante la funcion normal proviene de una optimizacion a partir de la derivacion de la funcion de costo. Que en este caso sera el error medio cuadratico, una funcion de costo que se destaca por castigar los grandes errores.
  
                         <img src="https://latex.codecogs.com/svg.latex?J(\theta&space;)&space;=&space;\sum_{i=1}^{m}&space;(h(x_{i})&space;-&space;y_{i})^2" title="J(\theta ) = \sum_{i=1}^{m} (h(x_{i}) - y_{i})^2" />
