### **Módulo 3: Dominando la Generación de Código: De Comentarios a Funciones**

#### **Objetivo**
Este es el módulo donde aprenderás la habilidad más importante para trabajar con Copilot: **el arte de dar instrucciones a través de comentarios**. Descubrirás cómo la calidad de tus comentarios (prompts) impacta directamente en la calidad del código generado. Pasaremos de generar funciones simples a estructuras de código más complejas.

#### **La Regla de Oro: "Basura entra, basura sale" (Garbage In, Garbage Out)**
Copilot es increíblemente potente, pero no puede leer tu mente. La calidad de sus sugerencias es directamente proporcional a la calidad del contexto que le proporcionas. Un comentario vago o ambiguo dará como resultado un código genérico o incorrecto. Un comentario claro, específico y detallado producirá un código preciso y útil.

#### **Práctica 1: Generación de Funciones Simples**
Vamos a empezar con lo básico.

1.  **Comentario claro y conciso**:
    *   En un archivo JavaScript, escribe:
        ```javascript
        // Crea una función que reciba dos números y devuelva su suma
        ```
    *   Presiona `Enter` después del comentario. Copilot debería ofrecerte la función completa.

2.  **Especificando nombres**:
    *   Puedes ser más específico sobre cómo quieres que se llame la función.
        ```javascript
        // Crea una función llamada 'sumarNumeros' que reciba 'a' y 'b' y devuelva la suma
        ```

#### **Práctica 2: Añadiendo Complejidad y Lógica**
Ahora, vamos a pedirle a Copilot que piense un poco más.

1.  **Manejo de casos borde**:
    *   En el mismo archivo, intenta con un comentario más robusto:
        ```javascript
        // Función que encuentra el número más grande en un array de números
        // Si el array está vacío, debe devolver null
        ```
    *   Observa cómo Copilot genera no solo el bucle o método para encontrar el máximo, sino también la comprobación inicial del array vacío.

2.  **Describiendo el "qué", no el "cómo"**:
    *   Un buen prompt se centra en el objetivo, no en los pasos de la implementación.
    *   **Mal prompt (demasiado prescriptivo)**: `// Itera sobre el array con un bucle for, mantén una variable para el máximo, compara cada elemento...`
    *   **Buen prompt (descriptivo)**: `// Encuentra el número más alto en el array 'numeros'`
    *   Deja que Copilot elija la mejor manera de implementarlo (podría usar `Math.max`, un `reduce`, etc.).

#### **Práctica 3: Generando Código con Dependencias**
Copilot es consciente del contexto de tu proyecto, incluyendo las librerías que podrías estar usando.

1.  **Simulando una dependencia**:
    *   Imagina que estás trabajando en un proyecto de Node.js que usa la librería `axios` para peticiones HTTP.
    *   Escribe el siguiente comentario:
        ```javascript
        // Importa axios
        // Crea una función asíncrona llamada 'obtenerUsuario' que reciba un id de usuario
        // Debe hacer una petición GET a la API de JSONPlaceholder para obtener los datos de ese usuario
        // La URL es https://jsonplaceholder.typicode.com/users/{id}
        // La función debe devolver los datos del usuario en formato JSON
        ```
    *   Copilot no solo generará la función con `async/await` y la lógica de `axios.get`, sino que también añadirá la línea `import axios from 'axios';` si no la tienes.

#### **Práctica 4: Generación de Clases y Objetos**
Puedes usar comentarios para definir la estructura completa de una clase.

*   Intenta con esto en un archivo TypeScript (`user.ts`):
    ```typescript
    // Crea una clase 'Usuario' con las siguientes propiedades:
    // - id: número, solo lectura
    // - nombre: string
    // - email: string
    // El constructor debe aceptar nombre y email, y generar un id numérico aleatorio
    // Incluye un método 'imprimirDetalles' que imprima los datos del usuario en la consola
    ```

#### **Consejos Avanzados para Prompts Efectivos**
*   **Proporciona ejemplos**: Para transformaciones de datos complejas, dar un ejemplo de entrada y salida en el comentario es muy útil. `// Convierte "apellido, nombre" a "nombre apellido", ej. "Doe, John" -> "John Doe"`
*   **Divide y vencerás**: Para una funcionalidad muy grande, no intentes generarla toda con un solo comentario. Divídela en funciones más pequeñas y genéralas una por una.
*   **Itera**: Si la primera sugerencia no es perfecta, ¡no la descartes! Acéptala y luego usa el chat de Copilot para refinarla: selecciona el código y pide cambios específicos.

Al final de este módulo, habrás desarrollado una intuición sobre cómo "hablar" con Copilot para que se convierta en un asistente de programación verdaderamente eficaz.
