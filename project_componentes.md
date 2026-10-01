# 🐚 Especificación del Proyecto: Buenas Prácticas y Programación Funcional en Bash (project.md)

---

## 🎯 ¿Qué voy a aprender?

- **QUÉ es estructurar código modular** en entornos de terminal con Bash 💻
- **PARA QUÉ sirve aislar la lógica** en funciones puras y seguir un flujo predecible
- **CÓMO aplicar patrones de arquitectura (MVC)** incluso procesando archivos de texto plano 📁

---

## 📊 Estándar de Código: Requerimientos Obligatorios

| Criterio | Nivel | Regla Estricta |
|---|---|---|
| **Modularidad** | 🔴 Obligatorio | El código jamás se escribe suelto. Todo debe estar estructurado en **funciones** 📦 |
| **Función Main** | 🔴 Obligatorio | La función `main` debe actuar exclusivamente como un **menú de operaciones** 📋 |
| **Filosofía** | 🔴 Obligatorio | Estilo **Declarativo y Funcional**. Código legible, optimizado y sin "grasa" de alto nivel 🧠 |
| **Arquitectura** | 🟡 Si hay datos | Patrón **MVC** (Modelo-Vista-Controlador) para cualquier persistencia, incluidos archivos de texto 🏗️ |

---

## ✍️ Cómo estructurar cada script (La Anatomía Funcional)

Para que cualquier ejercicio sea válido ante la OpenSpec, debe cumplir con estos 5 pilares de desarrollo:

1. **Estructura en Funciones:** Ninguna línea de lógica real puede vivir fuera de una función. El script solo debe invocar a la función `main` al final del archivo.
2. **El Menú `main`:** La función principal se limita a coordinar. Lee la intención del usuario (argumentos o menú visual) y delega el trabajo llamando a las funciones especialistas.
3. **Funciones Puras:** En la medida de lo posible y sin forzar la legibilidad, las funciones deben recibir parámetros por `$1, $2` y evitar modificar variables globales (efectos secundarios).
4. **Enfoque Declarativo:** Escribe código que describa *qué* hace y no solo *cómo* lo hace de forma caótica. Usa constantes en mayúsculas para configuraciones fijas.
5. **MVC para Texto Plano:** Si el script guarda datos (por ejemplo, una lista de usuarios en un `.txt`):
   - **Modelo:** Funciones que leen/escriben en el archivo de texto.
   - **Controlador:** Funciones que procesan y validan la lógica del negocio.
   - **Vista:** Funciones que imprimen el texto formateado o colores en la terminal (`echo`).

---

## 🔍 Restricciones de Optimización y Peso

- **Cero código redundante:** No añadas librerías externas ni comandos masivos de alto nivel si no son estrictamente necesarios para resolver el problema.
- **Humano-Céntrico:** El código debe estar optimizado para la máquina pero ser 100% entendible para un desarrollador humano. Usa nombres de variables y funciones autoexplicativos.

---

## ⚠️ Cuidado con:

- Mezclar la lógica de lectura de archivos (Modelo) con los comandos de impresión en pantalla `echo` (Vista).
- Dejar variables "sueltas" por todo el script que contaminen la memoria de la terminal.
- Olvidar que la optimización importa, pero la claridad del código ante un humano siempre es la prioridad.

---

## ✅ Siguiente Paso para el Alumno
Este documento define las reglas del juego. A partir de ahora, cualquier archivo de tareas (`tasks.md`) que recibas exigirá que tus scripts sigan este estándar de arquitectura funcional en Bash.


EJERCICIO:  IA crea tabla comparativa comandos básicos de Bash con palabras reservadas Python

