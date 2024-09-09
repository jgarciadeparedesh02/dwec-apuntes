# Recursos y Preguntas Frecuentes

## Recursos

A continuación, te dejo una lista de recursos útiles para profundizar en los temas clave de este módulo:

### Entornos y herramientas de desarrollo de código en el cliente web
- **[Visual Studio Code](https://code.visualstudio.com/)**: Uno de los entornos de desarrollo más utilizados para trabajar con JavaScript y HTML.
- **[CodePen](https://codepen.io/)**: Plataforma para probar código en HTML, CSS y JavaScript en tiempo real.
  
---

## Preguntas Frecuentes (FAQ)

### 1. ¿Qué es un mecanismo de ejecución de código en un navegador web?
El mecanismo de ejecución de código se refiere a cómo los navegadores interpretan y ejecutan el código, como JavaScript, para crear interactividad en una página web. Esto incluye el proceso de descarga, análisis y ejecución de scripts.

### 2. ¿Cuáles son las limitaciones de ejecutar código en el navegador?
El código que se ejecuta en el navegador está limitado por el entorno del cliente, es decir, depende del rendimiento del dispositivo del usuario y de la compatibilidad del navegador. No puede acceder directamente a los recursos del sistema operativo por razones de seguridad.

### 3. ¿Qué lenguajes de programación se utilizan comúnmente en el entorno cliente?
JavaScript es el lenguaje más comúnmente utilizado en el lado del cliente. Además, tecnologías como HTML y CSS son fundamentales para el desarrollo web en el cliente, ya que definen la estructura y el estilo del contenido.

### 4. ¿Cuál es la diferencia entre un script en línea y un script externo?
- Un **script en línea** es el código JavaScript que se incluye directamente en el archivo HTML mediante la etiqueta `<script>`.
- Un **script externo** se aloja en un archivo separado con la extensión `.js` y se referencia en el HTML con `<script src="archivo.js"></script>`.

### 5. ¿Qué ventajas tiene utilizar frameworks como React o Angular?
Los frameworks de JavaScript como React y Angular simplifican el desarrollo de aplicaciones web complejas. Ofrecen herramientas y bibliotecas que facilitan la creación de componentes reutilizables, optimizan el rendimiento y mejoran la organización del código.

### 6. ¿Cuáles son los entornos de desarrollo más recomendados para trabajar en el cliente web?
Algunas de las mejores herramientas para el desarrollo en el cliente web son **Visual Studio Code** (un editor de código potente y con muchas extensiones) y **CodePen** (una plataforma en línea para experimentar con HTML, CSS y JavaScript).

### 7. ¿Qué es la etiqueta `defer` y cómo se utiliza en los scripts?
La etiqueta `defer` permite que el navegador descargue el script mientras continúa procesando el HTML. El script se ejecuta solo después de que el documento HTML esté completamente cargado. Esto es útil cuando tu script depende del contenido HTML.

```html
<script src="script.js" defer></script>
```

### 8. ¿Cuándo debería usar `async` en lugar de `defer`?
`async` es útil cuando el script no depende del DOM ni de otros scripts. Con `async`, el script se ejecuta tan pronto como esté disponible, sin esperar a que el HTML termine de cargarse.

```html
<script src="script.js" async></script>
```

### 9. ¿Cómo elegir la arquitectura adecuada para mi proyecto?
La elección de la arquitectura depende del tamaño y los requisitos del proyecto. Por ejemplo, una arquitectura monolítica puede ser suficiente para una aplicación pequeña, pero si el proyecto crece, podría ser mejor adoptar una arquitectura de microservicios para facilitar el mantenimiento y la escalabilidad.

### 10. ¿Qué herramientas son recomendables para probar código en el cliente?
Herramientas como **Chrome DevTools**, **Firefox Developer Tools** y plataformas como **CodePen** son muy útiles para depurar y probar tu código JavaScript en tiempo real.
