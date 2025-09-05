---
icon: material/code-braces
---

# Clase 02: Variables + Expresiones
En esta clase veremos qué son las variables y constantes, aprenderemos a definirlas y usarlas junto con los
elementos que vimos hasta ahora (nuestros tipos primitivos, cadenas de texto o `String` y operadores). Veremos también a
qué se llama "expresión" y cómo las construimos.

## Variables
Una variable es un contenedor en el que se guarda un valor o dato. Sería algo similar a una caja donde _metemos_ un valor
y a la que le ponemos una etiqueta en el frente.
La etiqueta es el nombre o, técnicamente hablando, el **identificador** de la variable, que nos va a permitir acceder a
ella (y así a su valor), manipularla y reutilizarla.

Las variables nos permiten reutilizar valores tantas veces como queramos sin tener que estar repitiendo ese valor cada
vez. El nombre de la variable se convierte entonces en una **representación del valor** que le *_asignamos_* (atención a
esta palabrita).

Por otro lado, y como lo indica su nombre, las variables pueden cambiar su valor a lo largo de nuestro programa. Por
ejemplo, una variable `nombre` puede tener un valor inicial de **"Juan Domingo"** y luego ese valor puede transformarse
en **"Cristina"**.

???+ note "Variable"
    Una variable es un elemento en el que podemos almacenar datos.

     - Tienen un identificador (o nombre) :label:
     - Su valor puede modificarse a lo largo de la ejecución del programa :fontawesome-solid-arrows-spin:
     - En Java, debemos especificar su _tipo_ :material-shape:

¿Cómo creamos entonces una variable? Bien sencillo, vamos a escribir el nombre o **identificador** de nuestra variable,
pero ¡OJO! :eyes: En Java, al ser un lenguaje de tipado estricto, debemos además decirle al sistema qué tipo de dato
vamos a querer guardar ahí. Esto se llama en programación **declaración de variables**. Porque al crearla estamos también
declarando su **tipo** y comprometiéndonos con el sistema a sólo guardar valores que sean admitidos por ese tipo. Veamos:

Imaginemos que estamos trabajando en un sistema que manejará la compra de entradas en una sala de teatro, y necesitamos
entonces en algún momento de nuestro programa definir y guardar la cantidad total de asientos que tiene la sala.

```java
byte totalAsientos;
```

