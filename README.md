El objetivo de este ejercicio es realizar una heurística simple para conseguir una solución al Traveling Salesman Problem. 

Para hacer esto, habrá que trabajar sobre el archivo solver.py. El mismo ya tiene una función, llamada solve_it que lee el archivo input (tsp_70_1) y crea una lista, llamada points. Cada elemento de la lista points es un punto, definido por una coordenada X y una coordenada Y.  Si se observa el archivo tsp_70_1 se puede ver que la primera fila indica la cantidad de puntos que quedarán en points y el resto de las filas muestran las coordenadas X y Y de cada uno.

Supongamos que arrancamos en el punto 0 (es decir, el primer elemento de la lista points) y tenemos que recorrer todos los otros puntos una sola vez, pero volviendo al final al punto inicial. ¿Cómo sabemos en qué orden visitar estos puntos? Una solución bien simple es la propuesta en la línea 26 del código -> visitamos primero el punto 0, luego el 1, luego el 2, y así sucesivamente hasta llegar al punto 69 (luego del punto 69, volveríamos a 0). Sin embargo, esto podría ser una solución ineficiente ya que podríamos estar haciendo potencialmente muchas “idas y vueltas”.

Por lo tanto, la idea del código es intentar mejorar esta solución, llegando a un recorrido que genere una distancia menor al actual. De esta forma, el output debería ser una lista, llamada solution, que marque el orden del recorrido (importante, el primer punto de esa lista siempre debería ser el cero). 
En la solución ejemplo, solution es igual a [0, 1, 2, ….], indicando que se arranca por el punto 0, luego se va a 1, luego a 2, etc. Otra solución posible es [0, 10, 11, …]: es decir, luego de arrancar en 0 se visita al punto 10, luego al 11, y así.

IMPORTANTE: el objetivo de este ejercicio no es llegar a la MEJOR solución, sino a una solución que tenga sentido y mejore lo que exista. No se utilizan librerías de optimización para resolverlo, sino armar una solución que nazca de operaciones lógicas.

La solucion está orientada a una optimización combinatoria de N caminos posibles.
