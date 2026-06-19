# Project, Natural Expressions (prospect)

Status: **Concept sent to client, awaiting feedback.** Last updated 2026-06-19.

## The business
- **Natural Expressions** (Natural Expressions Cc), a luxury day spa, nearly 30 years old.
- **Location:** 114, 11th Street, Parkmore, Sandton, 2194.
- **Phone:** 011 783 0270 · **Mobile / WhatsApp:** 071 860 6973 (intl 27718606973).
- **Email:** info@naturalexpressions.co.za
- **Social:** Facebook & Instagram (@naturalexpressionssalon, also naturalexpressions.aesthetics).
- **Google:** 4.7 stars, 43 reviews. Also listed on Fresha (booking).
- **Platform:** WordPress, Visual Composer page builder, "spalab" theme, circa 2015 (dated).
- **Product houses stocked:** Guinot, Dermalogica, RegimA. **Laser:** Accent Prime.
- **Goal of the project:** conversions, specifically WhatsApp bookings.

## What we built (concept revamp)
A full, modern, multi-page redesign in their real brand (warm taupe-brown + cream, elegant serif), WhatsApp booking styled in their brown (not green), Google map in the footer of every page, real Google reviews and rating, real before/afters, real brand logos and product shots, and high-quality real spa photography (Unsplash) replacing their dated images.

**Live concept (sent to client):**
https://seth-gorton.github.io/searchly-mockups/natural-expressions/

**Pages:** index (Home), face-care, body-care, laser (with real before/afters), gentlemans-club, products (Guinot/Dermalogica/RegimA), price-list (their real prices), contact (large map + directions), about.

**Repo:** Seth-Gorton/searchly-mockups (public, GitHub Pages), folder `natural-expressions/`.
**Local:** `clients/_leads/mockups/natural-expressions/` (pages + `assets/` with `style.css`, `stock/` photos, `products/`, logos, before/after polaroids).

## Brand tokens used
brown `#8a6f52`, dark `#5f4a34`, deep `#473526`, gold `#c2a06b`, cream `#f7f1e8`, ink `#3a2f25`. Fonts: Cormorant Garamond (display) + Jost (body). All driven from `assets/style.css` `:root` so the palette can be re-skinned in seconds.

## Messages (ready to reuse)
**Access request (when engaged):** ask them to add **sethg@searchly.co.za** as an **Administrator** user in WordPress (Users > Add New > role Administrator).

**Concept share (sent):** "Would you mind taking a look... just a draft of what the site could look like... happy to make any changes you would like."

## Real Google reviews used (4.7 / 43)
Home: P BD, Elana Snoyman, Brittany Paige Joubert. About: Cherer Smith, Moira Sanders, Mandy Annandale. (Pulled from their Google listing; lightly tidied for typos.)

## Open items / placeholders to confirm with client
- **Opening hours** (used a sensible placeholder: Mon-Fri 9:00-18:00, Sat 8:00-15:00).
- **Exact prices** not published on the old site are shown as "On enquiry".
- **Live Google reviews widget** recommended for the real WordPress build (auto-updates instead of hardcoded reviews).

## Next steps if they say yes
1. Get WordPress Administrator access (message above).
2. Collect real photos, exact hours, full price list, any before/afters they own.
3. Build on WordPress (their platform), apply real branding, install live Google reviews widget.
4. Set up tracking (GA4 + Google Ads conversions) and WhatsApp click tracking.
5. QA (performance, accessibility, mobile), then launch with redirects.
