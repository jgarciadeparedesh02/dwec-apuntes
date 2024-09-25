# **Ejercicios Básicos de JavaScript - Soluciones**

#### **Nivel 1: Principiante**

1. **Declaración e Inicialización de Variables**

   **Enunciado:** Declara tres variables usando `let`, `const`, y `var`. Inicializa una con tu nombre, otra con tu edad, y otra con un booleano que indique si te gusta programar. Muestra los valores en la consola.

   ```javascript
   const readline = require('readline-sync');

   let nombre = readline.question("¿Cuál es tu nombre? ");
   const edad = parseInt(readline.question("¿Cuál es tu edad? "));
   var gustaProgramar = readline.keyInYN("¿Te gusta programar? ");

   console.log(`Nombre: ${nombre}, Edad: ${edad}, ¿Gusta Programar?: ${gustaProgramar}`);
   ```

2. **Suma de Dos Números**

   **Enunciado:** Declara dos variables `a` y `b`, asígnales valores numéricos y muestra en la consola la suma de ambos.

   ```javascript
   const readline = require('readline-sync');

   let a = parseFloat(readline.question("Introduce el primer número: "));
   let b = parseFloat(readline.question("Introduce el segundo número: "));
   console.log(`La suma es: ${a + b}`);
   ```

3. **Concatenación de Cadenas**

   **Enunciado:** Declara dos variables con tu nombre y apellido. Concáténalas para mostrar tu nombre completo en la consola.

   ```javascript
   const readline = require('readline-sync');

   let nombre = readline.question("Introduce tu nombre: ");
   let apellido = readline.question("Introduce tu apellido: ");
   console.log(`Nombre completo: ${nombre} ${apellido}`);
   ```

4. **Conversión de Tipos**

   **Enunciado:** Declara una variable con el valor `"50"`. Convierte esta variable a un número utilizando `Number()` y muestra el tipo resultante usando `typeof`.

   ```javascript
   let valor = "50";
   let numero = Number(valor);
   console.log(`Valor: ${numero}, Tipo: ${typeof numero}`);
   ```

5. **Operaciones Matemáticas Básicas**

   **Enunciado:** Declara dos variables numéricas. Realiza y muestra en la consola la suma, resta, multiplicación, y división de ambas.

   ```javascript
   const readline = require('readline-sync');

   let x = parseFloat(readline.question("Introduce el primer número: "));
   let y = parseFloat(readline.question("Introduce el segundo número: "));
   console.log(`Suma: ${x + y}`);
   console.log(`Resta: ${x - y}`);
   console.log(`Multiplicación: ${x * y}`);
   console.log(`División: ${x / y}`);
   ```

6. **Condicional Simple: Mayor o Menor**

   **Enunciado:** Pide al usuario un número y verifica si es mayor o menor que 10. Muestra un mensaje indicando el resultado.

   ```javascript
   const readline = require('readline-sync');

   let numero = parseInt(readline.question("Introduce un número: "));
   if (numero > 10) {
       console.log("El número es mayor que 10.");
   } else {
       console.log("El número es menor o igual a 10.");
   }
   ```

#### **Nivel 2: Intermedio**

7. **Determinar Par o Impar**

   **Enunciado:** Escribe un programa que pida un número al usuario y determine si es par o impar usando un condicional `if-else`.

   ```javascript
   const readline = require('readline-sync');

   let numero = parseInt(readline.question("Introduce un número: "));
   if (numero % 2 === 0) {
       console.log("El número es par.");
   } else {
       console.log("El número es impar.");
   }
   ```

8. **Contador de Números del 1 al 10**

   **Enunciado:** Usa un bucle `for` para imprimir los números del 1 al 10 en la consola.

   ```javascript
   for (let i = 1; i <= 10; i++) {
       console.log(i);
   }
   ```

9. **Calcular Factorial**

   **Enunciado:** Escribe un programa que pida un número al usuario y calcule su factorial utilizando un bucle `while`.

   ```javascript
   const readline = require('readline-sync');

   let numero = parseInt(readline.question("Introduce un número: "));
   let factorial = 1;
   while (numero > 1) {
       factorial *= numero;
       numero--;
   }
   console.log(`El factorial es: ${factorial}`);
   ```

10. **Tabla de Multiplicar**

    **Enunciado:** Pide al usuario un número y muestra su tabla de multiplicar del 1 al 10 usando un bucle `for`.

    ```javascript
    const readline = require('readline-sync');

    let numero = parseInt(readline.question("Introduce un número: "));
    for (let i = 1; i <= 10; i++) {
        console.log(`${numero} x ${i} = ${numero * i}`);
    }
    ```

