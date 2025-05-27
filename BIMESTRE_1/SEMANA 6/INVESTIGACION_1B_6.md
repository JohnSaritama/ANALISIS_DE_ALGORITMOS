Tema 4.2 – Análisis de las Estructuras de Control

(Brassard y Bratley, 2000)

1. Introducción

El análisis de algoritmos no solo se basa en comprender las funciones matemáticas que representan su comportamiento, sino también en estudiar las estructuras de control que los componen. Las estructuras de control determinan el flujo de ejecución de un algoritmo, y su impacto en la eficiencia es significativo.

Brassard y Bratley, en las páginas 111 a 117, explican cómo analizar de forma detallada los efectos de las instrucciones básicas, las estructuras condicionales y los bucles, especialmente desde el punto de vista del tiempo de ejecución.


---

2. Instrucciones Básicas

Las instrucciones básicas son aquellas operaciones que se consideran de tiempo constante (tiempo de ejecución no depende del tamaño de la entrada n).

Ejemplos típicos incluyen:

Asignaciones: x = a + b;

Comparaciones: if (a > b)

Lectura o escritura de un valor

Aritmética básica: suma, resta, multiplicación, división


Coste: Se dice que cada una tiene un costo constante, denotado como O(1).


---

3. Estructuras de Control Condicionales

3.1. Condicional if-else

La estructura if introduce bifurcaciones en el flujo de control. El análisis debe considerar ambos caminos (el mejor caso, el peor caso y el caso promedio).

Ejemplo:

if (x > y) {
    // bloque A
} else {
    // bloque B
}

Para el análisis, se calcula el tiempo de ejecución de cada bloque y se expresa el total como:

Mejor caso: el camino más corto (el más rápido)

Peor caso: el camino más largo (el más costoso)

Caso promedio: si se conoce la probabilidad de cada camino



---

4. Bucles o Ciclos

Los bucles son estructuras clave para la repetición de tareas. Su análisis se enfoca en contar cuántas veces se ejecuta el cuerpo del bucle, y multiplicarlo por el costo del cuerpo.

4.1. Bucle for

Es el más fácil de analizar cuando el número de iteraciones es explícito.

Ejemplo:

for (i = 0; i < n; i++) {
    // cuerpo del bucle (coste C)
}

Análisis:

El bucle se ejecuta n veces.

Tiempo total = 

Orden de crecimiento: O(n)


4.2. Bucles anidados

Si hay bucles dentro de otros, el tiempo total es el producto de las iteraciones.

Ejemplo:

for (i = 0; i < n; i++) {
    for (j = 0; j < n; j++) {
        // cuerpo del bucle (coste C)
    }
}

Análisis:

Total de iteraciones: 

Orden de crecimiento: O(n²)


4.3. Bucle while

Este bucle depende de una condición que puede ser más difícil de predecir. Se requiere entender cómo cambia la condición en cada iteración.

Ejemplo:

while (n > 1) {
    n = n / 2;
}

Análisis:

El valor de n se reduce a la mitad en cada iteración.

Número de iteraciones: 

Orden de crecimiento: O(log n)



---

5. Análisis Compuesto de Control

Muchos algoritmos combinan estructuras. El análisis consiste en sumar o multiplicar los costos de los componentes según cómo se ejecuten.

Reglas generales:

Estructuras secuenciales: se suman sus tiempos.

Estructuras anidadas: se multiplican sus tiempos.


Ejemplo combinado:

if (condición) {
    for (i = 0; i < n; i++) {
        // O(1)
    }
}

Si la condición es verdadera:

Coste del for: O(n)
Si no se cumple: O(1) (solo la comparación).



---



7. Conclusión

El análisis de estructuras de control es vital para entender la eficiencia de un algoritmo. Las estructuras básicas como condicionales y bucles tienen un impacto directo en el tiempo de ejecución. Brassard y Bratley muestran que un buen análisis debe incluir tanto la estructura como el comportamiento dinámico del código.

Este tipo de análisis es el primer paso hacia la optimización y el diseño de algoritmos eficientes, lo que es esencial en ciencias de la computación y programación.
