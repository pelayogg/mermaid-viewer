# Mermaid Viewer

Visor y editor de diagramas [Mermaid](https://mermaid.js.org) en un único `index.html`, sin build, desplegable en GitHub Pages.

Alternativa minimalista y editorial a [mermaid.live](https://mermaid.live) con varias mejoras de UX.

![preview](https://img.shields.io/badge/stack-vanilla%20HTML-1a1a1a) ![mermaid](https://img.shields.io/badge/mermaid-11.x-3a6bea) ![license](https://img.shields.io/badge/license-MIT-888)

## Demo

GitHub Pages: <https://pelayogg.github.io/mermaid-viewer/>

## Features

| Capacidad | Detalle |
|-----------|---------|
| Render en vivo | Debounce 220 ms, indicador de estado (ok / busy / error) |
| Editor decente | CodeMirror 5 con números de línea, active line, brackets, tab=2 espacios |
| Errores legibles | Barra inferior con el mensaje del parser de Mermaid |
| 12 plantillas | flowchart, sequence, class, state, ER, gantt, journey, pie, mindmap, timeline, gitgraph, C4 |
| Temas Mermaid | default · neutral · dark · forest · base |
| Pan & Zoom | `svg-pan-zoom`, botones +/−/fit/1:1 y pantalla completa |
| Exportar | SVG, PNG @2x (fondo blanco), `.mmd`, copiar SVG al portapapeles |
| Share por URL | Formato `#pako:…` **compatible con mermaid.live** (mismo deflate+base64url) |
| Autosave | `localStorage` con timestamp en el footer |
| Abrir fichero | Botón Abrir o drag & drop sobre el panel |
| Format | Reindentado básico de 2 espacios respetando `end`/`subgraph` |
| Atajos | `⌘/Ctrl+S` share · `⌘/Ctrl+O` abrir · `⇧⌥F` format · `Esc` salir fullscreen |
| Splitter | Arrastrable, responsive (vertical en móvil) |
| Sin build | Un solo HTML, todo desde CDN |

## Diferencias frente a mermaid.live

- **Diseño editorial** (light, tipografía Inter, acentos azul/naranja inspirados en el sistema de diseño interno de Inditex).
- **Galería de plantillas integrada** (mermaid.live solo expone Sample Diagrams).
- **PNG export con DPR 2x y fondo blanco** sin pasar por mermaid.ink.
- **Drag & drop de ficheros** directo al editor.
- **Compatible con enlaces de mermaid.live** (mismo encoding `pako:`), por lo que puedes pegar URLs cruzadas.
- **Cero telemetría, cero login, cero backend.**

## Desarrollo local

```bash
# Sirve estático en :8080
npx serve .
# o bien:
python3 -m http.server 8080
```

Abre <http://localhost:8080>.

## Despliegue

GitHub Pages se publica automáticamente en cada push a `main` vía workflow (`.github/workflows/pages.yml`). El sitio queda en `https://<user>.github.io/mermaid-viewer/`.

## Licencia

MIT — ver [LICENSE](LICENSE).
