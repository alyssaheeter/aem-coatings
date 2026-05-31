# Task: "Approve & Select" — the approval gate

This is the **one interactive surface** the client touches. It lives in the `01 · Proposal`
folder. Andres is a comment-only guest here.

## Task description (client-facing)

> **Ready to move forward? This is the spot.**
>
> Two quick choices and we're off:
>
> **1. Pick your package** (details on the *Service Packages* page):
> - ☐ Foundation
> - ☐ Foundation + Reputation
> - ☐ Growth  ← *recommended*
> - ☐ Full Marketing Partner
>
> **2. Pick your design direction** (try them on the *Design Concepts* page):
> - ☐ Concept A — Heritage Trust
> - ☐ Concept B — Bold & Local
> - ☐ Concept C — Clean Service-First
>
> **3. Deposit** — once you've picked, I'll send the deposit details to start.
>
> Have a question or want a tweak before you decide? Just drop a comment here — no pressure.
>
> *This proposal is valid through June 30.*

## Configuration (custom fields, statuses)

> ⚠️ **The ClickUp MCP API cannot create custom fields or custom statuses** — these are set
> in the ClickUp UI. They're listed on the **manual-finish checklist**. Until then, the
> checkboxes in the description above act as the selection surface.

**Custom fields to add (UI):**
- `Selected Package` — dropdown: Foundation · Foundation + Reputation · Growth · Full Marketing Partner
- `Design Direction` — dropdown: A — Heritage Trust · B — Bold & Local · C — Clean Service-First
- `Deposit` — dropdown: Pending · Paid

**Statuses to configure (UI):**
- `In Review` → `Changes Requested` → `Approved`
