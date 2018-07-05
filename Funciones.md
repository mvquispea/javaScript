# Funciones

Las funciones te permiten agrupar código que se va poder utilizar y reutilizar en distintas
partes del programa.

Algunas funciones pueden recivir parametros. Los parametros de la funcion se escriben en 
una lista separada por comas y entre parentesis despues del nombre de la función.

Por Ejemplo

```
// funcion sin parametros
function hola() {
  var mensaje = "Hola!"
  console.log(mensaje);
}
```

```
// funcion con parametros
function hola(nombre) {
  var mensaje = "Hola, "
  console.log(mensaje + nombre);
}
```


## Valores de return

Las funciones pueden devolver valores. 

Por Ejemplo

```
// funcion con parametros
function hola(nombre) {
  var mensaje = "Hola, " + nombre;
  return mensaje; // Devuelve la variable mensaje
}
```

## Ejecutar las funciones

Las funciones se ejecutan escribiendo su nombre seguido por parentesis.

Por ejemplo

```
hola();
```

En caso que la función tengar parameros se deben escribir entre los parentesis.


Por ejemplo

```
var nombre = "Marco";
console.log(hola(nombre));
```

## Parametros vs Argumentos

Los parametros son variables que se utilizan para almacenar los datos que son 
pasados a la función.

Los argumentos son datos actuales que le pasamos a la función.

Por ejemplo

```
// x , y son parametros de la función
function add(x, y) {
  var sum = x + y;
  return sum; // returna la suma
}

// 1 y 2 son los argumentos pasados a la función
var sum = add(1, 2);
```

## Cuerpo de la función 

El cuerpo de la función esta formado por el código que esta entre la llave abierta y llave cerrada.

```
function add(x, y) {
    // cuerpo de la función
}
```

### Ejercicios 

1. Declara una función "risa" que devuelva la cadena "jajajaja".
2. Declara una función "risa" que reciva un parametro con el número de "ja" para devolver.

# Scope

El scope es el contexto donde una variable o función es visible y utilizable. 
Cuando utilizamos una variable nos tenemos que hacer la pregunta si es que "esta" dentro el 
scope.

- Mostra ejemplo de la biblioteca

En JavaScript tenemos dos tipos de scopes: Global y funcional.

## Global scope 

Una variable que esta definida fuera de una función se considera que esta en el Scope global.
Eso significa que puede ser leida en cualquier parte del codigo.

## Function scope 

Si una variable esta definida dentro una función esta puede ser leida en cualquir parte del cuerpo de la función. Incluso en otra funciones definidas dentro de la misma.

#### Ejercicio 

Donde puedo imprimir el valor de `z` sin que se verifique un error.

```
var a = 1;
function x() {
  var b = 2;
  function y() {
    var c = 3;
    function z() {
      var d = 4;
    }
    z();
  }
  y();
}

x();
```

## Shadowing the scope 

Hay ocasiones que se sobre escribe el scope.

Por ejemplo 

```
var nombre = "Marco";
console.log(nombre);

function imprimir() {
  nombre = "Jose";
  console.log(nombre);
}

imprimir();
console.log(nombre);
```

## Variables globales

Las variables globales se consideran mala practica.

## Hoisting

En la mayoria de lenguajes de programación tienes que definir las funciones antes de ser utilizadas.
El programa se interpreta de arriba hacia abajo.

Por ejemplo 

```
hola("Julia");

function hola(name) {
  console.log("Hola " + name);
}
```

En JavaScript antes de ejecutar el código las funciones son movidas hacia la parte superior. 
Esta accion en ingles se llama "Hoisting".

Por ejemplo 

```
function hola(name) {
  console.log("Hola " + name);
}

hola("Julia");
```

Para evitar confusiones es considerado buena practica declarar las funciones y variables antes en la parte superior de código antes de utilizarlas.

La declaracion de variable tambien son movidas a la parte superior del codigo pero no la asignación de la misma.

Por ejemplo 

```
function hola(name) {
  console.log(saludo + name);
  var saludo = "Hola";
}

hola("Julia");
```

Resulta en

```
function hola(name) {
  var saludo;
  console.log(saludo + name); // Undefined
  saludo = "Hola";
}

hola("Julia");
```


## Funciones como expresiones

Asi como puedo almacenar datos en variables tambien puedo almacenar funciones en varibles.

Por Ejemplo

```
var saludo = function() {
  return "Hola";
}
```

La función no tiene nombre y es considerada anonima.

Probar en la consola.

```
var saludo = function() {
  return "Hola";
}

console.log(saludo);
```

La asignación de una función no se mueven hacia la parte superior del código porque se comportan
como variables.

## Funciones como parametros 

Es posible enviar funciones como parametros al igual que cualquier otra variable. Este tipo 
de parameros se llaman callbacks.

```
var risa = function(max) {
  var risa = "";
  for (var i = 0; i < max; i++) {
    risa += "ja";
  }
  return risa;
};

// function declaration helloCat accepting a callback
function carcajada(callbackFunc) {
  return callbackFunc(5);
}

// pass in catSays as a callback function
console.log(carcajada(risa));
```

## Funciones en linea

Podemos declarar funcion anonimas directamente como un atributo a una funcion. 

Por Ejemplo

```
document.body.addEventListener('click', function () {
     var myParent = document.getElementsByTagName("H1")[0].innerHTML = "Bienvenidos al curso de JavaScript"; 
});
```




