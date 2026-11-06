# Melius Events

Static site for meliusevents.com. No build step: the site lives in `public/`
(`index.html` is the page, photos are in `public/assets/`).

## Cloudflare

Served by the Cloudflare Worker `old-meadow-4cbf` (see `wrangler.jsonc`).
Connect it under the Worker's Settings → Build:

- Git repository: this repo, branch `main`
- Build command: (leave empty)
- Deploy command: `npx wrangler deploy` (the default)
- Root directory: `/`

Every push to `main` then publishes the site. If the Worker is renamed,
change `"name"` in `wrangler.jsonc` to match or the deploy will fail.
