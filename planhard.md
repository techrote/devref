Review the relevant planning conversations and convert the resulting plan into a complete, implementable, and repository-native development workflow for username/repo using @GitHub 

This is intended to be a long-horizon autonomous execution task. Do not stop after reviewing, summarizing, or reformulating the plan. Continue through all applicable planning, documentation, issue-creation, reconciliation, and consistency-review stages in the same run.

Work through the following stages autonomously:

1. Thoroughly inspect and reconcile the relevant conversations.
2. Determine whether the plan is ready for implementation decomposition.
3. Identify and repair omissions, contradictions, weak assumptions, unsupported claims, missing research, missing dependencies, and untestable requirements.
4. Create any supporting RAG, research, architecture, decision, specification, or verification documents needed for future implementation agents.
5. Formulate a milestone and dependency hierarchy.
6. Determine which work can safely proceed concurrently and which work must be serialized.
7. Inspect the current repository and GitHub state before making changes.
8. Create or update the canonical project documentation.
9. Create or update the GitHub issues in username/repo
10. Review the resulting issue set for omissions, duplication, circular dependencies, unsafe concurrency, oversized tasks, missing acceptance criteria, and missing verification paths.
11. Correct all issues found during the review.
12. Perform a final repository-wide consistency pass.

Maintain an execution ledger in the repository or in the primary planning document. Do not consider the task complete while any applicable stage remains incomplete.

The goal is not merely to produce a plan. The goal is to leave the repository with a usable autonomous implementation workflow.

When creating issues:
- each issue must have a clear objective;
- include scope and non-goals;
- include dependencies and concurrency guidance;
- include all required context or links to canonical documents;
- include an implementation prompt for a future coding agent;
- include acceptance criteria;
- include verification instructions;
- include expected artifacts;
- include blocking and stopping conditions;
- avoid duplicating long canonical documentation unnecessarily.

Use repository documents as the source of truth for large shared material. Issues should contain the context needed to execute their individual task and should link to the relevant canonical documents.

When using research or reference material:
- distinguish requirements, preferences, research findings, design decisions, implementation tasks, assumptions, and speculation;
- record sources and unresolved questions;
- do not silently convert suggestions into requirements;
- do not invent citations, empirical results, or validation.

Treat the operation as repeatable and idempotent:
- inspect existing issues and documents first;
- update or reconcile existing artifacts rather than blindly duplicating them;
- preserve useful work;
- record significant changes to the plan;
- avoid creating duplicate milestones, issues, labels, or documents.

If an issue is blocked:
- record the blocker;
- identify dependent work;
- create a decision or research issue where appropriate;
- continue all independent work;
- do not stop the entire task unless the blocker invalidates the overall project.

After the first apparently complete pass, perform another independent review specifically looking for:
- missing work;
- hidden assumptions;
- broken dependencies;
- contradictory requirements;
- missing tests or verification;
- unsafe parallelism;
- issues that are too large to implement reliably;
- documentation that future agents would need but cannot currently find.

Use the available tools and session duration productively. Prefer making durable repository and GitHub changes over narrating routine reasoning. Do not ask for confirmation for ordinary planning, documentation, issue creation, inspection, or reconciliation actions. Ask only when an external permission, credential, destructive action, or genuinely irreconcilable product decision is required.

At the end, provide only a concise summary of:
- artifacts created or updated;
- issues created or updated;
- major decisions;
- unresolved blockers;
- verification or consistency checks performed.
