# Engineering Equations and Notation

Use this reference when drafting or revising engineering, simulation, modeling, algorithm, or technical empirical manuscripts that involve formulas, equations, notation, metric definitions, model formulation, objective functions, constraints, units, or mathematical definitions.

## Purpose

Equations in engineering papers are not decoration. Use them when they make a method, metric, model, assumption, or data-processing step reproducible and unambiguous.

Do not force equations into sections that are already clear in prose. Do not omit equations when prose cannot define the calculation, model, constraint, or metric precisely enough for a peer to reproduce it.

## Default Output Format

Unless the user asks for a file format, write equations in chat-ready Markdown with LaTeX math:

- Inline math: `$v_i(t)$`, `$q = N/T$`.
- Display math:

```markdown
$$
q = \frac{N}{T}
$$
```

Do not generate `.tex`, `.docx`, `.pdf`, numbered equation environments, or compiled artifacts unless the user asks for them. If the target manuscript is LaTeX, preserve existing labels, references, and equation environments.

## When To Add Or Request Equations

Actively check for equation needs in these cases:

- Model definitions: state variables, update rules, car-following/lane-changing models, control laws, prediction models, calibration equations.
- Metric definitions: throughput, completion ratio, delay, travel time, density, flow, speed, safety surrogate, comfort, emissions, error metrics, robustness scores.
- Data processing: aggregation, normalization, smoothing, filtering, weighting, statistical summaries, confidence intervals, missing-data handling.
- Optimization or control: objective functions, constraints, decision variables, feasible sets, penalty terms, reward functions.
- Algorithmic papers: loss functions, scoring rules, convergence criteria, complexity-related definitions.
- Validation: goodness-of-fit, error measures, sensitivity indices, ablation metrics, statistical tests.

For a simple descriptive metric, a prose definition may be enough. For any metric that can be calculated in more than one way, provide a formula or flag that the calculation rule needs author confirmation.

## Equation Writing Contract

Before or after each important equation, make these elements clear:

| Element | Requirement |
|---|---|
| Role | Say whether the equation defines a metric, model, constraint, objective, transformation, or validation measure. |
| Equation | Use clear LaTeX math; avoid unnecessary symbols or over-complex notation. |
| Symbols | Define every symbol at first use. |
| Units | Give units for dimensional quantities. |
| Scope | State indices, time windows, aggregation area, sample set, scenario, or boundary conditions. |
| Assumption | State simplifications that affect interpretation. |
| Manuscript link | Connect the equation to the method step, result, figure/table, or claim it supports. |

If the user has not provided the actual formula, do not invent one as fact. Either ask for the definition or present a candidate as an explicit assumption.

## Avoid Equation Dumping

Do not stack several display equations back-to-back without explanatory prose unless the manuscript is presenting a necessary derivation and each step changes the reasoning.

For journal-style engineering Methods, organize equations by method function:

- Sensitivity-analysis definitions.
- Core efficiency metrics.
- Stability, safety-proxy, or robustness metrics.
- Normalization or relative-change definitions.
- Model, objective, or constraint definitions.

Introduce each group with its purpose and scope, then define only the formulas needed for reproducibility. After the group, explain variables, units, data source, inclusion rule, and interpretation boundary. If many basic metrics are being defined at once, prefer a compact metric-definition table plus a few essential formulas rather than a long equation sequence.

Failure signs:

- The text says "computed as follows" and then lists three or more numbered equations without a paragraph-level purpose.
- Equation numbers become the structure of the method subsection.
- The symbol explanation is a long unreadable list because too many unrelated metrics were introduced together.
- Formulas are included to look technical even though a table or prose definition would be clearer.

## Notation Ledger

For formula-heavy sections, build a compact notation table before or alongside the draft:

| Symbol | Meaning | Unit | Scope/Index | Source/Value |
|---|---|---|---|---|
| `$q$` | Traffic flow / throughput | veh/h | Aggregated over time interval `$T$` | Derived from simulation output |
| `$N$` | Number of completed vehicles | veh | Completed within the analysis interval | Simulation output |
| `$T$` | Analysis duration | h | Excludes warm-up if applicable | Experiment setting |

