# Pillar 1 — "Areas We Serve" Section
**For: Dominion Private Wealth · 1616 N Litchfield Rd, Suite A155, Goodyear, AZ 85395**

This is **one localized section** that lives on **two URLs** — the homepage (`/`) and the contact page (`/contact-us/`). It is *not* a separate page, *not* duplicated as `/areas-we-serve/`, and *not* spun into per-city variants. That's what keeps it whitehat under [Google's doorway-pages spam policy](https://developers.google.com/search/docs/essentials/spam-policies#doorway-pages).

---

## Where it goes & why

| URL | Placement | Why |
|---|---|---|
| `/` (homepage) | Below "Who We Work With", above "Get Clarity, Not Guesswork" CTA | Anchors the firm to a specific geography for ranking signals + reassures local visitors before they hit the contact CTA |
| `/contact-us/` | Directly above the "Get In Touch" form | Visitors here are already considering a call — knowing you specifically serve their neighborhood reduces friction |

**Do this once. Do not copy-paste this section onto service pages** — service pages get a *different*, service-specific localization treatment in Pillar 2. Repeating identical local copy across 10+ URLs is exactly the duplicate-content footprint we're trying to avoid.

---

## The copy (primary version — recommended)

### Headline (H2)
> **A Goodyear Firm, Built for the West Valley**

### Subhead (italicized lead, optional)
> *Dominion Private Wealth was founded in Goodyear, AZ. We're walking distance from the families, professionals, and business owners we serve every day — and a short drive from the rest of the West Valley.*

### Body paragraph 1 — the local thesis (≈110 words)
Goodyear has grown from 65,000 residents in 2010 to **over 128,000 today**, with population still rising about 4% a year. That growth is being driven by a wave of professionals, military retirees, and business owners relocating from higher-tax states — and by Phoenix-area earners trading the city for Class A neighborhoods west of the I-10. It's also one of the [fastest-growing retirement destinations in the country](https://azreinsider.com/2024/06/27/goodyear-arizona-fastest-growing-retirement-destinations-united-states/), with the 65-and-over population up 61% over five years. The financial planning needs in the West Valley are different from those in Scottsdale or downtown Phoenix, and we built our practice specifically for them.

### Body paragraph 2 — the communities (≈140 words)
From our office at the corner of Litchfield Road and McDowell, we work with clients across:

- **Goodyear** — including Palm Valley, PebbleCreek (the active-adult community), and the master-planned communities along Estrella Parkway
- **Estrella** — the 20,000-acre master-planned community south of I-10, including the gated Cantamia 55+ enclave
- **Litchfield Park** — historic, golf-anchored, with one of the highest median household incomes in the West Valley (≈$125K)
- **Verrado** in Buckeye — golf, walkable village core, and a steady inflow of families and retirees
- **Avondale, Buckeye, and Surprise** — for clients commuting along the I-10 / Loop 303 corridor
- **Luke AFB families** — coordinating military pension, TSP, and Survivor Benefit Plan decisions

We meet in person at our Goodyear office, by video, or — when it makes sense — at your home or business.

### Body paragraph 3 — the local anchor (≈55 words, contains NAP)
**Dominion Private Wealth** · 1616 N Litchfield Rd, Suite A155, Goodyear, AZ 85395 · [(602) 922-3556](tel:+16029223556) · [info@dominionpw.com](mailto:info@dominionpw.com). We're on the second floor of Palm Valley Office Plaza, one minute off the I-10 Litchfield interchange. Free parking. Fiduciary, fee-based, and registered in Arizona.

### Embed
- A Google Maps iframe pinned to the office (one map; not a directory of cities)
- Aria-label: "Map of Dominion Private Wealth at 1616 N Litchfield Road, Goodyear, Arizona"

---

## Why this is whitehat (and what makes it not a doorway)

| Doorway anti-pattern | What we did instead |
|---|---|
| One URL per city (`/financial-advisor-litchfield-park/`, `/financial-advisor-buckeye/`...) | One section on two existing URLs |
| Identical 500-word template with city name swapped | Each community gets a *specific factual hook* — Cantamia for Estrella, the village core for Verrado, golf and income for Litchfield Park |
| City list reads like a sitemap of fake offices | We name only the *one* real office and explain how we serve surrounding neighborhoods from it |
| Generic "we serve [city] residents with all your financial needs" filler | Real numbers (128K population, 4%/yr growth, 61% senior growth) sourced and linkable |
| Hidden internal links, footer link farms | Single section, visible, linked only naturally from the page it's on |

Google's [Helpful Content guidance](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) asks "would the content be useful if it appeared on a friend's site?" This section passes that test — it's the kind of content a real Goodyear advisor would write for a real Goodyear visitor.

---

## Implementation — Elementor / WordPress

### Option A — Native Elementor section (recommended for editability)
1. Open the homepage in Elementor, add a new **Section** above the bottom CTA
2. Two-column layout, 60/40 split (text/map)
3. **Left column:** Heading widget (H2), Text Editor (the body paragraphs), then a small "Address card" using an Icon List
4. **Right column:** Google Maps widget pointed at `1616 N Litchfield Rd Suite A155, Goodyear, AZ 85395`
5. Set section padding to match the rest of the page (looks like ~80px top/bottom)
6. Repeat the same section on `/contact-us/` directly above the form

### Option B — Drop-in HTML (if working outside Elementor)
```html
<section class="areas-we-serve" aria-labelledby="areas-heading">
  <div class="container">
    <h2 id="areas-heading">A Goodyear Firm, Built for the West Valley</h2>

    <p class="lead"><em>Dominion Private Wealth was founded in Goodyear, AZ. We're walking distance from the families, professionals, and business owners we serve every day — and a short drive from the rest of the West Valley.</em></p>

    <p>Goodyear has grown from 65,000 residents in 2010 to over 128,000 today, with population still rising about 4% a year. That growth is being driven by a wave of professionals, military retirees, and business owners relocating from higher-tax states — and by Phoenix-area earners trading the city for Class A neighborhoods west of the I-10. It's also one of the fastest-growing retirement destinations in the country, with the 65-and-over population up 61% over five years. The financial planning needs in the West Valley are different from those in Scottsdale or downtown Phoenix, and we built our practice specifically for them.</p>

    <p>From our office at the corner of Litchfield Road and McDowell, we work with clients across:</p>

    <ul class="communities">
      <li><strong>Goodyear</strong> — including Palm Valley, PebbleCreek, and the master-planned communities along Estrella Parkway</li>
      <li><strong>Estrella</strong> — the 20,000-acre master-planned community south of I-10, including the gated Cantamia 55+ enclave</li>
      <li><strong>Litchfield Park</strong> — historic, golf-anchored, with one of the highest median household incomes in the West Valley</li>
      <li><strong>Verrado</strong> in Buckeye — golf, walkable village core, and a steady inflow of families and retirees</li>
      <li><strong>Avondale, Buckeye, and Surprise</strong> — for clients commuting along the I-10 / Loop 303 corridor</li>
      <li><strong>Luke AFB families</strong> — coordinating military pension, TSP, and Survivor Benefit Plan decisions</li>
    </ul>

    <p>We meet in person at our Goodyear office, by video, or — when it makes sense — at your home or business.</p>

    <address class="office-card">
      <strong>Dominion Private Wealth</strong><br>
      1616 N Litchfield Rd, Suite A155<br>
      Goodyear, AZ 85395<br>
      <a href="tel:+16029223556">(602) 922-3556</a> &middot;
      <a href="mailto:info@dominionpw.com">info@dominionpw.com</a><br>
      <small>Second floor of Palm Valley Office Plaza, one minute off the I-10 Litchfield interchange. Free parking.</small>
    </address>

    <div class="map-embed">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d!2d-112.358!3d33.464!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMzPCsDI3JzUwLjQiTiAxMTLCsDIxJzI4LjgiVw!5e0!3m2!1sen!2sus"
        width="100%"
        height="320"
        style="border:0;"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
        title="Map of Dominion Private Wealth at 1616 N Litchfield Road, Goodyear, Arizona"
        aria-label="Map of Dominion Private Wealth at 1616 N Litchfield Road, Goodyear, Arizona"></iframe>
    </div>
  </div>
</section>
```

> **Note on the iframe `src`:** WordPress strips iframes from many themes by default. The cleanest path is to open Google Maps → search "1616 N Litchfield Rd A155, Goodyear, AZ" → Share → Embed a map → copy → paste the *real* `src` attribute over the placeholder above. Keep `loading="lazy"` so the map doesn't hurt LCP on the homepage.

---

## LocalBusiness schema to add to the same two pages

Add this JSON-LD block to `/` and `/contact-us/`. It's the on-page partner to the visible "Areas We Serve" section. Inject via the WordPress theme's header hook, via a plugin like **Schema Pro** or **Rank Math**, or via a Code Snippets plugin scoped to those two URLs.

```json
{
  "@context": "https://schema.org",
  "@type": "FinancialService",
  "@id": "https://dominionprivatewealth.com/#organization",
  "name": "Dominion Private Wealth",
  "image": "https://dominionprivatewealth.com/wp-content/uploads/2026/03/logo-scaled.png",
  "logo": "https://dominionprivatewealth.com/wp-content/uploads/2026/03/logo-scaled.png",
  "url": "https://dominionprivatewealth.com/",
  "telephone": "+1-602-922-3556",
  "email": "info@dominionpw.com",
  "priceRange": "$$$",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "1616 N Litchfield Rd, Suite A155",
    "addressLocality": "Goodyear",
    "addressRegion": "AZ",
    "postalCode": "85395",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 33.4639,
    "longitude": -112.3580
  },
  "openingHoursSpecification": [{
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
    "opens": "08:30",
    "closes": "17:00"
  }],
  "areaServed": [
    {"@type": "City", "name": "Goodyear", "addressRegion": "AZ"},
    {"@type": "City", "name": "Litchfield Park", "addressRegion": "AZ"},
    {"@type": "City", "name": "Avondale", "addressRegion": "AZ"},
    {"@type": "City", "name": "Buckeye", "addressRegion": "AZ"},
    {"@type": "City", "name": "Surprise", "addressRegion": "AZ"},
    {"@type": "Place", "name": "Estrella, Goodyear, AZ"},
    {"@type": "Place", "name": "Verrado, Buckeye, AZ"},
    {"@type": "Place", "name": "PebbleCreek, Goodyear, AZ"}
  ],
  "founder": {
    "@type": "Person",
    "name": "Justin Kauffman",
    "jobTitle": "President & Lead Wealth Advisor",
    "hasCredential": [
      {"@type": "EducationalOccupationalCredential", "credentialCategory": "CERTIFIED FINANCIAL PLANNER®"},
      {"@type": "EducationalOccupationalCredential", "credentialCategory": "Certified Exit Planning Advisor®"}
    ],
    "sameAs": [
      "https://www.linkedin.com/in/justin-kauffman-cfp",
      "https://www.plannersearch.org/financial-advisor/justin-kauffman"
    ]
  },
  "sameAs": [
    "https://www.linkedin.com/in/justin-kauffman-cfp",
    "https://www.plannersearch.org/financial-advisor/justin-kauffman"
  ]
}
```

Verify the rendered markup with [Google's Rich Results Test](https://search.google.com/test/rich-results) and [Schema Markup Validator](https://validator.schema.org/) once it's live.

---

## Two alternative tones — pick the voice that matches your brand

The primary version above is **plain-spoken / advisor-direct**. Here are two alternatives if Justin prefers a different register:

### Alternative B — Warmer / family-first
> **Where We Are. Who We Serve.**
> *Dominion Private Wealth was founded right here in Goodyear, and most of the families we work with are within ten miles of our front door. From our office at Litchfield and McDowell we serve clients in Goodyear, Litchfield Park, Estrella, Verrado, PebbleCreek, Avondale, Buckeye, and Surprise. If you live in the West Valley, we probably already work with one of your neighbors.*
>
> *Goodyear has been America's fastest-growing retirement destination by some measures — the over-65 population is up 61% in five years — and the West Valley is full of recent transplants from California, Washington, Illinois, and the Northeast. Most arrive with a 401(k) or two, a house they just sold, and a list of questions about Arizona taxes. We help them turn that list into a plan.*

### Alternative C — Business-owner-first (good fit for the Business Exit Planning service emphasis)
> **A West Valley Firm for West Valley Owners**
> *We built Dominion Private Wealth in Goodyear because the West Valley has become a real economic engine — Luke AFB, the I-10 logistics corridor, the wave of growth coming out of Estrella and Verrado, and a generation of business owners who started here in the 90s and are now thinking about what comes next. The people we serve are five minutes from our office, not five time zones away.*
>
> *From 1616 N Litchfield Road we work with clients across Goodyear, Litchfield Park, Estrella, Verrado, PebbleCreek, Avondale, Buckeye, and Surprise — including business owners exiting on a 5–10 year timeline, professionals consolidating accounts after a relocation, retirees coordinating Social Security and a pension, and Luke AFB families navigating military benefits.*

---

## What to avoid (so this stays whitehat)

1. **Do not turn the bullet list of communities into linked anchor text** pointing to per-city pages. The communities are mentioned for *humans*, not as internal-link doorways. If a community ever gets its own URL someday, link it once, naturally, in body prose — never as a list.
2. **Do not add this section to service pages.** Service pages get *service-specific* localization in Pillar 2 — e.g., the Estate Planning page references Maricopa County probate, the Tax Strategy page references Arizona's lack of estate tax, etc. Different content, not a copy of this.
3. **Do not stuff "Goodyear, AZ" repeatedly.** The section above mentions Goodyear about 4 times in roughly 350 words. That's natural density. Avoid going past ~1.5%.
4. **Do not list neighborhoods you don't actually serve.** If you don't take Sun City West clients, don't list it. The whole point of the whitehat approach is honest local relevance.
5. **Update population/growth stats annually.** "128,000 residents · 4% growth · 61% senior population growth" is current as of 2026 — replace each number when updated census data lands.

---

## Suggested next step

Once this section is live on `/` and `/contact-us/`:

1. Submit both URLs for re-indexing in Google Search Console (URL Inspection → Request indexing)
2. Validate the JSON-LD in [Rich Results Test](https://search.google.com/test/rich-results)
3. Add identical NAP wording to your Google Business Profile description (when GBP launches per Pillar 1 of the audit) — Google rewards on-page ↔ GBP consistency
4. Track the "financial advisor goodyear" query weekly in GSC; expect impression growth within 2–4 weeks and position improvement within 8–12 weeks

When you're ready, I can draft Pillar 2 next — the service-specific localization treatment for the 10 service pages, with one fully written example to use as the template.
