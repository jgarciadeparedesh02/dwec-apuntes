# Interacción con el Navegador: Objetos Predefinidos Asociados

JavaScript nos permite una interacción rica con el navegador gracias a **objetos predefinidos**. Estos objetos nos permiten manipular el entorno del navegador, controlar ventanas emergentes, gestionar la navegación y mucho más. A continuación, exploramos los principales objetos y métodos que podemos utilizar.

## 🌟 **1. `window`: El Contenedor Global del Navegador**

El objeto `window` es el contenedor global donde se ejecuta todo el código JavaScript en el navegador. Nos da acceso a funcionalidades como la apertura de nuevas ventanas, la interacción con el usuario y la manipulación del estado de la ventana actual.

### 🖼️ **Control de Ventanas con `window`**

#### 1. **Abrir una nueva ventana**: `window.open()`

Este método permite abrir una nueva ventana o pestaña en el navegador.

```javascript
window.open('https://www.ejemplo.com', '_blank', 'width=600,height=400');
```

Parámetros:

- **URL**: La dirección que se abrirá.
- **Target**: El destino (`_blank` abre una nueva pestaña, `_self` abre en la pestaña actual).
- **Características**: Como el tamaño de la ventana, barras de desplazamiento, etc.

#### 2. **Cerrar la ventana actual**: `window.close()`

Permite cerrar la ventana o pestaña actual, o bien una ventana abierta previamente por `window.open()`.

```javascript
window.close();
```

> ⚠️ Este método solo funciona en ventanas que fueron abiertas por `window.open()` y puede estar restringido por algunos navegadores por razones de seguridad.

#### 3. **Mover la ventana**: `window.moveTo()`

Este método permite mover la ventana a una nueva posición en la pantalla, definiendo las coordenadas X e Y.

```javascript
window.moveTo(100, 150); // Mueve la ventana a la posición (100, 150) en la pantalla
```

#### 4. **Cambiar el tamaño de la ventana**: `window.resizeTo()`

Permite ajustar el tamaño de la ventana del navegador a un valor específico de ancho y alto.

```javascript
window.resizeTo(800, 600); // Cambia el tamaño de la ventana a 800px de ancho y 600px de alto
```

### 🔔 **Interacción con el Usuario: Alertas, Confirmaciones y Prompts**

#### 1. **Mostrar una alerta**: `window.alert()`

Muestra un cuadro de alerta simple con un mensaje. El usuario debe cerrarlo para continuar.

```javascript
window.alert('Este es un mensaje de alerta.');
```

Es ideal para mostrar mensajes informativos rápidos, aunque su uso frecuente puede ser molesto para los usuarios.

#### 2. **Solicitar confirmación**: `window.confirm()`

Este método muestra un cuadro de diálogo con un mensaje y botones de confirmación ("Aceptar" o "Cancelar"). Retorna `true` si el usuario presiona "Aceptar" y `false` si presiona "Cancelar".

```javascript
let decision = window.confirm('¿Estás seguro de que deseas continuar?');
if (decision) {
  console.log('El usuario aceptó');
} else {
  console.log('El usuario canceló');
}
```

Útil cuando necesitas que el usuario confirme una acción importante, como eliminar un archivo.

#### 3. **Solicitar entrada del usuario**: `window.prompt()`

Este método muestra un cuadro de diálogo que solicita al usuario una entrada de texto. Retorna el texto ingresado o `null` si el usuario cancela la operación.

```javascript
let nombre = window.prompt('¿Cuál es tu nombre?', 'Nombre por defecto');
console.log('El nombre ingresado es: ' + nombre);
```

Puedes usarlo para recolectar datos rápidos, aunque es preferible usar formularios HTML para entradas más complejas.

---

## 🏗️ **2. `document`: Manipulando el DOM**

El objeto `document` nos proporciona una interfaz para manipular la estructura del DOM (Document Object Model), que es esencialmente la estructura de la página web. Podemos seleccionar, crear y modificar elementos HTML directamente desde JavaScript.

```javascript
// Cambiar el contenido de un elemento con ID "titulo"
document.getElementById('titulo').innerText = '¡Hola, Mundo!';
```

### Métodos clave del objeto `document`:

- **`getElementById()`**: Selecciona un elemento por su ID.
- **`querySelector()`**: Selecciona el primer elemento que coincida con un selector CSS.
- **`createElement()`**: Crea un nuevo elemento HTML.

```javascript
// Crear un nuevo párrafo y añadirlo al cuerpo
let parrafo = document.createElement('p');
parrafo.innerText = 'Este es un nuevo párrafo.';
document.body.appendChild(parrafo);
```

---

## 🔄 **3. `navigator`: Información sobre el Navegador**

El objeto `navigator` proporciona información sobre el navegador y el dispositivo que está utilizando el usuario, como la geolocalización, si está en línea y su idioma preferido.

```javascript
console.log(navigator.userAgent); // Información sobre el navegador y el sistema
```

### Propiedades clave de `navigator`:

- **`navigator.geolocation`**: Acceso a la geolocalización del dispositivo.
- **`navigator.onLine`**: Saber si el usuario tiene conexión a Internet.
- **`navigator.language`**: El idioma preferido del navegador.

```javascript
if (navigator.onLine) {
  console.log("Conexión a Internet disponible.");
} else {
  console.log("Estás desconectado.");
}
```

---

## ⏳ **4. `history`: Control del Historial de Navegación**

El objeto `history` permite navegar hacia adelante o hacia atrás en el historial del navegador, sin necesidad de recargar la página. También puedes manipular el historial para gestionar aplicaciones SPA (Single Page Applications).

```javascript
history.back();  // Regresar a la página anterior
history.forward();  // Avanzar a la siguiente página
```

También puedes añadir estados personalizados al historial mediante:

```javascript
history.pushState({ page: 2 }, 'Título', '/pagina2');
```

---

## 🌍 **5. `location`: Manipulación de la URL**

El objeto `location` permite trabajar con la URL de la página actual. Puedes cambiar la URL, redirigir al usuario o recargar la página sin necesidad de recargar todo el documento.

```javascript
console.log(location.href);  // URL completa actual
location.reload();  // Recargar la página
```

---

## 🚀 **Conclusión**

Los objetos predefinidos como `window`, `document`, `navigator`, `history` y `location` en JavaScript ofrecen una rica interfaz para interactuar con el navegador y el DOM. Estos métodos te permiten controlar las ventanas, interactuar con los usuarios mediante cuadros de diálogo y gestionar el historial de navegación de manera efectiva. ¡Con estas herramientas, puedes crear experiencias de usuario más dinámicas e interactivas!

