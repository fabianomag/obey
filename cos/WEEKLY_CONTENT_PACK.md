# Weekly Content Pack

**Week of:** 2026-04-19
**Status:** draft (pending Frank approval)

## Theme

How to make AI obey inside a real workflow.

## Source material (real, in repo)

- `COS_MIGRATION_BRIEF.md` — today's role rewiring (Frank leads / Codex builds / COS supports)
- `ARCHITECTURE.md` — V1 product wedge, layer model, `.obey/` runtime state schema
- `WEDGE_WHATSAPP_PUBLISHING.md` — 7-stage pipeline + example UX
- `DISTRIBUTION.md` — 5-level obedience ladder + minimum viable content engine
- `COS_MODEL.md` — 5-layer hybrid system

Repo state: initial architecture snapshot is committed; the COS role migration is in flight in the working set (covering `COS_MIGRATION_BRIEF.md`, `COS_BOOTSTRAP_PROMPT.md`, `INTERACTION_MODEL.md`, and the `cos/` operating-state files). This week's pack is grounded in those documents and the v0 architecture docs. Refresh git state before quoting commit-level facts.

---

## Deliverables

### 1 SGOPS note — "The Obedience Ladder"

- **Working title:** Five levels of agent obedience (and why most agents are stuck at level 2)
- **Source:** `DISTRIBUTION.md` §4 in full + `ARCHITECTURE.md` §1-2
- **Spine:**
  1. People assume agent failures are intelligence failures. They are usually obedience failures.
  2. Five levels: draft / context / workflow / platform / full external autonomy.
  3. Most "AI is amazing" demos prove level 1. Most production pain is at levels 2-3.
  4. OBEY is designed to make levels 2-3 reliable before promising level 5.
- **Length:** medium (≈ 600-900 words)
- **Status:** draft body not written; outline only

### 1 OBEY proof update — "Architecture lock + COS role boundary (week of 2026-04-19)"

- **Source:** the COS role migration document set (`COS_MIGRATION_BRIEF.md`, `COS_BOOTSTRAP_PROMPT.md`, `INTERACTION_MODEL.md`) + `cos/CURRENT_PRIORITY.md`
- **Spine:**
  1. What was decided: architecture v0 frozen; COS scoped to internal proactive layer; Codex named as versioning steward.
  2. Why it matters: removes the "is COS the boss?" failure mode that was bleeding founder energy.
  3. What ships next: Milestone 1 (executable wedge skeleton).
- **Format:** short repo update / changelog-style post
- **Status:** outline only; needs Frank's voice on framing

### 3 short posts

1. **"Raw AI is smart. It still drifts."**
   - source: `ARCHITECTURE.md` §2 (problem statement)
   - hook: list the 5 failure modes from §2; close with one sentence on the obedience layer
   - audience: agent-builders feeling the pain

2. **"Internal does not mean useless: why COS matters before it is public."**
   - source: `README.md` "Internal does not mean useless" + `COS_MODEL.md` §1, §11
   - hook: three value paths (service / product / media) for an internal layer
   - audience: founders trying to decide whether to build infra they cannot sell directly

3. **"The right demo is not 'AI does everything.' It is 'AI completes a real workflow.'"**
   - source: `WEDGE_WHATSAPP_PUBLISHING.md` §6-7 + `DISTRIBUTION.md` §3
   - hook: rebuild the wedge in one paragraph (command → context → approval → publish → trace)
   - audience: people pitching or evaluating AI products

---

## Approval checklist

- [ ] aligned with current positioning (`POSITIONING.md`)
- [ ] tied to real work (every item has a `source:` reference inside this repo)
- [ ] no exaggerated claims (no "fully autonomous" / "zero setup" language)
- [ ] points toward the wedge (command → context → approval → execution)
- [ ] no claim of a running demo until Milestone 1 ships

## Out of scope this week

- demo video / GIF (requires running system; Milestone 1 not built)
- comparison benchmark posts (requires before/after data)
- platform-specific publishing tactics (Instagram/LinkedIn) — secondary surface still undecided per `DISTRIBUTION.md` §6

## Publish order suggestion (for Frank to decide)

1. SGOPS note first — establishes the conceptual frame
2. OBEY proof update — anchors the frame to repo activity
3. Short posts — distribute fragments across the week

## Owner gates

- writing the drafts: Codex or Frank, COS can prepare scaffolds
- approving language: Frank
- publishing: manual per `DISTRIBUTION.md` §5; COS does not push
- repo commits / version bumps: Codex per `INTERACTION_MODEL.md` §4.5
