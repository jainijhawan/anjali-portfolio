# Contributing

Thanks for wanting to help! This is a small static site, so contributing is easy.

## Quick start

1. **Fork** this repo and clone your fork.
2. Create a branch: `git checkout -b fix/short-description`
3. Preview locally: `python3 -m http.server 8000` → http://localhost:8000
4. Make your change, then check it in both light and dark mode and at phone width (~375px).
5. Commit with a clear message and open a **Pull Request** against `main`.

## Guidelines

- Keep it **plain HTML/CSS/JS**. Please don't add frameworks, build tools or npm dependencies.
- Use the existing **CSS variables** (`--bg`, `--text`, `--accent`, …) instead of hard-coded colors.
- Keep the site **accessible**: semantic HTML, alt text on images, visible focus, sufficient contrast.
- The site should still **work with JavaScript disabled**.
- Personal content (bio, experience, projects) is up to the site owner. Please open an issue
  before changing it.
- If you're an AI agent or a maintainer, also update [AGENTS.md](AGENTS.md) (Status, Next steps, Change log).

## Reporting issues

Open an issue with what you saw, what you expected, and your browser and device. Screenshots help.

By contributing, you agree that your contributions are licensed under the [MIT License](LICENSE).
