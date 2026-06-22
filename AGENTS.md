# AGENTS.md

## Project Context

This is a static website for Slim Power Advisory (SPA), an electrical and power consulting business. The site is a single-page Bootstrap HTML site in `docs/index.html`.

The site is served via GitHub Pages from the `docs/` folder on the `main` branch. All published files (HTML, CSS, images) must live under `docs/`.

## Code Style

- Keep edits simple, explicit, and easy to review.
- Prefer small, focused changes over broad refactors.
- Preserve the existing Bootstrap-based structure unless there is a clear reason to change it.
- Use double quotes for HTML attributes.
- Keep indentation consistent with the existing file: two spaces.
- Avoid comments that simply restate what the markup already says.

## Web Design Guidelines

- Use Bootstrap classes and components as much as possible for layout, spacing, typography, responsive behaviour, and common UI patterns.
- The site uses the **Bootswatch Minty** theme (Bootstrap 5.3.3) loaded from jsDelivr CDN. Do not swap the theme CDN link without being asked.
- The SPA design system lives in `docs/assets/style.css`, layered on top of Minty. Only add CSS there for styling Bootstrap utility classes cannot express cleanly; keep additions minimal and avoid duplicating utility classes.
- Prefer Bootstrap responsive grid and utility classes before adding custom media queries.
- Keep the visual style restrained, professional, and suitable for an advisory business. Avoid decorative clutter, gradients, and unnecessary visual effects.

### Design system

Direction "the load curve" — calm, authoritative, grounded in the electricity-network subject matter. Spend boldness on the one signature element (the hero load curve); keep everything else quiet.

- **Palette** (CSS custom properties in `style.css`, also re-pointed at Bootstrap's `--bs-*` tokens):
  - `--spa-ink` `#0B1F2A` — dark slate ground (hero, footer, profile sidebar) and heading text
  - `--spa-teal` `#0E7C7B` — primary; `--spa-teal-d` `#0A5D5C` darker variant
  - `--spa-amber` `#E8A317` — accent, used sparingly (CTA, signature); `--spa-amber-d` `#C7860B` hover
  - `--spa-mist` `#F5F7F7` — alternating section background (`.section--mist`)
  - `--spa-body` `#4A5A61` body text; `--spa-line` `#DCE4E5` borders
- **Type:** Bootswatch Minty's stock font stack — no custom web fonts. Headings carry only colour + `letter-spacing` overrides. `.eyebrow` = uppercase, tracked, weight-600 label (`.eyebrow.on-dark` switches it to amber on dark grounds).
- **Signature:** an animated SVG daily-demand load curve traced across the dark hero on load (`.hero-curve`, amber stroke). Respects `prefers-reduced-motion`. Don't add competing animations elsewhere.
- **Components:** quiet bordered service tiles (`.svc`, not drop-shadow cards); three-panel advisor block (`.profile`). Buttons: `.btn-amber` (deepens fill to `--spa-amber-d` on hover/focus-visible, keeps ink text); `.hero .btn-outline-light` shifts border+text to amber on hover instead of Bootstrap's white-fill flip.
- Keep a quality floor: responsive to mobile, visible keyboard focus (amber outline), reduced motion respected.
- Avoid the generic AI-design defaults (cream + ornate serif + terracotta; near-black + acid-green; broadsheet hairline columns).

## Content Guidelines

- Keep copy professional, clear, and business-focused.
- Use Australian spelling where applicable, such as `organisation`, `optimise`, and `favour`.
- Do not invent credentials, employment history, locations, contact details, or client claims.
- If content is taken from LinkedIn, screenshots, or other supplied references, stay faithful to the provided material.
- Keep Sarah Lim's profile content aligned with:
  - energy infrastructure leadership
  - business cases
  - regulation
  - asset management
  - innovation
  - commercially sound investment decisions
  - Australia's energy transition

## Images

- Store project images in `docs/assets/`.
- Use descriptive filenames, for example `sarah-lim.png`.
- Reference images with paths relative to `docs/index.html`, for example `assets/sarah-lim.png`.
- Prefer local images over remote hotlinks.
- When replacing an image, verify the file renders correctly and is referenced from `docs/index.html`.

## Verification

After edits, check:

- The page still loads as plain static HTML.
- Navigation anchor links still work.
- The team section renders cleanly on desktop and mobile widths.
- Image paths are valid.
- External links use `target="_blank"` and `rel="noopener noreferrer"`.

## Git / Safety

- Do not revert unrelated user changes.
- Do not run destructive git commands unless explicitly requested.
- Keep diffs focused on the requested change.
