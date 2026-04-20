# Five Levels of Agent Obedience (and Why Most Agents Are Stuck at Level 2)

**By Fabiano Frank · SGOPS / OBEY**
**Status:** draft — not approved, not published
**Source documents:** `OBEY/DISTRIBUTION.md` §4, `OBEY/ARCHITECTURE.md` §1-2
**Audience:** builders and founders already using Claude Code, Codex, Cursor, or similar agents
**Length target:** 600–900 words

---

When a long agent run goes wrong, the first instinct is to blame intelligence. The model "didn't understand." It "needs a better prompt." It "wasn't smart enough." That framing is comfortable because it puts the failure outside the workflow, somewhere in the model weights, where nobody on the team is responsible.

Most of the time, that framing is wrong.

Capable agents still drift. They forget what was decided two messages ago. They reintroduce ideas that were explicitly rejected. They pick up references nobody asked for and drop the ones that were approved. They restart with generic priors instead of the project's specific state. None of that is a reasoning failure. It is an obedience failure, and obedience is a different axis from intelligence.

It helps to name the levels.

### Level 1 — Draft obedience

Given a source, the agent produces the requested output in the requested format. A post draft. An outline. CTA options. A summary. This is what most "look how good AI is now" demos prove. It is real, and it is also the easiest level on the ladder. Every modern frontier model clears it.

### Level 2 — Context obedience

The agent keeps the right references, decisions, tone, and positioning across outputs. It uses the offer that actually exists. It respects claims marked as approved. It reuses the project references fed in earlier. It stays inside the brand angle that was defined.

This is where things start to break. A model that nails Level 1 in isolation will quietly regress at Level 2 the moment the conversation is long enough or the context window pressure is high enough. The output looks correct in form and wrong in substance. Wrong tone. Wrong claim. Wrong reference. Wrong angle.

### Level 3 — Workflow obedience

The agent updates files, project state, and linked surfaces in a controlled way. It creates the new article in the right folder. It updates the queue. It writes captions to the publish folder. It links related artifacts. The output stops being a single message and becomes a set of changes to a real workspace.

Most production frustration with agents lives at Levels 2 and 3. The model is plenty smart. The workflow is what breaks.

### Level 4 — Platform obedience

The agent publishes through external systems with approval checkpoints. CMS posts. Scheduled content. Asset uploads. Harder than it sounds, mostly because it forces the system to honor an approval gate before doing anything externally visible.

### Level 5 — Full external autonomy

The agent creates accounts, configures APIs, and runs third-party surfaces with little supervision. This level gets all the marketing attention and almost none of the production reliability. Anti-bot systems, shifting interfaces, authentication friction, platform restrictions. Promising it as the first proof point is how products lose credibility.

---

The ladder matters because the levels are not interchangeable. A team that needs Level 3 cannot solve their problem by making the model "smarter" at Level 1. A product that promises Level 5 cannot deliver it just because Level 1 looks impressive in a demo.

The ladder also explains why "memory" alone is not the fix people hope it is. Long-term memory helps Level 2 a little. It does very little for Level 3, where the issue is that the agent has no notion of what counts as a decision versus a discussion, what counts as approved versus pending, and what state on disk belongs to which project. Memory is a recall mechanism. Obedience is a behavior contract. Different things.

This is the gap a behavior layer is supposed to close. Treat decisions as first-class objects, not chat history. Treat approvals as a state transition, not a tone of voice. Treat references as a structured pack the agent must consult, not vibes inherited from earlier turns. Treat workflow updates as something an execution contract specifies, not something the model improvises.

None of that requires a smarter model. It requires a layer above the model that the model has to obey.

The practical takeaway is small. Before reaching for a bigger model, ask which level you are actually failing on. If the agent is failing at Level 2, more parameters will not help. Better context discipline will. If you are failing at Level 3, you do not need a new model release. You need a workflow the model is forced to honor. If you are promising Level 5 to win deals, you are setting yourself up to defend something the entire industry cannot yet do reliably.

Most of the value people want from agents this year lives at Levels 2 and 3. That is a much more tractable problem than "general intelligence," and it is the one worth solving first.

---

**Internal note (not for publication):** Argues from the framework, not from a benchmark. No measured before/after yet because no executable wedge exists to produce one. When Milestone 1 ships, a follow-up can convert this from "framework piece" into "framework + evidence."
