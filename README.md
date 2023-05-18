## Práctica 4: Prolog

**Entrega: 23 de mayo de 2023**

*La práctica podrá realizarse en equipos de máximo 3 integrantes*

### Instrucciones

1. El Dr. Vegapunk ha estado trabajando en la cura un virus mortal de manera secreta. Después de varios meses ha logrado crear de manera satisfactoria una cura, sin embargo, cada experimento ha sido guardado en frascos de colores diferentes y ahora no sabe en cual frasco se encuentra la vacuna final. El Dr. Vegapunk te ha contactado para que le ayudes a saber en qué frascos se encuentra la cura.

 Lo que se sabe es que cada frasco tiene un color diferente: rojo, anaranjado, amarillo, verde, azul y violeta. Después de cierto tiempo el doctor recordó que hay tres pares de frascos, en los que para cada par, sabemos que en uno de los frascos está la cura:
 
 - los frascos violeta y azul.
 - los frascos rojo y amarillo.
 - los frascos azul y anaranjado.

 Por otro lado, el doctor también recuerda que hay tres pares donde para cada par, hay uno en el que definitivamente no está la vacuna.

 - el violeta y el amarillo.
 - el rojo y el anaranjado.
 - el verde y el azul

 Además, parece ser que el frasco rojo contiene mermelada de fresa.

 Define, usando esta información, las consultas y base de conocimientos necesarias para ayudar al Dr. Vegapunk a encontrar la cura.

   ```bash
   ?- cura(rojo).
   false.
   ?- cura(azul).
   ???
   ```
   
2. Define el predicado `nth(XS, N, E)` que es verdadero si E es el n-ésimo elemento de XS.  

   ```bash
   ?- nth([1 ,2 ,3], 1, E).
   E = 1.
   ?- nth([1 ,2 ,3], 10, E).
   false.
   ```
   
3. Define el predicado `rota(XS,N,L)` que es verdadero si L es la lista resultante de rotar N veces XS a la derecha. 

   ```bash
   ?- rotacion([1 ,2 ,3 ,4], 2, X).
   X = [3 ,4 ,1 ,2].
   ?- rotacion ([1 ,2 ,3 ,4], 0, X).
   X = [1 ,2 ,3 ,4].
   ```
   
4. Observe la siguiente consulta y su resultado.

   ```bash
   ?- member(1 ,[1 ,1 ,1 ,1]).
   true;
   true;
   true;
   true.
   ```
   Como se puede observar, no importa si se ha encontrado un elemento, la búsqueda continúa. Define el predicado `pertenece(X, XS)` que es análogo a member, con la diferencia de que basta con encontrar la primer aparación de X para detener la búsqueda.
   
5. Un árbol binario de búsqueda es un tipo especial de árbol binario que tiene la siguientes características:
 - El subárbol izquierdo de un nodo contiene solo nodos con elementos menores que el elemento de la raíz.
 - El subárbol derecho de un nodo contiene solo nodos con elementos mayores que el elemento de la raíz.
 - El subárbol izquierdo y derecho también son arboles binarios de búsqueda.
 
 En Prolog podemos representar árboles binarios de la siguiente manera:
 - El átomo vacio representa al árbol vació.
 - El término compuesto `nodo(N, L, R)` representa un nodo de un árbol en donde N representa el valor de la raíz y L y R son árboles binarios de búsqueda.

Define el predicado `busca(X, Arbol)` que es verdadero si X es un elemento de Arbol.

**Nota**: Asegurarse de no hacer búsquedas innecesarias, para eso se debe de usar el operador de corte.

  ```bash
   ?- busca(2, nodo(2, nodo(1, vacio, vacio), nodo(3, vacio, vacio)).
   true.
   ?- busca(10, nodo(2, nodo(1, vacio, vacio), nodo(3, vacio, vacio)).
   false.
   ```



   **Es requisito indispensable para revisar el resto de ejercicios que esta parte funcione correctamente. En caso contrario la calificación de la práctica será CERO.**
   
### Restricciones

- La hora máxima de entrega será a las **23:59:59** de la fecha indicada al inicio de este documento.

- Para poder pedir una prórroga sobre la entrega es requisito **indispensable** que todos los equipos de estudiantes
  hagan cambios (*commit*) constantes a su repositorio a lo largo del periodo de realización de la práctica.

- **Todas las copias serán calificadas automáticamente con cero**.

