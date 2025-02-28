# ROD CUTTING PROBLEM (BUTTOM-UP)

## 11. Provea el pseudocódigo que calcula el valor de la solución óptima para el rod-cutting *problem* usando el acercamiento *bottom up*

Para encontrar la solución del Rod Cutting problem (buttom-up) debemos utilizar
algoritmo iterativo que recorre cada nodo del arbol hasta encontrar la mejor solución.

```{pseudo}
Buttom-Up-Cut-Rod(n, p):
    let arr[0..n]                       // Creamos el arreglo
    arr[0]                                // Para la longitud 0 no hay ganancia

    for j = 1 hasta n:                  // Se exploran todos los cortes posibles desde 1 hasta j
        q = -inf
        for i = 1 hasta j:              
            q = max(q, p[i] + arr[j - i]) // Se busca la máxima ganancia entre p[i] y r[j-i]
        arr[j] = q
    
    return r[n]                         // El resultado final se encontrará en r[n]
```

El algoritmo consiste en:
- Crear el arreglo arr
- Inicializar arr[0] como la no ganancia para el corte 0
- Iterar sobre todos los cortes posibles
- Buscar la ganancia máxima entre p[i] y arr[j-i]
- Cuando lleguemos a r[n] el resultado estará almacenado en el *n* elemento de arr

## Knowledge Check
¿Qué representa el índice i en el algoritmo Bottom-Up-Cut-Rod?

r// Representa las posibles posiciones de corte para el subtubo de longitud j
