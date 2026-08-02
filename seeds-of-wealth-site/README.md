# Seeds of Wealth — Website (rebuilt as static HTML/CSS/JS)

This replaces the Hostinger Website Builder version of seedsofwealth.ca with a plain,
code-based site: no page builder lock-in, and Claude Code can edit it directly going forward.

## What's in here

- `index.html`, `about.html`, `programs.html`, `join.html`, `contact.html`, `donate.html`,
  `terms.html`, `privacy-policy.html` — one file per page, easy to edit individually
- `assets/css/style.css` — all styling (forest green + gold, DM Serif Display / Inter / DM Mono)
- `assets/js/main.js` — mobile menu toggle + donate amount buttons
- `assets/images/` — put your logo file here (see below)

Content was pulled from your real program docs and Impact One-Pager in Google Drive, not
the old site — a few things on the live site were placeholder text from the page builder
(wrong program names, a fake phone number/address, and a false "CRA tax receipt" claim).
Those are fixed here.

## 3 things to finish before this goes live

1. **Logo file.** I couldn't download your logo from this sandbox (network restriction), so
   every page currently references it — add your real logo file at
   `assets/images/logo.png` (same filename, so nothing else needs to change).

2. **Donation link** (`donate.html`). The "Donate Now" button currently points to `href="#"`.
   Get a donate link from PayPal (paypal.com/ca/webapps/mpp/donate-with-paypal) or a Stripe
   Payment Link (dashboard.stripe.com/payment-links), then paste it into that `href`.

3. **Form endpoint** (`join.html` and `contact.html`). Both forms currently submit to
   `https://formspree.io/f/YOUR_FORM_ID`, a placeholder. Create a free form at
   formspree.io, then replace `YOUR_FORM_ID` in both files' `<form action="...">` line.
   (Alternative: swap in a Google Form embed instead of Formspree if you'd rather have
   submissions land straight into a Sheet.)

Each of these has a yellow banner on the page itself as a reminder — delete the
`<div class="setup-banner">...</div>` block once you've wired the real link/ID in.

## How to publish this

1. **Create a GitHub repo** (github.com → New repository), then upload this whole folder
   (drag-and-drop works fine, or `git init && git add . && git commit -m "init" && git push`
   if you're comfortable with git).
2. **Connect it to Hostinger:** in hPanel, go to Websites → your site → Git, and point it at
   this repo. Hostinger will pull the files and serve them as your static site. (This
   replaces the Website Builder — you may need to switch your site type in hPanel to
   "regular hosting" first if it's currently locked to Website Builder.)
3. **Future edits:** once this is a real repo, you can `cd` into it and run `claude` (Claude
   Code) any time you want changes — "update the donate page," "add a testimonials
   section," etc. — and it'll edit the files directly instead of you touching code by hand.

## Notes

- Photos are hotlinked from Unsplash (same images the old site used) — fine to keep, or
  swap for your own photos from BGC Durham sessions once you have them.
- Stats shown (12 youth / 6 sessions / 6 programs) reflect the BGC Durham pilot per your
  June 2026 Impact One-Pager. Update these once you have new pilot data.
