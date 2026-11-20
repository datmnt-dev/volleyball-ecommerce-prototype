# SÂN/06 — Volleyball E-commerce UI Concept (Vietnamese)

**Two-page responsive UI prototype:**
- `index.html`: **Homepage / storefront** — navigation, brand hero, categories, collection filters, product cards, quick size select, simulated cart, size guide and newsletter demo.
- `landing.html`: **Campaign landing page** — Drop 01 brand narrative, full-screen hero, manifesto, lookbook, featured lineup, FAQ, CTA linking to the shop.
- `styles.css` shared responsive visual system; `app.js` shared behavior; `assets/*.svg` original vector illustration of demo products.

## Run locally

You can open `index.html` or `landing.html` directly. For the most consistent result, serve the folder via a static HTTP server:

```bash
cd volleyball-store
python -m http.server 8000
# http://localhost:8000/  (homepage)
# http://localhost:8000/landing.html  (landing)
```

Product illustrations are bundled; typography and volleyball action photo load from external sources if connected to the internet, with standard font/color fallbacks. **No build dependencies required.**

## Brand assumptions — replace before production

- `SÂN/06` is a **working fictional concept name** (not legally checked, not a real trademark claim).
- All product images, descriptions, product features, prices, sizes and availability are **mock/sample data**. No representation that actual products exist.
- Product SVGs were created for this prototype and do not depict real inventory.
- There is no backend, inventory, account, payment, checkout, fulfillment, contact or email-list collection. Add-to-cart is a browser-only localStorage simulation (`san06-demo-cart-v1`).
- Subscription UX validates an email locally but does not collect or transmit it.
- Address `hello@example.com` is a placeholder.
- Verify product and supplier details, shipping/returns, business information, and legal/commercial content before launch.

## Design system

| Token | Value | Use |
|---|---|---|
| Paper | `#f1f0e9` | Base canvas |
| Dark navy | `#123653` | Functional CTAs, navigation and editorial blocks |
| Ink | `#183953` | Main text |
| Rust | `#d66749` | Controlled emphasis |
| Gold | `#dfb963` | Volleyball / high-energy accent |
| Display | Barlow Condensed 800–900 | Impactful sports headlines |
| Interface | Manrope 500–900 | Navigation, product information and controls |

Layout: max content width 1360px, 4-column desktop grid, 2-column mobile grid, bolder type hierarchy and one purposeful moving marquee. Avoid generic gradient glows, 3D decorations, arbitrary animated cards and repeated pill-shaped SaaS UI components.

## Homepage / landing distinctions

**Homepage** answers: What can I buy? Can I navigate by category? What is the price? Which size? Where is the cart?

**Landing** answers: Why does this brand exist? What is Drop 01? What is the emotional story? Where can I explore the collection?

Both link into a consistent commercial discovery journey.

## Conversion and UX checklist for implementation

1. Establish actual audience: volleyball clubs, school/student players, competitive athletes, beach vs indoor; price segment and product sourcing.
2. Confirm brand and product photography. Real shooting should show players in motion AND product fit/product material. Never use third-party athlete imagery to imply endorsement.
3. Replace product data with reliable catalog source: product ID/SKU, category, variants, actual stock, image dimensions, price and discount price, specifications, fabric composition, legal size charts, reviews if real.
4. Add search with keyboard focus, filter/sort, actual search results, collection pagination and empty states.
5. Build PDP with detailed images, size finder, wash instructions, available stock, exchange policy, shipping estimate, FAQ, related items.
6. Connect cart to real platform and inventory, validate prices server-side, add checkout, payment provider, order confirmation and error states. Never trust browser cart values.
7. Add required business pages, returns, privacy, terms, accessibility and SEO metadata, analytics with privacy choices.
8. Measure Web Vitals (LCP, CLS, INP), use `next/image` and production photo assets; test keyboard, screen readers, mobile performance, 320/375/768/1440px.
9. Perform 5–8 customer usability sessions on mobile: locate desired item, find correct size, add item, estimate total cost, reach checkout.

## Production-ready architecture recommendation

For a developer-led custom shop, use **Next.js App Router + TypeScript + Tailwind CSS** with a headless commerce platform (e.g. Shopify Storefront APIs). For a fast merchant-operated launch, a **Shopify theme (Horizon / Impact)** customized with this visual system is often simpler. Do not hand-roll payment or order security. Shopify licensing and pricing depend on the merchant plan and theme chosen.

Suggested conceptual Next.js structure:

```
app/
  (marketing)/drop-01/page.tsx
  (store)/page.tsx
  (store)/collections/[slug]/page.tsx
  (store)/products/[handle]/page.tsx
  cart/page.tsx
components/{layout,commerce,editorial}/
lib/{catalog,cart,analytics}/
styles/tokens.css
```

## Research/design sources used

- Anthropic's official frontend design guidance: https://github.com/anthropics/claude-code/blob/main/plugins/frontend-design/skills/frontend-design/SKILL.md
- Anthropic design article: https://claude.com/resources/articles/improving-frontend-design-through-skills
- Shopify Impact: https://themes.shopify.com/themes/impact/presets/impact
- Shopify Prestige: https://themes.shopify.com/themes/prestige/presets/prestige
- Shopify Horizon: https://themes.shopify.com/themes/horizon/presets/horizon
- Vercel Next.js Commerce: https://examples.vercel.com/templates/template/nextjs-commerce
- LOVB Shop: https://shop.lovb.com/
- Volleyballa: https://volleyballa.com/
- Volleyball action photograph (Unsplash): https://unsplash.com/ja/%E5%86%99%E7%9C%9F/%E3%83%90%E3%83%AC%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%AB%E3%81%AE%E8%A9%A6%E5%90%88%E3%82%92%E3%81%99%E3%82%8B%E8%8B%A5%E8%80%85%E3%81%9F%E3%81%A1%E3%81%AE%E3%82%B0%E3%83%AB%E3%83%BC%E3%83%97-iIjBPKg5p6s
- Unsplash license: https://unsplash.com/license

**Note:** Earlier datmnt-dev portfolio/TripMate details were recovered from available prior-project evidence. GitHub connector did not expose those repositories' code in this session, so do not represent this as a pixel-matched implementation of the existing portfolio design system. No Figma account, repository, or live site was modified.
