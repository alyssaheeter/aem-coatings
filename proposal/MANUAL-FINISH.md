# Manual finish — hand-back checklist (UI-only)

These steps can't be done through the available APIs and are left for Alyssa in the ClickUp
/ GitHub UI. Ordered by priority.

## A. GitHub Pages — DONE (verify only)
PRs #2 and #3 are merged to `main`, and Pages serves from **Settings → Pages → Deploy from a
branch → `main` / `(root)`**. The ClickUp Doc and the client email use the live Pages URLs:
- https://alyssaheeter.github.io/aem-coatings/concepts/a.html
- https://alyssaheeter.github.io/aem-coatings/concepts/b.html
- https://alyssaheeter.github.io/aem-coatings/concepts/c.html
- https://alyssaheeter.github.io/aem-coatings/concepts/pricing.html

## A2. Logo file — DONE
The official badge is committed at **`assets/aem-logo.jpg`** and referenced by every page; it
displays automatically on Pages. (Optional polish: a square / transparent-background version would
look cleaner on the light layouts — drop a replacement at the same path to swap it.)

## B. Turn the preview links into live embeds (ClickUp Doc)
The Doc currently shows clean **"▶ Open …" links** (client-ready as-is). To upgrade them to
**live inline previews**, the ClickUp API can't insert `/embed` blocks — do it in the UI:
1. On the **Design Concepts** page: click in, type **`/embed`**, paste a concept GitHub Pages URL,
   Enter. Repeat for A, B, C.
2. On the **Pricing Schedule** page: same with the `pricing.html` GitHub Pages URL (the quote builder).
3. If a URL shows only a **bookmark card**, leave the card **and** keep the labeled link beneath
   it. Confirm all four render before sending.

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
