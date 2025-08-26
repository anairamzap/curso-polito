# Clase 02: Variables + Constantes + Expresiones + Java API
En esta clase veremos qué son las variables y constantes, aprenderemos a definirlas y usarlas junto con los
elementos que vimos hasta ahora (nuestros tipos primitivos, cadenas de texto o `String` y operadores). Veremos también a
qué se llama "expresión" y cómo las construimos y, por último, veremos qué es una API y qué son las clases que conforman
la API de Java.

## Variables
Una variable es un contenedor en el que se guarda un valor o dato. Sería algo similar a una caja donde _metemos_ un valor
y a la que le ponemos una etiqueta en el frente.
La etiqueta es el nombre o, técnicamente hablando el **identificador** de la variable, que nos va a permitir acceder a ella
(y así a su valor), manipularla y reutilizarla.

Las variables nos permiten reutilizar valores tantas veces como queramos sin tener que estar repitiendo ese valor cada
vez. El nombre de la variable se convierte entonces en una **representación del valor** que le *_asignamos_* (atención a esta
palabrita).

Por otro lado, y como lo indica su nombre, las variables pueden variar a lo largo de nuestro programa. Una variable
`nombre` puede tener un valor inicial de "Juan Domingo" y luego podemos cambiarle su valor a "Cristina". La modificación
del valor de una variable forma parte de las prestaciones que tiene este elemento ya de base.

???+ note "Variable"
    Una variable es un elemento en el que podemos almacenar datos.

     - Tienen un identificador (o nombre) :label:
     - Su valor puede modificarse a lo largo de la ejecución del programa :fontawesome-solid-arrows-spin:

¿Cómo creamos entonces una variable? Bien sencillo, vamos a escribir el nombre o identificador de nuestra variable, pero
¡OJO! En Java, al ser un lenguaje de tipado estricto, debemos además decirle al sistema qué tipo de dato vamos a querer
guardar ahí. Esto se llama en programación **declaración de variables**. Porque al crearla estamos también declarando su
**tipo** y comprometiéndonos con el sistema a sólo guardar valores que sean admitidos por ese tipo. Veamos:

```java
byte totalAsientos;
```
Con esa línea ya estamos declarando nuestra variable y le estamos diciendo al sistema que `totalAsientos` tendrá un valor
del tipo `byte`. El sistema entonces nos tomará la palabra y reservará en memoria ese cachito de espacio minúsculo que
requiere un byte. Noten como nuestra línea termina con un punto y coma. Eso forma parte de la sintaxis de Java y lo
veremos más adelante cuando veamos Expresiones. 

Vamos ahora a **asignarle** un valor a nuestra flamante variable. ¿Les suena de algún lado esa palabrita "asignar"?
Ciertamente, ya la habíamos visto cuando vimos [Operadores](clase_1.md#operadores-de-asignacion), así que usaremos el 
operador de asignación (`=`) para asignarle un valor:

```java
totalAsientos = 125;
```

Estas dos líneas de código también se pueden sintetizar en una sola si queremos declarar nuestra variable Y asignarle un
valor en el mismo momento, simplemente unimos las dos sentencias:

```java
byte totalAsientos = 125;
```
De esta manera estaremos declarando nuestra variable de tipo byte con un valor numérico de 125.

Ahora bien, ¿qué pasa si cuando estamos desarrollando nuestro programa algo cambia y resulta que el total de asientos
disponibles es, digamos, `300`?

:fontawesome-solid-exclamation-triangle: Cuando decimos que el valor de la variable puede cambiar y el sistema no nos va
a reprochar nada, pues las _variables varían_... debemos prestar mucha atención a un tema ya a esta altura recurrente:
Java es un lenguaje estricto con sus tipos de datos.

Ya nos habíamos comprometido con el sistema a guardar valores de tipo byte en nuestra variable, y el sistema ya nos había
reservado ese espacio en memoria, pero resulta que `300` no es un valor disponible en el tipo `byte`. Así que si intentamos
cambiar el valor inicial de nuestra variable a 300 el sistema simplemente no nos va a dejar y nos indicará el error.

Por eso es importante siempre intentar anticiparse a este tipo de cambios o dicho de otra forma no confiarse en que las
especificaciones no cambiarán y será mejor trabajar con tipos de datos que tengan un buen margen para esos cambios.

Lxs invitamos a que hagan la prueba de modificar su variable de tipo byte a un valor más grande que el admitido, a ver
qué pasa, si total... la diferencia es muy chiquita :pinching_hand_tone4:. Qué tan grave pueden ser unos bits más unos
bits menos :zany_face:



## Constantes
Las constantes son un tipo especial de Variable. Y por su nombre suponemos ya sospechan qué es lo que
será diferente en este elemento: su mutabilidad. Evidentemente las constantes son... constantes y no pueden variar su
valor a lo largo del programa.

???+ note "Constantes"
    Las constantes son un contenedor en el que podemos guardar datos o valores.

    - Tienen un identificador :label:
    - Su valor es inalterable durante toda la ejecución del programa :lock:

Cualquier dato que no cambie es candidato a guardarse en una constante. Ejemplos:

- El número pi (π)
- La cantidad de meses que tiene un año
- La velocidad de la luz

La declaración de las constantes es igual a la de las variables, pero le tenemos que sumar una palabra que las definirá como
constantes: `final`:

``` java
// Declaramos las constantes porque hay cosas que nunca cambian (¿?).
final double NUMERO_PI = 3.1415926535;
final String MEJOR_PAIS = "Argentina";
```

### Identificadores
Para usar los identificadores, que no son más que el 'nombre' que le damos a nuestras variables y constantes, debemos tener
algunas reglas en cuenta.

!!! abstract annotate "Sintaxis de los identificadores"
    
    - No se pueden utilizar palabras reservadas
    - El identificador debe ser único.
    - Deben comenzar siempre por una letra (1).
    - Los siguientes caractéres pueden ser letras, dígitos, guión bajo (`_`) o el signo de pesos (`$`).
    - Se distingue entre mayúsculas y minúsculas. (2)
    - No hay una largo máximo ni mínimo establecido.

1. La gente de Oracle (la empresa que desarrolló Java) recomienda NO utilizar giuones bajos (`_`) ni signo de pesos (`$`)
    como primer caracter de un identificador aunque estos estén permitidos.
2. :material-caps-lock: :eyes: Java es sensible a mayúsculas y minúsculas, con lo cual, el identificador `coso` será
    diferente a `Coso` o `COSO` (o cualquier otra variación).

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
    - En ningún caso podremos usar tildes, diéresis ni `ñ` en nuestros identificadores :broken_heart: 
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

c = a + b
```

- `a`, `b` y `c`: Son **valores** o datos.
- `=` y `+`: Son **operadores**.
- `a + b`: Es una **expresión**.
- `c = a + b`: Es una **sentencia**.

{==[Agregar otros ejemplos fáciles para que detecten en clase qué es cada cosa]==}


### {==Type cast y precedencia ?==}

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


## API de Java
Una API 