# CLAUDE.md

See [AGENTS.md](AGENTS.md) for all project guidance — context, code style, the web design system, content rules, image handling, verification steps, and git safety. Keep that file as the single source of truth; update it (not this file) when guidance changes.

## Quick reference

- Single-page static Bootstrap site in `docs/index.html`, served via GitHub Pages from `docs/` on `main`. All published files live under `docs/`.
- Theme: Bootswatch Minty (Bootstrap 5.3.3) via jsDelivr CDN. Custom styling in `docs/assets/style.css` (the SPA "load curve" design system) layered on top — prefer Bootstrap utilities first.
- Australian spelling. Keep copy professional and faithful to supplied material; don't invent credentials or claims.
- Keep diffs small and focused. Don't revert unrelated user changes or run destructive git commands unless asked.
