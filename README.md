# digitec.com.co

Sitio oficial de DIGITEC GLOBAL SAS. Producción en Hostinger, publicada desde este repositorio con la integración Git nativa de Hostinger.

## Cómo se publica

```
editar → commit → push a main → Hostinger (integración Git) → digitec.com.co
```

En hPanel el sitio está conectado a este repositorio como despliegue estático. Para publicar cambios basta hacer push a `main` y redesplegar (o automático si el webhook de auto-deploy está activo en hPanel → Git).

## Contenido

- `index.html` — sitio completo, autocontenido (fuentes, imágenes y lógica embebidas)
- `og.jpg` — imagen para compartir en redes (Open Graph)
- `.htaccess` — HTTPS forzado y compresión
- `robots.txt` / `sitemap.xml` — SEO

## Futuro

Cuando el sitio migre a Next.js, este repositorio pasará a desplegarse con paso de build; el dominio y el flujo no cambian.
