# Experiment and Methodology Writing

## Method Section Job

The methods section lets a skeptical reader reproduce the evidence and judge whether comparisons are fair.

For Materials and Methods, make two things explicit:

1. **Study object/material**: what is being tested, modeled, measured, or compared.
2. **Study procedure/method**: how conditions are created, variables are controlled, data are produced, and results are processed.

Do not write Methods as software narration or equipment inventory. The section should explain why the design can answer the research question.

For engineering manuscripts, Methods should make a three-part logic visible:

```text
Design/procedure: what was built, tested, simulated, modeled, or compared.
Rationale: why the chosen conditions, parameters, controls, modules, or baselines are appropriate.
Validation role: how the design supports reproducibility, fair comparison, mechanism isolation, robustness, or application assessment.
```

If a paragraph only lists tools, software commands, instruments, modules, or parameter values without explaining rationale or validation role, convert the list into a table and use prose to explain the design logic.

## Essential Elements

For simulation or experiment papers, report:

- Study objective and hypotheses or research questions.
- Platform/tool/version when relevant.
- Network/site/scenario design.
- Agent/vehicle/entity types.
- Parameters and their source or rationale.
- Independent variables.
- Controlled variables.
- Demand/input conditions.
- Random seeds and repetitions.
- Warm-up, simulation duration, sampling interval.
- Metrics and formulas, with symbols, units, aggregation scope, and calculation rules defined when needed.
- Data processing and statistical summaries.
- Validity checks: collisions, missing data, convergence, completion, robustness.

## Study-Type Templates

### Physical / Experimental Studies

Use this order when the work is based on laboratory, field, vehicle, equipment, or material tests:

```text
Test object/material and equipment.
Test conditions and controlled variables.
Test procedure or cycle.
Measurement and error handling.
Data processing and statistical analysis.
```

### Simulation / Modeling Studies

Use this order when the work is based on simulation, numerical modeling, microsimulation, or scenario experiments:

```text
Model/platform and version.
Model structure, validation, or scenario basis.
Parameter settings and rationale.
Simulation scenarios and operating conditions.
Experiment matrix and control variables.
Output metrics and result-analysis method.
Validity, robustness, sensitivity, or ablation checks.
```

### Algorithm / Method Papers

Use this order when the contribution is an algorithm, model, calibration method, control strategy, optimization method, or evaluation framework:

```text
Problem definition and notation.
Assumptions and scope.
Model, algorithm, or framework modules.
Objective functions, constraints, losses, or decision rules when needed.
Training/calibration/solution procedure.
Baselines and comparison fairness.
Evaluation protocol, metrics, ablation, sensitivity, and robustness checks.
Complexity, reproducibility, or implementation details only when they affect interpretation.
```

Do not hide the method contribution inside implementation details. Each module should state its design purpose, input/output, and role in supporting the claim.

### Engineering System / Application Studies

Use this order when the contribution is a prototype, platform, workflow, engineering system, deployment scheme, or application assessment:

```text
Engineering requirement or design constraint.
System architecture and module responsibilities.
Implementation or deployment setup.
Input/output interfaces and operating conditions.
Evaluation scenario, baseline, and performance criteria.
Failure modes, robustness checks, and practical boundaries.
```

A system paper should evaluate the claims implied by the system design: performance, reliability, usability, scalability, safety, cost, or deployment feasibility. Do not treat a screenshot, workflow diagram, or module list as evidence by itself.

## Condition Rationale Rule

Every scenario, demand/input level, parameter level, comparison group, and test condition should have a rationale. Acceptable rationales include:

- Literature or empirical range.
- Engineering or regulatory range.
- Coverage of free-flow, near-capacity, and oversaturated states.
- Mechanism isolation or control of a confounder.
- Sensitivity, ablation, or robustness testing.
- Upper-bound, lower-bound, baseline, or reference-case logic.

Avoid relying on “previous studies used this” as the only reason unless the condition is also relevant to the current research question.

## Recommended Tables and Schematics

Use tables or schematic figures for details that would otherwise become dense prose:

- Study object, equipment, model, or vehicle/entity settings.
- Scenario geometry, network/site layout, or test setup.
- Parameter settings and sources/rationales.
- Experiment matrix, condition levels, and controlled variables.
- Data processing flow, metric definitions, and statistical summaries.

## Control-Variable Logic

When simplifying, explain why:

```text
To isolate [target mechanism], this study controls [confounder] by assuming [simplification]. This design does not represent [excluded factor], which is treated as a limitation/future extension.
```

This is stronger than apologizing for every simplification.

## Experiment Matrix Template

| Dimension | Levels | Purpose |
|---|---|---|
| Scenario | ... | Tests transfer across contexts |
| Behavior type | ... | Separates mechanism assumptions |
| Penetration rate | ... | Tests threshold/nonlinearity |
| Demand | ... | Covers free-flow, near-capacity, oversaturated states |
| Seed | ... | Captures stochastic variation |
| Sensitivity | ... | Tests parameter dependence |

## Writing Baselines

Every experiment needs a clear baseline:

- Baseline should be plausible, not a strawman.
- Explain why it is the reference.
- Use relative changes only after reporting absolute values.
- For upper-bound cases, label them as upper bounds.

For algorithm, model, and engineering system papers, baselines should match the claim:

- If claiming accuracy or performance, compare with accepted methods or current practice.
- If claiming robustness, test harder conditions or perturbations.
- If claiming efficiency, report runtime, resource use, cost, or operational burden.
- If claiming practical value, include a realistic scenario, workflow, or application constraint.

## Metrics Writing

Define metrics before interpreting them:

- Throughput: completed vehicles per unit time.
- Completion ratio: completed vehicles divided by generated demand.
- Travel time: average over completed vehicles; mention possible survivor/completion bias.
- Residual vehicles: vehicles still waiting or running at simulation end.
- Speed/density/flow: specify aggregation area and period.
- Safety surrogate: state that it is a proxy, not crash risk itself.

When a metric can be calculated in multiple ways, provide a formula or flag the calculation rule for author confirmation. For detailed equation, notation, symbol, and unit rules, use `engineering-equations-and-notation.md`.

## Sensitivity and Ablation

Use sensitivity analysis to support mechanism claims:

```text
If varying parameter X changes outcome Y while other parameters remain fixed, X is a plausible driver in this simulation setting.
```

Avoid:

```text
Parameter X is the real-world cause of Y.
```

Simulation sensitivity supports model-based mechanism, not universal causality.

Use ablation to support design claims:

```text
Removing module A reduces outcome B, suggesting that module A contributes to the claimed mechanism under the tested conditions.
```

Avoid using ablation as a decorative checklist. Each ablation should correspond to a design choice, mechanism, or reviewer concern.
