
# 🤖 Tareas de Aprendizaje: Estructura Bootstrap y CSS

---

## 🎯 El Objetivo de este Bloque
Aprenderás a maquetar una interfaz web limpia combinando dos herramientas: **Bootstrap** (para la estructura y colocación de elementos) y **CSS Estándar** (para aplicar tu propia paleta de colores mediante variables `--var`). 

Evitaremos por completo los estilos inline (`style="..."`). Todo el diseño visual estará centralizado en tu hoja de estilos para mantener el código ordenado y entendible.

---

## 📅 Hito 1: La Barra de Navegación (Navbar) y el CSS Base

Antes de crear cajas o grids, prepararemos nuestro archivo de estilos principal con variables inmutables que simulan constantes de color.

- [ ] **Tarea 1.1: Inicializar el entorno.** Crea un archivo llamado `index.html` en tu editor. Añade la estructura base e importa la CDN de Bootstrap. Déjalo exactamente así:
  
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Laboratorio de Estilos OpenSpec</title>
    <link href="[https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/dist/css/bootstrap.min.css](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/dist/css/bootstrap.min.css)" rel="stylesheet">
</head>
    <body>

    </body>
  </html>
```

- [ ] **Tarea 1.2: Crear el CSS de Marca** En la sección <head>, justo debajo de la CDN de Bootstrap, añade una etiqueta ```<style>``` que actuará como nuestro CSS principal. Definiremos los colores en variables globales (:root):

``` HTML
<style>
    /* Variables de color de nuestra marca (Constantes de diseño) */
    :root {
        --branding-oscuro: #1a252f;
        --branding-primario: #34495e;
        --branding-destacado: #e67e22;
        --texto-claro: #ffffff;
    }

    /* Regla CSS estándar que aplica nuestra constante de color */
    .custom-navbar {
        background-color: var(--branding-oscuro) !important;
    }
</style>
```
- [ ] **Tarea 1.3:** El componente Navbar. Inyecta la barra de navegación al inicio del <body>. Observa cómo usa las utilidades estructurales de Bootstrap, pero el color proviene de nuestra clase CSS externa:

```HTML
<nav class="navbar custom-navbar">
    <div class="container-fluid">
        <span class="navbar-brand text-white h1 mb-0">🚀 OpenSpec Studio</span>
    </div>
</nav>
```

- [ ] **Tarea 1.4:** Verificación Visual e IA. Abre tu archivo index.html en el navegador web. Comprueba que aparece la barra superior con el color oscuro personalizado (#1a252f). Tras verlo, pregúntale a tu IA:

"Actua como un profesor moderno y motivador, con metáforas entendibles si hace falta. Estoy definiendo mis colores en el bloque CSS :root y llamándolos con var(). ¿Por qué separar los colores de esta forma es una mejor práctica arquitectónica que escribir el color directamente inline dentro de las etiquetas HTML?"

---


## 📂 Hito 2: El Layout de Columnas y Componentes ##
Ahora organizaremos el cuerpo de la página web utilizando el sistema de rejilla (Grid) de Bootstrap para las columnas, pero el estilo del contenedor interior se definirá de forma limpia en el CSS principal.

- [ ] **Tarea 2.1:** Ampliar el CSS principal. Añade esta nueva regla de diseño dentro de tu bloque "style" en el "head" para dar formato a los bloques de contenido de manera centralizada:

``` css
.bloque-contenido {
    background-color: var(--branding-primario);
    color: var(--texto-claro);
    transition: background-color 0.3s ease;
}

.bloque-contenido:hover {
    background-color: var(--branding-destacado);
}
```


- [ ] **Tarea 2.2:** Construir la rejilla de Bootstrap. Añade el contenedor principal de la página justo debajo de la etiqueta </nav> en tu <body>:

```HTML
<main class="container my-5">
    <div class="row">

        <div class="col-md-6 mb-3">
            <div class="bloque-contenido">
                <h3>Componente Alfa</h3>
                <p class="m-0">La estructura la maneja Bootstrap, pero el color y el efecto interactivo provienen de nuestro CSS estándar.</p>
            </div>
        </div>

        <div class="col-md-6 mb-3">
            <div class="bloque-contenido">
                <h3>Componente Beta</h3>
                <p class="m-0">Al reutilizar la clase, este bloque hereda inmediatamente toda nuestra paleta corporativa.</p>
            </div>
        </div>

    </div>
