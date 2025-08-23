# Clase 01: ¿qué es un programa? + fases de desarrollo + estructura y sintaxis

## Breve repaso
En la clase pasada habíamos intentado encontrar una definición para la acción de programar.
Vimos que programar no era exclusivo de la informática, sino una forma de pensar (lógica) para elaborar una serie de
instrucciones (algoritmo) que serán ejecutadas por una máquina o sistema.

???+ question "¿Qué es programar?"
    Programar es una forma de pensar para elaborar una serie de instrucciones que serán ejecutadas por un sistema.

Vimos también qué era un lenguaje de programación: una forma de escribir esas instrucciones. Y los categorizamos por
algunas de sus posibles características: por su forma de ejecución, por su nivel de rigurosidad en su sintáxis y semántica,
por sus paradigmas y por su nivel de abstracción.

Vimos también que los lenguajes de programación de "alto nivel" intentan arrimarse al lenguaje humano y al igual que ese
tienen una serie de reglas de sintaxis y semántica con las que hay que cumplir para que, al fin de cuentas, la máquina
pueda ejecutar nuestras instrucciones de la manera en que las pensamos.

???+ note "Los lenguajes de programación"
    - Un lenguaje de programación es una forma de escribir instrucciones.
    - Se los suele agrupar por sus características distintivas.
    - Al igual que el lenguaje humano, cada lenguaje tiene reglas **sintácticas** y **semánticas**.

A partir de estas definiciones, ya podemos adentrarnos en dilucidar... ¿qué corno es entonces un programa?

## Programa

La palabra programa puede hacer referencia a muchas cosas no tan disímiles como aparentan:
Un programa de una materia de la facu, una programa de televisión (¿sigue existiendo ese antro?), un programa político
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

Esto lo veremos en detalle más adelante cuando veamos problemas, pero vale la pena mencionarlo aquí para tener una idea
general de las fases que tiene el desarrollo de un programa.

¿Por qué insistimos tanto en esto de que programar no es exclusivamente escribir código en un lenguaje elegido? La
programación empieza mucho antes de sentarse a escribir: **se arranca siempre pensando un problema**, antes incluso de
pensar en cómo resolverlo. Recuerdan que dijimos en la primera clase que programar es pensar en soluciones creativas
para problemas complejos.

Es decir, primero vamos a intentar **descomponer el problema en pasos lógicos**, luego vamos a **imaginar y diseñar soluciones
posibles** y, finalmente como último paso, vamos a **traducir las soluciones a código** en el lenguaje que hayamos elegido.

## Estructura de un programa

Vamos a ver cómo se ve un programita básico ("[Hola Mundo](https://es.wikipedia.org/wiki/Hola_mundo)"[^1]) para intentar
descomponer su estructura.

```java
package HolaMundo;

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
- Las líneas parecieran estar agrupadas en “bloques”
- Hay unas líneas "especiales" que empiezan con símbolos: barras y asteriscos (`/**` `//`) 
- Para imprimir un texto, el lenguaje "ya viene" con una función definida para tal fin (`System.out.print()`)


[^1]:"Hola, mundo" en informática es un programa que muestra el texto «Hola, mundo» en un dispositivo de visualización,
en la mayoría de los casos la pantalla de un monitor. Este programa suele ser usado como introducción al estudio de un
lenguaje de programación, siendo un primer ejercicio típico considerado fundamental desde el punto de vista didáctico.


++ctrl+z++

### Sentencias y bloques

Las líneas de nuestro programa son... ¡las sentencias! Estas vienen a ser la representación de las acciones que nuestro
programa debe ejecutar.

A la agrupación de líneas de código que conforman una sola sentencia, las llamaremos bloques.
Indentación

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

1. int
2. short
3. long
4. double
5. float
6. boolean
7. byte
8. char

## Operadores
[Yo sigo acá mañana]