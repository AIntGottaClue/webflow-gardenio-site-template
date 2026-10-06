# Gardenio - Site Template (Astro)

Original-code site template inspired by the light, garden-fresh look of the
Gardenio Webflow template (soft green-white canvas, deep forest green,
lime accent, Instrument Serif display + Instrument Sans text). No Webflow
markup, scripts, assets, or tracking are used. One codebase, one config,
many cities via the city-data switcher.

## Quick start

1. `npm install` then `npm run dev` to preview locally.
2. Set the launch city: copy `src/data/cities/_placeholder.json` to
   `src/data/cities/your-city.json` and point `ACTIVE_CITY` in
   `src/data/cities.ts` at the slug.
3. `npm run build` outputs a static site to `dist/`.

## City data switcher

- `src/data/cities.ts` sets `ACTIVE_CITY = '_placeholder'` for the demo.
- Each file in `src/data/cities/` holds brand, phone, email, service names,
  location names, guide titles, and copy. Tokens like {Biz Name} and
  {City, ST} render from this file.
- The GitHub Pages workflow builds with BASE=/webflow-gardenio-site-template.

## Structure

- `src/layouts/Base.astro` - shell: header with hover dropdowns, footer,
  sticky mobile call bar.
- `src/components/RequestForm.astro` - the single request form, rendered in
  the hero of every page.
- `src/components/Hero.astro`, `ServiceCard.astro`, `SectionHead.astro`,
  `GuideCard.astro` - shared sections.
- `src/pages/` - 15 routes: home, services hub + 3 service pages,
  guides hub + 2 guides, neighborhoods hub + 3 location pages,
  contact, privacy, terms.
- `src/styles/global.css` - full design system (palette, buttons, chips,
  cards, forms, hero variants, footer, motion tokens).
- `public/assets/js/fx.js` - lightweight vanilla JS effects: pointer-driven
  parallax on hero art and scroll-reveal. No scroll-jacking, no libraries.
