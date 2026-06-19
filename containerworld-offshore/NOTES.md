# Container World Offshore, Audit Notes

Source: https://www.containerworldoffshore.com/ (audited 2026-06-19)

## Business summary
Container World Offshore is the offshore/marine arm of Container World (Pty) Ltd, a Cape Town container business operating since 1983. The offshore site sells and supplies certified offshore shipping containers and oilfield/marine cargo-carrying units, all certified to DNV 2.7-1 and EN 12079, serving oil, gas and marine operators across Africa (East and West) and beyond.

### How it differs from containerworld.co.za (the parent)
- **containerworld.co.za** = the established **on-shore** division: storage containers, leasing, and container conversions (accommodation, dining, kitchen, ablution, office units) for the general African market. This is the older, core business with ~12 branches across SA.
- **containerworldoffshore.com** = a newer, specialised **off-shore** spin-off site (assets uploaded 2025), targeting the oil/gas/marine sector with DNV/EN-certified offshore-rated equipment (reefers, cargo baskets, gas racks, skips, portable tanks, rigging lofts, deck offices). Both share the same Cape Town HQ (44 Firgrove Way, Macassar), the same phone (021 511 2598), and the same parent company. The offshore site even links back to containerworld.co.za in its main nav ("Container World").
- The offshore site is multilingual on the homepage (English, French, Portuguese) to address Francophone and Lusophone West/Central African oil markets (Angola, Gabon, Congo, Equatorial Guinea, Mozambique, etc.).

## What they sell (products)
Storage Containers, Reefers (DNV refrigerated), Half Heights, Mini offshore containers, Cargo baskets (certified slings and shackles), Gas racks (2/6/12 bottle), Open Tops, Skips (boat-shape, non-hazardous waste), Tool boxes, Portable Tanks (hazardous liquids, fuels, chemicals, liquid nitrogen), Deck offices, Rigging lofts (build-to-spec, no rental). All certified DNV 2.7-1 / EN 12079; recognised by DNV and Lloyd's Register.

## SCALE: MEDIUM (leaning medium-large as a business, small-medium as a website)
- **Business scale: medium-to-large.** A 40+ year company, 12 branches, division of an established group, serving an international B2B oil/gas/marine market across 28+ listed countries. Real industrial depth and an extensive product catalogue.
- **Website scale: small-to-medium.** Despite the business's reach, the actual site is thin: a handful of pages (Home, Products listing, Locations, Blog with 2 posts, Contact, Privacy). Products are described in one-line teasers with "Read More" but there is no deep per-product spec/detail content, no pricing, no datasheets, no gallery depth. The Locations page lists 28+ countries but each is a stub ("(1)", same phone, "Loading..." map). So: a substantial business represented by a shallow brochure site, which is exactly the redesign opportunity.

## Platform / stack
- **WordPress** with the **LogisCargo** theme (+ logiscargo-child child theme).
- Page building via **WPBakery (js_composer 8.7.2)** and **Slider Revolution (RevSlider 6.7.55)** for the hero.
- Forms: **Contact Form 7** + CF7 redirect-to-thank-you + invisible reCAPTCHA v3.
- Tracking present: **GA4 (G-TBDVZPPHJL)** and **GTM (GTM-52MW6B84)** already installed.
- Fonts: Roboto, Poppins, Open Sans, Alegreya (multiple font families loaded, bloat).
- Built by Vetro Media (vetro.co.za).

## Brand hex palette (pulled from CSS + logo)
- Primary blue: **#158acb** (also rendered as #258bcb / #188bcb across the theme, inconsistent)
- Accent / alert red: **#e21f26** (logo wave/accent and CTAs)
- Dark text: **#323232 / #313131 / #231f20**
- Near-black: **#000000**
- White: **#ffffff**
- Light grey panels: **#e7e7e7**
Note: the blue is used in at least three near-identical but non-matching hex values, a sign of no design-token discipline. Standardise on one blue.

## Assets downloaded (in ./assets/)
- `logo.png` (140x116, small, low-res, transparent PNG, will need a higher-res or vector version)
- `slider-1.jpg` (hero: offshore reefer over Table Mountain / Cape Town sea, strong real brand image)
- `slider-3.jpg`, `slider-4.jpg`, `slider-5.jpg` (additional real hero/product sliders)
- `rigging-lofts.png` (real interior shot of a rigging loft conversion)
- `portable-tanks.png` (real product image)
All verified: correct MIME types, all images over 15KB (logo is a small UI asset).

## Real reviews / social proof
- **No public star rating found.** Facebook page (facebook.com/containerworldoffshore) shows "Not yet rated, 1 Review". No Google Business rating surfaced for the offshore entity.
- Third-party industry presence exists (Offshore-Technology.com and Oil Review Africa both list/feature Container World Offshore as a DNV offshore container supplier), which is credible trade validation but not customer reviews.
- The live site itself displays **zero testimonials, zero reviews, zero client logos, zero case studies**. For a high-value B2B industrial buyer this is a major trust gap.

