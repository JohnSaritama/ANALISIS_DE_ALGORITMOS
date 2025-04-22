
# TRABAJO DE INVESTIGACION

## Nombre:John Paul Saritama

## Fecha:22/04/2025


## Algoritmia Elemental e Introducción a la Análisis de Algoritmos

## 1. Capítulo 2: Insertion Sort (Cormen et al., 2022)
## 1.1 ¿Qué es Insertion Sort?
Insertion Sort (ordenamiento por inserción) es un algoritmo de ordenación sencillo pero efectivo en ciertos contextos. Su funcionamiento simula la forma en que ordenamos cartas en la mano: se toma un elemento del conjunto no ordenado y se inserta en la posición adecuada dentro del subconjunto ordenado.

## 1.2 Funcionamiento del Algoritmo
Supongamos un arreglo A[1...n]. Insertion Sort comienza con el segundo elemento (índice 2), lo compara con los elementos anteriores y lo "inserta" en la posición correcta.

Pseudocódigo (simplificado):
```java


para j = 2 hasta n
    clave = A[j]
    i = j - 1
    mientras i > 0 y A[i] > clave
        A[i + 1] = A[i]
        i = i - 1
    A[i + 1] = clave
``` 
## 1.3 Análisis del Rendimiento
Peor caso (orden inverso): O(n²)

Mejor caso (ya ordenado): O(n)

Caso promedio: O(n²)

A pesar de no ser el más eficiente para grandes volúmenes de datos, Insertion Sort tiene ventajas como:

Eficiencia para arreglos pequeños.

Estabilidad (no cambia el orden relativo de elementos iguales).

Simplicidad de implementación.

## 2. Capítulo 2: Analyzing Algorithms (Cormen et al., 2022)
## 2.1 Importancia del Análisis de Algoritmos
El análisis de algoritmos permite anticipar el comportamiento de un programa en cuanto a tiempo y uso de recursos. Se evalúan dos principales factores:

Tiempo de ejecución.

Uso de memoria.

##  2.2 Notación Asintótica
Las notaciones asintóticas permiten describir el crecimiento de la complejidad de un algoritmo:

O (mayor o igual): Límite superior (peor caso).

Ω (mayor o igual): Límite inferior (mejor caso).

Θ (igual): Límite ajustado (caso promedio o comportamiento general).

##  2.3 Modelos de análisis
Cormen utiliza el modelo de máquina de acceso aleatorio (RAM), donde cada operación básica (suma, resta, comparación, etc.) se considera de tiempo constante.

## 3. Capítulo 2: Algoritmia Elemental (Brassard y Bratley)
## 3.1 ¿Qué es la Algoritmia Elemental?
Es el conjunto de técnicas básicas utilizadas para resolver problemas computacionales simples. Estas técnicas incluyen:

Iteración (bucles).

Recursión.

Búsqueda y ordenamiento básicos.

Comparación y conteo.

Brassard y Bratley explican cómo estas técnicas pueden aplicarse a problemas más complejos cuando se combinan adecuadamente.

## 3.2 Ejemplos de algoritmos elementales
Búsqueda lineal: Recorre uno a uno los elementos hasta encontrar el objetivo.

Búsqueda binaria: Divide el arreglo ordenado en mitades sucesivas. Complejidad: O(log n).

Ordenamientos clásicos: Bubble Sort, Selection Sort, Insertion Sort.

## 3.3 Estudio de la Eficiencia
Se introduce el concepto de eficiencia mediante el conteo de operaciones y la estimación de complejidad temporal. Brassard introduce la importancia de elegir estructuras de datos adecuadas y usar estrategias de resolución eficaces como dividir y conquistar.


## 4. Conclusión
Los temas abordados son pilares fundamentales para cualquier estudiante de ciencias computacionales. Comprender cómo funcionan algoritmos básicos como el Insertion Sort y cómo analizarlos permite tomar decisiones informadas al diseñar software. Además, conocer el análisis asintótico y la eficiencia ayuda a escalar soluciones a problemas reales.

El dominio de estas técnicas es esencial para avanzar hacia algoritmos más complejos como los de búsqueda avanzada, grafos, programación dinámica o estructuras de datos eficientes.

