# Repository-work fragments

Reusable instructions for repository-native execution and cleanup.

## Read repository authority first

> Before implementing substantial changes, inspect the repository's own README, architecture notes, contribution guidance, issue state, recent relevant commits, and any agent or handover documentation that appears authoritative. Reconcile the task against the repository that actually exists rather than assuming the prompt contains the whole state.

## Repository-native completion

> Do not treat local code changes as the whole task. Where appropriate, carry the work through repository-native completion: tests, documentation, generated artifacts, commit history, pull request description, issue reconciliation, and verification of the resulting remote state.

## Do not redo completed work

> Inspect the current branch, commits, pull requests, issues, and existing artifacts before starting implementation. If work has already been completed and verified, continue from that state rather than recreating it. Reassessment should be proportional to evidence of uncertainty, not automatic.

## Reconcile issues after implementation

> After completing work, update the relevant issues so they accurately describe the resulting repository state. Close work that is genuinely complete, record residual blockers precisely, and avoid leaving stale issue text that will mislead the next agent.

## Keep implementation prompts executable

> When creating issues intended for future implementation agents, include enough repository context, objective, constraints, expected outputs, and verification instructions that the issue can be executed without reconstructing the entire planning conversation. Avoid vague issue bodies that merely restate a title.

## Preserve repository history when useful

> Prefer changes that leave a comprehensible history: focused commits, useful messages, and pull request descriptions that explain what changed and why. Do not over-fragment trivial edits, but make it possible for a future agent to recover the reasoning without the original chat.

## Verify merge and closure explicitly

> After merging a pull request or closing an issue, query the remote state and confirm the action actually occurred. Do not report success solely because a merge or update command returned without an obvious error.

## Repair first, tidy second

> When addressing a concrete defect, prioritize establishing and fixing the behaviour before broad cleanup. Once the repair is verified, perform only the cleanup that improves correctness, maintainability, or future diagnosis. Avoid burying a focused fix inside unrelated aesthetic refactoring unless the task explicitly invites it.

## Update documentation with code

> If a change alters interfaces, commands, assumptions, architecture, workflows, or operational behaviour that future contributors will rely on, update the relevant documentation in the same work. Do not leave known-stale guidance behind a correct implementation.

## Fresh-state verification

> When practical, verify the result from a clean or fresh state rather than relying entirely on an already-mutated development environment. This is especially useful for installation, packaging, migration, setup, generated files, and stateful configuration work.
