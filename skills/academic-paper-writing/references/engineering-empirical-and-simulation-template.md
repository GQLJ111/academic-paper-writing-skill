# Engineering Empirical and Simulation Manuscript Template

Use this reference for engineering manuscripts whose contribution is new evidence from experiments, tests, measurements, numerical/simulation studies, field data, or applied case studies. It applies across mechanical, materials, civil, electrical, control, automation, computer/AI, energy, chemical, and environmental engineering. Domain-specific instantiations (e.g., traffic simulation) are given as examples, not as the required content.

## 1. Pre-Writing Brief

Before drafting, produce this brief:

```text
Target article type:
Target audience/journal family:
Central claim in one sentence:
Research questions:
Core contribution:
Main study object / data / scenarios:
Main comparisons (baselines):
Primary metrics:
Main evidence clusters:
Reference strategy:
Boundary not to overclaim:
Material to move out of main text:
```

If the central claim cannot be written in one sentence, the manuscript is not ready for full drafting.

## 2. Common Journal Structure

For non-review empirical/experimental/simulation engineering papers, use IMRaD by default:

```text
Title
Abstract
Keywords
1. Introduction
2. Materials and Methods / Methodology and Experimental Design
3. Results
4. Discussion
5. Conclusions
References
Supplementary Material
```

Add a separate Literature Review / Related Work section only when the target journal requires it or when the relevant theory, model families, or competing methods are too complex to synthesize inside the Introduction. If added, it must explain why the present study is needed, not summarize every paper read.

Some journals combine Results and Discussion. Use a combined section only if each subsection can report a result and immediately interpret it without duplicating a later discussion.

## 3. Section Content

### Introduction

Typical flow:

1. Practical or scientific problem.
2. What the literature already knows.
3. Why existing results diverge or remain incomplete.
4. Research questions.
5. Contributions.

For Chinese engineering manuscripts, this can be written as a funnel: a broad but relevant problem -> focused literature synthesis -> the unresolved mechanism/condition/metric problem -> research objective -> a compressed Methods overview covering the study object, platform/equipment/data, comparison groups, variables, and evaluation logic.

Useful gap types for engineering empirical/simulation papers:

- A governing factor, mechanism, or parameter is assumed homogeneous when it is actually heterogeneous.
- A control variable, load level, or operating condition is studied without separating the underlying mechanism.
- Results from idealized, bench-scale, single-condition, or single-scenario settings are not clearly connected to harder or more realistic conditions.
- Performance is reported on one metric without checking completion, efficiency, reliability, cost, or safety trade-offs.
- Idealized model/simulation findings conflict with measured or field findings.

### Literature Review / Related Work, If Used

Organize by mechanism, method family, or research question, not by paper:

1. Established findings on the target phenomenon, performance, or behavior.
2. Modeling, measurement, or characterization approaches and their assumptions.
3. Design strategies, control objectives, or material/process choices.
4. Operating conditions, load cases, scenarios, or deployment contexts.
5. Multi-objective evaluation: accuracy, efficiency, stability, robustness, reliability, safety, cost, energy, emissions.

Use representative high-value papers. Do not force every read paper into the main review.

### Methodology and Experimental Design

This section should let a reviewer judge fairness and reproducibility.

Write Methods as **study object plus procedure**:

- Study object: the system, specimen, device, network, dataset, model, or process under study, plus the comparison groups.
- Procedure: how conditions are created, which variables change, which variables are controlled, how outputs are collected, and how metrics are summarized.

Include, when relevant to the subtype:

- Platform/equipment/instrument/software and version.
- Specimen/site/network/dataset/scenario design.
- Entity, component, agent, or material classes and their models.
- Parameter table only when repeated settings require lookup or comparison, with rationale or source.
- Independent variables, factor levels, load/demand/operating conditions.
- Controlled variables and how confounders are isolated.
- Random seeds, repetitions, sampling interval, warm-up, and run duration for stochastic or time-evolving studies.
- Experiment matrix.
- Metrics and formulas/definitions, including symbols, units, aggregation scope, and inclusion/exclusion rules.
- Validity checks: convergence, calibration, measurement error, missing data, completion, instability, and robustness.

Every condition level, factor level, comparison group, and parameter choice needs a rationale. Use rationales such as operating-state coverage, mechanism isolation, literature/empirical/standard ranges, upper-/lower-bound logic, or sensitivity/ablation design.

Use tables for repeated parameter or experiment-matrix fields when they improve lookup or comparison; use schematics for geometry, architecture, and data-processing flow when spatial or process relations matter. Keep simple facts in prose. Prose should explain why the design isolates the target mechanism.

When Methods includes a workflow figure, schematic, scenario/setup diagram, parameter table, or experiment matrix, do not let it stand alone after a heading. First state what design decision or reproducibility question the visual answers; after the visual, explain the key modules, variables, controlled factors, or boundaries needed for the reader to use it.

### Results

Use the evidence-cluster protocol in `results-and-discussion.md`. For an engineering paper, a useful default order is:

1. Baseline fairness and absolute performance.
2. Primary outcome supporting the central claim.
3. Mechanism, parameter, condition, or design-choice effect.
4. Robustness, sensitivity, ablation, or supplementary diagnostic.

Each subsection should follow:

```text
Question or claim -> evidence cluster -> main observation with numbers -> comparison to baseline -> short interpretation -> local boundary.
```

Use only the metrics and visuals needed to answer the question. Synthesize similar figures as one evidence cluster, and apply `lead-in -> visual/evidence cluster -> uptake` rather than starting a subsection with a display or placing visuals back-to-back.

### Discussion

Use the Discussion architecture in `results-and-discussion.md`. The engineering-specific discussion should explain:

- Why the main pattern occurred (mechanism).
- Why findings agree or conflict with prior literature.
- What the results imply for modeling, design, deployment, or practice.
- Which assumptions limit generalization.
- Which future work follows directly from those limits.

Common engineering boundaries to state where they matter (do not repeat the full list in every section):

- A parameterized or simulated model is not the physical system itself.
- Idealized 100%/perfect-condition cases are upper bounds, not predictions.
- Bench-scale, single-specimen, or single-site results may not transfer to full scale or other sites.
- Fixed operating assumptions exclude adaptation, wear, aging, or disturbance.
- Perfect sensing/communication/control excludes delay, noise, and degradation.
- Surrogate or proxy metrics are diagnostics, not direct measures of safety, reliability, or risk.

### Conclusions

Use the paragraph-style conclusion pattern in `top-journal-section-patterns.md`: restate the problem and scope, synthesize only the supported findings, then state the contribution/implication and most consequential boundary. Use numbered findings only when the user, target template, or thesis/course format explicitly requires them; do not infer numbering from a Chinese, engineering, or applied context.

Do not introduce new citations, methods, or data.

## 4. Main Evidence and Figure/Table Chain

Engineering empirical/simulation papers usually need a clear evidence chain. Use figures and tables to support claims, not as a required sequence to be narrated one by one:

| Evidence role | Possible item | Purpose |
|---|---|---|
| Study design | Figure or table | Research framework, setup/architecture schematic, scenario logic, parameters, or experiment matrix |
| Primary performance claim | Figure/table cluster | Main result versus baseline, using only the metrics needed for the claim |
| Mechanism or condition contrast | Figure/table cluster | Condition transfer, load-case comparison, ablation, or characteristic curve |
| Robustness and boundary | Table/figure/supplement | Robustness, sensitivity, uncertainty, proxy metrics, or supplementary diagnostic |

Only keep figures in the main text if they support a core claim. Similar charts, secondary metrics, and exploratory checks belong in supplements unless they change the main interpretation; use a compact table only when exact values or repeated comparisons remain necessary.

Every retained figure/table should have a manuscript anchor: a preceding sentence or paragraph that tells the reader why to inspect it, and a following sentence or paragraph that states what it contributes to the argument.

## 5. Reference Strategy

Use references by job:

- Introduction: 3-8 high-value references establishing importance, disagreement, and gap.
- Literature review: representative technical and review papers by theme.
- Methods: cite platform/instrument, models, standards, calibration sources, or metric definitions.
- Results: usually light citation unless comparing with prior findings.
- Discussion: cite papers that explain agreement, disagreement, or boundary conditions.

Avoid long citation chains that do not change the argument.

## 6. Reviewer-Attack Checklist

Before finalizing, answer:

- Are key parameters/assumptions justified or clearly framed as scenarios?
- Is the baseline fair and aligned with the claim?
- Are operating conditions, geometry/architecture, and load/demand levels explained?
- Are stochastic seeds, repetitions, and aggregation rules reported?
- Are metric formulas, symbols, units, and inclusion rules defined where prose would be ambiguous?
- Does any aggregate metric hide a boundary (e.g., an average over only completed/successful samples)?
- Are primary, secondary, and trade-off metrics interpreted together?
- Are Results written around research questions/evidence clusters rather than a sequence of figure numbers?
- Are figures/tables anchored by prose before and after the visual rather than placed immediately after headings or back-to-back?
- Are similar curves across conditions or metrics synthesized rather than narrated separately?
- Does any claim confuse one mechanism with another (e.g., attributing an effect to the wrong factor)?
- Are idealized or upper-bound cases clearly labeled?
- Are proxy/surrogate metrics framed as diagnostics, not direct conclusions?
- Are sensitivity or ablation results sufficient to support mechanism/design claims?

## 7. Domain Instantiation Example: Traffic / AV Simulation

The template above is domain-neutral. As a worked instantiation, a mixed-traffic AV/CAV microsimulation paper (SUMO/VISSIM/Aimsun) would fill it as:

- Study object: road network/scenario, vehicle classes (HDV/AV/CAV), demand, car-following/lane-changing behavior model, comparison groups.
- Independent variables: penetration rate, behavior type, spatial distribution, demand level, geometry.
- Metrics: throughput/flow, completion ratio, residual vehicles, average travel time (over completed vehicles), speed/density, safety/comfort surrogates.
- Key boundaries: parameterized AV/CAV behavior is not a real product; CAV 100% is an upper bound; passenger-car-only excludes truck effects; safety proxies are not crash-risk estimates; average travel time must be read together with completion ratio.
- Reviewer trap: do not confuse pure car-following effects with lane-changing or merging effects; label upper-bound scenarios; interpret throughput, completion, and residual vehicles together.

For other domains, instantiate the same slots with field-appropriate objects, variables, metrics, and boundaries (see `engineering-domain-examples.md`).
