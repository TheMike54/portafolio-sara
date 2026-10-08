# portafolio-sara — portafolio web de Sarai Lara Méndez

Página estática (un solo `index.html`, sin build) con el portafolio de Sarai Lara Méndez: Derecho, relaciones internacionales y política. Mientras ella escoge, lleva una barra para cambiar entre 3 propuestas, 4 paletas y el modo del botón de WhatsApp.

<!-- plantilla: proyecto v1 · variante 1 · 2026-10-08 -->

## Primero
Leer `ESTADO.md`.

## Comandos
- Ver en local: `python -m http.server 8765 --bind 127.0.0.1 --directory Z:\Jueguitos\Proyectitos\portafolio-sara` y abrir `http://127.0.0.1:8765/`.
- Verificar un cambio: no hay pruebas ejecutables. Mirar las 3 propuestas en celular (390 px) y en 1280×720, 1920×1080 y 2560×1440: sin barra horizontal, sin fotos encimadas al texto y con todas las secciones visibles al bajar. En la sesión de Miguel se prueba con Claude in Chrome (Brave); Brave no baja de 500 px de ancho, así que el celular se mide con Playwright de Python.

## Entorno y trampas
- El repo es público y GitHub Pages publica la rama `main` en `https://themike54.github.io/portafolio-sara/`: un push es publicar.
- `referencias\` (transcripción de la llamada, capturas del TikTok) no se sube: está en `.gitignore`.
- La URL guarda la propuesta escogida (`#p3-dorado-burbuja`); `localStorage` la recuerda con la llave `portafolio-sarai`.
- Las fuentes vienen de Google Fonts: sin internet la página cae a fuentes del sistema.

## Decisiones cerradas
- Celular primero: Sarai lo va a abrir sobre todo desde el celular. En celular el menú es un botón "Menú" desplegable; la fila deslizable se veía cortada.
- Una sola página con selector de propuesta, no tres archivos: lo pidió Miguel para que ella compare.
- Todo sobre el azul marino "Noche" (`#0E1424`): es el color que ella escogió. Las paletas solo cambian letras y acentos.
- Las 3 propuestas llevan animaciones al bajar; la 1 sutil (valores de Lumina: 8 px, 520 ms, `cubic-bezier(.2,.7,.3,1)`), la 3 fuerte. Todas respetan "reducir movimiento".
- La propuesta 3 toma del TikTok el encaje, el clip, el fotomatón y los títulos en cursiva; nunca objetos encima del texto ni letra chica.
- FAISA, ABogatitos y Escencia van primero y grandes; donde solo colaboró (Cámara, Senado, PRI, embajadas) va en segundo plano.

## Reglas de este proyecto
- Los textos son de Sarai: se recortan con sus palabras, no se reescriben ni se agregan cargos, fechas o logros. Lo que falta se deja como hueco visible ("pendiente").
- Su nombre es Sarai Lara Méndez (sin h).
- No subir datos que ella no haya dado para publicar.
- Git: Claude hace commit; el push lo autoriza Miguel cada vez, porque publica en GitHub Pages. Los commits llevan atribución de IA.
- Lo reemplazado va a `_archivo\` con la fecha al inicio del nombre; no se borra. Las claves van solo en `.env`.

## Dónde está lo demás
| Qué | Dónde | Cuándo leerlo |
|---|---|---|
| Estado, pendientes y fechas | `ESTADO.md` | Al empezar |
| Llamada con Sarai del 2026-10-08 (lo que pidió) | `referencias\llamada-2026-10-08_transcript.md` | Antes de cambiar contenido o diseño |
| Capturas del TikTok que le gustó | `referencias\tiktok\` | Al tocar la propuesta 3 |
| Fotos que sí se publican | `fotos\` | Al poner fotos |
