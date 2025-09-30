---
icon: material/code-braces
---

# Estructuras de control de flujo
Cuando programamos, nuestro programa sigue un camino predeterminado: a eso lo llamamos **control de flujo**.

En condiciones normales, este flujo es **secuencial**, es decir, el programa empieza en la primera instrucción y
continúa en el mismo orden en el que escribimos las sentencias en la IDE.
Veamos un ejemplo:

```java
String miNombre = "Juan";
String miApellido = "Fernandez";

System.out.println("Hola ¿cómo estás? " + miNombre + " " + miApellido);
```

Y ejecutamos vemos por consola:

`Hola ¿como estas? Juan Fernandez`

Si cambiamos el orden:

```java
String miApellido = "Fernandez";
String miNombre = "Juan";

System.out.println("Hola ¿cómo estás? " + miNombre + " " + miApellido);
```

La salida por consola será:

`Hola ¿como estas? Fernandez Juan`

👉 Como se ve, el flujo del programa fue **sentencia a sentencia, una después de la otra**, sin que nosotros 
lo controlemos de manera especial.

En clases anteriores usamos la clase **Scanner** para leer datos del usuario. Por ejemplo:

```java
Scanner ingreso = new Scanner(System.in);

System.out.println("Ingrese su nombre: ");
String miNombre = ingreso.next();
System.out.println("Hola ¿cómo estás? " + miNombre);
```

Cuando lo ejecutamos, la consola muestra:

***Ingrese su nombre:***

El programa se detiene y espera que el usuario escriba un valor y presione Enter.

Cuando lo hacíamos y apretábamos enter


El flujo continúa:

Ingrese su nombre:

Juan

Hola ¿cómo estás? Juan


Esto nos enseña que un programa no siempre avanza de manera automática: a veces depende de datos externos o 
de condiciones.


Por lo tanto, ya podemos deducir que un programa no siempre sigue un único camino. A veces necesita 
**tomar decisiones** o **esperar una intervención externa**.

Las **estructuras de control** son justamente las que permiten al programa **elegir qué camino tomar**.


## Estructuras condicionales
Tomemos un ejemplo de la vida real:

Si está lloviendo, salgo con paraguas;
si no, salgo sin paraguas.

En programación, esto se traduce en una estructura if – else.

Lo podemos representar en pseudocódigo o de manera casi coloquial

```
Si (llueve) entonces

    salgo con paraguas

Sino

	salgo sin paraguas.
```

Si analizamos lo que escribimos arriba tenemos 

1. →  “Si” Es la declaración inicial de la condición.
2. →  (llueve) Esto es la condición que va a evaluar.
3. → “entonces” Sería qué hacer si está lloviendo.
4. → “salgo con paraguas” La acción que hará el programa si efectivamente está lloviendo.
5. → “Sino” Declaración si la evaluación no se cumple.
6. → “salgo sin paraguas.” Acción que hará el programa si no está lloviendo.

Es importante entender que la sentencia inicial

***→ Si (llueve) entonces*** 

evalúa si la condición que está entre paréntesis se cumple, para nosotros: si es verdadera.

Hagamos un ejemplo en nuestro código

```java
boolean llueve = true;
        
if (llueve) {
    System.out.println("Salgo con paraguas");
} else {
    System.out.println("Salgo sin paraguas");
}
```

Cuando lo ejecutamos nos va a mostrar por consola:

***→ Salgo con paraguas***

Si cambiamos el valor de llueve a false

```java
boolean llueve = false;
        
if (llueve) {
    System.out.println("Salgo con paraguas");
} else {
    System.out.println("Salgo sin paraguas");
}
```

Al ejecutar el programa vemos por consola:

***→ Salgo sin paraguas***


👉 Acá conviene entender bien el concepto de que evalúa que se cumpla la condición.

**¿Qué significa “se cumple la condición”?**

Cuando hablamos de que una condición se cumple, queremos decir que la **expresión dentro de los paréntesis 
del if se evalúa como true**.

Si es true, se ejecuta el bloque del if.

Si es false, se ejecuta el bloque del else (si lo hubiera).


## Operador de negación !

Podemos usar el operador **! (NOT)** para negar una condición.

Ilustremos con un ejemplo:

```java
boolean estado = true;

if (!estado) {
    System.out.println("Salgo con paraguas");
} else {
    System.out.println("Salgo sin paraguas");
}
```

En este caso, estado es true, pero !estado significa “NO verdadero”, es decir, false.

Por lo tanto, el programa muestra:

***Salgo sin paraguas***

Ahora cambiemos estado al valor = false


```java
boolean estado = false;
        
if (!estado) {
    System.out.println("Salgo con paraguas");
} else {
    System.out.println("Salgo sin paraguas");
}
```

En este ejemplo **estado** ya viene con valor falso, por lo tanto como nosotros estamos evaluando que NO sea verdadero, 
el programa va evaluar que se cumple la condición y va a mostrar el primer mensaje

***→ Salgo con paraguas.*** 

Tenemos que acostumbrarnos que cuando se habla de que se cumple la condición nos referimos a que es verdadera. 
O sea que la condición que evaluamos es verdadera, más allá del valor que tiene desde antes los elementos que se 
evalúan.

### Para recordar

1. Una condición es una expresión que se evalúa como true o false.
2. El if ejecuta el bloque de código solo si la condición es verdadera.
3. El else se ejecuta cuando la condición es falsa.
4. El operador `!` invierte el valor de la condición.
