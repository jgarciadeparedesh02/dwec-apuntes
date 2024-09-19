# 🧮 Operadores en JavaScript

Los **operadores** en JavaScript son símbolos especiales que realizan operaciones sobre datos. Son como herramientas mágicas que nos permiten **sumar, restar, comparar, asignar, y mucho más**. ¡Explorémoslos uno a uno! ✨

### 1️⃣ Operadores Aritméticos 🧮

Los **operadores aritméticos** se utilizan para realizar cálculos matemáticos básicos como suma, resta, multiplicación y división.

#### 🔹 Suma (`+`)

Suma dos valores. También se usa para concatenar cadenas de texto.

**Ejemplo:**

```javascript
let a = 10;
let b = 5;
console.log(a + b); // Output: 15

let saludo = "Hola, ";
let nombre = "Mundo!";
console.log(saludo + nombre); // Output: Hola, Mundo!
```

#### 🔹 Resta (`-`)

Resta un valor de otro.

**Ejemplo:**

```javascript
let x = 20;
let y = 7;
console.log(x - y); // Output: 13
```

#### 🔹 Multiplicación (`*`)

Multiplica dos valores.

**Ejemplo:**

```javascript
let base = 4;
let altura = 5;
console.log(base * altura); // Output: 20
```

#### 🔹 División (`/`)

Divide un valor entre otro.

**Ejemplo:**

```javascript
let total = 100;
let partes = 4;
console.log(total / partes); // Output: 25
```

#### 🔹 Módulo (`%`)

Devuelve el resto de una división.

**Ejemplo:**

```javascript
let numero = 17;
let divisor = 3;
console.log(numero % divisor); // Output: 2 (el resto de 17/3)
```

#### 🔹 Exponenciación (`**`)

Eleva un número a la potencia de otro.

**Ejemplo:**

```javascript
let base = 3;
let exponente = 3;
console.log(base ** exponente); // Output: 27 (3 elevado a la 3)
```

### 2️⃣ Operadores de Comparación 🤔

Los **operadores de comparación** comparan dos valores y devuelven un booleano (`true` o `false`). ¡Perfecto para decisiones en el código!

#### 🔹 Igualdad (`==`) y Estricta Igualdad (`===`)

- `==` compara valores y convierte tipos si es necesario.
- `===` compara valores y tipos, sin conversiones automáticas.

**Ejemplo:**

```javascript
console.log(5 == "5"); // Output: true (convierte "5" a número)
console.log(5 === "5"); // Output: false (diferentes tipos: número vs. string)
```

#### 🔹 Desigualdad (`!=`) y Estricta Desigualdad (`!==`)

- `!=` verifica si los valores son diferentes.
- `!==` verifica si los valores y tipos son diferentes.

**Ejemplo:**

```javascript
console.log(10 != "10"); // Output: false (convierte "10" a número)
console.log(10 !== "10"); // Output: true (diferentes tipos)
```

#### 🔹 Mayor que (`>`) y Menor que (`<`)

Comparan si un valor es mayor o menor que otro.

**Ejemplo:**

```javascript
console.log(8 > 3); // Output: true
console.log(3 < 8); // Output: true
```

#### 🔹 Mayor o Igual (`>=`) y Menor o Igual (`<=`)

Comparan si un valor es mayor o igual, o menor o igual.

**Ejemplo:**

```javascript
console.log(5 >= 5); // Output: true
console.log(4 <= 3); // Output: false
```

### 3️⃣ Operadores Lógicos 🧠

Los **operadores lógicos** nos permiten combinar múltiples condiciones, perfectos para estructuras de control como `if` o `while`.

#### 🔹 Y Lógico (`&&`)

Devuelve `true` si **ambas condiciones** son verdaderas.

**Ejemplo:**

```javascript
let esMayor = true;
let tienePermiso = true;
console.log(esMayor && tienePermiso); // Output: true
```

#### 🔹 O Lógico (`||`)

Devuelve `true` si **una o ambas condiciones** son verdaderas.

**Ejemplo:**

```javascript
let esAdulto = false;
let tienePermisoEspecial = true;
console.log(esAdulto || tienePermisoEspecial); // Output: true
```

#### 🔹 No Lógico (`!`)

Niega el valor de una condición, invirtiéndola.

**Ejemplo:**

```javascript
let esDia = false;
console.log(!esDia); // Output: true
```

### 4️⃣ Operadores de Asignación 📥

Los **operadores de asignación** asignan valores a variables. Además del básico `=`, hay combinaciones para operaciones más avanzadas.

#### 🔹 Asignación Básica (`=`)

**Ejemplo:**

```javascript
let puntos = 100; // Asigna 100 a la variable puntos
```

#### 🔹 Combinados con Aritméticos (`+=`, `-=`, `*=`, `/=`, etc.)

**Ejemplo:**

```javascript
let score = 10;
score += 5; // Es lo mismo que score = score + 5
console.log(score); // Output: 15
```

### 5️⃣ Operador Ternario 🧐

El operador ternario (`? :`) es una forma abreviada de escribir `if...else` en una sola línea. Se usa para evaluar una condición y devolver uno de dos valores.

**Ejemplo:**

```javascript
let edad = 18;
let acceso = edad >= 18 ? "Permitido" : "Denegado";
console.log(acceso); // Output: Permitido
```

### 6️⃣ Operador de Encadenamiento Opcional (`?.`) 🚦

Este operador permite acceder a propiedades de objetos sin causar errores si alguna parte de la cadena no existe.

**Ejemplo:**

```javascript
let usuario = { nombre: "Ana", direccion: { ciudad: "Madrid" } };
console.log(usuario.direccion?.ciudad); // Output: Madrid
console.log(usuario.contacto?.telefono); // Output: undefined (no causa error)
```

### 🌟 Buenas Prácticas al Usar Operadores

1. **Prefiere `===` en lugar de `==`** para evitar conversiones inesperadas de tipos.
2. **Combina operadores lógicos con paréntesis** para asegurar claridad en condiciones complejas.
3. **Utiliza el operador ternario** para simplificar decisiones simples en tu código.
4. **Prueba el operador de encadenamiento opcional** para evitar errores al acceder a propiedades de objetos que pueden no existir.

---

Con estos operadores, tienes una caja de herramientas poderosa para manipular y comparar datos en JavaScript. ¡Úsalos sabiamente para crear código más eficiente y expresivo! ⚡🖥️
