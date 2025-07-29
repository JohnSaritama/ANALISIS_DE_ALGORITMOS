# TEMA 1 : Divide-and-Conquer 

**Fuente:** Cormen et al. (2022) – Capítulo 4



## Introducción

La estrategia **Divide-and-Conquer** (dividir y vencer) es uno de los enfoques más poderosos y ampliamente utilizados en el diseño de algoritmos eficientes. Se basa en descomponer un problema en subproblemas más pequeños, resolver cada uno recursivamente y luego combinar las soluciones para resolver el problema original. En este informe se expone la estructura general de esta técnica según Cormen et al. (2022), con especial atención al análisis mediante recurrencias y el uso del Teorema Maestro.



## Objetivos

- Comprender los tres pasos clave de un algoritmo Divide-and-Conquer.
- Analizar cómo modelar y resolver el tiempo de ejecución usando recurrencias.
- Estudiar el Teorema Maestro y su aplicación.
- Conocer ejemplos típicos y su eficiencia.



## Desarrollo

### Estructura general

Todo algoritmo Divide-and-Conquer sigue este patrón:

1. **Dividir**: El problema de tamaño `n` se divide en `a` subproblemas, cada uno de tamaño `n/b`.
2. **Conquistar**: Se resuelven los subproblemas recursivamente.
3. **Combinar**: Se combinan las soluciones de los subproblemas en una solución para el problema original.

### Forma de recurrencia

El tiempo de ejecución de un algoritmo de este tipo se modela con la siguiente ecuación:





Donde:
- `a`: número de subproblemas generados.
- `n/b`: tamaño de cada subproblema.
- `f(n)`: costo de dividir y combinar.

### Teorema Maestro

Este teorema permite resolver recurrencias y determinar la complejidad de algoritmos Divide-and-Conquer:

- Si `f(n) = O(n^log_b(a - ε))`, entonces `T(n) = Θ(n^log_b a)`
- Si `f(n) = Θ(n^log_b a)`, entonces `T(n) = Θ(n^log_b a * log n)`
- Si `f(n) = Ω(n^log_b(a + ε))` y se cumple la condición de regularidad, entonces `T(n) = Θ(f(n))`

### Ejemplos destacados

- **Mergesort**: `T(n) = 2T(n/2) + Θ(n)` → `Θ(n log n)`
- **Quicksort (mejor caso)**: `T(n) = 2T(n/2) + Θ(n)` → `Θ(n log n)`
- **Multiplicación de matrices de Strassen**: reduce el número de multiplicaciones de 8 a 7 → `T(n) = 7T(n/2) + Θ(n^2)` → `Θ(n^log₂7) ≈ Θ(n^2.81)`



## Conclusiones

- Divide-and-Conquer es una técnica esencial para resolver problemas recursivos de manera eficiente.
- Su análisis formal con el Teorema Maestro permite predecir el rendimiento del algoritmo.
- Es especialmente útil cuando se puede reducir un problema en partes del mismo tipo, y la combinación no es costosa.
- Es la base de muchos algoritmos clásicos usados en ordenamiento, búsqueda, y multiplicación de matrices.



# TEMA 2: Divide y Vencerás  
**Fuente:** Brassard & Bratley (2006) – Capítulo 7

## Introducción

La estrategia **Divide y Vencerás** es un enfoque clásico para resolver problemas algorítmicos complejos descomponiéndolos en partes más pequeñas y manejables. En este informe se explora esta técnica según el enfoque pedagógico de Brassard y Bratley (2006), haciendo énfasis en su estructura recursiva, ventajas, y ejemplos prácticos.

## Objetivos

- Entender la lógica detrás del paradigma Divide y Vencerás.
- Aplicar esta técnica a problemas comunes de ordenamiento y cálculo.
- Comparar su utilidad frente a otros métodos como programación dinámica.
- Reconocer su utilidad práctica a través de ejemplos clave.



## Desarrollo

### Estructura general

La estrategia se basa en tres pasos:

1. **Dividir**: separar el problema en subproblemas más pequeños.
2. **Resolver**: resolver cada subproblema (generalmente de manera recursiva).
3. **Combinar**: unir las soluciones de los subproblemas para resolver el problema original.

Este enfoque se aplica especialmente cuando la división del problema es sencilla y la combinación no implica un alto costo.

### Ejemplos clásicos

- **Mergesort**:
  - Divide el arreglo en dos mitades.
  - Ordena cada mitad recursivamente.
  - Combina las mitades ordenadas.
  - Tiempo de ejecución: `Θ(n log n)`

- **Multiplicación rápida de matrices (Strassen)**:
  - Reduce de 8 a 7 multiplicaciones recursivas.
  - Tiempo: `Θ(n^2.81)`, mejor que el método clásico `Θ(n^3)`

- **Transformada rápida de Fourier (FFT)**:
  - Divide la señal de entrada en dos partes usando propiedades de simetría.
  - Aplica recursión para reducir el tiempo de cálculo a `Θ(n log n)`

### Ventajas

- Código más limpio gracias a la recursión.
- Reducción drástica del tiempo en comparación con métodos iterativos ingenuos.
- Estructura flexible y reutilizable en muchos tipos de problemas.

### Comparación con otras técnicas

- A diferencia de **programación dinámica**, no guarda resultados intermedios.
- Frente a **algoritmos voraces**, Divide y Vencerás puede ser más costoso, pero garantiza la solución óptima en muchos casos.



## Conclusiones

- Divide y Vencerás es una técnica clave para construir algoritmos eficientes y escalables.
- Su enfoque recursivo favorece la claridad y modularidad del código.
- Es ideal para problemas que se pueden descomponer de forma natural.
- Contribuye a soluciones de menor complejidad en problemas críticos como ordenamiento, búsqueda y transformadas.





