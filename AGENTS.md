# AGENTS.md — Project memory & handoff log

> **For any AI coding agent (Claude, Codex, Copilot, Cursor, …) or human picking this up:**
> Read this whole file before making changes. It is the single source of truth for
> project context, decisions, current status, and what to do next.
> **After every change you make, update the "Status", "Next steps" and "Change log"
> sections below and commit this file together with your change.**

---

## 1. Project at a glance

| Item | Value |
|---|---|
| What | Personal portfolio website |
| Repo | https://github.com/jainijhawan/anjali-portfolio (public, open to contributions) |
| Live site | https://jainijhawan.github.io/anjali-portfolio/ |
| Hosting | GitHub Pages, deployed from branch `main`, folder `/` (root) — no build step |
| GitHub account | `jainijhawan` (sign in with jainijhawan@gmail.com) |
| Stack | Plain HTML + CSS + vanilla JS. No frameworks, no bundler, no npm. |
| Design | Clean minimal; light/dark follows OS, with a manual toggle saved in `localStorage` |

## 2. File map

```
index.html              All page content (hero, about, experience, projects, skills, contact)
404.html                Not-found page (uses absolute /anjali-portfolio/ paths — see gotchas)
assets/css/style.css    All styles. Colors are tokens on :root; dark theme overrides below them
assets/js/main.js       Theme toggle, mobile nav, footer year, scroll fade-in (optional enhancements)
assets/img/favicon.svg  Favicon
.nojekyll               Tells GitHub Pages to serve files as-is (skip Jekyll)
AGENTS.md               THIS FILE — project memory / handoff log
CLAUDE.md               Points Claude Code at this file
README.md               Public-facing readme
CONTRIBUTING.md         How outside contributors propose changes
.github/                PR + issue templates
```

## 3. How to work on it

**Preview locally** (any static server works):

```bash
python3 -m http.server 8000
```

then open http://localhost:8000.

**Deploy:** push to `main`. GitHub Pages rebuilds automatically within ~1 minute.
Check the deployment status with `gh api repos/jainijhawan/anjali-portfolio/pages/builds/latest --jq .status`.

**Set up on a new machine:**

```bash
brew install gh            # or see https://cli.github.com
gh auth login              # sign in as jainijhawan
gh repo clone jainijhawan/anjali-portfolio
cd anjali-portfolio
git config user.name "Jai Nijhawan"
git config user.email "jainijhawan@gmail.com"
```

## 4. Conventions & decisions

- **No build step.** Keep it plain HTML/CSS/JS so anyone can contribute and Pages serves it directly.
- **Content lives in `index.html`.** Each repeatable block (role, project) has a `TODO(content)` comment
  marking the template to copy. Search for `TODO(content)` to find unfilled spots.
- **Colors only via CSS tokens** in `:root` (light) and the two dark-mode blocks. When adding a token,
  add it to all three blocks.
- **Site must work without JS.** JS only adds enhancements.
- **Accessibility:** keep the skip link, `aria-*` on toggles, visible focus styles, and `prefers-reduced-motion` support.
- **Contributions:** outside contributors fork and open a PR against `main` (see CONTRIBUTING.md).
  The owner reviews and merges. Don't push directly to `main` on others' behalf without the owner's OK.
- Repo name chosen by the owner: "anjali portfolio" → `anjali-portfolio` (GitHub doesn't allow spaces).

### Gotchas

- The site is served from a **sub-path** (`/anjali-portfolio/`). Use **relative** paths in `index.html`.
  `404.html` must use **absolute** `/anjali-portfolio/...` paths because it's served at arbitrary URLs.
  If the repo is ever renamed, update the paths in `404.html` and the links in this file and README.md.
- The account also has an older, separate portfolio at https://jainijhawan.github.io
  (repo `jainijhawan/jainijhawan.github.io`). Don't touch it from this project.

## 5. Status (keep current)

- ✅ Site skeleton built (all sections, light/dark, responsive, 404 page)
- ✅ Public repo created, GitHub Pages enabled
- ⏳ **Real content not added yet**: every section still has `[placeholder]` text. Still open:
  whose portfolio this is (name/initials), headline, bio, experience, projects, skills, contact links.

## 6. Next steps

1. Get the portfolio owner's content (name, headline, bio, experience, projects, skills, email, LinkedIn/GitHub)
   and replace every `[placeholder]` / `TODO(content)` in `index.html`. Also update `[Your Name]` in `404.html`
   and the favicon letter in `assets/img/favicon.svg`.
2. Optional: add a profile photo (`assets/img/`), a résumé PDF link, and an Open Graph preview image.
3. Optional: add a custom domain (CNAME file + DNS) if wanted.

## 7. Change log (newest first)

Format: `YYYY-MM-DD — agent/person — what changed and why`

- 2026-10-18 — Claude (Claude Code) — Initial scaffold: index.html, 404.html, CSS, JS, favicon, `.nojekyll`,
  README, CONTRIBUTING, MIT LICENSE, PR/issue templates, this AGENTS.md + CLAUDE.md. Created public repo
  `jainijhawan/anjali-portfolio` and enabled GitHub Pages from `main` /. Name fields use `[Your Name]`
  placeholders until the owner confirms whose portfolio it is.