## Contact
- Address: 44 Firgrove Way, Macassar, Cape Town, 7134
- Tel: 021 511 2598
- Email: info@containerworldoffshore.co.za (note: .co.za on a .com site)
- Sales contacts named on Contact page: Esha Munsamy (esha@containerworld.co.za), Darren Singh (darrens@containerworld.co.za), again on @containerworld.co.za, not the offshore domain
- Hours: Mon-Fri 08:00-17:00, weekends closed

---

## CONVERSION AUDIT, primary desired action = GET A QUOTE
The site currently has no real "Get a Quote" path. The CTA is a generic "CONTACT US" leading to a basic contact form. For a B2B industrial buyer comparing certified offshore equipment suppliers, the following are hurting quote/lead conversion:

1. **No dedicated "Request a Quote" path or CTA.** The only action is a generic "Contact Us". For an industrial buyer the desired action is a quote on specific units/quantities. **Fix:** Add a prominent, persistent "Get a Quote" primary CTA in the header and on every product, leading to a purpose-built quote form (product type, qty, certification needed, destination port/country, hire vs buy, timeline). Make "Contact" the secondary action.

2. **Product pages are one-line teasers with no detail, specs, or imagery depth.** Each product is a sentence and a "Read More". Buyers cannot self-qualify (sizes, payloads, certification, lead time, ex-stock availability). **Fix:** Build real product pages with specs, dimensions, certification badges (DNV 2.7-1 / EN 12079), photo galleries, and a per-product "Quote this product" button that pre-fills the form.

3. **Zero trust signals / social proof.** No testimonials, client/operator logos, case studies, certifications shown as badges, or "since 1983 / 40+ years / 12 branches" credibility band. **Fix:** Add a trust strip (years in business, branches, countries served, DNV & Lloyd's Register marks) plus 2-4 client testimonials or project case studies; surface the trade-press features (Offshore-Technology, Oil Review Africa) as "as seen in".

4. **Weak, buried, friction-heavy contact form.** Single generic CF7 form on one page, no quote-specific fields, no inline reassurance, reCAPTCHA can silently block. No WhatsApp option, important in African B2B. **Fix:** Quote form with the right qualifying fields, a phone and WhatsApp click-to-chat, and a clear "we reply within X hours" promise. Test reCAPTCHA isn't dropping submissions.

5. **Email/contact identity is inconsistent and off-brand.** Site is .com but emails are @containerworld.co.za and @containerworldoffshore.co.za; named contacts use the parent domain. This reads as unprofessional/unfinished to an international buyer. **Fix:** Standardise on @containerworldoffshore.com addresses and present a single clear sales contact route.

6. **Locations page is broken/empty placeholder.** 28+ countries each show "(1)", the same Cape Town phone, and a perpetual "Loading..." map. It promises local presence it cannot back up and looks broken. **Fix:** Either show genuine regional coverage (ports served, lead times by region, real local/agent contacts) or replace with an honest "We ship across Africa from Cape Town, ex-stock" coverage map. A broken page erodes trust at the decision moment.

7. **No clear value proposition or differentiation above the fold for the offshore buyer.** Hero says "Africa's Trusted Offshore Shipping Containers Supplier" but doesn't lead with the buyer's decision criteria (DNV/EN certified, ex-stock in Cape Town, short lead times, hire or buy, East & West Africa). **Fix:** Rewrite the hero around the buyer's job: certified, ex-stock, fast lead times, served across Africa, with the quote CTA right there.

8. **Multilingual content is dumped on one homepage instead of being properly localised.** English, French and Portuguese blocks stack on the home page, which is messy and hurts SEO and clarity. **Fix:** Proper language switching (hreflang, separate localised paths) so Francophone/Lusophone buyers get a clean, fully-translated experience including the quote form.

9. **Performance and SEO bloat from a heavy theme stack.** LogisCargo + WPBakery + RevSlider + multiple Google font families + jQuery migrate = slow, heavy pages on connections that matter for African mobile users. Thin content also limits ranking for "DNV offshore containers" type queries. **Fix:** Rebuild lighter (lean theme/blocks, optimised hero, fewer font families, lazy images), add proper product/service schema and substantive per-product copy so the site ranks and loads fast, which directly feeds quote volume.

### One-line opportunity
A 40-year, credible, internationally-relevant offshore B2B supplier is being represented by a thin, broken-in-places brochure site with no quote path and no trust signals. A goal-first rebuild around "Get a Quote" (real product pages + specs + certifications + trust + a proper quote form + clean localisation) is a clear, high-leverage win.
