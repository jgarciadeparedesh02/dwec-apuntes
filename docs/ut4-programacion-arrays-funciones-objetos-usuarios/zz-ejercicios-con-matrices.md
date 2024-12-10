# 📝 **Enunciado: Simulador de Movimiento en una Matriz con Visualización en una Página Web**

---

## **Descripción del Proyecto**

Desarrolla una aplicación web que permita simular el movimiento de un objeto dentro de una matriz cuadrada. El objetivo es que el usuario pueda visualizar cómo el objeto se desplaza dentro de la matriz siguiendo una serie de instrucciones proporcionadas. La aplicación debe estar construida utilizando **HTML**, **CSS**, y **JavaScript**.

---

## **Requisitos Funcionales**

1. **Creación de la Matriz**:
   - La matriz debe ser de tamaño `5 x 5`.
   - Todas las celdas deben estar vacías inicialmente, excepto una celda que contendrá el objeto representado por una letra o símbolo (por ejemplo, `"O"`).
   - La posición inicial del objeto será la celda central (fila 2, columna 2).

2. **Interfaz de Usuario**:
   - Un campo de texto donde el usuario pueda introducir una secuencia de movimientos usando las siguientes letras:
     - **`U`**: Mover hacia arriba (Up).
     - **`D`**: Mover hacia abajo (Down).
     - **`L`**: Mover hacia la izquierda (Left).
     - **`R`**: Mover hacia la derecha (Right).
   - Un botón para ejecutar los movimientos.
   - Un botón para reiniciar la simulación y restaurar la posición inicial del objeto.

3. **Lógica del Movimiento**:
   - El objeto se moverá por la matriz siguiendo la secuencia de instrucciones ingresadas por el usuario.
   - El objeto **no debe salir de los límites** de la matriz (los movimientos que excedan los bordes deben ser ignorados).
   - Se debe visualizar claramente el camino recorrido por el objeto.

4. **Visualización Clara**:
   - La matriz debe mostrarse visualmente en la página web.
   - La posición actual del objeto debe destacarse con un color específico.
   - Las celdas por las que el objeto ha pasado deben marcarse con un símbolo o color diferente para representar el camino recorrido.

5. **Estilos y Diseño**:
   - Utilizar **CSS** para dar un diseño limpio y moderno a la interfaz.
   - Los elementos de control (campo de texto y botones) deben estar bien organizados.
   - La matriz debe estar bien delimitada y las celdas deben ser claramente visibles.

---

## **Ejemplo de Uso**

1. El usuario abre la aplicación y ve una matriz `5 x 5` con el objeto en la posición central.
2. El usuario introduce la secuencia de movimientos: `UURDLL`.
3. Al hacer clic en el botón **"Mover"**, el objeto se desplaza por la matriz siguiendo la secuencia y el camino recorrido se visualiza claramente.
4. El usuario puede hacer clic en el botón **"Reiniciar"** para restablecer la posición inicial y borrar el camino recorrido.

