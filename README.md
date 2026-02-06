# mdpdf

A single-file markdown editor with live preview, syntax highlighting, and PDF export. No build step, no server, no dependencies to install — just open the HTML file in a browser.

## Features

- **Live preview** — side-by-side markdown editing with instant rendered output
- **PDF export** — uses the browser's native print dialog (Save as PDF)
- **Copy as HTML** — one-click copy of the rendered HTML to clipboard
- **Syntax highlighting** — code blocks highlighted via [highlight.js](https://highlightjs.org/)
- **Drag and drop** — drop a `.md` file anywhere on the page to load it
- **GFM support** — tables, task lists, strikethrough, and more

## Usage

Open `index.html` in a browser. That's it.

Or drag and drop any `.md` file onto the page to load it.

## How it works

Everything lives in a single `index.html` file. External dependencies are loaded from CDNs:

- [marked.js](https://marked.js.org/) — markdown parsing
- [highlight.js](https://highlightjs.org/) — syntax highlighting

PDF export uses `window.print()` with a `@media print` stylesheet that hides the editor UI and prints only the rendered preview.
