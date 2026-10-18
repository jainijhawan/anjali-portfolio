# anjali-portfolio

A clean, minimal personal portfolio built with plain HTML, CSS and a little vanilla JavaScript, hosted on GitHub Pages.

**Live:** https://jainijhawan.github.io/anjali-portfolio/

## Features

- No build step and no dependencies: open `index.html` and edit it
- Light and dark themes that follow the OS, with a manual toggle
- Responsive and accessible: skip link, keyboard focus styles, reduced-motion support
- Works without JavaScript

## Run locally

```bash
git clone https://github.com/jainijhawan/anjali-portfolio.git
cd anjali-portfolio
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Project structure

| Path | Purpose |
|---|---|
| `index.html` | All page content |
| `assets/css/style.css` | Styles (colors are CSS variables at the top) |
| `assets/js/main.js` | Theme toggle, mobile menu, small animations |
| `404.html` | Not-found page |
| `AGENTS.md` | Project memory and handoff log for maintainers and AI agents |

## Contributing

Contributions are welcome. Fixes, accessibility improvements and design polish are all appreciated.
See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE)
