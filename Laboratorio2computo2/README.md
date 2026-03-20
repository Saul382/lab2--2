Saul Antonio Amaya Umanzor 
Francisco Javier Hernandez Aguirre

1. ¿Qué es Vue.js y cuál es su función dentro de la página web desarrollada?
Vue.js es un framework de JavaScript progresivo diseñado para construir interfaces de usuario de forma sencilla y eficiente. En mi aplicación, su función principal es actuar como el motor de reactividad. Esto permite que la página se actualice automáticamente cada vez que el usuario agrega o elimina un videojuego de la lista, sin necesidad de recargar el navegador, logrando una experiencia de usuario más fluida y moderna.

2. Descripción de las variables reactivas utilizadas
En el sistema implementé 5 variables reactivas que gestionan el estado de la aplicación:

listaJuegos (Array): Almacena el listado de objetos (videojuegos) que el usuario va registrando.

nuevoJuego (Object): Captura en tiempo real los datos (nombre y plataforma) que el usuario escribe en el formulario.

mensajeError (String): Guarda el texto de las validaciones para informar al usuario si intenta ingresar datos incorrectos.

filtroBusqueda (String): Permite realizar búsquedas dinámicas dentro de la colección existente.

totalJuegos (Computed): Una propiedad reactiva que calcula automáticamente cuántos juegos hay registrados en total.

3. Diferencia entre las directivas v-bind y v-model
v-bind (Enlace unidireccional): Se utiliza para enlazar atributos de HTML a una expresión de Vue. Por ejemplo, la usé para cambiar dinámicamente el color del texto o clases CSS según la plataforma del juego. Los datos viajan del código hacia la vista.

v-model (Enlace bidireccional): Crea una conexión de doble vía. Si el usuario escribe en un input, la variable en el código se actualiza al instante; y si el código cambia la variable, el input muestra el nuevo valor.

4. Ejemplo de evento utilizado
Utilicé el evento @submit.prevent en el formulario de registro. Su función es capturar el envío de datos y ejecutar la lógica de guardado, evitando que la página se recargue (comportamiento por defecto del navegador), lo cual es fundamental en las aplicaciones de una sola página (SPA).

5. ¿Para qué se utilizó la directiva v-for?
La utilicé para realizar el renderizado de listas. Gracias a v-for, el programa recorre el arreglo listaJuegos y genera automáticamente una fila en la tabla de HTML por cada videojuego guardado, ahorrando código repetitivo.

6. ¿En qué situación se utilizó v-if y qué problema resuelve?
Se utilizó para el renderizado condicional en dos situaciones críticas:

Para mostrar el cuadro de mensaje de error solo cuando una validación falla.

Para mostrar un aviso de "No hay juegos registrados" cuando la lista está vacía.
Esto resuelve el problema de tener una interfaz estática o confusa, proporcionando retroalimentación visual clara al usuario.

7. Validación de datos y su importancia
La validación se realiza mediante una función lógica que comprueba si los campos de texto están vacíos o si cumplen con el formato esperado antes de permitir el guardado.
Importancia: Es vital para mantener la integridad de la información. Sin validación, el sistema podría colapsar al intentar procesar datos nulos, o la base de datos se llenaría de información basura, afectando la calidad del software.


