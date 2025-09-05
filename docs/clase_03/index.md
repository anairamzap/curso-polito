---
icon: material/code-braces
---

# Clase 03: Más variables

## {==A que llamamos "casteo"==} 
¿Qué es el casteo?

En Java, castear significa convertir un valor de un tipo de dato a otro. <br>
El compilador necesita que le indiques cómo transformar un dato para que “encaje” en el nuevo tipo.<br>
Es como decirle a Java: “tratá este valor como si fuera de este otro tipo”. <br>
¿Por qué necesitaríamos hacer esto? <br>
¡Buena pregunta!

Hagamos está operación en nuestra IDE:
```java
int numero1 = 19; <br>
int numero2 = 2;

double resultado = numero1 / número 2;

System.out.print("El resultado de la división es: " + resultado);
```
Ejecutamos el programa y vamos a tener la salida por consola: 9.0 <br>
Sabemos que el tipo de dato double maneja número con coma, entonces ¿Por qué el resultado es incorrecto, 
sabemos que es 9,5? <br>
Esto es porque el compilador no puede manejar automáticamente la transformación de tipo int a tipo double ya que 
los lenguajes crean sus datos gracias a estándares que se consensúan internacionalmente. <br>
¡NO es algo que a alguien se le ocurre y listo! <br>
Por lo tanto cuando nosotros decimos que vamos a crear un dato del tipo int, el compilador, 
basándose en esos estándares construye el dato.

Imaginemos que tenemos dos ficheros donde guardamos todos los nombres de las personas que conocemos en orden 
alfabético. <br>
En el primero tenemos los nombres de la **A a la M** y en el segundo tenemos los nombres de la **N a Z**. <br>
Después creamos otro fichero donde vamos a guardar, también organizado alfabéticamente, todos los nombres de 
la **A a la Z**. <br>
Ahora bien, viene una compañera o compañero y nos pide los primeros 100 nombres.
Nosotros se los damos. <br>
Pero cuando nuestra compañera o compañero lo va a guardar en el fichero que le dieron descubre que su fichero 
**está organizado en grupos**. Por ej: Familiares, Amigos, Trabajo, etc. <br><br>
Queda claro que si no lo organiza antes de guardarlo va a tener todos los contactos desordenados y sería inservible.
<br><br>
En resumen, castear es la manera que tenemos en Java de decirle al compilador cómo convertir un dato para 
que encaje en otro tipo, sin perder de vista que a veces puede haber pérdida de información.


**MUY IMPORTANTE**: Lo que hay que entender es que siempre tenemos el mismo tamaño de datos.
Recordemos lo que vimos en la clase de tipos de datos primitivos.
Cuando creábamos un int, estábamos creando un dato de 32 bits. Y cuando creábamos un float también estábamos 
creando un dato de 32 bits. <br>
**→ Solo cambia la forma de organizar esos bits.**

Pasemos ahora a como se hace el casteo. Es muy simple.


Nuestro ejemplo quedaría así
```java
int numero1 = 19;
int numero2 = 2;

double resultado = (double) numero1 / número 2;

System.out.print("El resultado de la división es: " + resultado);
```
Si ejecutamos el programa ahora vamos a tener el resultado que necesitamos.
<br>
<br>
## {==Clase Scanner==} 

La Clase Scanner forma parte del paquete java.util. O sea es un elemento dentro de ese paquete que contiene 
muchas otras utilidades. <br>
Algo muy práctico a la hora de programar.
<br><br>
¿Para que nos sirve esta utilidad? <br>
Principalmente se usa para interactuar con el usuario para que este ingrese datos a nuestro programa.

Por ejemplo: Tenemos que calcular el área de un cuadrado. Sabemos que la fórmula es L x L (lado por lado), 
pero no nos dan el valor sino que nos piden que se lo pidamos al usuario.
<br>¿Como hacemos eso?

Tenemos que crear una variable usando la Clase Scanner.

Hacemos en nuestra IDE dentro de nuestra función Main:<br><br>
```java
Scanner ingreso = new Scanner(System.in);<br>
System.out.println(“Ingrese el valor del lado del cuadrado ”);<br> 
int lado = ingreso.nextInt();

int area = lado * lado;

System.out.println(“El area del cuadrado es: ” +  area);
```
Si ejecutamos el programa vamos a ver en consola que el programa queda detenido en el mensaje: <br>
**Ingrese el valor del lado del cuadrado** 

Eso es porque está esperando la intervención del usuario. <br>
Si hacemos clic con el mouse en la consola nos va aparecer un promp (van a  ver esté símbolo | parpadeando) <br>
Ahí ya pueden ingresar un número y al presionar enter el programa va calcular el área, lo va a mostrar por la consola y va a terminar.

Está Clase permite la entrada por teclado distintos tipos de datos. <br>
(usamos en este caso la misma variable que creamos en primer ejemplo: 
Scanner ingreso = new Scanner(System.in);) <br><br>
Algunos ejemplos son:

Para textos: <br>
```java
String nombre = ingreso.next()<br>
```
Para un número float:<br>
```java
float numFloat = ingreso.nextFloat();<br>
```
Para un número double:<br>
```java
double numDouble = ingreso.nextDouble();<br>
```
