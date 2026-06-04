# assets/

Brand assets for the AEM proposal bundle.

## aem-logo.png  ← add this file

Drop the official AEM circular badge here, named exactly **`aem-logo.png`**.

Every page (`index.html`, `concepts/a.html`, `b.html`, `c.html`, `pricing.html`) already
references `assets/aem-logo.png` and will show it automatically once it's committed. Until
then, each page falls back to its placeholder mark — nothing breaks.

**Tips**
- A **square** image looks best (it's cropped to a circle in the headers).
- A **transparent-background** PNG (just the badge, no maroon square) looks cleanest on the
  light layouts (Concept C, the pricing page, the gallery). The full maroon-background version
  works fine too — it reads as a medallion.
- After committing it to `main`, GitHub Pages redeploys automatically; hard-refresh to see it.
