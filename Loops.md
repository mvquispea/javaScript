# Loops

Los loops se utilizan para repetir operaciones en el código.

Ejemplo clasico

```
for(var i=0; i<=10; i++) {
    console.log(i);
}
```

Exiten varios tipos de loops pero alfinal todos hacen los mismo. Repetir código.

Todos los loops tienen 3 partes fundamentales:

- Como iniciar
- Como parar
- Como avanzar a la siguiente repetición

## While loop 

El while loop consiste en la siguiente forma:

```
var start = 0; // Como iniciar
while (start < 10) { // Como parar
  console.log(start);
  start = start + 2; // Como avanzar a la siguiente repetición
}
```

El ejemplo cuenta de dos en dos.

Si algunas de las partes fundamentales del código no esta presente el loop puede fallar.

Por ejemplo

```
while (true) {
  console.log("Estoy dentro un loop infinito");
}
```

```
var x = 0;

while (x < 1) { // La condición es siempre verdadera osea nunca para
  console.log('Oops!');
}
```

#### Ejercicio

¿Que falta en el siguiente while loop?

```
while (x < 6) {
  console.log('Printing out x = ' + x);
}
```

## For loop 

El for loop te obliga a definir las 3 partes fundamentales del loop. 

- Como iniciar
- Como parar
- Como avanzar a la siguiente repetición

Si te olvidas de algúna te da un error de sintaxis.

```
for ( Como iniciar; Como parar; Como avanzar a la siguiente repetición ) {
  // do this thing
}
```

Ejemplo 

```
for (var i = 0; i < 6; i = i + 1) {
  console.log("i = " + i);
}
```

## Incrementar y decrementar

Se pueden incrementar variables de la siguiente forma:

- x++ or ++x // x = x + 1 
- x-- or --x // x = x - 1
- x += 3     // x = x + 3
- x -= 6     // x = x - 6
- x *= 2     // x = x * 2
- x /= 5     // x = x / 5

#### Ejercicio 

Crear un for loop para calcular el factorial de 5

El factorial de 5! = 1*2*3*4*5;

