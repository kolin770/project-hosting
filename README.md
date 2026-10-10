# נובה הוסטינג – Pricing & Navigation

A premium, Hebrew (RTL) landing page for a managed hosting and IT services company. It features a three-tier "WooCommerce Super" pricing comparison and a sticky top navigation bar, designed to feel modern and trustworthy compared to legacy hosting sites.

## Key technologies

- React 19 + TanStack Start (file-based routing, SSR)
- Tailwind CSS 4 for all styling
- lucide-react icons
- Heebo font (Google Fonts)
- Deployed on Netlify

## Components

- `src/components/PricingComparison.tsx` – `PricingComparison`, maps over the plan array and renders the three cards. The Premium (annual) tier is scaled up, set on a deep-blue background, and carries the "המשתלם ביותר" tag. On mobile it stacks first.
- `src/components/Navbar.tsx` – `Navbar`, a sticky header with a hosting dropdown (WordPress, WooCommerce, VPS, managed cloud), a collapsible mobile menu, and "אזור לקוחות" / "פתיחת פניה" CTAs.
- `src/data/pricing.ts` – plan data (titles, prices, features, order links).

## Connecting the billing system

Every CTA is a conversion point. Replace the placeholder links marked `TODO` with your WHMCS / FOSSBilling URLs:

- Plan order links: `orderUrl` on each plan in `src/data/pricing.ts`
- Client area and ticket links: `CLIENT_PORTAL_URL` and `OPEN_TICKET_URL` in `src/components/Navbar.tsx`

## Running locally

```bash
pnpm install
netlify dev   # or: pnpm dev
```
