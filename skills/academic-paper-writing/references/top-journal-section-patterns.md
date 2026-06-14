# Top-Journal Section Patterns

Use this reference when drafting or diagnosing specific paper sections. The goal is not to imitate one journal mechanically, but to reproduce the logic common to strong papers: every section narrows uncertainty, connects to evidence, and avoids overclaiming.

## 0. Manuscript Economy

Strong papers are not complete because they say everything. They are complete because the reader can follow one defensible argument without unnecessary detours.

## 0.1 Whole-Manuscript Architectures

For full-paper architecture selection, thesis vs journal structure, section role separation, and compression targets, read `whole-manuscript-architectures.md`. This file focuses on section-level patterns after the manuscript architecture has been chosen.

### Section Role Separation

| Content type | Full development belongs in | Other sections may only |
|---|---|---|
| Practical motivation | Introduction | Mention in one sentence |
| Literature streams and gap | Introduction, or Literature Review if separately needed | Cite briefly |
| Experimental design choices | Methodology | Refer to setup/table |
| Numerical results | Results | Summarize only the strongest finding |
| Mechanism and interpretation | Discussion | Give one-sentence interpretation in Results |
| Limitations and boundaries | Discussion or Limitations | Include short local cautions only when needed |
| Durable findings | Conclusion | Avoid re-explaining methods or literature |

### Anti-Repetition Rule

For any recurring idea, choose one of three treatments:

1. **Define once**: give the full explanation in the section where it belongs.
2. **Refer briefly**: later sections use a short phrase, not a second explanation.
3. **Delete**: if the idea does not change the reader's interpretation at that point.

Do not fully explain the same boundary in Abstract, Introduction, Method, Discussion, and Conclusion. For example, a simulation paper may mention model boundaries briefly in the abstract, justify controlled assumptions in methods, and discuss generalizability in limitations; it should not restate the same warning after every result.

### Compression Targets

Use these as judgment guides, not fixed word limits:

- Abstract: problem, method, 2-4 key results, contribution, one boundary.
- Introduction: 4-6 focused paragraphs; include the focused literature synthesis needed to establish the gap.
- Literature review, if separately used: 3-5 thematic streams plus a synthesis gap; no paper-by-paper catalog.
- Methods: tables for parameters and matrices; equations for ambiguous metrics, models, objectives, or constraints; prose explains design logic.
- Results: each subsection answers one question; report only numbers needed for the claim.
- Discussion: 4-6 conceptual moves; do not re-report result tables.
- Conclusion: the smallest prose synthesis of durable findings plus brief limitation/future work; not a second abstract.

### Bloat Symptoms

- The same phrase appears in multiple sections with only minor wording changes.
- Every claim is followed by a long caveat.
- The text says "this paper constructs/compares/analyzes" repeatedly instead of advancing the argument.
- Results and discussion both describe the same figure in detail.
- The conclusion repeats the abstract, methods, and limitations instead of stating durable findings.

## 1. Title

### Job

Name the object, angle, and outcome without sounding like a slogan.

### Strong Patterns

```text
[Mechanism/variable] effects on [outcome] under [context]
[Method] analysis of [problem] in [system/scenario]
Distinguishing [A] and [B] in [research object]: evidence from [method/context]
```

### Avoid

- “Research on...”
- “Study of...”
- “Optimization of...” when no optimization is performed.
- Claims like “improving” or “enhancing” unless the paper actually proposes and evaluates an intervention.

### Quick Check

Can a reader infer what is studied, how, and in what context? If not, the title is too vague.

## 2. Abstract

### Job

Compress the whole paper into a problem-gap-method-result-contribution chain.

### Top-Journal Structure

```text
1. Problem and unresolved gap.
2. Objective or research question.
3. Method, data, scenarios, or experiment design.
4. Key results with the most important quantitative evidence.
5. Contribution, implication, and boundary.
```

This is the logical chain, not a paragraph quota. For Chinese journal-style abstracts, prefer a compact three-block rhythm unless the target journal requires another format:

```text
Sentence 1: background/problem, with no mini literature review.
Sentences 2-4: research objective, method, scenarios/data, and main comparison content.
Sentences 5-11: main findings, ordered by importance and supported by key quantitative evidence where useful.
```

Chinese abstracts commonly fit around 250-300 Chinese characters or roughly 8-11 sentences, but target-journal requirements override this. Do not force the exact sentence count; use it to keep the background short, methods concrete, and findings dominant.

