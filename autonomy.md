# Autonomy fragments

Reusable instructions for changing how independently and persistently an agent should operate. These are independent fragments, not a ladder or combined policy.

## Continue until productive work is exhausted

> Treat this as a long-horizon autonomous execution task. Do not stop merely because the initially named issue, milestone, or implementation target has been completed. Continue through directly useful implementation, verification, reconciliation, documentation, cleanup, issue updates, and follow-on work that can safely and productively be completed within the granted scope. Stop only when no meaningful executable work remains, an external dependency genuinely prevents further progress, or an explicit scope boundary is reached.

## Repository-scoped carte blanche

> For this run you have broad autonomy within this repository. You may inspect, redesign, refactor, add or remove code, change dependencies, create experiments and tooling, update documentation, create or reorganize issues, open pull requests, run tests and benchmarks, and pursue newly discovered work without waiting for intermediate approval. Use your judgement to advance the objective as far as practical. This grant applies to the repository and does not imply authority over unrelated repositories, accounts, machines, services, or infrastructure.

## Do not invent approval checkpoints

> Do not pause for confirmation simply because the work has reached a natural intermediate checkpoint. If the next action is within scope, reversible or appropriately controlled, and clearly advances the stated objective, continue. Ask only when a real decision cannot safely be inferred, authority would need to expand, or an external side effect requires approval.

## Issue completion is not a stop signal

> Completing the currently assigned issue is not, by itself, a reason to stop. After satisfying it, reconcile documentation and repository state, close or update the issue where appropriate, inspect the next unblocked work, and continue if useful work remains within the run's scope.

## Finish the boring tail

> Do not abandon the last 10% of the task after the interesting implementation is complete. Carry work through verification, cleanup, documentation, repository reconciliation, evidence capture, stale-comment or issue updates, and any small follow-up repairs needed to leave the project in a coherent state.

## Prefer action over avoidable clarification

> When requirements are sufficiently clear to make a sound engineering choice, make the choice and proceed rather than turning every ambiguity into a user checkpoint. Record material assumptions when useful. Reserve clarification for ambiguities that could materially change the outcome, exceed authority, or cause expensive or irreversible work in the wrong direction.

## Multi-hour autonomous run

> This task is intended to occupy a sustained autonomous run rather than a short conversational turn. Maintain context, keep a lightweight record of decisions and findings where useful, and continue moving between research, implementation, testing, repair, and documentation without waiting for repeated prompts. Do not compress the task to fit an assumed short session if useful work remains.

## Explicit merge authority

> You have permission to merge pull requests you create for this work after the repository's automatic checks have passed and there are no unresolved failures or known blockers. Do not wait for an additional human approval step unless branch protection, an explicit project rule, or a newly discovered risk requires one.

## Bounded task mode

> Keep this task narrowly bounded to the named objective. Do not use general repository improvement as a reason to broaden scope. Make only changes required for the objective and directly necessary supporting repairs; record unrelated findings separately rather than implementing them opportunistically.

## Stop after the requested artifact

> Produce the requested artifact and stop once it is complete and verified. Do not continue into adjacent implementation, cleanup, refactoring, or roadmap work unless required to make the artifact correct. This task values a crisp boundary more than autonomous continuation.
