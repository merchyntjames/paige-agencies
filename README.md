# Paige for Agencies — Landing Pages

Value-prop landing pages for the **May 2026 — Paige Trial Value Prop Campaign (Agencies)** Facebook campaign. One landing page per ad angle.

**Primary domain:** [paigeforagencies.com](https://paigeforagencies.com)
**Defensive domain (also owned, not in use):** hirepaige.com
**Vercel fallback URL:** paige-agencies.vercel.app

## Live pages

| Angle | URL | Status |
|---|---|---|
| AI Visibility | https://paigeforagencies.com/ai-visibility | ✅ Built |
| Save Time | https://paigeforagencies.com/save-time | ✅ Built |
| Boost Margins | https://paigeforagencies.com/boost-margins | ✅ Built |

## Stack

- Static HTML
- Tailwind CSS via CDN (no build step)
- DM Sans via Google Fonts
- Hosted on Vercel
- Vercel Analytics (auto page views)

## Brand tokens (Paige palette — blue/teal-led)

```js
{
  navy:    '#0f007d',
  blue:    '#0063fd',  // PRIMARY — CTAs
  skyblue: '#31A8FF',
  aqua:    '#5CE5DC',
  pink:    '#dd0cf7',  // demoted — secondary accent only
  purple:  '#8b00cc',
  green:   '#05c168',
  orange:  '#ff9e2c',
  dark:    '#1c1f23',
}
```

## Conventions

- Each angle = one HTML file at the repo root, served via Vercel `cleanUrls`
- Primary CTA: `Start FREE TRIAL` → `https://app.localmarketingmanager.com/?agency=true`
- All CTAs use `class="cta-link"` so a small JS snippet auto-forwards UTM params from the LP URL → trial flow URL
- All pages have `noindex, nofollow` (paid traffic only — should not compete with merchynt.com in organic search)
- Hero is 2-column 50/50 (copy left, video placeholder right) — *deliberate departure from the centered single-column pattern of the GBP audit pages*

## Adding a new angle

1. Copy `ai-visibility.html` → `<new-angle>.html`
2. Update H1, problem section, value-prop deep dive, FAQ angle-specific item, final CTA H2
3. Keep all other sections identical (shared design system)
4. Add to README table above

## Local preview

```bash
# Any static server works
python3 -m http.server 8000
# then open http://localhost:8000/ai-visibility.html
```

## Deploy

Vercel auto-deploys on push to `main`.
