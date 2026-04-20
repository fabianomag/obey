# OBEY Proof Update — Architecture Lock and COS Role Boundary

**By Fabiano Frank · OBEY**
**Date:** 2026-04-19
**Status:** draft — not approved, not published
**Source documents:** `OBEY/COS_MIGRATION_BRIEF.md`, `OBEY/COS_BOOTSTRAP_PROMPT.md`, `OBEY/INTERACTION_MODEL.md`, `OBEY/cos/CURRENT_PRIORITY.md`
**Length target:** 200–300 words

---

This week the OBEY repo went through a small but load-bearing change. Architecture v0 was frozen, and the COS role was given a clean boundary.

Three decisions:

- Architecture v0 is locked. Layer model, V1 wedge, `.obey/` runtime state schema, and the phased roadmap are now the working baseline instead of being re-derived every session.
- COS is scoped to an internal proactive operating layer. Not the CEO. Not the product. Not a fully autonomous employee. Its job is continuity, packaging, and bounded support inside the current priority — Marketing Operations as primary mode, Product Operations as secondary.
- Codex is named as the versioning and publication steward for the repo ecosystem in this phase. COS may surface release candidates and version-worthy changes; it does not take git actions on its own.

Why it matters: the previous failure mode was COS slowly drifting into "founder replacement" framing — issuing daily orders, claiming strategic ownership, expanding scope without authorization. That mode burned founder energy without producing proof. Closing the boundary lets each layer do what it is actually good at. Frank leads. Codex builds. COS supports.

What ships next: Milestone 1 — the executable wedge skeleton (`command → context → approval → execution`) running locally, with mock publishing. That is the first real demo target, and the first opportunity to convert the obedience-ladder framework from a written model into observable behavior change.

No public demo yet. No benchmark yet. This week's deliverable is the role contract that makes the demo possible.

---

**Internal note (not for publication):** Treat this as an internal proof artifact. The migration documents are real and they describe a correction inside our own operating model. They are not, on their own, evidence that OBEY makes external agents behave better. That evidence comes from Milestone 1 onward.
