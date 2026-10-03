| Word / phrase | What it implicitly encourages | Typical failure mode | Safer constrained form |
|---|---|---|---|
| **complete** | Finish everything plausibly belonging to the task | Pulls adjacent work into scope; keeps going after the actual acceptance criteria are met | “Complete **the stated acceptance criteria only**.” |
| **fully** | Remove every apparent incompleteness | Turns bounded work into polish/refactor/documentation expansion | “Fully satisfy **#123's explicit contract**.” |
| **comprehensive** | Survey the entire surrounding problem | Excellent for synthesis; dangerous for implementation because it invites breadth | “Comprehensive **evidence review; implementation remains bounded**.” |
| **exhaustive** | Enumerate/test every possibility | Combinatorial explosion, broad sweeps, excessive testing | “Exhaustive **over this finite enumerated set**.” |
| **thorough** / **thoroughly** | Spend extra effort looking for omissions | Repeated checks and speculative edge cases after sufficient proof exists | “Thoroughly review **the changed paths only**.” |
| **robust** | Anticipate failures beyond current requirements | Defensive machinery, retries, abstractions and error handling not justified by evidence | “Robust against **these named failure modes**.” |
| **production-ready** | Satisfy an implicit deployment checklist | Security, observability, docs, backwards compatibility, deployment, performance, etc. suddenly enter scope | Spell out the actual readiness criteria instead |
| **production-grade** | Similar, often even broader | Gold-plating and architecture changes | “Suitable for the existing production path under **X/Y/Z constraints**.” |
| **harden** | Find and eliminate plausible weaknesses | Open-ended bug/security/edge-case search | “Harden **this invariant against these cases**.” |
| **future-proof** | Design for unknown future requirements | Premature abstraction/generalization | Usually avoid; name the future seam you actually need |
| **generalize** | Replace a specific solution with a reusable abstraction | Turns a local fix into framework work | “Generalize only across **A, B and C**, which already require identical behavior.” |
| **clean up** | Improve anything nearby that looks untidy | Classic scope-creep trigger; formatting, naming, dead code and refactoring appear | “Clean up **only artifacts introduced by this change**.” |
| **polish** | Improve subjective quality until it feels finished | No objective stopping condition | Specify exact defects to polish |
| **refactor** | Change structure while preserving behavior | Encourages wider structural rewrites than the actual defect requires | “Refactor **X only**, preserving Y/Z interfaces.” |
| **simplify** | Reduce apparent complexity | Can delete deliberate edge-case handling or architecture seams | “Simplify without changing **these named invariants**.” |
| **modernize** | Replace old patterns with newer ones | Huge implicit technology/style migration | Name the specific obsolete construct |
| **improve** | Make something “better” by unspecified criteria | Agent invents its own objective function | “Improve **latency / readability / allocation count** under these constraints.” |
| **optimize** | Seek performance gains broadly | Premature or speculative optimization, benchmark expansion | “Optimize **this measured hotspot only**; retain only measured wins.” |
| **efficient** | Minimize some unspecified cost | Agent chooses CPU/memory/code-size/latency trade-offs itself | Name the resource being optimized |
| **fix** | Make an observed problem disappear | Can encourage symptom suppression rather than causal correction | “Fix the demonstrated invariant violation; do not mask the symptom.” |
| **resolve** | Eliminate the issue entirely | Stronger than “investigate”; may pressure uncertain evidence into a conclusion | “Resolve **or record a precise evidence-backed blocker**.” |
| **investigate** | Explore until the cause becomes clear | Potentially unbounded research loop | “Run a **bounded investigation** answering X.” |
| **diagnose** | Determine causality | Can overstate conclusions from weak evidence | “Diagnose to the **strongest defensible evidence boundary**.” |
| **prove** | Establish certainty | Can lead to over-testing or unjustified claims when absolute proof is unavailable | “Establish the strongest reproducible evidence for…” |
| **verify** | Confirm correctness | Ambiguous about depth: one test? all tests? independent evidence? | “Verify **these criteria with these tests**.” |
| **validate** | Similar to verify, often broader | Can blur static validation, CI, physical behavior and acceptance | Name the validation class: source, CI, physical, numerical, etc. |
| **review** | Inspect for problems | Agent may review everything rather than the relevant delta | “Review **the diff and acceptance mapping**.” |
| **audit** | Systematically examine for omissions/violations | Often expands to every related subsystem | “Audit **these five invariants**.” |
| **reassess** | Reopen earlier conclusions | Can cause previously accepted work to be unnecessarily relitigated | “Reassess only if **new evidence contradicts X**.” |
| **revisit** | Return to an old area | Can resurrect intentionally closed/no-go work | “Revisit only **the unresolved portion**.” |
| **finish** | Continue until some implicit notion of completion | Dangerous if the agent's definition of “finished” exceeds yours | “Finish **this issue only**.” |
| **continue** | Resume prior trajectory | If state is messy, it may continue the *wrong* trajectory without reconciling | “Reconcile live state, then continue the current owner task.” |
| **proceed** | Move forward without further questions | Can bypass an important decision boundary | “Proceed **only if gate X passes**.” |
| **go ahead** | Broad permission to execute | Context can make this surprisingly expansive | Attach it to the exact next operation |
| **handle** | Take care of whatever the problem requires | Agent chooses both scope and solution | “Handle **the failing CI job only**.” |
| **address** | Do something about an issue | May result in docs/workaround rather than actual correction—or vice versa | State whether you mean investigate, repair, document or close |
| **take care of** | Resolve surrounding loose ends | Highly contextual and broad | Usually replace with an explicit verb |
| **as needed** | Agent decides what is necessary | Hidden delegation of scope control | “Only if required by criterion X.” |
| **as appropriate** | Agent applies its own judgment broadly | Can silently add actions, tests, docs, cleanup | Define what counts as appropriate |
| **where necessary** | Same issue | Necessity becomes model-defined | Tie necessity to an explicit gate |
| **if useful** | Permission for optional expansion | Nearly anything can be rationalized as useful | “Only if it materially changes decision X.” |
| **best effort** | Keep trying despite obstacles | Can weaken failure/stop semantics and produce partial-but-presented-as-done results | “Stop and record the blocker if X cannot be established.” |
| **do whatever is necessary** | Maximum discretion | One of the strongest scope-expansion phrases possible | Avoid unless you genuinely want broad delegation |
| **whatever it takes** | Persistence plus scope freedom | Can override sensible stopping conditions | Avoid in engineering-agent prompts |
| **until done** | No natural stopping boundary other than agent judgement | Loops, retries, adjacent fixes, lengthy polishing | “Until **these explicit criteria** pass or a blocker is established.” |
| **do not stop** | Persistence despite uncertainty/failure | Can conflict with safety/resource/context limits | Prefer positive completion conditions |
| **keep going** | Suppresses ordinary stopping behaviour | Especially bad after evidence saturation or repeated failure | “Continue with **the next named step only**.” |
| **autonomous / autonomously** | Grants broad planning and execution discretion | Can implicitly combine investigation, implementation, review, merging, cleanup and follow-on work | Usually unnecessary if permissions and stopping conditions are already explicit |
| **independently** | Don't rely on previous claims; check for yourself | Good for review, but can duplicate expensive work or repeat risky tests | “Independently review **existing evidence; do not repeat physical tests**.” |
| **fresh** | Recompute rather than reuse stale state | Can unnecessarily repeat expensive measurements/builds | “Fresh **state reconciliation**, reuse accepted immutable evidence.” |
| **re-run** | Obtain new evidence | Can consume scarce hardware/CI resources even when old evidence is sufficient | “Re-run only if the prior result is stale or source identity changed.” |
| **latest** | Prefer newest state | Can accidentally make temporal recency outrank accepted authority | “Use latest **accepted** state.” |
| **current** | Use live state | Useful, but may silently discard historically important pinned evidence | “Reconcile current state while preserving pinned historical evidence.” |
| **all** | Universal quantifier | Often far broader than intended | Enumerate the finite set whenever possible |
| **every** | Same, but even more forceful | One missed peripheral item turns into an apparent task failure | Use only when the set is genuinely finite and known |
| **any** | Very permissive scope | “Fix any failures” can mean unrelated existing failures too | “Fix failures attributable to this change.” |
| **relevant** | Requires semantic judgement about scope | Models can find an enormous amount “relevant” | “Relevant to **criterion X / files Y / issue Z**.” |
| **necessary** | High-density delegation of judgement | Agent decides both whether and why something is required | Anchor it to an explicit dependency or acceptance criterion |
| **safe** | Invokes an unspecified safety model | Can result in excessive conservatism or irrelevant mitigations | Name the exact safety invariant |
| **properly** | Implies there is an unstated correct standard | Agent fills in its own standard | State what “properly” means |
| **correctly** | Similar | Fine when correctness is already formally defined; vague otherwise | Point to the canonical contract |
| **best** | Requires global comparison/optimization | Can cause broad alternative search | “Best among **these three candidates under criterion X**.” |
| **optimal** | Implies mathematical/global optimum | Grossly disproportionate work unless the search space is explicit | Prefer “measured improvement” |
| **ideal** | Invites redesign toward an imagined endpoint | Scope explosion and speculative architecture | Use concrete criteria instead |
| **elegant** | Optimizes aesthetics/abstraction | May trade simplicity of change for cleverness | Usually avoid in execution prompts |
