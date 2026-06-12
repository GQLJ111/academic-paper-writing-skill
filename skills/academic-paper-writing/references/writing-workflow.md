# Academic Paper Writing Workflow

## Paper-Level Argument

Before drafting, state the paper in one sentence:

```text
This paper investigates [object] under [context] using [method] to explain/test [mechanism or relationship], showing [main finding] with [boundary].
```

If this sentence is vague, do not start full drafting. First clarify object, context, method, finding, and boundary.

## Standard Section Jobs

| Section | Job | Failure Mode |
|---|---|---|
| Title | Names object, method/angle, and outcome without overclaiming | Too broad or slogan-like |
| Abstract | Compresses motivation, gap, method, results, contribution | Background-heavy, result-light |
| Introduction | Moves from problem to gap to research question to contribution | Generic background, weak gap |
| Literature Review | Synthesizes streams and exposes unresolved issue | Paper-by-paper listing |
| Methods | Makes evidence production reproducible and fair | Missing parameters, baselines, controls |
| Results | Answers research questions with figures/tables | Reports numbers without interpretation |
| Discussion | Explains mechanisms, implications, and boundaries | Repeats results |
| Conclusion | States durable findings and future work | Introduces new evidence |

## Recommended Workflow

1. **Inventory evidence**
   List datasets, experiments, figures, tables, metrics, and strongest numerical findings.

2. **Define research questions**
   Use 2-4 questions. Each result subsection should answer one question.

3. **Map evidence to claims**
   For each claim, identify exact supporting figure/table and boundary.

4. **Draft methods before results**
   Methods define what the results can legitimately claim.

5. **Draft results as answer blocks**
   Observation -> comparison -> interpretation -> boundary.

6. **Draft introduction after results are clear**
   A strong introduction is easier once contributions are known.

7. **Write abstract and conclusion last**
   Ensure they match the actual evidence, not the original ambition.

## Diagnostic Checklist

Ask:

- What is the central uncertainty this paper resolves?
- What does the paper compare against?
- What is controlled, varied, and measured?
- Which result is the strongest evidence?
- Which result is surprising or non-monotonic?
- What should not be generalized?
- What would a reviewer attack first?

## Section Transition Pattern

Use transitions that narrow the logic:

```text
Existing studies show [known].
However, [gap/uncertainty] remains.
Therefore, this study [does X] to test [Y].
The results show [finding], suggesting [implication] under [boundary].
```
