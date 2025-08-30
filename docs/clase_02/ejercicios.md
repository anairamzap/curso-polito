---
icon: material/pencil
---

# Ejercicios para la clase 02
En esta clase vimos variables, constantes y expresiones.

Primeros pasos para estos ejercicios:

1. Abrir la IDE (Netbeans)
2. Crear un nuevo programa (o abrir uno existente)
     1. Si estás creando uno nuevo, acordate de seleccionar la opción "Java with Ant".

## Ejercicio 01: Suma de enteros
Declará dos variables enteras `a` y `b`, asignales valores y mostrá por consola la suma de ambas.

## Ejercicio 02: Área de un rectángulo
Usá dos variables base y altura (tipo double) y calculá el área (fórmula: `base * altura`). Mostrá el resultado.

## Ejercicio 03: Promedio de tres números
Imaginemos que tenemos que sacar el promedio de una materia que tuvo 3 exámenes.

1. Guardá cada nota en una variable de tipo entera 
2. Calculá el promedio
3. Mostralo con decimales

## Ejercicio 04: Intercambio de valores
Tenés dos variables: `x = 5` e `y = 10`. Intercambiá los valores y mostrá el resultado.

## Ejercicio 05: Conversión de temperatura
Imaginemos que tenemos un tío paquete que vive en Canadá y cada vez que hablamos por teléfono nos pregunta cómo está el
clima en Buenos Aires. Hagamos un programita que nos ayude a convertir los grados de Celcius a Farenheit:

1. Declará una variable para la temperatura actual en grados Celcius
2. Usá la fórmula `F = (C * 9/5) + 32`
3. Mostrá la temperatura en grados Fahrenheit

## Ejercicio 06: Cálculo de sueldo
Guardá en variables el sueldo base y un bono extra. Calculá el sueldo total y mostralo. (Pensá si los sueldos y el bono
son valores enteros o reales)

---
## `java.util.Scanner`
## Ejercicio 07: Edad en meses y días
Pedí que se ingrese por teclado un valor y guardala en una variable edadAnios, calculá la edad en meses y en días (
aproximando con 365 días al año). Mostrá ambos resultados.

## Ejercicio 08: Concatenación de cadenas
Pedir que se ingrese por teclado nombre y apellido. Mostrá un mensaje que diga "Hola, Nombre Apellido".

## Ejercicio 09: Número par o impar
Ingresar el valor de una variable entera numero, mostrá en consola si es par o impar.

## Ejercicio 10: Hipotenusa (Teorema de Pitágoras)

1. Ingresar los valores de dos variables catetoA y catetoB (`double`),
2. calculá la hipotenusa con la fórmula: $`h = \sqrt{a^2 + b^2}`$
3. y mostrá el resultado

## Ejercicio 11: Área de un círculo
Pedir que se ingrese el valor del radio `r`, calculá el área con la fórmula: $`A = \pi \times r^2`$

## Ejercicio 12: Perímetro de un cuadrado
Ingresar el valor del valor del lado (`l`), calculá el perímetro con la fórmula: $`4 \times l`$.

## Ejercicio 13: Velocidad promedio
Tenés una distancia (`distanciaKm`) y un tiempo (`horas`). Calculá la velocidad promedio en km/h.

## Ejercicio 14: Minutos a horas y minutos
Tenés un número entero de minutos. Convertilo a horas y minutos. Ejemplo: 130 minutos → 2 horas y 10 minutos.

## Ejercicio 15: Dígito de las unidades
Ingresar por teclado el valor de un número entero `num`, obtené el dígito de las unidades con `num` `%` 10.

## Ejercicio 16: División entera y resto
Pedir el valor de dos variables enteras a y b, mostrá el cociente entero y el resto.

## Ejercicio 17: Potencia
Pedir el valor de dos variables enteras base y exponente, calculá la potencia

## Ejercicio 18: Kilogramos a libras
Convertí un peso en kilogramos (kg) a libras usando la fórmula: $`libras = kg \times 2.20462`$.

## Ejercicio 19: Promedio de notas con decimales
Pedir el ingreso de 4 notas. Calculá el promedio y mostrálo con 2 decimales

## Ejercicio 20: Doble y triple de un número
Pedir que se ingrese el valor de un número entero, calculá y mostrá el doble y el triple.

## Ejercicio 21: Área y perímetro de un triángulo equilátero
Sabiendo el valor de una lado `a`

1. Calculá el perímetro con la fórmula: $`P = a \times 3`$
2. Calculá el area. Con la fórmula: $`A = a^2 \times \frac{\sqrt{3}}{4}`$

## Ejercicio 22: Conversión de metros a cm y mm
Pedir que se ingrese el valor de una longitud en metros (double), convertila a centímetros y milímetros.

## Ejercicio 23: Promedio de velocidad en metros por segundo
Convertí una velocidad en km/h (`vKmH`) a m/s (`vMs`) $`vMs = vKmH \times 1000 \div 3600`$.

## Ejercicio 24: Descuento en un producto
Pedir que se ingresen los valores de un precio y un porcentaje de descuento, calculá el precio final.

## Ejercicio 25: Tiempo de viaje
Pedir que se ingrese el valor de una distancia en km y una velocidad en km/h, calculá el tiempo de viaje en horas.

## Ejercicio 26: Concatenación de edad
Dado nombre y edad, mostrá el mensaje "Me llamo <nombre> y tengo <edad> años."

## {==Ejercicio 27: Interés simple==}
Calculá el interés simple con la fórmula: I = capital * tasa * tiempo.

## {==Ejercicio 28: Interés compuesto==}
Calculá el monto final con la fórmula: M = capital * (1 + tasa)^tiempo.

## {==Ejercicio 29: Conversión de dólares a pesos==}
Pedir que se ingrese un monto en dólares y un tipo de cambio, calculá el equivalente en pesos.

## Ejercicio 30: Conversión de segundos a horas:minutos:segundos
Pedir que se ingrese el valor de un entero segundosTotales, convertilo a formato `hh:mm:ss`.

## {==Ejercicio 31: Promedio ponderado==}
Tenés tres notas: n1, n2, n3 con pesos 0.2, 0.3 y 0.5 respectivamente. Calculá el promedio ponderado.

## {--Ejercicio 32: Calcular IMC (Índice de Masa Corporal)--}
Pedir que se ingresen los valores del peso en kg y la altura en metros, calculá el IMC con la fórmula:
IMC = peso / (altura * altura).

## Ejercicio 33: Promedio de edad de un grupo
Pedir el ingreso de la edad de 4 personas en variables y calculá el promedio.

## Ejercicio 34: Separar decenas y unidades
Pedir que se ingrese el valor de un número de dos cifras, obtené la decena y la unidad.
Por ejemplo, si el número entero es 23 la decena es el 2 y la unidad es el 3.