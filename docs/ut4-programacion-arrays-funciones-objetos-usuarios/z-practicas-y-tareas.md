### **Tareas Básicas**
1. **Crea un array de tus comidas favoritas** y:
    - Añade dos nuevas comidas al principio y al final del array.
    - Elimina la primera y última comida del array.
    - Encuentra la posición de una comida específica usando `indexOf`.

2. **Crea un array de números del 1 al 10** y:
    - Encuentra los números pares usando `filter`.
    - Duplica todos los números con `map`.
    - Calcula la suma total con `reduce`.

3. **Transforma un string en un array** usando `Array.from` o `split`:
   ```javascript
   const frase = "Aprender JavaScript es divertido";
   const palabras = frase.split(" ");
   console.log(palabras); // ["Aprender", "JavaScript", "es", "divertido"]
   ```

---

### **Tareas de Manipulación**
4. **Crea un array de colores primarios** y:
    - Inserta un nuevo color en la segunda posición usando `splice`.
    - Extrae los dos últimos colores en un nuevo array con `slice`.

5. **Combina arrays**:
    - Crea dos arrays, uno con nombres y otro con edades.
    - Usa `concat` para combinarlos en uno solo.
    - Usa `join` para convertirlos en una cadena de texto con comas.

6. **Ordena y reorganiza un array**:
    - Genera un array de números aleatorios.
    - Ordénalo en orden ascendente usando `sort`.
    - Inviértelo con `reverse`.

---

### **Tareas Avanzadas**
7. **Iteración en arrays multidimensionales**:
    - Crea una tabla (array bidimensional) con nombres de estudiantes y sus calificaciones.
    - Accede y modifica una calificación específica.
    - Usa `flat` para convertir el array bidimensional en uno unidimensional.

8. **Busca en un array de objetos**:
    - Crea un array de objetos que representen productos (nombre, precio, cantidad).
    - Encuentra el producto más caro usando `reduce`.
    - Usa `find` para buscar un producto por nombre.
    - Verifica si todos los productos tienen precio mayor a 10 con `every`.

---

### **Retos Prácticos**
9. **Simula una cola (FIFO)**:
    - Usa `push` y `shift` para agregar y eliminar elementos.
    ```javascript
    const cola = [];
    cola.push("Tarea 1");
    cola.push("Tarea 2");
    console.log(cola.shift()); // "Tarea 1"
    console.log(cola); // ["Tarea 2"]
    ```

10. **Simula una pila (LIFO)**:
    - Usa `push` y `pop` para agregar y eliminar elementos.

11. **Crea un buscador simple**:
    - Dado un array de palabras, implementa una función que busque palabras que comiencen con una letra específica usando `filter`.

12. **Genera una matriz identidad**:
    - Usa un bucle para crear un array bidimensional que represente una matriz identidad.
    ```javascript
    const matrizIdentidad = Array.from({ length: 3 }, (_, i) =>
      Array.from({ length: 3 }, (_, j) => (i === j ? 1 : 0))
    );
    console.log(matrizIdentidad);
    ```

---

### **Tareas Creativas**
13. **Crea un sistema de inventario**:
    - Usa un array para representar un inventario.
    - Implementa funciones para agregar, eliminar y buscar productos.

14. **Simula un carrito de compras**:
    - Cada producto es un objeto con nombre, precio y cantidad.
    - Calcula el precio total usando `reduce`.
    - Filtra los productos con cantidad mayor a 1.

15. **Aplana arrays**:
    - Usa un array anidado y aplanarlo con `flat` y `flatMap`.

---

### **Desafíos Divertidos**
16. **Encuentra la palabra más larga**:
    - Dado un array de palabras, encuentra la más larga usando `reduce`.

17. **Genera números únicos**:
    - Crea un array de números aleatorios únicos entre 1 y 100 usando bucles y `includes`.

18. **Análisis de texto**:
    - Convierte un texto en un array de palabras.
    - Cuenta la cantidad de palabras únicas.