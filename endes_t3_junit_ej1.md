[Solucion](https://github.com/guillermoroman/endes-t3-daw-demo-1)

## Ejercicio 1: Verificar si un número es par

Enunciado:
En la clase `MathUtils`, crea una función llamada esPar que acepte un entero como entrada y devuelva true si el número es par, y false en caso contrario. Escribe pruebas unitarias para verificar:
- Un número par positivo.
- Un número impar positivo.
- Un número negativo par.
- El caso especial del número 0.

## Ejercicio 2: Comparar dos cadenas de texto

Enunciado:
En una clase `StringUtils`, escribe una función llamada sonIguales que tome dos cadenas de texto y devuelva true si son exactamente iguales, o false en caso contrario. Escribe pruebas unitarias que comprueben:
- Dos cadenas exactamente iguales.
- Dos cadenas con distinto contenido.
- Dos cadenas donde una esté en mayúsculas y la otra en minúsculas.
- Una cadena vacía comparada con otra cadena no vacía.

## Ejercicio 3: Calcular el cuadrado de un número

Enunciado:
En la clase `MathUtils`, crea una función llamada cuadrado que acepte un número entero y devuelva su cuadrado. Escribe pruebas unitarias para verificar:
- El cuadrado de un número positivo.
- El cuadrado de un número negativo.
- El cuadrado del número 0.
- El cuadrado de un número grande.

## Ejercicio 4: Determinar si una palabra contiene una letra

Enunciado:
En la clase `StringUtils`, desarrolla una función llamada contieneLetra que acepte una palabra y una letra como entradas, y devuelva true si la palabra contiene esa letra, o false en caso contrario. Escribe pruebas unitarias para comprobar:
- Una palabra que contiene la letra (en minúscula).
- Una palabra que no contiene la letra.
- Una palabra que contiene la letra en mayúscula, pero la entrada de la letra está en minúscula.
- Una palabra vacía.


## Ejercicio 5
Se quiere realizar una clase `TempConverter`que convierta grados Fahrenheit a Celsius, y viceversa. Debemos averiguar la fórmula e implementar dos métodos `fahrenheitToCelsius` y `celsiusToFahrenheit` que conviertan grados de una a otra, y viceversa.
Además, se quiere testear que convierten los métodos correctamente los valores -5, 0, 15 y 32. 


## Ejercicio 6
Un banco precisa una clase `Gestor de Tarjetas` que contenga el método estático `emitirTarjeta`

`emitirTarjeta` admite dos argumentos (`edad` y `sueldo`) y devuelve un String con el tipo de tarjeta otorgada al cliente en función de unos parámetros:
- Edad mínima para cualquier tarjeta: 18 años.
- Sueldo necesario para la "Tarjeta Dorada":`[800, 1500)`.
- Sueldo necesario para la "Tarjeta Platino": `[1500, 3000)`.
- Sueldo necesario para la "Tarjeta Negra": `[3000,  )`.
- En caso de no cumplir requisitos, el método devuelve `null`.

Crear una clase de pruebas unitarias con métodos @Test que prueben, mediante aserciones, que el comportamiento del método es el adecuado. Pensad en Particiones de Equivalencia y Valores Límite para elegir los valores que utilizarán los test.

