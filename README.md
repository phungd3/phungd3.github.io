# derekphung.com starter

A lightweight static academic website for Derek Phung.

## Files

- `index.html` — homepage
- `style.css` — all styling
- `CNAME` — tells GitHub Pages to use `derekphung.com`
- `.nojekyll` — tells GitHub Pages to serve the static files directly
- `assets/` — put your CV, research figures, and optional profile photo here

## Before publishing

Search `index.html` for `href="#"` and replace those placeholders with:
1. your GitHub profile
2. your LinkedIn profile
3. the correct repository links for HighFidelityEphemerisModel.jl and AstrodynamicsCore.jl

Add your CV as:

`assets/Derek_Phung_CV.pdf`

For the research figure, replace the `.figure-placeholder` block in `index.html`
with an `<img>` once you choose the image. We can do that together.

## GitHub Pages

The easiest setup is a public repository named:

`YOUR_GITHUB_USERNAME.github.io`

Upload these files to the root of that repository, then go to:

**Repository → Settings → Pages**

Choose **Deploy from a branch**, select `main` and `/ (root)`, and save.

Then under **Custom domain**, enter:

`derekphung.com`

GitHub will use the included `CNAME` file for the custom domain.

## Porkbun DNS

Do this only after the GitHub Pages site/custom domain has been configured.

For the apex `derekphung.com`, create four `A` records with host `@`:

- `185.199.108.153`
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

For `www`, create a `CNAME` record pointing to:

`YOUR_GITHUB_USERNAME.github.io`

Keep your Porkbun email-forwarding records intact.

Once DNS has propagated, enable **Enforce HTTPS** in GitHub Pages settings.

## Design direction

The site is intentionally:
- academic rather than "portfolio-ish"
- text-forward, inspired by simple researcher homepages
- responsive
- framework-free
- easy to maintain during grad school and beyond
