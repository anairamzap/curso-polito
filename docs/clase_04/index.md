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

**En resumen un array es una colección ordenada porque tiene un índice único, una vez creado no puede cambiar la 
cantidad de elementos que va a contener pero sí se puede cambiar el valor que guardaremos en cada ubicación del
array**
