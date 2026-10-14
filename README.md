# Mili Fernández Sabaté — Sitio personal

Landing page personal para presentarme como desarrolladora de software a medida.

Sitio estático (HTML/CSS/JS puro, sin frameworks ni build step).

## Estructura

```
index.html       # Markup del sitio (una sola página)
css/styles.css   # Estilos (dark mode, diseño responsive)
js/i18n.js       # Diccionario de traducciones ES/EN
js/main.js       # Nav móvil, scroll reveal, switch de idioma
assets/          # Imágenes (foto de perfil)
```

## Desarrollo local

```bash
python3 -m http.server 5173
```

Luego abrir http://localhost:5173

## Deploy

Al ser un sitio 100% estático, no requiere build command ni variables de entorno.

### Opción A: Vercel
1. Crear cuenta / loguearse en https://vercel.com
2. "Add New Project" → importar este repo (o usar `vercel` CLI desde esta carpeta)
3. Framework preset: **Other** (sin build command, output directory = raíz)
4. Deploy

### Opción B: GitHub Pages
1. Subir este repo a GitHub
2. Settings → Pages → Source: rama `main`, carpeta `/ (root)`
3. Guardar — el sitio queda publicado en `https://<usuario>.github.io/<repo>/`

## Pendiente

- Sección de Testimonios: está en el HTML pero oculta (`hidden`) hasta tener el testimonio del marido de Mili. Buscar el comentario `<!-- Testimonials -->` en `index.html` para reactivarla.
