# AEM Coatings & Carpet Care — Website Concepts + Pricing Demo

Static, hosted assets for the **AEM Coatings and Carpet Care LLC** (Northwest Indiana)
website + marketing proposal, prepared by **Alyssa Heeter Consulting**. These pages are
previewed live and embedded inside the client proposal (a ClickUp Doc).

## What's here

| Path | What it is |
|---|---|
| `index.html` | Landing hub linking the three concepts |
| `concepts/a.html` | **Concept A — Heritage Trust** (badge-forward, warm/editorial, credibility-first) |
| `concepts/b.html` | **Concept B — Bold & Local** (high-contrast, NW-Indiana pride, conversion-punchy) |
| `concepts/c.html` | **Concept C — Clean Service-First** (minimal, dual-service split, instant-quote) |
| `concepts/pricing.html` | **Interactive quote builder** — pick a package + add-ons, live total, copyable JSON summary |
| `content/aem.json` | **Single source of truth** — business facts, brand palette, the 4 tiers + pricing, add-ons, concept captions |
| `proposal/` | Staged ClickUp proposal copy (one markdown file per Doc page) + ID map + manual-finish checklist |
| `assets/aem-logo.png` | Official AEM badge, shown on every page (see `assets/README.md`) |

## Runbook — editing & redeploying (no dev required)

### 1. Edit copy or prices
Open **`content/aem.json`** and edit in place. It drives:
- the **pricing demo** (`concepts/pricing.html`) — tiers, monthly figures, add-ons, valid-through date;
- the **proposal** copy reference (business facts, concept captions, brand hex).

Every dollar figure is a benchmarked **recommendation** flagged `"fillin": true` / `[FILL-IN]`
until Alyssa confirms. Keep the JSON valid (commas, quotes) — paste it into any JSON validator
if unsure.

> The three concept pages (`a/b/c.html`) are intentionally **self-contained** for fast, dependency-free
> previewing. `aem.json` is the canonical content source; when concept copy changes, update both the
> JSON and the concept file. `pricing.html` reads `aem.json` at runtime (with an inline fallback copy
> so it still works if the file can't be fetched).

### 2. Redeploy GitHub Pages
Pages is served from **Settings → Pages → Deploy from a branch → `main` / `(root)`**. Just
commit + push to `main` and it redeploys automatically (a minute or two — hard-refresh to see it).
Live URLs: `https://alyssaheeter.github.io/aem-coatings/concepts/<file>`

### 3. Live preview URLs used in the proposal
The ClickUp Doc embeds the live GitHub Pages URLs:
- `https://alyssaheeter.github.io/aem-coatings/concepts/a.html`
- `https://alyssaheeter.github.io/aem-coatings/concepts/b.html`
- `https://alyssaheeter.github.io/aem-coatings/concepts/c.html`
- `https://alyssaheeter.github.io/aem-coatings/concepts/pricing.html`

### 4. Re-embed in ClickUp
In a Doc page, type `/embed` and paste the URL above to turn a link into a live inline preview.
Do this for all four (A, B, C, pricing). If one renders only as a bookmark card, keep the card
**and** the labeled link beneath it.

## Notes
- All copy and images are **realistic placeholders for layout review** — not verified marketing claims.
  Items needing client input are marked `[FILL-IN: …]` or `[CAPTURE: …]`.
- Brand colors are **sampled from the official AEM circular badge** (oxblood `#6E2526`,
  gold `#BD9A4C`, espresso `#2E2018`, taupe `#BBA88C`, brick `#8A3A2E`, cream `#EFE5CE`).
- The real badge loads from **`assets/aem-logo.png`** on every page (with a placeholder
  fallback until that file is committed — see `assets/README.md`).
- The coating product **Ekopel is confirmed**, but its warranty/lifespan/durability claims require
  manufacturer-spec verification before going on the live site.
- Real business details used: AEM Coatings and Carpet Care LLC · Owner Andres Bedolla ·
  219-255-0949 · andres.bedolla@aemsurfacecare.com · Est. 2024 · "For a Fresh Start."
- Self-contained HTML + CSS, mobile-responsive, no external dependencies.
