# Clase 01: ¿qué es un programa? + fases de desarrollo + estructura y sintaxis

## Breve repaso

En la clase pasada habíamos llegado a una definición para la acción de programar.
Vimos que programar no era exclusivo de la informática, sino una forma de pensar (lógica) para elaborar una serie de
instrucciones (algoritmo) que serán ejecutadas por una máquina o sistema.

???+ question "¿Qué es programar?"
    Programar es una forma de pensar para elaborar una serie de instrucciones que serán ejecutadas por un sistema.

???+ question "¿Qué es un algoritmo?"
    - Un algoritmo es una creación humana.
    - Se lo puede definir como una serie de instrucciones ordenadas o una lista ordenada de pasos para lograr un objetivo.
    - Ejemplos clásicos: Una receta de cocina 📖🥣, un manual para armar un mueble 🗒️, tomarse el colectivo :material-bus-stop-covered:

Vimos también qué era un lenguaje de programación: una forma de escribir esas instrucciones. Y los categorizamos por
algunas de sus posibles características: por su forma de ejecución, por su nivel de rigurosidad en su sintáxis y
semántica,
por sus paradigmas y por su nivel de abstracción.

Vimos también que los lenguajes de programación de "alto nivel" intentan arrimarse al lenguaje humano y, al igual que ese,
tienen una serie de reglas de sintaxis y semántica con las que hay que cumplir para que, al fin de cuentas, la máquina
pueda ejecutar nuestras instrucciones de la manera en que las pensamos.

???+ note "Los lenguajes de programación"
    - Un lenguaje de programación es una forma de escribir instrucciones.
    - Se los suele agrupar por sus características distintivas.
    - Al igual que el lenguaje humano, cada lenguaje tiene reglas **sintácticas** y **semánticas**.

A partir de estas definiciones, ya podemos adentrarnos en dilucidar... ¿qué es entonces un programa?

## Programa

La palabra programa puede hacer referencia a muchas cosas no tan disímiles como aparentan:
Un programa de una materia de la facu, un programa de televisión, un programa político
(quienes tengan cercanía a espacios de discusión política, habrán notado los constantes reclamos de la existencia de
dicha cosa), etc...

Como podrán observar, todas esas acepciones de la palabra "programa" son bastante similares: Es un conjunto ordenado de
tópicos que se deben seguir en el orden establecido y de una forma más o menos constante.

Pues bien, entonces un programa informático no es más que una seguidilla de sentencias que se ejecutan desde el inicio
hasta el final (ya veremos un poco más esto), realizando así las acciones que definimos dentro de ese programa.

???+ question "¿Qué es un programa?"
    Un programa informático es un conjunto de sentencias que se ejecutan desde el inicio hasta el final realizando así las acciones definidas.

## Fases de desarrollo

Esto lo veremos en detalle más adelante cuando veamos ejercicios de *problemas*, pero vale la pena mencionarlo aquí para
tener una idea general de las fases que tiene el desarrollo de un programa.

¿Por qué insistimos tanto en esto de que programar no es exclusivamente escribir código en un lenguaje elegido? La
programación empieza mucho antes de sentarse a escribir: **se arranca siempre pensando un problema**, antes incluso de
pensar en cómo resolverlo. Recuerden que dijimos en la primera clase que programar es pensar en soluciones creativas
para problemas complejos.

Es decir, primero vamos a intentar **descomponer el problema en pasos lógicos** y ordenados, luego vamos a **imaginar y
diseñar soluciones posibles** y, finalmente como último paso, vamos a **traducir esas soluciones a código** en el
lenguaje que hayamos elegido.

???+ abstract "Fases de desarrollo"
    1. Descomponer el problema en pasos lógicos y ordenados
    2. Imaginar y diseñar las soluciones posibles
    3. Traducir las soluciones elegidas a código


## Estructura de un programa

Vamos a ver cómo se ve un programita básico ("[Hola Mundo](https://es.wikipedia.org/wiki/Hola_mundo)"[^1]) para intentar
descomponer su estructura.

```java linenums="1"

/**
 *
 * @author nombre
 */
public class HolaMundo {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO: el código a ejecutar viene acá abajo.
        System.out.print("¡Hola mundo!");
    }
}

```

Descomponemos el programa:

- Vemos que hay **líneas** de texto
- Las líneas parecieran estar agrupadas en "bloques"
- Hay llaves que "engloban" líneas
- Hay paréntesis que "abrazan" palabras
- Hay unas líneas "especiales" que empiezan con símbolos: barras y asteriscos (`/**` `//`)
- La línea que imprime el texto (`System.out.print()`), "ya viene" con el lenguaje. 

[^1]:"Hola, mundo" en informática es un programa que muestra el texto «Hola, mundo» en un dispositivo de visualización,
en la mayoría de los casos la pantalla de un monitor. Este programa suele ser usado como introducción al estudio de un
lenguaje de programación, siendo un primer ejercicio típico considerado fundamental desde el punto de vista didáctico.

