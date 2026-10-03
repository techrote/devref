# High-Leverage Memetic Hazards

A useful formal taxonomy is:

1. **Scope expanders** — increase the amount or breadth of work the agent considers in scope.
2. **Persistence amplifiers** — make the agent reluctant to stop, accept a blocker, or terminate at an evidence boundary.
3. **Judgment delegators** — transfer unstated scope/priority/necessity decisions to the agent.
4. **Evidence inflators** — encourage stronger certainty or acceptance claims than the evidence necessarily supports.

Some terms could reasonably live in two categories; I’ve placed each under its **primary failure mode**.

## Scope expanders

| Word / phrase | What it implicitly encourages | Typical failure mode | Safer constrained form |
|---|---|---|---|
| **comprehensive** | Survey the entire surrounding problem | Excellent for synthesis; dangerous for implementation because it invites breadth | “Comprehensive **evidence review; implementation remains bounded**.” |
| **exhaustive** | Enumerate/test every possibility | Combinatorial explosion, broad sweeps, excessive testing | “Exhaustive **over this finite enumerated set**.” |
| **thorough / thoroughly** | Spend additional effort looking for omissions | Speculative edge cases and repeated checks after sufficient proof exists | “Thoroughly review **the changed paths only**.” |
| **robust** | Anticipate failures beyond the immediate requirement | Extra abstractions, retries, validation and defensive machinery | “Robust against **these named failure modes**.” |
| **production-ready** | Satisfy an implicit deployment checklist | Security, observability, compatibility, performance and docs all enter scope | Enumerate the actual readiness criteria |
| **production-grade** | Build to an implied high engineering standard | Gold-plating and architectural work | “Suitable for the existing production path under **X/Y/Z**.” |
| **harden** | Search for and eliminate plausible weaknesses | Open-ended security/correctness/edge-case expansion | “Harden **this invariant against these cases**.” |
| **future-proof** | Design for unknown future requirements | Premature abstraction and generality | Name the particular future seam required |
| **generalize** | Replace a specific solution with a reusable abstraction | Local fix becomes framework work | “Generalize across **A/B/C only**.” |
| **clean up** | Improve nearby untidy things | Unrelated naming, formatting, dead-code and structural work | “Clean up **only artifacts introduced by this change**.” |
| **polish** | Improve subjective quality until satisfactory | No objective stopping condition | Name the defects to be polished |
| **refactor** | Change surrounding structure while preserving behaviour | Much larger diff than required for the issue | “Refactor **X only**, preserving Y/Z interfaces.” |
| **simplify** | Remove apparent complexity | Deletes deliberate edge-case handling or useful seams | “Simplify while preserving **these invariants**.” |
| **modernize** | Replace old techniques with newer ones | Technology/style migration | Name the obsolete construct specifically |
| **improve** | Make something generally better | Agent invents its own optimization objective | “Improve **startup latency**…” |
| **optimize** | Seek performance gains | Hotspot search and speculative performance work expands | “Optimize **this measured hotspot only**.” |
| **efficient** | Minimize an unspecified resource | Agent chooses its own CPU/memory/latency trade-off | Specify which resource matters |
| **best** | Compare alternatives globally | Broad search for superior implementations | “Best among **these candidates under criterion X**.” |
| **optimal** | Find a global optimum | Disproportionate search/measurement effort | Prefer “measured improvement” |
| **ideal** | Redesign toward an imagined endpoint | Architectural scope creep | Replace with explicit criteria |
| **elegant** | Optimize aesthetics/abstraction | Clever redesign instead of minimal implementation | Usually omit from execution prompts |
| **all** | Universal coverage | Peripheral items become requirements | Enumerate the finite set |
| **every** | Universal coverage with stronger force | One irrelevant omission becomes task failure | Use only for a genuinely closed set |
| **any** | Broad permission | “Fix any failures” captures unrelated pre-existing failures | “Fix failures attributable to this change.” |

**Characteristic smell:** *the task acquires more surface area every time the agent inspects something.*

---

## Persistence amplifiers