### English Abstract Skeleton

```text
Although [topic] has been widely studied, [specific gap] remains unclear. This study investigates [research question] by [method/design]. [Key setup: data/scenarios/variables]. Results show that [finding 1 with metric], while [finding 2 or contrast]. Further analysis indicates that [mechanism/robustness]. These findings suggest that [contribution/implication], with results interpreted under [boundary].
```

### Chinese Abstract Skeleton

```text
针对……中……尚不清晰的问题，本文……。首先/进一步/最后，基于……构建……，比较……。结果表明：……；……；……。研究说明……，可为……提供参考。需要指出的是，相关结论适用于……条件。
```

### Avoid

- Background longer than method and results combined.
- “The results are significant” without actual result.
- New claims not shown in the paper.
- Repeating all limitations. Include only the boundary needed to prevent the main overclaim.

## 3. Introduction

### Job

Lead the reader from broad relevance to a precise unresolved question, then show why this paper is designed to answer it.

### Five-Move Pattern

```text
Move 1: Establish the practical/scientific problem.
Move 2: Summarize what existing studies have established.
Move 3: Identify a precise limitation/gap in existing work.
Move 4: State the research question and method logic.
Move 5: State contributions and paper organization.
```

### Chinese Funnel Introduction

For Chinese journal-style papers, the five moves often read best as a funnel. Use this shape unless the target journal or paper type requires otherwise:

```text
1. Related broad background: place the topic in its practical/scientific context, but avoid empty "rapid development" openings.
2. Focused literature transition: synthesize the main knowledge, disagreement, or research streams; do not write a full literature review.
3. Unknown/problem: state the precise unresolved issue that follows from the literature.
4. Research focus and objective: specify what this study asks, explains, or tests.
5. Research content and method overview: briefly summarize the study object, material/data/simulation design, comparison groups, and method logic as a compressed version of Methods, then state contributions or paper organization if needed.
```

The funnel should narrow at every step. If the introduction ends a paragraph with "therefore further research is needed," the next paragraph must say exactly what is unknown, not repeat the same need in broader words.

### Strong Gap Transition

```text
However, what remains unclear is not whether [broad factor] matters, but how [specific mechanism] affects [specific outcome] under [specific condition].
```

### Contribution Paragraph Pattern

```text
This study contributes to the literature in three ways. First, ... Second, ... Third, ...
```

For Chinese:

```text
本文的主要贡献包括：第一，……；第二，……；第三，……。
```

### Avoid

- Starting too broad: society, technology, modernization, rapid development.
- Reviewing all literature in the introduction.
- Claiming novelty before proving the gap.
- Contributions that are just a list of tasks.
- Repeating detailed limitations that belong in Methods or Discussion.
- Ending multiple paragraphs with the same "therefore further research is needed" move.

## 4. Literature Review / Related Work

### Job

Classify literature streams and explain why the current paper is needed.

### Section Pattern

```text
Stream 1: what is known about [theme].
Stream 2: what is known about [method/scenario/mechanism].
Stream 3: why existing findings differ or remain incomplete.
Synthesis: the exact gap this paper addresses.
```

### Strong Synthesis Sentence

```text
Taken together, these studies provide evidence that [known], but they do not fully explain [gap] because [assumption/missing comparison/missing scenario].
```

### Avoid

- One paragraph per paper.
- “Scholar A did..., Scholar B did...” without comparison.
- Treating review papers as evidence for all technical claims.
- Ending the review without a gap paragraph.
- Forcing every available paper into the review. Use representative, high-value references.
- Repeating the same "findings are inconsistent" statement in every subsection without explaining a new source of inconsistency.

## 5. Research Gap

### Job

Convert literature limitations into a testable need.

### Strong Gap Formula

```text
Existing work has examined [X], often using [Y]. However, [specific assumption/omission] limits understanding of [Z]. Therefore, it remains unclear whether/how [research question].
```

### Gap Quality Check

A good gap should identify:

- Object: what is missing.
- Reason: why prior work does not resolve it.
- Consequence: why the missing piece matters.
- Test path: how this paper can address it.

## 6. Contributions

### Job

Explain what intellectual value the paper adds.

### Strong Contribution Types

