Markdown
# 🤖 Primer Layout Modular con Bootstrap

---

## 🎯 El Objetivo de este Bloque
Aprenderás a maquetar una página web utilizando los dos pilares fundamentales de Bootstrap: una **barra de navegación (Navbar)** básica y un **sistema de rejilla (Grid)** de columnas adaptables. Escribirás el código paso a paso, abriendo tu navegador para verificar el resultado visual en cada hito antes de avanzar.

---

## 📅 Hito 1: Plantilla Base y Barra de Navegación (Navbar)

El primer componente visual que ve un usuario en cualquier aplicación web es el menú superior. Vamos a construir uno minimalista y limpio.

- [ ] **Tarea 1.1: Inicializar el entorno.** Crea un archivo llamado `proyecto.html` en tu editor. Añade la estructura limpia obligatoria importando Bootstrap por CDN:
  ```html
  <!DOCTYPE html>
  <html lang="es">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Mi Primer Layout Bootstrap</title>
      <link href="[https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/dist/css/bootstrap.min.css](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/dist/css/bootstrap.min.css)" rel="stylesheet">
  </head>
  <body>

  </body>
  </html>
    ```

- [ ] ***Tarea 1.2:*** El componente Navbar. Añade este menú de navegación sencillo en la parte del body:

    ```HTML
    <nav class="navbar navbar-dark bg-dark">
        <div class="container-fluid">
            <span class="navbar-brand mb-0 h1">🚀 Laboratorio Dev</span>
        </div>
    </nav>
    ```

- [ ] **Tarea 1.3:** Verificación y Auditoría con IA.
1. Utiliza una de las extensiones "view in browser", "live server" o haz doble clic en tu archivo proyecto.html para abrirlo en el navegador web. Comprueba que aparece una franja negra superior con el título alineado a la izquierda.

2. Copia el código de la barra de navegación, dáselo a la IA y lánzale este prompt:
"Actúa como un Profesor moderno y motivador. Acabo de renderizar esta barra de navegación en mi navegador. Explícame de forma muy breve qué hacen exactamente las clases navbar-dark y bg-dark y por qué el título no se pega totalmente al borde de la pantalla gracias a container-fluid."

3. Escribe el siguiente prompt para aprender más tipos de container en Bootstrap:
"Responde de una froma sencilla y entendible. Explicame que tipos de container tiene preparados Bootstrap. Compara con los tipos de container de CSS standart"


## 📂 Hito 2: El Contenedor y el Sistema de Columnas (Grid) ##
Bootstrap organiza el contenido en filas (row) y columnas (col). Vamos a dividir la pantalla en dos secciones proporcionales: una zona principal para contenido y una barra lateral para información adicional.

- [ ] **Tarea 2.1:** Crear la estructura del Grid. Justo debajo de la etiqueta "nav", añade el contenedor principal y su fila divisoria:

``` HTML
<main class="container my-4">
    <div class="row">

        <div class="col-md-8 bg-light p-3 border">
            <h2>Sección de Contenido</h2>
            <p>Esta es la zona donde irá el texto principal de nuestra aplicación web.</p>
        </div>

        # CONTENIDO_OCULTO: Espacio preparado para la Columna 2

    </div>
</main>
```

- [ ] **Tarea 2.2:** Añadir la Columna Secundaria. Reemplaza la línea # CONTENIDO_OCULTO por la columna de la barra lateral, completando la fila:

```HTML
        <div class="col-md-4 bg-secondary text-white p-3 border">
            <h3>Barra Lateral</h3>
            <p>Información complementaria, enlaces o estadísticas del sistema.</p>
        </div>
```

- [ ] **Tarea 2.3:** Interroga a la IA sobre Responsividad. Abre tu navegador y refresca la página (F5). Observa cómo se distribuye el espacio en tu pantalla. Luego, pregúntale a la IA:

"Tengo maquetadas dos columnas con las clases col-md-8 y col-md-4. ¿Por qué la suma da exactamente 12? ¿Qué comportamiento visual ocurrirá en mi navegador si reduzco el tamaño de la ventana al tamaño de un teléfono móvil debido al modificador -md-?"


## 🛠️ Ensamblaje Final (La Estructura Limpia) ##
Revisa que tu archivo final coincida exactamente con este mapa técnico para asegurar que todas las etiquetas abren y cierran en su lugar correspondiente.

Código Completo (proyecto.html):

```HTML
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Primer Layout Bootstrap</title>
    <link href="[https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/dist/css/bootstrap.min.css](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/dist/css/bootstrap.min.css)" rel="stylesheet">
</head>
<body>

    <nav class="navbar navbar-dark bg-dark">
        <div class="container-fluid">
            <span class="navbar-brand mb-0 h1">🚀 Laboratorio Dev</span>
        </div>
    </nav>

    <main class="container my-4">
        <div class="row">
            
            <div class="col-md-8 bg-light p-3 border">
                <h2>Sección de Contenido</h2>
                <p>Esta es la zona donde irá el texto principal de nuestra aplicación web.</p>
            </div>

            <div class="col-md-4 bg-secondary text-white p-3 border">
                <h3>Barra Lateral</h3>
                <p>Información complementaria, enlaces o estadísticas del sistema.</p>
            </div>

        </div>
    </main>

</body>
</html>

```

### 📋 Entrega (Tu OpenSpec Checklist) ###
Para asegurar que has aprendido a manejar la cuadrícula o Grid de manera autónoma, realiza este ejercicio de control:

- [ ] **Tarea 3.1:** Modifica las clases de tus columnas en el archivo para que el contenido principal use col-md-9 y la barra lateral use col-md-3. Guarda, refresca tu navegador y observa el cambio de proporciones.

- [ ] **Tarea 3.2:** Pídele a la IA la validación final con este prompt:

"He cambiado las proporciones de mi Grid a 9 y 3. Explícame brevemente cómo calcula Bootstrap el ancho en porcentajes automáticos basándose en su sistema de 12 columnas. Haz un resumen en una tabla Markdown muy simple."


---
Guarda la respuesta en un archivo llamado conclusiones_layout.md y comparte tus archivos con el profesor. ¡Hito superado!