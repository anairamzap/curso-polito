---
icon: material/code-braces
---

# Clase 04: Arrays (vectores y matrices)

**DEFINICIÓN:**<br>
Los arrays en java son una colección ordenada, indexada y de tamaño fijo. Cuyos elementos pueden cambiar de valor pero 
no de tipo.<br>
Esto que a primera vista es complejo y confuso lo vamos a ir desgranando paso a paso para entenderlo. 


## {==Vectores (Arrays unidimensionales)==}

Empecemos por este tipo de array para adentrarnos en estos conceptos.

Imaginemos que tenemos un estante donde ubicamos una serie de cajas, por ej: 10 cajas<br>
Es importante que las cajas sean iguales y pueden contener un solo tipo de elemento, por ejemplo: zapatillas<br>
Debajo de cada caja vamos a numerar el orden de las cajas.<br>
Acá hagamos una aclaración.<br>
Naturalmente si nosotros les decimos que numeren el orden de las cajas, ustedes harían: **1, 2, 3, ... 10**<br>
Pero para nuestro ejemplo lo vamos hacer iniciando en 0. O sea, nos quedará: **0, 1, 2, 3, ... 9**<br>
¿Por qué es esto?<br>
Porque tenemos que recordar que el 0 para nosotros es un valor (existe) y siempre lo tomamos como el primer número
entero positivo.

Si volvemos a nuestro ejemplo nos quedaría algo parecido a la imagen <br>

<img src="../../images/estante.jpg">

Pasemos a trabajar con un Array unidimensional en java. <br>
Crear un vector no es otra cosa que crear una variable y declarla de una manera que el compilador entienda que lo 
que estamos creando es un array.<br>
A lo que ya sabemos en la declaración de una variable del tipo entera:

```java
int numero = 4;
```

La modificamos de está manera:

```java
int[] numeros = new int[3];
```

Como podemos ver, a el formato que aprendimos al declarar variables le hicimos algunos cambios.<br>
Tenemos<br> 
TIPO    IDENTIFICADOR   OPERADOR    VALOR<br>

Analicemos lo que cambió: <br>
En el TIPO: Le agregamos el modificador [] (corchete de apertura y de cerrado)<br>
Ese modificador le dice al compilador que estamos creando un array.<br>
Y finalmente después del operador relacional "=" vemos que para el valor usamos: **new int[3]**;<br>
Si aprovechamos la analogía de nuestro estante, estamos diciendo:<br>
Vamos a crear un estante nuevo con 3 cajas.<br>
Si ajustamos nuestro código a la analogía de nuestro estante haríamos esto:

```java
int[] numeros = new int[10];
```
Creamos un estante con 10 cajas para guardar enteros.<br>
Es importante entender que solo estamos creando el estante con las cajas y su número identificador, pero todavía no hemos
puesto números adentro de esas cajas.<br>
Tendríamos esto:<br>
Caja 0 -> vacía <br>
Caja 1 -> vacía <br>
Caja 2 -> vacía <br>
Caja 3 -> vacía <br>
...<br>
Caja 9 -> vacía <br>

Ahora bien. Lo que necesitamos ahora es llenar esas cajas.<br>
Pasando a nuestro código lo hacemos así:<br>

```java
int[] numeros = new int[4];

numeros[0] = 25;
numeros[1] = 2;
numeros[2] = -8;
numeros[3] = 123;
```

Como podemos ver usamos el identificador del array con el número de orden (índice) entre corchetes para que el 
compilador sepa exactamente donde ubicar el valor.<br>
O sea en la primera caja, que tiene como índice 0, le ponemos el valor 25 adentro.<br>
En la segunda caja, con el índice 1, le ponemos el valor 2 adentro.<br>
En la tercera caja, con el índice 2, le penemos el valor -8 adentro.<br>
En la cuarta caja, con el índice 3, le penemos el valor 123 adentro.<br><br>

##Si queremos ver por consola el contenido de algún elemento del arrays, hacemos

