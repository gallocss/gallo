# 🐓 Gallo CSS

[![npm version](https://img.shields.io/npm/v/@gallocss/gallo?color=e8931a)](https://www.npmjs.com/package/@gallocss/gallo)
[![License](https://img.shields.io/badge/license-MIT-e8931a)](./LICENSE.md)

A classless CSS framework with character. Drop in one stylesheet, write semantic HTML, get a beautiful result with three baked-in themes including the signature **Gallo** dark theme.

- 🎨 Three themes — Light, Dark &  Gallo
- 🏷️ Classless — pure semantic HTML
- ⚡ Zero dependencies, zero build step for users
- 📦 ~10 KB minified
- 🎛️ Fully customizable via CSS variables

---

## Quick start

### CDN (fastest)

```html
<!-- Latest minified -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@gallocss/gallo/gallo.min.css">

<!-- Pin to a version -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@gallocss/gallo@1.0.1/gallo.min.css">
```

### npm

```bash
npm install @gallocss/gallo
```

Then in your HTML:
```html
<link rel="stylesheet" href="node_modules/@gallocss/gallo/gallo.min.css">
```

Or import in your CSS/JS bundler:
```css
import "@gallocss/gallo/gallo.css";
```

### Download manually

Grab `gallo.min.css` from the [latest release](https://github.com/gallocss/gallo/releases/latest) and link it in your `<head>`.

---

## Themes

Switch themes by setting `data-theme` on your `<html>` element:

```html
<html data-theme="light">   <!-- default -->
<html data-theme="dark">
<html data-theme="gallo">   <!-- signature warm dark theme -->
```

Toggle with JavaScript:
```js
document.documentElement.dataset.theme = 'dark'
```

Auto-detect system preference:
```js
if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
  document.documentElement.dataset.theme = 'dark'
}
```

---

## CSS Variables

All design tokens are CSS custom properties prefixed with `--g-`. Override any of them in your own stylesheet:

```css
:root {
  --g-accent:  hotpink;
  --g-radius:  0px;        /* go full square */
  --g-measure: 80ch;       /* wider line length */
  --g-font:    "Georgia", serif;
}
```

| Token | Description |
|---|---|
| `--g-bg` | Page background |
| `--g-bg-alt` | Alternate background (code, table rows) |
| `--g-surface` | Surface background (cards, dialogs) |
| `--g-border` | Border color |
| `--g-text` | Primary text color |
| `--g-text-muted` | Secondary / muted text |
| `--g-accent` | Accent color (links, buttons, focus) |
| `--g-accent-fg` | Text on accent background |
| `--g-accent-h` | Accent hover state |
| `--g-focus` | Focus ring color (rgba) |
| `--g-danger` | Destructive action color |
| `--g-success` | Success state color |
| `--g-radius` | Base border radius |
| `--g-radius-lg` | Large border radius |
| `--g-font` | Body font stack |
| `--g-mono` | Monospace font stack |
| `--g-sans` | Sans-serif stack (UI elements) |
| `--g-leading` | Line height |
| `--g-measure` | Max line width |
| `--g-form-gap` | Spacing between form elements |

---

## Browser support

Tested on the latest stable versions of Chrome, Firefox, Safari, and Edge.

---

## License

[MIT](./LICENSE)