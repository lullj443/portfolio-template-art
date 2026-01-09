# Variables

Las variables CSS están definidas principalmente en [assets/css/theme.css](assets/css/theme.css). Usar variables te permite cambiar colores, tamaños y comportamientos globales sin editar cada regla individual.

Ejemplo: para cambiar el color principal edita o sobrescribe las variables en `:root`:

```css
:root {
  --color-bg: #ffffff;
  --color-text: #222222;
  --color-accent: #ff6b6b;
}
```

Consejos:

- Modifica primero las variables en [assets/css/theme.css](assets/css/theme.css).
- Para pruebas rápidas crea un archivo `assets/css/custom.css` y cárgalo después del resto para sobrescribir valores.

# Textos

Los textos y contenido están en [index.html](index.html). Busca títulos, subtítulos y párrafos que contienen el contenido visible.

Buenas prácticas:

- Mantén la estructura HTML: cambia solo el texto dentro de las etiquetas (`<h1>`, `<p>`, `<li>`, etc.).
- Evita eliminar clases o atributos usados por CSS/JS.
- Usa búsquedas (Ctrl+F) con palabras clave para localizar bloques de contenido rápidos.

# Imágenes

Las imágenes se referencian en [index.html](index.html) con etiquetas `<img src="...">` o como fondos CSS. Ejemplo típico:

```html
<img
  src="https://ik.imagekit.io/llj/ejemplo.jpg"
  alt="Descripción"
  loading="lazy"
/>
```

Recomendaciones:

- Usa CDNs (imagekit.io, Cloudinary) para servir imágenes optimizadas.
- Añade siempre `alt` para accesibilidad y SEO.
- Usa `loading="lazy"` para mejorar el rendimiento.
- Si necesitas cambiar tamaño/crop, hazlo desde el CDN o sube varias resoluciones para responsive.

# Estilos (CSS)

Carpeta: [assets/css/](assets/css/). Archivos claves: `base.css`, `layout.css`, `theme.css`, `index.css`, `nav.css`.

Cómo personalizar:

- Para cambios globales usa `theme.css` (variables).
- Para ajustes específicos modifica el archivo correspondiente (`nav.css` para navegación, `index.css` para la portada).
- Si quieres añadir reglas propias crea `assets/css/custom.css` y enlázalo al final en `index.html` para que tenga prioridad.

# JavaScript

El comportamiento interactivo está en [assets/js/main.js](assets/js/main.js). Ahí encontrarás listeners y pequeñas funciones (animaciones, menús, etc.).

Cambios comunes:

- Para desactivar una funcionalidad comenta o elimina el `script` correspondiente en `index.html`.
- Para ajustar tiempos o animaciones edita las constantes en `main.js`.

# Previsualización local

Opciones rápidas para ver la web en local (desde la raíz del proyecto):

PowerShell (si tienes Python instalado):

```powershell
python -m http.server 8000
# luego abre http://localhost:8000 en tu navegador
```

Con Node (si tienes `http-server` disponible):

```bash
npx http-server . -p 8000
```

# Buenas prácticas y despliegue

- Haz una copia de seguridad de `index.html` y de `assets/css/theme.css` antes de cambios mayores.
- Optimiza imágenes para web (webp/jpg con compresión razonable).
- Prueba la web en móvil y escritorio (herramientas de desarrollador del navegador).
- Para publicar, sube los archivos a tu hosting o servicio estático (GitHub Pages, Netlify, Vercel).

# Resumen rápido

- Variables: [assets/css/theme.css](assets/css/theme.css)
- Contenido: [index.html](index.html)
- Imágenes: usa CDN y `loading="lazy"`
- CSS: añade `assets/css/custom.css` para sobrescribir
- JS: [assets/js/main.js](assets/js/main.js)

¿Quieres que haga cambios concretos (colores, textos o imágenes) y suba un ejemplo listo para desplegar?
