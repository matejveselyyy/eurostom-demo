# EUROSTOM demo site

Free-value cold-outreach demo for a family-run cosmetic dentistry clinic in Brno, CZ.
Single-file static site. No framework, no build step.

**Live:** https://eurostom-demo.vercel.app

## Stack

- `index.html` — single file, inline CSS + JS
- MapLibre GL JS (Carto light raster tiles) with custom tan pin
- Playfair Display 300 + Inter, warm tan (`#A6957E`) on cream (`#FDFBF5`)
- IntersectionObserver for reveals, `requestAnimationFrame` for hero parallax
- Vercel static hosting

## Design bar

Editorial luxury, reference: [maisonabelane.com](https://maisonabelane.com). Not SaaS, not healthcare template.

## Hard constraints

1. Light mode only
2. Playfair 300 for H1/H2 (never bold, never 400+)
3. Pill CTAs only (`border-radius: 9999px`)
4. Eyebrows use `— ` em-dash prefix. That is the ONE place em-dashes are allowed.
5. Czech copy only
6. Real clinic photos only (`thumbs_dsc_*.jpg`, or `slide*.jpg` where slide ≠ `slide1.jpg`)
7. Keep `<meta name="robots" content="noindex">`, the demo HTML comment, and the Carto map
8. `prefers-reduced-motion: reduce` must kill all animation
9. Every interactive needs the tan double focus ring
10. Mobile is equal priority (test at 390×844)

## Deferred

- Real Google review quotes for testimonials band (currently dashed placeholders)
- Real form backend — contact modal is mailto fallback only

## Deploy

```bash
vercel --prod
```
