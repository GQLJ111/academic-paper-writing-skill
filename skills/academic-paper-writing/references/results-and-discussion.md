# Results and Discussion

## Results Section Pattern

Each result subsection should answer one research question or support one claim. Do not let the figure number determine the paragraph order.

Use:

```text
Question/topic sentence.
Evidence cluster: one or more figures/tables/metrics that jointly answer the question.
Main observation with only the numbers needed for the claim.
Comparison to baseline.
Mechanism interpretation.
Boundary or caution.
Transition to next result.
```

One result subsection may synthesize several figures or tables when they support the same claim. Conversely, a secondary figure may need only one sentence, a caption, or a supplement placement rather than a full paragraph.

For engineering papers, organize result subsections around the questions a reviewer would ask:

- Is the baseline fair, and what is the absolute performance?
- Does the primary result support the central claim?
- Which mechanism, module, parameter, condition, or design choice drives the result?
- Does the claim survive ablation, sensitivity, robustness, uncertainty, or harder conditions?
- What boundary prevents overgeneralization?

These questions should shape the order of evidence. Do not use software output order, figure order, experiment log order, or metric order as the manuscript structure.

## Figure/Table Anchoring Pattern

Use a `lead-in prose -> figure/table -> uptake prose` pattern for manuscript logic, regardless of where the journal eventually floats the visual.

- **Lead-in prose**: state the research question, claim, comparison, method decision, or reading focus before referring to the figure or table.
- **Figure/table**: present the visual evidence, parameter matrix, workflow, scenario, or summary.
- **Uptake prose**: interpret the key observation, important number, contrast, anomaly, boundary, or transition after the visual.

Do not place a figure or table immediately after a Results subsection title without a sentence that tells the reader why it is being shown. Do not place two or more visuals back-to-back unless the manuscript text first defines them as one evidence cluster and then interprets the cluster afterward. A caption cannot carry the whole interpretation by itself.

## Observation vs Interpretation

Observation:

```text
Under the high-load condition, configuration A reduces the average response time from 12.4 ms to 9.8 ms compared with the baseline.
```

Interpretation:

```text
This suggests that the redesigned module reduces processing delay under the tested operating condition.
```

Boundary:

```text
The result should not be interpreted as evidence of robustness under untested workloads or hardware platforms.
```

## Figure and Table Rules

- Every main figure should answer a question.
- Do not include redundant figures in the main text.
- Do not write figure-by-figure prose such as "Figure 2 shows..., Figure 3 shows..., Figure 4 shows..." unless each figure answers a genuinely different research question.
- If several figures show the same pattern across metrics, scenarios, or robustness checks, synthesize the pattern in one paragraph and cite the figures as an evidence cluster.
- Use figure captions to state what is plotted, under what condition, and what comparison matters.
- In the manuscript text, anchor each main figure or table with lead-in prose before it and uptake prose after it.
- Put detailed sensitivity, robustness, and secondary metrics in supplements unless they carry a core claim.
- Mention uncertainty or seed variation when available.

## Figure Dump Check

Before delivering Results, scan for these failure signs:

- Consecutive paragraphs begin with figure or table references.
- The subsection order follows figure numbers rather than research questions.
- A subsection begins with a figure or table before any prose states the question or claim.
- A figure or table is followed immediately by another visual or by a new subsection without uptake prose.
- Several similar line charts receive separate prose even though they support one claim.
- Captions carry the actual interpretation while the text only points to figures.

Fix by rewriting around `lead-in -> visual/evidence cluster -> uptake -> boundary`. Move secondary figures to captions, tables, appendix, or supplementary material when they do not change the main claim.

## Discussion Section Jobs

Discussion should do at least three of these:

1. Explain mechanisms behind the results.
2. Compare results with prior literature.
3. Explain why findings differ from prior studies.
4. State practical/modeling implications.
5. Clarify boundaries and limitations.
6. Suggest future work tied to limitations.

## Standalone vs Combined Discussion

Choose the Discussion architecture before drafting.

Use a standalone **Discussion** when:

- The manuscript needs mechanism synthesis across several result subsections.
- Prior literature must be compared, reconciled, or contradicted.
- Engineering implications, design tradeoffs, deployment meaning, or external validity need conceptual development.
- Limitations affect how several results should be interpreted.

Use **Results and Discussion / Results and Analysis / 结果与分析** when:

- The paper is compact or applied, and each result can be interpreted immediately after the evidence.
- A separate Discussion would mostly repeat result numbers.
- The target journal or Chinese engineering style commonly combines result reporting and interpretation.
- Each subsection can follow `question -> evidence -> observation -> interpretation -> boundary`.

Do not combine Results and Discussion by simply writing longer result paragraphs. A combined section still needs interpretation, mechanism, implication, and boundary statements; it just places them locally with the evidence instead of in a later conceptual section.

If a draft already has both Results and Discussion, audit for duplication:

- Move numerical detail and figure-by-figure description to Results.
- Keep cross-result mechanism, literature comparison, implications, and limitations in Discussion.
- If Discussion has no conceptual content after removing repeated numbers, merge it into Results and Discussion or a short limitations paragraph.

## Limitation Writing

A limitation should be honest but contained:

```text
This study controls [factor] to isolate [mechanism]. Therefore, the results do not capture [excluded effect]. Future work can extend the design by [specific extension].
```

Avoid:

- “Due to limited time...”
- “The model is simple, so the results may be inaccurate.”
- Limitations that imply the entire study is invalid.

## Conclusion Pattern

Use a compact paragraph-style conclusion for journal manuscripts:

Opening paragraph: briefly restate the research problem, method, and core material/experimental scope.

Middle paragraph(s): synthesize the supported findings as coherent prose. Each finding should keep one claim and only the key condition or number needed; use only as many findings as the results support.

Closing paragraph: state the contribution/implication, the most consequential boundary, and future work.

Do not use `(1)`, `(2)`, `(3)`, `1.`, `2.`, `3.`, or `第一/第二/第三` unless the user explicitly asks for numbered conclusions, a provided target journal/template requires numbering, or the output is for a thesis/course report that requires enumerated findings.

Do not introduce new numbers or claims not shown in results. Do not repeat the full methods, literature gap, or every limitation.
