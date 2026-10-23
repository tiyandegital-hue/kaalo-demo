# KAALO — Coffee Roasters (DEMO CONCEPT) · DESIGN.md

## Psychology brief (workflow step 2)
- Visitor: Dhaka home-brewer / small café buyer, burned before by stale "fresh" beans with no roast date.
- Pain: freshness is claimed everywhere, proven nowhere.
- One action: order this week's roast on WhatsApp.
- Trust gap: closed by radical date transparency — the roast log IS the page; every bag hand-stamped.
- Emotion: craft, ritual, honesty. Peak = the freshness verdict. End = the giant name + one order line.

## Inventory (subject-only facts the idea is built from)
1. Roasts Thursdays only, 12 kg drum, small batches · 2. Single-lot Bandarban arabica + one house blend · 3. Best window: 7–21 days post-roast · 4. Usually sold out by Sunday · 5. Every bag hand-stamped with roast date · 6. Dhaka delivery 24h, cash on delivery · 7. Roastery pickup only (Banani), no café · 8. Ground to order: whole / espresso / filter.
**Idea: "The roast log is the page."** Competitor test: a stale-bean seller could never publish this page — the log would expose them.

## Tokens
```yaml
canvas: "#F5F4F0"   # warm stone paper
ink: "#16130E"
body: "#3E3A31"
muted: "#6E685B"
hairline: "rgba(22,19,14,.16)"
surface-1: "#FFFFFF"
surface-2: "#ECEAE2"
voltage: "#17633B"  # roast green — ALL calls to action, <5% of any screen
voltage-ink: "#0E4527"
radius-ceiling: 2px  # logbook character: near-square, deliberate
spacing: 4px base; section gap 96px desktop / 64px phone
```

## Typography
- Display + body: **Fraunces** (serif = craft/heritage). Headline 64px desktop / 40px phone, ≤2 lines, tracking -0.01em.
- Data/stamps/labels: **IBM Plex Mono** (precision = the log). 12–13px, uppercase, letterspaced.
- Max 2 typefaces + mono as the data voice (mono here IS the second face's job).

## Layout
- Margins: 28px desktop, 18px phone, EQUAL both sides. One anchor line: content starts at margin; hero text block and section heads share it.
- No two neighbouring sections share a layout: hero split → checker band (surface) → log rows → price lines → giant-name ending.
- Depth: hairlines + surface ladder only. No shadows. No gradients. No icon cards.
- Pages (multipage — Tanjir standing rule 2026-10-23: never one-page): index.html (home: hero + teasers + ending scene) · roast-log.html (full log + photo strip) · freshness.html (the live checker + the three states) · prices.html (full prices + how ordering works). Shared style.css; nav identical on every page with the current page underlined in voltage.
- Ending is a designed scene: KAALO at full width, then one order line + credits.

## Components
- Nav: wordmark / 3 text links / 1 voltage action. No bar background.
- Freshness checker (the one live thing): date input → days-since-roast → verdict vs the real 7–21 day window (Too fresh / In the window / Past peak). All states: empty, valid, future-date error.
- Roast log: hairline rows — date · lot · process · note · status stamp.
- Prices: dotted-leader lines (the idea survives into pricing), grind options as one mono line.

## Motion
- CSS only: mask-reveal headline lines (stagger 120ms), fade-up blocks. Transform/opacity only. `prefers-reduced-motion` = everything static. No JS animation libraries (budget: 0 timelines).

## Imagery
- ≥4 real photographs from Openverse (CC-licensed), downloaded locally, credits recorded in `credits.json` and printed in the footer. No hotlinking, no stock-people endorsing.

## Do's and Don'ts
- DO print real dates, real prices, the sold-out truth. DON'T invent reviews, ratings, or "best coffee in Dhaka" claims.
- DO keep voltage under 5% of any screen. DON'T add a second accent.
- DON'T use icon cards, pill badges, eyebrow labels with numbers, or a link-column footer.

## Known Gaps
- Demo concept: business facts are illustrative, not a real client's (labeled on-page).
- WhatsApp order link is a placeholder number format, not wired to a real account.
- No checkout — by design; the real business takes COD orders by message.
