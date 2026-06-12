# Transport Simulation Journal Template

Use this reference for traffic engineering, autonomous driving, AV/CAV, mixed traffic, car-following, lane-changing, bottleneck, merging, SUMO, VISSIM, Aimsun, trajectory-data, or microsimulation manuscripts.

## 1. Pre-Writing Brief

Before drafting, produce this brief:

```text
Target article type:
Target audience/journal family:
Central claim in one sentence:
Research questions:
Core contribution:
Main scenarios/data:
Main comparisons:
Primary metrics:
Main evidence clusters:
Reference strategy:
Boundary not to overclaim:
Material to move out of main text:
```

If the central claim cannot be written in one sentence, the manuscript is not ready for full drafting.

## 2. Common Journal Structure

For non-review empirical/simulation transport papers, use IMRaD by default:

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

Add a separate Literature Review / Related Work section only when the target journal requires it or when AV/CAV behavior assumptions, traffic-flow mechanisms, or model families are too complex to synthesize inside the Introduction. If added, it must explain why the present experiment is needed, not summarize every paper read.

Some journals combine Results and Discussion. Use a combined section only if each subsection can report a result and immediately interpret it without duplicating a later discussion.

## 3. Section Content

### Introduction

Typical flow:

1. Practical/scientific problem.
2. What the literature already knows.
3. Why existing results diverge or remain incomplete.
4. Research questions.
5. Contributions.

For Chinese transport-simulation manuscripts, this can be written as a funnel: broad but relevant traffic problem -> focused literature synthesis -> unresolved mechanism/scenario/metric problem -> research objective -> compressed Methods overview covering simulation platform, scenarios, vehicle/behavior groups, variables, and evaluation logic.

For AV/CAV traffic-flow papers, useful gap types include:

- AV/CAV behavior assumptions are treated as homogeneous.
- Penetration rate is studied without separating behavior mechanism or spatial distribution.
- Results from ring roads, basic segments, bottlenecks, and merging scenarios are not clearly connected.
- Efficiency metrics are used without checking completion, residual vehicles, or safety/comfort proxies.
- Realistic ACC/AV findings conflict with idealized CAV findings.

### Literature Review / Related Work, If Used

Organize by mechanism, not by paper:

1. AV/CAV impacts on traffic efficiency and stability.
2. Car-following behavior, headway, minimum gap, randomness, and capacity.
3. Driving style, conservative/aggressive/cooperative behavior, and control objectives.
4. Penetration rate, platooning, spatial distribution, and local vehicle combinations.
5. Bottleneck, merging, intersection, and lane-changing scenarios.
6. Multi-objective metrics: throughput, delay, travel time, completion, safety, comfort, emissions.

Use representative high-value papers. Do not force every read paper into the main review.

### Methodology and Experimental Design

This section should let a reviewer judge fairness and reproducibility.

For traffic simulation papers, write Methods as **study object plus simulation procedure**:

- Study object: road network/scenario, vehicle or agent classes, traffic demand, behavior model, and comparison groups.
- Simulation procedure: how scenarios are generated, which variables change, which variables are controlled, how outputs are collected, and how metrics are summarized.

Include:

- Simulation platform and version.
- Road network or site/scenario design.
- Vehicle types and behavior model.
- Parameter table with rationale or source.
- Demand levels and penetration rates.
- Spatial distribution or route generation logic.
- Random seeds, simulation duration, warm-up, and aggregation period.
- Experiment matrix.
- Metrics and formulas/definitions, including symbols, units, aggregation periods, and completion/residual-vehicle handling when relevant.
- Validity checks: collisions, teleporting, lane-change counts when relevant, completion/residual vehicles, seed robustness.

Every demand level, penetration rate, vehicle distribution, parameter level, and comparison group needs a rationale. Use rationales such as traffic state coverage, mechanism isolation, literature/empirical range, upper-bound logic, or sensitivity/ablation design.

Use tables and schematics for parameters, scenario geometry, experiment matrices, and data-processing flow. Prose should explain why the design isolates the target mechanism.

When Methods includes a workflow figure, network schematic, scenario diagram, parameter table, or experiment matrix, do not let it stand alone after a heading. First state what design decision or reproducibility question the visual answers; after the visual, explain the key modules, variables, controlled factors, or boundaries needed for the reader to use it.

### Results

Organize by research question and evidence clusters:

1. Main efficiency outcome.
2. Mechanism or scenario-specific result.
3. Penetration/spatial-distribution/sensitivity result.
4. Robustness or supplementary diagnostic.

For each result subsection:

```text
Question or claim -> evidence cluster -> main observation with numbers -> comparison to baseline -> short interpretation -> local boundary.
```

