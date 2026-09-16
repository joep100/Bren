# AI Search Ireland — website

A single-page site. One file, no build step, no framework.

## Files

- `index.html` — the whole site: text, layout and styling in one file
- `README.md` — this file

Fonts (Inter and JetBrains Mono) load from Google Fonts. Nothing else is external.

## Deploying on Vercel

1. Push this folder to a new GitHub repo.
2. In Vercel, **Add New → Project**, and pick the repo.
3. Framework preset: **Other**. Leave the build and output settings empty.
4. Deploy. Vercel serves `index.html` as the homepage automatically.
5. Add the real domain under **Settings → Domains** once it's registered.

## Things still to fill in

- `brendan@example.ie` — appears twice in the contact section and once in the footer area. Replace with the real address on the real domain.
- `PHOTO OF BRENDAN` — the grey square in the About section. Replace that `<div class="photo">` with `<img src="brendan.jpg" alt="Brendan Walsh">` and put the image in this folder.
- The two sample cards (the accountancy query test, and the four-market table) are **illustrative examples**, not real findings. Swap them for real anonymised results as soon as there are any.
- The KC Lincoln quote needs his sign-off before it goes live.

## Changing the highlight colour

Near the top of `index.html`:

```css
--hi:#0F8A78;
--hi-soft:rgba(15,138,120,.10);
```

`--hi` is the highlight used on the nav numbers, section labels, statuses, the quote rule and button hovers. `--hi-soft` is the same colour at 10% opacity, used to tint one table row. Change both together.

Alternatives already tried: blue `#2F6BFF`, violet `#6A4BF2`.

## Fonts

- **Inter** — all reading text: headlines, body, buttons, prices.
- **JetBrains Mono** — anything that reads as data: the numbered nav, section labels, card headers, market codes, NAMED / NOT NAMED statuses, price tier labels.

Rule of thumb when adding pages: if it's a finding, a label or a code, it's mono. If it's a sentence meant to persuade, it's Inter.

## Notes

- The contact links are `mailto:` and `tel:` — there is no form and no server. If a real form is wanted later, it needs somewhere to send submissions.
- Light and dark colour schemes are both handled; the page follows the visitor's system setting.
