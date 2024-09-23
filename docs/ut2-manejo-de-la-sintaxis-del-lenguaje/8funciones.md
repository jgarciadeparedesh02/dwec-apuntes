# Funciones y Parámetros en JavaScript

### 🧑‍💻 ¿Qué son las Funciones en JavaScript?

Las funciones son bloques de código reutilizables que permiten realizar tareas específicas. En JavaScript, son fundamentales para la modularización del código y la reutilización de lógica, ayudando a mantener el código limpio y organizado.

```javascript
// Declaración de una función simple
function saludar() {
    console.log("¡Hola, mundo!");
}

// Llamada a la función
saludar(); // Output: ¡Hola, mundo!
```

### 🔍 Tipos de Funciones en JavaScript

#### 1. **Funciones Declarativas**

Son las funciones definidas utilizando la palabra clave `function`. Son fáciles de leer y permiten ser llamadas antes de ser declaradas, gracias al concepto de hoisting.

```javascript
// Declaración de función
function sumar(a, b) {
    return a + b;
}

console.log(sumar(3, 4)); // Output: 7
```

#### 2. **Funciones Anónimas (Funciones de Expresión)**

Son funciones sin nombre que se asignan a variables. A diferencia de las declarativas, no pueden ser llamadas antes de su definición.

```javascript
// Función anónima asignada a una variable
const restar = function(a, b) {
    return a - b;
};

console.log(restar(10, 3)); // Output: 7
```

#### 3. **Funciones Flecha (Arrow Functions)**

Introducidas en ES6, las funciones flecha (`=>`) permiten una sintaxis más compacta y no tienen su propio `this`, lo cual es útil en algunos contextos.

```javascript
// Ejemplo de función flecha
const multiplicar = (a, b) => a * b;

console.log(multiplicar(5, 2)); // Output: 10
```

### 🎯 Parámetros y Argumentos en JavaScript

Los **parámetros** son variables que se definen en la declaración de la función, mientras que los **argumentos** son los valores que pasamos a la función cuando la llamamos.

```javascript
// Función con parámetros
function presentar(nombre, edad) {
    console.log(`¡Hola! Soy ${nombre} y tengo ${edad} años.`);
}

// Llamada a la función con argumentos
presentar("Ana", 25); // Output: ¡Hola! Soy Ana y tengo 25 años.
```

### 🌟 Parámetros Predeterminados

JavaScript permite definir valores predeterminados para los parámetros. Si no se proporciona un argumento, la función usará el valor por defecto.

```javascript
// Parámetro con valor predeterminado
function saludar(nombre = "Invitado") {
    console.log(`Hola, ${nombre}!`);
}

saludar(); // Output: Hola, Invitado!
saludar("Carlos"); // Output: Hola, Carlos!
```

### 📊 Parámetros Rest y Spread

- **Rest (`...`)**: Permite agrupar múltiples argumentos en un solo parámetro como un array.
  
  ```javascript
  function sumarTodos(...numeros) {
      return numeros.reduce((total, num) => total + num, 0);
  }

  console.log(sumarTodos(1, 2, 3, 4)); // Output: 10
  ```

- **Spread (`...`)**: Permite expandir un array en múltiples elementos, útil para pasar un conjunto de valores a una función.

  ```javascript
  const numeros = [10, 20, 30];
  console.log(Math.max(...numeros)); // Output: 30
  ```

### 🎨 Funciones Anidadas y Funciones de Orden Superior

JavaScript permite funciones dentro de otras funciones, así como pasar funciones como argumentos o retornarlas como valores.

```javascript
// Función de orden superior
function calcular(operacion, a, b) {
    return operacion(a, b);
}

// Función que se pasa como argumento
const division = (x, y) => x / y;

console.log(calcular(division, 10, 2)); // Output: 5
```