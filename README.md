# Email Developer Portfolio — Brittany Nation

Five hand-coded, responsive HTML email templates. No frameworks, no JavaScript — just tables, inline CSS, and email-client wrangling.

**Live demo:** https://brittanynation.github.io/email-dev-portfolio/

## Templates

| Template | What it shows |
|---|---|
| [Welcome](welcome/) | Bulletproof CTA button (VML for Outlook), dashed promo-code block, 3-column perks that stack on mobile |
| [Newsletter](newsletter/) | Featured story + 2-column card layout, fluid images, editorial masthead |
| [Promo](promo/) | Announcement bar, 3-column product grid with sale pricing, promo code block |
| [Order confirmation](order-confirmation/) | Transactional order-summary table, numbered shipping timeline |
| [Win-back](win-back/) | Re-engagement tone, comeback offer, preference-center nudge |

## Techniques used in every template

- **Table-based layout** with `role="presentation"` — divs and flexbox are unreliable in email clients
- **Fully inline CSS** — Gmail and others strip or ignore `<style>` blocks, so critical styling lives on the elements
- **Bulletproof buttons** — VML (`v:roundrect`) inside `<!--[if mso]>` conditionals so buttons render in Outlook, real `<a>` buttons everywhere else
- **Hybrid responsive design** — fluid tables (`width:100%; max-width:600px`) plus media queries that stack columns under 620px
- **Outlook conditionals** — fixed-width wrapper tables for desktop Outlook (Word rendering engine)
- **Dark-mode support** — `prefers-color-scheme` overrides for Apple Mail / iOS
- **Hidden preheader text** — the preview snippet you see in the inbox list
- **Accessible contrast + alt text** on every image and CTA

## Why no JavaScript?

Email clients strip `<script>` entirely. Email development is a pure HTML-and-CSS discipline — which is exactly what makes it a great fit for designers who think visually.
