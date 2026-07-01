# Eden — web (landing + legal)

Static site: landing page + Privacy Policy + Terms of Use. Separate from the iOS
app repo on purpose.

## Before publishing

- Replace the "Coming soon" status with the live App Store URL after Apple makes
  the product page available.
- Confirm that `edensupport@gmail.com` is actively monitored.
- Have counsel review the governing-law and privacy language for the operating entity.

## Hosting (Cloudflare Pages — you already have Cloudflare)
1. Push this folder to its own GitHub repo (e.g. `eden-web`).
2. Cloudflare dashboard → Workers & Pages → Create → Pages → connect the repo.
3. Build settings: framework = None, build command = none, output dir = `/` (root).
4. Deploy. You get a URL like `https://eden-web.pages.dev` (or attach a custom domain).

(Alternative: GitHub Pages — repo Settings → Pages → deploy from branch `main` / root.)

## Where the URLs go
- **App Store Connect → App Privacy / Privacy Policy URL:** `https://<your-domain>/privacy.html`
- **Paywall (RevenueCat) Terms & Privacy links:** `terms.html` and `privacy.html` URLs.
- **Carousels link-in-bio:** the landing root `https://<your-domain>/`.

> These legal docs are solid starting templates, not legal advice. Review before publishing.
