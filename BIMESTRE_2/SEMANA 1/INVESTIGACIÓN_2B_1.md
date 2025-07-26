# 1 Consulta

## Fuente: Cormen et al., 2022 – Capítulo 1

### Objetivos:

Comprender qué son los algoritmos y cómo se aplican en la informática.

Analizar su rol como herramienta esencial en la solución de problemas computacionales.

Estudiar la importancia de su eficiencia y cómo se comparan mediante técnicas de análisis.



## ¿Qué es un algoritmo?

Un algoritmo es un conjunto de pasos bien definidos, ordenados y finitos que permiten resolver un problema específico. Puede ser algo tan simple como un algoritmo para sumar dos números, o tan complejo como los algoritmos que usan los motores de búsqueda como Google.

Un algoritmo debe cumplir con ciertas características:

Entrada: uno o más datos iniciales.

Proceso: operaciones o instrucciones a realizar.

Salida: uno o más resultados.

Finitud: debe terminar después de un número determinado de pasos.

Claridad: las instrucciones deben ser comprensibles.

## Algoritmos en la práctica

En la informática moderna, los algoritmos son el motor interno de muchas aplicaciones. Por ejemplo:

Un algoritmo de búsqueda permite encontrar una palabra dentro de un archivo.

Un algoritmo de cifrado protege tus datos bancarios en línea.

Algoritmos de aprendizaje automático permiten que los sistemas “aprendan” a reconocer imágenes, patrones, etc.

## Algoritmos vs programas

Aunque un programa y un algoritmo están relacionados, no son lo mismo. Un programa es una implementación de uno o varios algoritmos en un lenguaje específico, mientras que un algoritmo puede existir sin estar ligado a un lenguaje de programación.

## Eficiencia y análisis de algoritmos

Uno de los principales enfoques del análisis de algoritmos es medir su eficiencia, lo cual se hace principalmente de dos formas:

Tiempo de ejecución (complejidad temporal): cuánto tiempo le toma al algoritmo procesar una entrada de cierto tamaño.

Uso de memoria (complejidad espacial): cuánta memoria necesita para ejecutarse.

Para esto se utiliza la notación Big-O, que permite describir el comportamiento del algoritmo a medida que el tamaño del problema crece. Algunos ejemplos:

𝑂(1)O(1): tiempo constante, ideal.

𝑂(𝑛)O(n): tiempo lineal, proporcional al tamaño de la entrada.

𝑂(𝑛log𝑛) O (nlogn): algoritmo más rápido que el cuadrático, pero más lento que el lineal.

𝑂(𝑛2)O(n 2): tiempo cuadrático, común en algoritmos de comparación simple.

## Importancia práctica

A veces, mejorar el algoritmo tiene más impacto que mejorar el hardware. Por ejemplo, un algoritmo más eficiente puede reducir horas de procesamiento a minutos, incluso si se ejecuta en una máquina más modesta.

## Conclusiones

Los algoritmos son esenciales para la resolución de problemas en informática.

Son una tecnología por sí mismos, capaces de transformar datos y procesos.

El análisis de su eficiencia permite elegir las mejores soluciones posibles, optimizando recursos como el tiempo y la memoria.

Comprender algoritmos es fundamental para cualquier científico o ingeniero en computación.




# CONSULTA 2: 

Capítulo 1 – Preliminares

Fuente: Brassard & Bratley, 2006


## Objetivos

Brindar una base teórica sólida para el estudio formal de algoritmos.

Presentar conceptos matemáticos y computacionales clave.

Introducir técnicas y estrategias comunes para diseñar algoritmos eficientes.






## Fundamentos teóricos

Antes de estudiar algoritmos complejos, es necesario conocer ciertos fundamentos:

Modelos computacionales como la máquina RAM, que simplifican el análisis al representar la computadora como una secuencia de instrucciones.

Conceptos básicos de matemática discreta, como funciones, sumatorias, recursión y lógica, que son herramientas esenciales para analizar algoritmos.


## Tipos de problemas algorítmicos

Los algoritmos se diseñan para resolver diferentes tipos de problemas:

Problemas de decisión: la salida es "sí" o "no". Ej.: ¿Existe un camino entre dos nodos?

Problemas de optimización: se busca la mejor solución entre muchas. Ej.: encontrar el camino más corto.

Problemas de búsqueda: encontrar un elemento dentro de una estructura. Ej.: buscar un número en una lista.


Notación y complejidad

La notación Big-O y otras variantes como Omega () y Theta () permiten describir el comportamiento de un algoritmo:

: cota superior (peor caso).

: cota inferior (mejor caso).

: comportamiento exacto (caso promedio o general).


También se introducen recurrencias para analizar algoritmos recursivos. Por ejemplo, si un algoritmo se llama a sí mismo dividiendo el problema a la mitad, su tiempo puede expresarse como:

T(n) = 2T(n/2) + n

Técnicas para diseñar algoritmos

1. Divide y vencerás: dividir el problema en partes más pequeñas, resolverlas por separado y unir las soluciones. Ej.: Mergesort.


2. Programación dinámica: guardar resultados intermedios para no repetir cálculos. Ej.: cálculo de Fibonacci.


3. Algoritmos voraces (greedy): tomar la mejor decisión local en cada paso. Ej.: algoritmo de Kruskal para árboles de expansión mínima.


4. Backtracking: explorar todas las posibilidades hasta encontrar una solución, retrocediendo cuando se detecta un error. Ej.: resolver el Sudoku.



Estas estrategias se eligen dependiendo de la naturaleza del problema y el tipo de solución deseada.


---

Conclusiones

Comprender los fundamentos matemáticos y teóricos permite desarrollar algoritmos sólidos y eficientes.

El análisis de la complejidad es clave para determinar si un algoritmo es útil en la práctica.

Las técnicas como divide y vencerás o programación dinámica ofrecen formas potentes y comprobadas de construir algoritmos efectivos.

Este capítulo es esencial para tener una base firme antes de adentrarse en el diseño y análisis de algoritmos complejos.


