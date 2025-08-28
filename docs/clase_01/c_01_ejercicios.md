---
icon: material/pencil
---
# Ejercicios para la clase 01
En esta clase vimos cómo crear nuestro primer programa (HolaMundo) y como hacer para que nos imprima algo en la consola
del IDE.

Primeros pasos para estos ejercicios:
1. Abrir la IDE (Netbeans)
2. Crear un nuevo programa (o abrir uno existente)
3. 

## Ejercicio 1 :wave_tone4:
Usando las herramientas del sistema (`System.out.print`), impriman un texto en la consola de Netbeans.

Y ahora jueguen usando los operadores. Por ejemplo, podemos sumar dos cadenas de texto.

``` java
System.out.print("Hola," + " " + "¿qué tal?");
```
Podemos también sumar o "juntar" caracteres:

``` java
// No me acuerdo ni uno, pero https://www.unicode.org/charts/script/chart_Symbol-Other.html
System.out.println("H" + '\u2665' + "l" + "u");

System.out.println("Venceremos " + '\u270C');

System.out.println("Extraño la " + '\u00F1');
```


## Ejercicio 2
Utilicen el otro método para imprimir mensajes, para que agregue un salto de línea cuando termina el texto
(`System.out.println`).

Esto nos va a venir bien para que no nos quede todos los mensajes ahí amontonados en una sóla línea :)

¿Qué otro operador se puede usar con cadenas de texto? ¿Podremos dividir, restar o multiplicar?

Hagan la prueba, cuando Java no sepa qué hacer con el operador y la cadena, se los va a decir en forma de error cuando
compilen.

### Sugerencias:

- Prueben usando operadores relacionales.

## Ejercicio 3
Usando este último método, prueben imprimir mensajes de texto y prueben también si pueden hacer cuentas y comparar valores.

**Recuerden que si queremos imprimir texto usamos las comillas envolviendo el texto**, pero los números y operadores
deben ir por fuera de las comillas.

Ponemos acá ejemplos para que se guíen, pero ¡no los copien tal cual! Inventen cualquiera cosa, sin miedo, que la mejor
manera de aprender es insistir en el error, tratar de entenderlo y después arreglarlo para llegar al resultado esperado :)

Unos ejemplos básicos para arrancar:

``` java
// Multiplicamos y comparamos.
System.out.println(2*3 == 6);

System.out.println(2*3 == 2 + 2 + 2);

// Comparamos dos cadenas. 
System.out.println("peras" == "manzanas");

// Atenti al uso de los paréntesis.
System.out.println("¿las peras NO son manzanas? " + ("peras" != "manzanas"));
```

``` java
// Multiplicamos.
System.out.println(2*3);
```

Prueben ahora agregarle una cadena de texto (string):

```java
   // Agregamos texto a la cuenta.
   System.out.print("Se sabe que 2 x 3 es: " +    2*3);
//         ^                    ^            ^     ^
//Método pa' imprimir    Cadena de texto     OP   Cuentita
```

Bueno, parece que todo marcha bien, probemos qué pasa si en lugar de multiplicar sumamos...

```java
// Agregamos texto a la cuenta.
System.out.print("Todo el mundo sabe que habrá un 5: " + 2 + 3);
```

:interrobang: ¡¿Qué pasoooó?! :thinking: 

Les dejamos este interrogante para que traten de entender por qué no sumó, sino que "juntó" los números.

### 🕵🏽‍♀️ Pistas:

- Cuando multiplicamos, todo salió como esperamos. ¿Cuál puede ser la diferencia?
- ¿Se acuerdan de matemática y las precedencias (o el "orden de evaluación")? Algo muy parecido está pasando acá.



---
Un pequeño adelanto: Esta herramienta que usamos se descomopone en:

- `System` --> Es una clase (`class`) de la librería Java. De allí su nombre "sistema".
- `out` --> Es un attributo (o campo) de la clase. Esta palabra es "salida" en español. Bastante clarito su nombre :)
- `print` y `println` son dos métodos de la clase. _Print_ es "imprimir" y _println_ probablemente sea la contracción de
"imprimir línea". Es decir que termina la línea escribiendo una línea nueva (lo que nosotrxs hacemos cuando apretamos
la tecla enter). 