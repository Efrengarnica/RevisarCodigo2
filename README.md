# Formulario de Invitados

En esta App, mediante un formulario, se van agregando invitados a una lista. A continuación, se explica brevemente su funcionamiento y los métodos utilizados:

1. **Selección del Formulario**: Se selecciona el formulario usando `document.querySelector`.

2. **Manejo del Evento `submit`**: 
   - Se previene el comportamiento por defecto con `event.preventDefault()`.
   - Se obtienen los valores de los campos de entrada usando `formulario.elements`.

3. **Validación de Datos**:
   - Se verifica que el nombre no esté vacío y que la edad esté entre 18 y 120 años.
   - Se añaden clases de error con `classList.add` si los datos no son válidos.

4. **Agregar Invitado**:
   - Si los datos son válidos, se llama a una función para agregar el invitado.
   - Se restablece el formulario con `reset()`.

5. **Función para Agregar Invitado**:
   - Convierte la nacionalidad a su forma completa.
   - Crea elementos HTML con `createElement` y los añade al DOM con `appendChild`.
   - Añade texto a los elementos con `textContent`.
   - Obtiene el índice seleccionado con `selectedIndex` y el valor de la opción seleccionada con `options[i].value`.

6. **Eliminar Invitado**:
   - El botón de eliminar remueve al invitado del DOM usando `parentNode.remove()`.
