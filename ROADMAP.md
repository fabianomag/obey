# OBEY Roadmap

**Status:** draft v0  
**Purpose:** define build order so execution does not depend on rethinking the whole project every day.

---

## Milestone 1 - Executable wedge skeleton

Goal:

Create the minimum local architecture for:

`command -> context -> approval -> execution`

This milestone should produce:

- repo/app skeleton
- core data model
- command schema
- project state structure
- approval record structure
- publish adapter interface

Done means:

- the system can run locally with mock publishing
- the flow is visible and testable

---

## Milestone 2 - Founder demo loop

Goal:

Make the wedge usable for Frank's own workflow.

This milestone should produce:

- one command entry path
- one context pack format
- one generated artifact flow
- one approval step
- one publish simulation or first integration

Done means:

- Frank can demonstrate the flow end-to-end

---

## Milestone 3 - Real connector

Goal:

Connect one real external surface.

Recommended first connector:

- WhatsApp intake or Instagram publish

Not both at full breadth immediately unless implementation falls into place cleanly.

Done means:

- one real external action works reliably enough to demo

---

## Milestone 4 - Public explanation layer

Goal:

Make the public surfaces explain a real thing.

This milestone should produce:

- OBEY site
- SGOPS note(s)
- OSS framing
- demo narrative

Done means:

- public messaging describes implemented behavior, not wishful language

---

## Milestone 5 - COS integration layer

Goal:

Let COS support the product build and authority loop more deeply.

This milestone should produce:

- better state packaging
- better content extraction from work
- better proactive reminders and queues

Done means:

- COS reduces orchestration load without pretending to replace the founder

---

## Current next step

The next build step is:

**Milestone 1**

Specifically:

- scaffold the executable wedge
- define inputs, state, approvals, and adapter boundaries
- make the loop runnable locally before any serious external integration
