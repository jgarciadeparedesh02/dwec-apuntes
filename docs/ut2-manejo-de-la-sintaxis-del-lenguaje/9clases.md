# Clases y Objetos en JavaScript

### 🧑‍💻 ¿Qué son las Clases en JavaScript?

Las **clases** en JavaScript son plantillas para crear objetos que encapsulan datos y comportamientos. Introducidas en ECMAScript 6 (ES6), las clases hacen que la programación orientada a objetos sea más intuitiva y fácil de implementar.

```javascript
// Definición de una clase simple
class Persona {
    constructor(nombre, edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    // Método de la clase
    saludar() {
        console.log(`¡Hola! Me llamo ${this.nombre} y tengo ${this.edad} años.`);
    }
}

// Crear un objeto (instancia) de la clase
const persona1 = new Persona('Carlos', 30);
persona1.saludar(); // Output: ¡Hola! Me llamo Carlos y tengo 30 años.
```

### 🏗️ Componentes de una Clase

1. **Constructor**: Es un método especial para inicializar los objetos creados con la clase. Se ejecuta automáticamente al crear una nueva instancia.

    ```javascript
    class Animal {
        constructor(nombre) {
            this.nombre = nombre; // Propiedad del objeto
        }
    }
    
    const perro = new Animal('Rex');
    console.log(perro.nombre); // Output: Rex
    ```

2. **Propiedades**: Son las variables definidas dentro de la clase y se asignan dentro del constructor.

3. **Métodos**: Son funciones asociadas a los objetos creados por la clase. Pueden realizar acciones o manipular las propiedades del objeto.

    ```javascript
    class Coche {
        constructor(marca, modelo) {
            this.marca = marca;
            this.modelo = modelo;
        }
        
        detalles() {
            return `Este coche es un ${this.marca} ${this.modelo}.`;
        }
    }

    const miCoche = new Coche('Toyota', 'Corolla');
    console.log(miCoche.detalles()); // Output: Este coche es un Toyota Corolla.
    ```

### 🧩 Objetos en JavaScript

Los **objetos** son instancias de las clases, representando entidades del mundo real con propiedades (atributos) y métodos (funcionalidades).

```javascript
// Definición de un objeto usando una clase
const gato = new Animal('Miau');
console.log(gato.nombre); // Output: Miau
```

### 📚 Herencia en Clases

La **herencia** permite crear nuevas clases basadas en clases existentes, reutilizando código y agregando nuevas funcionalidades. Para ello, se utiliza la palabra clave `extends`.

```javascript
// Clase base
class Vehiculo {
    constructor(marca) {
        this.marca = marca;
    }

    mostrarMarca() {
        console.log(`Vehículo de marca: ${this.marca}`);
    }
}

// Clase derivada
class Moto extends Vehiculo {
    constructor(marca, tipo) {
        super(marca); // Llama al constructor de la clase padre
        this.tipo = tipo;
    }

    mostrarTipo() {
        console.log(`Esta moto es de tipo: ${this.tipo}`);
    }
}

const miMoto = new Moto('Honda', 'Deportiva');
miMoto.mostrarMarca(); // Output: Vehículo de marca: Honda
miMoto.mostrarTipo(); // Output: Esta moto es de tipo: Deportiva
```

### 🛠️ Encapsulamiento y Métodos Privados

El encapsulamiento permite controlar el acceso a los datos de un objeto. En JavaScript, se puede utilizar el símbolo `#` para definir propiedades y métodos privados.

```javascript
class CuentaBancaria {
    #saldo = 0; // Propiedad privada

    depositar(cantidad) {
        this.#saldo += cantidad;
        console.log(`Depósito exitoso. Saldo actual: ${this.#saldo}`);
    }

    retirar(cantidad) {
        if (cantidad <= this.#saldo) {
            this.#saldo -= cantidad;
            console.log(`Retiro exitoso. Saldo actual: ${this.#saldo}`);
        } else {
            console.log('Saldo insuficiente.');
        }
    }
}

const miCuenta = new CuentaBancaria();
miCuenta.depositar(100); // Output: Depósito exitoso. Saldo actual: 100
miCuenta.retirar(50);    // Output: Retiro exitoso. Saldo actual: 50
// miCuenta.#saldo;       // Error: No se puede acceder a una propiedad privada
```

### 🎨 Polimorfismo: Flexibilidad en la Orientación a Objetos

El **polimorfismo** permite que las clases hijas redefinan métodos de la clase padre. Esto hace que el comportamiento de los métodos cambie dependiendo del objeto que los invoque.

```javascript
class Animal {
    hacerSonido() {
        console.log('El animal hace un sonido.');
    }
}

class Perro extends Animal {
    hacerSonido() {
        console.log('El perro ladra: ¡Guau!');
    }
}

const animal = new Animal();
const perro = new Perro();

animal.hacerSonido(); // Output: El animal hace un sonido.
perro.hacerSonido();  // Output: El perro ladra: ¡Guau!
```