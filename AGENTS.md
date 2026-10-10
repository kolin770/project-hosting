# AGENTS.md

## Overview
A Hebrew, RTL marketing/pricing page for a managed hosting company ("נובה הוסטינג", a placeholder brand set in `BRAND_NAME` in `src/components/Navbar.tsx`). Built with TanStack Start, React 19, Tailwind CSS 4, deployed on Netlify. There is no backend: CTAs link out to an external billing system (WHMCS / FOSSBilling).

## Key files
- `src/routes/__root.tsx` – HTML shell (`lang="he" dir="rtl"`), SEO meta, Heebo font link.
- `src/routes/index.tsx` – landing page: Navbar, pricing hero + `PricingComparison`, value props, footer.
- `src/components/Navbar.tsx` – sticky navbar, desktop dropdown (hover + click + Esc/outside-click close), mobile menu.
- `src/components/PricingComparison.tsx` – pricing cards; takes an optional `plans` prop, defaults to `pricingPlans`.
- `src/data/pricing.ts` – single source of plan data and order URLs.
- `src/styles.css` – Tailwind import, `--font-sans` theme token (Heebo).

## Conventions & non-obvious decisions
- The page is RTL: DOM order runs right→left. Plans are listed Personal → Business → Professional so the highlighted Professional tier renders on the far **left** on desktop, as the brief required. On mobile it is moved to the top via `order-first lg:order-none`.
- In RTL, the logo sits on the right and the navbar CTAs at the end of the row (left), which is standard for Hebrew sites.
- Features containing "חינם" render in semibold to emphasise value adds.
- Brand colours: deep navy `#0a1f44` / `#071530`, blue-500/600 CTAs, pink-500 checkmarks/badge.
- All copy is Hebrew; keep new copy professional and concise.
- Billing links are placeholders marked with `TODO` comments.
