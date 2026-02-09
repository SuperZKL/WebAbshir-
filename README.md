# Photography Portfolio — Run & Deploy

Quick instructions to run this static portfolio locally and deploy it.

## Run locally

- Open index.html directly in your browser (works for simple testing).
- Or run a local static server:

  - Python 3:

    ```bash
    python3 -m http.server 8000
    # then open http://localhost:8000 in your browser
    ```

  - Node (no install required each time):

    ```bash
    npm start
    # this uses npx serve to serve the current folder
    ```

## Deploy options (fast)

- GitHub Pages: push this repository to GitHub and enable Pages from the `gh-pages` branch or `main`/`docs` folder. See GitHub docs for one-click setup.
- Vercel: sign up at vercel.com and import the repo — zero-config for static sites.
- Netlify: drag & drop the built folder or connect the repo for continuous deploys.

## Quick checklist — "Great list" to make the site production-ready

- Replace placeholder images (picsum) with optimized real images (WebP/AVIF) and add `loading="lazy"`.
- Add `manifest.json` and favicon for PWA/branding.
- Add a hosted contact form or form backend (Formspree, Netlify Forms, or a small serverless function).
- Improve SEO: add Open Graph tags, Twitter card metadata, and structured data (JSON-LD).
- Accessibility audit: semantic elements, ARIA where needed, keyboard focus states, color contrast.
- Analytics & privacy: add consent and analytics (Plausible, Fathom, GA4) if desired.
- Performance: minify CSS, compress images, and enable caching/headers via host.

## Next steps I can do for you

- Add `manifest.json` + favicon and link them into `index.html`.
- Replace image placeholders with lazy-loaded examples and real URLs.
- Add deployment workflow (GitHub Actions) for automatic GitHub Pages deploy.
- Wire a simple serverless contact endpoint or connect a third-party form.

Tell me which of the next steps you want me to do and I’ll continue.
