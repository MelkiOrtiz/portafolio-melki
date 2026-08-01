# Portafolio Personal — Melki Ortiz

Página web de presentación personal desarrollada con **Bootstrap 5**, HTML5 semántico y CSS personalizado. Funciona como un perfil o currículum digital completamente responsive.

## Objetivo del proyecto

Crear una página web de presentación personal aplicando los conceptos de **HTML5 semántico**, **diseño responsive** y **personalización mediante CSS**, con la finalidad de aprender a integrar un framework CSS moderno como Bootstrap sin perder la identidad visual del sitio.

## Cómo ejecutar la página

El proyecto es 100% estático y usa **Bootstrap 5 por CDN**, por lo que no requiere instalación de dependencias.

### Opción 1 — Abrir directamente

Doble clic en `index.html` o desde la terminal:

```powershell
Start-Process "index.html"
```

### Opción 2 — Servidor local

Para una experiencia más cercana a producción:

```powershell
# Con Python
python -m http.server 8000
# Luego abre http://localhost:8000
```

```powershell
# Con Node.js
npx serve .
```

## Componentes de Bootstrap utilizados

| Componente | Uso |
|---|---|
| **Navbar** | Barra de navegación responsive con botón hamburguesa y colapso en pantallas pequeñas. Fija con `sticky-top`. |
| **Grid System** | Estructura `container > row > col` en todas las secciones para el layout responsive. |
| **Badges / Rounded Pills** | Presentación de las 7 habilidades como pills personalizadas. |
| **Cards** | Tres tarjetas para proyectos y pasatiempos con imagen, título, descripción y botón. |
| **Buttons** | Botones primarios y outline para llamadas a la acción y enlaces a GitHub. |
| **Bootstrap Icons** | Iconos de redes sociales (GitHub, GitLab, Discord, Instagram, X, Goodreads y correo). |

## Elementos personalizados en CSS (`css/style.css`)

- **Paleta de colores**: variables CSS con azul oscuro (`#0f172a`) como color base y azul vibrante (`#2563eb`) como acento.
- **Tipografía**: Google Fonts — *Inter* para el cuerpo y *Poppins* para títulos.
- **Espaciados**: padding propio en secciones (`section-padding`) con ajustes por breakpoint.
- **Sombras**: sombras suaves y elevadas para cards, navbar e interacciones.
- **Animaciones**: efectos hover con `transform` y `transition` en foto de perfil, badges, cards, botones y redes sociales.
- **Gradiente**: fondo degradado en la sección hero.
- **Scroll suave**: `scroll-behavior: smooth` para navegación entre secciones.
- **Media queries**: ajustes específicos para 320px, 768px y 1280px.
- Sin uso de `!important`.

## Principales decisiones de diseño

1. **Navbar fija con `sticky-top`**: se colocó la `<nav>` como hija directa de `<body>` (fuera de `<header>`) porque `position: sticky` solo se mantiene dentro del límite de su elemento padre; así la barra sigue visible en todo el scroll.
2. **Paleta oscura con acento azul**: fondo navy en navbar, hero y footer da contraste profesional; el azul vibrante resalta elementos interactivos.
3. **Hero con gradiente**: el degradado transmite profundidad y mantiene la identidad sin depender de imágenes de fondo.
4. **Secciones alternadas**: fondo claro (`#f8fafc`) en biografía y habilidades para crear jerarquía visual y evitar monotonía.
5. **Imágenes uniformes en cards**: altura fija de 200px con `object-fit: cover` para que las tarjetas se vean alineadas sin importar las dimensiones del archivo.
6. **Accesibilidad**: etiquetas `aria-label`, `role="contentinfo"`, `alt` descriptivos y `rel="noopener noreferrer"` en enlaces externos.
7. **Sistema Grid para responsive**: las columnas colapsan de 3 → 2 → 1 según el tamaño (col-lg-4, col-md-6), evitando desplazamiento horizontal en cualquier pantalla.

## Capturas de pantalla responsive

### 1280 px
![Captura 1280 px](captures/1280%20px.png)

### 768 px
![Captura 768 px](captures/768%20px.png)

### 320 px
![Captura 320 px](captures/320%20px.png)
