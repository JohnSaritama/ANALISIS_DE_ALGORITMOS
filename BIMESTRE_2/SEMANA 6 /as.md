
# TEMA 1: Algoritmos Probabilistas  
**Fuente:** Brassard & Bratley (2006) – Capítulo 10


## Introducción

Los **algoritmos probabilistas** son algoritmos que hacen uso de la aleatoriedad para tomar decisiones durante su ejecución. A diferencia de los algoritmos deterministas, estos pueden producir distintos resultados aun con la misma entrada, dependiendo de las elecciones aleatorias que realicen. Esta clase de algoritmos es fundamental cuando se necesita eficiencia en promedio o cuando no existe un método determinista práctico.

El capítulo 10 de *Fundamentos de algoritmos* de Brassard y Bratley (2006) presenta una introducción clara a los algoritmos probabilistas, sus tipos, ejemplos comunes y su análisis de eficiencia.


## Objetivos

- Comprender qué es un algoritmo probabilista y cómo se diferencia de uno determinista.
- Conocer los principales tipos: Monte Carlo y Las Vegas.
- Analizar ventajas, desventajas y áreas de aplicación.
- Estudiar ejemplos prácticos y cómo se mide su desempeño.


## Desarrollo

### ¿Qué es un algoritmo probabilista?

Un algoritmo probabilista incorpora **elecciones aleatorias** como parte de su lógica. Al ejecutarlo varias veces con la misma entrada, puede:
- **Dar distintos resultados** (si es un algoritmo de tipo Monte Carlo).
- **Tardar distinto tiempo en completarse**, pero siempre da el mismo resultado correcto (si es tipo Las Vegas).

Estos algoritmos **no son incorrectos** por ser aleatorios; de hecho, su uso puede permitir soluciones más rápidas o más simples a problemas complejos.


### Tipos de algoritmos probabilistas

#### 1. Algoritmos de **Monte Carlo**
- **Siempre se ejecutan en tiempo acotado**, pero **pueden dar una respuesta incorrecta con baja probabilidad**.
- Muy útiles cuando se desea rapidez y se puede tolerar cierto margen de error.
- La probabilidad de error puede reducirse ejecutando el algoritmo varias veces y tomando decisiones por mayoría.

**Ejemplo típico**: Verificación de primalidad (algoritmo de Miller–Rabin).

#### 2. Algoritmos de **Las Vegas**
- **Siempre producen una respuesta correcta**, pero su tiempo de ejecución **puede variar** dependiendo del resultado de las decisiones aleatorias.
- No aceptan errores, solo incertidumbre en el tiempo.
- También pueden convertirse en algoritmos de Monte Carlo si se les impone un límite de tiempo.

**Ejemplo típico**: Selección aleatoria en quicksort con pivotes aleatorios.


### Ejemplos prácticos

- **Verificación de primalidad**: Probabilista de Monte Carlo como Miller–Rabin permite probar números grandes en tiempo rápido.
- **Algoritmo de Freivalds**: Verifica la multiplicación de matrices A * B = C con alta probabilidad y en menor tiempo que recalcular el producto completo.
- **Algoritmos de hashing**: Muy utilizados en estructuras de datos eficientes como tablas hash.
- **Algoritmos de búsqueda y aproximación**: Se usan cuando el conjunto de soluciones es muy grande y la búsqueda exacta sería costosa.


### Análisis de eficiencia

En los algoritmos probabilistas se considera:
- **Complejidad esperada**: tiempo promedio esperado sobre muchas ejecuciones.
- **Probabilidad de error**: en algoritmos de Monte Carlo, se mide cuán probable es que falle.
- **Tiempo en el peor caso**: útil para comparar con algoritmos deterministas.

Brassard y Bratley destacan que, en muchos casos, los algoritmos probabilistas son **más simples y más rápidos** que los deterministas conocidos, aunque hay que tener en cuenta su naturaleza no determinista.


## Conclusiones

- Los algoritmos probabilistas representan un enfoque poderoso y práctico para resolver problemas complejos con eficiencia aceptable.
- Existen dos grandes tipos: Monte Carlo (permiten errores) y Las Vegas (siempre correctos, tiempo variable).
- Son ampliamente utilizados en áreas como criptografía, verificación, búsqueda, algoritmos numéricos y más.
- Aunque implican incertidumbre, su análisis permite controlar su exactitud y eficiencia, lo que los hace herramientas clave en la programación moderna.


