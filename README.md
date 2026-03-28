# XIII Coloquio Internacional de Lenguaje y Cultura

Proyecto base en **Astro** para el sitio web del Coloquio.

## 1. Instalar dependencias

```bash
npm install
```

## 2. Ejecutar en modo local

```bash
npm run dev
```

Luego abre en el navegador la URL que te muestre la terminal.

## 3. Estructura principal

- `src/pages/index.astro`: página principal
- `src/components/Header.astro`: menú superior
- `src/components/Footer.astro`: pie de página
- `src/layouts/BaseLayout.astro`: estructura base HTML
- `src/styles/global.css`: estilos del sitio
- `.github/workflows/deploy.yml`: despliegue automático a GitHub Pages

## 4. Qué debes editar primero

### Textos
Edita en `src/pages/index.astro`:
- presentación
- objetivos
- justificación
- ejes temáticos
- conferencistas
- convocatoria
- fechas importantes
- datos de contacto

### URL del sitio
Edita `astro.config.mjs`.

Si vas a publicar primero en GitHub Pages con la URL del repositorio, puedes usar:

```js
export default defineConfig({
  site: 'https://TU-USUARIO.github.io',
  base: '/xiii-coloquio-lenguaje-cultura',
  integrations: [sitemap()],
});
```

Cuando compres y conectes el dominio propio, cambia a algo así:

```js
export default defineConfig({
  site: 'https://tudominio.com',
  integrations: [sitemap()],
});
```

## 5. Publicar en GitHub Pages

Astro recomienda crear el proyecto con `npm create astro@latest` y desplegar en GitHub Pages mediante GitHub Actions. La documentación oficial también indica el flujo recomendado con un archivo `.github/workflows/deploy.yml`. citeturn0search0turn0search1

Pasos generales:

1. Crear repositorio en GitHub.
2. Subir este proyecto.
3. En GitHub, ir a **Settings > Pages**.
4. En **Build and deployment**, escoger **GitHub Actions**.
5. Hacer push a la rama `main`.
6. Esperar a que el workflow publique el sitio.

## 6. Dominio propio después

GitHub Pages permite usar dominio personalizado. GitHub recomienda configurar primero el dominio en el repositorio y luego ajustar los DNS con el proveedor del dominio. citeturn0search1
