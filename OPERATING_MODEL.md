# OBEY Operating Model

**Status:** draft v0
**Date:** 2026-04-19
**Purpose:** define how this becomes real in practice instead of another drifting concept.

---

## 1. Core rule

Frank should not wake up every day asking:

- what do I work on?
- is COS doing this or not?
- should Codex build or should I build?
- are we making product, content, or experiments?

The operating model exists to remove that confusion.

---

## 2. Roles

### Frank

Founder, product owner, curator, and primary dogfooder.

Responsibilities:

- choose the problem worth solving
- approve architecture and product direction
- supply real project pain from his own work
- review demos and outputs
- decide what is good enough to publish
- protect the wedge from dilution

Frank is not required to invent architecture from scratch every day.

### Codex

Architecture and implementation partner.

Responsibilities:

- translate product thesis into concrete system design
- create technical docs, schemas, and project structure
- implement runtime and product layers
- keep the codebase coherent
- validate builds and reduce ambiguity

Codex is the main builder of the initial product architecture.

### Claude Code

Primary dogfooding engine and real-world operational surface.

Responsibilities:

- serve as one of the main substrates that COS operationalizes
- provide a real environment for OBEY patterns to be tested
- help validate whether the product improves agent behavior in practice

Claude Code is not the product.
It is one of the first environments where the product thesis must prove itself.

### COS

Internal support engine.

Responsibilities in this phase:

- summarize sessions
- digest logs and transcripts
- turn founder notes into structured briefs
- track decisions and candidates
- support research and spec hygiene
- keep bounded operating loops moving proactively
- support authority and distribution work when that is the current priority

COS is **not** the main builder of OBEY v1.
COS is support infrastructure around the core build.
It can evolve into a powerful internal skill layer without becoming the main public product.

---

## 3. Decision rule: who does what

### Frank does

- product judgment
- wedge selection
- founder intuition
- demo taste
- publish/no-publish decisions

### Codex does

- architecture
- code implementation
- repo organization
- technical docs
- system integration

### Claude Code does

- serve as primary operational testbed
- run founder workflows under COS guidance
- expose real pain and drift patterns

### COS does

- synthesis
- memory hygiene
- session compression
- background digestion
- structured notes for future work
- proactive packaging of work into next actions and publishable artifacts

---

## 4. Workstreams

This project has four separate workstreams.

### Workstream A - OBEY Product

Main focus.

Includes:

- OSS behavior layer
- runtime
- adapters
- product site
- engine compatibility

### Workstream B - SGOPS Lab

Research and public thinking.

Includes:

- essays
- failure analysis
- comparison posts
- ecosystem framing

Important:

SGOPS is not the whole distribution engine by itself.
It is the lab and documentation surface.

### Workstream C - Authority and Distribution

Current founder pain.

Includes:

- content queue
- proof extraction
- cross-linking between surfaces
- publishing cadence
- authority-building artifacts

Important:

This is where COS should be most proactively useful in the current phase.

### Workstream D - Client/Reality Feed

Source of real pain.

Includes:

- Julia
- Daniela
- Frank's own projects

Important:

clients are not the product.
they are the signal source.

---

## 5. Weekly cadence

This should not be an amorphous "work on it every day" project.

Recommended weekly cadence:

### Monday

- choose one primary objective for the week
- define one proof target
- freeze distractions

### Tuesday to Thursday

- implementation and validation
- one lane only unless blocked

### Friday

- review what changed
- extract SGOPS write-up if relevant
- update decisions
- define next week's focus

### Weekend or optional slot

- demos
- reflection
- founder thinking

---

## 6. Daily cadence

Recommended daily structure for OBEY work:

### Block 1 - Product

One focused block on product architecture or code.

### Block 2 - Review

Review outputs, compare behavior across engines, record decisions.

### Block 3 - Capture

COS can summarize what was learned and update support material.

If there is not enough time for all three:

only Block 1 is mandatory.

---

## 7. How work should start

Every meaningful work session should begin with a short session brief:

- current objective
- current blocking question
- what counts as done
- what not to touch
- which engine is being used for this session

Codex can work from that.
COS can summarize around that.

---

## 8. What not to do

### Do not do open-ended ideation every day

New ideas go to backlog, not to the steering wheel.

### Do not make COS responsible for undefined product invention

COS supports.
It does not replace architecture leadership at this stage.

### Do not split focus across too many fronts

If OBEY is the main bet, SGOPS becomes lab and client work becomes signal only.

### Do not chase virality before wedge proof

Without a strong wedge, virality just amplifies confusion.

---

## 9. Publish rule

Something should be published only if it satisfies at least one:

- proves the wedge
- attracts the right technical audience
- clarifies the category

If it does none of these, it is likely noise.

---

## 10. Success criteria for the next phase

The next phase is successful when all of these are true:

- OBEY has a stable thesis
- the architecture is no longer fuzzy
- Frank knows what the product is
- Codex knows what to build
- COS knows how to support
- there is one clear proof target

That is the threshold before aggressive implementation.

---

## 11. Immediate working agreement

For now:

- Frank owns direction
- Codex owns architecture and implementation scaffolding
- Claude Code is the primary real-world execution substrate to operationalize
- COS supports notes, synthesis, workflow compression, and future digestion

This avoids the worst failure mode:

**trying to make COS invent the product while the product itself is still undefined.**
