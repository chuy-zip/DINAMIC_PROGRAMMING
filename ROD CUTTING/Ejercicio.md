# ROD CUTTING PROBLEM

El rod cutting problem es un problema donde se tiene una varilla de largo n. Además de esto también se tiene el valor de los cortes dependiendo del largo del corte. Al final lo que se busca es optimizar la ganancia por cortar la varilla. Osea obtener el máximo ingreso al cortar la varilla pedazos y vender dichos pedazos.

### 3. Identifique las decisiones y los subproblemas en el rod-cutting problem.

#### Decisión:

La decisión que hay que tomar es determinar en donde y de que longitud será el corte de la varilla. Generalmente en este problema se define a un corte con la letra "i", entonces el resto de la varilla luego de un corte sería n - i. Se tiene que decidir cual es el primer corte. Otra decisión por lo que tengo entendido es decidir si cortar o no también. Puede que en un caso sea más conveniente dejar de cortar que cortar hasta estar muy cerca de 0.

#### Subproblemas:

Cada vez que se corta la varilla, se generan 2 sobproblemas. Si se tiene una varilla y se corta, luego se tienen 2 varillas. A estas se les puede hacer un corte siempre y cuando el largo sea mayor que 0 para poder vender el pedazo cortado. Cada que se corta la varilla, es que se da un subproblema. Si se vuelve a cortar hay aún más subproblemas de rod cutting y así sucesivamente.Suponemos que el corte en i lleva solución óptima.

### 4. Demuestre que el rod-cutting problem exhibe subestructura óptima, completando la respuesta anterior con la demostración de necesaria optimalidad.

Imaginemos que cortamos la varilla, Luego de cortar la varilla imaginemos que las 2 varillas no se cortan optimamente. Eso quiere decir que obtendríamos 2 ganancias que no son óptimas. Si tenemos 2 ganancias menores/no optimas (c1,c2) eso quiere decir que existe un corte donde las ganacias son mejores que el corte que hicimos previamente (c3,c4 donde c3 y c4 son mejores). Pero en este punto es que estaríamos contradiciendo el supuesto original, porque estaríamos diciendo que el corte i que hicmos inicialmente, no fue óptimo cuando debió habrlo sido. Entonces para que el cortie inicial seá óptimo, las sub varillas deben ser óptimos con sus cortes también. Los cortes de los subproblemas deben ser óptimos si queremos que el corte general de la varilla sea óptimo para maximizar la ganancia. Con esto vemps que hay subestructuras óptimas en el problema. Si el corte inicial es óptimo, las sub varillas deben serlo también, sino tendríamos el problema de determinar todas los posibles subcortes.