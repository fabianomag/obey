# Raw AI Is Smart. It Still Drifts.

**By Fabiano Frank · SGOPS / OBEY**
**Status:** draft — not approved, not published
**Source documents:** `OBEY/ARCHITECTURE.md` §2 (problem statement)
**Format:** site-first short post (≈ 200–300 words)

---

The model is not the bottleneck anymore.

Anyone running long agent work has felt the same five failure modes show up over and over, regardless of which frontier model is sitting underneath:

- the agent treats discussion and approval as the same thing
- it forgets visual, editorial, or operational constraints between turns
- it restarts from generic priors instead of the project's specific state
- it does not learn from corrections; the same fix has to be repeated
- there is no stable execution contract, so every run drifts in a new direction

None of these are reasoning failures. The model can reason. It just has no behavioral layer telling it what to honor and what to ignore. So it improvises. The improvisation looks competent in any single message and falls apart across a week of work.

Memory does not fix this. A smarter base model does not fix this. What is missing is a layer that turns decisions into first-class objects, makes approvals a real state transition, and gives the agent a contract it has to respect.

Most agent failures in production are workflow failures wearing an intelligence costume.

---

**Internal note (not for publication):** Framework angle, not a benchmark. Holds up without a demo because every reader running agents has lived these five failure modes.
