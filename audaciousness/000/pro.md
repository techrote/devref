# Long-Horizon Astra Pro — Mission Design Protocol

When crafting substantial Astra Pro engineering prompts, incorporate the following execution principles. These are intended to maximise productive engineering while avoiding orchestrator context exhaustion, excessive scope expansion and the commonly encountered five-hour execution timeout.

## Orchestrator and delegation

Employ three concurrent specialist subagents enthusiastically and throughout the productive mission.

The principal agent should act primarily as technical director, architect, integrator and decision-maker, rather than undertaking most of the implementation personally.

- Aim to delegate at least 80% of substantive implementation wherever practical.
- Give specialists clearly defined implementation ownership, technical objectives and acceptance criteria.
- Use isolated branches or worktrees where appropriate.
- Redeploy specialists dynamically as assignments finish or become blocked.
- Delegate corrective follow-up work back to the responsible specialist.
- Retain central authority over architectural decisions, shared contracts, integration and final disposition.
- Avoid duplicated investigation and competing implementations.

The orchestrator should intervene directly where its reasoning or integration authority provides genuine additional value.

## Context conservation

Treat the orchestrator's conversation length as a scarce engineering resource.

Specialists should maintain detailed technical findings, implementation records and qualification evidence in durable repository locations.

Their reports to the orchestrator should be compact and structured, containing:

- Accomplished work.
- Exact source identities.
- Important findings and decisions.
- Qualification results.
- Outstanding blockers.
- Recommended next actions.

Avoid transferring enormous logs, full source files or repetitive evidence into the orchestrator's context.

Maintain one concise mission ledger containing current priorities, specialist assignments, integration checkpoints and remaining work. Ensure that interruption or context exhaustion does not cause completed engineering to be lost.

## Execution budget

**Target completion: 4 hours 15 minutes.**

**Hard operational closure deadline: 4 hours 30 minutes.**

Avoid approaching the approximately five-hour timeout observed in previous missions.

| Elapsed time | Principal activity |
|---|---|
| 0–25 minutes | Reconnaissance, architecture, delegation and baseline establishment |
| 25–135 minutes | Intensive parallel implementation and focused testing |
| 100–165 minutes | Incremental integration and cross-review |
| 145–225 minutes | Combined qualification and corrective work |
| 225–255 minutes | Final delivery and closure |
| 255–270 minutes | Contingency and mandatory handover |

These phases should overlap productively rather than operate as rigid sequential barriers.

At 2h30, cease speculative development.

At 3h, freeze substantial architectural changes and concentrate on remaining acceptance defects.

At 4h, prioritise qualification, packaging, publication and durable recovery.

At 4h30, conclude with the strongest verified deliverable available and an honest account of any remaining blockers.

Do not artificially prolong completed work.

## Scope discipline

Distinguish explicitly between:

- Mandatory current-mission objectives.
- Desirable improvements.
- Conditional stretch goals.
- Deferred successor development.

Make the current implementation dependable before attempting its ambitious successor.

Exercise architectural foresight without prematurely implementing future complexity. Preserve useful extension points and record empirically established bottlenecks and promising future approaches.

Authorise architectural restructuring where justified by demonstrated problems, not merely because a theoretically superior architecture is conceivable.

Do not allow speculative improvements to jeopardise delivery of the primary objective.

## Qualification and integration

Begin qualification incrementally during implementation. Do not leave expensive CI, platform testing or packaging until the final hour.

Recover existing useful implementations and trustworthy evidence rather than repeating completed investigations.

Use independent cross-review, targeted regression, representative practical workloads and source-matched qualification.

Preserve negative findings and distinguish measured results from assumptions.

Never weaken correctness or acceptance criteria merely to finish within the time budget.

Publish useful checkpoints throughout the mission.

## Completion and delivery

Define completion in terms of actual working deliverables, not the volume of implementation, investigation or documentation produced.

Complete the authorised integration, qualification and delivery process wherever achievable.

Provide exact source identities, test results, artifact links and concise operating instructions.

Explicitly distinguish technical qualification, physical owner acceptance and merge authorisation.

If complete success becomes impossible within the available budget, preserve the strongest coherent implementation, verified evidence and immediately actionable recovery instructions.

Do not create another extensive audit or recovery programme simply to explain why the original work remains unfinished.

**Delegate aggressively. Conserve orchestrator context. Maintain productive parallelism. Converge progressively. Deliver working results before the execution deadline.**
