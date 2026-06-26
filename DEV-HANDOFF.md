# HumanSide of AI — Foundations · Landing Page (Course 1)

Conversion landing page for the **HumanSide of AI Foundations** public cohort, built for the LinkedIn/paid-ad launch.

- **Live client site (reference):** https://thehumansideof.us/humanside-of-ai
- **Course:** The HumanSide of AI™ · Foundations — 3 live sessions, 3 hours each
- **Price:** $1,500 per seat · 10% group enrollment discount · up to 5 seats per company · capped at 50
- **Format:** 3 live sessions · virtual or in-person · weekly/biweekly (~every 3 weeks) · tool-agnostic · pre/post-evaluation
- **Fall 2026 public cohorts:** Cohort 1 — Aug 13 / Aug 27 / Sep 10 · Cohort 2 — Oct 1 / Oct 15 / Oct 29
- **Founder / contact:** Katie Greenman — katie@thehumansideof.us · program inbox hello@thehumansideof.us

> **All page copy is now taken from the client's official sell sheets** (the 4 PDFs): real session names (Clarity / Control / Momentum), the five AI-fluency competencies, the six walk-away deliverables, the BCG 70% insight, cohort dates, and the $1,500 + 10% group discount.

> This is **Course 1 only**. Course 2 — "Leading with Purpose: Human Skills for the AI Era" (6 sessions, 4 hours each, cross-company cohort; per Slack $3,750/seat) — has its own sell sheet and can be produced by cloning this template. Its Fall 2026 cohorts: Cohort 1 Aug 20→Oct 29, Cohort 2 Sep 10→Nov 19.

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | Entire page markup + inline JS (sticky nav, smooth scroll, scroll-reveal). |
| `styles.css` | Design system + all section styling + responsive rules. |
| `assets/logo.png` | **Official HumanSide logo** (white script wordmark, pulled from the live Squarespace site). |
| `assets/favicon.ico` | **Official favicon** from the live site. |
| `assets/eiko-italic.ttf` | **PP Eiko Medium Italic** — the brand's accent font, used for italic `<em>` words in headings (loaded via `@font-face`). |
| `.claude/launch.json` | Local preview config (`npx serve` on port 4602). |

No build step. It's static HTML/CSS/JS — open `index.html` or serve the folder.

### Run locally
```bash
cd HumanSide-Landing-Page
npx -y serve -l 4602 .
# → http://localhost:4602
```

---

## ⚠️ Placeholders to wire before launch

### 1. Enrollment CTA (highest priority)
Every "Reserve your seat" button and the pricing card currently point to the in-page anchor **`#enroll`** (the pricing card). Once Habib provides the **Stripe checkout + GHL form/calendar embed**, do one of:

- **Quick swap:** find/replace `href="#enroll"` with the real checkout/form URL (add `target="_blank" rel="noopener"` for external links). There are CTAs in: the nav, hero (x1), pricing card, final CTA, plus `See what's inside` (this one correctly points to `#program` — leave it).
- **Embedded form:** drop the GHL embed into the `#enroll` pricing card section (`<section id="pricing">`), replacing the placeholder button.

Search `index.html` for `#enroll` to find every spot.

### 2. Client logos (trust bar)
The trust row now uses the **approved sell-sheet credibility set**: Google, Nike, WHOOP · 11 Brandon Hall awards · 12+ years. They're currently **styled text wordmarks** (class `.trust-logo`), not official logo images — swap for real logo art from Katie's shared asset folder if/when image usage is cleared.

### 3. Hero / visual assets
The hero is currently typographic on a brand-colored gradient (no photo). If the client wants the AI visual assets from Katie's shared folder, add them to `/assets` and place into the hero. Update `assets/og-image.png` (referenced in `<head>` for social sharing) — not yet created.

### 4. Testimonial
Uses the approved **Jesse Chamberlain (Manager, Google)** testimonial. Wording is a representative draft — confirm exact approved quote with Katie before launch.

---

## Brand notes (matched to thehumansideof.us)

The theme is pulled directly from the live Squarespace site so this page feels native to the brand.

- **Tone:** warm, practical, human-centered. Tagline "We make work work better."
- **Core ad messaging used:** "The driver's ed for AI" + "AI adoption is a leadership problem, not a technology problem" (one outcome: confident, human-centered AI fluency).
- **Type:** **Poppins** (headings + body, Google Fonts) with **PP Eiko Medium Italic** for italic `<em>` accent words in headings — exactly mirroring the brand site's `h1 em { font-family: 'EikoItalic' }` treatment.
- **Logo:** official white script wordmark (`assets/logo.png`). It's white art, so: in the light sticky nav it's rendered dark via `filter: invert(1) brightness(0.12)`; on the dark footer it's used as-is.
- **Palette (CSS vars in `:root`), taken from the site's theme tokens:**
  - Blue `#1059e5` — primary brand accent (program section, price, links)
  - Cyan `#00b8c9` / aqua `#80dee4` / light-blue `#b4dafd` — secondary accents
  - Orange `#fa6a3a` — pop / primary CTA color
  - Cream `#faf6ee` background, navy `#0c1838` for dark sections (about + footer)
- **Shape language:** large rounded corners (cards 28–34px, pill buttons) + subtle hover lift/scale, matching the site's playful, friendly feel.

## Compliance guardrails honored (per Slack brief)
- ❌ No tax-credit percentages mentioned (pending CPA approval).
- ❌ AI Fluency Assessment is **not** used as a CTA.
- ✅ Approved pricing only ($1,500/seat for Foundations).
- ✅ Warm, human-centered tone; avoids generic AI/tech hype; one focused outcome.

## Accessibility / quality
- Responsive at desktop / tablet (≤940px) / mobile (≤760px, ≤460px).
- `prefers-reduced-motion` disables all animations.
- Semantic landmarks, alt-ready structure, keyboard-focusable CTAs.
- Verified: no console errors; renders cleanly at 1280 / 800 / 390 widths.
