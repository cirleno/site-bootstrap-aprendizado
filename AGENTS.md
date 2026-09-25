# Repository guide

## Structure
- Static, pt-BR Bootstrap exercise site. `Index.html` is the app entrypoint; `404.html` is a standalone error page; app-wide overrides live in `style/style.css`.
- The page originated in Ricardo Sanches' Bootstrap 4 course. Lorem/Mussum paragraphs and dummy form data are intentional exercise content, not placeholder defects.
- `package.json` is metadata only: there are no local dependencies, scripts, build, test, lint, formatter, or typecheck commands. Do not add an npm workflow unless requested.

## Preview and verification
- No install step. Serve the repository root over HTTP and open `/Index.html`; a `file://` preview will not resolve the leading-slash favicon links faithfully.
- Bootstrap 5.3.8 CSS/bundle and Bootstrap Icons 1.11.3 are pinned in `Index.html` via jsDelivr; internet is required for CDN assets and YouTube embeds. If changing a CDN version, update its SRI hash.
- No automated checks are defined; verify UI changes manually in a browser, including responsive navigation and JavaScript components.

## Constraints
- Runtime target is Bootstrap 5.3, not the course's Bootstrap 4: retain `data-bs-*`, current spacing/accessibility utilities, and vanilla JavaScript. Do not restore jQuery, `data-toggle`, `jumbotron`, `embed-responsive`, `sr-only`, or `ml-*`/`mr-*`.
- Custom JavaScript is inline at the end of `Index.html`; there is no backend, and the contact form only performs client-side validation.
- Root-relative URLs assume the repository is deployed at its root. Preserve the exact case of `Index.html`, `Images/`, and `style/`.
- Keep user-facing copy in pt-BR and honor `.editorconfig` (UTF-8, LF, two spaces, final newline).
- `.agents/`, `agent/`, `skills-lock.json`, and `Novo Documento de Texto.txt` are gitignored local tooling, not site sources.
