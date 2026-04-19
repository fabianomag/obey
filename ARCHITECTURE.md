# OBEY Architecture

**Status:** draft v0
**Date:** 2026-04-19
**Purpose:** define exactly where the system is going before implementation starts.

---

## 1. Product thesis

OBEY is a runtime and behavior layer for AI agents.

Its job is not to store all memory.
Its job is not to be a general model.

Its job is to make agents:

- obey project context
- obey approved decisions
- obey reference material
- obey execution constraints
- produce outputs that are easier to trust and reuse

Core thesis:

**Memory without behavioral control is not enough.**

---

## 2. Problem statement

Current agents often fail in long-running work because they:

- treat discussion and approval as the same thing
- forget visual, editorial, or operational constraints
- restart from generic priors instead of project-specific state
- fail to learn from corrections
- lack a stable execution contract

This creates constant human re-supervision.

OBEY is designed to reduce that failure mode.

---

## 3. Product boundaries

### What OBEY is

- a behavior layer
- a runtime layer
- a project-state layer
- an execution-contract layer
- a decision/approval aware system

### What OBEY is not

- not a foundation model
- not a general-purpose note app
- not a plain prompt pack
- not a generic "agent marketplace"
- not a full autonomous employee in v1

---

## 4. Ecosystem map

```text
                    +----------------------+
                    |        SGOPS         |
                    |   Lab / Media / GEO  |
                    |   docs + failures    |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    |         OBEY         |
                    |   Product / Brand    |
                    |   OSS + Runtime      |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    |          COS         |
                    | Internal engine      |
                    | founder ops + learn  |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    |   Claude / Codex /   |
                    | other frontier agents|
                    +----------------------+
```

Meaning:

- `OBEY` is the product
- `COS` is the internal engine and operating layer
- `SGOPS` is the lab and publishing surface
- frontier models are underlying execution engines

### Engine strategy

The system should explicitly assume multiple engines.

Initial engines:

- Claude Code
- Codex

Interpretation:

- these are not competitors to OBEY
- these are execution substrates under OBEY and COS
- OBEY must be useful even if the active engine changes

---

## 5. V1 product wedge

### Wedge

**Decision-aware execution for project work**

### Plain-English pitch

OBEY makes agents stop improvising and start following project rules.

### User type for v1

Not end-clients like Julia or Daniela.

Primary v1 user:

- builders
- founders
- power users of agents
- people already using Claude/Codex/Cursor and feeling pain from drift

### Core pain for v1 user

"The agent is smart, but it still does not stay aligned with the project."

---

## 6. V1 system architecture

### 6.1 Layers

#### Layer 0 - Frontier Engines

Responsibilities:

- planning
- code generation
- editing
- execution

Examples:

- Claude Code
- Codex

These engines do not define the product.
They are the programmable substrate.

#### Layer A - OBEY OSS

Free entry surface.

Responsibilities:

- teach the agent the OBEY workflow
- define concepts: decision, approval, reference pack, contract, run
- create visible behavior improvement
- drive users toward OBEY Runtime

Output:

- open-source skill/spec/installable package

#### Layer B - OBEY Runtime

Core monetizable layer.

Responsibilities:

- persist state per project
- read and write structured project files
- assemble runtime context
- enforce execution contracts
- record runs and approvals
- expose CLI commands

Output:

- CLI/runtime package

#### Layer C - Agent Connectors

Responsibilities:

- connect runtime behavior to Claude/Codex/other agents
- make OBEY usable across engines

Output:

- adapter docs
- engine-specific wrappers if needed

#### Layer D - COS Skill Layer

Internal layer for founder operations.

Responsibilities:

- operationalize Claude Code and Codex for Frank's workflow
- encode founder-specific practices
- digest transcripts and project context
- support internal execution hygiene

Important:

COS is not the same thing as OBEY Runtime.
COS is a consumer and producer of patterns that may later feed OBEY.

---

## 6.2 Public and private boundary

The architecture only works if the boundary is explicit.

### Private: COS

Should remain internal in the beginning:

- founder notes
- client context
- personal workflows
- project-specific heuristics
- session summaries
- experimental prompts and routines

### Public: OBEY OSS

Should expose only the reusable method:

- project brief format
- decision log format
- approval contract format
- reference pack structure
- run workflow
- engine adapter instructions

### Paid later: OBEY Runtime

Should monetize the durable execution layer:

- persistent project state
- multi-project operation
- approvals and audit trail
- team workflows
- reusable runtime commands

This is the key distinction:

COS is where Frank gets leverage.
OBEY is where the market can touch that leverage.

---

## 6.3 Value capture model

