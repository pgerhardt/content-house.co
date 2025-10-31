# Creative Content House – Handoff Bundle (v2)

Finalized static landing with editorial palette and updated copy and appointment booking flow.

## Files
- `index.html` — final markup with the tagline “Strategy and design for modern brands, from concept to execution.”
- `styles.css` — typography and palette
- `assets/favicon.svg` — CCH monogram
- `assets/og-cover.png` — social preview
- `README.md` — implementation notes

## Hooking up the Purchase Button (no Calendly)
Use **Stripe Checkout** to sell a single “Consulting Session” product. To cap availability at **10 total sessions** without showing any limit text on the site:

**Stripe**
1. Create a Product: “Consulting Session” (fixed quantity = 1 per checkout).
2. In the Product's Inventory settings, set **Inventory = finite** and **Quantity = 10**.
3. Create a **Payment Link** or Checkout Session URL for that product.
4. Paste the link into `index.html` where the CTA `href="#"` is.
5. When inventory reaches 0, the link will show “Sold out” automatically.

**Google Calender**
- Use Google Workspace Basic and enable calender booking

## Deploy
- **GitHub Pages**: push and enable Pages.

## Notes
- Fonts: Playfair Display (headline) + Inter (body).
- Palette: Warm white (#FAF8F3), Charcoal (#1B1A18), Muted gold (#B59B72).