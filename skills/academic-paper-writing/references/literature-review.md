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

- Research object: behavior, system performance, safety, emissions, control, policy.
- Method: empirical data, simulation, analytical model, machine learning, optimization, field test.
- Scenario: freeway, urban network, intersection, bottleneck, merging, mixed traffic.
- Vehicle assumption: HDV, AV, CAV, ACC/CACC, heterogeneous behavior.
- Outcome: capacity, travel time, stability, safety surrogate, emissions, equity.
- Evidence scale: microscopic behavior, link-level capacity, network-level MFD, system-level policy.

## Paragraph Template

```text
Studies on [theme] have shown [established finding]. For example, [group of papers] typically [method/scenario]. These studies are useful because [value]. However, they often assume [limitation] or do not distinguish [missing mechanism]. As a result, it remains unclear whether [specific unresolved question].
```

## Comparing Literature

When papers disagree, do not simply say results are inconsistent. Explain likely sources:

- Different AV behavior assumptions.
- Different penetration rates.
- Different road geometry or demand state.
- Different car-following/lane-changing models.
- Different metrics: throughput vs travel time vs speed vs completion rate.
- Different calibration or lack of empirical validation.

## Common Mistakes

- Listing papers one by one without synthesis.
- Saying “few studies have examined...” without specifying what exact combination is missing.
- Treating all AV studies as equivalent.
- Ignoring negative, non-monotonic, or scenario-dependent findings.
- Using review papers as substitutes for technical evidence.

## Strong Gap Sentence Forms

- “What remains less clear is not whether [broad topic] matters, but how [specific mechanism] changes [specific outcome] under [specific condition].”
- “Existing studies have compared penetration rates, but they often do not separate [behavior type A] from [behavior type B].”
- “This makes it difficult to determine whether reported efficiency gains arise from [mechanism 1], [mechanism 2], or [scenario condition].”
