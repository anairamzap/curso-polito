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
Un programa informático es un conjunto de sentencias que se ejecutan desde el inicio hasta el final realizando así
las acciones definidas.

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

```java

/**
 *
 * @author nombre
 */
public class HolaMundo {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO: el código a ejecutar viene acá abajo
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
- La línea que imprime el texto, usa algo que "ya viene" con el lenguaje (`System.out.print()`)

[^1]:"Hola, mundo" en informática es un programa que muestra el texto «Hola, mundo» en un dispositivo de visualización,
en la mayoría de los casos la pantalla de un monitor. Este programa suele ser usado como introducción al estudio de un
lenguaje de programación, siendo un primer ejercicio típico considerado fundamental desde el punto de vista didáctico.

++ctrl+z++

### Sentencias y bloques

Las líneas de nuestro programa son... ¡las sentencias! Una sentencia es una representación de la acción que nuestro
programa debe ejecutar.

A la agrupación de líneas de código que conforman una sola sentencia, las llamaremos bloques.

### Indentación
El espacio en blanco que vemos antes de las líneas de código es la indentación o el indentado. En la sintaxis de los
lenguajes humanos esto se conoce como sangría. 

### Comentarios

Un comentario es una línea de texto que no es ejecutada, es algo así como una nota que agrega quien escribe el programa
para hacer aclaraciones acerca de ese código. Pueden ser notas sobre la funcionalidad (qué hace), y también para
facilitar la comprensión de la solución implementada (cómo lo hace). Es una buena práctica utilizar los comentarios para
"documentar" nuestro código y así facilitar que otras personas puedan modificarlo (o incluso para nuestro yo del
futuro :) ).

### Ciclo del programa: Inicio, proceso, final.

Analicemos el ciclo:

- Inicio: Punto de entrada
- Proceso: El código es ejecutado (una vez que se cargó en memoria) y el sistema operativo gestiona los recursos del
  entorno (asigna recursos, comunica con dispositivos I/O, archivos, etc).
- Final: Códigos de salida

## Tipos de datos y valores

Los tipos de datos clasifican datos según sus características específicas. Por otro lado, los valores son los datos
dentro de cada tipo.

Recuerdan que en la primera clase vimos que había lenguajes fuertemente tipados o débilmente tipados, esta
caractéristica de los lenguajes hará que en nuestro programa debamos explicitar (o no) el tipo de dato que vamos a
manipular.

### Tipos primitivos

[Abe:: Copié esto del doc de la clase, pero modificalo, agregá, borrá]

Los “tipos primitivos” no son unos ñatos que conviven con dinosaurios y viven en cuevas, sino... los tipos de datos que
ya vienen definidos por el lenguaje.
Estos ocuparán un espacio definido en memoria que debemos saber para utilizar cada “tipo” adecuadamente.
Recordemos que las maquinas solo interpretan datos binarios, esto quiere decir que solo entiende el 1 y el 0
Por lo tanto para las maquinas todo es una convinación de esos dos valores a los que definimos como bit: Un bit tiene el
valor 1 o 0.
Tengamos en claro eso como base para entender como se definien los tipos de datos primitivos.
Aprovechemos el primer tipo de datos para profundizar en esto:
1. **byte**  
Es un tipo de dato que representa una estructura de 8 bits. O sea es el conjunto de 8 bits: 
byte = 00000000 <br>
Este tipo de datos puede almacenar los valores númericos enteros que van desde -128 al 127 (ambos inclusive) <br>
Ustedes se preguntarán ¿Como es que eso sucede? Bueno la maquina construye los números alternando 1 y 0 en esa
sucesion de bits.<br>
Por ejemplo lo que escribimos más arriba: **byte = 00000000** representa un 0 para la maquina, o sea nosotros ecribimos un 0 en el teclado y la maquina lo traduce a ese conjunto
de bits. Si nosotros escribimos un 5 la maquina lo traduce como **00000101**. Como pueden ver siguen siendo 8 bits lo que cambia es
que posiciones tienen un 1 o un 0.<br>
Todo esto es importante porque les da la dimensión de lo que se ocupa en la memoria al crear datos.
Cuando nosotros creamos un dato la computadora reserva en memoria el tamaño mayor que puede alcanzar ese dato.
En el ejemplo que estamos usando, un byte, la maquina va a reservar 8 bits (8 lugares para poner 1 y 0).<br>
Entonces es importante que antes de crear datos pensemos qué valores vamos a manejar
2. **short** <br>
Representa un tipo de dato de 16 bits. El doble en el uso de la memoria, o sea: **00000000 00000000** <br>
Puede almacenar valores númericos enteros de -32.768 a 32.767. Por supuesto también lo hace convinando 1 y 0 en esas 16 posiciones
3. **int** <br> Este tipo de datos puede amacenar valores númericos enteros de 32 bits, o sea **4 veces nuestro primer dato 00000000**
Los valoes van desde -2³¹ al 2³¹-1. Como pueden ver ya el tamaño del número que permite manejar en mucho más grande.<br>
Podemos trabajar con números un poco superiores a los 2 mill millones -2.147.483.648 y 2.147.483.647.
4. **long** <br> Es un tipo de datos de 64 bits o sea 8 veces nuestro primer tipo de dato: <br>
00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000<br>
Y puede almacenar números enteros que van desde -2⁶³ al 2⁶³-1. Como se puede imaginar es extremadamente grande:
9.223372 × 10¹⁸ 
5. **float** <br> Es un tipo de dato de 32 bits, como el int, solo que permite manejar números com coma flotante.
Por ejemplo 16,4 o 1879223,45
6. **double** <br> En este caso es un tipo de dato de 64 bits, como el long, y también premite manejar números con coma
flotante.<br>
La direfencia entre el float y double es, obviamente que maneja un número mucho mñas grande, pero principalmente es 
la precisión del número. Al ser un número decimal su exactitud depende de la cantidad de dígitos maneja después de la coma.
El tipo de dato double tiene el doble de precisión en ese sentido.
7. **boolean** <br> Este es un tipo de dato de un bit que representa verdadero o falso.
8. **char** <br> Es un tipo de dato que representa un carácter Unicode ("https://www.rapidtables.org/code/text/unicode-characters.html")
de 16 bits. Se utiliza mucho el tipo de dato char para manejar un a letra y no un pedazo de texto.
9. **String** <br> Este tipo de datos lo ponemos como primitivo, pero no lo es.
En principio hay que observar que empieza con una mayúscula. En casi todos los lenguajes de
programación orientada a objetos esto tiene un significado importante. Por ahora podemos decir que
cuando tenemos que trabajar con textos, usamos este tipo de datos.

## Operadores

[Yo sigo acá mañana]
