# Chris — Product designer

A responsive Astro static portfolio with locally bundled Inter, reduced-motion support, and no client-side JavaScript required.

## Local development

Use Node.js 22.19 or later. From this directory:

```sh
npm ci
npm run dev
```

Open the local address printed by Astro. Run `npm run build` to generate `dist/`, then `npm run preview` to inspect the production build.

## GitHub Pages

1. Put the contents of this directory at the root of a GitHub repository, including `.github/` and the lockfile.
2. Push to the `main` branch.
3. In the repository's **Settings → Pages**, select **GitHub Actions** as the source.
4. Run the included deployment workflow, or push another change to `main`. Its deployment result supplies the published URL.

The workflow gets the origin and repository base path from GitHub Pages, supporting both account sites and repository subpaths. For a custom domain, configure it in GitHub Pages before rebuilding. No personal URLs are assumed.

For manual builds set `SITE_URL` to the full site origin and `BASE_PATH` to the repository path (for example `/portfolio`), or `/` for an account site or custom domain.

## Editing

Content and page styles live in `src/pages/index.astro`. The self-contained `src/components/Hero.astro` owns the hero and decorative animation. Replace its `hero-art` element with a Rive canvas when an asset is available; retain the HTML name and subtitle, keep decorative art hidden from assistive technology, and respect reduced motion. The current CSS illustration requires no Rive dependency.

QAKoala remains unlinked until a real destination is supplied. Company names are plain text. The site contains no invented contact links.
