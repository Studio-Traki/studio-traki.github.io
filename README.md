# Traki studio website

Static site for **studio-traki.github.io**: studio home, privacy policy, terms, support, licenses, and `app-ads.txt`.
No build step. This folder is the source of truth; it's published by pushing its contents to the
root of the `Studio-Traki/studio-traki.github.io` repo (GitHub Pages, branch `main`, folder `/`).

- Palette (Midnight arcade): `#07070D` bg · `#7C5CFF` violet · `#FFD447` sun · `#E8E8FF` text
- Logo: `assets/logo.svg` (lockup), `assets/logo-mark.svg` (mark), `assets/favicon.svg` (app-icon tile),
  PNG exports `logo-1600.png`, `logo-icon-1024.png`, `apple-touch-icon.png`, `og-image.png`
- Contact email used across pages: `notvaja@gmail.com` (temporary)

## When adding a game
1. Add a card to `index.html`, a FAQ block to `support.html` (`id="<slug>"`), and a row to the
   game table in `privacy.html`, and a section to `licenses.html` (open-source components and their
   copyright lines). Re-check the privacy policy if the game adds any new SDK.
2. Bump the "Effective" date on any legal page you change.

## Before publishing
Replace every `[BRACKETED]` placeholder in `privacy.html` and `terms.html` (owner legal name, city/country,
governing-law country). Search: `grep -n '\[' privacy.html terms.html`.

## app-ads.txt
Replace the commented line with the real AdMob publisher line once the AdMob account exists. For iOS,
AdMob finds this file via the App Store listing's **Marketing URL**, so that field must point at this domain.
