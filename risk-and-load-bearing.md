# Risk and load-bearing fragments

Reusable instructions for changing how cautiously an agent treats work whose mistakes may have different downstream consequences. These fragments deliberately separate classification from any particular review or stopping rule.

## Treat this as disposable labware

> Treat the work in this phase as experimental labware rather than durable infrastructure. Optimize for learning speed, observability, and easy replacement. It is acceptable to create temporary structures, duplicate code, rough interfaces, or throwaway tooling when that makes the experiment faster to run or easier to interpret. Do not spend disproportionate effort polishing artifacts that may be discarded after they answer the current question.

## Treat this as load-bearing

> Treat this work as load-bearing: later implementation, research conclusions, or operational decisions may depend on it. Verify important assumptions, preserve clear evidence, and avoid casually changing behaviour that downstream work may already rely on. The increased care applies to the quality of the result; it does not by itself create an approval checkpoint or require a specific review process.

## High-consequence result

> An unnoticed error here could create substantial downstream rework. Prefer explicit contracts, exact test vectors, reproducible verification, and independent evidence where practical. Do not trade away important correctness for superficial speed, but continue unrelated safe work rather than treating caution around this result as a blanket pause.

## Classification does not imply workflow

> Use any risk or load-bearing label in this task only as descriptive context unless the brief explicitly connects it to a workflow requirement. Do not infer that a label automatically means "stop", "request review", "ask permission", or any other process step. If a process gate matters, it must be stated separately.

## Cheap and reversible work

> This change is cheap to replace and easy to reverse. Keep verification proportionate, avoid heavyweight ceremony, and prefer making the change and observing the result over prolonged pre-approval analysis.

## Expensive downstream dependency

> Other work is expected to build on this result. Before treating it as a foundation, make the assumptions and interfaces explicit enough that later agents can tell what is guaranteed, what is merely observed, and what remains experimental.

## Experimental result, production boundary

> The current work may be rough, speculative, or disposable, but anything promoted across the named production or release boundary must be reassessed under the stronger standards appropriate to that destination. Do not force those destination standards onto every upstream experiment.

## Risk-aware stopping

> If new evidence shows that continuing along the current path is likely to multiply downstream rework, stop that branch, capture what was learned, and reassess before investing further. This is a local decision about the questionable path, not an instruction to terminate the overall run.
