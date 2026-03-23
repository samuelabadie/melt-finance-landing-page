# Melt Finance — Website

Jekyll static site with multilingual support (EN / FR / ES).

## Stack
- Jekyll 4.3
- Tailwind CSS v4 (CDN for dev)
- GSAP 3 (ScrollTrigger)
- Geist font (Google Fonts)

## Setup

```bash
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000` — redirects to `/en/` by default.

## Structure

```
_data/          # Translation files (en.yml, fr.yml, es.yml)
_includes/      # nav.html, hero.html
_layouts/       # default.html
assets/images/  # ⏳ Drop logo.svg here
en/ fr/ es/     # Language entry points
```

## Pending (from PRD)

- [ ] Replace `assets/images/logo.svg` with the real logo
- [ ] Add Unicorn Studio embed in `_includes/hero.html` (marked with ⏳)
- [ ] Confirm/replace 3rd language (`es` → your target language)
- [ ] Confirm CTA destination (update `href="#"` in hero.html)
- [ ] Switch Tailwind CDN to a proper build for production
