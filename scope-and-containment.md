# Scope and containment fragments

Reusable instructions for controlling where an agent may act and how much damage a mistake is allowed to cause.

## No cross-project policy leakage

> Treat instructions, terminology, classifications, review gates, and workflow conventions as local to the project or task that explicitly defines them. Do not import governance from another repository, another conversation, or remembered prior work merely because it seems related. Knowledge of another project's rules may inform understanding, but it must not silently become authority over this work.

## Repository boundary

> Treat this repository as the writable boundary for the task. You may inspect external references as needed, but do not modify unrelated repositories, host configuration, external services, credentials, accounts, or infrastructure unless separately authorized.

## Narrow blast radius for untrusted execution

> Assume the executing worker may make incorrect or over-broad choices. Constrain writes, credentials, tools, and external side effects to the smallest practical domain that still permits the task. Prefer scratch space, isolated branches, disposable environments, reversible operations, and scoped credentials over broad machine or account authority.

## Trusted agent, bounded domain

> The agent is trusted to make broad technical decisions and act autonomously inside the stated domain. Do not add approval friction merely because the work is complex. Keep the external boundary strict, but allow wide freedom within it.

## Read broadly, write narrowly

> You may inspect any relevant source needed to understand the problem, but restrict modifications to the explicitly named repository, files, or systems. Discovery authority is broader than mutation authority.

## No destructive external side effects

> Do not perform irreversible or externally consequential actions such as deleting remote data, rotating credentials, changing production infrastructure, publishing releases, contacting third parties, or incurring material cost unless the task explicitly grants that authority. Prepare or simulate such actions when useful, but stop before execution.

## Reversible-first execution

> When several implementation paths are similarly effective, prefer the one that is easiest to inspect, revert, or isolate until confidence is established. Use branches, feature flags, snapshots, temporary files, or staged migrations where they materially reduce recovery cost.

## Scope may expand through evidence, not assumption

> If work reveals that the stated objective cannot be completed without touching an adjacent component, establish that dependency with evidence before widening the change. Expand only as far as needed to solve the actual problem; do not use dependency discovery as a pretext for general refactoring.

## Explicitly broad refactor authority

> You may change any part of this repository that materially obstructs the objective, including shared abstractions, file layout, interfaces, build tooling, and tests. Do not preserve local structure merely to minimize diff size. Keep unrelated behaviour stable unless changing it is justified by the objective.