Keep one symbol for one concept across the manuscript. Do not rename the same metric between Methods, Results, captions, and tables.

## Formula Prose Patterns

### English

```text
The [metric/model] is defined as:

$$
M = ...
$$

where ... denotes ..., measured in ...; ... represents ... . This definition is used to [method/result purpose], and it is interpreted within [scope/boundary].
```

### Chinese

```text
[指标/模型] 定义如下：

$$
M = ...
$$

式中，... 表示 ...，单位为 ...；... 表示 ...。该定义用于表征/计算/约束 ...，其适用范围为 ...。
```

For journal prose, keep the explanation compact. Avoid turning every formula into a textbook derivation unless the derivation is the paper's contribution.

## Common Engineering Patterns

### Metric Definition

Use when the paper reports a metric that reviewers may calculate differently:

```markdown
$$
C = \frac{N_\mathrm{completed}}{N_\mathrm{generated}}
$$
```

Then define numerator, denominator, unit or dimensionless status, analysis interval, and whether unfinished samples are excluded or counted separately.

### Model Or State Update

Use when a method has a reproducible mechanism:

```markdown
$$
x_{t+1} = f(x_t, u_t, \theta)
$$
```

Then define state, input/control, parameters, time step, assumptions, and whether `f` is empirical, learned, simulated, or derived from a cited model.

### Objective And Constraints

Use when the manuscript claims optimization, control, planning, calibration, or parameter fitting:

```markdown
$$
\min_{\theta} \; J(\theta)
$$

subject to

$$
g_k(\theta) \le 0,\quad k = 1,\ldots,K.
$$
```

Then define decision variables, objective meaning, constraints, feasible range, and how the solution is obtained.

### Aggregation Or Statistical Summary

Use when results depend on repeated runs, seeds, samples, time windows, or scenario aggregation:

```markdown
$$
\bar{y} = \frac{1}{R}\sum_{r=1}^{R} y_r
$$
```

Then define repetitions/seeds, sample inclusion rules, aggregation period, and whether uncertainty is reported.

## Traffic And Simulation Notes

For traffic simulation manuscripts, formulas are often needed for:

- Throughput or flow: define completed vehicles, aggregation interval, and units.
- Completion ratio: define generated demand, completed vehicles, and whether residual vehicles are reported separately.
- Average travel time: define whether only completed vehicles are included and flag completion bias.
- Density/speed/flow: define spatial segment, time interval, and aggregation rule.
- Safety/comfort proxies: define surrogate metric precisely and avoid calling it crash risk unless validated for that purpose.
- Penetration rate and vehicle class proportions: define numerator, denominator, and scenario scope.
- Random-seed summaries: define mean, variance, confidence interval, or robustness statistic.

When a metric can hide an important boundary, pair the formula with the boundary. For example, average travel time over completed vehicles should be interpreted together with completion ratio or residual vehicles.

## Do Not Invent Rule

Never fabricate:

- a physical law, control objective, reward function, constraint, or calibration formula not provided by the user or source material;
- parameter values, units, or variable meanings;
- equation numbers, citations, or labels for files the user has not provided;
- a complex equation merely to make the manuscript look more technical.

If a needed equation is missing, write one of these instead:

```text
The calculation rule for [metric] needs author confirmation before a formula can be finalized.
```

```text
Assuming [explicit calculation rule], the metric can be written as:
...
```

## Equation Audit Checklist

Before delivering a formula-heavy section, check:

- Does each equation have a clear manuscript role?
- Is every symbol defined at first use?
- Are dimensional units stated?
- Are indices, intervals, sets, and aggregation scopes clear?
- Is the equation referenced or explained in prose?
- Does the formula match the described experiment, figure, table, or result?
- Are assumptions and boundaries stated where they affect interpretation?
- Are candidate formulas clearly marked when author confirmation is needed?
- Has unnecessary mathematical decoration been removed?
- Are equations grouped by method decision or metric family rather than dumped as a consecutive list?