There are three monetization paths in this architecture.

### Path 1 - Cashflow now

Frank uses COS internally to operate Claude Code and Codex for client work.

This is a service business.

The client does not need to buy COS.
The client only needs to feel the result:

- less confusion
- faster execution
- fewer repeated explanations
- better project continuity

### Path 2 - Adoption and proof

OBEY OSS is the public wedge.

It gives builders a visible way to improve agent behavior without buying a full SaaS.

This creates:

- usage
- discussion
- proof
- trust

### Path 3 - Software revenue later

OBEY Runtime becomes the paid layer when the method is proven.

That is where the system can monetize durable state and repeatable execution, not just advice.

Important:

Frank does not need to choose between service and product immediately.
Service can fund product, and product can later reduce dependence on service.

---

## 7. Core concepts

### Project

A durable workspace under OBEY management.

### Decision

Something explicitly chosen and expected to remain true until changed.

Examples:

- approved homepage tone
- approved visual references
- rejected design directions
- delivery scope constraints

### Approval

A higher-trust state than discussion.

Examples:

- "use this direction"
- "this reference is now canonical"
- "do not revert this change"

### Reference Pack

A structured bundle of references relevant to the task.

Examples:

- screenshots
- URLs
- notes from founder/client
- approved examples
- anti-examples

### Execution Contract

A task-specific operating contract that tells the agent:

- what to do
- what not to do
- which references matter
- what counts as done
- what needs approval

### Run

A concrete execution attempt tracked by OBEY.

Contains:

- task
- context used
- decisions applied
- output generated
- status

---

## 8. Runtime state model

Each project should be representable as structured files on disk.

Proposed initial shape:

```text
.obey/
  project.json
  decisions/
    approved.md
    rejected.md
    pending.md
  references/
    references.json
    notes.md
  contracts/
    active-task.md
  runs/
    2026-04-19-run-001.md
  outputs/
  memory/
    summaries.md
```

Important:

- this is not trying to store everything
- this is trying to store what changes behavior

---

## 9. V1 flow

### Flow 1 - Create a task

1. user defines project
2. user adds references
3. user records decisions
4. OBEY generates execution contract
5. agent runs under that contract

### Flow 2 - Review a result

1. user reviews output
2. changes are classified as:
   - approved
   - rejected
   - pending
3. OBEY updates project state

### Flow 3 - Re-run later

1. user asks for another task
2. OBEY assembles relevant context from state
3. agent runs with less drift

---

## 10. What v1 must prove

V1 does not need to prove autonomy.

V1 must prove:

- lower drift
- better reference adherence
- better continuity
- less repeated correction

And it should prove this across at least two execution contexts:

- direct use of an engine
- engine routed through OBEY/COS patterns

The demonstration should be:

**same engine, same task, better result through OBEY**

---

## 11. Non-goals for v1

Do not build these now:

- WhatsApp-native agent
- full autonomous employee
- generalized long-term memory platform
- GUI-heavy SaaS dashboard
- marketplace of many random skills
- end-client automation suite
- a public promise that COS itself already does everything

Those are downstream possibilities, not v1 requirements.

---

## 12. Suggested technical stack

### Runtime

- TypeScript
- Node.js CLI
- Markdown + JSON as local-first state

### Product site

- likely Next.js

### Internal skill layer

- Markdown skill/spec
- local workflow docs
- adapters for Claude Code and Codex usage

### Model layer

- model-agnostic by design
- first-class support can start with Claude/Codex style workflows

### Why local-first first

- easier to reason about
- founder can dogfood it daily
- lower product risk
- easier to demo behavior change

---

## 13. Phased roadmap

## Phase 0 - Architecture lock

Deliverables:

- brand architecture
- system boundaries
- state model
- operating model
- product wedge

## Phase 1 - OBEY OSS

Deliverables:

- open-source behavior layer
- OBEY concepts formalized
- install/use docs
- first Claude Code and Codex usage path

## Phase 2 - OBEY Runtime local

Deliverables:

- CLI
- project state
- decision/approval storage
- execution contracts
- run logging
- engine adapters

## Phase 3 - Demonstration proofs

Deliverables:

- public comparison demos
- SGOPS write-ups
- benchmark-style examples

## Phase 4 - Monetization layer

Deliverables:

- premium runtime features
- hosted or team workflow components if needed

---

## 14. Strategic rule

The project wins if it becomes known for one thing:

**agents behave better under OBEY than without it.**

COS contributes to that internally.
OBEY captures that externally.

If that becomes true, everything else becomes easier:

- product
- content
- demos
- monetization
- ecosystem expansion

If that does not become true, the brand is just language.
