# AiSpy — website

A single-page site. One file, no build step, no framework.

## Files

- `index.html` — the whole site: text, layout and styling in one file
- `logo.svg` — the AiSpy wordmark, for use outside the site
- `README.md` — this file

Fonts (Inter and JetBrains Mono) load from Google Fonts. Nothing else is external.

## Deploying on Vercel

1. Push this folder to a new GitHub repo.
2. In Vercel, **Add New → Project**, and pick the repo.
3. Framework preset: **Other**. Leave the build and output settings empty.
4. Deploy. Vercel serves `index.html` as the homepage automatically.
5. Add the real domain under **Settings → Domains** once it's registered.

## The logo

The logo is the supplied SVG, inlined directly into `index.html` so it scales cleanly and follows the colour scheme. `logo.svg` in this folder is the original as supplied, kept for use elsewhere (email signatures, documents, print).

Inside the page, two fills were made dynamic: the "Spy" lettering uses `currentColor` so it flips to light text in dark mode, and the "Ai" uses `var(--logo-violet)` so it brightens slightly against a dark background.

## The contact form

The form does not send anywhere yet. Its `action` is set to `https://formspree.io/f/YOUR_FORM_ID` — until that ID is replaced, submitting just shows the thank-you message and nothing reaches Brendan.

To make it work: create a free Formspree account, add a form, copy the endpoint it gives you, and paste it over that URL. Ask if you want walking through it.

## Things still to fill in

- `brendan@example.ie` — appears twice in the contact section and once in the footer area. Replace with the real address on the real domain.
- `PHOTO OF BRENDAN` — the grey square in the About section. Replace that `<div class="photo">` with `<img src="brendan.jpg" alt="Brendan Walsh">` and put the image in this folder.
- The two sample cards (the accountancy query test, and the four-market table) are **illustrative examples**, not real findings. Swap them for real anonymised results as soon as there are any.
- The KC Lincoln quote needs his sign-off before it goes live.
- The Formspree form ID (see above).


## Changing the highlight colour

Near the top of `index.html`:

```css
--hi:#5E17EB;
--hi-soft:rgba(94,23,235,.10);
--logo-violet:#5E17EB;
```

`--hi` is the highlight used on the nav numbers, section labels, statuses, the quote rule and button hovers. `--hi-soft` is the same colour at 10% opacity, used to tint one table row. Change both together.

Brand violet is `#5E17EB`, taken from the logo. The dark colour scheme uses a lighter violet (`#9A6BFF`) so it stays readable on a dark background — if you change one, change both.

## Fonts

- **Inter** — all reading text: headlines, body, buttons, prices.
- **JetBrains Mono** — anything that reads as data: the numbered nav, section labels, card headers, market codes, NAMED / NOT NAMED statuses, price tier labels.

Rule of thumb when adding pages: if it's a finding, a label or a code, it's mono. If it's a sentence meant to persuade, it's Inter.

## Notes

- The contact links are `mailto:` and `tel:` — there is no form and no server. If a real form is wanted later, it needs somewhere to send submissions.
- Light and dark colour schemes are both handled; the page follows the visitor's system setting.