1. Conceptual: new distinction, mechanism framing, or research question.
2. Methodological: experimental design, decomposition, robustness, comparison logic.
3. Empirical/simulation: key finding with condition.
4. Practical: implication for modeling, deployment, policy, or design.

### Avoid

- “We built a model, ran experiments, and drew conclusions.”
- “This paper fills the gap” without saying how.
- Too many contributions; 2-4 is usually stronger.

## 7. Methodology

### Job

Make the evidence credible, reproducible, and aligned with the research question.

### Top-Journal Method Pattern

```text
Research design overview.
Study object/scenario/data/model.
Variables and controlled conditions.
Parameter settings and rationale.
Experiment matrix or analytical procedure.
Evaluation metrics.
Formula, notation, or unit definitions when metrics or models would otherwise be ambiguous.
Validation, robustness, or sensitivity checks.
```

For Materials and Methods, keep the logic visible:

```text
What is the study object?
What method/procedure produces the evidence?
What conditions are varied?
What conditions are fixed?
Why were these condition levels chosen?
How are results processed and checked?
```

For simulation and experiment papers, condition choices need reasons. Do not list scenarios, parameter levels, or demand levels without explaining whether they represent literature ranges, operating states, mechanism isolation, baseline/upper-bound logic, or sensitivity testing.

### Control-Variable Sentence

```text
To isolate [target effect], [potential confounder] was controlled by [design choice]. Therefore, the results should be interpreted as [specific effect], not as [broader effect].
```

### Avoid

- Hiding key parameters in prose.
- Explaining software but not experimental logic.
- Missing baselines.
- Missing formula, notation, unit, or aggregation definition for metrics or models that can be interpreted in multiple ways.
- No seed/repetition/statistical statement for stochastic experiments.
- Repeating the research background.
- Explaining every minor parameter in full prose when a table plus one rationale sentence is clearer.
- Apologizing for controlled assumptions. State what was controlled, why, and where the boundary is discussed.
- Listing test conditions without saying why those conditions were chosen.

## 8. Experiments / Case Study

### Job

Translate the method into evidence-producing comparisons.

### Experiment Subsection Pattern

```text
Purpose of the experiment.
Scenario and controlled variables.
Compared groups.
Metrics.
Expected mechanism or hypothesis.
```

### Matrix Table Columns

```text
Experiment | Scenario | Variable varied | Controlled variables | Metrics | Purpose
```

### Avoid

- Running many cases without saying what each case tests.
- Mixing main experiments and supplementary checks without hierarchy.
- Calling a scenario “realistic” without explaining its geometry, demand, or behavior assumptions.
- Giving equal weight to exploratory checks and core experiments.
- Repeating the full method description in every experiment subsection.

## 9. Results

### Job

Answer research questions with evidence, not just describe figures.

### Result Paragraph Pattern

```text
[Question or claim]. The relevant evidence comes from [figure/table/evidence cluster]. The main observation is [result with number]. Compared with [baseline], [change]. This suggests [mechanism/interpretation]. However, [boundary/caution].
```

Use figure or table numbers only after the claim has been stated. If several figures answer the same question, synthesize them as one evidence cluster rather than writing separate figure-led paragraphs.

### Figure/Table Placement Pattern

Use a `lead-in prose -> visual -> uptake prose` pattern for Results visuals:

```text
Lead-in: what question, claim, comparison, or evidence cluster the reader should inspect.
Figure/table: the visual evidence.
Uptake: the key observation, number, contrast, anomaly, boundary, or transition.
```

Do not start a Results subsection with a figure or table as the first substantive item. Do not let a caption replace the uptake paragraph or sentence. When several visuals belong together, introduce them as one evidence cluster before the first visual and interpret the cluster after the last visual.

### Strong Results Sequence

1. Start with the main outcome.
2. Add robustness or sensitivity.
3. Explain non-monotonic or unexpected results.
4. Connect back to the research question.

### Avoid

- “It can be seen from the figure...”
- Reporting every minor value.
- Ignoring results that complicate the story.
- Treating averages over only completed/successful samples as overall system performance when completion or success rates differ.
- Explaining full mechanisms that belong in Discussion.
- Ending every paragraph with the same general boundary statement.
- Duplicating figure captions in the text.
- Letting figure numbers determine the Results structure.
- Placing a figure or table directly after a subsection heading without lead-in prose.
- Moving on after a figure or table without uptake prose that interprets its role in the argument.

## 10. Discussion

### Job

