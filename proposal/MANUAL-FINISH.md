# Manual finish — hand-back checklist (UI-only)

These steps can't be done through the available APIs and are left for Alyssa in the ClickUp
/ GitHub UI. Ordered by priority.

## A. Make the design concepts go live (GitHub Pages)
The concept files are committed to the repo, but **GitHub Pages must be enabled by hand** —
there's no API tool for it in this environment.

1. Go to **GitHub → `alyssaheeter/aem-coatings` → Settings → Pages**.
2. Under **Build and deployment**, Source = **Deploy from a branch**; Branch = **`main`**,
   folder = **`/ (root)`**; Save. (Merge PR #1 to `main` first, or pick the feature branch.)
3. Wait ~1 min, then confirm these return 200 and render:
   - https://alyssaheeter.github.io/aem-coatings/concepts/a.html
   - https://alyssaheeter.github.io/aem-coatings/concepts/b.html
   - https://alyssaheeter.github.io/aem-coatings/concepts/c.html
   *(Instant fallback that needs no Pages setup, already framable:
   `https://raw.githack.com/alyssaheeter/aem-coatings/main/concepts/a.html`, etc.)*

> Note: this sandbox could only reach `raw.githubusercontent.com` (files confirmed live
> there), so I could not enable Pages or screenshot the rendered pages from here.

## B. Turn the concept links into live embeds (ClickUp Doc)
On the **Design Concepts** page of the `AEM Proposal` Doc:
1. Click into the page, type **`/embed`**, paste a concept URL, Enter. Repeat for A, B, C.
2. If a URL shows only a **bookmark card**, leave the card **and** keep the labeled text
   link beneath it (already in the page) as a fallback.
3. Confirm all three render before sending.

## C. Gate-task custom fields + statuses (ClickUp UI)
On the **Approve & Select** task / its list (the API can't create these):
1. Add custom fields:
   - `Selected Package` — dropdown: Foundation · Foundation + Reputation · Growth · Full Marketing Partner
   - `Design Direction` — dropdown: A — Heritage Trust · B — Bold & Local · C — Clean Service-First
   - `Deposit` — dropdown: Pending · Paid
2. Configure statuses on the list: `In Review` → `Changes Requested` → `Approved`.

## D. Automation rule (ClickUp Automations UI)
On the `Approve & Select` task: **when status = `Approved`** →
- notify Alyssa, **and**
- create a kickoff task in the `02 · Delivery` folder.

## E. Guest invite — STAGED, do not send yet
- Add **Andres Bedolla** (`andres.bedolla@aemsurfacecare.com`) as a **Guest**,
  **comment-only**, scoped to **`01 · Proposal` only** (never the other spaces/folders).
- **Leave it staged.** Send when you're ready.

## F. (Optional) Rename the Space
The build reused your existing empty **"AEM"** space (the API has no create/rename-space
call). If you want it titled **"AEM Coatings & Carpet Care,"** rename it in the UI:
Space → ⋯ → Rename.
