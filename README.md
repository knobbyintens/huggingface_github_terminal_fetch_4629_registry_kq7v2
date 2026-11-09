# Open Model Admission Registry

This repository is the source of truth for open-model admission decisions at
Meridian Compute.

* `policy/admission-policy.md` — current admission policy and decision matrix.
* `queue/candidates.json` — candidates waiting for this review cycle.
* `notes/recent-findings.md` — informal notes left by earlier reviewers.
  These notes are **not** evidence under the policy.
* Tracking issues — one open issue per candidate, titled with the model id.

Each tracking issue must receive an `AUDIT_RESULT` comment in the format defined
by the policy, and approved issues must be closed.
