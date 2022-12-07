## Respuestas al Test de JavaScript

Recuerda que estas respuestas (o al  menos la mayoría) NO SON ABSOLUTAS. Es completamente válido (en la mayoría de casos) si tienes otras respuestas. Recuerda que podemos discutirlo en la sección de comentarios del curso. :D


## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?

Cajtas (espacios en memoria) donde podemos guardar información (dependiendo de los tipos y estructuras de datos que soporte nuestro lenguaje).

- ¿Cuál es la diferencia entre declarar e inicializar una variable?

Declarar es cuando le decimos a JavaScript que vamos a crear una variable con el nombre tal. Mientras que inicializar (o reinicializar) es asignarle un valor a esa variable.

- ¿Cuál es la diferencia entre sumar números y concatenar strings?
- ¿Cuál operador me permite sumar o concatenar?

EL operador que nos permite sumar o concatenar es +. Este operador nos permite sumar números cuando lo usamos con números. Pero cuando los strings, lo que hace es unir (concatenar, así se dice) ambos strings.

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre: string
- Apellido: string
- Nombre de usuario en Platzi: strig (@fulanito)
- Edad: number
- Correo electrónico: string (lala@gmail.com)
- Mayor de edad: boolean
- Dinero ahorrado: number
- Deudas: number

### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```
let nombre = 'Elmer';
let apellido = 'Rosado Diaz';
let username = 'rdae07';
let edad = 33;
let mail = 'rosadoelmer61@gmail.com';
let esMayorDeEdad = true;
let dineroAhorrado = 1000;
let deudas = 100;
```

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

```
let nombreCompleto = nombre + ' ' + apellido;
let dineroReal = dineroAhorrado - deudas;
```



## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?
Las funciones nos permiten encapsular (guardar) bloques de codigo para reutilizarlos y ejecutarlos en el futuro.

- ¿Cuándo me sirve usar una función en mi código?
Nos sirve cuando tenemos variables o bloques de codigo muy parecidos (con cambios que ser parametros y argumentos).
Tambien nos sirve para ordenar y mejorar la legibilidad de nuestro codigo


- ¿Cuál es la diferencia entre parámetros y argumentos de una función?
las funciones reciben parametros cuando las creamos. Y les enviamos argumentos cuando las ejecutamos.

### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```js
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
function nombreCompleto(name, lastName) {
    return name + ' ' + lastName;
}

function saludo(name, lastName, userName) {
    const completeName = nombreCompleto(name, lastName);
    console.log('Mi nombre es ' + completeName + ', pero prefiero que me digas ' + userName + '.');
}

```


## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?
Son la forma en que ejecutamos un bloque de codigo u otro dependiendo de alguna condicion o validacion.

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
IF (else y else if), switch
El condicional if(con el else y else if), nos permite hacer validaciones completamente distintas (si asi queremos) en cada validacion o condicional. En cambio, en el switch todos los cases se comparan con la misma variable o condicion que definimos en el switch

- ¿Puedo combinar funciones y condicionales?
Si. Las funciones pueden encapsular cualquier bloque de codigo, incluyendo condicionales. 

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```js
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}
```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).
```js
if(tipoDeSuscripcion === 'free') {
    console.log('Solo puedes tomar los cursos gratis')
} else if(tipoDeSuscripcion === 'Basic') {
    console.log('Puedes tomar casi todos los cursos de platzi durante un mes');
} else if(tipoDeSuscripcion === 'Expert') {
    console.log('Puedes tomar casi todos los curso de Platzi durante un año');
}  else if(tipoDeSuscripcion === 'ExpertPlus') {
    console.log('Tu y alguien mas pueden tomar TODOS los cursos de Platzi durante un año')
} else {
    console.log('No puedes tomar ningun curso')
}

function conseguirTipoDeSuscripcion(suscripcion) {
    if(suscripcion === 'free') {
        console.log('Solo puedes tomar los cursos gratis')
        return;
    } 
    if(suscripcion === 'Basic') {
        console.log('Puedes tomar casi todos los cursos de platzi   durante un mes');
        return;
    }
    if(suscripcion === 'Expert') {
        console.log('Puedes tomar casi todos los curso de Platzi durante un año');
        return;
    }  
    if(suscripcion === 'ExpertPlus') {
        console.log('Tu y alguien mas pueden tomar TODOS los cursos de Platzi durante un año')
        return;
    } 
    console.warn('No puedes tomar ningun curso')

}


```
> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays y un solo condicional. 😏
```js
const tipoDeSuscripcion = {
    free: 'Solo puedes tomar los cursos gratis',
    basic: 'Puedes tomar casi todo los cursos de Platzi durante un mes',
    expert: 'Puedes tomar casi todos los curso de Platzi durante un año',
    expertPlus: 'Tu y alguien mas pueden tomar TODOS los cursos de Platzi durante un año'
}

function conseguirTipoDeSuscripcion(suscripcion) {
    if(tipoDeSuscripcion[suscripcion]) {
        console.log(tipoDeSuscripcion[suscripcion])
        return;
    }
    console.warn('Ese tipo de suscripcion no existe')
}
```

## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?
La forma de ejecutar un bloque de codigo hasta que se cumpla cierta condicion.

- ¿Qué tipos de ciclos existen en JavaScript?
while, do while, for.

- ¿Qué es un ciclo infinito y por qué es un problema?
Es cuuando la validacion de nuestros condicionales nunca se cumple y termina dañando la aplicacion.

- ¿Puedo mezclar ciclos y condicionales?
Si, aunque los ciclos son una especie de condicionales, nada nos impide agregar mas condicionales dentro del ciclo 

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:


```js
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

var i = 0;

while (i < 5) {
    console.log('El valor de i es: ' + i)
    i++;
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```
```js

var i = 10;

while (i > 0) {
    console.log('El valor de i es: ' + i)
    i--;
}

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

```js
let respuesta;
while(respuesta != '4') {
    let pregunta = prompt('Cuanto es 2 + 2')
    respuesta = pregunta;
}
```
## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?
Es una lista de elementos 
```js
const array = [1, 'Hola', true, false]
```


- ¿Qué es un objeto?
Es una lista de elementos pero cada elemento tiene un nombre clave
```js
const obj = {
    nombre: 'Elmer',
    edad: 33
}
```

- ¿Cuándo es mejor usar objetos o arrays?
Arrays cuando lo que haremos en un elemento es lo mismo que en todos los demas (la regla se puede incumplir). Mientras que un objeto cuando los nombres de cada elemento son importantes para nuestro algoritmo.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
Si


### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.
```js
function imprimirPrimerElememtoArray(arr) {
    console.log(arr[0]);
}
imprimirPrimerElementoArray([1, 2, 3, 4])
```
### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```js
function imprimirElementoPorElemento(arr) {
    for(let i = 0; i < arr.length; i++)
    console.log(arr[i]) 
}

imprimirElementoPorElemento(['Elmer', 'Rosado', 'Diaz'])

```
### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```js
function imprimirElementoPorElementoObjeto(obj) {
    const arr = Object.values(obj)
    for(let i = 0; i < arr.length; i++)
    console.log(arr[i]) 
}

const obj = {
    nombre: 'Elmer',
    edad: 33
}

```