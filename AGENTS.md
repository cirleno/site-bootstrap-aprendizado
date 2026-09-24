# AGENTS.md

## Overview
- Static single-page Bootstrap 4 exercise site (pt-BR text). Only page: `Index.html`. No build system, no tests, no lint.
- Based on the "Curso de Bootstrap 4 (Ricardo Sanches)" YouTube series; body text is intentional Lorem/Mussum demo filler.

## Running
- No dependencies required — the page loads everything from CDNs: Bootstrap 4.0.0-alpha.6 (CSS + JS), jQuery 3.2.1. Just open `Index.html` in the browser.
- Requires internet for the CDN links in `<head>` and at the end of `</body>`.

## Gotchas
- Target is Bootstrap 4 alpha (`navbar-expand-lg`, `data-toggle="pill"`) loaded from CDN — don't introduce Bootstrap 5 syntax or switch the CDN to a newer 4.x (classes like `bg-gradient-primary` only exist in alpha/beta).
- Custom CSS lives only in `style/style.css`. Ignore `.sass-cache/` (Ruby Sass watcher output).
- jQuery is loaded via CDN before the inline `$(...)` popover init script — keep that order.
- `package.json` is metadata-only (no dependencies); `pnpm-lock.yaml`, `package-lock.json`, and `node_modules/` are leftovers of the old local-server setup. `node_modules/` is gitignored.
- `.agents/`, `agent/`, `skills-lock.json`, and `Novo Documento de Texto.txt` are gitignored local tooling, not part of the site.

## Conventions
- Keep user-facing text in pt-BR.