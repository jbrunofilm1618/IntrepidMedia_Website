# CLAUDE.md

## Project Overview

Intrepid Media is a static marketing website for a creative production consultancy, hosted on GitHub Pages at **intrepidmedia.co**.

## Architecture

- **Single-page static site**: The entire site is one `index.html` file with embedded CSS and JavaScript
- **No build process**: No bundler, compiler, or preprocessor — edit and push
- **No dependencies**: No package.json, no npm modules — only Google Fonts loaded externally
- **Deployment**: GitHub Pages with custom domain (configured via `CNAME` file)

## File Structure

```
index.html        # Complete website (HTML + embedded CSS + embedded JS)
CNAME             # GitHub Pages custom domain config (intrepidmedia.co)
og-image (1).png  # Open Graph social sharing image
```

## Tech Stack

- HTML5 with semantic markup
- Vanilla CSS3 with custom properties (no Sass/Less)
- Vanilla JavaScript (no frameworks)
- Google Fonts: Cormorant Garamond, Lora, Outfit, Playfair Display
- Inline SVG icons (no icon library)
- Schema.org JSON-LD structured data (ProfessionalService, FAQPage)

## Development Workflow

- **No build step**: Edit `index.html` directly
- **No linting/formatting tools**: No ESLint, Prettier, or similar configured
- **No tests**: No testing framework — manual browser testing only
- **Deploy**: Push to `main` branch; GitHub Pages serves automatically

## Key Sections in index.html

1. **CSS custom properties & styles** (top of file)
2. **Hero** with rotating word animation
3. **Services** — 4 cards with SVG icons
4. **Work** — 6 client project cards
5. **Approach** — EDGE framework with collapsible Boyd/OODA Loop detail
6. **Clients** — logo text display
7. **About** — founder bio with stats
8. **Contact** — email link (hello@intrepidmedia.co)
9. **FAQ** — 6 collapsible Q&A items
10. **Footer**
11. **JavaScript** (bottom of file): nav scroll effect, mobile menu, word rotation, IntersectionObserver animations

## Conventions

- All code lives in a single HTML file — CSS in `<style>`, JS in `<script>`
- Mobile-first responsive design with breakpoints at 768px and 480px
- Animations use CSS transitions and IntersectionObserver for scroll reveals
- No environment variables — all content is hardcoded