```java
System.out.println(numeros[0]); // muestra el contenido de la caja 0 → imprime 25
System.out.println(numeros[1]); // muestra el contenido de la caja 1 → imprime 2
System.out.println(numeros[2]); // muestra el contenido de la caja 2 → imprime -8
System.out.println(numeros[3]); // muestra el contenido de la caja 3 → imprime 123
```



##Ahora cambiemos algún valor de los ya asignados a nuestro array<br>
Si hacemos esto

```java
numeros[2] = 1000;
```

Cuando lo mostremos por consola, veremos esto:
```java
System.out.println(numeros[0]); // muestra el contenido de la caja 0 → imprime 25
System.out.println(numeros[1]); // muestra el contenido de la caja 1 → imprime 2
System.out.println(numeros[2]); // muestra el contenido de la caja 2 → imprime 1000
System.out.println(numeros[3]); // muestra el contenido de la caja 3 → imprime 123
```


**Por último veamos otra manera de declarar un array.<br>**
Podemos crear el array y darle valores a cada índice en la misma declaración. Lo único que cambia es la forma de darle 
valor después del operador relacional<br>

```java
int[] numeros = {55,1, 0, 29, 44, 100};
```

En este caso estamos creando un estante con 6 cajas y al mismo tiempo las llenamos con esos valores.<br>
En la primera caja, que tiene como índice 0, le ponemos el valor 55 adentro.<br>
En la segunda caja, con el índice 1, le ponemos el valor 1 adentro.<br>
En la tercera caja, con el índice 2, le penemos el valor 0 adentro.<br>
En la cuarta caja, con el índice 3, le penemos el valor 29 adentro.<br>
En la quinta caja, con el índice 4, le penemos el valor 44 adentro.<br>
En la sexta caja, con el índice 5, le penemos el valor 100 adentro.<br>

Al hacerlo de está manera el compilador entiende que cada coma separa un valor de otro.
<br><br>
## {==Matrices (Arrays bidimensionales)==}

Ahora ampliemos la analogía que usamos para el vector.<br>
Vamos a crear una estantería en lugar de solo un estante. Entonces vamos a tener varios estantes del mismo tamaño
<br><br>
<img src="../../images/estanteria.png">
<br><br>
Fíjense que ahora cada estante tiene otro índice.<br>
Para que lo veamos claramente lo pusimos en color verde.<br>
Tenemos 4 filas (los números en verde) y cada fila tiene 10 columnas (los números en celeste)<br>
En nuestra estantería armamos un primer estante (0, recordemos que nuestro primer número natural es 0, no 1) con 
10 cajas.<br>
De la misma manera para el segundo: Tendrá el índice 1 y 10 cajas también.<br>
Así hasta el último estante = 3.<br>
Es importante recordar que no puede hacer un estante con 3 cajas. Todos los estantes tienen el mismo tamaño.<br>
Vayamos a como lo declaramos nuestra estantería en java.<br>

```java
int[][] matriz = new int[4][10];
```
Fíjense que es similar al vector, solo le agregamos otra dimensión.<br>
En el vector hacíamos, por ejemplo
```java
int[] vector = new int[10];
```

Solo decimos cuantos lugares va a tener el estante. En este caso va a tener 10 lugares.<br>
En la matriz le agregamos cuantas filas va a tener.<br>
Esa nueva dimensión va antes de lo que teníamos, por eso [4] va antes de las columnas:<br>

```java
int[][] matriz = new int[4][10]
```
Ahora hablemos de como el asignamos valores. Como hay dos dimensiones si queremos darle valor a nuestra
matriz tenemos que especificar a qué fila y qué columna nos referimos.<br>
Si queremos cargar un valor en el primer lugar. Nuestra primer caja de nuestro primer estante<br>
<img src="../../images/primerLugar.png">
<br>
<br>
Lo hacemos así:

```java
matriz[0][0] = 22;
```

