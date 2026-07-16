# digitec.com.co

Sitio oficial de DIGITEC GLOBAL SAS. Producción en Hostinger, publicado automáticamente desde GitHub.

## Cómo se publica

Cada push a `main` dispara el workflow **Desplegar a Hostinger** (GitHub Actions), que sube el contenido de `site/` al `public_html` del dominio por FTPS. Nadie sube archivos a mano.

```
editar site/ → commit → push a main → GitHub Actions → Hostinger → digitec.com.co
```

También se puede lanzar manualmente desde la pestaña Actions (workflow_dispatch).

## Secrets requeridos (Settings → Secrets and variables → Actions)

| Secret | Valor |
|---|---|
| `FTP_SERVER` | Host FTP del sitio en Hostinger |
| `FTP_USERNAME` | Usuario FTP (cuenta con raíz en el public_html de digitec.com.co) |
| `FTP_PASSWORD` | Contraseña de esa cuenta FTP |

## Estructura

- `site/` — contenido publicado tal cual (index.html autocontenido, og.jpg, .htaccess, robots.txt, sitemap.xml)
- `.github/workflows/deploy.yml` — pipeline de despliegue

## Futuro

Cuando el sitio migre a Next.js (repo Digitec), este mismo workflow gana un paso de build y el destino no cambia.
