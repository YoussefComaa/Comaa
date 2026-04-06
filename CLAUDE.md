# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

"Davies" is a static personal portfolio HTML template. It consists of plain HTML pages, SCSS compiled to CSS, and vanilla JS with third-party libraries. There is no build system beyond the Sass compiler.

## Commands

**Compile SCSS to CSS (with watch):**
```
sass assets/scss/app.scss assets/css/styles.css --watch
```

**One-time compile:**
```
sass assets/scss/app.scss assets/css/styles.css
```

## Architecture

### Pages
- `index.html` — main portfolio page
- `version-2.html` / `landing.html` — alternate homepage versions
- `blog-*.html` — blog listing pages (single, standard, two-columns, three-columns)
- `404.html` — error page

### Styles (`assets/scss/`)
- `app.scss` — entry point that `@use`s all partials
- `abstracts/` — variables and mixins (imported as `abstract` namespace)
- `core/` — reset, typography, utility classes
- `component/` — per-component partials (header, footer, blog, elements like buttons, sliders, tabs, etc.)
- Compiled output: `assets/css/styles.css` (do not edit directly)

### JavaScript (`assets/js/`)
- `main.js` — primary custom JS (initialization, UI behavior)
- `gsapAnimation.js` — GSAP scroll animations using ScrollTrigger/ScrollSmoother/SplitText
- `carousel.js` — carousel/slider initialization (Slick, Swiper)
- Third-party libs bundled as minified files: jQuery, Bootstrap, GSAP, Swiper, Slick, Odometer, Nice Select, UnicornStudio

### Assets
- `assets/images/` — all image assets organized by category (blog, brand, item, etc.)
- `assets/fonts/` — custom font declarations
- `assets/icon/icomoon/` — icon font (icomoon) with selection.json for regenerating the font set
