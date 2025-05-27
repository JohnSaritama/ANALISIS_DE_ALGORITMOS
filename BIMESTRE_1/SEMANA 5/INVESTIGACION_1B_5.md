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