| Word / phrase | What it implicitly encourages | Typical failure mode | Safer constrained form |
|---|---|---|---|
| **complete** | Finish everything plausibly associated with the task | Continues beyond explicit acceptance criteria | “Complete **the stated acceptance criteria only**.” |
| **fully** | Eliminate every apparent incompleteness | Turns bounded work into polish and adjacent fixes | “Fully satisfy **#123's explicit contract**.” |
| **finish** | Continue until an implicit notion of completion | Agent's definition of “finished” exceeds yours | “Finish **this issue only**.” |
| **resolve** | Eliminate the issue entirely | Refuses to terminate at an honest unresolved boundary | “Resolve **or record a precise evidence-backed blocker**.” |
| **until done** | Continue until subjective completion | Repeated retries and follow-on work | “Until **these criteria pass or blocker X is established**.” |
| **do not stop** | Override ordinary stopping behaviour | Agent continues through diminishing returns or failed gates | Prefer positive termination conditions |
| **keep going** | Suppress natural stopping points | Continues after saturation/no-go/blocker | “Continue with **the next named step only**.” |
| **whatever it takes** | Persistence plus almost unlimited discretion | Stop conditions effectively disappear | Avoid |
| **do whatever is necessary** | Broad means plus persistence | Scope and stopping decisions are both delegated | Avoid; state exact allowed actions |
| **best effort** | Keep trying despite obstacles | Partial result can blur into claimed completion | “If X cannot be established, stop and record the blocker.” |
| **continue** | Resume the previous trajectory | Continues stale or erroneous work without reconciliation | “Reconcile live state, then continue the current owner task.” |
| **proceed** | Move forward | Crosses gates that should have required explicit satisfaction | “Proceed **only if gate X passes**.” |
| **go ahead** | General execution permission | Can be interpreted much more broadly than intended | Attach it to the exact action |
| **revisit** | Return to something previously closed | Resurrects no-go or accepted work | “Revisit only **the unresolved portion**.” |
| **reassess** | Reopen a previous conclusion | Re-runs accepted work without new contradictory evidence | “Reassess only if **new evidence contradicts X**.” |
| **re-run** | Obtain fresh evidence | Repeats costly CI/hardware tests unnecessarily | “Re-run only if source identity changed or evidence is stale.” |
| **fresh** | Recompute rather than reuse | Discards valid accepted evidence and repeats expensive work | “Fresh **state reconciliation**; reuse accepted evidence.” |

**Characteristic smell:** *the agent has a valid terminal state available, but linguistically feels compelled to keep moving.*

---

## Judgment delegators

| Word / phrase | What it implicitly delegates | Typical failure mode | Safer constrained form |
|---|---|---|---|
| **as needed** | Decide what work is necessary | Agent silently expands its mandate | “Only if required by **criterion X**.” |
| **as appropriate** | Decide which actions are suitable | Hidden permission for docs/tests/refactors/cleanup | Define what makes an action appropriate |
| **where necessary** | Decide necessity | Model invents prerequisite work | Tie necessity to a named gate |
| **if useful** | Decide expected value | Almost anything can be rationalized as useful | “Only if it materially changes **decision X**.” |
| **relevant** | Decide scope relevance | Huge surrounding corpus becomes fair game | “Relevant to **issue X/files Y/criterion Z**.” |
| **necessary** | Decide whether something is required | Agent becomes requirements authority | Anchor to explicit dependency/acceptance criteria |
| **properly** | Infer the unstated standard of correctness | Agent supplies its own quality bar | Define “properly” explicitly |
| **correctly** | Infer the governing correctness contract | Ambiguous when several standards exist | Reference the canonical contract |
| **suitable** | Decide fitness criteria | Agent chooses hidden quality attributes | State fitness criteria |
| **reasonable** | Apply model judgement | Highly elastic threshold | Replace with measurable bounds |
| **handle** | Decide both diagnosis and remedy | Agent chooses scope and method | “Handle **the failing CI job only**.” |
| **address** | Decide what sort of intervention is needed | Documentation, mitigation or repair may be substituted for each other | Say “investigate”, “repair”, “document”, etc. |
| **take care of** | Resolve surrounding loose ends | Very broad implicit authority | Use an explicit verb |
| **safe** | Determine what “safe” entails | Excessive conservatism or unrelated mitigations | Name the safety invariant |
| **autonomous / autonomously** | Choose plan, actions, sequencing and stopping | Broad implicit permission; may combine multiple phases/tasks | Usually unnecessary when permissions are explicit |
| **independently** | Decide what needs independent duplication | May repeat expensive/risky evidence generation | “Independently review **existing evidence; do not rerun tests X**.” |
| **current** | Decide that present state outranks older state | Historically pinned evidence gets discarded | “Reconcile current state while preserving pinned historical evidence.” |
| **latest** | Prefer recency | Newer but provisional text outranks older accepted authority | “Use latest **accepted** state.” |
| **comparable** | Decide what counts as equivalent enough | Different runs/configurations get grouped too readily | Define comparison dimensions |
| **representative** | Decide which workload/sample represents reality | Convenient but unrepresentative test selected | Name the workload/population |
| **material** | Decide significance | Important disagreement gets dismissed as immaterial, or vice versa | Define threshold where practical |
| **meaningful** | Decide what matters | Subjective filtering of evidence/results | Specify the consequence being measured |

**Characteristic smell:** *the prompt contains a tiny phrase that secretly asks the model to write part of the specification itself.*

---

## Evidence inflators

