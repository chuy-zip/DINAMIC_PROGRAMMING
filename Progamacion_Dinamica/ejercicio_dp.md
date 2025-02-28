# Ejercicio: Solución con Programación Dinámica

En (Soltys 2012) se listan 3 pasos para desarrollar una solución con programación dinámica: definir una clase de subproblemas, proveer una recurencia que resuelva los problemas en términos de subproblemas; y proveer un algoritmo que compute la recurrencia. Itendifique los pasos con los descritos anteriormente. Explique su razonamiento.

---

##### Paso 1: Definir una clase de subproblemas

El primer paso es identificar y formalizar los subproblemas que, en conjunto, abarcan la totalidad del problema original. Esto implica determinar una estructura o parámetro (o conjunto de parámetros) que capture el estado de cada subproblema. Por ejemplo, si se está resolviendo un problema de optimización, se podría definir cada subproblema como la optimización de un prefijo o una parte del conjunto de decisiones. La clave es que:

- Cada subproblema sea más sencillo que el original.
- La solución del problema principal pueda ser construida a partir de las soluciones a estos subproblemas.

##### Paso 2: Proveer una recurrencia que resuelva los problemas en términos de subproblemas

El siguiente paso consiste en desarrollar una recurrencia que exprese la solución de cada subproblema en función de soluciones a subproblemas aún más simples. Esta relación recursiva:

- Determina cómo se combinan los resultados parciales.
- Especifica la “fórmula” que permite obtener la solución de un subproblema a partir de soluciones ya calculadas.
- A menudo se acompaña de condiciones base, que definen los casos más simples para los cuales la solución es directa o conocida.


##### Paso 3: Proveer un algoritmo que compute la recurrencia

Finalmente, se desarrolla un algoritmo que implementa la recurrencia de manera efectiva. En la programación dinámica, este algoritmo suele trabajar de forma "bottom-up" (de abajo hacia arriba):

- Se comienza resolviendo los subproblemas más simples.
- Luego se utilizan esas soluciones para construir soluciones a problemas de mayor complejidad.
- Es crucial almacenar las soluciones de los subproblemas para evitar cálculos redundantes, lo que mejora la eficiencia.
