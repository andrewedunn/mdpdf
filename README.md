# Markdown to PDF Converter

A single-file Markdown editor with live preview, syntax highlighting, clipboard export, and PDF export. No build step, no server, no dependencies to install. Open the HTML file in a browser.

## Features

- Live preview beside the Markdown editor
- PDF export through the browser print dialog
- Clipboard buttons for Markdown and rendered HTML
- Code block highlighting with [highlight.js](https://highlightjs.org/)
- Drag-and-drop loading for `.md` and `.markdown` files
- GitHub-flavored Markdown support for tables, task lists, and strikethrough
- Crawlable page text, canonical metadata, structured data, sitemap, and no-JavaScript fallback content

## Usage

Open `index.html` in a browser. That's it.

Or drag and drop any `.md` file onto the page to load it.

## How it works

Everything lives in `index.html`. External dependencies are loaded from CDNs:

- [marked.js](https://marked.js.org/) for Markdown parsing
- [highlight.js](https://highlightjs.org/) for syntax highlighting

PDF export uses `window.print()` with a `@media print` stylesheet that hides the editor UI and prints only the rendered preview.
