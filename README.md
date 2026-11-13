# Promatic Media GPS - Landing Page Corporativa

Sitio web corporativo para **Promatic Media GPS**, enfocado en la presentación de servicios de monitoreo de flotas, videotelemática y analítica de datos. El proyecto es una landing page moderna, completamente responsiva, diseñada para maximizar la conversión y destacar la propuesta de valor (retorno de inversión, seguridad y eficiencia) a nivel B2B.

## Características Principales

*   **Diseño Moderno y Responsivo:** Adaptable a todo tipo de dispositivos (Móvil, Tablet, Desktop).
*   **Animaciones al hacer Scroll:** Uso de AOS (Animate On Scroll) para revelar elementos suavemente a medida que el usuario navega.
*   **Menú Dinámico (Sticky):** Barra de navegación que cambia de estado (transparente a color sólido) al hacer scroll.
*   **Sección de Casos de Éxito:** Carrusel infinito animado por CSS puro para mostrar los clientes de la marca.
*   **Botones de Acción Rápida (FAB):** Botón flotante para volver arriba y botón directo a WhatsApp.
*   **Metodología BEM:** Hojas de estilo estructuradas y mantenibles siguiendo el patrón Block-Element-Modifier.

## Tecnologías y Librerías Utilizadas

*   **HTML5:** Estructura semántica.
*   **CSS3 (Vanilla):** Variables nativas, Flexbox, CSS Grid y animaciones keyframes. Escrito bajo metodología **BEM**.
*   **JavaScript (Vanilla):** Lógica del DOM, menús móviles, scroll suave e inicialización de librerías. No requiere frameworks pesados.
*   **[AOS (Animate on Scroll)](https://michalsnik.github.io/aos/):** Librería para animaciones de entrada.
*   **[Font Awesome 6.4.0](https://fontawesome.com/):** Iconografía vectorial.

## Estructura del Proyecto

```text
/
├── assets/
│   ├── css/
│   │   └── styles.css          # Archivo principal de estilos (Variables, utilidades, BEM)
│   ├── js/
│   │   └── script.js           # Lógica frontend (AOS, Navbar, Mobile Menu, Form handler)
│   ├── img/                    # Imágenes y logotipos (SVG, PNG, WEBP)
│   └── videos/                 # Videos de fondo (MP4) optimizados para web
├── index.html                  # Landing page principal
└── README.md                   # Documentación del proyecto
```

## ESTADO DEL PROYECTO: Integración Backend Pendiente

Actualmente, la maqueta y el comportamiento del lado del cliente (Frontend) están completados. Sin embargo, **la integración del formulario de contacto y el sistema anti-spam debe ser finalizada por el equipo de desarrollo backend.**

### Tareas a realizar por el desarrollador a cargo:

1.  **Cloudflare Turnstile:** 
    *   El script de frontend para Turnstile está insertado en `index.html` y referenciado en `script.js`.
    *   Falta reemplazar el placeholder `TU_SITE_KEY_AQUI` en el `data-sitekey` del HTML con la clave pública real.
    *   **CRÍTICO:** Implementar la validación del *Secret Key* en el servidor.
2.  **Backend (PHP):**
    *   Se requiere crear la arquitectura de envío de correos (ej: `enviar.php`).
    *   Se sugiere crear archivos de configuración seguros (ej: `config.local.php` u ocultar credenciales vía `.env`) para manejar las contraseñas SMTP y las API Keys de Cloudflare.
    *   El `script.js` actualmente hace un `fetch()` apuntando a `tu_backend_aqui.php`. Esta ruta debe ser actualizada al archivo final. El JS espera una respuesta en formato JSON con la estructura: `{ ok: true/false, message: "..." }`.

## Cómo ejecutar el proyecto en local

Al ser un proyecto estático (mientras no se implemente el PHP), solo necesitas un servidor local básico:

1. Clona este repositorio.
2. Abre la carpeta del proyecto en tu editor de código (ej. VS Code).
3. Utiliza una extensión como **Live Server** para abrir el archivo `index.html`.
4. El sitio estará corriendo habitualmente en `http://127.0.0.1:5500`.

---
*Desarrollado para Promatic Media S.A.*