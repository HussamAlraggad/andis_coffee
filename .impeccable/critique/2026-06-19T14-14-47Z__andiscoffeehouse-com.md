---
target: "https://andiscoffeehouse.com"
total_score: 26
p0_count: 0
p1_count: 1
p2_count: 3
p3_count: 2
timestamp: 2026-06-19T14-14-47Z
slug: andiscoffeehouse-com
---
## Design Health Score (Corrected)

| # | Heuristic | Score | Key Issue |
|---|-----------|-------|-----------|
| 1 | Visibility of System Status | 3 | No loading states on interactive tab switches |
| 2 | Match System / Real World | 4 | Excellent bilingual, natural terminology |
| 3 | User Control and Freedom | 2 | "Back to map" button has low visibility on Explore — users may feel trapped |
| 4 | Consistency and Standards | 3 | Menu tab names don't match section headers (Coffee & Tea vs Espresso Bar) |
| 5 | Error Prevention | 2 | Feedback form has no visible validation or confirmation |
| 6 | Recognition Rather Than Recall | 3 | Prices visible, but nav links could be more prominent for first-timers |
| 7 | Flexibility and Efficiency of Use | 2 | No search/filter among 50+ menu items |
| 8 | Aesthetic and Minimalist Design | 3 | Clean overall; minor polish items |
| 9 | Error Recovery | 1 | No fallback if SPA crashes on slow network |
| 10 | Help and Documentation | 3 | Cafe hours are culturally understood — not a real gap |
| **Total** | | **26/40** | **Acceptable → Good** |

## Corrected Priority Issues

### [P1] SPA has no fallback for JS-disabled or crashed state
If JavaScript fails on Jordanian 3G, users see a blank white page. Fix: hero + key content SSR, or meaningful error/loading shell.

### [P2] "Back to map" button too subtle on Explore
The button exists but has low visual prominence. Users don't spot it easily. Fix: increase contrast/size, add a closing gesture.

### [P2] Menu tab vs section naming mismatch
Category tabs say "Coffee & Tea" but sections inside are labeled Espresso Bar, Sweet Latte Signatures, Frappe Blends, etc. Inconsistent naming creates confusion.

### [P2] No SEO-reachable content for crawlers
React SPA with no SSR means Google can't read menu/visit pages. "Cafe near University of Jordan" is a high-intent search you're missing.

### [P3] Nav links lack prominence on mobile
First-time visitors may not spot the nav links quickly enough. Fix: increase tap target size, add visual weight (underline, bg, or icon).

### [P3] Feedback form has no success state
No confirmation after submission. Users don't know if their message went through.
