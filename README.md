## Regresion Lineal multiple

Este es un proyecto de ejecucion de un modelo de regresion lineal multiple, optimizando la funcion de costo a traves de dos metodos diferentes,
con el fin de explicar de forma concisa y practica el funcionamiento de estos modelos.

**Objetivos**
1. Desarrollar un modelo de regresion lineal utilizando como metodo de optimizacion a la ecuacion normal.
2. Desarrollar un modelo de regresion lineal utilizando como metodo de optimizacion al descenso del gradiente.
3. Evitar el uso de librerias que implementes estos algoritmos (No Scikit-Learn) Para abordar de una forma mas profunda su funcionamiento.

### Funcion normal

El metodo de optimizacion mediante la funcion normal proviene de una optimizacion a partir de la derivacion de la funcion de costo. Que en este caso sera el error medio cuadratico, una funcion de costo que se destaca por castigar los grandes errores.
  
![error](<img src="http://www.sciweavers.org/tex2img.php?eq=J%28%5Ctheta%20%29%3D%5Csum_%7Bi%3D1%7D%5E%7Bm%7D%28h%28x_%7Bi%7D%29-y_%7Bi%7D%29%5E2&bc=White&fc=Black&im=png&fs=18&ff=arev&edit=0" align="center" border="0" alt="J(\theta )=\sum_{i=1}^{m}(h(x_{i})-y_{i})^2" width="265" height="75" />)