Avoid describing every metric or every figure. Use the few metrics and figures needed to answer the question. If several figures show the same pattern across average speed, travel time, throughput, or robustness checks, synthesize them as one evidence cluster instead of writing separate figure-by-figure paragraphs.

For each main Results figure or table, use `lead-in -> visual/evidence cluster -> uptake`: introduce the question or comparison before the visual, then interpret the key trend, number, anomaly, or boundary after it. Do not start a result subsection with a figure/table or place several visuals back-to-back without prose that frames and interprets them.

### Discussion

Discussion should not re-report tables. It should explain:

- Why the main pattern occurred.
- Why findings agree or conflict with prior literature.
- What the results imply for simulation modeling or AV/CAV deployment assessment.
- Which assumptions limit generalization.
- Which future work follows directly from those limits.

For AV/CAV simulation, common boundaries:

- Parameterized AV/CAV behavior is not a real vehicle product.
- CAV 100% is an upper-bound or idealized scenario.
- Passenger-car-only assumptions exclude truck effects.
- Fixed HDV behavior excludes human adaptation.
- Perfect communication excludes delay, packet loss, and control degradation.
- Safety/comfort proxies are not crash-risk estimates.

State each boundary where it matters. Do not repeat the full list in every section.

### Conclusions

Use a short cap plus a compact set of supported findings. For high-level
journal style, use compact paragraphs by default rather than numbered findings:

Opening paragraph: restate the traffic problem, simulation/data method, and main scenarios or comparisons.

Middle paragraph(s): synthesize the main answer, strongest quantitative result, mechanism/condition, and practical/modeling implication as coherent prose. Use only as many findings as the evidence supports; short/single-experiment papers may need fewer, and complex papers may need more.

Closing paragraph: state the most consequential boundary and direct future direction.

Use numbered findings only when the user explicitly asks for numbered conclusions,
the provided target journal/template explicitly requires them, or the output is
for a thesis/course report that requires enumerated findings. Do not infer
numbering merely because the manuscript is a Chinese, engineering, applied, or
traffic-simulation paper.

Do not introduce new citations, methods, or data.

## 4. Main Evidence and Figure/Table Chain

Transport simulation journal papers usually need a clear evidence chain. Use figures and tables to support claims, not as a required sequence to be narrated one by one:

| Evidence role | Possible item | Purpose |
|---|---|
| Study design | Figure or table | Research framework, scenario logic, network schematic, parameters, or experiment matrix |
| Primary efficiency claim | Figure/table cluster | Main efficiency result versus baseline, using only the metrics needed for the claim |
| Mechanism or scenario contrast | Figure/table cluster | Scenario transfer, bottleneck/merge/intersection comparison, or fundamental diagram |
| Robustness and boundary | Table/figure/supplement | Robustness, safety/comfort proxy, emissions, sensitivity, or supplementary diagnostic |

Only keep figures in the main text if they support a core claim. Similar line charts, secondary metrics, and exploratory checks belong in supplements or compact tables unless they change the main interpretation.

Every retained figure/table should have a manuscript anchor: a preceding sentence or paragraph that tells the reader why to inspect it, and a following sentence or paragraph that states what it contributes to the argument. This applies to Introduction frameworks, Methods schematics/tables, Results evidence, and Discussion synthesis visuals.

## 5. Reference Strategy

Use references by job:

- Introduction: 3-8 high-value references establishing importance, disagreement, and gap.
- Literature review: representative technical and review papers by theme.
- Methods: cite simulation platform, car-following/lane-changing model, calibration source, or metric source.
- Results: usually light citation unless comparing with prior findings.
- Discussion: cite papers that explain agreement, disagreement, or boundary conditions.

Avoid long citation chains that do not change the argument.

## 6. Reviewer-Attack Checklist

Before finalizing, answer:

- Are AV/CAV parameters justified or clearly framed as scenarios?
- Is the baseline fair?
- Are demand levels and geometry explained?
- Are stochastic seeds and aggregation rules reported?
- Are metric formulas, symbols, units, and inclusion rules defined where prose would be ambiguous?
- Does average travel time ignore unfinished vehicles?
- Are throughput, completion, and residual vehicles interpreted together?
- Are Results written around research questions/evidence clusters rather than a sequence of figure numbers?
- Are figures/tables anchored by prose before and after the visual rather than placed immediately after headings or back-to-back?
- Are similar speed, travel-time, throughput, robustness, or safety-proxy plots synthesized rather than narrated separately?
- Does any claim confuse car-following effects with lane-changing or merging effects?
- Is an upper-bound CAV scenario clearly labeled?
- Are safety/comfort proxies framed as diagnostics, not crash-risk conclusions?
- Are sensitivity or ablation results sufficient to support mechanism claims?
