# TEMA 1: Algoritmos Probabilistas  
**Fuente:** Brassard & Bratley (2006) – Capítulo 10


## Introducción

En muchos problemas de computación, especialmente cuando el tamaño de los datos es muy grande o el problema es complejo, los algoritmos tradicionales no resultan prácticos. En estos casos, los **algoritmos probabilistas** ofrecen una solución más rápida y flexible, incorporando el uso de números aleatorios en su ejecución. Aunque su comportamiento no siempre es predecible, su eficiencia los hace ideales para ciertas tareas como verificación rápida o búsquedas en estructuras grandes.

Este informe revisa la idea general, los tipos principales y ejemplos representativos de esta técnica, tal como se presenta en Brassard y Bratley (2006).


## Objetivos

- Explicar el concepto de algoritmo probabilista y su importancia.
- Diferenciar entre los tipos Monte Carlo y Las Vegas.
- Analizar ejemplos comunes de uso.
- Valorar las ventajas y limitaciones de este enfoque.


## Desarrollo

### ¿Qué son los algoritmos probabilistas?

Un **algoritmo probabilista** utiliza una fuente de aleatoriedad (como una función que devuelve un número aleatorio) como parte de su lógica interna. Esto significa que la **misma entrada puede dar resultados distintos** en diferentes ejecuciones.

A diferencia de los algoritmos deterministas, donde todo está perfectamente definido, aquí las decisiones se toman en parte al azar. Sin embargo, ese “azar” está **controlado matemáticamente** y permite obtener resultados útiles en menos tiempo.


### Tipos de algoritmos probabilistas

#### 1. Algoritmos Monte Carlo
- Ejecutan siempre en un **tiempo fijo o controlado**.
- **Pueden fallar**, es decir, dar una respuesta incorrecta, aunque con baja probabilidad.
- Se usan cuando se necesita rapidez y se puede aceptar un pequeño margen de error.

**Ejemplo**:  
El **algoritmo de Miller–Rabin** se utiliza para verificar si un número es primo. No siempre garantiza la respuesta correcta, pero si se repite varias veces, la probabilidad de error se reduce drásticamente.

#### 2. Algoritmos Las Vegas
- **Siempre producen una respuesta correcta**.
- Su **tiempo de ejecución no es fijo**: depende del azar cuántas veces se ejecuten ciertos pasos.
- Son útiles cuando no se puede aceptar error, pero se tolera variabilidad en el tiempo.

**Ejemplo**:  
Un algoritmo que elige un pivote aleatorio en quicksort puede ser más eficiente en promedio que una versión determinista.


### ¿Por qué usar algoritmos probabilistas?

Los algoritmos probabilistas son útiles cuando:
- No se conoce una solución determinista eficiente.
- Se necesita una solución aproximada o rápida.
- El problema es tan grande que una solución exacta sería demasiado lenta.

Brassard y Bratley señalan que **la simplicidad** y **velocidad promedio** de estos algoritmos los hace preferibles en contextos como:
- Criptografía
- Verificación de grandes cálculos
- Simulaciones aleatorias
- Búsqueda de patrones


### Ejemplos importantes

- **Freivalds**: verifica si A × B = C para matrices, sin hacer la multiplicación completa. Usa aleatoriedad para hacer una verificación más rápida.
- **Hashing aleatorio**: en tablas hash, se utilizan funciones hash aleatorias para distribuir elementos uniformemente y evitar colisiones.
- **Métodos de Monte Carlo en simulaciones**: se aplican para estimar integrales, simular procesos físicos o financieros.


## Conclusiones

- Los algoritmos probabilistas ofrecen una alternativa poderosa a los métodos clásicos, especialmente en contextos donde se necesita rapidez.
- Aunque algunos pueden fallar (Monte Carlo), sus errores pueden controlarse estadísticamente.
- Otros, como los de tipo Las Vegas, nunca fallan pero pueden tardar más en algunos casos.
- Su uso es cada vez más común en problemas reales, gracias a su eficiencia en promedio y la facilidad de implementación.
- Son una herramienta clave en la computación moderna, particularmente en inteligencia artificial, criptografía y análisis de datos.
