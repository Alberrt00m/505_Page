# 505 — Landing page de la miniserie

Sitio estático (HTML5 + CSS + JavaScript vanilla, sin frameworks ni build step) listo para publicarse en GitHub Pages.

## Estructura

```
505-site/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── assets/
│   └── logo.png
└── README.md
```

## Cómo publicarlo en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `505-miniserie`).
2. Sube estos archivos manteniendo la misma estructura de carpetas (`css/`, `js/`, `assets/` deben quedar junto a `index.html`).
3. En el repositorio, ve a **Settings → Pages**.
4. En "Build and deployment", selecciona **Deploy from a branch**.
5. Elige la rama `main` y la carpeta `/ (root)`.
6. Guarda. GitHub te dará una URL tipo `https://tu-usuario.github.io/505-miniserie/`.

## Qué personalizar antes de publicar

- **Productores** (`index.html`, sección `#productores`): reemplaza los nombres, roles y fotos de ejemplo (`Nombre Apellido`) por los datos reales del equipo. Puedes cambiar `<span>NN</span>` por una imagen: `<img src="assets/foto-productor.jpg" alt="Nombre Apellido">`.
- **Teasers y capítulos** (`index.html`, sección `#capitulos`): cada tarjeta `.tape-card` tiene un atributo `data-video=""`. Cuando tengas el link de YouTube/Vimeo, pon ahí la URL de **embed** (por ejemplo `https://www.youtube.com/embed/XXXXXXXX`) y el modal reproducirá el video automáticamente. Mientras esté vacío, se mostrará "Señal no disponible / Próximamente".
- **Logo**: ya está tomado de la imagen que compartiste (`assets/logo.png`), usado como favicon, en la barra de navegación, el hero y el pie de página.
- **Paleta de color**: definida como variables CSS en la parte superior de `css/style.css` (`:root`), tomada directamente de tu paleta ("Azul Petróleo Oscuro", "Gris Hielo", "Rojo Apagado/Sangre Seca", etc.). Cambiar un valor ahí actualiza todo el sitio.

## Notas de diseño

La página está construida como un "expediente" de interrogatorio: navegación en forma de pestañas de carpeta, un contador de grabación ambiental en la esquina superior, la sinopsis presentada como una declaración con fragmentos redactados (tócalos para revelarlos) y los capítulos como cintas de evidencia con carrete giratorio al pasar el cursor. Todo el movimiento respeta `prefers-reduced-motion`.
