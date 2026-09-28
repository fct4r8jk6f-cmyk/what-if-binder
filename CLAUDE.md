# The What-If Binder / Le Classeur Au Cas Où

This repo IS the deployed app: GitHub Pages serves the two editions at
https://fct4r8jk6f-cmyk.github.io/what-if-binder/ (EN) and
https://fct4r8jk6f-cmyk.github.io/what-if-binder/le-classeur-au-cas-ou.html (fr-CA).

## What this is
A bilingual (EN + fr-CA) family-emergency binder app: if something happened to
you tonight, could your family find what they'd need? One self-contained HTML
file per edition, local-first (answers stay in the browser via localStorage — no
account, no server), with backup/restore and print-to-PDF built in, and 15
guided sections per edition (key people, medical, money, insurance, digital
life, legal documents, final wishes, and more).

## Hard rules
- **Public repo, faceless.** This repo is public, so no owner name, face, or
  personal paths in any file here. The product carries no personal brand.
- **One self-contained file per edition.** No frameworks, no build step, no
  external requests — each edition must work offline from a single HTML file.
- **Bilingual EN / fr-CA.** French is Québec French (fr-CA), never
  France-French (liquidateur, mandat de protection, notaire — not the France
  equivalents). Keep the two editions at feature parity.
- **Local-first privacy is the promise.** Answers never leave the device; do not
  add analytics, cloud sync, or any network call.

## How the files here are made
- `index.html` and `le-classeur-au-cas-ou.html` are **byte-identical copies** of
  `app/the-what-if-binder.html` / `app/le-classeur-au-cas-ou.html` in the private
  `whatif` repo. Edit there, run its `tools/verify.js`, then copy here — never
  edit these two files directly, or the next sync overwrites the change.
- `og-en.jpg` / `og-fr.jpg` are the link-preview cards (rendered by `whatif`'s
  `tools/build.js`). The `og:`/`description` meta tags are inert when the page
  runs — they don't make requests.
- **`SHOP_URL`** (top of each file's script) is the Etsy listing for the paid
  print-ready kit. Empty = the "Get the print-ready kit" link stays hidden; it
  only ever shows on this hosted copy (never in a downloaded `file:` copy).
  Set it in `whatif/app/*.html`, verify, and sync here once the listings exist.
- Buyers on iPhone/iPad are sent here (the downloaded file only previews on
  iOS). Safari wipes a site's saved data after ~7 days without a visit, so the
  app shows an iOS-only backup note and nags for a backup after 5 edits there.
  Don't remove that.
- If this site's URL ever changes (account rename, custom domain), update the
  hard-coded URLs in both apps' read-only fallback and meta tags, and in both
  quick-start guides in `whatif` — buyers' PDFs point here.

## Related projects
Sibling repos under the same account (ask to add via add_repo when a task needs
them):
- **`fct4r8jk6f-cmyk/whatif`** (private): the product workshop this app is
  generated from — sources, printable PDF deliverables, listing copy, launch
  docs. Business/sales ops happen there, in local sessions.
- **`fct4r8jk6f-cmyk/pixelboreal`** (public): the pixelboreal web-studio
  portfolio site (https://fct4r8jk6f-cmyk.github.io/pixelboreal/), which
  features this binder as a work sample — keep its claims about this app in
  sync with what actually ships here.
- **`fct4r8jk6f-cmyk/perchapp`** (public): Perch, a social-app demo, the other
  pixelboreal work sample.
