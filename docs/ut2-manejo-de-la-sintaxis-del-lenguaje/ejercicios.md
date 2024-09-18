## Ejercicios de JavaScript: Sintaxis y conceptos básicos

### 1. Variables: Declaración, Inicialización, y Ámbito
**Ejercicio 1.1: Declaración e Inicialización de Variables**
Declara tres variables: una de tipo `var`, otra de tipo `let` y otra de tipo `const`. Inicialízalas con cualquier valor.

```javascript
// Declara una variable con var
var nombre = "Juan";

// Declara una variable con let
let edad = 25;

// Declara una constante con const
const PI = 3.1416;
```

**Ejercicio 1.2: Ámbito de Variables**
Escribe un código donde demuestres el comportamiento de `var`, `let`, y `const` dentro y fuera de un bloque (`if`, `for`, etc.).

```javascript
function pruebaAmbito() {
    if (true) {
        var variableVar = "Dentro del bloque con var";
        let variableLet = "Dentro del bloque con let";
        const variableConst = "Dentro del bloque con const";
    }
    console.log(variableVar); // Accesible
    console.log(variableLet); // Error: No accesible
    console.log(variableConst); // Error: No accesible
}
pruebaAmbito();
```

**Ejercicio 1.3: Reasignación de Variables**
Declara una variable con `let` y reasígnale un nuevo valor más adelante en el código. Haz lo mismo con una variable `var` y una constante `const` para observar qué sucede.

```javascript
let ciudad = "Madrid";
ciudad = "Barcelona"; // Reasignación válida

var pais = "España";
pais = "Francia"; // Reasignación válida

const continente = "Europa";
// continente = "Asia"; // Error: No se puede reasignar una constante
```

**Ejercicio 1.4: Hoisting**
Demuestra el comportamiento del hoisting con `var`, `let` y `const`. Escribe un código donde declares variables después de usarlas, para ver cómo actúa el hoisting en cada caso.

```javascript
console.log(x); // Undefined, debido al hoisting de var
var x = 5;

try {
    console.log(y); // Error: no se puede acceder antes de la declaración
    let y = 10;
} catch (e) {
    console.log(e.message);
}

try {
    console.log(z); // Error: no se puede acceder antes de la declaración
    const z = 15;
} catch (e) {
    console.log(e.message);
}
```

**Ejercicio 1.5: Ámbito Funcional vs Ámbito de Bloque**
Crea una función y dentro de ella declara variables con `var`, `let` y `const`. Muestra la diferencia de comportamiento de `var` frente a `let` y `const` en el ámbito funcional y de bloque.

```javascript
function pruebaAmbitoFuncional() {
    if (true) {
        var varEnBloque = "var dentro del bloque";
        let letEnBloque = "let dentro del bloque";
        const constEnBloque = "const dentro del bloque";
    }
    console.log(varEnBloque); // Accesible: var tiene ámbito funcional
    try {
        console.log(letEnBloque); // Error: let tiene ámbito de bloque
    } catch (e) {
        console.log(e.message);
    }
    try {
        console.log(constEnBloque); // Error: const tiene ámbito de bloque
    } catch (e) {
        console.log(e.message);
    }
}
pruebaAmbitoFuncional();
```

### 2. Tipos de Datos y Conversión de Tipos
**Ejercicio 2.1: Tipos de Datos Básicos**
Declara variables de los siguientes tipos: string, number, boolean, array, objeto.

```javascript
let cadena = "Hola Mundo";
let numero = 42;
let booleano = true;
let arreglo = [1, 2, 3, 4];
let objeto = { nombre: "Juan", edad: 25 };
```

**Ejercicio 2.2: Conversión de Tipos**
Convierte los siguientes valores: 
1. De número a string.
2. De string a número.
3. De booleano a número.

```javascript
let num = 10;
let str = num.toString(); // Conversión a string
let nuevoNum = Number("20"); // Conversión a número
let booleanoANum = Number(true); // Conversión de booleano a número (1)
```

### 3. Asignaciones
**Ejercicio 3.1: Asignaciones Básicas**
Declara una variable y asígnale un valor. Luego, actualiza su valor usando operadores de asignación como `+=`, `-=`, `*=`, `/=`.

```javascript
let contador = 5;
contador += 3; // Ahora contador es 8
contador -= 2; // Ahora contador es 6
contador *= 2; // Ahora contador es 12
contador /= 3; // Ahora contador es 4
```

### 4. Operadores
**Ejercicio 4.1: Operadores Aritméticos**
Crea una función que reciba dos números y devuelva la suma, resta, multiplicación, y división de ambos.

```javascript
function operacionesBasicas(a, b) {
    console.log("Suma:", a + b);
    console.log("Resta:", a - b);
    console.log("Multiplicación:", a * b);
    console.log("División:", a / b);
}
operacionesBasicas(10, 5);
```

**Ejercicio 4.2: Operadores Lógicos**
Usa operadores lógicos (`&&`, `||`, `!`) para evaluar condiciones.

```javascript
let a = true;
let b = false;

console.log(a && b); // false
console.log(a || b); // true
console.log(!a); // false
```

### 5. Comentarios al Código
**Ejercicio 5.1: Añade Comentarios**
Escribe un código básico y añade comentarios que expliquen cada paso. Usa comentarios de línea y de bloque.

```javascript
// Comentario de una línea
let numero = 10; // Inicializa una variable

/*
   Este bloque de código multiplica el valor de la variable por 2
   y lo imprime en la consola.
*/
numero *= 2;
console.log(numero);
```

### 6. Sentencias y Condicionales
**Ejercicio 6.1: Condicionales If/Else**
Escribe una función que reciba un número y muestre un mensaje dependiendo de si es positivo, negativo o cero.

```javascript
function evaluarNumero(numero) {
    if (numero > 0) {
        console.log("El número es positivo");
    } else if (numero < 0) {
        console.log("El número es negativo");
    } else {
        console.log("El número es cero");
    }
}
evaluarNumero(10);
```

**Ejercicio 6.2: Switch Case**
Crea un programa que use `switch` para elegir una acción basada en el día de la semana.

```javascript
let dia = "martes";

switch (dia) {
    case "lunes":
        console.log("Es lunes, comienzo de la semana");
        break;
    case "martes":
        console.log("Es martes, sigue adelante");
        break;
    case "viernes":
        console.log("Es viernes, casi fin de semana");
        break;
    default:
        console.log("Día no válido");
}
```

### 7. Bucles
**Ejercicio 7.1: Bucle For**
Escribe un bucle `for` que imprima los números del 1 al 10.

```javascript
for (let i = 1; i <= 10; i++) {
    console.log(i);
}
```

**Ejercicio 7.2: Bucle While**
Usa un bucle `while` para contar hacia atrás desde 5 hasta 1.

```javascript
let contador = 5;
while (contador > 0) {
    console.log(contador);
    contador--;
}
```

**Ejercicio 7.3: Sentencias de Ruptura de Bucle**
Usa las sentencias `break` y `continue` en un bucle `for`.

```javascript
for (let i = 1; i <= 10; i++) {
    if (i === 5) {
        continue; // Salta la iteración cuando i es 5
    }
    if (i === 8) {
        break; // Termina el bucle cuando i es 8
    }
    console.log(i);
}
```