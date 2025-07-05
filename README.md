# Astrofy | Personal Portfolio Website Template

## Despliegue

1. Instala las dependencias con `npm install` o `pnpm install`.
2. Ejecuta `npm run build` para generar la versión de producción en la carpeta `dist/`.
3. Publica el contenido de `dist/` en tu proveedor de hosting estático favorito.

Este repositorio incluye un flujo de trabajo de GitHub Actions (`.github/workflows/astro.yml`) que compila y despliega el sitio en GitHub Pages cuando haces push a la rama `main`. Configura el secreto `GH_TOKEN` con un token de acceso personal para habilitar este despliegue automático.
