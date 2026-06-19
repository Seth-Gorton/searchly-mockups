# Self Storage CW Midrand, Audit Notes

URL audited: https://www.selfstoragecwmidrand.co.za/
Date: 2026-06-19
Auditor: Searchly Web (pre-pitch teardown)

## Business summary

Self Storage CW Midrand is the Midrand-area landing site for **Self Storage CW**, the
self-storage arm of the **Container World** group. They rent new shipping-container storage
units (6.05m x 2.44m x 2.59m) on a secured, floodlit, CCTV-monitored site for both private
and business customers, on short or long-term terms. The single desired action is a quote /
enquiry via the on-page form or a phone call.

One line: A container-based self-storage facility serving Midrand / Johannesburg, selling
secure, affordable monthly storage units to households and businesses, where the goal is to
capture a quote enquiry.

## Offering

- New steel anti-vandal storage containers (6.05m x 2.44m x 2.59m, roughly 36 sq m footprint).
- Two pricing tiers advertised:
  - **Top level units from R700 excl VAT** (per month).
  - **Ground floor units from R950 excl VAT** (per month).
- Long-term OR short-term rentals; private OR business use.
- Security stack: electric fence, CCTV cameras, fire protection system, floodlit paved areas.
- Access weekdays 08h00 to 17h00, after-hours by arrangement.

## Scale

**SMALL.** Single-location, single-page WordPress/Elementor landing page (one published page,
ID 54). No product catalogue, no booking engine, no e-commerce, no blog, no multi-page nav.
The whole site is a vertical scroll: hero, pricing band, benefits, security, "why choose",
contact + one enquiry form. The parent brand (selfstoragecw.co.za) is itself a thin single-
page multi-location site (Durban, Polokwane, Midrand, Nelspruit). This is a lead-capture
microsite, not a platform. A redesign is a 1 to 2 page craft + conversion job, not a build.

## Platform

- **WordPress + Elementor** (3,300+ Elementor references in DOM; wp-content/wp-includes/wp-json present).
- Forms: Gravity Forms-style enquiry form with reCAPTCHA ("CAPTCHA", honeypot "Comments" field).
- Hosting/theme not deeply probed; uploads dated 2021/10 (site largely untouched since ~2021).
- Designed by "Vetro Media" (footer credit). Copyright auto-rolls to 2026.

## Brand hex palette (pulled from live CSS / inline styles)

| Role | Hex | Notes |
|------|-----|-------|
| Primary blue | `#008AD1` | Logo + CTA accent, most-used brand colour |
| Deep blue | `#005CA8` | Darker logo blue / gradient |
| Brand red | `#E31513` | "SELF STORE IT!" / urgency accent |
| Dark red | `#C02B0A` | Secondary red / hover |
| Body grey | `#606060` | Body text |
| Dark grey | `#3F3F3F` | Headings |
| White | `#FFFFFF` | Reversed text on photo/blue bands |

Logo is the "SELF STORAGE / CONTAINER WORLD" wordmark with a blue stacked-cube mark.

## Asset filenames (downloaded to ./assets/, all verified valid images)

- `logo.png` (401x401, the Self Storage CW stacked-cube logo)
- `cw-logo.png` (646x100, Container World horizontal logo)
- `hero-fan.jpeg` (2000x1332, current hero: man behind a fan in a cluttered room)
- `container-exterior-1.jpg` (2000x1500, real facility container photo)
- `container-exterior-2.jpg` (2000x1500, real facility container photo)
- `facility-pic.jpg` (1280x680, facility/site shot)
- `family-living.jpg` (2000x1708, lifestyle, family in tidy living room)
- `storage-boxes.jpg` (1200x801, stacked moving boxes stock)

The two `container-exterior-*.jpg` and `facility-pic.jpg` are the genuinely valuable real
assets (actual units / site). The hero stock photo is weak and off-message.

## Real reviews

**None found.** No Google rating, review count, or testimonials are publicly discoverable for
this facility (searches across Google, Facebook page "SelfStorageMidrand", Converted Containers
listing, and the parent brand site all returned no star rating or quotes). The site itself
carries zero testimonials or trust ratings. This is a conversion gap, not just a research gap:
competitors (e.g. Stor-Age Midrand) actively surface named, glowing customer reviews.

## Unit types

- Container units, 6.05m x 2.44m x 2.59m (one standard size, positioned by floor level).
- Top-level units from R700 excl VAT/month.
- Ground-floor units from R950 excl VAT/month (premium for drive-up convenience).

## Contact and location

