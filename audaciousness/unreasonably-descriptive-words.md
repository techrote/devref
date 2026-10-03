| Word / compact term | What it tends to imply in an agentic prompt | Example |
|---|---|---|
| **reconcile** | Inspect live state, compare it with supplied assumptions, resolve discrepancies, don't blindly trust the prompt | “Reconcile live main, issues, PRs and CI first.” |
| **bounded** | Finite scope, explicit limits, don't expand indefinitely, stop when the defined objective is met | “Run a bounded investigation.” |
| **canonical** | Treat this as the normative source of truth; other descriptions are secondary | “Read the canonical contract first.” |
| **authoritative** | Stronger than “relevant”: this source controls when accounts conflict | “Treat the latest accepted report as authoritative.” |
| **fail-closed** | Ambiguity or missing proof means do not accept/proceed/unblock | “Evaluate the gate fail-closed.” |
| **idempotent** | Safe to repeat; detect existing work rather than duplicating or corrupting it | “Make the recovery procedure idempotent.” |
| **deduplicate** | Search for already-existing equivalent work and reuse/resume it | “Deduplicate against existing issues and branches.” |
| **preserve** | Don't delete, rewrite, flatten or discard existing evidence/state/history | “Preserve failed attempts and STOP files.” |
| **immutable** | Stronger preserve: the named evidence must not be edited/reinterpreted in place | “Treat historical manifests as immutable.” |
| **atomic** | Keep one conceptual change together; don't mix unrelated fixes | “Make the repair atomic.” |
| **surgical** | Modify the smallest necessary surface while leaving surrounding behaviour untouched | “Use a surgical source change.” |
| **minimal** | Smallest sufficient implementation/evidence, avoid speculative extras | “Implement the minimal repair.” |
| **orthogonal** | Keep two concerns independent; don't make progress on one depend unnecessarily on the other | “Keep profiling orthogonal to correctness.” |
| **deterministic** | Same inputs → stable result; eliminate timing/random/environment ambiguity | “Add a deterministic reproducer.” |
| **reproducible** | Record enough identity/procedure that someone else can recreate the result | “Produce reproducible evidence.” |
| **traceable** | Every conclusion/change should map back to evidence, source, issue, test or requirement | “Keep every acceptance claim traceable.” |
| **evidence-backed** | Don't promote inference, intuition or coincidence into a conclusion | “Give each incident an evidence-backed disposition.” |
| **preregistered** | State hypothesis, change and expected interpretations before executing the experiment | “Use one preregistered discriminator.” |
| **discriminating** | Design the next action to distinguish hypotheses rather than merely gather more data | “Choose the next discriminating test.” |
| **saturated** | Enough evidence has been collected; further repetitions add little and should stop | “Stop physical testing at saturation.” |
| **conservative** | Prefer weaker defensible claims over stronger uncertain ones | “Use a conservative recovery disposition.” |
| **explicit** | Do not leave assumptions, fallbacks, unknowns or state transitions implicit | “Record an explicit residual limitation.” |
| **exact** | Pin identities/values rather than approximate them or substitute equivalents | “Verify the exact PR head.” |
| **independent** | Require a separate verification path rather than self-confirming evidence | “Obtain an independent review.” |
| **adversarial** | Test edge cases specifically designed to break the claimed invariant | “Add adversarial fixtures.” |
| **comprehensive** | Cover the whole relevant surface, not merely the easiest successful path | “Perform a comprehensive synthesis.” |
| **succinct** | Compress aggressively while retaining essential information | “Create a succinct handoff prompt.” |
| **review-ready** | Implementation, tests, documentation, diff cleanliness and known limitations should all be in a state suitable for review | “Leave the PR review-ready.” |
| **dependency-ready** | Preconditions are satisfied, but **do not actually start the dependent task** | “Mark PF-019 dependency-ready.” |
| **superseded** | Old result remains historical evidence but is no longer current truth | “Mark the diagnostic hypothesis superseded.” |
