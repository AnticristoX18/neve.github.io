# Névé: Arte Helado

Landing page de una sola página para Névé, un concepto de aguas frescas. Sitio estático (HTML + CSS + JS en un solo archivo, sin dependencias ni build), optimizado para móvil y escritorio.

## ⚠️ Antes de publicar

Edita el número de WhatsApp en `index.html` (cerca del final, dentro de la etiqueta `<script>`):

```js
const WHATSAPP_NUMBER = "521XXXXXXXXXX";
```

Reemplázalo por el número real en formato internacional sin signos ni espacios (ej. `5215512345678`).

## Estructura

```
.
├── index.html     # Toda la página (HTML, CSS y JS inline)
├── .nojekyll      # Evita que GitHub Pages procese el sitio con Jekyll
└── .gitignore
```

## Ver el sitio en local

No requiere instalación. Basta con abrir `index.html` en el navegador, o levantar un servidor simple:

```bash
python3 -m http.server 8000
# luego abre http://localhost:8000
```

## Subir a GitHub

```bash
git init
git add .
git commit -m "Sitio Névé: Arte Helado"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/TU-REPO.git
git push -u origin main
```

## Publicar con GitHub Pages

1. Ve a tu repositorio en GitHub → **Settings** → **Pages**.
2. En **Source**, elige la rama `main` y la carpeta `/ (root)`.
3. Guarda. En un par de minutos el sitio quedará disponible en:
   `https://TU-USUARIO.github.io/TU-REPO/`

## Notas técnicas

- Sin frameworks ni dependencias externas: un solo archivo `index.html`.
- Responsive: menú hamburguesa en móvil, carrusel táctil de sabores en móvil/tablet y cuadrícula fija en escritorio.
- Usa `100dvh` con fallback a `100vh` para evitar saltos de layout en Safari/iOS.
- Respeta `prefers-reduced-motion` para usuarios sensibles a animaciones.
