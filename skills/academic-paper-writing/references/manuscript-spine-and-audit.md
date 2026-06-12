# Manuscript Spine and Audit

Use this reference for full-paper drafting, major revision, thesis-to-paper conversion, from-materials writing, figure/table-centered results writing, citation planning, or final manuscript audit. Keep it lightweight: apply only the parts needed for the user's task.

## 1. Manuscript Spine

Before large writing tasks, define the paper's spine in a compact block:

| Element | Question | Output |
|---|---|---|
| Central problem | What concrete uncertainty or practical/scientific problem is this paper about? | One focused sentence |
| Specific gap | What exactly remains unresolved by prior work or the current draft? | One testable gap, not a broad topic |
| Core contribution | What does this paper add that the evidence can actually support? | One to three narrow contribution claims |
| Evidence chain | Which data, experiments, figures, models, cases, or references support the contribution? | Ordered evidence list |
| Claim boundary | What should the paper not claim? | Scope limits and forbidden overclaims |

If the spine cannot be filled from available material, stop and ask for the missing evidence rather than inventing a stronger contribution.

## 2. Claim-Evidence-Citation Map

Use this map before drafting introductions, discussions, conclusions, or major result sections:

| Claim | User Evidence | Citation Function | Section | Boundary |
|---|---|---|---|---|
| Main claim or paragraph-level claim | Figure, table, experiment, dataset, model, equation group, note, or draft evidence | background / gap / method source / benchmark / mechanism / limitation / application / discussion comparison | Where the claim belongs | What the claim does not prove |

Rules:

- A claim without user evidence can be framed only as background, hypothesis, or literature context.
- A citation cannot replace missing results from the current study.
- Prefer one precise citation function over broad citation clusters.
- For review papers, citations are evidence and should be grouped by theme, method, finding, disagreement, or gap.
- For empirical, simulation, modeling, algorithm, and experiment papers, citations usually support context, method choices, benchmarks, and discussion comparisons; the paper's own results support the main findings.

## 3. Figure/Table and Equation Contracts

Before writing around a major figure, table, or equation group, define:

| Item | Check |
|---|---|
| Claim or method decision | What exact claim or reproducible definition should this item support? |
| Reader question | What uncertainty does it answer? |
| Evidence cluster | Which figures, tables, metrics, or equations belong together? |
| Main panel, metric, or equation | Which part carries the main evidence or definition? |
| Comparison baseline | What is the fair comparison group or reference condition? |
| Boundary | What cannot be concluded from this display? |
| Manuscript home | Results, Methods, Discussion, supplement, caption, or appendix |
| Prose anchors | What lead-in text introduces this item, and what uptake text interprets it afterward? |

Do not describe every visual or equation detail. Write around the claim, research question, or method decision the evidence is supposed to support. Do not let figure numbers or equation numbers determine the prose order. For main figures and tables, avoid orphan placement: the manuscript should set up the visual before it appears and interpret its role after it appears, even if final journal layout floats the display elsewhere.

## 4. Section-Aware Duties

Use section-specific revision targets:

| Section | Must Do | Must Avoid |
|---|---|---|
| Title | Name object, method/angle, and context | Vague "study/research on" titles or unsupported outcome claims |
| Abstract | State problem, method, key results, contribution, and one boundary | Literature review, vague significance, new claims not in paper |
| Introduction | Move from importance to specific gap and contribution | Broad openings, paper-by-paper literature lists, task-list contributions |
| Literature Review | Synthesize streams and expose the unresolved issue | One paragraph per paper, citation inventory, no synthesis paragraph |
| Methods | Make design, variables, controls, metrics, formulas/notation when needed, and reproducibility clear | Manual-like prose when a table or equation is clearer |
| Results | Report observations that answer research questions using evidence clusters | Figure-by-figure reporting, long mechanism explanations, literature debate, unsupported causality |
| Discussion | Explain mechanisms, implications, comparison with prior work, and boundaries | Repeating result numbers or introducing new experiments |
| Conclusion | State the smallest durable set of supported findings | New citations, new evidence, a second abstract, overbroad recommendations |
| Reviewer Response | Map comment, action, manuscript location, and response | Polite but unverifiable promises |

## 5. Pre-Delivery Audit

Before delivering substantial prose, run this quick audit:

| Check | Failure Sign | Fix |
|---|---|---|
| Spine alignment | Section advances a different paper identity | Reframe or move the section |
| Claim support | Claim lacks user evidence or citation function | Narrow claim, add evidence anchor, or flag missing input |
| Citation quality | Long citation cluster attached to a generic statement | Replace with functional, representative citations |
| Equation/notation clarity | Metrics, models, or constraints are described only in prose despite ambiguous calculation or symbols | Add a compact equation/notation block or flag the missing author definition |
| Equation dump | Several equations appear back-to-back without purpose, scope, or interpretation prose | Group equations by metric family or method decision; add prose or move basic definitions to a table |
| Results/discussion split | Results explain mechanisms for several sentences | Move mechanism to Discussion |
| Conclusion boundary | Conclusion claims practical impact beyond evidence | Convert to supported finding or implication |
| Repetition | Same gap, limitation, or motivation fully explained in multiple sections | Choose one home and shorten later mentions |
| Figure/table role | Figure is described but not tied to a research question | Rewrite around the question and claim |
| Figure/table dump | Consecutive paragraphs follow figure or table numbers rather than claims | Merge into evidence clusters, demote secondary visuals, or move them to supplement |
| Orphan figure/table | A figure or table appears immediately after a heading, appears back-to-back with another visual, or is not followed by interpretation prose | Add lead-in prose before the visual and uptake prose after it; if visuals form one cluster, introduce and interpret the cluster |
| Reviewer response traceability | Response says "revised" without location/action | Add stable comment ID, action, and manuscript location |

If an audit issue can be fixed from provided material, fix it before responding. If fixing requires missing data, exact references, figure meanings, target journal rules, or author intent, flag it explicitly.

## 6. Lightweight Output Templates

For large tasks, keep planning visible but short:

```text
Manuscript spine:
- Central problem:
- Specific gap:
- Core contribution:
- Evidence chain:
- Claim boundary:
```

```text
Claim-evidence-citation map:
| Claim | Evidence anchor | Citation function | Section | Boundary |
|---|---|---|---|---|
```

```text
Reviewer response map:
| ID | Reviewer concern | Revision action | Manuscript location | Response status |
|---|---|---|---|---|
```

Do not show these templates for small one-paragraph polishing unless the user asks for diagnosis.
