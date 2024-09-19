# 🧩 Tipos de Datos en JavaScript

En JavaScript, los **tipos de datos** son fundamentales para manejar y manipular la información. Conocerlos te ayudará a escribir código más robusto y comprender mejor cómo funcionan las variables en tu programa. JavaScript tiene **tipos de datos primitivos** y **tipos de datos complejos**. ¡Vamos a explorarlos! 🎉

### 1️⃣ Tipos de Datos Primitivos

Los tipos de datos primitivos son los más básicos y no tienen métodos ni propiedades. Estos incluyen:

#### 🔹 `string` (Cadenas de texto)

Las cadenas son secuencias de caracteres, y se definen entre comillas simples (`' '`) o dobles (`" "`).

**Ejemplo:**

```javascript
let nombre = "JavaScript"; // String
console.log(nombre); // Output: JavaScript
```

#### 🔹 `number` (Números)

En JavaScript, todos los números (enteros y decimales) son del mismo tipo: `number`.

**Ejemplo:**

```javascript
let edad = 30; // Entero
let precio = 19.99; // Decimal
console.log(edad, precio); // Output: 30 19.99
```

#### 🔹 `boolean` (Booleanos)

Un booleano solo puede tener dos valores: `true` (verdadero) o `false` (falso).

**Ejemplo:**

```javascript
let esMayor = true;
let esMenor = false;
console.log(esMayor); // Output: true
```

#### 🔹 `undefined`

Una variable sin un valor asignado automáticamente tiene el tipo `undefined`.

**Ejemplo:**

```javascript
let sinDefinir;
console.log(sinDefinir); // Output: undefined
```

#### 🔹 `null`

`null` representa la ausencia intencionada de cualquier valor.

**Ejemplo:**

```javascript
let vacio = null;
console.log(vacio); // Output: null
```

#### 🔹 `symbol` (Símbolos)

Los `symbol` son valores únicos e inmutables, útiles para identificar propiedades de objetos.

**Ejemplo:**

```javascript
let simbolo1 = Symbol("miSimbolo");
console.log(simbolo1); // Output: Symbol(miSimbolo)
```

#### 🔹 `bigint` (Números Grandes)

`bigint` permite manejar números enteros extremadamente grandes, más allá del límite de `number`.

**Ejemplo:**

```javascript
let numeroGrande = 1234567890123456789012345678901234567890n; // Usa 'n' al final
console.log(numeroGrande); // Output: 1234567890123456789012345678901234567890n
```

### 2️⃣ Tipos de Datos Complejos (Objetos)

Los **objetos** son colecciones de pares clave-valor y pueden contener múltiples tipos de datos, incluso otros objetos.

#### 🔹 `Object`

Un objeto es una colección de datos y funciones relacionadas.

**Ejemplo:**

```javascript
let persona = {
  nombre: "Ana",
  edad: 28,
  esProgramador: true,
};

console.log(persona); // Output: { nombre: 'Ana', edad: 28, esProgramador: true }
```

#### 🔹 `Array` (Arreglos)

Un array es un tipo especial de objeto que almacena valores en forma de lista ordenada.

**Ejemplo:**

```javascript
let colores = ["rojo", "verde", "azul"];
console.log(colores); // Output: [ 'rojo', 'verde', 'azul' ]
```

### 🛠️ Conversión de Tipos de Datos

La **conversión de tipos** (type casting) es el proceso de cambiar un tipo de dato a otro. Esto es útil cuando necesitas manipular datos de diferentes formas en tu programa.

### 1️⃣ Conversión de Números a Cadenas (`number` ➡️ `string`)

Para convertir un número a una cadena, puedes usar `String()` o el método `.toString()`.

**Ejemplo:**

```javascript
let numero = 123;
let cadenaNumero = String(numero); // Conversión usando String()
let cadenaNumero2 = numero.toString(); // Conversión usando .toString()
console.log(cadenaNumero, cadenaNumero2); // Output: "123" "123"
```

### 2️⃣ Conversión de Cadenas a Números (`string` ➡️ `number`)

Para convertir una cadena a un número, usa `Number()`, `parseInt()`, o `parseFloat()`.

**Ejemplo:**

```javascript
let cadena = "456";
let numeroEntero = Number(cadena); // Conversión a número
let numeroEntero2 = parseInt(cadena); // Conversión a número entero
let numeroDecimal = parseFloat("456.78"); // Conversión a número decimal
console.log(numeroEntero, numeroEntero2, numeroDecimal); // Output: 456 456 456.78
```

### 3️⃣ Conversión a Booleanos (`boolean`)

Puedes convertir otros tipos a `boolean` usando `Boolean()`.

**Ejemplo:**

```javascript
let valor = 1; // Cualquier número distinto de 0 es true
let cadenaVacia = ""; // Cadenas vacías son false
console.log(Boolean(valor)); // Output: true
console.log(Boolean(cadenaVacia)); // Output: false
```

### 4️⃣ Conversión Automática (Coerción de Tipos)

JavaScript a menudo convierte tipos automáticamente en segundo plano, ¡lo que puede llevar a algunos comportamientos inesperados! ⚠️

**Ejemplo:**

```javascript
console.log("5" + 2); // Output: "52" (convierte 2 a string)
console.log("5" - 2); // Output: 3 (convierte "5" a número)
```

### 🌟 Buenas Prácticas al Trabajar con Tipos de Datos

1. **Evita Coerciones Inesperadas**: Sé explícito con las conversiones para evitar errores.
2. **Usa `===` para Comparaciones Estrictas**: Esto evita comparaciones con coerción de tipo, asegurando que tanto el tipo como el valor coincidan.
3. **Prefiere `Number()`, `String()` y `Boolean()`** para conversiones claras y predecibles.
4. **Verifica Tipos con `typeof`**: Usa `typeof` para asegurarte del tipo de una variable antes de manipularla.

```javascript
let valor = "123";
console.log(typeof valor); // Output: string
```

---

¡Y eso es todo sobre los tipos de datos y la conversión de tipos en JavaScript! Ahora tienes el conocimiento para manipular y cambiar tipos de datos como un profesional. ¡Asegúrate de usar estas herramientas sabiamente para evitar errores inesperados en tu código! 🎯✨
