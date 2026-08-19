# alphamaxxing.xyz

The Alpha Den landing page — Saga DAO's weekly X Spaces show. Static site (GitHub Pages).

## Structure

- `index.html` — the whole site. Content (episodes, host/co-host bios) is hand-edited inline; PFPs are embedded as base64 data URIs.
- `CNAME` — custom domain for GitHub Pages.

## Updating episodes

Pulled from `space-forge`'s `captures` table (`title LIKE '%Alpha Den%'`, most recent 2 by `created_at`). Update the `.ep-list` block in `index.html` by hand for now; a sync script can replace this once the back-catalog is indexed.

## Email list

Signup form posts to a self-hosted Listmonk instance (not yet deployed — see the `TODO(infra)` comment in `index.html` for the placeholder endpoint).

## Deploy

GitHub Pages from `main`. DNS: Cloudflare → apex A records to GitHub Pages IPs (185.199.108/109/110/111.153), `www` CNAME to `oldmanstillcan.github.io`. SSL auto via Pages.

## Local dev

Static — open `index.html` or `python3 -m http.server` in the repo root.
