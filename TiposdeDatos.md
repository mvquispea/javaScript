#### Tipos de datos

La computadoras almacenan la información en la memoria. La información almacenada puede ser de varios tipos por ejemplo: El nombre de una persona equivalen a un conjunto de letras. La edad de una persona es un número. En JavaScript tenemos 4 tipos de datos principales

- numbers (Números)
- string (Cadenas)
- boolean 
- undefined

Las cadenas o string son un conjunto de letras escrias entre comillas dobre o simples por ejemplo "Bienvenidos".

- Probar en la consola "Bienvenidos"
- Probar en la consola Bienvenidos

## Números

En JavaScript se pueden definir números enteros, decimales, negativos o positivos de manera muy sencilla.

- Probar en la consola 
- 12
- 52.3
- -56

### Operaciones aritmeticas

Es posible ejecutar todas las operaciones aritmeticas con los números.

- Probar en la consola
- 10 + 20
- 5 * 99
- (10/5) * 4 - 20

### Comparar números

Comparar dos número es muy sencillo. 

- 10 > 50
- 0 == 1
- 10 == 10

El resultado de comparar dos números es un valor boleano verdadero o falso.

| Operador | Significado  |
| -  
| <        | Menor |
| >	       | Mayor |
| <=       | Menor o igual |
| >=       | Mayor o igual |
| ==       | Igual    |
| !=       | Distinto |

## Comentarios

En JavaScript los comentarios se escriben agregando la doble barra al inicio de la sentencia. En caso que se quiera agregar comentario es más de una linea se agrega el simbolo /\* para abrir el comentario y \*/ para cerrar el comentario. Los comentarios son ignorados por JavaScript.

```
// Esto es un comentario de una sola linea
console.log("Hola");
/*
 Este es 
 un comentario 
 multilinea
*/
```

## Strings (Cadenas)

Los strings son un conjunto de letras entre comillas dobles o simple. Podemos utilizar las cadenas para formar frases, oraciones y nombres.

Por ejemplo

```
"hola como estan";
'Muy bien';
```

Es correcto utilizar comilla dobles o simple pero es recomendable utilizar solo una de ellas.

- Probar en la consola
- "Hola"
- 'chao'
- adios

#### Concatenación de Cadenas

Es posible juntar cadenas para formar cadenas más grandes. Esta operación se llama concatenar las cadenas. El operador para concatenar dos cadenas con el operador `+`.

- Probar en la consola
- "Hola, " + "Lima"
- "Hola" + "todos"
- ¿Cual es el resultado de "Hello + 5*10"?
- Y "Hello" + 5*10

## Variables

Hasta ahora todos los datos que hemos utilizado se pueden utilizar una sola vez. En JavaScript se puede almacenar los datos en variables. Los datos almacenados en variables quedan grabados en la memoria de la computadora y puede ser reutilizados.

Ejemplo:

```
var saludo = "Hola";
saludo + " Marco";
saludo + " Todos";
var edad = 10;
edad < 18
```

Se puede almacenar cualquier tipo de datos en una variable.

#### Convenciones

JavaScript utiliza la convecions camelCase para escribir el nombre de las variables. CamelCase dice que las variables tienen que empezar con una letra minuscula y cada nueva palabra la primera con mayusculas.

- ¿Cuales son buenos nombres para las variables?
- var edad;
- var t;
- var correo;
- var nombreApellido;
- var cosa;

#### Ejercicio

Programar un transformador de temperatura de Celcius a Fahrenheit con la formula. Tip. utilizar console log y las variables:

- var fahrenheit;
- var celcius;

`F = C x 1.8 + 32`

## Indice en cadenas 

Es posible acceder a todas las letras que forman una cadena con el indice que indica su posición. El indice empieza con el número 0.

- Probar en la consola
- "Marco"[0];
- "Marco"[2];
- "Marco"[10];
- "El indice empieza con el número 0"[4];

El indice tambien funciona con las variables.

- Probar en la consola
- var nombre = "Marco";
- nombre[2];

## Letras especiales en las cadenas

- Probar en la consola
- "Literalmente dijo: "Porfavor responde.""

La consola de una error de sintaxis: `SyntaxError`. Para evitar los errors de sintaxis debermos "escapar" las letras especiales con el simbolo `\`.
 
- Probar en la consola
- "Literalmente dijo: \"Porfavor responde.\""

Escapar la letra le dice a JavaScript que ignore el significado especial de la misma y que la imprima literalmente.

### Letras especiales

| Code | Character | 
| -
| \\   | \ (backslash)
| \"   | '' (comilla dobre)
| \'   | ' (comilla simple)
| \n   | salto de linea
| \t   | tab

- Probar en la consola
- "Sube sube\n\tbaja baja"
- "Sube sube\\n\\tbaja baja"

#### Ejercicio

¿Como se imprime la siguiente frase?
"The file located at "C:\\Desktop\My Documents\Roster\names.txt" contains the names on the roster."

## Comparar Cadenas

Asi como los números se pueden compara cadenas en manera sencilla.

- Probar en la consola
- "rojo" == "rojo"
- "si" == "si"
- "verde" == "Verde"
- "verde" > "Verde"

JavaScript compara letra por letra utilizando su valos númerico. Para ver el valor número de las letras ir a: https://www.ascii-code.com/

#### Ejercicio

Imprimir en la consola en siguiente chiste (dos lineas).

```
¿Quién es el hermano de "James Bond"?
Car Bon.
```

## Boleanos

Las variables boleanas solo pueden almacenar dos valores: verdadero o falso.

## Null, Undefined, and NaN

Asi como a una variable le podemos asignar un número pero ejemplo:

- var edad = 10;

Tambien podemos asignar a el valor `null` a una variale.

### Diferencias entre null y Undefined

`null` significa que la variable "no tiene valor" mientras que `Undefined` significa la ausencia de valor.

- Probar en la consola
- var edad = null;
- console.log(edad);
- var x;
- console.log(x);

## Que significa NaN?

`Ǹan` significa "Not a number" y normalmente es el resultado de operaciones matematicas invalidas.

- Probar en la consola
- Math.sqrt(-10)
- "hola"/5

####

Que valor va a salir en la consola cuando pongo:

```
var signedIn;
console.log(signedIn);
```

## Igualdad entre datos

Hasta ahora hemos visto que para comparar datos utilizamos el operador "==". El operador funciona bien con se comparan datos del mismo tipo pero cuando se comparan datos de tipos distintos pueden dar resultados incorrectos.

- Probar en la consola
- "1" == true
- 0 == false

¿Porque?

En JavaScript no es necesario definir el tipo de la variable tecnicamente se llama _loosely typed language_. Cuando el código es ejectuado JavaScript convierte las variables al tipo de dato apropiado automaticament esto se llama _implicit type coercion_. 

- Probar en la consola
- "julia" + 1

En este ejemplo el resultado es la cadena "julia1". En otros lenguajes de programación esto seria un error ya no se podria sumar la cadenas más 1.

### Igualdad estricta

En algunos casos se quiere comparar el valor de la variable y ademas el tipo de variable. Para hacer una comparación estricta se utiliza el operador `===`.

- Probar en la consola
- 1 === "1"


#### Ejercicio

Calcular la cuenta de un restaurante más la propina.


