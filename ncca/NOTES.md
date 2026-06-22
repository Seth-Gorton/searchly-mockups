# NCCA, Audit & Pitch Notes

URL audited: https://www.ncca.co.za/
Date: 2026-06-22

## What NCCA is (one line)
The National Contract Cleaners Association (NCCA), a South African industry/employers' association and professional body founded in 1989 that represents, accredits, and supports contract cleaning companies (and their suppliers) and positions itself as "The Voice of the Cleaning Industry in South Africa."

## What they do / offer
- A membership body for the contract cleaning industry (cleaning companies + industry suppliers).
- Sets and upholds professional standards; runs member audits and compliance.
- Awards member designations (professional-body status).
- Member benefits: networking, advocacy/representation (registered with the Department of Labour as an Employers Association), education, supplier directory, branch structure across provinces.
- Runs and promotes industry events and webinars (Cleantex Africa 2026, Facilities Management Expo, Golf Days, Women's Day events).
- Publishes articles/communications and member FAQs.

## Scale assessment: SMALL to lower-MEDIUM
WHY:
- Page count is modest: Home, Professional Body (about), National Members, Branches, Articles, Member FAQs, Apply for Membership / Membership Application Form, plus a cluster of dated event pages (Cleantex 2026, FM Expo 2026, Golf Day, JHB/WC Women's Day, Completed Events).
- The "directories" (National Members, Branches) are powered by a single WP Store Locator map plugin, not large bespoke CMS templates, so they don't add structural complexity.
- It is a single-purpose association site (inform members + recruit members), not a multi-service, multi-product, or transactional site.
- No ecommerce, no logins/portal of real depth (a basic member login exists), no deep content library.
- Net: a small organisation with a focused, content-light site. Sits at the top end of "small" because of the event sub-pages and two map directories.

## Platform / stack
- WordPress.
- Theme: GeneratePress (parent) with a child theme `generatepress_neo`.
- Builder: Elementor + Elementor Pro, heavily loaded with add-ons: Elementor Extras, Essential Addons, PowerPack Elements (flipbox, etc.).
- Plugins of note: WP Store Locator (member + branch maps).
- Fonts: Montserrat, Poppins, Roboto, Roboto Slab (multiple families loaded, a perf flag).
- Some legacy Divi CSS references still present in the DOM (likely leftover from a previous build), a bloat/cleanup flag.

## Real brand palette (HEX, from rendered DOM + screenshot)
- Primary blue: `#00a8dd` (the NCCA cyan/sky blue, logo + buttons + headings accent)
- Dark navy: `#071c3d` (footer / dark sections / deep headings)
- Secondary/legacy blue: `#1e73be`
- Neutrals: `#ffffff` (dominant background), `#000000`, greys `#3f3f3f`, `#666666`, `#222222`
The brand reads: corporate, clean, blue + white, slightly dated chrome/gradient logo.

## Logo + key images downloaded (in ./assets/)
- logo.png (the NCCA glossy blue diamond mark + wordmark, 176K)
- hero-bg.png (homepage hero cleaning background, 1.8M, oversized)
- image-1.jpg, image-2.jpg, image-3.jpg ("Why Appoint an NCCA Member" section photos)
- cleaners.png (cleaners imagery)
- cleantex-2026.png (Cleantex Africa 2026 event artwork)
- womens-day.jpg ("Women Thriving in Every Season" event card)
All verified as real images (image/png, image/jpeg) above 15KB.

## Reviews / social proof (real)
- No public Google Business star rating or review count surfaced for the NCCA (expected: it is a B2B membership association, not a consumer-facing business).
- Facebook: "National Contract Cleaners Association - NCCA | Germiston" page exists; no star rating / review count published.
- LinkedIn company page exists (NCCA South Africa).
- IMPLICATION for the pitch: the site cannot lean on consumer reviews. Its credibility currency is institutional, member logos, "since 1989," Department of Labour registration, professional-body/designation status, partner/brand logos (ISSA, Cleantex, Cleantex). These trust signals are present but under-used (see audit).

## Services / sections (homepage + nav)
Homepage sections (in order): Hero ("The Voice of the Cleaning Industry in South Africa", Apply for Membership / Find Your Nearest Branch) > three quick-action cards (Member Login, Search Contract Cleaner, Search Supplier) > "Why Appoint an NCCA Member?" benefits block > Upcoming Events & Webinars carousel > Featured Brands logo strip (ISSA, Cleaning World, Cleantex) > footer.
Nav / key pages: Home, Professional Body (about), National Members (map directory), Branches (map directory), Articles, Member FAQs, Apply for Membership / Membership Application Form, Designations, Compliance, Announcements, Communications, Completed Events, plus event pages (Cleantex Africa 2026, FM Expo 2026, Gauteng Golf Day 2026, JHB & WC Women's Day).

## Contact details
- Public email: national@ncca.co.za  (BEST public contact email)
- Phone: 0861 105 881
- Address: Helvetia House, 3rd Floor, 80 Greenvale Road, Germiston
- Hours: Mon to Fri, 08:00 to 16:30

## Primary conversion action this site should drive
Get qualified cleaning companies (and suppliers) to APPLY FOR / ENQUIRE ABOUT MEMBERSHIP. Secondary: let end clients find and trust an NCCA member (the member directory) so membership becomes more valuable, which feeds applications.

## Conversion-focused audit (issues hurting membership conversion + fixes)

1. The value proposition is vague and inward-looking.
   "The Voice of the Cleaning Industry" tells a prospect nothing about what membership DOES for their business. Fix: lead with an outcome-driven headline ("Win more cleaning contracts, prove you're compliant, and protect your business, join the NCCA") plus 3 to 4 concrete member benefits above the fold.

2. The primary CTA competes with three equal-weight cards.
   Member Login, Search Cleaner, and Search Supplier sit at the same visual weight as the membership goal, splitting attention. Fix: make "Apply for Membership" the single dominant CTA in the hero and repeated at section ends; demote utility actions (login/search) to a slimmer secondary row or header.

3. No proof of why membership is worth paying for.
   No member count, no "since 1989," no Department of Labour / professional-body credibility, no member testimonials surfaced near the CTA. Fix: add a trust band (years established, number of members, provinces, designations awarded) and 2 to 3 short member quotes with company names and logos.

4. Membership cost, categories, and process are hidden.
   Prospects can't see fees, member categories, or what the application steps are without hunting through PDFs. Fix: a clear "How to join" 3-step section + a transparent membership categories/fees comparison block. Pricing transparency removes the biggest objection.

5. Weak, slow, image-heavy hero with poor performance hygiene.
   Hero background is a 1.8MB PNG, four font families are loaded, and legacy Divi CSS plus a stack of Elementor add-ons bloat the page, hurting LCP and mobile experience. Fix: compress/convert hero to WebP under 200KB, cut to two fonts, remove unused Divi/add-on CSS, lazy-load below-fold media. Faster page = more completed applications, especially on mobile.

6. The member directory (the asset that makes membership valuable) is buried and basic.
   "Search Contract Cleaner / Supplier" run on a generic WP Store Locator map; an end client can't easily browse, filter by service or region, or see member profiles. Fix: rebuild the directory as a filterable, profile-rich listing (services, region, designation badge). A stronger public directory makes membership more sellable to prospects.

7. Forms and enquiry paths create friction.
   Membership is gated behind a downloadable application form rather than a simple inline "request membership info / start application" form, and there's no visible WhatsApp/quick-enquiry option, which converts well in SA B2B. Fix: add a short inline lead form (name, company, email, phone, province) plus a WhatsApp click-to-chat; deliver the full PDF after capture so leads aren't lost.

8. Events dominate but don't capture or convert.
   Dated event cards (some past) crowd the homepage, can look stale, and have no clear "register / add to calendar / notify me" capture. Fix: auto-hide past events, add a single "Upcoming events" CTA with email capture, and use events as a top-of-funnel lead magnet that routes interested non-members toward membership.

9. Trust/compliance signals are under-used and SEO/structure is thin.
   Designations, Compliance, and professional-body status are real differentiators but live as buried nav items, not front-and-centre proof; partner logos (ISSA, Cleantex) appear with no context. Fix: surface "Designations & Compliance" as a homepage trust pillar, label partner logos as accreditations/partners, and add clear page titles, meta, and schema (Organization) so the association ranks for "contract cleaning association South Africa" and "is my cleaner NCCA accredited."

## Pricing recommendation
R20 000 (once-off rebuild).
Justification: this is a small, single-purpose association site (about 8 to 12 real pages plus event sub-pages and two map directories), with no ecommerce or complex portal, so it fits the smaller-site tier; the main effort is conversion/trust restructuring and a cleaner directory, not page volume.
