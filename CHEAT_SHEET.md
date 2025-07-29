# GitHub Copilot: La Guía Definitiva (Cheat Sheet)

Esta guía es tu recurso central para dominar GitHub Copilot. El secreto no es memorizar comandos, sino entender el **flujo de trabajo** y cómo **darle a Copilot el contexto correcto** para cada tarea.

---

### Principios Fundamentales: Cómo Evitar que Copilot "Alucine"

Copilot da malas sugerencias cuando le falta contexto. Tu misión es dárselo. La calidad de tu entrada (prompt) determina la calidad de su salida.

1.  **Contexto Implícito**: Copilot siempre considera el archivo que tienes abierto y, a menudo, otros archivos abiertos de la misma carpeta.
2.  **Contexto Explícito (¡La Clave!)**: Usa las herramientas del chat para decirle a Copilot **exactamente** dónde mirar y con quién hablar.

---

### Los 3 Pilares del Chat de Copilot

Domina estos tres conceptos y dominarás el chat.

| Tipo | Prefijo | Propósito | Ejemplo |
| :--- | :--- | :--- | :--- |
| **Participantes** | `@` | **A quién le preguntas.** Elige al "experto" para tu tarea. | `@workspace`, `@vscode`, `@terminal` |
| **Variables** | `#` | **Sobre qué le preguntas.** Especifica archivos, carpetas o código. | `#file`, `#selection`, `#path` |
| **Comandos** | `/` | **Qué quieres que haga.** Acciones rápidas para tareas comunes. | `/fix`, `/explain`, `/tests` |

---

### Escenarios Prácticos: Aplicando los 3 Pilares

#### Escenario 1: Onboarding y Entender Código Ajeno

*   **Tu Meta**: Entender rápidamente un archivo o proyecto nuevo.
*   **Tu Herramienta Principal**: `@workspace /explain`

| Tarea | Prompt de Ejemplo en el Chat |
| :--- | :--- |
| **Entender un archivo completo** | `@workspace /explain #file:src/api/auth.js` |
| **Entender una función específica** | *Selecciona la función en el editor*, luego abre el chat (`Cmd+I`) y escribe: `/explain` |
| **Entender la arquitectura general** | `@workspace /explain ¿Cuál es la estructura de este proyecto? ¿Qué patrón de diseño utiliza?` |
| **Aclarar una expresión regular** | *Selecciona la regex*, luego: `/explain ¿Qué hace esta regex y qué significa cada parte?` |

#### Escenario 2: Escribir Código Nuevo

*   **Tu Meta**: Generar código desde cero, desde fragmentos hasta archivos completos.
*   **Tus Herramientas**: Comentarios descriptivos y el comando `/new`.

| Tarea | Prompt de Ejemplo en el Chat |
| :--- | :--- |
| **Crear un nuevo proyecto (Workspace)** | `@workspace /new crea una app de React con Vite y TypeScript` |
| **Generar un archivo completo** | `@workspace /new crea un componente de React llamado 'Login' con campos para email y password, usando Tailwind CSS para los estilos.` |
| **Generar una función (en el editor)** | Escribe un comentario detallado: `// Función asíncrona 'fetchData' que usa axios para hacer un GET a la API de 'https://api.example.com/data' y maneja los errores con un bloque try-catch.` |

#### Escenario 3: Mejorar y Refactorizar Código

*   **Tu Meta**: Modernizar, simplificar y robustecer el código existente.
*   **Tu Herramienta Principal**: `@workspace /fix`

| Tarea | Prompt de Ejemplo en el Chat (con código seleccionado) |
| :--- | :--- |
| **Refactorizar para legibilidad** | `@workspace /fix haz este código más declarativo, usa métodos de array en lugar de bucles for.` |
| **Extraer lógica a una función** | `@workspace /fix extrae esta lógica a una nueva función llamada 'validateInput'.` |
| **Añadir manejo de errores** | `@workspace /fix añade un bloque try-catch a esta función para manejar errores de la API.` |
| **Optimizar rendimiento** | `@workspace /fix ¿Hay una forma más performante de escribir esto? Quizás usando un Map o un Set.` **(¡Advertencia! Siempre mide el rendimiento después)** |

#### Escenario 4: Pruebas, Documentación y Calidad

*   **Tu Meta**: Acelerar las tareas que garantizan la calidad del software.
*   **Tus Herramientas**: `/doc`, `/tests`

| Tarea | Prompt de Ejemplo en el Chat |
| :--- | :--- |
| **Generar documentación** | *Selecciona una función/clase*, luego: `@workspace /doc` |
| **Crear pruebas unitarias** | `@workspace /tests para #file:src/utils/helpers.js usando Vitest. Mockea las dependencias necesarias.` |
| **Arreglar una prueba fallida** | `@workspace /fixTestFailure` (Copilot analizará el error de la prueba y propondrá una solución) |

#### Escenario 5: Interactuar con tu Entorno (VS Code y Terminal)

*   **Tu Meta**: Usar lenguaje natural para controlar tu editor y tu terminal.
*   **Tus Herramientas**: `@vscode`, `@terminal`

| Tarea | Prompt de Ejemplo en el Chat |
| :--- | :--- |
| **Encontrar un comando de VS Code** | `@vscode ¿Cómo puedo cambiar el tema de color?` |
| **Generar un comando de terminal** | `@terminal lista todos los archivos .js en el directorio 'src', ordenados por tamaño.` |
| **Depurar un comando de terminal** | `@terminal este comando 'grep ...' no funciona como espero. ¿Puedes corregirlo?` |

---

### Atajos de Teclado Esenciales (VS Code)

| Acción | Windows / Linux | macOS |
| :--- | :--- | :--- |
| **Aceptar sugerencia en línea** | `Tab` | `Tab` |
| **Rechazar sugerencia en línea** | `Esc` | `Esc` |
| **Ver sugerencia SIGUIENTE** | `Alt + ]` | `Option (⌥) + ]` |
| **Ver sugerencia ANTERIOR** | `Alt + [` | `Option (⌥) + [` |
| **Abrir panel con 10 sugerencias** | `Ctrl + Enter` | `Cmd (⌘) + Enter` |
| **Abrir Chat RÁPIDO (en línea)** | `Ctrl + I` | `Cmd (⌘) + I` |
| **Abrir panel de CHAT principal** | `Ctrl + Alt + I` | `Cmd (⌘) + Option (⌥) + I` |

---

### Pro-Tips: Más Allá de lo Básico

*   **Combina herramientas**: Usa variables dentro de tus peticiones a los participantes. Ejemplo: `@workspace /explain la función #selection en el archivo #file`.
*   **Sé hiper-específico**: No digas solo `/fix`. Di `@workspace /fix refactoriza esto para usar el patrón 'Singleton' y añade comentarios explicando por qué`.
*   **Usa el chat para aprender**: Si no entiendes una sugerencia, pregunta. `¿Por qué es mejor usar 'async/await' que promesas anidadas aquí?`
*   **Itera**: El primer resultado no tiene que ser el final. Sigue conversando con el chat para refinar la respuesta. "Ok, eso funciona. Ahora asegúrate de que la función también maneje el caso en que la entrada sea nula."
*   **Limpia la conversación**: Usa `/clear` en el chat para empezar una nueva sesión y evitar que el contexto anterior influya en tus nuevas preguntas.

**Recuerda**: La IA es una herramienta. Tú eres el artesano. Domina estos flujos de trabajo y transformarás a Copilot de un autocompletado glorificado a un verdadero compañero de desarrollo.
