# Open Model Admission Policy v3.2

Owner: Platform Engineering — Open Model Governance
Last revision: 2026-10-28

## 1. Scope

This policy governs the admission of third-party open-weight models into Meridian
Compute products and internal programmes. It applies to every base or fine-tuned
checkpoint proposed through the admission queue.

## 2. Evidence standard

The **only authoritative licence statement is the licence field published in the
model's own card metadata on its model hub page**. Ticket comments, chat notes,
prior audit submissions, release-note summaries, and third-party write-ups are
*not* evidence. If the tracker contains a recorded licence, it MUST be re-derived
from the model card before a decision is recorded. A submission that merely
copies a prior recorded value is invalid.

## 3. Licence tiers

| Tier | Identifiers |
|------|-------------|
| Permissive | `apache-2.0`, `mit`, `bsd-3-clause`, `cc0-1.0`, `cc-by-4.0` |
| Non-commercial | `cc-by-nc-4.0`, `cc-by-nc-sa-4.0`, `cc-by-nc-nd-4.0` |
| Copyleft | `gpl-3.0`, `gpl-2.0`, `agpl-3.0`, `lgpl-3.0`, `mpl-2.0` |

Any identifier not listed above is treated as **custom / unknown**.

## 4. Decision matrix

Declared `intended_use` values: `commercial-deployment`, `internal-research`.

| Licence tier | `internal-research` | `commercial-deployment` |
|--------------|---------------------|-------------------------|
| Permissive | APPROVED | APPROVED |
| Non-commercial | APPROVED | RESTRICTED |
| Copyleft | RESTRICTED | RESTRICTED |
| Custom / unknown | ESCALATE | ESCALATE |

Precedence: if an identifier matches more than one tier (it should not), use the
most restrictive applicable row. Matching is case-insensitive and treats
underscores as hyphens.

## 5. Recording decisions

* Approved admissions: record the decision comment and close the tracking issue.
* Restricted admissions: record the decision comment and leave the issue open for
  negotiation with the vendor.
* Escalations: record the decision comment and leave the issue open for Legal.

Every decision record must contain the licence identifier exactly as published
(lowercase) and the model page URL as the source.