Es la fila 0 y la columna 0.<br>
Si queremos llenar más cajas de nuestro primer estante tenemos que usar la referencia al estante y 
vamos cambiando la caja donde guardar el valor. Por ej: el primer estante con la segunda y tercer caja.<br>

```java
matriz[0][1] = 13;
matriz[0][2] = 8;
```

¿Y si queremos guardar en la décima caja?<br>

```java
matriz[0][9] = 2;
```

¿Y si queremos guardar en la cuarta caja del tercer estante?<br>
<img src="../../images/cuartoLugarTercerEstante.png">
<br>
<br>
```java
matriz[2][3] = 55;
```

De manera similar si lo queremos mostrar por consola. Tenemos que hacer referencia a los dos 
índices: el de la fila y el de la columna.

```java
System.out.println(“Mostramos el último valor que agregamos: ” + matriz[2][3]);
```
<br><br>
### Ahora vamos a declarar la matriz y asignarle valores a las posiciones, lo hacemos de está manera.

```java
int [ ][ ] numeros = {{72,55,89},{21,3,1}};
```

Separemos por grupos para ver como se construye la asignación de valores.<br><br>
Tomemos la parte de asignación de valores -> {{72,55,89},{21,3,1}}<br><br>
Las primeras llaves { } corresponden al bloque que corresponde a la matriz completa.<br>
Las llaves interiores separadas por la coma (,) agrupan los valores por fila y columna.<br>
Por lo tanto {72,55,89} son los valores de la primera fila, la que tiene índice 0 y las columnas de esa fila.

Fila 0 → Columna 0 = 72
Fila 0 → Columna 1 = 55
Fila 0 → Columna 2 = 89

El otro grupo {21,3,1} son los valores de la segunda fila, con índice 1 y sus correspondientes columnas.

Fila 1 → Columna 0 = 21
Fila 1 → Columna 1 = 3
Fila 1 → Columna 2 = 1
La impresión por consola es igual a lo que ya hemos hecho.

## {==Matrices (Arrays tridimensionales)==}

Algo importante a tener en cuenta es que se puede agregar una capa más.<br>
Este escenario es del caso de la programación y diseño 3D. Por ejemplo: Unity.<br>
Unity es un motor de videojuegos que se programa y diseña en 3D.

Vayamos a ver un ejemplo.<br>
Supongamos que nuestra estantería es como un cubo: 3 estantes con 3 cajas en cada columna y 3 filas de cajas 
en cada estante. 

<img src="../../images/cubo_original.png"> <br><br>

Para poder usarlo como figura de referencia tenemos que determinar sobre que lados vamos a 
identificar nuestras filas, columnas y la profundidad del cubo.

<img src="../../images/cubo_matriz_ejes.png"> <br><br>

O sea todos los lugares del cubo se van a identificar de está forma general: <br>
cubo[x][y][z]
<br>
En la figura marcamos cada eje, su índice y la “dirección” en la que tiene su dominio con un mismo color.<br> 
El eje X es en color naranja, el eje Y en negro y el eje Z en azul.<br>
Ahora marquemos 3 lugares de nuestro cubo para poder determinar sus coordenadas.<br>
Veamos la siguiente figura:


<img src="../../images/cubo_matriz_ejes_puntos.png"> <br><br>

Podemos ver los lugares donde están a, b y c.<br>
Para el lugar “a” vemos que está en línea con la coordenada 1 de X. La coordenada 1 de Y. Pero no tiene 
desplazamiento sobre el eje Z, está al frente del cubo. O sea corresponde con la coordenada 0 del eje Z.<br>
Obviando por ahora la sintaxis de java podemos identificar el punto a de la siguiente manera.<br><br>
cubo[1][1][0] <br><br>
Analicemos el punto “b”. Sobre el eje X está en la coordenada 2. Sobre el eje Y está en la coordenada 1 y tiene 
la coordenada 1 del eje Z.<br>
Por lo tanto lo podemos identificar así:<br><br>
cubo[2][1][1] <br><br>
Por último tenemos el punto “c” que su coordenada X es 2, su coordenada Y es 0 y la coordenada Z es 2.<br>
Nos quedaría así:<br><br>
cubo[2][0][2]

