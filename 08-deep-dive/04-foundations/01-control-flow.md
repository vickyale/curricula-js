# Control de Flujo

* Formato: `lectura`
* Duración: `15 min`

***

## Loops

### Mecanismos que pueden ser usados con cliclos

Los siguientes mecanismos pueden ser usados con ciclos:

A través de toda la formación que a este minuto has recibido, ya sabes cuáles son las sentencias condicionales, además conoces los bucles o loops , que pertenecen a toda el área de control de flujo en Javascript, en ésta parte me gustaría más contarte a cerca de las sentencias de manejo de excepciones.
Prácticamente cualquier objeto puede ser lanzado en JavaScript. Sin embargo, no todos los objetos lanzados son creados igual. Mientras que es bastante común lanzar números o strings como errores, frecuentemente es más efectivo utilizar uno de los tipos de excepciones específicamente creados para este proposito:


#### `break [label]`

Sale de un ciclo.


#### `continue [label]`

Detiene la iteración actual e inmediatamente ejecuta la siguiente.

#### `Labels`

Un `label`(etiqueta) es un identificador seguido por `:`. Al inicio de un ciclo,
un label te permite hacer `break` o `continue` incluso si está dentro anidado de
otro ciclo anidado. Cuando está al inicio de un bloque, te permite salir del
mismo con la sentencia `break`. En ambos casos, el nombre del label se convierte
en un argumento de `break` o `continue`. Aquí un ejemplo de `break`:

```javascript
const findEvenNumber = arr => {
  loop: { // label
    for (let i = 0, l = arr.length; i < l; i++) {
      let element = arr[i];
      if (element % 2 === 0) {
        console.log(`Found: ${element}`);
        break loop;
      }
    }
    console.log('No even number found.');
  }
  console.log('DONE');
};
```

### while

Un ciclo while:

```javascript
while (condition) {
  // statement
}
```

Ejecuta `statement` tantas veces como la condición se cumpla. Si la condición es
siempre `true`, entonces entra en un `infinite loop` (ciclo infinito).

```javascript
// infinite loop
while (1 === 1) { }
```

En el siguiente ejemplo, eliminamos todos los elementos del arreglo y los
mostramos en la consola:

```javascript
const arr = ['a', 'b', 'c'];
>>>>>>> e56650d53cc10d9025ae29fb70547825f7ef0f9c

while (arr.length > 0) {
  console.log(arr.shift());
}


/*
 *
 * La salida de este código será:
 * a
 * b
 * c
 *
 */
```


### do-while

Un ciclo do-while:

```javascript
do {
  // statements
} while (condition);
```


```javascript
const pattern = /^[0-9]+$/;
let line;
do {
  line = prompt('Enter a number:');
} while(!pattern.test(line));
```

### for

En un ciclo for:

```javascript
for ([init]; [condition]; [post_iteration]) {
  // statements
}
```

`init` es ejecuta una vez antes que inicie el ciclo, que ejecuta `statements`
tantas veces como `condition` sea `true`. Puedes usar `let` para declarar
variables, pero el scope de dicha variable solo será dentro del cliclo.
`post_iteration` se ejecuta luego de cada iteración. Por ejemplo:

```javascript
const arr = ['a', 'b', 'c'];

for (let i = 0, l = arr.length; i < l; i++) {
  console.log(arr[i]);
}

/*
 *
 * El resultado de este código es:
 * a
 * b
 * c
 *
 */
```

***

[Continuar](02-built-in-objects.md)