### Sentencias y bloques

Las líneas de nuestro programa son... ¡las sentencias! Una sentencia es una representación de la acción que nuestro
programa debe ejecutar.

A la agrupación de líneas de código que conforman una sola sentencia, las llamaremos bloques.

### Llaves y paréntesis
Las llaves son las que construyen la estructura del código, delimitando los bloques. Indican que todo lo que está entre
la llave de apertura (`{`) y la de clausura (`}`) "pertence" a la línea que antecede inmediatamente a la apertura.

En nuestro ejemplo tenemos dos "conjuntos" de llaves:

```java
public class HolaMundo {
    // Hay cosas acá adentro.
    // Y todas pertenecen a esta clase (class) pública (public) llamada HolaMundo.
}
```
y

```java
public static void main(String[] args) {
    // Hay cosas acá adentro.
    // Y todas pertenecen esta función pública y estática (static) llamada main.
}
```

Los paréntesis también cumplen la función de agrupar, pero a diferencia de las llaves no conforman bloques, sino algo
similar a un agrupamiento de palabras o incluso una palabra sola.

Veremos esto más en detalle cuando veamos "Funciones" (que se suele representar: `f(x)`) pero por ahora recordemos que lo
que está dentro de un paréntesis "pertenece" a la *palabra* o expresión que antecede inmediatamente el de apertura `(`.

```java linenums="1" hl_lines="5 14 10 13"

/**
 *
 * @author nombre
 */
public class HolaMundo {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO: el código a ejecutar viene acá abajo.
        System.out.print("¡Hola mundo!");
    }
}

```

### Indentación
El espacio en blanco que vemos antes de las líneas de código es la indentación o el indentado. En la sintaxis de los
lenguajes humanos esto se conoce como sangría. En el caso de Java la indentación no tiene importancia sintáctica ni
semántica, peeeero es importante respetarla porque facilita visualmente la comprensión y la identificación de los bloques.

### Comentarios

Un comentario es una línea de texto que no es ejecutada, es una nota que agrega quien escribe el programa
para hacer aclaraciones sobre ese código. Pueden ser notas sobre la funcionalidad (qué hace), o para facilitar la
comprensión de la solución implementada (cómo lo hace).

Es una buena práctica utilizar los comentarios para "documentar" nuestro código y así facilitar que otras personas
puedan modificarlo (o incluso para nuestro *yo del futuro* :) ).

### Ciclo del programa: Inicio, proceso, final.
Veremos esto en clase cuando "corramos" :person_running_facing_right_tone5: nuestro programa, pero dejamos aquí una
definición muy esquemática de un ciclo. 

Analicemos el ciclo:

- **Inicio**: Punto de entrada (o _entrypoint_ en inglés)
- **Proceso**: Una vez que se cargó en memoria, el código es ejecutado y el sistema operativo gestionará los recursos del
  entorno (asignando recursos, comunicando con dispositivos de entrada y salida, archivos, etc...).
- **Final**: Código de salida.

## Tipos de datos y valores

Los tipos de datos **clasifican datos según sus características específicas**. Los valores son los datos en sí mismos
(y pertenecerán a un tipo u otro).
Entenderemos un poco más el concepto de valor y dato cuando veamos Variables.

Recuerdan que en la primera clase vimos que había lenguajes fuertemente tipados o débilmente tipados, esta
caractéristica de los lenguajes hará que en nuestro programa debamos explicitar (o no) el tipo de dato que vamos a
manipular. Veamos entonces ahora los tipos de datos llamados primitivos o elementales que nos ofrece Java.

### Tipos primitivos

Los "tipos primitivos"[^2], a veces llamados también Tipos Elementales, son los tipos de datos originales de cada lenguaje.
Es decir que cada lenguaje ya nos proporciona esos tipos y así también los define:

1. Qué **tipo de dato** se puede representar (números -enteros o decimales-, caractéres -letras y símbolos-, etc...)
2. Sus **rangos de valores posibles**
3. Y por lo anterior entonces también se define **el espacio que ocuparán en memoria** los datos pertenecientes a cada
tipo

[^2]: En todos los elementos de Java vamos a ver que estos reciben nombres en inglés. Junto a cada tipo vamos a poner su
traducción en castellano para entenderlos, pero cuando los utilicemos siempre tendrá que ser con su nombre inglés.

Recordemos que las máquinas solamente "entienden" datos que llamamos **binarios**, esto quiere decir que sólo pueden
ejecutar unos y ceros. Por lo tanto, para las máquinas todo será una combinación de esos dos valores a los que definimos
como **bits**: Un bit puede tener un valor de 1 o de 0.