| Word / phrase | What it implicitly encourages | Typical failure mode | Safer constrained form |
|---|---|---|---|
| **prove** | Establish strong/absolute causality | Excessive testing or stronger claim than evidence supports | “Establish the strongest reproducible evidence for…” |
| **verify** | Confirm correctness | Blurs source inspection, tests, CI and physical validation | “Verify **criterion X using evidence Y**.” |
| **validate** | Establish validity | Different validation classes get conflated | Say CPU/static/CI/physical/numerical validation |
| **confirm** | Turn a hypothesis into an affirmative conclusion | Weak evidence becomes confirmation | “Determine whether the evidence supports…” |
| **establish** | Treat a proposition as settled | Can push ambiguous result across the threshold | “Establish **if supported; otherwise mark NOT ESTABLISHED**.” |
| **root cause** | Find the singular underlying cause | Multiple causal families get artificially unified | “Determine causal mechanism or strongest evidence boundary.” |
| **fixed** | Declare the problem eliminated | Symptom disappearance substitutes for causal repair | “Demonstrated repair for **the defined reproducer**.” |
| **resolved** | Declare final disposition | Uncertainty gets compressed away | Use “resolved”, “bounded unresolved”, “no-go”, etc. explicitly |
| **correct** | Binary correctness conclusion | Clean tests get promoted into universal correctness | Name the contract proven |
| **safe** | Can also operate here | Clean validation treated as proof of universal safety | “No violation observed under **this test scope**.” |
| **equivalent** | Assert sameness | Different execution states called equivalent from incomplete observations | State the dimensions/tolerance of equivalence |
| **identical** | Assert exact sameness | Visual/state similarity gets over-promoted | Reserve for actual byte/pixel/identity equality |
| **reproducible** | Imply stable causality | Repeated symptoms can be mistaken for repeated mechanism | Distinguish “reproducible failure” from “reproducible cause” |
| **consistent with** | Suggest support | Often rhetorically drifts into “therefore caused by” | Pair with explicit competing explanations |
| **likely** | Assign confidence | Can become unsupported probabilistic judgement | Give concrete evidence and uncertainty instead |
| **demonstrated** | Promote observation into proof | Too broad unless object is tightly specified | “Demonstrated **route completion**”, not “demonstrated common cause” |
| **accepted** | Give epistemic authority | Acceptance process may be confused with truth/correctness | State what exactly was accepted and under which criteria |
| **clean** | Suggest absence of defects | “Clean validation” gets read as “correct implementation” | “Zero diagnostics in mode X for workload Y” |
| **passes** | Suggest overall success | One test suite passing becomes task-level acceptance | Name the exact test/gate that passes |
| **success** | Positive framing | Host/tool success can be conflated with renderer success | Qualify it: route success, control success, capture success |
| **failure** | Negative framing | Harness/host timeout becomes product defect | Classify the failure domain explicitly |
| **regression** | Causal comparison | Ordinary variance or unrelated breakage becomes attributed to the change | Require matched baseline and defined metric |
| **causal** | Mechanistic inference | Correlation gets upgraded prematurely | Require a discriminator/intervention chain |
| **defect** | Assign fault to implementation/vendor | Observation becomes blame attribution | Prefer “observed failure” until contract violation is established |

**Characteristic smell:** *the wording quietly pushes the answer one rung higher on the epistemic ladder.*

---

## Especially hazardous combinations

The individual words are manageable; combinations can be much more potent.

| Phrase | Implied behavioural payload |
|---|---|
| **“comprehensively resolve”** | broaden the investigation *and* refuse to stop at uncertainty |
| **“fully harden”** | search for arbitrary weaknesses until no apparent problems remain |
| **“production-ready implementation”** | invent a full readiness standard and satisfy it |
| **“do whatever is necessary to complete”** | delegate scope, methods and stopping conditions simultaneously |
| **“thoroughly investigate and fix”** | open-ended exploration plus pressure to produce a repair regardless of causal certainty |
| **“verify everything”** | universal scope plus unspecified evidence standard |
| **“continue until fully resolved”** | essentially deletes blocker/no-go as legitimate terminal states |
| **“independently verify”** | potentially duplicate all previous work unless evidence reuse is explicitly allowed |
| **“fresh comprehensive review”** | discard/re-litigate accepted evidence across a broad surface |
| **“robust, general solution”** | abstraction pressure + speculative future requirements |
| **“clean up all relevant issues”** | three simultaneous scope delegators |
| **“complete any necessary follow-up”** | agent gets to invent both follow-up tasks and completion criteria |

A particularly nasty construction is:

> **“Do whatever is necessary to comprehensively resolve any remaining issues.”**

It is only eleven words, but effectively delegates **problem discovery, scope definition, prioritization, solution choice, persistence policy, evidence threshold and stopping condition**.

That is almost the inverse of a bounded agent prompt.

## Compact warning mnemonic

For **high-leverage-memetic-hazards**, I’d use:

> **S P J E** — **Scope, Persistence, Judgment, Evidence**

When a high-density word appears in a prompt, ask:

- **S — Scope:** does this make more things part of the task?
- **P — Persistence:** does this make stopping harder?
- **J — Judgment:** am I unintentionally delegating specification decisions?
- **E — Evidence:** does this wording encourage a stronger conclusion than the evidence warrants?

That gives you a fairly quick lint pass for agent prompts without requiring a long checklist every time.
