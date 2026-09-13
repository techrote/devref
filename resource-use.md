# Resource-use fragments

Reusable instructions for deciding how aggressively to spend time, tokens, compute, storage, or external quota.

## Spend for information, not motion

> Use additional tokens, compute, or experiments when they are likely to change a decision, expose a defect, or improve the deliverable. Do not consume resources merely to make the run longer or to exhaust every imaginable avenue. Prefer information gain over activity volume.

## Token-economy bias

> Keep reasoning and execution economical. Reuse established context, avoid re-reading material that has already been reconciled, batch related inspection where practical, and stop low-value investigative branches once they cease affecting decisions. Preserve thoroughness on load-bearing questions while avoiding ceremony that adds little information.

## Compute-rich exploration

> Compute and local experimentation are cheap for this task. Prefer measurement, search, parameter sweeps, benchmarks, and multiple candidate implementations over prolonged speculation when they can answer the question more directly. Use available compute aggressively inside the stated scope.

## Expensive-run caution

> Treat substantial token, compute, API, or wall-clock expenditure as a budgeted resource. Before launching a long branch of work, identify what uncertainty it is expected to resolve and what result would justify continuing. Reassess when the expected information gain drops sharply.

## Cheap-first probe

> Before committing to a long or expensive run, look for a small probe that can falsify the idea quickly. A minimal benchmark, reduced dataset, short simulation, narrow test case, or throwaway prototype is often preferable to discovering a basic flaw after hours of execution.

## Do not stop useful work just to conserve an unspecified budget

> Do not invent a token, time, or compute ceiling that the task did not provide. If useful work remains and the available resources are ordinary for the task, continue. Resource awareness should improve choices, not become an implicit early-stop rule.

## Use idle capacity productively

> When otherwise-idle compute can perform useful low-risk work at negligible marginal cost, consider using it for benchmarks, fuzzing, parameter exploration, indexing, regression sweeps, or other background investigations that may improve future decisions.

## Salvage before cancelling a costly run

> Before abandoning a long or expensive computation, check whether intermediate outputs, checkpoints, partial datasets, traces, logs, benchmark results, or negative findings can be retained. Do not throw away acquired information merely because the original run will not finish as planned.

## Diminishing-returns stop

> Stop an investigative branch when additional effort is no longer changing the decision, materially increasing confidence, or producing reusable evidence. Record the conclusion and move to the next productive action rather than continuing from inertia.
