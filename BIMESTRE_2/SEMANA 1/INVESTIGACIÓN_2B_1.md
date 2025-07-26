# Informe: Algoritmos Voraces
## Fuente: Brassard & Bratley, 2006

## Introducción

En el campo del diseño de algoritmos, existen varias estrategias que permiten resolver problemas computacionales de forma eficiente. Una de las más utilizadas por su simplicidad y velocidad es la técnica de los algoritmos voraces (greedy algorithms). Esta técnica consiste en tomar decisiones que parecen óptimas en cada paso con la esperanza de llegar a una solución globalmente óptima. En este informe se presenta un análisis claro del enfoque voraz, sus características, condiciones de aplicabilidad y ejemplos típicos, basado en el texto clásico de Brassard y Bratley (2006).

## Objetivos

Comprender el enfoque de diseño conocido como algoritmo voraz.

Identificar los criterios que permiten aplicar esta técnica correctamente.

Conocer ejemplos clásicos donde los algoritmos voraces son efectivos.

Reconocer sus ventajas, limitaciones y diferencias con otras estrategias como programación dinámica o backtracking.

## Desarrollo

### ¿Qué es un algoritmo voraz?

Un algoritmo voraz (greedy) es una estrategia de resolución de problemas que elige siempre la mejor opción disponible en ese momento, sin considerar las consecuencias a largo plazo. Es decir, realiza elecciones locales óptimas esperando que lleven a una solución global óptima.

Este tipo de algoritmo se construye paso a paso:

Se selecciona la opción más prometedora en ese instante.

Se verifica que esa elección sea válida dentro de las restricciones del problema.

Se continúa hasta completar la solución.

### Características clave

Simplicidad: los algoritmos voraces suelen ser más fáciles de implementar que otras técnicas.

Eficiencia: por no explorar todas las posibles combinaciones, suelen ser más rápidos.

No siempre garantizan la solución óptima: solo funcionan correctamente en problemas que cumplen ciertas propiedades matemáticas.

### Condiciones para que funcione un algoritmo voraz

No todos los problemas pueden resolverse correctamente con algoritmos voraces. Para que funcionen, el problema debe cumplir dos propiedades:

Subestructura óptima: una solución óptima del problema contiene soluciones óptimas de sus subproblemas.

Propiedad de elección voraz: se puede construir una solución óptima haciendo elecciones locales óptimas sin necesidad de reconsiderar decisiones anteriores.

Si estas dos condiciones no se cumplen, el algoritmo voraz puede devolver una solución incorrecta o subóptima.

### Ejemplos clásicos

1. Problema del cambio de monedas
Objetivo: devolver una cantidad de dinero usando el menor número de monedas posible.

Algoritmo voraz: tomar la moneda de mayor valor que no supere el monto restante.

Nota: funciona bien si las monedas están bien diseñadas (como en muchos sistemas monetarios), pero puede fallar en otros casos.

2. Algoritmo de Kruskal (árbol de expansión mínima)
Se usa en grafos para construir un árbol de menor costo que conecta todos los nodos.

Selecciona las aristas de menor peso que no formen ciclos.

Este algoritmo sí cumple con las condiciones voraces y garantiza la solución óptima.

3. Algoritmo de Prim (también para árboles mínimos)
Similar a Kruskal, pero comienza desde un nodo y va agregando los más cercanos.

También es voraz y óptimo.

4. Problema de la mochila fraccionaria
Dado un conjunto de objetos con peso y valor, seleccionar los más valiosos hasta llenar una mochila con capacidad máxima.

El algoritmo toma primero los objetos con mayor valor por unidad de peso.

Funciona solo si se permite fraccionar los objetos.

### Ventajas y limitaciones

Ventajas
Rapidez: se evita la búsqueda completa, lo que reduce la complejidad.

Simplicidad: los pasos del algoritmo suelen ser más claros y directos.

Útil como aproximación: incluso cuando no garantiza la solución óptima, puede usarse para obtener soluciones razonables rápidamente.

### Limitaciones

No siempre garantiza la mejor solución.

Se debe verificar que el problema cumpla las condiciones voraces.

No se puede aplicar en problemas donde las decisiones futuras dependen de las elecciones actuales (como en programación dinámica).

### Conclusiones

Los algoritmos voraces son una técnica poderosa para resolver problemas que permiten una estrategia basada en decisiones locales óptimas.

Funcionan bien solo en problemas con subestructura óptima y propiedad de elección voraz.

Son ampliamente usados en grafos, optimización de recursos, planificación y problemas de cobertura.

Aunque no siempre garantizan la solución óptima, su eficiencia y facilidad de implementación los hace muy útiles en la práctica.