11. **Contar Vocales en una Cadena**

    **Enunciado:** Solicita al usuario una cadena de texto y cuenta cuántas vocales tiene. Imprime el resultado en la consola.

    ```javascript
    const readline = require('readline-sync');

    let cadena = readline.question("Introduce una cadena: ");
    let contadorVocales = (cadena.match(/[aeiouAEIOU]/g) || []).length;
    console.log(`La cadena tiene ${contadorVocales} vocales.`);
    ```

12. **Array de Nombres**

    **Enunciado:** Declara un array con tres nombres y usa un bucle `for` para imprimir cada nombre en la consola.

    ```javascript
    let nombres = ["Ana", "Luis", "Marta"];
    for (let nombre of nombres) {
        console.log(nombre);
    }
    ```

#### **Nivel 3: Avanzado**

13. **Calculadora Básica**

    **Enunciado:** Crea un programa que pida dos números y un operador (`+`, `-`, `*`, `/`) al usuario. Realiza la operación y muestra el resultado en la consola.

    ```javascript
    const readline = require('readline-sync');

    let num1 = parseFloat(readline.question("Introduce el primer número: "));
    let num2 = parseFloat(readline.question("Introduce el segundo número: "));
    let operador = readline.question("Introduce un operador (+, -, *, /): ");

    switch (operador) {
        case "+":
            console.log(`Resultado: ${num1 + num2}`);
            break;
        case "-":
            console.log(`Resultado: ${num1 - num2}`);
            break;
        case "*":
            console.log(`Resultado: ${num1 * num2}`);
            break;
        case "/":
            console.log(`Resultado: ${num1 / num2}`);
            break;
        default:
            console.log("Operador no válido.");
    }
    ```

14. **Contador de Palabras**

    **Enunciado:** Solicita una frase al usuario y cuenta cuántas palabras tiene. Usa `split()` para separar las palabras y cuenta la longitud del array resultante.

    ```javascript
    const readline = require('readline-sync');

    let frase = readline.question("Introduce una frase: ");
    let palabras = frase.trim().split(/\s+/);
    console.log(`La frase tiene ${palabras.length} palabras.`);
    ```

15. **Invertir una Cadena**

    **Enunciado:** Escribe un programa que tome una cadena ingresada por el usuario e imprima la cadena invertida.

    ```javascript
    const readline = require('readline-sync');

    let cadena = readline.question("Introduce una cadena: ");
    let invertida = cadena.split("").reverse().join("");
    console.log(`Cadena invertida: ${invertida}`);
    ```

16. **Encuentra el Número Mayor**

    **Enunciado:** Pide tres números al usuario y determina cuál es el mayor utilizando condicionales.

    ```javascript
    const readline = require('readline-sync');

    let num1 = parseFloat(readline.question("Introduce el primer número: "));
    let num2 = parseFloat(readline.question("Introduce el segundo número: "));
    let num3 = parseFloat(readline.question("Introduce el tercer número: "));

    if (num1 >= num2 && num1 >= num3) {
        console.log(`El mayor es: ${num1}`);
    } else if (num2 >= num1 && num2 >= num3) {
        console.log(`El mayor es: ${num2}`);
    } else {
        console.log(`El mayor es: ${num3}`);
    }
    ```

17. **Número Primo**

    **Enunciado:** Pide al usuario un número y determina si es primo. Imprime un mensaje indicando si es primo o no.

    ```javascript
    const readline = require('readline-sync');

    let numero = parseInt(readline.question("Introduce un número: "));
    let esPrimo = numero > 1

;

    for (let i = 2; i <= Math.sqrt(numero); i++) {
        if (numero % i === 0) {
            esPrimo = false;
            break;
        }
    }
    console.log(esPrimo ? "Es primo." : "No es primo.");
    ```

18. **Clase Básica de Círculo**

    **Enunciado:** Crea una clase `Círculo` con un atributo `radio`. Añade un método para calcular el área del círculo. Instancia la clase y muestra el área en la consola.

    ```javascript
    class Circulo {
        constructor(radio) {
            this.radio = radio;
        }

        calcularArea() {
            return Math.PI * Math.pow(this.radio, 2);
        }
    }

    const readline = require('readline-sync');
    let radio = parseFloat(readline.question("Introduce el radio del círculo: "));
    let miCirculo = new Circulo(radio);
    console.log(`El área del círculo es: ${miCirculo.calcularArea()}`);
    ```

