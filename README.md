# CV / Portfolio — Franco Barrionuevo

Sitio de una sola página (CV interactivo + versión imprimible / ATS) hecho con
**Astro 6** y **Tailwind CSS v4**.

## Estructura

```
src/
├── layouts/Layout.astro     # <head>: SEO, Open Graph, JSON-LD (Person), fuentes
├── pages/index.astro        # Contenido del CV (hero, experiencia, skills, formación)
├── components/
│   └── FloatingContact.astro # Botones flotantes: WhatsApp, llamar, mail, imprimir
└── styles/global.css        # Tailwind + tokens de tema (--font-display, etc.)
public/
├── favicon.svg
├── robots.txt
└── og.png                   # 1200×630 — imagen de previsualización al compartir (agregar)
```

Los datos de contacto y enlaces viven en el objeto `data` al inicio de
`src/pages/index.astro`.

## Comandos

| Comando          | Acción                                        |
| :--------------- | :-------------------------------------------- |
| `npm install`    | Instala dependencias                          |
| `npm run dev`    | Servidor local en `localhost:4321`           |
| `npm run build`  | Build de producción en `./dist/`            |
| `npm run preview`| Previsualiza el build                         |

## Deploy

Configurado para **Cloudflare Pages** (`wrangler.json`, salida en `./dist`).

## Pendiente

- Agregar `public/og.png` (1200×630) para las previsualizaciones al compartir.
- Opcional: `npx astro add sitemap` para generar `sitemap-index.xml`.
