# Paper Quality Review

Use this reference to diagnose a draft before rewriting. Lead with structural issues, not sentence polishing.

## 1. Review Output Format

Use a compact table:

| Dimension | Score (1-5) | Main issue | Evidence in draft | Revision action |
|---|---:|---|---|---|

Scores:

- **5**: publishable or near-publishable.
- **4**: solid, needs focused improvement.
- **3**: usable but structurally weak.
- **2**: major revision needed.
- **1**: unclear or unsupported.

## 2. Core Dimensions

### Central Argument

Check:

- Can the paper be summarized in one sentence?
- Does every section serve that argument?
- Are there competing paper identities, such as thesis report vs journal article?
- Is the engineering subtype clear: experiment/test, simulation/numerical study, modeling/algorithm, engineering system/application, method comparison, or review?
- Does the section architecture match that subtype instead of forcing a generic template?

### Research Gap and Contribution

Check:

- Is the gap specific and testable?
- Does the paper explain why prior work does not already answer it?
- Are contributions intellectual, not just task lists?

### Literature Use

Check:

- Is literature synthesized by theme?
- Are references selected for argumentative function?
- Are review papers and technical papers used appropriately?
- Is there citation padding?

### Method and Reproducibility

Check:

- Are scenarios, parameters, baselines, demand, seeds, and metrics clear?
- Are necessary formulas, symbols, units, and aggregation rules defined for metrics, models, objectives, or constraints?
- Is the study object/material clear, and is the study procedure/method reproducible?
- Does Methods state design/procedure, rationale, and validation role rather than only listing tools, equipment, software, modules, or parameters?
- Does each scenario, demand level, parameter level, and comparison group have a rationale?
- Are controlled variables justified?
- Are assumptions framed as design choices rather than apologies?
- For algorithm/model/system papers, do baselines, ablations, robustness checks, and performance criteria match the actual claim?

### Figure/Table Evidence Chain

Check:

- Does each main figure answer a research question?
- Are figures/tables redundant?
- Are core claims supported visually or numerically?
- Are figures/tables integrated into evidence clusters rather than narrated one by one?
- Is each main figure/table anchored by lead-in prose before it and uptake prose after it?
- Are secondary checks moved to supplement when appropriate?

### Results

Check:

- Does each result subsection answer one question?
- Does the Results structure follow research questions or claims rather than figure/table numbers?
- Are results organized around baseline fairness, primary claim support, mechanism/design contribution, robustness, and boundary where relevant?
- Are observations separated from interpretation?
- Are absolute values reported before relative changes?
- Are incomplete trips, residual vehicles, or sample biases handled?

### Discussion

Check:

- Does discussion explain mechanisms rather than repeat results?
- Does it compare with prior literature?
- Does it state implications and boundaries without becoming defensive?
- Is a standalone Discussion necessary, or would `Results and Discussion / Results and Analysis` be cleaner?
- If Discussion remains standalone, does it add cross-result synthesis rather than re-reporting numbers?

### Conclusion

Check:

- Does it state a compact set of durable findings, using only as many items as the evidence supports?
- Does it avoid new evidence and new citations?
- Is it shorter and sharper than the discussion?

### Language and Style

Check:

- Does each paragraph have one claim?
- Are topic sentences clear?
- Are repeated phrases or caveats removed?
- Is the tone measured and evidence-based?

Use a quick reverse outline for substantial sections:

| Paragraph | Function | Keep / Merge / Move / Delete |
|---|---|---|
| P1 | problem, gap, design choice, evidence, mechanism, boundary, implication, or transition | ... |

If a paragraph's function cannot be named, it is usually filler or duplicated material.

## 3. Common Diagnosis Patterns

| Symptom | Likely cause | Revision |
|---|---|---|
| Locally clear but globally bloated | Sections written independently | Rebuild whole-paper architecture |
| Long review with many citations | Literature used as inventory | Reorganize by theme and gap |
| Methods read like a manual | Too much prose detail | Convert to parameter/matrix tables |
| Methods read like an inventory | Tools, software, modules, or parameters listed without rationale | Add design/procedure, rationale, and validation role |
| Methods contain formula dumping | Consecutive equations without purpose/scope prose | Group by metric family or method decision; use a metric table when clearer |
| Results are descriptive | Figures not tied to questions | Rewrite each result around one question |
| Results read like a figure list | Consecutive figure-led paragraphs | Merge into claim-driven evidence clusters and demote secondary figures |
| Figures/tables are orphaned | Visuals appear immediately after headings, back-to-back, or without follow-up interpretation | Add lead-in and uptake prose, or merge/demote the visual |
| Discussion repeats numbers | Results/discussion roles blurred | Move numbers to Results; keep mechanism in Discussion |
| Standalone Discussion feels thin | No cross-result mechanism, literature comparison, implication, or boundary synthesis | Merge into Results and Discussion or keep only a short limitations paragraph |
| Paragraphs feel correct but heavy | Multiple paragraphs perform the same function | Reverse-outline the section and merge or delete repeated roles |
| Conclusion repeats abstract | No durable finding hierarchy | Reduce to the smallest supported finding set |

## 4. General Engineering Reviewer Checks

For engineering manuscripts across disciplines:

- Is the paper type clear: physical experiment, simulation/numerical study, model/algorithm, system/application, or review?
- Does the architecture match that type?
- Are baselines plausible and aligned with the claim?
- Are variables, units, formulas, and calculation scopes defined where ambiguity would affect reproducibility?
- Are controlled variables and simplifying assumptions justified as design choices?
- Are results ordered by claim and evidence chain rather than by figure, metric, or experiment log?
- Are ablation, sensitivity, robustness, uncertainty, or harder-condition checks sufficient for mechanism/design claims?
- Are engineering implications stated at the right level, without turning scenario results into universal claims?
- Is the Discussion architecture justified: standalone, combined with Results, or brief limitations only?

## 5. Domain-Specific Reviewer Checks (Example: Traffic Simulation)

Build a domain-specific reviewer checklist for the paper's field. The list below is a worked example for AV/CAV, SUMO, VISSIM, Aimsun, car-following, merging, bottleneck, and mixed-traffic manuscripts; instantiate the equivalent checks for other fields (e.g., specimen/batch controls for materials, stability/delay/saturation for control, data-split/tuning-budget fairness for ML, off-design/scale-up for process systems):

- Are behavior parameters justified or explicitly framed as scenarios?
- Is the baseline fair?
- Are demand states and geometry clear?
- Are demand levels, penetration rates, distribution patterns, and sensitivity levels justified by traffic-state coverage, literature/empirical ranges, mechanism isolation, or upper-bound/baseline logic?
- Are random seeds and aggregation rules reported?
- Are formulas grouped by method function rather than listed as consecutive equation numbers?
- Are throughput, completion, residual vehicles, and travel time interpreted together?
- Are similar speed, travel-time, throughput, robustness, or safety-proxy plots synthesized rather than narrated separately?
- Does the paper avoid confusing pure car-following effects with lane-changing or merging effects?
- Are upper-bound or idealized CAV scenarios labeled?
- Are safety/comfort metrics framed as proxies, not crash-risk conclusions?
- Is sensitivity/ablation sufficient for mechanism claims?

## 6. Priority Ranking

After scoring, list revisions in this order:

1. Architecture and central claim.
2. Evidence chain and figure/table selection.
3. Section role overlap and repetition.
4. Literature and citation strategy.
5. Paragraph compression and wording.

Do not start by polishing sentences if the architecture score is below 4.