Explain why results matter beyond the immediate numbers.

### Discussion Moves

```text
Mechanism: why did this pattern occur?
Literature connection: how does it align or differ from prior work?
Implication: what should modelers/practitioners/researchers do differently?
Boundary: where should this not be generalized?
Future work: what extension follows from the boundary?
```

### Strong Discussion Sentence

```text
This result helps explain why previous studies have reported inconsistent effects: [factor] changes [mechanism], so the same input or parameter level can produce different system-level outcomes.
```

### Avoid

- Repeating the results section.
- Adding new results.
- Turning every limitation into future work without explaining its impact.
- Re-listing all numerical findings.
- Discussing every supplementary result with the same weight as core evidence.
- Repeating limitations already handled in the Methods unless they affect interpretation.

## 11. Limitations

### Job

Protect the paper from overgeneralization while preserving its contribution.

### Strong Limitation Pattern

```text
This study controls [factor] to isolate [mechanism]. As a result, the findings do not capture [excluded effect]. Future work can extend the design by [specific extension].
```

### Avoid

- “Due to limited time...”
- “The model is simple...”
- Limitations so broad that they invalidate the study.
- A long defensive list disconnected from the main claims.
- Repeating future-work paragraphs already used in the conclusion.

## 12. Conclusion

### Job

State what remains true after all evidence and limitations.

### Structure

```text
Restate objective.
Summarize only the key supported findings; do not force a fixed count or list format.
State contribution/implication.
State limitations/future work briefly.
```

### Default Paragraph Conclusion Pattern

For high-level journal manuscripts, especially English or top-journal style papers, use compact paragraphs by default rather than numbered findings:

```text
Opening paragraph: restate the research problem, method, and core experimental/material scope in one or two sentences.
Middle paragraph(s): synthesize the key supported findings as a coherent argument without forcing a fixed count or numbered list.
Closing paragraph: state the contribution/implication, most consequential boundary, and direct future extension.
```

The opening paragraph is a light methods-and-scope recap, not a second abstract. It may mention the study object, method, scenarios/data, and comparison groups, but should not repeat the literature gap or full experimental matrix.

Use numbered conclusions only when the user explicitly asks for numbered conclusions, the provided target journal/template explicitly requires them, or the output is for a thesis/course report that requires enumerated findings. Do not infer numbering merely because the manuscript is Chinese, engineering-oriented, applied, or contains several findings. When numbering is required, each item should contain one supported finding and only the key condition or number needed; do not split one mechanism into multiple items just to reach a count.

### Avoid

- New citations, new data, or new figures.
- A second abstract with no findings.
- Overly general final claims.
- Repeating the full methodology or literature gap.
- Restating every limitation. Keep only the most consequential boundary and future extension.

## 13. Figures and Tables

### Job

Build the evidence chain visually.

Figures and tables may appear in Introduction, Methods, Results, Discussion, or other body sections, but their rhetorical job changes by section:

- Introduction: clarify the problem structure, research framework, or scope after the text has established the need.
- Methods: make study design, workflow, scenario layout, variables, parameters, or experiment matrices reproducible.
- Results: provide evidence for a research question or claim.
- Discussion: synthesize mechanisms, implications, comparisons, or boundaries.
- Conclusion: normally avoid new figures or tables unless the target article type explicitly expects a summary framework.

In all sections, anchor main visuals with prose before and after the display. The lead-in states why the visual is needed; the uptake explains what the reader should conclude from it. Journal layout may float figures, but manuscript logic should still place the figure reference between setup and interpretation.

### Main Figure Selection

Choose figures that:

- Answer a research question.
- Show a contrast, mechanism, or robustness result.
- Are interpretable without excessive text.
- Do not duplicate another main figure.
- Can be integrated into a claim-driven evidence cluster.

### Caption Pattern

```text
What is plotted + scenario/condition + key comparison + interpretation boundary.
```

### Avoid

- Too many similar line charts.
- Captions that only repeat axis names.
- Figures whose message is not mentioned in the text.
- A figure or table as the first substantive item after a section or subsection heading.
- Back-to-back figures or tables without prose that introduces and interprets them as one evidence cluster.

## 14. Section-Level Diagnosis

When reviewing a section, check:

- What question does this section answer?
- What claim is made?
- What evidence supports it?
- What prior literature does it connect to?
- What boundary prevents overclaiming?
- What should the next section naturally address?
