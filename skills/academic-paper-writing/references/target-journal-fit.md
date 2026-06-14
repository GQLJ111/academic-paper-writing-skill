# Target Journal Fit

Use this reference when adapting a manuscript to a journal family or deciding what writing style the paper should follow. Do not invent target-journal requirements; treat the archetypes below as heuristics and defer to the actual author guide when it is provided.

## 1. Fit Questions

Before revising for journal fit, identify:

```text
Target journal or journal family:
Main contribution type:
Evidence type:
Expected reader:
Required level of methodological rigor:
Expected article length:
What the journal likely values:
What the journal likely rejects:
```

## 2. Engineering Journal Archetypes

Most engineering venues fall into a few archetypes. Match the paper to the archetype, then adopt its emphasis.

### Mechanism / Phenomenon Journals

Likely values:

- New understanding of why a system, material, or process behaves as it does.
- Clear link between assumptions/conditions and observed outcomes.

Writing emphasis:

- Make the mechanism explicit and explain why findings differ from prior work.
- Keep conditions, specimens, and assumptions transparent.

Avoid:

- Treating idealized or single-condition results as universal predictions.
- Many cases without a mechanism.

### Theory / Methodology Journals

Likely values:

- Problem formulation, modeling rigor, analytical contribution, and generalizable insight.
- Equations/notation, assumptions, proofs or validation when the method carries the contribution.

Writing emphasis:

- Clarify model structure, assumptions, and why the method advances knowledge.
- Define key equations, symbols, units, objectives, or constraints when they carry the contribution.
- Use experiments to validate a method or theory, not just to report cases.

Avoid:

- A purely descriptive case study with weak methodological novelty.

### Algorithm / System / Transactions Journals

Likely values:

- Algorithms, systems, control, sensing, communication, optimization, implementation.
- Engineering validation, robustness, and comparative baselines.

Writing emphasis:

- Present method/system architecture clearly.
- Include baselines, ablation, sensitivity, and robustness.
- Make the technical contribution explicit.

Avoid:

- Long narrative literature review without technical payoff.

### Safety / Reliability / Risk Journals

Likely values:

- Failure, safety, reliability, risk, or human-factors evidence.
- Careful experimental design and cautious interpretation.

Writing emphasis:

- Define safety/reliability/risk metrics precisely.
- Avoid equating efficiency or performance with safety.
- Discuss failure and risk mechanisms.

Avoid:

- Strong safety/reliability claims from limited proxy metrics.

### Applied / Practice / Letters / Short-Format Journals

Likely values:

- Applied evidence, practical modeling, case studies, operations/policy insight, or timely short results.

Writing emphasis:

- Clear problem, reproducible method, practical interpretation.
- Less theoretical ambition is acceptable if the evidence is useful and scoped.

Avoid:

- Overstated novelty or overly broad generalization.

### Broad-Scope / Interdisciplinary Journals

Likely values:

- Complete structure, interdisciplinary framing, application context, accessible methods.

Writing emphasis:

- Clear motivation, full method, readable results, practical implications.

Avoid:

- Overly long generic background.
- Weak link between results and the application/impact claim.

## 3. Contribution-Type Fit

| Contribution type | Best-fit archetype |
|---|---|
| New mechanism/phenomenon insight | Mechanism/phenomenon journal |
| New model/method/control/theory | Theory/methodology journal |
| New algorithm/system/implementation | Algorithm/system/transactions journal |
| Failure, safety, reliability, or risk evidence | Safety/reliability/risk journal |
| Applied case study or evaluation | Applied/practice or letters journal |
| Full thesis chapter | Thesis structure first; later compress to journal form |

## 4. Adaptation Rules

- For mechanism journals, reduce generic background and strengthen causal/mechanism logic.
- For methodology journals, move problem formulation and method novelty earlier.
- For algorithm/system journals, strengthen baselines, ablation, and robustness.
- For applied journals, make the setup, reproducibility, and practical implications clearer.
- For safety/reliability journals, narrow performance claims and expand metric validity.
- For broad journals, keep structure accessible but remove filler.

## 5. Worked Example: Transport / Automation Families

The archetypes map onto real venue families. As one instantiation:

- Transportation Research Part C → mechanism/phenomenon archetype (ITS, automation, connected vehicles; make the transport/automation mechanism explicit; do not treat SUMO scenarios as field predictions).
- Transportation Research Part B → theory/methodology archetype (modeling rigor, formulation, generalizable insight).
- IEEE Transactions on ITS → algorithm/system archetype (architecture, baselines, ablation, robustness).
- Accident Analysis & Prevention → safety/reliability archetype (precise safety metrics; do not equate efficiency with safety).
- Transportation Research Record / Transportation Letters → applied/letters archetype (reproducible, practical, scoped).
- Sustainability / Applied Sciences → broad-scope archetype (accessible structure, clear application link).

For another field, find the venue that matches the archetype rather than copying these titles.

## 6. Fit Diagnosis Output

Use:

```text
Best target family:
Why it fits:
What must be strengthened:
What should be cut:
Risk if submitted as-is:
Recommended structure:
```