Esto lo tenemos que tener claro para entender como se definen los tipos de datos primitivos.

Aprovechemos el primer tipo de datos para profundizar en esto:

#### byte (byte -anglicismo- u octeto)

Es un tipo de dato que representa una estructura de **8 bits**. O sea, es el conjunto de 8 bits:

```
byte = 00000000
```

Este tipo de dato puede almacenar **valores numéricos enteros** que van desde -128 hasta 127 (ambos inclusive).

Ustedes se preguntarán ¿cómo es que eso sucede? bueno, la maquina construye los números alternando `1` y `0` en esa
sucesión de bits.

Por ejemplo, lo que escribimos más arriba: `byte = 00000000` para la máquina representa `0`. O sea, nosotros
escribimos un `0` en el teclado y la máquina lo "traducirá" a ese conjunto de (8) bits. Si nosotros escribimos un 5,
la máquina lo traducirá como `00000101`. Como pueden ver siguen siendo 8 bits, lo que cambian son las posiciones que tienen
un `1` o un `0`.

Todo esto es importante porque les da la dimensión de lo que ocupan en memoria los datos.

Cuando nosotros creamos un dato, la computadora reserva en memoria el tamaño mayor que puede llegar a alcanzar ese dato.
En el ejemplo que estamos usando, un byte, la máquina va a reservar 8 bits (8 lugares para poner unos y ceros).

Entonces es importante que **antes de crear datos pensemos qué valores vamos a querer manejar**.

#### short (entero corto)

Representa un tipo de dato de **16 bits**. O sea, que usará el doble de memoria que nuestro tipo anterior: `00000000 00000000`.

Puede almacenar **valores numéricos enteros desde -32.768 hasta 32.767**. Por supuesto también lo hace combinando `1`s y `0`s
en esas 16 posiciones.

#### int (entero)
Este tipo de dato puede almacenar **valores numéricos enteros** de 32 bits, o sea **4 veces nuestro primer dato `00000000`**
Los valores van desde -2^31^ hasta 2^31^-1. Como pueden ver, el tamaño del número que permite manejar en mucho más
grande.

Podemos trabajar con números un poco superiores a los 2 mill millones -2.147.483.648 y 2.147.483.647.

#### long (entero largo)
Es un tipo de datos de **64 bits** o sea **8 veces nuestro primer tipo de dato**:
 `00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000`
Y puede almacenar **números enteros que van desde -2^63^ hasta 2^63^-1**. Como se puede imaginar es extremadamente grande:
9.223372 × 10^18^

#### float (coma flotante o 'real')
Es un tipo de dato de **32 bits**, como el int, pero permite manejar números com coma flotante. Por ejemplo `16,4` o
`1879223,45`. Estos números son los que usualmente se conocen como "decimales".

Este tipo de dato tiene una precisión simple, esto es algo que veremos más adelante, pero por el momento alcanza con
saber que no debe ser utilizado si vamos a necesitar números con alta precisión (es decir, lo podemos usar para
aplicaciones gráficas o videojuegos, pero no para información científica o financiera).

#### double (coma flotante doble o 'real largo') 
En este caso es un tipo de dato de **64 bits**, como el long, pero permite manejar números con coma flotante, como el float.

Las diferencias entre el float y double son:
- El rango numérico (es el doble) 
- La precisión (es, también, el doble)
  Al ser un número decimal su "exactitud" depende de la cantidad de dígitos que puede manejar después de la coma. Por eso,
  el tipo de dato "double" tiene el doble de precisión que el "float".

#### boolean (booleano -anglicismo- o lógico)
Este es un tipo de dato de **un bit** que representa verdadero (en inglés "true") o falso (en inglés "false")
(que también podría ser sí o no, 1 o 0, lleno o vacío, etc...).

