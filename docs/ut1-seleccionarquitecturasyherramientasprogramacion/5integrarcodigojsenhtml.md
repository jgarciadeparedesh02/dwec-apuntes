Integrar código JavaScript en un documento HTML es una práctica fundamental en el desarrollo web. JavaScript se utiliza para hacer que las páginas web sean interactivas y dinámicas. A continuación, se detalla cómo se puede integrar JavaScript en HTML, abordando los métodos más comunes y sus particularidades.

### Formas de integrar código JavaScript
#### 1. **Código JavaScript en Línea**

Puedes incluir código JavaScript directamente dentro de una etiqueta HTML usando el atributo `onclick`, `onmouseover`, o cualquier otro evento. Este método se utiliza para pequeños fragmentos de código o para manejar eventos específicos.

**Ejemplo:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript en Línea</title>
</head>
<body>
    <button onclick="alert('¡Hola, mundo!')">Haz clic en mí</button>
</body>
</html>
```

En este ejemplo, el código JavaScript `alert('¡Hola, mundo!')` se ejecutará cuando el usuario haga clic en el botón.

#### 2. **Código JavaScript Interno**

Para incluir JavaScript directamente en el archivo HTML pero en una sección separada, utiliza la etiqueta `<script>` en la sección `<head>` o al final del `<body>`. Este método es útil para scripts que son específicos de una sola página.

**Ejemplo:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Interno</title>
    <script>
        function saludar() {
            alert('¡Hola, mundo!');
        }
    </script>
</head>
<body>
    <button onclick="saludar()">Haz clic en mí</button>
</body>
</html>
```

En este caso, el script definido dentro de la etiqueta `<script>` puede ser llamado desde el HTML. Este enfoque permite que el código JavaScript sea más organizado y reutilizable dentro de la misma página.

#### 3. **Código JavaScript Externo**

Para proyectos más grandes y para mantener el código HTML más limpio, es recomendable usar archivos JavaScript externos. El código JavaScript se coloca en un archivo separado con extensión `.js`, que luego se enlaza en el HTML usando la etiqueta `<script>` con el atributo `src`.

**Ejemplo de archivo HTML (`index.html`):**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Externo</title>
    <script src="script.js" defer></script>
</head>
<body>
    <button id="myButton">Haz clic en mí</button>
</body>
</html>
```

**Ejemplo de archivo JavaScript (`script.js`):**

```javascript
document.addEventListener('DOMContentLoaded', (event) => {
    document.getElementById('myButton').addEventListener('click', () => {
        alert('¡Hola, mundo!');
    });
});
```

En este ejemplo, el archivo `script.js` contiene el código JavaScript, y se enlaza a través del atributo `src` en la etiqueta `<script>`. El atributo `defer` asegura que el script se ejecute solo después de que el documento HTML se haya cargado completamente.

#### 4. **Buenas Prácticas**

- **Separación de Responsabilidades**: Mantén el código JavaScript en archivos separados para facilitar la organización y mantenimiento.
- **Carga Diferida (`defer` y `async`)**: Utiliza los atributos `defer` o `async` en la etiqueta `<script>` para controlar la carga y ejecución del JavaScript sin bloquear la carga de la página.
  - `defer`: El script se ejecuta en el orden en que aparece en el HTML después de que el documento se haya cargado.
  - `async`: El script se descarga en paralelo con el HTML y se ejecuta tan pronto como esté disponible.
- **Evita el JavaScript en Línea**: Para proyectos más grandes, es preferible evitar el JavaScript en línea por razones de seguridad y mantenimiento.

Integrar JavaScript en HTML puede mejorar significativamente la interactividad y funcionalidad de una página web. Utilizar estos métodos y buenas prácticas ayudará a mantener tu código organizado y eficiente.


Claro, aquí tienes un ejemplo de cómo usar los atributos `async` y `defer` en la etiqueta `<script>` para controlar la carga y ejecución de scripts en un documento HTML:

### Defer y Async
#### 1. **Uso de `defer`**

El atributo `defer` se utiliza para garantizar que el script se ejecute en el orden en que aparece en el HTML, pero solo después de que el documento HTML haya sido completamente cargado. Esto es útil para scripts que **necesitan interactuar con el DOM**.

**Ejemplo con `defer`:**

**Archivo HTML (`index.html`):**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Uso de defer</title>
    <!-- Cargar el script con defer -->
    <script src="deferred-script.js" defer></script>
</head>
<body>
    <h1>Hola Mundo</h1>
    <button id="deferButton">Haz clic en mí</button>
</body>
</html>
```

**Archivo JavaScript (`deferred-script.js`):**

```javascript
document.addEventListener('DOMContentLoaded', (event) => {
    document.getElementById('deferButton').addEventListener('click', () => {
        alert('¡Botón con defer clicado!');
    });
});
```

En este ejemplo, el script `deferred-script.js` se cargará en el orden en que aparece en el HTML, pero solo después de que el documento se haya cargado completamente. Esto asegura que el botón exista en el DOM antes de que el script intente añadir un manejador de eventos.

#### 2. **Uso de `async`**

El atributo `async` se utiliza para cargar el script en paralelo con la carga del HTML y ejecutarlo tan pronto como esté disponible. Esto es útil para scripts que **no dependen del DOM** o de otros scripts y pueden ejecutarse de forma independiente.

**Ejemplo con `async`:**

***Archivo HTML (`index.html`):**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Uso de async</title>
    <!-- Cargar el script con async -->
    <script src="async-script.js" async></script>
</head>
<body>
    <h1>Hola Mundo</h1>
    <button id="asyncButton">Haz clic en mí</button>
</body>
</html>
```

**Archivo JavaScript (`async-script.js`):**

```javascript
document.addEventListener('DOMContentLoaded', (event) => {
    // Este script se ejecutará tan pronto como esté disponible
    alert('¡Script con async ejecutado!');
});
```

En este caso, el script `async-script.js` se cargará de forma asíncrona y se ejecutará tan pronto como esté disponible, sin esperar a que el documento se haya cargado completamente. Esto puede ser adecuado para scripts que no afectan a la estructura del DOM o que no dependen de otros scripts.

#### **Comparación de `async` y `defer`**


| **Atributo** | **Características**                                                                                                                                 | **Uso Ideal**                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| **`defer`**  | - Carga el script en paralelo con el HTML.<br>- Ejecuta el script en el orden en que aparece en el HTML después de que el documento se haya cargado completamente. | Ideal para scripts que interactúan con el DOM.            |
| **`async`**  | - Carga el script en paralelo con el HTML.<br>- Ejecuta el script tan pronto como esté disponible, sin esperar a que el HTML se haya cargado completamente. | Ideal para scripts independientes que no dependen del DOM ni de otros scripts. |


Utilizar `defer` y `async` correctamente puede ayudar a optimizar la carga de tu página web y mejorar la experiencia del usuario al garantizar que los scripts no bloqueen el renderizado de la página.