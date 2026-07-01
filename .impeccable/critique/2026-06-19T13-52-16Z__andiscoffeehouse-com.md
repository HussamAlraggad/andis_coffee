---
target: "https://andiscoffeehouse.com"
total_score: 23
p0_count: 0
p1_count: 2
p2_count: 3
timestamp: 2026-06-19T13-52-16Z
slug: andiscoffeehouse-com
---
## Design Health Score

| # | Heuristic | Score | Key Issue |
|---|-----------|-------|-----------|
| 1 | Visibility of System Status | 3 | No loading states on interactive tab switches |
| 2 | Match System / Real World | 4 | Excellent bilingual, natural terminology |
| 3 | User Control and Freedom | 2 | No back/undo on the interactive "Explore" map; trapped once a hotspot is clicked |
| 4 | Consistency and Standards | 3 | Tab-based menu is clean but category names don't match section headers |
| 5 | Error Prevention | 2 | No form validation visible on feedback form, no confirmation on submission |
| 6 | Recognition Rather Than Recall | 3 | Menu items listed but prices not visible without tapping each item |
| 7 | Flexibility and Efficiency of Use | 1 | No search, no filter, no favorites |
| 8 | Aesthetic and Minimalist Design | 3 | Clean overall but the repeating ✦ marquee is visual noise |
| 9 | Error Recovery | 1 | No way to recover if the SPA crashes — one big `#root` div with no fallback |
| 10 | Help and Documentation | 1 | No contact info sheet, no FAQ, no "how to order" guide |
| **Total** | | **23/40** | **Acceptable** |

## Anti-Patterns Verdict

Does NOT look AI-generated overall. Intentional design with brand green `#4C5A3E`, split hero, interactive explore map, multi-tab menu. However: repeating ✦ marquee is an AI-favored filler device, numbered section markers (01/02/03) hit the eyebrow ban, and the callout cards in Explore are a hero-metric variant.

## What's Working

1. **Bilingual execution is excellent.** Full RTL layout, native Arabic fonts (Alexandria), translated nav labels — rare and well done.
2. **Interactive "Explore" map** is a genuine differentiator — tapping hotspots to preview seating areas tells the space story better than static images.
3. **Full menu with prices live.** Most cafes in Amman don't have this. React SPA with every item and price is ahead of competitors.

## Priority Issues

### [P1] Menu prices hidden behind taps
Menu items show only name + image. Price is invisible until tap/click. Users scan menus by price first; hiding prices behind 50+ taps creates cognitive load. Fix: show prices on the card face, reserve expanded view for descriptions.

### [P1] SPA has no fallback for JS-disabled or crashed state
Entire page is `<div id="root"></div>`. If JS fails on Jordanian 3G, users see blank white. Noscript shows text but not menu data. Fix: SSR hero + key menu items, or meaningful loading/error state.

### [P2] Explore interactive map traps users
Once a hotspot is tapped, no obvious "back" or "close" gesture. View changes with no way to return to full map. Fix: add prominent "Back to map" or swipe-to-dismiss.

### [P2] No SEO-reachable content
React SPA with no SSR. Google sees a blank shell for menu/visit pages. "Cafe near University of Jordan" is a high-intent query. Fix: add SSR or pre-render key pages for crawlers.

### [P2] Menu tab vs section naming mismatch
Category tabs say "Coffee & Tea", "Cold & Refreshing", "Bakery & Bites" but section headers say Espresso Bar, Sweet Latte Signatures, Frappe Blends, etc. Inconsistent naming confuses users.

### [P3] Repetitive ✦ marquee
Two rows of "Andi's Coffee ✦ The Art of Coffee ✦ 100% Arabica..." scrolling in opposite directions. Visual noise with no info value. Fix: one row, slower, or static brand statement.

### [P3] Feedback form has no success state
No confirmation after submission. Users don't know if message sent. Fix: show success toast or inline confirmation.

## Persona Red Flags

- **Jordan (First-Timer):** Beautiful hero but has to tap each menu item to see prices — gives up after 3.
- **Casey (Mobile):** Hero image takes 60% of viewport on mobile; must scroll past it to reach menu. Menu tabs are deep in the page. No thumb-zone CTA.
- **Sam (Accessible):** Explore map hotspots are small div targets without clear focus indicators. Prices gated behind interaction means screen readers may miss them. ✦ marquee has no `prefers-reduced-motion` respect.
