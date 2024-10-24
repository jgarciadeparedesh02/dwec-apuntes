Aquí tienes una serie de tareas prácticas para que los estudiantes trabajen con cookies en un entorno de desarrollo web. Las tareas están orientadas a entender cómo crear, leer, actualizar y eliminar cookies, así como a utilizar su contenido para mejorar la experiencia del usuario.

### Serie de tareas sobre cookies:

#### **Tarea 1: Crear una cookie de bienvenida**

**Objetivo:** Familiarizarse con la creación y escritura de cookies.

1. **Descripción:**

   - Crea una página web que, al ser visitada por primera vez, almacene una cookie que indique la fecha y la hora de la visita.
   - Muestra un mensaje de bienvenida en la página que diga: "¡Bienvenido a nuestra página! Primera visita: [fecha y hora]".

2. **Instrucciones:**
   - Utiliza `document.cookie` para crear una cookie con el valor de la fecha y la hora actual.
   - Guarda la cookie con una duración de 7 días.

---

#### **Tarea 2: Leer y mostrar las cookies**

**Objetivo:** Aprender a leer cookies desde JavaScript.

1. **Descripción:**

   - Modifica la tarea anterior para que, si el usuario vuelve a visitar la página, se muestre un mensaje personalizado que diga: "¡Bienvenido de nuevo! Última visita: [fecha y hora de la última visita]".
   - Actualiza la cookie cada vez que el usuario vuelva a visitar la página.

2. **Instrucciones:**
   - Lee las cookies almacenadas utilizando `document.cookie`.
   - Usa funciones para extraer la información de la cookie y mostrarla en la página.
   - Actualiza la cookie cada vez que el usuario accede, almacenando la nueva fecha y hora.

---

#### **Tarea 3: Crear una cookie con preferencias del usuario**

**Objetivo:** Almacenar preferencias de usuario en cookies.

1. **Descripción:**

   - Crea una página que permita al usuario elegir entre dos temas de colores (ej. claro y oscuro).
   - Guarda la elección del usuario en una cookie y aplica el tema seleccionado la próxima vez que el usuario visite la página.

2. **Instrucciones:**
   - Utiliza una cookie para guardar la preferencia de tema (ej. `tema=oscuro`).
   - Cuando el usuario cambie el tema, guarda la nueva preferencia en la cookie.
   - Cada vez que el usuario visita la página, lee la cookie y aplica el tema correcto.

---

#### **Tarea 4: Expiración de cookies**

**Objetivo:** Trabajar con la expiración y la eliminación de cookies.

1. **Descripción:**

   - Crea una página con una cuenta regresiva que expire en 1 minuto. Al expirar, muestra un mensaje indicando que la sesión ha caducado.
   - Usa una cookie con una expiración de 1 minuto para gestionar la sesión.

2. **Instrucciones:**
   - Crea una cookie con la fecha y hora de expiración 1 minuto después de que el usuario acceda.
   - Si la cookie ha caducado, muestra un mensaje como: "Sesión caducada. Por favor, recarga la página".
   - Permite al usuario eliminar manualmente la cookie con un botón.

---

#### **Tarea 5: Almacenar y eliminar cookies de login**

**Objetivo:** Crear un sistema de login simple utilizando cookies.

1. **Descripción:**

   - Implementa un formulario de login simple en el que el usuario ingrese su nombre de usuario.
   - Al hacer login, guarda el nombre de usuario en una cookie con una duración de 24 horas.
   - Muestra el nombre del usuario en la página después de hacer login.
   - Incluye un botón de logout que borre la cookie y redirija al usuario a la página de login.

2. **Instrucciones:**
   - Almacena el nombre de usuario en una cookie usando `document.cookie`.
   - Al recargar la página, verifica si la cookie del usuario existe y, si es así, muestra su nombre.
   - Crea un botón de logout que borre la cookie (`document.cookie = "usuario=; expires=Thu, 01 Jan 1970 00:00:00 UTC;"`).

---

#### **Tarea 6: Seguridad en cookies (opcional)**

**Objetivo:** Introducir conceptos de seguridad con cookies.

1. **Descripción:**

   - Investiga cómo proteger cookies usando la bandera `HttpOnly` (solo desde el servidor) y `Secure` (solo en conexiones HTTPS).
   - Discute los riesgos de las cookies que no son seguras y cómo mitigar ataques como el robo de sesiones.

2. **Instrucciones:**
   - En esta tarea, los alumnos investigarán cómo estos parámetros pueden ser configurados desde el servidor, discutiendo la relevancia de estos conceptos en aplicaciones reales.
   - No es necesario implementar estos cambios en el código, sino discutir su importancia.

---

Estas tareas permitirán a los estudiantes aprender gradualmente cómo trabajar con cookies y aplicar este conocimiento en escenarios que simulan el uso en aplicaciones reales, como personalización de temas, manejo de sesiones y almacenamiento de preferencias.
