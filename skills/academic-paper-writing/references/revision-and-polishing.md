# Revision and Polishing

## Revision Order

Revise in this order:

1. Research question and contribution.
2. Section structure and paragraph order.
3. Claim-evidence alignment.
4. Figure/table integration.
5. Paragraph clarity.
6. Sentence-skeleton and information integrity.
7. Sentence-level style.
8. Grammar, terminology, and formatting.

Do not start with word polishing if the argument is unclear.

## Sentence and Information Integrity Pass

At step 6, run an internal two-level integrity pass before stylistic polishing. Treat grammatical completeness as a clear semantic skeleton, not as a requirement that every sentence contain all traditional Chinese components.

### L1: Sentence Skeleton

For each sentence:

1. Reduce it to `research object or phenomenon -> action, state, or relation -> required object, result, or boundary`.
2. Keep the subject explicit, or omit it only when the same subject is unambiguous from the preceding sentence. Restore it when the subject drifts between clauses.
3. Use a complete predicate. Do not leave a sentence as a nominal phrase or as an introductory `通过/基于/针对/考虑到/在……条件下` chain without a main clause.
4. Supply the object, result, complement, comparison baseline, condition, or scope required by the predicate and intended claim.
5. Attach each modifier to the intended noun or action. Recast long `……的……的……` chains and split clauses when attachment becomes ambiguous.
6. Replace unclear references such as `其/该/这种/上述/这` or bare English `this/these` with the concrete finding, variable, mechanism, or result.
7. Make coordination, causality, contrast, and progression explicit. Do not join independent claims with commas alone.

### L2: Claim Information

A sentence can be grammatically complete but still fail to communicate a usable engineering claim. Check evidence-bearing predicates against the information they require:

| Claim function | Required information |
|---|---|
| Effect: `improve/reduce/affect` | Factor or intervention, affected object or metric, baseline/comparator, condition, and magnitude when supported |
| Validation: `validate/verify` | Model or method being validated, data or baseline used, criterion or metric, and operating scope |
| Comparison: `compare/outperform` | Compared alternatives, common metric, baseline, and matched conditions |
| Inference: `show/indicate/suggest` | Concrete finding, supporting evidence, appropriate strength, and boundary |

Required information may be distributed across adjacent sentences, an equation, a table, or a figure, but it must be explicit and easy to recover without guessing. Treat `该方法验证了有效性` or `The method was validated` as underspecified when the surrounding context does not already supply the validation target, evidence, criterion, and scope. Fill missing roles only from user evidence; otherwise narrow the statement or flag the exact missing input rather than inventing detail.

Do not expose grammatical parsing in the delivered manuscript unless the user asks for diagnosis. For a long draft, inspect every sentence internally and give extra attention to the topic sentence, the longest sentence, sentences whose subject changes, evidence-bearing predicates, and sentences beginning with `通过/基于/针对/随着/在……条件下/结果表明`.

## Anti-Meta and Anti-Teaching Pass

For manuscript delivery, remove language whose main function is to narrate the writing process, teach the author how to read the sentence, or report an internal diagnosis. Apply three tests:

1. **Paper-content test**: does the sentence add a research object, relation, method decision, evidence, interpretation, condition, or boundary? If not, delete or recast it.
2. **Audience test**: is the sentence addressing the manuscript reader as a student or the author as an editor would? If so, replace the instruction with the actual academic content.
3. **Leakage test**: does the sentence reveal planning, rubric labels, grammatical parsing, revision reasons, or audit language? Keep that information outside the manuscript unless explicitly requested.

Common repairs:

| Weak manuscript wording | Repair |
|---|---|
| `为了便于理解，下面对该机制进行说明。` | State the mechanism directly and connect it to the relevant evidence or model relation |
| `需要注意的是，该参数会影响结果。` | Name the parameter, affected metric, direction, condition, and evidence-supported boundary |
| `这句话可以理解为……` / `This means that ...` used as a teaching gloss | Write the intended definition, inference, or mechanism as the manuscript sentence itself |
| `本段主要介绍……` / `The following section explains ...` | Use a topic sentence that states the section's actual claim or method purpose |
| `经检查，该句缺少主语，因此修改为……` | Deliver the corrected sentence; place the diagnosis in commentary only if requested |

Do not delete legitimate logical signposts merely because they resemble these forms. Retain them when they identify a real contrast, scope condition, exception, or interpretation boundary that the sentence then states precisely.

## Abstract Checklist

An abstract should include:

- Problem/gap.
- Objective.
- Method/data/scenarios.
- Key results, preferably quantitative.
- Contribution or implication.
- Boundary if the result is simulation/model-specific.

For Chinese journal abstracts, check the pacing:

- Is the first sentence enough to set the background/problem without becoming a literature review?
- Do sentences 2-4 make the research object, method, scenarios/data, and comparisons concrete?
- Do the remaining sentences emphasize findings rather than motivation or procedural detail?
- Is the length near 250-300 Chinese characters unless the journal requires otherwise?

## Title Checklist

A good title names:

- Object.
- Mechanism or method.
- Outcome.
- Context if needed.

Avoid:

- “Research on...”
- “Study of...”
- Overly broad claims such as “improving system performance.”

## Reviewer Response Pattern

For each reviewer comment:

```text
Thank the reviewer.
State what was changed or explain why not.
Point to exact section/table/figure.
Keep the tone factual.
```

Never argue from authority. Argue from evidence, scope, and manuscript changes.

## Logical Diagnosis Questions

- Does each section serve the central claim?
- Are there claims without data?
- Are there data without interpretation?
- Are limitations acknowledged near overclaim-prone results?
- Does the abstract match the actual results?
- Does the conclusion overstate the generality?

## English Polishing Principles

- Prefer short topic sentences.
- Use active voice when it clarifies agency.
- Ensure every independent sentence has a subject and a finite verb; repair fragments and dangling modifiers.
- Avoid stacked nouns when a prepositional phrase is clearer.
- Follow `this/these` with a concrete noun when the reference could be ambiguous, such as `this finding`, `this pattern`, or `these results`.
- Replace vague intensifiers with measured comparisons.
- Keep tense consistent: past for methods/results, present for general claims and paper structure.

## Chinese Polishing Principles

- Remove empty intensifiers.
- Avoid repeated “通过……，本文……”.
- Keep the subject stable and the predicate complete in long sentences; restore an omitted subject when the actor or phenomenon changes.
- Check that 定语、状语和补语 modify the intended noun or action rather than merely appearing near it.
- Use “表明/说明/提示” according to strength:
  - 表明: directly supported.
  - 说明: explanatory inference.
  - 提示: cautious implication.