Con esa línea ya estamos declarando nuestra variable y le estamos diciendo al sistema que `totalAsientos` tendrá un valor
del tipo `byte`. El sistema entonces nos tomará la palabra y reservará en memoria ese cachito de espacio minúsculo que
requiere un byte. Noten como nuestra línea termina con un punto y coma. Eso forma parte de la sintaxis de Java y lo
veremos más adelante cuando veamos [Expresiones](#expresiones).

Vamos ahora a **asignarle** un valor a nuestra flamante variable. ¿Les suena de algún lado esa palabra "asignar"?
Ciertamente, ya la habíamos visto cuando vimos [Operadores](../clase_01/index.md/#operadores-de-asignacion), así que
usaremos el operador de asignación (`=`) para asignarle un valor:

```java
byte totalAsientos; // --> Aquí la declaramos.

totalAsientos = 125; // --> Aquí le asignamos un valor.
```

Vean como cuando la declaramos, debemos definir su tipo, pero luego cuando queremos asignarle un valor, simplemente
ponemos su identificador seguido del operador de asignación y el valor.

Estas dos líneas de código también se pueden sintetizar en una sola si queremos **declarar** nuestra variable Y
**asignarle** un valor en el mismo momento, simplemente unimos las dos sentencias:

```java
  byte totalAsientos  =  125;
//  ^        ^        ^   ^
// TIPO    NOMBRE     OP  VAL
```

De esta manera estaremos declarando nuestra variable de tipo byte y le asignaremos un valor numérico de 125.

Usando nuestro primer ejemplo con cadenas podemos ver como es que se le cambia el valor a una variable:

```java
      String nombre = "Juan Domingo";
      System.out.println("Nombre inicial: " + nombre);
      // Acá pasan cosas.
      System.out.println("Pasan muchos años y muchas cosas...");
      nombre = "Cristina";
      System.out.println("Nombre luego: " + nombre);
```

### :warning: Atención máxima :eyes:
Ahora bien, ¿qué pasa si un tiempo después nos llaman de la sala de teatro y nos dicen que remodelaron la sala y la
ampliaron, que ahora tiene 300 butacas? Bueno, en principio si nos caían bien nos vamos a poner contentxs, y luego
buscaremos nuestro código e iremos a modificar nuestra variable que tenía el total de asientos para actualizarla con el
nuevo valor. Pareciera tan sencillo como encontrar la línea donde la declaramos y simplemente cambiar el número:

```java
byte totalAsientos  =  300;
```

Prueben declarar esta variable de este modo ^ a ver qué sucede :boom: .
Por más que la diferencia sea muy chiquita :pinching_hand_tone4: para Java ese no es un valor válido.

Cuando decimos que el valor de la variable puede cambiar y el sistema no nos va a reprochar nada, pues las _variables
varían_... debemos prestar mucha atención a un tema ya a esta altura recurrente: **Java es un lenguaje estricto con sus
tipos de datos**.

Ya nos habíamos comprometido con el sistema a guardar valores de tipo byte en nuestra variable `totalAsientos`, y el
sistema ya nos había reservado ese espacio en memoria, pero resulta que `300` ¡no es un valor válido en el tipo `byte`! (1)
{ .annotate }

1.  Rango de valores válidos de byte: [-128 .. 127].

Así que si intentamos cambiar el valor inicial de nuestra variable a 300 lo que sucederá es que el sistema simplemente
no nos va a dejar y nos indicará el error [^1].

[^1]: En situaciones excepcionales no nos va a tirar un error, sino que obtendremos valores totalmente inesperados. Ya
veremos esto en detalle más adelante.

Por eso es importante siempre intentar anticiparse a este tipo de cambios o, dicho de otra forma, no confiarse en que las
especificaciones no cambiarán. Siempre será mejor trabajar con tipos de datos que tengan un buen margen para esos cambios.

En este ejemplo que dimos queda muy evidente que nos estamos "pasando" porque simplemente le asignamos un valor más alto
cuando declaramos la variable, pero imaginen el siguiente ejemplo en donde una variable `totalEntradas` no tiene un valor
definido por nosotrxs 'a mano', sino que hay una serie de operaciones que definen su valor. Por ejemplo:

```java
byte totalEntradas;

// Unas cosas muy interesantes que hace nuestro programa.

byte entradasVendidas = estoVieneDeUnCalculoComplejo;
byte invitaciones = estoVieneDeOtroCalculo;

totalEntradas = entradasVendidas + invitaciones;

```

Si la operación de suma que determina el valor de nuestra variable es un número entero más grande que 127, vamos a estar
en problemas.

Para situaciones muy específicas en donde necesitamos explicitar que una variable no puede cambiar su valor,
es decir, para declarar variables que no varían (¡qué contradicción!) podemos hacer uso de otro elemento. Esos elementos
se llaman "constantes".


## Constantes
Las constantes son un tipo especial de variable. Y su nombre ya nos dice qué es lo que
será diferente en este elemento: su _mutabilidad_. Evidentemente, las constantes son... constantes y no pueden variar su
valor a lo largo del programa.

???+ note "Constantes"
    Las constantes son un contenedor en el que podemos guardar datos o valores.

    - Tienen un identificador :label:
    - Su valor es inalterable durante toda la ejecución del programa :lock:
    - En Java, debemos especificar su _tipo_ :material-shape:

Cualquier dato que no cambie es buen candidato para guardarse en una constante. Ejemplos:

- El número pi (`π`)
- La cantidad de meses que tiene un año
- La velocidad de la luz
- La burguesía Argentina :P

La declaración de las constantes es igual a la de las variables, pero le tenemos que sumar una palabra que las definirá
como constantes: `final`. Veamos unos ejemplos.

``` java
// Declaramos las constantes porque hay cosas que nunca cambian (¿?).
final double NUMERO_PI = 3.1415926535;
final String MEJOR_PAIS = "Argentina";
```

### Identificadores
Para usar los identificadores, que no son más que el 'nombre' que le damos a nuestras variables y constantes, debemos
tener algunas reglas en cuenta.

!!! abstract annotate "Sintaxis de los identificadores"

    - No se pueden utilizar [palabras reservadas](#palabras-reservadas "Dejamos acá abajo el machete.")
    - El identificador debe ser único.
    - Deben comenzar siempre por una letra (1).
    - Los siguientes caractéres pueden ser letras, dígitos, guión bajo (`_`) o el signo de pesos (`$`).
    - Se distingue entre mayúsculas y minúsculas (2).
    - No hay una largo máximo ni mínimo establecido.

1.  La gente de Oracle (la empresa que desarrolló Java) recomienda NO utilizar guiones bajos (`_`) ni signo de
    pesos (`$`) como primer caracter de un identificador aunque estos estén permitidos.
2.  :material-caps-lock: :eyes: Java es sensible a mayúsculas y minúsculas, con lo cual, el identificador `coso`
    será diferente a `Coso` o `COSO` (o cualquier otra variación).


Además de estas reglas de sintaxis hay otro conjunto de cuestiones a tener en cuenta que se suelen denominar "buenas
prácticas" de programación.

Estas son, como su nombre lo indica, una serie de buenos modales a la hora de escribir código, que pueden variar de lenguaje
en lenguaje. No van a hacer que nuestro código falle en sentido estricto, pero seguirlas le facilita (¡mucho!) la lectura
de nuestro código tanto a otras personas como a nosotrxs mismxs.

Hay bastantes estándares de programación que se pueden seguir y, por supuesto, siempre hay competencia entre cuál estándar
es mejor, pero con el tiempo una suele adoptar el que sea más utilizado en el lenguaje o tecnología que desarrolla o
incluso en el ámbito social en el que programamos (grupo de amigxs, trabajo, etc...).

Dentro de las buenas prácticas más extendidas de Java, hay algunas que aplican a los identificadores y las detallamos a
continuación:

!!! success "Buenas prácticas"
    - Usar identificadores que reflejen el **significado** o el **uso** de los elementos. Ejemplos:
        - `unasCosas` :x:
        - `cantidadSillas` :white_check_mark:
    - Usar "[camelCase](https://es.wikipedia.org/wiki/Camel_case)" (es un anglicismo que se podría traducir como "tipoCamello")
      para identificar variables. Ejemplos:
        - `cantidad_sillas` :x:
        - `cantidadsillas` :x:
        - `cantidadSillas` :white_check_mark:
    - Usar mayúsculas para identificar constantes. Ejemplos:
        - `mejor_pais` :x:
        - `MejorPais` :x:
        - `MEJOR_PAIS` :white_check_mark:
    - Se recomienda no usar nombres muy largos ni muy cortos. Los nombres cortos solo se recomiendan para variables
    _temporales_ de corta vida útil.
    - No podremos usar tildes, diéresis ni `ñ` en nuestros identificadores :broken_heart:
        - `añoActual` :x:
        - `canciónFinal` :x:
        - `PINGÜINOS` :x:


## Expresiones
Junto con los operadores, las **expresiones son los elementos básicos con los que armaremos nuestras sentencias**.

Repasemos qué era una sentencia: visualmente las vimos como líneas de código (1) que representan una **acción** que debe ser ejecutada. Los bloques nos permiten agrupar líneas de
código que serán "leídas" como una única sentencia.
{ .annotate }

1.    En Java -y otros lenguajes- terminan con un punto y coma `;`

En términos muy muy generales diremos que **una sentencia NO devuelve nada** y que **una expresión SÍ devuelve alguna cosa**.

Podemos definir una expresión como un fragmento de código que utiliza operadores para manipular valores y ^^producir un
resultado^^.

Lo que en matemática llamamos "hacer una cuenta" sería en programación "crear una expresión". La diferencia principal es
que las expresiones en programación además de valores numéricos (como en las cuentas) podemos también trabajar con palabras,
caractéres y _booleanos_.

???+ note "Expresiones"
    Una expresión es un conjunto de operadores, valores, variables, constantes y funciones que devuelve un resultado.

Veamos un ejemplo básico para determinar qué es una expresión, qué es un operador y qué es una sentencia y poder así
diferenciarlos.

```java

c = a + b;
```

- `a`, `b` y `c`: Son **valores** o datos.
- `=` y `+`: Son **operadores**.
- `a + b`: Es una **expresión**.
- `c = a + b;`: Es una **sentencia**.

## Palabras reservadas

!!! tip "Palabras reservadas en Java"
    |       |       |          |         |            |
    |:-----:|:-----:|:--------:|:-------:|:----------:|
    |`abstract`|`continue`|  `for`   |  `new`  |  `switch`  |
    |`assert`|`default`|  `goto`  |`package`|`synchronize`|
    |`boolean`| `do`  |   `if`   |`private`|   `this`   |
    |`break`|`double`|`implement`|`protected`|  `throw`   |
    |`byte` |`else` | `import` |`public` |  `thows`   |
    |`case` |`enum` |`instanceof`|`return` |`transient` |
    |`catch`|`extends`|  `int`   | `short` |   `try`    |
    |`char` |`final`|`interface`|`static` |   `void`   |
    |`class`|`finally`|  `long`  |`strictfp`| `volatile` |
    |`const`|`float`| `native` | `super` |  `while`   |
