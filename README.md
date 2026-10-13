# Editor de programaciones didácticas · CPM «Javier Perianes» (Huelva)

Herramienta web (un solo archivo, `index.html`) para actualizar una programación didáctica del curso anterior a la nueva normativa (Decreto 483/2026, de 31 de agosto, y Orden de 31 de agosto de 2026) y exportarla a **Word** o **PDF**.

## Qué hace
- Lee una programación en **PDF** o **Word (.docx)** y la divide en secciones.
- Muestra el original y una versión editable, lado a lado.
- Tabla de **cambios en normativa**: detecta los puntos de la programación afectados (convocatoria extraordinaria en septiembre, final de curso en 6.º, Departamento de Orientación, apartado de revisión…), explica el porqué y propone un texto en verde frente al original en rojo.
- Permite cambiar la portada y el curso (con la portada original como base cuando se sube un PDF).
- Incluye un informe del cotejo previo de las 66 programaciones del centro.
- Exporta a Word (con índice actualizable) y a PDF (desde el diálogo de impresión del navegador).

## Privacidad
Todo se procesa **en el navegador**: las programaciones que se suben no se envían a ningún servidor.

## Cómo publicarlo en GitHub Pages
1. Crea un repositorio en GitHub (por ejemplo `editor-programaciones`).
2. Sube los archivos de esta carpeta (`index.html`, `.nojekyll`, `README.md`).
3. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `/ (root)` → Save**.
4. En un par de minutos estará en `https://TU-USUARIO.github.io/editor-programaciones/`.

## Dependencias (se cargan desde CDN, hace falta conexión)
| Librería | Versión | Uso |
|---|---|---|
| mammoth | 1.6.0 (cdnjs) | leer .docx |
| pdf.js | 3.11.174 (cdnjs) | leer PDF y recortar la portada |
| docx | 8.5.0 (jsDelivr) | generar el Word |

Si quieres que funcione sin conexión, descarga esas tres librerías, guárdalas junto a `index.html` y cambia las tres etiquetas `<script src=...>` por rutas locales.

## Notas
- El archivo lleva `noindex` para que los buscadores no lo indexen. Quita la línea `<meta name="robots" ...>` si quieres lo contrario.
- El informe del cotejo incluye extractos de las programaciones del centro (ya publicadas en el blog del conservatorio). Revisa que no quieras ocultarlos antes de hacer público el repositorio.
- Los textos normativos se basan en el resumen oficial del Decreto 483/2026; contrasta las fechas con el BOJA y con la Orden de 31 de agosto de 2026.
- Los logos de la Junta de Andalucía y del conservatorio van incrustados en el HTML.
