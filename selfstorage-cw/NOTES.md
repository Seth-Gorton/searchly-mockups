# Self Storage CW, Audit Notes

Audited: 2026-06-19
URL: https://www.selfstoragecw.co.za
Primary desired action: GET A QUOTE / enquire to reserve a storage unit.

## Business summary

Self Storage CW is the self-storage arm of Container World (Pty) Ltd, a South African
container company. They rent out converted shipping-container storage units (new, steel,
anti-vandal, watertight, vermin-proof, hardwood floors) to the public for personal or
business use, short or long term, on a month-to-month lease. They operate across four
cities: Durban, Polokwane, Midrand (Johannesburg) and Nelspruit. The tagline they lead
with is "We provide you a self storage experience of trust and safety, to give you peace
of mind."

## What they offer

- Container self-storage units (single size: 6.05m x 2.44m x 2.59m, a standard 20ft container).
- Two unit tiers (per the Midrand microsite):
  - Top-level units from R700 excl VAT / month
  - Ground-floor units from R950 excl VAT / month
- Month-to-month lease, auto-renews on the 1st, 10-day written notice to vacate.
- Tenant brings and stores their own goods (no packing/moving service offered).
- Tenant arranges their own insurance (not included in rent).
- Restrictions: no explosives, flammables, hazardous goods, chemicals, contraband, gas bottles.

Selling points listed on the homepage ("We offer"):
Complete steel anti-vandal construction; watertight and durable; vermin proof; patented
easy-opening access door; hardwood flooring; 24-hour on-site security; affordable;
conveniently located. Security also includes electric fencing, CCTV, fire protection,
floodlit paved areas. Access weekdays 08:00 to 17:00, after-hours by arrangement.

## SCALE: SMALL-to-MEDIUM

Justification:
- It is a real multi-location operator (4 cities, 4 separate phone lines and email
  addresses), backed by a larger parent company (Container World), so it is NOT a
  one-person micro-business. That pushes it above "small."
- BUT the public web presence is tiny: a single-page WordPress site (one page, ID 719,
  no internal pages, no per-location pages, no unit-detail pages, no blog). A separate
  thin microsite exists for Midrand (selfstoragecwmidrand.co.za). One product (containers),
  effectively two price tiers.
- No ecommerce, no online reservation, no account system. Lead capture only.
- Conclusion: a small-to-medium lead-gen business with a small-site footprint. The
  redesign opportunity is medium: a proper multi-location lead-gen site (location pages,
  pricing, real photography, online enquiry/reserve) rather than a large build.

## Platform / stack

- CMS: WordPress
- Page builder: Elementor (kit 924), theme GeneratePress
- Forms: Gravity Forms ("Get A Quote" widget on homepage)
- Performance: WP Rocket (lazyload + delayed JS), Yoast SEO v27.6
- Hosting: standard WordPress hosting (wp-content/uploads), assets dated 2019 (site is ~7 years old, unchanged)
- Tags: Google Tag Manager dns-prefetch present (GTM/GA likely installed; not deeply verified)
- Built by Vetro Media (credit in footer)

## Brand HEX palette (pulled from rendered page + DOM)

- Primary blue (logo / headings accent): `#1289ca`
- Deep navy/blue (heading text used on hero, e.g. "GET A QUOTE"): `#075da8`
- Brand red (accent, Container World red): `#e31618`
- Darker red shade: `#c02b0a`
- Near-black text / dark grey: `#3c3c3b` (also `#27292a`, `#3a3a3a`)
- White: `#ffffff`
Hero imagery is dominated by container-blue (corrugated steel) tones, reinforcing the
blue-and-red brand. Logo "Self Storage" uses blue + red.

## Brand feel

Practical, utilitarian, trust-led. Hero is a friendly smiling man (in a blue checked shirt)
arms folded in front of a blue container, oversized red/blue all-caps condensed headline
"WE PROVIDE YOU A SELF STORAGE EXPERIENCE OF TRUST AND SAFETY." Stock-ish, dated 2019.
Reads honest and local but visually flat and old.

## Asset filenames (downloaded to ./assets/)

- logo-self-storage.png (842x384, transparent, the Self Storage CW logo)
- logo-container-world.png (310x170, parent Container World logo)
- hero-header.jpg (1000x754, blue container backdrop, hero)
- box-girl.jpg (1000x557, person with moving boxes)
- pushing.jpg (800x600, person pushing/moving)
- yard.png (800x540, container yard / facility)
- mid-slider.jpg (1200x802, mid-page slider image)
- solutions-2.jpg (679x843, solutions image, portrait)
- solutions-3.jpg (684x385, solutions image)
- man-units.jpg (600x600, man at the units, IMG_4829)

All ten verified as valid images. Note quality: JPEGs are gd-jpeg quality ~68 to 69
(noticeably compressed), low resolution by 2026 standards. Usable as placeholders;
a redesign should source fresh, higher-res facility/unit photography.

## Real reviews

No public Google rating, review count, or testimonials could be found. WebSearch across
Google/Facebook/directory listings returned the business profiles but surfaced no star
rating or count, and the homepage itself displays zero testimonials or trust badges.
This absence of social proof is itself a conversion finding (see audit issue 4).
The Facebook page (facebook.com/SelfStorageMidrand) exists but exposed no rating/review text.

