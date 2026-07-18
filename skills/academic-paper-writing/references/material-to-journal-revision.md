# Material Draft to Journal Manuscript Revision

Use this reference when a draft is complete but verbose, report-like, thesis-like, repetitive, or not yet shaped like a journal article.

## 1. Revision Goal

The goal is not to polish every sentence. The goal is to convert a full material draft into a narrow, evidence-driven manuscript.

```text
Material draft = preserves everything that might matter.
Journal manuscript = presents only what is needed for one defensible argument.
```

## 2. Diagnosis First

Before editing, create a diagnosis table:

| Issue | Evidence in draft | Action |
|---|---|---|
| Repeated claim | Sections where it repeats | Keep one full version; shorten/delete others |
| Section role overlap | Sections doing same job | Merge or redefine section jobs |
| Excess method prose | Long parameter/scenario paragraphs | Compress the prose; use a table only for repeated comparison/lookup fields, otherwise move detail to an appendix |
| Result overload | Too many similar metrics/figures or figure-by-figure result prose | Keep core evidence; synthesize evidence clusters; move secondary checks |
| Formula dump | Consecutive equations listed without prose logic | Group by method decision or metric family; move basic definitions to a table when clearer |
| Defensive caveats | Same boundary repeated | Keep local cautions brief; full discussion once |
| Citation padding | Long chains with same function | Keep representative references |

Do not rewrite until this table is clear.

## 3. Conversion Workflow

### Step 1: Define the Journal Core

Write:

```text
Central claim:
Target journal-style structure:
Three core contributions:
Main finding synthesis, in compact prose and determined by the actual evidence:
Main evidence clusters:
Material to delete:
Material to move to supplement:
```

### Step 2: Rebuild the Outline

Convert thesis/report structures into article structures.

Common conversion:

```text
Thesis/report:
1 Introduction
2 Literature Review
3 Methods and Experimental Plan
4 Full Results
5 Long Discussion
6 Conclusions

Journal article:
1 Introduction
2 Materials and Methods / Methodology and Experimental Design
3 Results
4 Discussion
5 Conclusions
Supplementary Material
```

Use a separate Related Work / Literature Review section only when the target journal requires it or when the literature synthesis cannot fit cleanly in the Introduction. If length must be tighter:

```text
1 Introduction
2 Methods
3 Results and Discussion
4 Conclusions
```

### Step 3: Assign Each Idea One Home

Examples:

- "The idealized 100% case is an upper bound" -> define in Methods; discuss implication in Limitations; only brief notes elsewhere.
- "The combined-loading scenario is not the isolated mechanism" -> define in scenario/experiment design; interpret in Discussion.
- "An average over only successful samples can be biased" -> define in Metrics; use in Results; explain in Discussion.
- "Findings differ across the literature" -> Introduction, or Literature Review if separately needed; do not repeat in Conclusion.

### Step 4: Cut by Function

Delete or move text that does not perform one of these functions:

- Establish gap.
- Justify design.
- Report core evidence.
- Interpret mechanism.
- State boundary.
- Conclude contribution.

If a paragraph only says the topic is important, repeats a known limitation, or previews what the next section will do without adding logic, delete or compress it.

### Step 5: Rebuild Results Around Claims

Use the evidence-cluster protocol in `results-and-discussion.md`. Create one result block for each research question, claim, or mechanism, not one block for every figure, table, metric, or experiment log. Each block should state the claim, identify the joint evidence, report only the numbers needed, and retain the comparison, interpretation, and boundary required by that claim.

When several visuals tell the same story, synthesize them in one block; when a visual does not change the main interpretation, demote it to a caption, appendix, or supplement.

### Step 6: Rewrite Discussion, Not Results

Discussion should contain:

1. Mechanism synthesis.
2. Relation to literature.
3. Modeling or practical implication.
4. Boundary and future work.

Move detailed result descriptions back to Results or delete them.

### Step 7: Rewrite Abstract and Conclusion Last

The abstract should match the final paper, not the original material draft.

Use the paragraph-style conclusion pattern in `top-journal-section-patterns.md`. Keep only the supported findings, contribution/implication, and most consequential boundary or future direction; do not introduce a fixed count or new evidence.

## 4. Sentence-Level Compression

Use after structural compression.

Patterns:

- Replace "本文首先..., 其次..., 最后..." repeated across sections with direct topic sentences.
- Replace long caveats with precise boundaries.
- Replace repeated "需要指出的是" with one integrated clause.
- Replace "可以看出" with the actual observation.
- Convert parameter prose to table references only when repeated fields make the table clearer than concise prose.
- Replace figure-by-figure transitions with claim-driven topic sentences.
- Replace stacked formulas with grouped metric definitions plus brief purpose/scope prose.
- Merge consecutive paragraphs if both explain the same mechanism.

Chinese-specific checks:

- Avoid multiple consecutive paragraphs starting with "本文".
- Avoid repeated "不是...而是..." unless it creates a real contrast.
- Keep one claim per paragraph.
- Put the topic sentence first.
- Delete phrases like "具有重要意义" unless the significance is immediately specified.

## 5. Final Journal-Readiness Checklist

- Can the paper's central claim be stated in one sentence?
- Does the introduction reach the gap quickly?
- If a literature review is used, does it synthesize instead of catalog? If not used, does the Introduction carry enough focused synthesis to prove the gap?
- Are methods reproducible without becoming a manual?
- Does each result subsection answer one research question?
- Are figures/tables non-redundant and integrated as evidence clusters rather than a figure list?
- Are formulas grouped by method function rather than dumped as consecutive equation numbers?
- Does discussion explain, not repeat?
- Is the conclusion shorter than the discussion?
- Are limitations honest but contained?
- Are references used by argumentative function, not by quantity?
