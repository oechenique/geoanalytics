# geoanalytics: resumen en español

[🇬🇧 English](README.md)

Landing estática que junta en un solo lugar mis repos de GIS con Python: seis tarjetas, una por tema, y cada una lleva a su repositorio. Está en vivo en [oechenique.github.io/geoanalytics](https://oechenique.github.io/geoanalytics/).

- **Qué hay**: un único `index.html`, sin build ni dependencias. El código Python vive en los repos que linkea (`python-gis-basics`, `Geocoding`, `analytics`, `data-engineering`, `remote_sensing`, `ai-predictions`).
- **Deploy**: GitHub Pages compila desde `main` (carpeta `/`) sin workflow propio, así que cada merge a `main` vuelve a publicar el sitio. También se sirve todo lo que esté en la raíz y no empiece con `.` o `_`, como este README.
- **Idiomas**: inglés, español, portugués y japonés. Primero manda `?lang=xx`, después la última elección guardada en `localStorage` y por último el idioma del navegador.
- **Analítica**: GA4 con `gtag.js` y un contenedor de Google Tag Manager. Los valores por defecto del consent mode se definen *antes* de configurar cualquier tag: en la UE arrancan denegados y en el resto del mundo, concedidos.
- **Límites**: la tarjeta *AI & Predictions* lleva a un repo que por ahora tiene solo un README. Si el contenedor de GTM también dispara un tag de GA4 con el mismo ID, cada visita se cuenta dos veces, y eso solo se puede verificar en la UI de GTM.
- **Licencia**: el código está bajo MIT ([LICENSE](LICENSE)). Las imágenes de `img/` y `docs/img/` son © Gastón Echenique, todos los derechos reservados. Son originales: algunas salieron de mis notebooks de Python y otras las hice con ayuda de IA (ChatGPT). La licencia MIT no las cubre.