Ahora pasemos a como declaramos una matriz tridimensional en java.<br>
Sigamos con el tamaño de la matriz que tenemos en la figura, la declaramos así<br>
```java
int[ ][ ][ ] matriz3D = new int[3][3][3];
```

Recuerden que al igual que en el caso del vector y de la matriz bidimensional en este tipo de declaración 
hacemos una matriz nueva indicando solo el tamaño. No le estamos asignando valores a la matriz.
<br>
Para asignarle valores hacemos parecido a lo que ya hicimos en los casos anteriores solo que necesitamos indicar 
las 3 coordenadas.<br>
Vamos a ingresar un valor en la primera ubicación de la matriz. La 0, 0, 0.<br>

<img src="../../images/cubo_matriz_ejes_punto0-0-0.png"> <br><br>

```java
matriz3D[0][0][0] = 77;
```

Si por el contrario queremos ingresar un valor en la última ubicación de la matriz, sería:
```java
matriz3D[2][2][2] = 134;
```

Y en la figura sería el punto que está al fondo y abajo a la derecha.<br>

<img src="../../images/cubo_matriz_ejes_punto2-2-2.png"> <br><br>

Ahora nos falta crear la matriz y asignar valores al mismo tiempo.<br>
Como referencia tenemos que pensar que necesitamos un par de llaves de apertura y de cierre por cada capa 
que agreguemos a nuestra matriz.
Nuestra matriz, la de la figura es de 3 x 3 x 3. Al crearla vamos a tener esto:<br>

```java
int[][][] cubo = { //Está llave representa al contenedor más grande que sería el cubo en sí
            
            {//Está llave es la apertura de todas las posiciones de la fila 0
                
                {72,55,89}, {21,3,1}, {18,19,4}
                    
            },
            {//Está llave es la apertura de las posiciones correspondiente a la fila 1
                
                {33,5,6}, {12,0,8}, {129,65,113}
                    
            },
            { //Está llave es la apertura de las posiciones correspondiente a la fila 2
                {77,54,7}, {88,11,71}, {54,7,10}
            }
        
    };
```
Tomemos este trozo de código:

{72,55,89}, {21,3,1}, {18,3,4}

Aquí tenemos que **cada coma entre las llaves separa las columnas y cada número separado por coma es la 
posición correspondiente a la profundidad: El eje Z**


Por ejemplo si quiero imprimir por consola el valor 129 que está en está parte del código:<br>
<pre>
{ //Está llave es la apertura de las posiciones correspondiente a la fila 1<br>
        {33,5,6},    {12,0,8},    {129,65,1}<br>
	//Columna0, Columna1,  Columna2
},
</pre>
Lo haríamos así:<br>
```java
System.out.println("Valor que se encuentra en el lugar  [1][2][0]: " + cubo[1][2][0]);
```
<br>
**En resumen** <br><br>
**Definición técnica en Java**<br>

**Array (vector 1D):**
1. Ordenado en una dimensión
2. Tamaño fijo (cantidad de elementos)
3. Acceso indexado con 1 índice
4. Mutable en contenido
<br>
**Array bidimensional (matriz 2D):**
1. Ordenado en dos dimensiones (filas y columnas)
2. Tamaño fijo (cantidad de filas y de columnas)
3. Acceso indexado con 2 índices [fila][columna]
4. Mutable en contenido

**Array tridimensional (cubo 3D):**
1. Ordenado en tres dimensiones (ejes X, Y y Z)
2. Tamaño fijo en cada dimensión
3. Acceso indexado con 3 índices [x][y][z]
4. Mutable en contenido
5. Puede pensarse como un conjunto de matrices 2D apiladas
