
# TRABAJO DE INVESTIGACION

## Nombre:John Paul Saritama

## Fecha:29/04/2025


# 1.Caracterización del Tiempo de Ejecución y Notación Asintótica
## 1. Introducción
Uno de los aspectos fundamentales en el estudio de algoritmos es comprender cómo se comportan en términos de eficiencia. Esto incluye evaluar su rendimiento en el peor, mejor y caso promedio. Para formalizar este análisis, se utiliza la notación asintótica, la cual nos permite expresar cómo crece el tiempo de ejecución o el uso de memoria en función del tamaño de la entrada.

Los autores Cormen et al. (2022) en el capítulo 3 de Introduction to Algorithms y Brassard y Bratley (2006) en su capítulo sobre notación asintótica abordan este tema clave desde perspectivas complementarias.

## 2. Tema: Characterizing Running Times (Cormen et al., 2022)
Objetivo
Explicar cómo describir matemáticamente el comportamiento de un algoritmo cuando el tamaño de la entrada crece indefinidamente.

Puntos clave:
a) Tiempo de ejecución como función del tamaño de entrada
El tiempo de ejecución de un algoritmo depende del tamaño de la entrada, denotado comúnmente como 𝑛.

El análisis se realiza en función de las operaciones elementales ejecutadas, no del tiempo físico.

b) Casos de análisis:
Peor caso (Worst-case): Máximo tiempo que un algoritmo puede tardar para una entrada de tamaño 𝑛.

Caso promedio (Average-case): Tiempo esperado de ejecución en promedio.

Mejor caso (Best-case): Mínimo tiempo posible (usualmente no muy útil para análisis comparativos).

c) Ejemplo: Búsqueda lineal
Para un arreglo de 𝑛 elementos:

Peor caso: el elemento está al final → 𝑇(𝑛)=𝑛T(n)=n

Mejor caso: el elemento está en la primera posición → 𝑇(𝑛)=1T(n)=1

Promedio: 𝑇(𝑛)=𝑛/2T(n)=n/2

d) Uso de funciones de crecimiento se emplean funciones como 𝑛, 𝑛2, 
log n,𝑛 log n, 𝑛 ,etc., para describir el crecimiento.

## 3. Comparación entre Cormen y Brassard

| **Aspecto**              | **Cormen et al. (2022)**                            | **Brassard & Bratley (2006)**               |
|--------------------------|-----------------------------------------------------|----------------------------------------------|
| **Enfoque principal**    | Interpretación práctica del tiempo de ejecución     | Formalización matemática del análisis         |
| **Casos analizados**     | Mejor, peor y promedio                              | Enfocado en comportamiento asintótico         |
| **Notación asintótica**  | Introducida informalmente                           | Explicada con definiciones matemáticas        |
| **Ejemplos**             | Búsqueda lineal, crecimiento de funciones           | Comparación de órdenes de crecimiento         |
| **Aplicabilidad**        | Evaluar algoritmos en diseño y pruebas              | Establecer límites teóricos precisos          |

## 4. Conclusion
Con la lectura del texto que se referencia entiendo que:

- Cormen proporciona una visión práctica para caracterizar tiempos de ejecución.

- Brassard y Bratley profundizan en el uso riguroso de la notación asintótica para comparar algoritmos.

  En conclusion saber ambos enfoques permite seleccionar o diseñar algoritmos eficientes y tomar decisiones informadas en el desarrollo de software y análisis de complejidad computacional.
