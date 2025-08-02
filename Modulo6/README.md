### **Módulo 6: Proyecto Final: Construyendo una App con Copilot como Co-piloto**

#### **Objetivo**
¡Es hora de unirlo todo! En este módulo final, construiremos un proyecto completo desde cero, aplicando todas las técnicas que hemos aprendido. Serás el piloto, y Copilot tu co-piloto.

#### **El Proyecto: Habit Tracker (Seguimiento de Hábitos)**
Crearemos una aplicación web de una sola página para hacer seguimiento de hábitos.
*   **Tecnologías**: HTML, Tailwind CSS para los estilos y JavaScript puro para la lógica.
*   **Características**:
    1.  Añadir nuevos hábitos a una lista.
    2.  Marcar un hábito como completado para el día de hoy.
    3.  Ver el estado de los hábitos (completado/pendiente).
    4.  Los datos se guardarán en `localStorage` para que persistan.
    5.  Diseño limpio y **responsivo** gracias a Tailwind CSS.

> **Consejo:** Antes de aceptar cualquier sugerencia de Copilot, revisa que las dependencias y el código propuesto coincidan con tu stack y necesidades. Si Copilot sugiere una librería o patrón que no usas, verifica si realmente lo necesitas.

---

#### **Paso 1: Configuración del Entorno**

1.  **Estructura de archivos**: Pídele al chat de Copilot: `Crea la estructura de archivos para una app web con HTML, JS y que use Tailwind CSS`. Te sugerirá `index.html`, una carpeta `src` con `styles.css` y `app.js`, y un archivo `tailwind.config.js`.
2.  **Configurar Tailwind CSS**: Este es un gran ejemplo de cómo usar Copilot para tareas de configuración. Pregúntale al chat: `dame los pasos para configurar Tailwind CSS en un proyecto simple. Necesito el script para el CDN en mi HTML y el comando para inicializar la configuración`.
    *   Copilot te dará el script para añadir al `<head>` de tu `index.html` y te explicará cómo configurar `tailwind.config.js`.

> **Tip:** Si tienes dudas sobre la configuración, pide a Copilot que te explique cada paso y compáralo con la documentación oficial de Tailwind.

---

#### **Paso 2: Creando la Interfaz con HTML y Tailwind**

1.  **Generar el HTML**: Abre `index.html`. Usa un comentario detallado para que Copilot genere la estructura.
    ```html
    <!--
      Crea la interfaz para una app de seguimiento de hábitos usando Tailwind CSS.
      Debe tener:
      1. Un contenedor principal centrado.
      2. Un título "Habit Tracker".
      3. Un formulario con un input de texto (placeholder: "Nuevo hábito...") y un botón para "Añadir".
      4. Una lista (ul) donde se mostrarán los hábitos.
      5. La UI debe ser responsiva, apilándose en pantallas pequeñas.
    -->
    ```
2.  **Refinar con Clases de Tailwind**: Acepta la sugerencia inicial de Copilot. Luego, usa el chat en línea (`Ctrl+I`) sobre elementos específicos para refinar los estilos. Selecciona el `div` principal y pide: `Añade más clases de Tailwind para que este contenedor tenga un fondo blanco, sombra, y esquinas redondeadas`.

> **Consejo:** Si la sugerencia de Copilot no es completamente responsiva o accesible, pide mejoras específicas en el prompt o solicita ejemplos de buenas prácticas de accesibilidad.

---

#### **Paso 3: La Lógica de la Aplicación con JavaScript**

Aquí es donde aplicaremos todo lo aprendido sobre generación de funciones, refactorización y pruebas.

> **Tip:** Divide la lógica en funciones pequeñas y bien documentadas. Si Copilot genera una función muy extensa, pídele que la refactorice o divida en partes más manejables.

1.  **Generar la lógica principal**: En `app.js`, usa un prompt que describa toda la funcionalidad.
    ```javascript
    // Lógica para la app de seguimiento de hábitos
    // 1. Obtener referencias a los elementos del DOM (input, botón, lista).
    // 2. El estado de los hábitos se guardará en un array de objetos. Ej: [{ id: 1, text: 'Leer 10 páginas', completed: false }]
    // 3. Función `renderHabits`: renderiza la lista de hábitos en el DOM. Cada hábito debe tener un botón para marcar/desmarcar y otro para eliminar.
    // 4. Función `addHabit`: añade un nuevo hábito al array, lo guarda en localStorage y vuelve a renderizar.
    // 5. Función `toggleHabit`: cambia el estado 'completed' de un hábito, guarda y renderiza.
    // 6. Función `deleteHabit`: elimina un hábito, guarda y renderiza.
    // 7. Función para cargar los hábitos desde localStorage al iniciar la app.
    // 8. Añadir los event listeners correspondientes.
    ```
2.  **Refactorizar y Mejorar**:
    *   Una vez generado el código, selecciona la función `renderHabits` y pide al chat: `/simplify esta función es muy larga, extrae la creación de cada elemento de hábito a una función separada 'createHabitElement'`.
3.  **Documentar y Probar**:
    *   Selecciona una de tus funciones puras (como la que añade un hábito al array de estado) y usa `/doc` para documentarla.
    *   Luego, usa `/tests` para generar pruebas unitarias con Jest, verificando que la lógica de estado funciona correctamente.

> **Advertencia:** Siempre revisa la eficiencia y seguridad del código generado, especialmente en el manejo de datos del usuario y almacenamiento local. Compara lo generado con la documentación oficial de JavaScript y buenas prácticas de seguridad.

---

#### **Conclusión del Taller**

¡Felicidades! Has construido una aplicación web funcional y moderna desde cero. Has actuado como un verdadero arquitecto de software:
*   **Diseñaste la estructura** y delegaste la implementación inicial a Copilot.
*   **Guías a la IA** con prompts claros y detallados.
*   **Refinaste y refactorizaste** el código generado.
*   **Aseguraste la calidad** con documentación y pruebas.

Este es el flujo de trabajo moderno del desarrollador asistido por IA. Ahora tienes las herramientas y la mentalidad para aplicar estas técnicas a cualquier proyecto, sin importar su complejidad.

---

### Buenas Prácticas y Limitaciones

- Copilot es más robusto en tecnologías populares (JavaScript, HTML, CSS) y puede ser menos preciso en stacks menos comunes.
- Si la sugerencia es extensa o compleja, pide a Copilot que divida el código en funciones pequeñas y bien documentadas.
- Si Copilot sugiere recursos externos (APIs, dependencias), revisa su validez y licenciamiento.
- No asumas que todo lo generado es óptimo: revisa, prueba y refina cada parte.
- Si tienes dudas, consulta la documentación oficial de las tecnologías usadas.
