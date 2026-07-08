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
