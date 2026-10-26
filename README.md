# Mili Fernández Sabaté — Sitio personal

Landing page personal para presentarme como desarrolladora de software a medida.

Sitio estático (HTML/CSS/JS puro, sin frameworks ni build step), en línea en
**https://milifs.github.io/**

## Estructura

```
index.html                    # Markup del sitio (una sola página)
css/styles.css                # Estilos (dark mode, diseño responsive)
js/i18n.js                    # Diccionario de traducciones ES/EN
js/main.js                    # Nav móvil, scroll reveal, switch de idioma
assets/profile.jpg            # Foto de perfil
assets/og.jpg                 # Preview 1200x630 al compartir el link
assets/favicon.svg            # Favicon
assets/apple-touch-icon.png   # Ícono para pantalla de inicio en iOS
tools/                        # Plantillas para regenerar og.jpg y el ícono
```

## Desarrollo local

```bash
python3 -m http.server 5173
```

Luego abrir http://localhost:5173

## Deploy

GitHub Pages, desde la rama `main` y la carpeta raíz
(Settings → Pages → Source). No hay build command ni variables de entorno:
cada push a `main` republica el sitio en un par de minutos.

## Notas

- **Metadatos para compartir:** `index.html` declara Open Graph y Twitter Card
  con URLs absolutas a `https://milifs.github.io/`. Si el dominio cambia, hay
  que actualizarlas a mano. Después de cambiar `assets/og.jpg` conviene pasar la
  URL por el Post Inspector de LinkedIn para que refresque su cache.

- **Clase `js` en el `<html>`:** un script inline en el `<head>` la agrega, y el
  CSS oculta los elementos `.reveal` solo cuando está presente. Así, si el JS no
  carga, el contenido se ve igual en lugar de quedar invisible.

## Pendiente

- **Sección de Testimonios:** está en el HTML pero oculta con `hidden` hasta
  tener testimonios reales. Buscar el comentario `<!-- TESTIMONIOS -->` en
  `index.html`, sumar cada testimonio con la estructura que figura ahí y quitar
  el atributo `hidden` de la sección.
