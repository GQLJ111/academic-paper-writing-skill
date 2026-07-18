# Whole Manuscript Architectures

Use this reference before drafting or restructuring a full paper. Choose the manuscript architecture first, then write sections.

## 1. Architecture Options

### Engineering Experimental / Simulation Journal Article

Use for laboratory tests, field experiments, simulations, numerical studies, field data, trajectory data, surveys, or engineering case studies where the contribution is new evidence.

```text
Title
Abstract
Keywords
1. Introduction
2. Materials and Methods / Methodology / Experimental Design
3. Results
4. Discussion or Results and Discussion
5. Conclusions
References
Supplementary Material
```

This IMRaD-style structure is the starting point for non-review empirical, experimental, and simulation journal articles. Put the focused literature synthesis inside the Introduction unless a separate review section is necessary.

Section jobs:

- **Introduction**: problem, established knowledge, precise gap, research questions, contributions.
- **Materials and Methods / Methodology / Experimental Design**: study design, scenarios/data, variables, controls, parameters, metrics/formulas when needed, notation, and validation.
- **Results**: evidence blocks aligned with research questions; core figures and tables only.
- **Discussion**: mechanism, literature comparison, implications, boundaries, future extensions. Combine it with Results when every result subsection already reports and interprets the finding and a separate Discussion would repeat numbers.
- **Conclusions**: compact prose synthesis of durable findings, contribution, and brief limitation/future work, determined by the actual evidence.

Add a separate **Literature Review / Related Work** section only when it has a real argumentative job: the target journal requires it, the literature disagreement is too complex for the introduction, a method/model paper needs technical positioning, or the paper's contribution depends on a classification of prior work. If used, it must synthesize themes and prove the gap, not list papers.

### Methods / Model Paper

Use when the contribution is a model, algorithm, calibration method, control method, or evaluation framework.

```text
1. Introduction
2. Related Work
3. Problem Formulation / Model
4. Method / Algorithm / Framework
5. Experimental Setup / Case Study
6. Results and Evaluation
7. Discussion / Limitations
8. Conclusions
```

Do not bury the method contribution inside a long case-study description.

### Engineering System / Application Paper

Use when the contribution is an engineered system, platform, workflow, prototype, deployment, or application assessment rather than only a controlled experiment.

```text
1. Introduction
2. Related Work / Design Requirements
3. System Architecture / Method
4. Implementation / Experimental Setup
5. Evaluation / Case Study
6. Discussion / Practical Implications
7. Conclusions
```

The system section should explain design requirements, module responsibilities, interfaces, constraints, and why the architecture answers the engineering problem. The evaluation section should test the claims made by the system design rather than merely demonstrate that the system exists.

### Review / Synthesis Paper

Use when the contribution is literature synthesis.

```text
1. Introduction
2. Review Scope and Method
3. Classification Framework
4. Thematic Findings
5. Gaps, Challenges, and Future Directions
6. Conclusions
```

Synthesize patterns; do not summarize papers one by one.

### Conference Paper

Use when length is tight.

```text
1. Introduction
2. Method / Experimental Design
3. Results
4. Discussion or Limitations
5. Conclusions
```

Move literature detail, secondary metrics, and sensitivity checks to brief citations or supplements. Center the paper on one claim.

### Thesis / Dissertation Structure

Use when the target is a thesis or long-form chapter.

```text
Chapter 1 Introduction
Chapter 2 Literature Review
Chapter 3 Methodology / Experimental Design
Chapter 4 Results
Chapter 5 Discussion
Chapter 6 Conclusions and Future Work
```

Thesis writing can include more background and method detail than journal writing, but still avoid repeating the same motivation or boundary in every chapter.

## 2. Architecture Selection Rules

- New evidence from tests, data, or simulations -> engineering experimental/simulation architecture.
- New method/model -> methods/model architecture.
- New system, prototype, platform, or deployment workflow -> engineering system/application architecture.
- Literature synthesis -> review architecture.
- Strict length limit -> conference architecture.
- "Chapter", "thesis", or complete long Chinese draft -> thesis architecture.
- Separate Literature Review / Related Work is optional for empirical/simulation articles; include it only when it prevents the Introduction from becoming overloaded or is required by the venue.
- Standalone Discussion is optional for engineering papers. Keep it when mechanism, literature comparison, implications, and boundaries need conceptual development; combine it with Results when interpretation is local to each result subsection.

## 3. Whole-Paper Planning Template

Before drafting, write:

```text
Paper type:
Engineering subtype:
Target form:
Central claim:
Target structure:
Discussion architecture: standalone / combined with Results / limitations-only
Section 1 adds:
Section 2 adds:
Section 3 adds:
Section 4 adds:
Section 5 adds:
Main figures/tables:
What goes to appendix/supplement:
```

If two sections add the same thing, merge or redefine them before drafting.

## 4. Section Role Separation

| Content type | Full development belongs in | Other sections may only |
|---|---|---|
| Practical motivation | Introduction | Mention in one sentence |
| Literature streams and gap | Introduction, or Literature Review if separately needed | Cite briefly |
| Experimental design choices | Materials and Methods / Methodology | Refer to setup/table |
| Numerical results | Results | Summarize only the strongest finding |
| Mechanism and interpretation | Discussion, or local interpretation in Results and Discussion | Give one-sentence interpretation in Results |
| Limitations and boundaries | Discussion or Limitations | Include short local cautions only when needed |
| Durable findings | Conclusion | Avoid re-explaining methods or literature |

## 5. Anti-Repetition Rule

For recurring ideas:

1. **Define once** in the proper section.
2. **Refer briefly** later.
3. **Delete** if it does not change interpretation.

Do not fully explain the same boundary in the abstract, introduction, method, discussion, and conclusion.

## 6. Compression Targets

- Abstract: problem, method, 2-4 key results, contribution, one boundary.
- Introduction: 4-6 focused paragraphs; include only the literature needed to establish the gap.
- Literature review, if used: 3-5 thematic streams plus a synthesis gap; no paper-by-paper catalog.
- Methods: tables only when repeated parameter/matrix fields require lookup or comparison; equations for ambiguous metrics, models, objectives, or constraints; prose explains design logic.
- Results: each subsection answers one question.
- Results and Discussion, if combined: each subsection reports the evidence, interprets mechanism or implication, and states a local boundary without duplicating a later discussion.
- Discussion, if standalone: 4-6 conceptual moves; do not re-report result tables.
- Conclusion: compact prose synthesis of supported findings plus brief limitation/future work; do not force a fixed count or list format.