## Contact + locations

- Polokwane: Tel +27 15-298 9118, pk@selfstoragecw.co.za
- Durban: Tel +27 31-825 6641, dbn@selfstoragecw.co.za
- Midrand (JHB): Tel +27 11-392 1284, jhb@selfstoragecw.co.za
  Address: Cnr Hooker St & Chloor Rd, Chloorkop, Edenvale, 1622
- Nelspruit: Tel +27 13-755 1719 / +27 13-755 1729, info.ns@containerworld.co.za

## CONVERSION AUDIT (primary action = Get a Quote / reserve a unit)

1. No pricing on the main site, the biggest objection unanswered.
   The homepage never states what a unit costs. Pricing (from R700 / from R950 excl VAT)
   exists only on the separate Midrand microsite. Storage shoppers compare on price first;
   hiding it forces them to enquire blind or bounce to a competitor who shows it.
   Fix: publish a clear pricing block on the homepage and on each location page (size,
   "from R___ /month", what is included), with a "Reserve this unit" CTA next to it.

2. Single generic enquiry form with no location selection clarity / no instant routing.
   One "Get A Quote" form serves four cities. Leads must be manually triaged, and the
   visitor cannot tell if there is even a unit near them before submitting. Slow routing
   loses hot leads.
   Fix: add a location selector that routes the lead to the right branch inbox, pre-fills
   the branch phone/WhatsApp, and shows that branch's availability/price. Auto-reply with
   next steps.

3. No WhatsApp or click-to-call prominence, the SA default for this audience.
   Phone numbers sit only in the footer. There is no sticky call/WhatsApp button. South
   African storage enquirers strongly prefer WhatsApp and a quick call.
   Fix: add a sticky "WhatsApp us" + "Call now" bar (mobile-first), one per location, plus
   click-to-call on every displayed number.

4. Zero social proof (no reviews, ratings, testimonials, or trust badges).
   Storage is a trust purchase ("are my belongings safe with strangers?"). The site asserts
   "trust and safety" but shows nothing to back it: no Google rating, no testimonials, no
   "years in business / units secured" numbers, no security accreditation logos.
   Fix: pull and embed Google reviews per location, add 3 to 5 written testimonials,
   surface the Container World heritage and "X years, 24/7 monitored" proof points.

5. No real "how it works" / reserve path, the journey to booking is undefined.
   A first-time storage renter does not know the steps (choose size, get quote, sign,
   move in, access). The site jumps from features straight to a form.
   Fix: add a simple 3 to 4 step "How it works" section ending in the primary CTA, and a
   size-guide ("what fits in a unit") to help self-qualify and reduce wrong-size enquiries.

6. Weak, low-trust hero with a typo in the page title.
   The browser title reads "A Self Storage Experience of Trust & Tafety" ("Tafety", a
   visible typo that also hurts SEO and credibility). The hero headline is huge but the
   value proposition (price, locations, security, "reserve online") is not summarised, and
   the CTA button copy is generic.
   Fix: fix the typo; rewrite the hero to lead with the concrete promise (secure 20ft
   container units in DBN/JHB/PBG/Nelspruit, from R700/mo, 24/7 monitored), and use action
   CTA copy ("Get my quote" / "Reserve a unit").

7. Dated, slow, heavy 2019 build with low-quality compressed images.
   All imagery dates to 2019 at quality ~68 JPEG, the design is a flat Elementor template,
   and the heavy Elementor + WP Rocket delay-JS stack adds weight. Slow, dated pages erode
   trust and Core Web Vitals (and Ads Quality Score / cost-per-lead).
   Fix: rebuild lighter with fresh, high-res facility and unit photography (real branches),
   modern responsive layout, and a performance budget so the quote form loads fast.

8. No per-location landing pages, hurts both conversion and local SEO/Ads.
   Four cities share one page (plus one stray Midrand microsite). A visitor searching
   "self storage Durban" lands on a generic national page with no Durban-specific address,
   map, photos, price, or hours. This also wastes Google Ads spend (poor message match,
   low Quality Score).
   Fix: build a dedicated, indexable landing page per location (address, embedded map,
   branch photos, branch price, branch hours, branch phone/WhatsApp, branch enquiry form)
   with LocalBusiness schema, and point each city's Ads campaign at its matching page.

9. Thin FAQ and no urgency / scarcity or guarantees near the CTA.
   The FAQ covers access and rules but nothing reassuring at the decision point (move-in
   today? deposit? cancellation? security guarantee). There is no nudge to act now.
   Fix: surface trust-and-objection answers right beside the form (no long lock-in,
   10-day notice to leave, 24/7 monitored, move in fast), and add a soft urgency line
   ("limited units per branch, reserve yours").

## Redesign recommendation (one line)

Rebuild as a fast, modern, multi-location lead-gen site (WordPress or lighter): one
indexable landing page per branch with real photography, transparent pricing, a
location-routed quote form, sticky WhatsApp/call, Google reviews, and a clear
"how it works to reserve" path, with GA4 + Ads conversion tracking on the enquiry.
