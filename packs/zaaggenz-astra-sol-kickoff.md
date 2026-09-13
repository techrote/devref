# ZaagGenZ — Astra/Sol Kickoff Fragment Pack

## Default operating posture

For specific projects such as zaaggenz, "mad scientist" mode should be the assumed default.

In addition to this I definately need to retain the ability to give specific projects or stages of projects, absolute carte blanche to run full steam ahead entirely autonomously for multiple hours. These kinds of situations would be almost exclusively Astra High or Sol Max tasks.

Zaaggenz in particular is a good candidate for carte blanche within it's repo, in some ways it is a REQUIRED candidate: in addition to the research carried out for the task, the project itself is an experiment in exploring the frontier of agentic self-guided research with a concrete continuous deliverable (the synthesis suite).

## Mad Scientist operating profile

I would now define **Mad Scientist** purely as an *operating/research profile*.

It means the agent should preferentially explore rather than conserve: form hypotheses, implement competing approaches, instrument things, benchmark them, generate weird prototypes, follow unexpected findings, discard failures, preserve useful negative results, exploit spare compute, create research notes and datasets, and continuously feed successful findings back into the concrete deliverable.

It also means **do not repeatedly stop merely because the next useful action was not spelled out in the original issue**.

## Carte blanche authority

**Carte blanche**, however, is an *authority grant*. Something like `authority=repo_sovereign` or `autonomy=carte_blanche`.

For an explicitly trusted Astra High / Sol Max task, that should mean the agent can operate continuously for the duration of the session without approval checkpoints: restructure architecture, create experiments, add or remove code, change dependencies, generate research material, modify documentation, create/reprioritise/close issues, create branches and PRs, run tests and benchmarks, reconcile its own findings, merge successful work where repository policy permits it, and move immediately to the next productive task.

The important boundary is then **scope**, not ceremony:

> **You own this repository for this run. Keep going until there is no productive executable work left.**

That is materially different from giving an untrusted worker broad machine/account authority.

## ZaagGenZ as the research experiment

Part of the experiment is:

> **Can a capable agent discover worthwhile research directions itself, investigate them rigorously enough to distinguish signal from nonsense, and continuously convert those discoveries into an increasingly interesting synthesis system?**

That requires surplus agency. If every excursion needs an issue, every surprising result requires permission to investigate, every architecture change requires independent review, and every experiment must have predetermined acceptance criteria, we would be destroying a substantial part of the experiment we are trying to run.

A failed experiment that produces a useful benchmark, negative result, new hypothesis, or reusable tool can be a successful Mad Scientist action even though it produced no shippable feature.

## Omnipanel is not ZaagGenZ policy

The only conclusion here is about **scope**:

> **Omnipanel specifications are specifications for Omnipanel. They are not a general-purpose development policy for agents working on unrelated projects.**

So concepts developed for Omnipanel—`steel`, independent-review requirements, blast-radius classifications, acceptance-gate semantics, worker trust assumptions, and so forth—must remain in an **Omnipanel-local namespace**. They should affect another project only if you explicitly decide to import a particular concept into that project's own rules.

ZaagGenZ is completely independent. Its development should derive authority from, in roughly this order, your instructions for that run, ZaagGenZ's own repository documentation/issues/policies, and the actual technical state of the project. **Omnipanel does not get a vote.**

## Specific failure mode to avoid

Given your instructions for a multi-hour autonomous ZaagGenZ run, an agent reaching some intermediate point after ~50 minutes and stopping because it inferred:

> `steel → independent review required → cannot continue`

from Omnipanel-derived concepts is precisely the behaviour that must be prevented. The problem isn't that the `steel` rule is necessarily wrong *inside Omnipanel*; it's that it crossed a project boundary without authority.

## No inferred cross-project governance

> **Never infer cross-project governance. Repository A's process, terminology, acceptance gates, review requirements, autonomy limits, or experimental classifications apply only to Repository A unless the user or Repository B explicitly adopts them.**

And specifically:

> **Knowledge of Omnipanel may inform understanding of Omnipanel; it must not constrain development of ZaagGenZ or any other unrelated project merely because it exists in conversational context or memory.**

## Default versus promotion-time conservatism

For ZaagGenZ specifically, I would treat **Mad Scientist + repo carte blanche as the default rather than an exceptional override**. More conservative review should enter when a particular output is being promoted into something whose correctness actually matters, rather than governing the entire exploratory process upstream.
