# TRABAJO DE INVESTIGACION

## Nombre:John Paul Saritama

## Fecha:22/04/2025


## 1.Diseño de algoritmos (Tema 2.3 - Cormen et al., 2022)

### 1. Introducción
El diseño de algoritmos es una parte fundamental de la informática teórica y práctica. En la sección 2.3 del capítulo "Getting Started", los autores Thomas H. Cormen y sus colaboradores presentan un ejemplo de cómo desarrollar un algoritmo desde cero, utilizando un enfoque estructurado y orientado a la resolución de problemas.

El objetivo de esta sección es mostrar cómo se puede diseñar un algoritmo eficiente a partir de un problema definido, guiando al lector por el proceso de análisis, planificación, implementación y verificación.

### 2. El problema: Multiplicación de enteros grandes
El ejemplo central utilizado en esta sección es el problema de multiplicar dos enteros muy grandes, es decir, números con cientos o miles de dígitos, lo que excede la capacidad de los tipos de datos estándar.

Se parte de la observación de que el método tradicional de multiplicación de lápiz y papel (el algoritmo de la escuela primaria) tiene una complejidad de tiempo de 
𝑂(𝑛2) O (n 2), siendo 𝑛
n la cantidad de dígitos de los números.

### 3. Primera solución: Enfoque directo
El enfoque inicial consiste en implementar el algoritmo clásico de multiplicación de dígitos:

Para cada dígito del primer número, se multiplica por cada dígito del segundo número.

Luego se realiza una suma desplazada de los resultados parciales.

Esta solución es funcional pero no eficiente para números extremadamente grandes.

### 4. Mejora con divide y vencerás
Aquí es donde los autores introducen la estrategia de diseño de algoritmos "divide y vencerás", que consiste en:

Dividir el problema en subproblemas más pequeños.

Resolver cada subproblema de forma recursiva.

Combinar las soluciones parciales para obtener la solución final.

​![image](https://github.com/user-attachments/assets/689e9156-bee9-4462-9e46-8e54a5ec3e07)

### Primer ciclo  while:

![image](https://github.com/user-attachments/assets/e9311ae5-ca06-4124-a004-f15a8e74bc6d)

### 5. Lecciones clave del diseño de algoritmos
Los autores destacan varios principios importantes para diseñar buenos algoritmos:

Buscar patrones en la estructura del problema.

Utilizar recursión para dividir problemas grandes en problemas más simples.

Analizar el tiempo de ejecución, ya que la eficiencia es crítica.

Pensar en alternativas más allá de la solución inmediata o intuitiva.

Elegir estructuras de datos adecuadas para facilitar operaciones rápidas.
