#1. Introducción

La notación asintótica es una herramienta matemática fundamental para el análisis de algoritmos. Permite describir el comportamiento del tiempo de ejecución o uso de memoria de un algoritmo a medida que el tamaño de la entrada crece, sin enfocarse en detalles de implementación o constantes menores.

# 2. Objetivo

El propósito de la notación asintótica es proporcionar una manera estandarizada de comparar algoritmos con base en su eficiencia computacional, especialmente para entradas grandes.


---

# 3. Notaciones Principales

a. Notación O (O-grande)

Definición: Representa una cota superior del crecimiento de una función.

Ejemplo: Si un algoritmo tiene una complejidad de tiempo de T(n) = 3n^2 + 5n + 2, entonces T(n) ∈ O(n^2).

Interpretación: En el peor de los casos, el tiempo de ejecución no crecerá más rápido que n^2 para entradas grandes.


b. Notación Ω (Omega)

Definición: Representa una cota inferior del crecimiento de una función.

Ejemplo: T(n) ∈ Ω(n) significa que el algoritmo requiere al menos tiempo lineal en el mejor caso.


c. Notación Θ (Theta)

Definición: Representa una cota ajustada o exacta del crecimiento.

Ejemplo: T(n) ∈ Θ(n log n) implica que el algoritmo crece exactamente a esa tasa, tanto en el mejor como en el peor caso (dentro de constantes).



---

# 4. Comparación de Algoritmos

Brassard y Bratley enfatizan que el análisis asintótico permite comparar algoritmos independientemente del hardware o lenguaje de programación. Por ejemplo:

Búsqueda lineal: Θ(n)

Búsqueda binaria: Θ(log n)

Ordenamiento por burbuja: Θ(n^2)

Mergesort: Θ(n log n)



---

# 5. Importancia Práctica

Facilita la selección de algoritmos adecuados según las restricciones del problema.

Aporta una visión clara sobre la escalabilidad.

Se enfoca en el crecimiento a largo plazo, ignorando factores menos relevantes como constantes pequeñas o coeficientes.



---

# 6. Conclusión

El análisis asintótico es esencial para el diseño eficiente de algoritmos. La comprensión profunda de las notaciones O, Ω y Θ permite a los programadores tomar decisiones informadas y optimizar el rendimiento de sus programas.

