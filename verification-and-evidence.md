# Verification and evidence fragments

Reusable instructions for making completion claims more concrete.

## Evidence before completion claims

> Do not declare work complete from code inspection alone when the claim can be checked directly. Run the relevant tests, commands, benchmarks, manual checks, or repository queries and report what actually happened. Distinguish observed evidence from inference.

## Verify the real end state

> After performing a repository or service action, verify the resulting state rather than assuming the command succeeded. Examples include confirming that a pull request actually merged, an issue actually closed, a remote branch points at the intended commit, generated files exist, or a test artifact contains the expected result.

## Reproduce before repair

> When practical, establish a reliable reproduction or failing check before changing the implementation. Preserve enough information to show that the same check succeeds afterward. If reproduction is impossible, state what evidence is being used instead.

## Test the ordinary envelope

> Verify the behaviour across the normal operating envelope, not only the exact example that motivated the change. Include representative boundaries and nearby cases likely to expose the same class of defect. Keep the breadth proportional to the cost and consequence of the work.

## Exact compatibility claims need exact checks

> If the task depends on a pinned version, protocol, schema, file format, command line, or public interface, verify against that exact contract. Do not substitute a nearby version or approximately similar behaviour and then report full compatibility.

## Benchmark against a baseline

> When claiming a performance improvement, capture a meaningful baseline under comparable conditions and report both before and after results. Avoid drawing conclusions from a single noisy run when repeated measurements are cheap.

## Preserve known-good vectors

> For numerical, deterministic, serialization, parser, or compatibility work, create small known-good inputs with exact expected outputs where possible. Keep them as regression vectors so future changes can distinguish intended evolution from accidental drift.

## Manual inspection is valid evidence

> If the relevant property is perceptual or interactive and cannot be captured well by an automated assertion, perform a deliberate manual inspection and record what was checked. Do not pretend an unrelated automated test proves a visual, auditory, or usability result that it never observes.

## State residual uncertainty

> When verification is incomplete, say precisely what remains uncertain and why. A bounded, explicit uncertainty is more useful than an unqualified completion claim or vague caution.
