# JavaScript

JavaScript es un lenguaje de programación creado para las páginas webs. En el año 1995 Brendan Eich creo JavaScript para facilitar la creación de páginas web dinamicas y la interacción con los usuarios. 

Hoy JavaScript se utiliza en todos los aspectos de desarrolo web desde el frontend and backend.

## Diferencias entre JavaScript, Html y Css

Html y CSS son lenguajes que se utilizan para describir un documento. El navegador dibuja la página web según como esta especificada en los documentos Html y Css. JavaScript es un lenguaje de programación que se utiliza para comunicar instrucciones a la computadora. Antes de la creación de JavaScript las páginas webs eran totalmente estaticas y consistian de unicamente Html y Css.

## Intrumentos para el curso

Vamos a utilizar la consola de Google Chrome para escribir código JavaScript.La consola es accesible atraves del enlace "developer tools" tambien vamos a utilizar la plataforma https://codepen.io/.

- Abrir la consola 
- Escribir tu nombre
- Escribir alert("Bienvenidos")

Ejecutar código directamente en el navegador se puede hacer para hacer pruebas rápidas pero no es lo más indicado para desarrollar JavaScript. Es recomendable utilizar un editor de texto para escribir todo el código JavaScript y luego pegarlo a la consola para probarlo en caso no tengamos un ambiente de trabajo se puede utilizar la plataforma codepen.io totalmente gratis.

## console.log

`console.log` se utiliza para imprimir información en la consola de JavaScript. Por lo general se utiliza para hacer pruebas y verificar que el código esta haciendo lo que nosotros esperamos.

```
console.log("Hola todos");
```

```
for (var i = 0; i < 10; i++) {
  console.log(i);
}
```

## JavaScript demo

- Entra a fullstack.pe
- Copiar el codigo en la consola de JavaScript
- ¿Que sucede?

```
document.body.addEventListener('click', function () {
     var myParent = document.getElementsByTagName("H1")[0].innerHTML = "Bienvenidos al curso de JavaScript"; 
});
```