19. **Sistema de Notas**

    **Enunciado:** Pide al usuario su calificación y usa condicionales para determinar si aprobó o reprobó. Usa las siguientes reglas: ≥ 60 aprobado, < 60 reprobado.

    ```javascript
    const readline = require('readline-sync');

    let calificacion = parseFloat(readline.question("Introduce tu calificación: "));
    console.log(calificacion >= 60 ? "Aprobado" : "Reprobado");
    ```

20. **Gestión de Tareas (Clases y Arrays)**

    **Enunciado:** Crea una clase `Tarea` con atributos `nombre` y `completada`. Crea un array de tareas y añade métodos para agregar, completar y mostrar tareas pendientes o completadas.

    ```javascript
    class Tarea {
        constructor(nombre) {
            this.nombre = nombre;
            this.completada = false;
        }

        completar() {
            this.completada = true;
        }
    }

    const tareas = [new Tarea("Estudiar"), new Tarea("Comprar comida")];

    // Completar la primera tarea
    tareas[0].completar();

    // Mostrar todas las tareas
    tareas.forEach((tarea, index) => {
        console.log(`${index + 1}. ${tarea.nombre} - Completada: ${tarea.completada}`);
    });
    ```

#### **Nivel 4: Desafío**

21. **Generador de Contraseñas Aleatorias**

    **Enunciado:** Crea una función que genere contraseñas aleatorias de longitud `n` usando caracteres alfanuméricos. Pide al usuario la longitud de la contraseña y genera una.

    ```javascript
    const readline = require('readline-sync');

    function generarContraseña(longitud) {
        let caracteres = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";
        let contraseña = "";
        for (let i = 0; i < longitud; i++) {
            contraseña += caracteres.charAt(Math.floor(Math.random() * caracteres.length));
        }
        return contraseña;
    }

    let longitud = parseInt(readline.question("Introduce la longitud de la contraseña: "));
    console.log("Contraseña generada: " + generarContraseña(longitud));
    ```

22. **Calculadora de Edad**

    **Enunciado:** Pide al usuario su fecha de nacimiento y calcula su edad actual. Usa la clase `Date` para realizar los cálculos.

    ```javascript
    const readline = require('readline-sync');

    let fechaNacimiento = readline.question("Introduce tu fecha de nacimiento (YYYY-MM-DD): ");
    let fecha = new Date(fechaNacimiento);
    let edad = new Date().getFullYear() - fecha.getFullYear();
    console.log("Tu edad es: " + edad + " años.");
    ```

23. **Fibonacci con Bucle**

    **Enunciado:** Crea un programa que genere la secuencia de Fibonacci hasta el décimo término usando un bucle.

    ```javascript
    let a = 0, b = 1, siguiente;
    console.log(a);
    for (let i = 1; i < 10; i++) {
        console.log(b);
        siguiente = a + b;
        a = b;
        b = siguiente;
    }
    ```

24. **Ordenar Números de un Array**

    **Enunciado:** Crea un array con números desordenados y escribe un programa que los ordene de menor a mayor sin usar el método `.sort()`.

    ```javascript
    let numeros = [5, 2, 9, 1, 7];
    for (let i = 0; i < numeros.length; i++) {
        for (let j = 0; j < numeros.length - i - 1; j++) {
            if (numeros[j] > numeros[j + 1]) {
                [numeros[j], numeros[j + 1]] = [numeros[j + 1], numeros[j]];
            }
        }
    }
    console.log(numeros);
    ```

25. **Adivina el Número**

    **Enunciado:** Crea un juego donde la máquina elija un número aleatorio entre 1 y 100. El usuario debe adivinarlo con pistas como “mayor” o “menor” hasta acertar.

    ```javascript
    const readline = require('readline-sync');

    let numeroSecreto = Math.floor(Math.random() * 100) + 1;
    let adivinanza;

    while (adivinanza !== numeroSecreto) {
        adivinanza = parseInt(readline.question("Adivina el número entre 1 y 100: "));
        if (adivinanza > numeroSecreto) {
            console.log("El número es menor.");
        } else if (adivinanza < numeroSecreto) {
            console.log("El número es mayor.");
        } else {
            console.log("¡Correcto! Adivinaste el número.");
        }
    }
    ``` 