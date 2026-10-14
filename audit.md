# Synergy Chiropractic website audit

Measured October 13, 2026 (mobile PageSpeed Insights, Lighthouse 13.5.0). Scores are lab snapshots and may vary between runs.

## Evidence-led recommendation

Use **synergychiromi.com** as the likely primary-domain candidate, subject to confirming Google Search Console, Analytics, backlink data, registrar ownership, and the Google Business Profile website field before migration.

Why: it uses the practice's consistent public phone number and physical address, names Dr. Eric Mintz, offers a functioning appointment path, has a self-referencing homepage canonical, and has multiple pages visibly indexed in search. The other domain has useful service/location URL inventory, but its homepage has serious template-quality and identity problems.

## 1. synergychiropracticmi.com — separately audited

- HTTP redirects to HTTPS and the homepage loads in a normal browser.
- Mobile PageSpeed: **49 Performance / 88 Accessibility / 100 Best Practices / 100 SEO**.
- Lab metrics: FCP 5.8s, LCP 7.5s, TBT 290ms, CLS 0.13, Speed Index 6.7s.
- No field data was available in PageSpeed Insights.
- Approximate payload reported by Lighthouse: 3,074 KiB.
- Major opportunities: unused JavaScript (~273 KiB), unused CSS (~51 KiB), render-blocking work, cache lifetimes, missing explicit image dimensions, nine long main-thread tasks, and contrast/semantic accessibility issues.
- The homepage has no discoverable canonical tag in the rendered document.
- Contact phone shown repeatedly: **(248) 505-5991**, which conflicts with the established practice number.
- Contact email shown: **dreric@hotmail.com**.
- The homepage has a lead form but no clear appointment-booking flow.
- It contains obvious contractor-template remnants: “Schedule Your Estimate,” “property visit,” “approve our estimate,” and “Get The Job Done.”
- One service image uses an unresolved template token in alt text: `{{ custom_values.service_1 }} in {{custom_values.biz_area_1})`.
- Empty placeholder URLs remain in navigation: service-9/10/11 and service-area-9 through 14.
- It has a broad service/location-page structure that may contain recoverable organic-search value, but that value needs Search Console and backlink verification.
- A focused public search did not surface this domain while the other domain returned multiple indexed pages. This is evidence of weaker visible index support, not proof that no URLs are indexed.

## 2. synergychiromi.com — separately audited

- Mobile PageSpeed: **61 Performance / 98 Accessibility / 100 Best Practices / 92 SEO**.
- Lab metrics: FCP 5.0s, LCP 12.1s, TBT 60ms, CLS 0, Speed Index 5.8s.
- No field data was available in PageSpeed Insights.
- Major opportunities: render-blocking work (~1.35s), image delivery (~371 KiB), unused JavaScript (~341 KiB), unused CSS (~128 KiB), missing explicit image dimensions, and an extremely slow hero/LCP asset.
- Homepage canonical is correctly self-referencing: `https://www.synergychiromi.com/`.
- Lighthouse flags a missing homepage meta description.
- Primary business details are consistent: **(248) 862-2202**, **6230 Orchard Lake Road, Suite 235, West Bloomfield, MI 48322**, **dreric@synergychiromi.com**.
- Names Dr. Eric Mintz and describes 25 years of experience.
- Provides contact/appointment paths and a detailed first-visit page.
- Multiple pages surfaced in public search: homepage, contact, about, services, first-visit, older articles, and patient-form PDFs.
- Current homepage includes visible draft residue (“YOUR PHOTOS HERE”); the services page also contains “Description text goes here” and “Item description.”
- Heading structure is weak: the rendered homepage has many empty H1 elements and one repeated marquee-like H1.
- The footer appointment link points to `/contact`, while the primary contact page is `/contact-us`; this should be tested and standardized.
- Search results expose legacy WordPress-era URLs/PDFs with an older address (6400 Farmington Rd), creating a local-SEO/NAP cleanup need.

## Duplicate-domain risk and migration plan

Two domains are not automatically a penalty. The risk is that overlapping pages split crawl signals, links, relevance, and brand trust while presenting contradictory contact information.

Recommended sequence:

1. Verify ownership and exports from Google Search Console, GA4, GBP, registrar, and each CMS.
2. Inventory every indexable URL, backlink-bearing URL, conversion path, form, and PDF on both domains.
3. Confirm the authoritative phone, email, address, services, and booking system with Dr. Eric.
4. Select one canonical domain based on evidence; current public evidence favors `synergychiromi.com`.
5. Rebuild the strongest useful service/location content without thin doorway pages or duplicated copy.
6. Create a one-to-one 301 map from every valuable retired URL to its closest new equivalent; do not blanket-redirect everything to the homepage.
7. Update canonicals, XML sitemap, robots directives, internal links, GBP website URL, citations, social profiles, and campaign links.
8. Keep redirects live long-term and monitor coverage, rankings, 404s, and conversions.

## Redesign performance target

The concept is mobile-first, static, accessible, and intentionally light on JavaScript. The implementation target is **90+ mobile Lighthouse**, not a guarantee. Final results depend on the production CMS, fonts, analytics, scheduling embeds, consent tools, hosting, and optimized image variants.
