### **Módulo 5: Pruebas, documentación y buenas prácticas**

#### **Descripción**

Un buen software no solo funciona, sino que también es fácil de mantener, probar y entender. En este módulo, aprenderás a usar GitHub Copilot para acelerar dos de las tareas más cruciales en el ciclo de vida del desarrollo: la **generación de pruebas unitarias** y la **creación de documentación**.

#### **Generación de pruebas unitarias con `/tests`**

Escribir pruebas es fundamental, pero a menudo tedioso. Copilot puede generar el código base de tus pruebas, permitiéndote centrarte en los casos límite y la lógica de negocio.

*   **¿Cómo funciona?**:
    1.  Abre el archivo con el código que quieres probar.
    2.  Abre el Chat de Copilot.
    3.  Escribe el comando `/tests` o una instrucción como `Genera pruebas unitarias para la función 'calcularAreaCirculo'`.
    4.  Copilot analizará la función y generará un conjunto de pruebas utilizando el framework de testing que detecte en tu proyecto (como Jest, PyTest, JUnit, etc.).

*   **Ejemplo con Jest (JavaScript)**:
    *   **Código fuente**:
        ```javascript
        function calcularAreaCirculo(radio) {
            if (radio < 0) {
                throw new Error('El radio no puede ser negativo');
            }
            return Math.PI * radio * radio;
        }
        ```
    *   **Comando en el chat**: `Genera pruebas unitarias para la función calcularAreaCirculo usando Jest`
    *   **Resultado de Copilot**:
        ```javascript
        describe('calcularAreaCirculo', () => {
            it('debería calcular el área correctamente para un radio positivo', () => {
                expect(calcularAreaCirculo(3)).toBeCloseTo(28.27, 2);
            });

            it('debería devolver 0 para un radio de 0', () => {
                expect(calcularAreaCirculo(0)).toBe(0);
            });

            it('debería lanzar un error para un radio negativo', () => {
                expect(() => calcularAreaCirculo(-1)).toThrow('El radio no puede ser negativo');
            });
        });
        ```

#### **Documentación automática con `/doc`**

Una buena documentación es clave para la colaboración y el mantenimiento a largo plazo. Copilot puede generar comentarios de documentación claros y estructurados.

*   **¿Cómo funciona?**:
    1.  Selecciona la función, clase o método que quieres documentar.
    2.  Abre el chat en línea (`Ctrl+I` o `Cmd+I`).
    3.  Escribe el comando `/doc`.
    4.  Copilot generará un bloque de comentarios en un formato estándar como JSDoc, TSDoc, o DocStrings de Python.

*   **Ejemplo con JSDoc (JavaScript)**:
    *   **Código fuente**:
        ```javascript
        function calcularAreaCirculo(radio) {
            if (radio < 0) {
                throw new Error('El radio no puede ser negativo');
            }
            return Math.PI * radio * radio;
        }
        ```
    *   **Comando**: `/doc`
    *   **Resultado de Copilot**:
        ```javascript
        /**
         * Calcula el área de un círculo dado su radio.
         * @param {number} radio - El radio del círculo. No puede ser negativo.
         * @returns {number} El área calculada del círculo.
         * @throws {Error} Lanza un error si el radio es negativo.
         */
        ```

#### **Integrando buenas prácticas con Copilot**

Copilot es una herramienta, y como toda herramienta, su eficacia depende de cómo se utilice.

*   **Revisión del código (Code Review)**: El código generado por Copilot **siempre** debe ser revisado por un humano. Trátalo como si fuera el código de un desarrollador junior: una buena base, pero que necesita supervisión.
*   **Seguridad**: Pregúntale a Copilot sobre posibles vulnerabilidades. Selecciona una función y pregunta en el chat: `¿Hay alguna vulnerabilidad de seguridad en este código?`. Copilot puede ayudarte a identificar problemas comunes como inyección de SQL, XSS, etc. (aunque no reemplaza a herramientas de análisis de seguridad especializadas).
*   **Consistencia de estilo**: Copilot intenta adaptarse al estilo de tu código existente. Sin embargo, para garantizar la consistencia en todo el proyecto, es fundamental usar linters (como ESLint) y formateadores (como Prettier). Copilot y estas herramientas se complementan perfectamente.
*   **No delegues el pensamiento crítico**: Usa Copilot para automatizar lo repetitivo, no para tomar decisiones de diseño de arquitectura. La responsabilidad final sobre la calidad, el rendimiento y la seguridad del software sigue siendo tuya.
