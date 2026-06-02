# Manual finish — hand-back checklist (UI-only)

These steps can't be done through the available APIs and are left for Alyssa in the ClickUp
/ GitHub UI. Ordered by priority.

## A. Merge + make the assets go live (GitHub)
The repo work is on branch `claude/aem-coatings-proposal-geXK6` (**draft PR #2**). The
ClickUp Doc embeds **githack** URLs pinned to `main`, so they resolve once the PR is merged.

1. Review & **merge PR #2 → `main`**: https://github.com/alyssaheeter/aem-coatings/pull/2
2. Enable Pages (a deploy workflow is already committed): **Settings → Pages →
   Build and deployment → Source = `GitHub Actions`**. Every push to `main` then redeploys.
   - Canonical URLs: `https://alyssaheeter.github.io/aem-coatings/concepts/{a,b,c,pricing}.html`
3. Confirm these githack URLs return 200 + render (used by the Doc — work without Pages):
   - https://raw.githack.com/alyssaheeter/aem-coatings/main/concepts/a.html
   - https://raw.githack.com/alyssaheeter/aem-coatings/main/concepts/b.html
   - https://raw.githack.com/alyssaheeter/aem-coatings/main/concepts/c.html
   - https://raw.githack.com/alyssaheeter/aem-coatings/main/concepts/pricing.html

> Note: WebFetch to external hosts was blocked in this build environment, so URL liveness /
> rendering could not be verified from here — please eyeball the 4 links above after merge.

## B. Turn the preview links into live embeds (ClickUp Doc)
The Doc currently shows clean **"▶ Open …" links** (client-ready as-is). To upgrade them to
**live inline previews**, the ClickUp API can't insert `/embed` blocks — do it in the UI:
1. On the **Design Concepts** page: click in, type **`/embed`**, paste a concept githack URL,
   Enter. Repeat for A, B, C.
2. On the **Pricing Schedule** page: same with the `pricing.html` githack URL (the quote builder).
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
