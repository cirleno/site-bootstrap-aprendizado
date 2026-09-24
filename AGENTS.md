# AGENTS.md

## Overview
- Static single-page Bootstrap 5 exercise site (pt-BR text). Only page: `Index.html`. No build system, no tests, no lint.
- Based on the "Curso de Bootstrap 4 (Ricardo Sanches)" YouTube series; body text is intentional Lorem/Mussum demo filler.

## Running
- No dependencies required — the page loads everything from CDNs: Bootstrap 5.3.8 (CSS + JS bundle from jsDelivr), Bootstrap Icons 1.11.3, jQuery **not** used (Bootstrap 5 = vanilla JS). Just open `Index.html` in the browser.
- Requires internet for the CDN links in `<head>` and at the end of `</body>`.

## Gotchas
- Target is Bootstrap 5.3 (`data-bs-*` attributes, `ratio ratio-16x9`, `visually-hidden`, `btn-close`) — don't reintroduce Bootstrap 4/alpha syntax (`data-toggle`, `data-target`, `jumbotron`, `embed-responsive`, `navbar-inverse`, `navbar-toggleable-*`, `sr-only`, `ml-`/`mr-`).
- Backend has no jQuery; interactive bits use vanilla JS (`document.querySelectorAll` + `new bootstrap.Popover(...)` for the only popover).
- Custom CSS lives only in `style/style.css`. `bg-white` is native Bootstrap (don't re-add the old custom rule).
- `.agents/`, `agent/`, `skills-lock.json`, and `Novo Documento de Texto.txt` are gitignored local tooling, not part of the site.

## Conventions
- Keep user-facing text in pt-BR.