</main>
```


- [ ] **Tarea 2.3:** Validación empírica. Guarda el documento y refresca tu navegador web (F5). Comprueba que la pantalla se divide en dos columnas idénticas y que al pasar el ratón por encima de cualquiera de los dos bloques, el color cambia suavemente al tono destacado (#e67e22).

## 🛠️ El Ensamblaje Final (La Plantilla Limpia) ##
Revisa que todo el código de tu archivo coincida exactamente con este plano de ingeniería. Observa cómo el HTML queda libre de códigos de color inline, delegando todo en el bloque de estilos superior.

Código Completo (index.html):

```HTML
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Laboratorio de Estilos OpenSpec</title>
    
    <link href="[https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/dist/css/bootstrap.min.css](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/dist/css/bootstrap.min.css)" rel="stylesheet">
    
    <style>
        :root {
            --branding-oscuro: #1a252f;
            --branding-primario: #34495e;
            --branding-destacado: #e67e22;
            --texto-claro: #ffffff;
        }

        /* Aplicación en Barra de Navegación */
        .custom-navbar {
            background-color: var(--branding-oscuro) !important;
        }

        /* Aplicación en Bloques Estructurales */
        .bloque-contenido {
            background-color: var(--branding-primario);
            color: var(--texto-claro);
            transition: background-color 0.3s ease;
        }

        /* Comportamiento interactivo */
        .bloque-contenido:hover {
            background-color: var(--branding-destacado);
        }
    </style>
</head>

<body>
    <nav class="navbar custom-navbar">
        <div class="container-fluid">
            <span class="navbar-brand text-white h1 mb-0">🚀 OpenSpec Studio</span>
        </div>
    </nav>

    <main class="container my-5">
        <div class="row">
            
            <div class="col-md-6 mb-3">
                <div class="p-4 border rounded shadow-sm bloque-contenido">
                    <h3>Componente Alfa</h3>
                    <p class="m-0">La estructura la maneja Bootstrap, pero el color y el efecto interactivo provienen de nuestro CSS estándar.</p>
                </div>
            </div>

            <div class="col-md-6 mb-3">
                <div class="p-4 border rounded shadow-sm bloque-contenido">
                    <h3>Componente Beta</h3>
                    <p class="m-0">Al reutilizar la clase, este bloque hereda inmediatamente toda nuestra paleta corporativa.</p>
                </div>
            </div>

        </div>
    </main>

</body>
</html>
```


### 📋 Entrega tu Checklist 
Para demostrar tu entendimiento sobre la arquitectura limpia y la separación de responsabilidades en Frontend, realiza este último control de calidad:

- [ ] **Tarea 3.1:** Prueba de Cambio Global. Cambia el valor de la variable --branding-primario dentro de tu CSS por un tono gris oscuro (por ejemplo, #2b2b2b). Guarda y refresca tu navegador web. Comprueba cómo cambian ambos bloques simultáneamente sin tocar una sola línea de tu HTML.

- [ ] **Tarea 3.2:** Auditoría final con IA. Envía este prompt a la IA para cerrar el laboratorio:

"Actúa como un Auditor de Código Senior. Revisa mi estructura donde combino clases nativas de Bootstrap (como col-md-6 ) con mis propias clases de CSS principal (bloque-contenido). Explícame por qué este enfoque mixto es el estándar de oro en empresas de software en lugar de modificar los archivos internos de Bootstrap."

Guarda las conclusiones de la IA en un archivo llamado auditoria_estilos.md en tu carpeta local y entrégalo junto con tu archivo HTML. ¡Hito superado con maestría!