---
icon: material/pencil
---

# Ejercicios iniciales
En esta clase vimos estructuras de control **condicionales**. Y aprendimos a escribir
[expresiones](../clase_02/index.md/#expresiones) con las siguientes estructuras

**Condición simple** (`if`)
```java
if (cond) {
    // Pasará algo si la condición (cond) se cumple.
}
```
**Condición compuesta** (`if` y `else`)

```java
if (cond) {
    // Pasará algo si la condición (cond) se cumple.
} else {
   // Pasará otra cosa si la condición NO se cumple.
}
```
**Condición múltiple** (`if`, `else if` y `else`)

```java
if (cond) {
    // Pasará algo si la condición (cond) se cumple.
} else if (cond2) {
   // Pasará algo si la otra condición (cond2) se cumple.
} else {
   // Pasará otra cosa si ninguna de las condiciones anteriores se cumple.
}
```
## Ejercicios con condicionales y clase Scanner

### Mayoría de edad
Pedir al usuario su edad e indicar si es mayor de edad (18 o más) o menor de edad.

### Número positivo o negativo
Leer un número entero y mostrar un mensaje indicando si es positivo, negativo o cero.

### Par o impar.
Pedir el ingreso de un número entero y mostrar un mensaje indicando si el número es par o impar.

### Descuento en tienda
Pedir que se ingrese el precio de un producto y mostrar un mensaje con el descuento que se aplicará y el precio
final.

- Si el precio es mayor a 1000, se aplicará un 10% de descuento.
- Si no, no se aplica descuento.

### Nota de examen
Pedir que se ingrese una nota (números enteros del 0 al 10) y mostrar un mensaje que indique si se aprobó o no.

- Si la nota es 7 o más → Aprobado.
- Si la nota es menor → Desaprobado.

### Comparar dos números
Ingresar dos números enteros y mostrar cuál es el mayor. Si son iguales, mostrar un mensaje especial.

### (simular) acceso a una página web
1. Declarar dos variables de tipo String para `usuario` y `clave` y asignarles un valor.
2. Pedir que se ingresen los datos para "usuario" y "clave"
3. Si los valores ingresados coinciden con los declarados, mostrar un mensaje de "Acceso permitido"
4. Si no coinciden mostrar "Ingreso denegado"

### Detectar la estación del año usando el mes.
Pedir que se ingrese el número del mes (1–12) y mostrar un mensaje que diga la estación del año que corresponde a
ese mes.

Usar una estructura de control con `else if()`:
```
if(cond1)
else if(cond2)
else if(cond3)
// etc...
```

Para saber que estación mostrar, podés ayudarte con esta lista:

- Los meses de diciembre, enero y febrero → verano.
- Los meses de marzo, abril y mayo → otoño.
- Para junio, julio y agosto → invierno.
- Y finalmente: septiembre, octubre y noviembre → primavera.

### Descuento por edad
Pedir la edad de una persona y mostrar un mensaje con el descuento que se aplicará:

- Menores de 12 → Entrada gratis.
- Entre 12 y 17 → 50% de descuento.
- 18 o más → Paga completo.

### Semáforo
Pedir el color del semáforo (texto/String: "rojo", "amarillo" o "verde") y mostrar un mensaje con la acción que
se deberá seguir.

- Si el color es "rojo" → La acción será "¡Frená!".
- Si es "amarillo" → "Ojo..."
- Si es "verde" → "Dale nomás."
- Si es otro valor → "Mhhh, en esta ciudad no tenemos semáforos con ese color."

## Acertar la posición :dart:
Ejercicio con condicionales, clase Scanner y vectores bidimensionales para integrar lo que vimos la clase
anterior (vectores) con condicionales.

1. Declarar un vector bidimensional (4x4) y asignarle valores a cada posición siguiendo la siguiente imagen
   
   ![biblioteca](../images/biblioteca_4x4.jpg){ width="250" }
/// caption
Una biblioteca de 4 estantes y 4 'columnas'.
///
2. Usando la clase Scanner, preguntar qué valor tendrá una posición. Por ejemplo, "¿Qué valor tiene nuestra
   biblioteca en la posición [0][0]?".
3. Si el valor ingresado coincide con el valor del vector, mostrar un mensaje de coincidencia. Si no coincide
   mostrar un mensaje de "pifie" y el valor correcto.
4. Repetir el último paso unas 3 o 4 veces, con distintas posiciones.