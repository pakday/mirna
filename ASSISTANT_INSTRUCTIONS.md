# Assistant Instructions — MC Homes Real Estate (Mirna Chinchilla)

This file is the primary reference for all preferences, conventions, and client details for this project.

---

## Client Details

- **Business:** MC Homes Real Estate | Mirna Chinchilla
- **Website:** https://www.homesdanbury.com
- **Phone:** (203) 744-9879 | `+12037449879`
- **Email:** mirna@homesdanbury.com
- **Address:** 57 North Street, Danbury, CT 06810
- **Licensed since:** 2001 | Powered by **VORO** high-technology real estate platform
- **Social:** LinkedIn, Instagram (@mchomesbuysell), YouTube (@Mchomesrealestate), Facebook (/homesdanbury, /mchomesrealestate), Zillow, Realtor.com, BiggerPockets

## Areas Served

Danbury, New Milford, Bethel, Brookfield, Sherman, New Fairfield, Newtown, Ridgefield, Southbury, Norwalk — Fairfield & Litchfield Counties, CT

---

## Brand Colors

- **Primary (orange):** `#f7951b`
- **Secondary (blue/navy):** `#38529e`
- **Dark navy:** `#1a1a2e` / `#131d4a`

## Client Images (in `content/images/`)

- `mirna chinchilla mc homes.webp` — Full-body shot (blue suit, orange top, beach bg) → best for hero sections
- `MC Homes Real Estate Mirna Chinchilla 13rsq0cf7qa9nxf4gngzsqz.webp` — Headshot → best for bio/about sections
- Use Unsplash for additional real estate / Connecticut / home images

---

## Page Specialties Content Areas

- Probate & Inherited Property sales
- Downsizing & Empty Nesters
- Out-of-State Owners
- Landlords & Multi-Family
- Mortgage Stress / Pre-Foreclosure
- Buyer guidance

---

## CMS Code Delivery Requirements (CRITICAL)

The client's CMS only accepts raw HTML code blocks (no framework, no React, no Tailwind). The following structure MUST be followed:

1. **CSS must be in a `<style>` tag in the BODY, NOT in `<head>`**
2. Each section = one `<div id="short-section-id">` followed by a `<style>` tag immediately below it
3. Each section+style block is **self-contained and portable** — client can reorder sections freely
4. **CSS prefix:** All classes use `amc-` prefix to prevent conflicts with the live site styles
5. **Section IDs:** Short, descriptive, prefixed: `amc-hero`, `amc-stats`, `amc-about`, `amc-services`, etc.
6. **Container:** Every section uses `.amc-wrap` (max-width: 1280px, padding 32px/24px/16px desktop/tablet/mobile) — repeat in every section's style block for portability

### Container boilerplate (repeat in every section style):

```css
.amc-wrap {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 32px;
}
@media (max-width: 768px) {
  .amc-wrap {
    padding: 0 24px;
  }
}
@media (max-width: 480px) {
  .amc-wrap {
    padding: 0 16px;
  }
}
```

---

## Icon Usage Policy

- **Buttons:** Use inline Lucide SVG icons — NOT emoji, NOT icon font classes
- **Contact info rows:** Use inline Lucide SVG icons (MapPin, Phone, Mail, Globe, Clock)
- **Service/feature cards:** Colored emoji icons are acceptable (user approved this style)
- **SVG icons:** All inline SVG, `stroke="currentColor"`, `fill="none"`, Lucide icon set
- **Do NOT** import Lucide from CDN — paste SVG `<path>` code inline

### Common Lucide icons (inline SVG code):

**Phone:** `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 13a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.61 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg>`

**Mail:** `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>`

**MapPin:** `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/></svg>`

**Globe:** `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M12 2a14.5 14.5 0 0 0 0 20 14.5 14.5 0 0 0 0-20"/><path d="M2 12h20"/></svg>`

**ArrowRight:** `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>`

**ExternalLink:** `<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M15 3h6v6"/><path d="M10 14 21 3"/><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/></svg>`

---

## Design Style Guidelines

- **Font:** Inter (Google Fonts import in global reset section)
- **Heading sizes:** `clamp()` based, range from 1.7rem–2.4rem for h2
- **Dark backgrounds:** Use `#1a1a2e` → `#1d3278` → `#2b4eac` gradient
- **Hero sections:** Slightly lighter navy gradient + subtle dot grid pattern via `::before`
- **Section backgrounds alternate:** `#fff` and `#f6f8ff`
- **Testimonials/reviews sections:** Dark gradient bg — always scope `.amc-h2 { color: #fff }` using `#section-id .amc-h2` to avoid cross-section cascade issues
- **Cards:** `border-radius: 16px`, subtle border, hover lift effect, gradient bottom border stripe on hover
- **Buttons:** Orange primary `#f7951b`, ghost outlined white for dark backgrounds
- **CSS specificity caveat:** When using repeating class names across portable sections, scope colors with `#section-id .class` to prevent later section styles overriding earlier ones

## Important Links

- **Downsizing Market Report (CloudCMA):** https://cloudattract.com/50d0ff — Featured as sticky CTA on pages
- **Probate page slug:** `/selling-ct-probate-downsizing-specialist`
- **About page slug:** `/about-mirna-chinchilla`
- **Downsizing page slug:** `/downsizing-connecticut-realtor`

---

## SEO / Content Requirements (Client Provided)

Use these keyword targets across pages:

- local realtor, real estate agent, real estate agent agency, real estate agent broker
- real estate agent commission, real estate agent in connecticut, real estate agents near me
- realtor, realtor agency near me, realtor agents near me, realtor broker, top realtors
- Use REALTOR as the beginning of meta titles where applicable
- Use "realtor" 6 times per page
- MC Homes Real Estate powered by VORO
- Since 2001, Mirna Chinchilla, (203) 744-9879
- Add FAQ sections with "near me" keywords
- Include top, middle, and bottom CTAs

---

## Pages Built

| Page                 | File                                                                             | Status     |
| -------------------- | -------------------------------------------------------------------------------- | ---------- |
| About Mirna          | `content/pages/about-mirna-chinchilla/about-mirna-chinchilla.html`               | ✅ Built   |
| Probate & Downsizing | `content/pages/selling-ct-probate-downsizing-specialist/selling-ct-probate.html` | 🔲 Pending |

---

## Original Content Sources

- `content/pages/about-mirna-chinchilla/content.md` — About page scraped content
- `content/pages/about/content.md` — About page
- `content/pages/home/content.md` — Homepage
- `content/pages/selling-ct-probate-downsizing-specialist/content.md` — Probate page
- `content/🏡 REALTOR _ Downsizing Guidance for Families in Connecticut.md` — Client SEO doc (assigned to about page)
- `content/🏡 Sell Your Home Fast in Danbury, CT.md` — Client SEO doc (for sell/home page context)

---

## Legacy Notes

- Always prefer `content.cleaned.html` files as the cleaned page source for reading existing page structure.
- Do not restore or use deleted `content.html` exports.
- Raw HTML exports were removed intentionally.
