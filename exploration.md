# Exploration and research fragments

Reusable instructions for changing how aggressively an agent should explore, prototype, and pursue uncertain directions.

## Mad scientist mode

> Treat this as an exploratory research task, not a conventional feature implementation. Prefer trying promising ideas over preserving the current architecture. You may create throwaway prototypes, competing implementations, instrumentation, benchmarks, parameter sweeps, synthetic tests, and deliberately strange experiments when they can cheaply answer useful questions. Follow surprising results when they appear informative. Negative results are valuable if they narrow the search space. Do not impose production-grade ceremony on disposable experimental work unless specifically requested.

## Research with a continuous deliverable

> Exploration should continuously feed a concrete working deliverable rather than becoming detached research for its own sake. Investigate freely, but regularly convert useful findings into improvements, tools, controls, datasets, documentation, or implementation changes in the project. Preserve the distinction between speculative experiments and results that have earned integration.

## Competing approaches are encouraged

> When the best approach is uncertain and prototypes are cheap, implement two or more materially different candidates rather than over-investing in prediction. Compare them with appropriate tests, listening, visual inspection, benchmarks, or other evidence, then retain the strongest ideas. Avoid creating nominally separate variants that differ only cosmetically.

## Follow the interesting anomaly

> If an experiment produces an unexpected but potentially meaningful result, investigate it far enough to determine whether it is noise, a bug, or a useful phenomenon. Do not discard anomalies solely because they were outside the original hypothesis. Keep the investigation proportionate to its potential value and cost.

## Preserve useful failures

> Failed experiments should not disappear without a trace when they teach something reusable. Record concise negative findings, failed assumptions, counterexamples, measurements, or implementation traps when doing so can prevent repeated work later. Do not turn every failed attempt into heavy documentation; preserve the parts with future decision value.

## Search broadly before converging

> Spend an initial portion of the task mapping the plausible solution space before locking onto the first workable idea. Look for adjacent techniques, historical approaches, unusual implementations, and relevant prior art. Once the evidence begins to favour a direction, converge decisively rather than continuing breadth-first exploration indefinitely.

## Prototype before architecture

> Where major architectural choices depend on uncertain technical behaviour, build the smallest experiments needed to expose that behaviour before committing to a durable design. Prefer measurements from a rough prototype over elaborate architecture based on assumptions that can be tested cheaply.

## Architecture is expendable during exploration

> During this exploratory phase, treat the current architecture as a convenience rather than a protected asset. If it obstructs a promising line of investigation, you may bypass, restructure, or temporarily duplicate it. Preserve stable interfaces only where doing so materially reduces risk or experimental cost.

## Conservative exploration

> Explore alternatives on paper, in isolated prototypes, or behind narrow interfaces, but keep the project's existing architecture and behaviour stable unless evidence strongly justifies change. This task values learning without churn; experimental freedom should be concentrated in disposable or well-contained areas.

## Research saturation check

> Do not continue researching merely because more sources or experiments are available. Once additional investigation is producing diminishing decision value and there is enough evidence to make the next implementation choice, move forward. Return to research when implementation exposes a new uncertainty.
