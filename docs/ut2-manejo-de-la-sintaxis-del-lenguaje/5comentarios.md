# 📝 Comentarios en el Código JavaScript

Los **comentarios** en JavaScript son líneas de texto que el navegador ignora al ejecutar el código. Son herramientas esenciales para describir qué hace el código, dejar notas para otros desarrolladores (o para ti mismo en el futuro), y desactivar partes del código temporalmente. ¡Vamos a ver cómo y cuándo usar los comentarios! 🧐

### 1️⃣ ¿Por qué Usar Comentarios? 🤔

Los comentarios ayudan a:

- **Explicar la lógica** detrás de fragmentos de código.
- **Anotar ideas** para mejorar o cambiar el código más adelante.
- **Desactivar partes del código temporalmente** sin borrarlas.
- **Facilitar la colaboración** en equipo, haciendo que el código sea más legible para otros desarrolladores.

### 2️⃣ Tipos de Comentarios en JavaScript

JavaScript admite dos tipos de comentarios: **Comentarios de una sola línea** y **Comentarios de varias líneas**.

#### 🔹 Comentarios de Una Sola Línea (`//`)

Se usan para comentarios cortos o para explicar una sola línea de código. Se añaden al comienzo de la línea y todo lo que sigue después de `//` es ignorado por JavaScript.

**Ejemplo:**

```javascript
// Este es un comentario de una sola línea
let nombre = "Carlos"; // Declara una variable con el nombre "Carlos"
console.log(nombre); // Muestra "Carlos" en la consola
```

#### 🔹 Comentarios de Varias Líneas (`/* */`)

Son útiles para comentarios más largos o para descripciones detalladas. Todo lo que se encuentra entre `/*` y `*/` es ignorado por JavaScript.

**Ejemplo:**

```javascript
/*
  Esta función calcula la suma de dos números.
  Parámetros:
  - a: Primer número
  - b: Segundo número
  Retorna: La suma de a y b
*/
function sumar(a, b) {
  return a + b;
}

console.log(sumar(10, 5)); // Output: 15
```

### 3️⃣ Usos Comunes de los Comentarios 🛠️

#### 🔹 Explicar la Lógica Compleja

Usa comentarios para explicar la lógica detrás de fragmentos de código complejos. Esto ayuda a otros (¡y a ti mismo!) a entender el propósito de un bloque de código.

**Ejemplo:**

```javascript
// Comprobamos si el número es primo
function esPrimo(numero) {
  if (numero <= 1) return false; // Los números menores o iguales a 1 no son primos
  for (let i = 2; i < numero; i++) {
    if (numero % i === 0) return false; // Si es divisible por otro número, no es primo
  }
  return true; // Si pasa todas las pruebas, es primo
}

console.log(esPrimo(7)); // Output: true
```

#### 🔹 Desactivar Código Temporalmente

Puedes usar comentarios para desactivar código sin eliminarlo, lo cual es útil para probar o depurar sin perder líneas de código.

**Ejemplo:**

```javascript
let resultado = 0;

// Desactiva la siguiente línea mientras pruebas otra cosa
// resultado = sumar(3, 7);

// Activamos una línea alternativa para la prueba
resultado = 10 + 5;
console.log(resultado); // Output: 15
```

#### 🔹 Dejar Notas o Recordatorios 📌

Los comentarios también son un excelente lugar para dejar notas sobre mejoras futuras, arreglos necesarios, o cualquier cosa que debas recordar.

**Ejemplo:**

```javascript
// TODO: Mejorar la eficiencia de este bucle
for (let i = 0; i < 100; i++) {
  console.log(i);
}
```

### 4️⃣ Buenas Prácticas al Usar Comentarios 🌟

1. **Sé Claro y Conciso**: Los comentarios deben explicar el "por qué" y el "cómo" del código de manera clara y breve.
2. **No Comentes lo Obvio**: No es necesario comentar cosas evidentes como `let x = 10; // Asigna 10 a x`. Mejor explica la lógica.
3. **Actualiza los Comentarios**: Si cambias el código, asegúrate de actualizar los comentarios para que sigan siendo precisos.
4. **Usa Comentarios para Planificar**: Al comenzar a escribir código, usa comentarios para estructurar tu lógica y pasos a seguir.

**Ejemplo de Planificación con Comentarios:**

```javascript
// 1. Solicitar el nombre del usuario
// 2. Saludar al usuario por su nombre
// 3. Mostrar la fecha actual

// Paso 1
let nombreUsuario = prompt("¿Cuál es tu nombre?");

// Paso 2
console.log(`Hola, ${nombreUsuario}! 👋`);

// Paso 3
let fechaActual = new Date();
console.log(`Hoy es: ${fechaActual.toDateString()}`);
```

### 5️⃣ Comentarios en el Código Limpio ✨

Mantener comentarios relevantes y actualizados es clave para un código limpio y profesional. Usa los comentarios para agregar valor, no para llenar líneas innecesariamente.

**Ejemplo de Código Limpio con Comentarios Útiles:**

```javascript
// Genera un número aleatorio entre un rango dado
function numeroAleatorio(min, max) {
  // Math.random() genera un número entre 0 y 1, que escalamos y ajustamos al rango
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(numeroAleatorio(1, 10)); // Output: Un número entre 1 y 10
```

---

Los comentarios son una parte fundamental del desarrollo de software, especialmente cuando trabajas en equipo o vuelves a revisar tu propio código después de un tiempo. Usa los comentarios para guiar, explicar, y documentar tu código de manera efectiva. ¡Con estos consejos, tendrás un código claro y fácil de mantener! ✍️🧑‍💻
