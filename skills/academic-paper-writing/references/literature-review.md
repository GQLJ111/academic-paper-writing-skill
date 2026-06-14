# Literature Review

## Purpose

A literature review is not a bibliography. It should classify what is known, compare how studies differ, identify why findings diverge, and lead to a precise research gap.

## Top-Journal Review Pattern

```text
Theme 1: what this stream established
Theme 2: what another stream added
Theme 3: where methods/scenarios/assumptions differ
Synthesis: what remains unresolved and why it matters for this paper
```

## Classification Axes

Choose axes that match the paper:

- Research object: behavior, performance, safety/reliability, efficiency, emissions, control, cost.
- Method: empirical data, simulation/numerical, analytical model, machine learning, optimization, lab/field test.
- Condition/scenario: operating conditions, load cases, scales, environments, or deployment contexts.
- Modeling assumption: homogeneous vs heterogeneous units, idealized vs realistic, steady vs transient.
- Outcome: accuracy, efficiency, stability, robustness, reliability, safety surrogate, energy, cost.
- Evidence scale: component-level, subsystem-level, system-level, or deployment/field-level.

(For a domain-specific axis set, instantiate these with the field's own terms; e.g., a traffic paper might use freeway/intersection/bottleneck/merging scenarios and HDV/AV/CAV vehicle assumptions.)

## Paragraph Template

```text
Studies on [theme] have shown [established finding]. For example, [group of papers] typically [method/scenario]. These studies are useful because [value]. However, they often assume [limitation] or do not distinguish [missing mechanism]. As a result, it remains unclear whether [specific unresolved question].
```

## Comparing Literature

When papers disagree, do not simply say results are inconsistent. Explain likely sources:

- Different modeling assumptions.
- Different parameter, load, or condition ranges.
- Different geometry, scale, or operating state.
- Different model families or solver/algorithm settings.
- Different metrics (e.g., efficiency vs accuracy vs reliability vs cost).
- Different calibration or lack of experimental validation.

## Common Mistakes

- Listing papers one by one without synthesis.
- Saying “few studies have examined...” without specifying what exact combination is missing.
- Treating all studies in a method family as equivalent.
- Ignoring negative, non-monotonic, or condition-dependent findings.
- Using review papers as substitutes for technical evidence.

## Strong Gap Sentence Forms

- “What remains less clear is not whether [broad topic] matters, but how [specific mechanism] changes [specific outcome] under [specific condition].”
- “Existing studies have compared [parameter levels], but they often do not separate [mechanism A] from [mechanism B].”
- “This makes it difficult to determine whether reported efficiency gains arise from [mechanism 1], [mechanism 2], or [scenario condition].”
