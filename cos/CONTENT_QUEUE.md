# Content Queue

**Last updated:** 2026-04-19 (cross-referenced against current OBEY repo state)

## Source-of-truth check

Repo state inspected: initial architecture snapshot is committed; the COS role migration documents (`COS_MIGRATION_BRIEF.md`, `COS_BOOTSTRAP_PROMPT.md`, `INTERACTION_MODEL.md`) and the `cos/` operating-state files are part of the working set this week. Refresh the live status before relying on commit-level claims.

Concrete artifacts available as proof material:

- `ARCHITECTURE.md` — V1 product wedge, layer model, `.obey/` runtime state schema, V1 flow
- `WEDGE_WHATSAPP_PUBLISHING.md` — 7-stage pipeline, example UX, scope boundaries
- `DISTRIBUTION.md` — 5-level obedience ladder, minimum viable content engine spec
- `COS_MODEL.md` — 5-layer hybrid system (policy / state / templates / connectors / triggers)
- `COS_MIGRATION_BRIEF.md` — today's role rewiring (Frank leads / Codex builds / COS supports)
- `INTERACTION_MODEL.md` — versioning steward boundary
- `cos/*.md` — first concrete implementation of structured COS state

---

## Ready to draft (lastro real existe)

- **Raw AI vs OBEY-mediated execution**
  - source: `ARCHITECTURE.md` §1-2 (thesis + problem statement) and `DISTRIBUTION.md` §4 (obedience ladder)
  - hook: "Memory without behavioral control is not enough."
  - format: short post or SGOPS note

- **Why memory alone is not enough**
  - source: `ARCHITECTURE.md` §1 ("Core thesis") + `DISTRIBUTION.md` §4 levels 1-3
  - format: SGOPS teardown
  - angle: distinguish memory from decisions, approvals, contracts

- **The WhatsApp → approval → Instagram wedge**
  - source: `WEDGE_WHATSAPP_PUBLISHING.md` §3 (example UX) + §5 (technical shape)
  - format: short post + diagram-style explainer
  - constraint: it is still a spec, not a running demo. Frame as "how the wedge is shaped" not "demo of running system"

- **The 5-level obedience ladder** [NEW — added by COS]
  - source: `DISTRIBUTION.md` §4 in full
  - format: SGOPS note with visual ladder
  - hook: most agent failures are not intelligence failures; they are workflow-level failures at level 2 or 3

- **Ecosystem map: OBEY / COS / SGOPS** [NEW — added by COS]
  - source: `ARCHITECTURE.md` §4 + `README.md` brand architecture
  - format: short post explaining the three roles
  - hook: public wedge, internal engine, lab — three different surfaces, one system

## Draft in progress

- **Why COS is internal and still valuable**
  - source: `COS_MODEL.md` §1, §11, §13 + `README.md` "Internal does not mean useless"
  - status: angle is clear but no draft body written yet
  - constraint: must avoid "agency theater" framing — emphasize bounded loops, structured state, gated proactivity

## Needs proof (waiting on real artifacts)

- **before/after comparison of agent behavior with and without OBEY**
  - blocker: requires Milestone 1 implementation; no executable wedge exists yet
  - what unblocks: the runnable local loop described in `ROADMAP.md` Milestone 1
  - until then: do not promise this artifact

- **one concrete founder workflow compressed by COS**
  - partial proof exists: today's COS migration itself (3 files updated, role boundary clarified) is a real founder workflow that COS structured
  - what unblocks: package today's session into a short narrative artifact

## Approved to publish

- none yet (Frank approval gate)

---

## Backlog (capture only, not for this week)

- comparison: OBEY vs LangGraph / Letta / Mem0 framing
- founder note: why COS is proactive but not sovereign
- visual: command → context → approval → execution as a single graphic

## Rule

Every content item should satisfy at least one of:

- proves the wedge
- builds authority
- links product work to public proof

Items in this queue without `source:` references are not yet groundable and should move to backlog or be killed.
