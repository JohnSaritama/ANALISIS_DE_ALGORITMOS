# Investigación: Tema 3 – Notación Asintótica (Brassard & Bratley, 2006)
## 1. Introducción
La notación asintótica es una herramienta fundamental en el análisis de algoritmos. Permite describir cómo crece el tiempo de ejecución (o el uso de memoria) de un algoritmo a medida que el tamaño de entrada crece, sin necesidad de detallar aspectos de implementación o hardware. Este concepto es esencial para comparar algoritmos de forma independiente a la plataforma en que se ejecuten.

Brassard y Bratley (2006) dedican el capítulo 3 de su obra a explicar con profundidad la notación asintótica, las clases de funciones más comunes, y cómo utilizarlas para analizar la eficiencia de los algoritmos.

## 2. Fundamentos de la Notación Asintótica
2.1. Objetivo
El objetivo principal de la notación asintótica es expresar el comportamiento de un algoritmo en el límite, es decir, cómo se comporta cuando el tamaño de entrada crece indefinidamente. Esto ayuda a abstraer los detalles específicos y concentrarse en el "orden de magnitud" de la eficiencia.

2.2. Tamaño de Entrada
Se asume que el tamaño de entrada se representa mediante una variable, usualmente denotada como n. El análisis se centra en cómo una función de tiempo o espacio T(n) crece respecto a n.

## 3. Tipos de Notaciones Asintóticas
3.1. Notación O Grande (Big-O): 𝑂(𝑓(𝑛))O(f(n))

La notación O grande proporciona un límite superior para el crecimiento de un algoritmo. Es decir, asegura que, más allá de cierto punto, el algoritmo no será más lento que una función dada (hasta una constante multiplicativa).
Definición formal:

Sea 𝑇(𝑛)T(n) una función de tiempo de ejecución. Se dice que:
𝑇(𝑛)∈𝑂(𝑓(𝑛)) si existen constantes 𝑐>0y 𝑛 0 tales que 𝑇(𝑛)≤𝑐⋅𝑓(𝑛)   para todo 𝑛≥𝑛0.T(n)∈O(f(n)) si existen constantes c>0 y n 0 tales que T(n)≤c⋅f(n) para todo n≥n 

3.2. Notación Omega (Ω): 

Esta notación da un límite inferior al crecimiento de un algoritmo. Garantiza que el algoritmo no será más rápido que una función dada (hasta constante multiplicativa).

Definición formal:

T(n) \in \Omega(f(n)) \text{ si existen constantes } c > 0 \text{ y } n_0 \text{ tales que } T(n) \geq c \cdot f(n) \text{ para todo } n \geq n_0.

3.3. Notación Theta (Θ): 

La notación Θ indica un ajuste exacto del orden de crecimiento, es decir, tanto límite superior como inferior. El algoritmo crece "a la misma velocidad" que  hasta constantes.

Definición formal:

T(n) \in \Theta(f(n)) \text{ si existen constantes } c_1, c_2 > 0 \text{ y } n_0 \text{ tales que } c_1 \cdot f(n) \leq T(n) \leq c_2 \cdot f(n) \text{ para todo } n \geq n_0.


---

4. Comparación de Funciones de Crecimiento

Brassard y Bratley analizan el crecimiento de diferentes funciones, desde las más lentas hasta las más rápidas. Algunas funciones comunes en la práctica:

Orden de crecimiento	Ejemplo de algoritmo

	Búsqueda binaria
	Búsqueda lineal
	Mergesort, Heapsort
	Bubble sort, selección, inserción
, 	Fuerza bruta en problemas NP



---

5. Importancia en el Análisis de Algoritmos

El uso de la notación asintótica permite:

Predecir el rendimiento de un algoritmo sin necesidad de implementarlo.

Comparar soluciones alternativas y elegir la más eficiente.

Identificar cuellos de botella y áreas críticas de mejora.


Además, ayuda a desarrollar algoritmos escalables, especialmente importantes en problemas que manejan grandes volúmenes de datos.



6. Conclusión

La notación asintótica es una piedra angular en el estudio de algoritmos. Su dominio permite diseñar programas más eficientes y sostenibles. Brassard y Bratley ofrecen una explicación clara y rigurosa de estos conceptos, con ejemplos y fundamentos matemáticos, convirtiendo el capítulo 3 en una lectura esencial para cualquier estudiante de ciencias de la computación