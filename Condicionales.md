# Condicionales

En JavaScript se utilizan los condicionales para tomar decisiones en el código. Por ejemplo nosotros todo el tiempo tomamos decisiones sobre que acciones tomar. 

Por ejemplo cuando voy a comprar algo primero me pregunto si tengo dinero suficiente.

Los condicionales utilizan las variable booleanas para tomar decisiones y la sentencia `if / else`.

```
var precio = 50; // El precio del producto
var dinero = 100; // Cuanto dinero tengo

if(dinero >= precio) {
    console.log("Lo compro");
} else {
    console.log("No lo puedo comprar");
}
```

Como se leen los condicionales

```
if (/* Si esta expresion es verdadera */) {
  // Ejecuta esta parte del código
} else {
  // Sino ejecuta esta parte del código
}
```

En algunas situaciones no es suficiente el `if / else` para eso podemos crear una cadena de `if / else`.

por ejemplo

```
var clima = "soleado";

if (clima === "nieve") {
  console.log("Poner una chompa.");
} else if (clima === "lluvia") {
  console.log("Sacar paraguas.");
} else {
  console.log("Salir con short.");
}
```

El último `else` seria el valor por defecto de la cadena.

#### Ejercicio

Escribir un programa para detectar número pares o impares. Tip: utilizar el operador `%`.

## Operadores logicos

Los operadores logicos sirven para combinar condiciones. Por Ejemplo

```
var agenda = "libre";
var clima = "soleado";

if (agenda === "libre" && clima === "soleado") {
  console.log("Ir al parque");
}
```

El operador `&&` significa el _y_ logico.

Los operadores logicos se utilizan para crear complejas condiciones logicas.

| Operador | Significado
| -
| && | 	Operador logico _y_.
| \\\| 	Operador logico _o_.
| !  |  Operador logico "distinto de".

Las expresiones logicas son evaluadas de izquierda a derecha.

#### Table boleana

| && | (AND)
| -
| A	| B | 	A && B
| true | true | true
| true | false | false
| false | true | false
| false	| false | false

|| (OR)
| -
| A	| B	OR A | B
| true | true | true
| false | true | true
| true | false | true
| false | false | false

## El operador ternario

A vece es demasiado largo escribir la sentencia `if / else`. 

Por ejemplo:

```
var cielo = true;
var color;

if (cielo) {
  color = "azul";
} else {
  color = "griz";
}

console.log(color);
```

Se puede escribir de la forma:

```
var cielo = true;
var color = cielo ? "azul" : "griz";
console.log(color);
```

El operador ternario se lee de la forma:

```
condición ? (se ejecuta si la condición es verdadera) : (se ejecuta si la condición es false)
```

## La sentencia Switch

La sentencia _switch_ sirve para abreviar las cadenas de `if / else`. 

Por Ejemplo

```
if (option === 1) {
  console.log("You selected option 1.");
} else if (option === 2) {
  console.log("You selected option 2.");
} else if (option === 3) {
  console.log("You selected option 3.");
} else if (option === 4) {
  console.log("You selected option 4.");
} else if (option === 5) {
  console.log("You selected option 5.");
} else if (option === 6) {
  console.log("You selected option 6.");
}
```

Se puede escribir de una manera más compacta utilizando la sentencia _switch_.


```
switch (option) {
  case 1:
    console.log("You selected option 1.");
  case 2:
    console.log("You selected option 2.");
  case 3:
    console.log("You selected option 3.");
  case 4:
    console.log("You selected option 4.");
  case 5:
    console.log("You selected option 5.");
  case 6:
    console.log("You selected option 6.");
}
```

### El operador _break_

El operador break se utiliza para separa los casos del _switch_. 

Por ejemplo:

```
var mes = 2;

switch(mes) {
  case 1:
  case 3:
  case 5:
  case 7:
  case 8:
  case 10:
  case 12:
    dias = 31;
    break;
  case 4:
  case 6:
  case 9:
  case 11:
    dias = 30;
    break;
  case 2:
    dias = 28;
}

console.log("Tenemos " + dias + " en el mes.");
```

Podemos agregar un valos por defecto al switch con el la palabra clave _default_.