- Tel: +27 11 392 1284 (note: on-site the tel link is broken, see audit issue #4).
- Email: JHB@selfstoragecw.co.za
- Address listed: Corner Hooker St & Chloor Rd, Chloorkop, Edenvale, 1622 (this is the JHB
  depot address; site copy says containers are "located in Midrand, Durban and Polokwane",
  which conflicts with the single Edenvale address shown, a clarity problem for a "Midrand" page).
- Hours: Weekdays 08h00 to 17h00, after-hours on arrangement.

## CONVERSION AUDIT (primary action: GET A QUOTE / reserve a unit)

1. **Weak, off-message hero image and headline.**
   The hero is a stock photo of a man behind a desk fan in a messy room with a vague pun
   ("NEED SOME BREATHING ROOM? DON'T JUST MOVE IT... SELF STORE IT!"). It does not show the
   product (clean secure containers), name the location, or state the offer.
   *Fix:* Lead with a real container/facility photo (we have `container-exterior-1/2.jpg`),
   a location-specific headline ("Secure self-storage units in Midrand, from R700/month"),
   and the quote CTA above the fold.

2. **No trust signals or reviews anywhere.**
   Zero testimonials, no star rating, no "X years / X customers", no Google reviews embed.
   Storage is a trust purchase (people leave their possessions for months).
   *Fix:* Add a reviews/testimonials strip, surface Google rating, add trust badges
   (CCTV/fire/electric-fence icons already exist as copy, turn into a visual security band),
   and a years-in-business / Container World group credibility line.

3. **Broken phone link.**
   The tel link renders as `href="https://+27113921284"` (data-wplink-url-error="true"),
   so tapping the number on mobile does nothing. A primary conversion path is dead.
   *Fix:* Correct to `tel:+27113921284`; make the number a sticky tap-to-call on mobile.

4. **Form is buried at the very bottom and is unfriendly.**
   The only enquiry form sits below all content; the visible field labels include a stray
   "Comments / This field is for validation purposes" line (honeypot leaking into UI), and
   there is no reassurance about response time or what happens next.
   *Fix:* Move a short quote form (Name, Phone, Unit need, Move-in date) into/near the hero,
   clean up the leaking honeypot label, and add a "We'll reply within 1 business hour"
   micro-reassurance plus a clear submit label ("Get my quote").

5. **No WhatsApp, despite SA's strongest conversion channel for local enquiries.**
   DOM references "WhatsApp" but there is no working click-to-chat path. For a Midrand
   storage buyer, WhatsApp is often the lowest-friction enquiry.
   *Fix:* Add a working WhatsApp click-to-chat button (floating + in contact section) with a
   prefilled "Hi, I'd like a quote for a storage unit in Midrand" message.

6. **Pricing is shown but the offer is incomplete and creates objections.**
   "From R700 excl VAT" with no minimum term, no deposit info, no "what's included", and no
   size comparison ("fits a 1-bed flat / 20 boxes / a small business stock"). Excl-VAT pricing
   without the inc-VAT number reads as a hidden cost.
   *Fix:* Add an inc-VAT figure, a "what fits" visual size guide, minimum-term and deposit
   clarity, and a comparison of top-level vs ground-floor so the buyer self-selects.

7. **Location ambiguity undermines a location landing page.**
   The page is "Midrand" but the only address shown is Chloorkop/Edenvale, and the copy says
   units are in "Midrand, Durban and Polokwane". A Midrand searcher cannot confirm where they'd
   actually store, and there is no map.
   *Fix:* State the exact Midrand site address, embed a Google Map with directions, and remove
   the multi-city copy that doesn't belong on a single-location page.

8. **No real CTA hierarchy, "ENQUIRE NOW" floats without urgency or path.**
   The single CTA scrolls to the bottom form. There is no secondary path (call / WhatsApp), no
   incentive (e.g. "first month deal" or "reserve, no obligation"), and the button repeats
   without a sticky persistent CTA as the user scrolls a long page.
   *Fix:* Sticky header CTA + dual path (Get a quote / WhatsApp / Call), add a low-commitment
   framing ("Reserve a unit, free to cancel"), and an availability nudge if real.

9. **Stale, low-craft, slow-feeling build (assets from 2021, generic Elementor).**
   Dated stock imagery, mixed message, no motion or considered typography, likely heavy
   Elementor DOM (3,300+ refs) hurting Core Web Vitals on mobile, which is where storage
   searches happen. The site reads as a 2021 template, not a credible secure facility.
   *Fix:* Rebuild as a fast, single-purpose, conversion-led page (lean markup, real photos,
   one creative concept, clear sections), with GA4 + Google Ads conversion tracking on the
   quote form / call / WhatsApp so the (likely Ads-driven) traffic is measurable.

## Relationship to selfstoragecw.co.za

This site is effectively a **single-location (Midrand/JHB) split-out of the same brand and
template** as the parent `selfstoragecw.co.za`. Same logo, same blue/red palette, same copy
blocks (the 6.05x2.44x2.59 container spec, the "Don't just move it, self store it" line, the
security feature list, the 08h00 to 17h00 hours, the same JHB email). The parent site is the
multi-location version (Durban, Polokwane, Midrand, Nelspruit) on the same thin single-page
WordPress/Elementor pattern with the same conversion weaknesses (no reviews, buried form, no
map). A redesign should treat this as the Midrand conversion landing page and the parent as the
group hub, with consistent branding but location-specific proof, address, and map here.