Se los llama así porque está basado en el álgebra "booleana", del filósofo y matemático inglés
[George Boole](https://es.wikipedia.org/wiki/George_Boole). 

#### char (carácter o símbolo)
Es un tipo de dato que representa un carácter [Unicode](https://www.rapidtables.org/code/text/unicode-characters.html)
de **16 bits**. Se utiliza mucho el tipo de dato char para manejar un símbolo o una letra (¡que es en última instancia un
símbolo!) y no un fragmento de texto.

#### String (cadena de texto)
Este tipo de dato lo ponemos como primitivo ¡pero no lo es! Lo incluimos aquí porque es tan utilizado como los primitivos.

En principio hay que observar que empieza con una mayúscula. En casi todos los lenguajes de programación orientada a
objetos esto tiene un significado importante. Por ahora podemos decir que cuando tenemos que trabajar con textos (frases
o palabras), usamos este tipo de dato.

---
### Tipos primitivos - Tabla
??? tip "Tipos primitivos de JAVA"
    |Tipo   |Traducción          |Memoria utilizada             |Rango de valores                   |Breve descripción                                                                                                                                                                                                |
    |:-----:|:------------------:|:----------------------------:|:---------------------------------:|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | byte  |Byte u Octeto (raro)|       1 byte (8 bits)        |           de -128 a 127           |Representación de un número entero positivo o negativo.                                                                                                                                                          |
    | short |    Entero corto    |       2 byte (16 bits)       |        de -32.768 a 32.767        |Representación de un entero positivo o negativo con rango corto.                                                                                                                                                 |
    |  int  |       Entero       |       4 byte (32 bits)       |        de -2^31^ a 2^31^-1        |Representación de un entero estándar.                                                                                                                                                                            |
    | long  |    Entero largo    |       8 byte (64 bits)       |        de -2^63^ a 2^63^-1        |Representación de un entero de rango ampliado.                                                                                                                                                                   |
    | float |Coma flotante o Real|       4 byte (32 bits)       |        de -10^32^ a 10^32^        |Representación de un número real estándar. La precisión del dato contenido varía en función del tamaño del número: la precisión se amplia con números más próximos a 0 y disminuye cuanto más se aleja del mismo.|
    |double |     Real largo     |       8 byte (64 bits)       |       de -10^300^ a 10^300^       |Representación de un número real con mucha precisión.                                                                                                                                                            |
    | char  |      Carácter      |       2 byte (16 bits)       |      de '\u0000' a '\uffff'       |Carácter o símbolo. Recordar que para utilizar una "cadena de texto" se debe usar la clase String.                                                                                                               |
    |boolean| Booleano o Lógico  |            1 bit             |           true - false            |Representa una 'posición' lógica con dos valores posibles: verdadero (true) o falso (false)                                                                                                                      |


## Operadores
Los operadores son símbolos o palabras que utilizamos para manipular y combinar expresiones.
Son elemento que nos permiten realizar, como su nombre lo indica, operaciones como:

- Comparaciones
- Procedimientos lógicos
- Cálculos aritméticos
- Asignaciones

### Operadores relacionales
Utilizamos los operadores relacionales cuando necesitamos comparar dos elementos o valores.

Dependiendo el operador que usemos tendremos que tener en cuenta, o no, la posición de los elementos con relación al
operador.

| **OPERADOR** | **DESCRIPCIÓN**   | **EJEMPLO** |
|:------------:|:-----------------:|:-----------:|
| `==`         | Es igual          | a == b      |
| `!=`         | Es distinto       | a != b      |
| `<`          | Menor que         | a < b       |
| `>`          | Mayor que         | a > b       |
| `<=`         | Menor o igual que | a <= b      |
| `>=`         | Mayor o igual que | a >= b      |

Es decir, decir que `a == b` es lo mismo que decir que `b == a`, sin embargo, no sería lo mismo intercambiar los operandos
cuando hacemos una comparación o relación mayor/menor: `a < b` no es lo mismo que `b < a`.

### Operadores lógicos
A diferencia de los relacionales que **comparan** elementos o valores, los operadores lógicos **combinan** operaciones
_booleanas_.

Son muy utilizados en estructuras condicionadles y _loops_, que veremos más adelante, para combinar condiciones y obtener
luego un resultado.

| **OPERADOR** | **DESCRIPCIÓN**  | **EJEMPLO**                       | **EJEMPLO COTIDIANO**                   |
|:------------:|:----------------:|-----------------------------------|-----------------------------------------|
| `&&`         | Y (de adición)   | si [condición] Y [otra condición] | Agarro la campera si hace frío Y llueve |
| `||`         | O (de exclusión) | si [condición] U [otra condición] | Agarro la campera si hace frío O llueve |
| `!`          | NO (de negación) | si NO [condición]                 | Dejo la campera si NO hace frío         |

Cuando usamos los operadores `&&` si nuestra primera condición devuelve _falso_ o usando el comparador `||` sin nuestra primera
condición devuelve _verdadero_ , en ambos casos la segunda condición no se evaluará.

Los operadores de negación simplemente invierten un valor lógico.

### Operadores aritméticos
Los operadores aritméticos se utilizan para realizar operaciones matemáticas básicas.

| **OPERADOR** | **DESCRIPCIÓN** |
|:------------:|:---------------:|
| `+`          | Adición         |
| `-`          | Resta           |
| `*`          | Multiplicación  |
| `/`          | División        |
| `%`          | Módulo          |

### Operadores de asignación
Los operadores de asignación se utilizan para asignar valores a las variables.

| **OPERADOR** | **DESCRIPCIÓN**     |
|:------------:|:-------------------:|
| `=`          | Asignación simple   |
| `+=`         | Añadir y asignar    |
| `-=`         | `Restar y asignar   |
| `*=`         | Multiplica y asigna |
| `/=`         | Divide y asigna     |
| `%=`         | Módulo y asignar    |
