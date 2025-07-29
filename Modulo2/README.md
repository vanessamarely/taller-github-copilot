### **Módulo 2: Instalación y Primeras Líneas de Código con Copilot**

#### **Objetivo**
En este módulo, pasaremos de la teoría a la práctica. Te guiaré paso a paso para que instales y configures GitHub Copilot en tu entorno de desarrollo. Al final, escribirás tus primeras líneas de código con la asistencia de la IA y aprenderás los comandos básicos de interacción.

#### **Paso 1: Requisitos y Licenciamiento**

*   **Cuenta de GitHub**: Es indispensable. Si no tienes una, créala.
*   **Editor de Código**: Usaremos **Visual Studio Code**, ya que ofrece la integración más completa. Asegúrate de tenerlo instalado.
*   **Licencia de Copilot**: GitHub Copilot es un servicio de suscripción.
    *   **Prueba gratuita**: Si es tu primera vez, puedes activar una prueba gratuita (generalmente de 30 días) desde la página de configuración de tu cuenta de GitHub.
    *   **Planes**: Existen planes para individuos y empresas.
    *   **Gratis para Estudiantes y Proyectos Open Source**: Si eres parte del GitHub Student Developer Pack o mantenedor de un proyecto de código abierto popular, puedes ser elegible para una licencia gratuita.

#### **Aclaración Importante: ¿Existe una versión gratuita o sin licencia?**

Esta es una duda muy común. La respuesta corta es **no**.

*   **No hay versión "gratuita" funcional**: Para que GitHub Copilot funcione y te ofrezca sugerencias, tu cuenta de GitHub **debe tener una suscripción activa**. Esto puede ser una prueba gratuita, un plan de pago (Individual o Business), o una de las licencias gratuitas para estudiantes o mantenedores de proyectos open source.
*   **¿Qué pasa si no tengo licencia?**: Si instalas la extensión pero no tienes una licencia activa, Copilot simplemente no funcionará. Te mostrará mensajes pidiéndote que inicies una prueba o te suscribas. No hay una modalidad "limitada" o "reducida" para usuarios sin licencia.
*   **¿Y los límites de tokens?**: Aunque los modelos de IA subyacentes funcionan con "tokens" (pedazos de palabras), **GitHub Copilot no impone un límite de tokens a los usuarios**. El servicio se vende como una suscripción de "todo lo que puedas usar". No tienes que preocuparte por cuántas sugerencias pides o cuánto código generas; no se te cobrará por uso ni se te cortará el servicio por "gastar tus tokens".

---

#### **Paso 2: Instalación en VS Code**

1.  Abre VS Code.
2.  Ve al panel de **Extensiones** en la barra de actividades de la izquierda (o presiona `Ctrl+Shift+X` / `Cmd+Shift+X`).
3.  En la barra de búsqueda, escribe `GitHub Copilot`.
4.  Busca la extensión oficial (publicada por `GitHub`) y haz clic en **Instalar**.
5.  Una vez instalada, VS Code te pedirá que inicies sesión. Haz clic en **"Sign in to GitHub"**.
6.  Se abrirá tu navegador para que autorices a VS Code a acceder a tu cuenta de GitHub. Sigue los pasos.
7.  ¡Listo! Si la autenticación fue exitosa, verás un pequeño ícono de Copilot en la barra de estado de VS Code, en la esquina inferior derecha.

#### **Paso 3: Tu Primera Interacción con Copilot**

Vamos a ver a Copilot en acción.

1.  **Crea un nuevo archivo**: Crea un archivo con la extensión de tu lenguaje favorito (ej. `app.js` para JavaScript o `main.py` para Python).
2.  **Sugerencias en línea (Inline Suggestions)**:
    *   Empieza a escribir el nombre de una función. Por ejemplo: `function diHola`
    *   Copilot probablemente te sugerirá el resto de la línea y el cuerpo de la función en un texto de color gris.
    *   **Para aceptar la sugerencia, presiona `Tab`**.
    *   **Para rechazarla, simplemente sigue escribiendo**.
3.  **Ver alternativas**:
    *   A veces, Copilot tiene varias ideas. Cuando veas una sugerencia, puedes usar los atajos `Alt+]` (o `Option+]`) y `Alt+[` (o `Option+[`) para ciclar entre diferentes opciones.
4.  **Abrir el panel de sugerencias**:
    *   Si no te gusta ninguna sugerencia en línea, puedes pedirle a Copilot un menú completo de opciones.
    *   Presiona `Ctrl+Enter` (o `Cmd+Enter`). Se abrirá un panel a la derecha con hasta 10 sugerencias diferentes. Puedes revisarlas y hacer clic en "Aceptar solución" en la que más te guste.

#### **Paso 4: El Poder del Chat de Copilot**

Copilot no solo sugiere código mientras escribes. También puedes "conversar" con él.

1.  **Abre la vista de Chat**: Busca el ícono de Copilot Chat en la barra de actividades de la izquierda.
2.  **Haz una pregunta**: En el cuadro de texto del chat, pídele algo en lenguaje natural.
    *   `"¿cómo hago una petición fetch en javascript?"`
    *   `"explícame qué es una promesa en javascript"`
    *   `"escribe una función en python que reciba una lista y la devuelva sin duplicados"`
3.  Copilot te responderá con explicaciones y fragmentos de código que puedes copiar o insertar directamente en tu archivo.

Al final de este módulo, te sentirás cómodo con el flujo de trabajo básico de Copilot: recibir, aceptar y alternar sugerencias, y usar el chat para obtener ayuda más específica.
