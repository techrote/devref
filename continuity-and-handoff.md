# Continuity and handoff fragments

Reusable instructions for long-running work, context transfer, and picking up existing work without losing momentum.

## Leave a durable handoff

> If the work cannot be completed in the current run, leave a concise repository-native handoff that records the current state, what was changed, what was verified, what remains uncertain, and the exact next executable actions. Prefer durable files, issue comments, or pull request notes over relying on conversational memory.

## Handoff only when needed

> Do not create elaborate handoff material while the work is still actively progressing and likely to finish in the same run. Produce a handoff when context, session, authority, or an external dependency is genuinely about to interrupt execution.

## Continue from evidence, not narration

> When resuming prior work, inspect the actual repository state, commits, tests, artifacts, and issue history before trusting a prose handoff. Use the handoff to navigate, then confirm the important claims against durable evidence.

## Preserve the next action

> When stopping at a blocker, record the smallest concrete next action that would resume progress. Avoid vague endings such as "continue debugging" when a specific command, file, failing test, decision, or missing input is already known.

## Keep a research scratchpad when the search branches

> For long exploratory work with many hypotheses, maintain a lightweight scratchpad of tested ideas, observations, dead ends, measurements, and promising next branches. Optimize it for the next agent's retrieval, not for polished prose. Periodically promote durable conclusions into the project's canonical documentation and prune obsolete scratch notes when useful.

## Context reconstruction pack

> For a project expected to involve many independent agents or long gaps between sessions, create a compact reference pack containing the architecture, current state, key decisions, interfaces, verification commands, known traps, and active roadmap. Keep it concise enough to load routinely and detailed enough to prevent repeated archaeology.

## Do not let the handoff become a second specification

> A handoff describes the state of work; it should not silently replace the project's actual requirements, architecture, or issue authority. Clearly separate observations and suggested next steps from binding project decisions.

## Resume without ritual re-planning

> When prior work is already well documented and repository evidence supports the handoff, resume execution from the next unblocked task. Do not restart the entire planning process merely because a new agent or session has taken over.
