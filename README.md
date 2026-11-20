# transitsketch.city

The TransitSketch landing page and beta interest form (TransitSketch/transitsketch#280). Plain static HTML and CSS, no build step, served by GitHub Pages from `main`.

- `index.html`: the page. The sign-up form is a Tally embed: set `data-tally-form` on the `.form` container to the form id (the part after `tally.so/r/`). Until then the page says the form opens soon.
- `styles.css`: colours mirror the app's tokens (`frontend/src/index.css` in the app repo).
- `assets/`: logo, social tile (1200×630, used for link previews), and Roboto (SIL OFL, see `assets/fonts/LICENSE-Roboto.txt`).

To preview locally: `python -m http.server` in this folder.

## Custom domain

Not set yet, so the site is at https://transitsketch.github.io/website/. To move it to `transitsketch.city`:

1. At Namecheap, add `A` records for the apex (`@`) to `185.199.108.153`, `185.199.109.153`, `185.199.110.153` and `185.199.111.153`, and a `CNAME` for `www` to `transitsketch.github.io`. Leave the `alpha` NS delegation to Route53 alone.
2. In this repo's Settings → Pages, set the custom domain to `transitsketch.city` (this commits a `CNAME` file) and tick "Enforce HTTPS" once the certificate is issued.
