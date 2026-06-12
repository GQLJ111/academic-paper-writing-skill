---
name: academic-paper-writing
description: Use when the user asks for formal academic manuscript, thesis, journal, SCI/SSCI, or conference-paper writing; section drafting or revision; abstract/introduction/methods/results/discussion/conclusion rewriting; methods, formulas, equations, notation, metrics, or model-definition writing; academic polishing; manuscript compression; reviewer response or rebuttal; or Chinese requests such as 论文润色、改摘要、改引言、期刊论文压缩、审稿意见回复.
---

# Academic Paper Writing

## Trigger Boundary

Use this skill when the user explicitly asks for this skill, such as academic-paper-writing, a paper-writing skill, thesis-writing skill, journal-writing skill, or asks for formal academic manuscript drafting, revision, polishing, reviewer response, or paper section writing.

Also use it for clear academic-writing requests that do not name the skill, including requests such as "revise this abstract", "make this introduction more journal-like", "compress this manuscript", "write a reviewer response", "论文润色", "改摘要", "改引言", "期刊论文压缩", "学术论文改写", or "审稿意见回复".

Do not trigger it for casual research brainstorming, literature reading, experiment planning, simulation setup, code work, or general technical discussion unless the user frames the task as academic writing or asks to use this skill.

## Overview

Use this skill to write like a rigorous academic author, not a generic editor. The goal is to build a defensible paper argument: research problem, literature gap, method, evidence, interpretation, contribution, and limitations.

This skill supports both Chinese and English academic writing. Do not simply translate between languages; adapt the rhetorical structure to the target language and publication context.

## First Decisions

Before writing, identify:

1. **Target language**: Chinese, English, or bilingual. If unspecified, use the user's current language.
2. **Paper type and target form**: journal paper, thesis chapter, conference paper, literature review, experiment paper, review response, or polishing task. Also identify whether the user needs a full material draft, journal-style manuscript, thesis-style chapter, or final compressed version.
3. **Discipline and evidence type**: simulation, experiment, survey, dataset analysis, modeling, algorithm, engineering system/application, theoretical, or review.
4. **Engineering subtype when relevant**: physical experiment/test, simulation/numerical study, modeling/algorithm paper, engineering system/application paper, method-comparison paper, or review/synthesis paper.
5. **Current stage**: outline, first draft, revision, condensation, translation/adaptation, journal-style polishing, or reviewer response.
6. **Citation mode**: review/literature-synthesis paper, or empirical/experimental/simulation/modeling/technical paper.

If these are unclear and the task is substantial, ask one concise question. For small edits, make a conservative assumption and state it.

## Decision Axes

For substantial tasks, classify the request along four axes before choosing references or writing:

| Axis | Values |
|---|---|
| `task_mode` | draft, revise, polish, compress, translate/adapt, audit, reviewer-response |
| `paper_type` | empirical, experiment, simulation, algorithm, modeling, engineering-system, theoretical, review, thesis-to-paper, report |
| `section` | title, abstract, introduction, literature review, methods, results, discussion, conclusion, response letter, whole manuscript |
| `language` | zh, en, bilingual, zh-to-en, en-to-zh |

Use the axes to load only the relevant reference files and to enforce section-specific duties. Do not apply the same polishing strategy to all sections.

## Task Mode Routing

Choose one task mode before writing. If multiple modes apply, handle the highest-level mode first: full-paper structure before section drafting, structural revision before sentence polishing, and evidence/citation diagnosis before citation placement.

| User intent | Default mode | Required output |
|---|---|---|
| Full paper, major revision, journal conversion, or thesis-to-paper rewrite | Whole-manuscript planning | Short pre-writing brief, target structure, evidence chain, compression plan, then prose or revision plan |
| Section drafting or rewriting | Section-level drafting | Section role note, publication-ready text, and missing evidence or boundary notes when needed |
| Abstract, title, conclusion, or short section polishing | Focused polishing | Assumptions, revised text, and brief note on any claim narrowed or unsupported |
| Verbose, repetitive, report-like, or thesis-like draft | Compression revision | Diagnosis table, keep/delete/merge/table/supplement decisions, revised outline or rewritten sample |
| Literature review, related work, gap, or contribution framing | Synthesis mode | Thematic structure, gap logic, representative citation functions, and draft text |
| Methods, experiment, simulation, variables, formulas, equations, notation, metrics, model definitions, or reproducibility writing | Methods mode | Design logic, variables/controls/metrics map, equation/notation needs, reproducibility details, and prose or table-ready content |
| Results, figures, tables, discussion, limitations, or conclusion writing | Evidence-interpretation mode | Claim-evidence-boundary map, result/discussion separation, and draft text |
| Reviewer response, rebuttal, appeal-like revision, or response letter | Reviewer-response mode | Comment/action/location/response structure, with unresolved author-input flags |

For small one-paragraph edits, keep the mode decision implicit but still preserve the relevant output contract. For substantial tasks, show the mode or pre-writing brief before final prose unless the user explicitly asks to skip planning.

## Default Mode

Default to **journal-style manuscript mode** unless the user explicitly asks for an exhaustive material draft, thesis chapter, or background report.

In journal-style manuscript mode:

- Write to a narrow argument, not to preserve every piece of available material.
- For non-review empirical, experimental, simulation, modeling, or engineering application papers, start from the closest engineering article architecture rather than forcing one fixed template. IMRaD is common, but `Results and Discussion` may be combined when each result is interpreted locally and a standalone Discussion would only repeat results. Add a separate Literature Review / Related Work section only when the venue requires it or the literature synthesis is too complex for the Introduction.
- Prefer fewer, stronger claims over comprehensive coverage.
- Put detailed parameter listings, secondary checks, and repeated cautions in tables, appendices, or notes unless they are central to the claim.
- Treat "complete" as logically complete, not long.
- If a previous draft is verbose, first diagnose duplication and section-role overlap before adding text.

Use **full material draft mode** only when the user asks to collect all evidence, produce a long internal draft, or preserve exploratory reasoning. Mark it clearly as a material draft, not a final manuscript.

## Whole-Paper First

For any substantial paper task, reason from the full manuscript before drafting a section.

Before writing section text, define:

1. **Manuscript type**: journal article, thesis chapter, conference paper, review, methods paper, or report.
2. **Section architecture**: the major sections and likely subsections.
3. **Information flow**: what each section must add that previous sections have not already said.
4. **Evidence map**: which figures, tables, experiments, references, or claims belong to each section.
5. **Compression plan**: what belongs in appendices, supplements, tables, captions, or notes rather than main text.

Do not write sections as isolated essays. Each section should be a necessary step in the paper-level argument. When revising an existing draft, first check whether the whole-paper architecture matches the target form; if it does not, restructure before sentence polishing.

For full-paper drafting or major revision, produce a short **pre-writing brief** before prose unless the user explicitly asks to skip planning. The brief should state target article type, central claim, target structure, core contribution, evidence chain, reference strategy, and what will be omitted or moved to supplements.

## Manuscript Spine

For whole-paper drafting, major revision, journal conversion, thesis-to-paper rewriting, or from-materials writing, define the manuscript spine before writing prose:

1. **Central problem**: the concrete uncertainty or problem the paper addresses.
2. **Specific gap**: what prior work, current practice, or the existing draft does not yet resolve.
3. **Core contribution**: the narrow contribution the available evidence can support.
4. **Evidence chain**: figures, tables, experiments, datasets, models, references, or reviewer actions that support the contribution.
5. **Claim boundary**: what the paper must not overclaim.

If the spine is uncertain, present it as a short assumption and ask for confirmation before a large rewrite. For small section edits, keep the spine implicit but preserve its constraints.

## Output Contracts

Use the output shape that matches the selected task mode:

- **Pre-writing brief**: target article type, central claim, target structure, core contribution, evidence chain, citation strategy, and material to omit or move.
- **Structural diagnosis**: table with `Issue`, `Evidence in draft`, `Why it weakens the paper`, and `Action`.
- **Compression decision table**: classify material as `keep`, `merge`, `delete`, `table`, `caption`, `appendix`, or `supplement`.
- **Claim-evidence-citation map**: for substantial claims, map `Claim`, `User evidence`, `Citation function`, `Section`, and `Boundary`.
- **Equation/notation block**: for engineering formulas, provide the equation role, LaTeX math, symbol definitions, units, assumptions or scope, and the manuscript claim or method step it supports.
- **Section draft**: provide publication-ready text first; add short notes only for assumptions, unsupported claims, missing evidence, or boundary choices.
- **Polishing/translation**: preserve the author's intended claim, adapt rhetoric to the target language, and list any narrowed claim.
- **Reviewer response**: preserve each reviewer comment, assign a stable ID, map the action, cite the manuscript location or placeholder, then draft the response.
- **Citation guidance**: state the citation function before adding or moving references; never fabricate bibliographic details.

Do not bury the answer under process notes. The diagnostic or planning block should be short enough to improve the final text, not replace it.

## Reference Selection

Load only the references needed for the task:

- For bilingual style, English SCI/SSCI writing, Chinese academic writing, or translation/adaptation: read `references/bilingual-writing-rules.md`.
- For full-paper architecture, article type, section order, thesis-vs-journal structure, or whole-paper planning: read `references/whole-manuscript-architectures.md`.
- For general writing workflow, argument chain, or writing from scattered materials: read `references/writing-workflow.md`.
- For top-journal section patterns, title, abstract, introduction, methods, results, discussion, conclusion, or section-by-section drafting: read `references/top-journal-section-patterns.md`.
- For literature review, related work, paper comparison, or synthesis from many papers: read `references/literature-review.md`.
- For research gap, novelty, contribution statements, or introduction logic: read `references/research-gap-and-contribution.md`.
- For methodology, experiment design, simulation setup, variables, indicators, reproducibility, or ablation/sensitivity: read `references/experiment-methods.md`.
- For formulas, equations, notation, symbols, units, metric definitions, model formulation, objective functions, constraints, data-processing formulas, or mathematical definitions in engineering manuscripts: read `references/engineering-equations-and-notation.md`.
- For results, figures/tables, discussion, limitations, or conclusion: read `references/results-and-discussion.md`.
- For whole-draft diagnosis, paper scoring, reviewer-style audit, or deciding what to revise first: read `references/paper-quality-review.md`.
- For adapting to a target journal family or deciding target-journal fit: read `references/target-journal-fit.md`.
- For final polishing, logical diagnosis, abstract/title revision, or reviewer response: read `references/revision-and-polishing.md`.
- For manuscript spine confirmation, claim-evidence-citation mapping, figure contracts, section-aware audit, or pre-delivery checks: read `references/manuscript-spine-and-audit.md`.
- For academic terms, phrase banks, and Chinese-English equivalents: read `references/terminology-and-phrases.md`.
- For traffic engineering, autonomous driving, mixed traffic flow, SUMO, car-following, or transport simulation examples: read `references/transport-automation-example.md`.
- For traffic simulation, AV/CAV, SUMO, car-following, lane-changing, bottleneck, merging, or mixed-traffic journal manuscripts: read `references/transport-simulation-journal-template.md`.
- For turning a verbose material draft, thesis-like draft, or research report into a journal-style manuscript: read `references/material-to-journal-revision.md`.

## Citation Placement by Manuscript Type

Before adding or moving citations, decide whether references are the paper's primary evidence or supporting context.

For **review papers, meta-analyses, bibliometric papers, and literature-synthesis papers**, citations are the main evidence base. They may appear throughout most body sections because the argument is built from comparing, classifying, and interpreting prior studies. Even then, citations should be organized by theme, method, finding, disagreement, or gap rather than as a paper-by-paper list.

For **empirical, experimental, simulation, modeling, algorithm, and other technical papers**, citations should usually be concentrated by function:

- **Introduction / Background**: establish practical importance, prior knowledge, disagreement, and the research gap.
- **Literature Review / Related Work, if used**: synthesize representative studies by theme and prove why the current study is needed.
- **Methods / Methodology**: cite datasets, instruments, software, models, protocols, metrics, calibration sources, parameter sources, and established procedures.
- **Results**: cite sparingly, only when directly comparing the current finding with prior findings or when a cited benchmark is part of the result interpretation.
- **Discussion**: cite studies that explain agreement, contradiction, mechanism, implication, or boundary conditions.
- **Conclusion**: normally avoid new citations. Do not introduce new literature as new evidence in the final section.
- **Abstract**: normally avoid citations unless the journal, discipline, or article type explicitly expects them.

Avoid attaching long citation chains to generic background claims, placing citations in Results merely to show familiarity with the field, or using citations to compensate for missing evidence in the current study.

## Core Writing Rules

1. **Every section must answer a job-specific question.**
   - Introduction: why this problem matters and what gap remains.
   - Literature review: what has been done, how streams differ, and what remains unresolved.
   - Methods: how the claim can be tested or reproduced.
   - Results: what evidence answers each research question.
   - Discussion: why the results occurred, what they imply, and where they do not apply.
   - Conclusion: what was found and what contribution remains after limitations.

2. **Use a claim-evidence-boundary pattern.**
   Make a claim, tie it to evidence, then state the boundary. Avoid broad claims unsupported by the current data.

   For major claims, also decide the citation function: background, gap, method source, benchmark, mechanism explanation, limitation, application context, or discussion comparison. Do not attach references to a claim until their function is clear.

3. **Do not write paper-shaped filler.**
   Avoid generic openings, literature laundry lists, exaggerated novelty, unsupported causal language, and conclusions that merely repeat figures.

4. **Write from the reader's uncertainty.**
   A strong paper anticipates what the reader might doubt: parameter validity, comparison fairness, statistical robustness, external validity, missing baselines, and interpretation limits.

5. **Separate observation from interpretation.**
   Observation reports what the data show. Interpretation explains mechanism or implication. Boundary states what the data do not prove.

6. **Assign each major idea one home.**
   A claim, limitation, definition, or motivation may be introduced briefly in multiple places, but it should be fully developed only once. Before drafting or revising, decide where each recurring idea lives:
   - Motivation and gap: Introduction.
   - Literature streams and unresolved issue: Literature review.
   - Design choices and controls: Methods.
   - Numerical evidence: Results.
   - Mechanism, implication, and boundaries: Discussion.
   - Durable takeaways: Conclusion.

7. **Use boundary statements sparingly.**
   Boundaries protect claims, but repeated defensive caveats make a paper bloated. State a boundary where the reader needs it to interpret evidence. Do not repeat the same caveat in the abstract, introduction, methods, results, discussion, and conclusion unless each occurrence is shorter and role-specific.

8. **Compress before polishing.**
   When a draft feels verbose, do not merely improve sentences. First remove duplicated claims, merge overlapping subsections, demote secondary material, and shorten topic sentences. Only then polish wording.

9. **Do not use all cited papers just because they are available.**
   Top-journal writing selects the minimum set of references needed to support the argument. In review papers, the evidence base may be citation-dense, but it still needs thematic synthesis. In technical papers, distribute citations by function: front-end positioning, method/source justification, and discussion-level comparison. Avoid citation padding, exhaustive literature coverage, and long "also related" chains unless writing a dedicated review.

10. **Use top-down and bottom-up writing together.**
   Top-down: start with the paper's argument, section architecture, and target article type. Bottom-up: use data, figures, references, and experiments to fill only the sections where they are needed. If the available material does not support the planned architecture, revise the architecture instead of stretching the text.

11. **Do not let materials dictate the prose order.**
   Do not organize manuscript sections by simply walking through figures, tables, equations, metrics, experiments, or citations in the order they appear. Organize Results by research question, claim, mechanism, or evidence cluster; organize Methods formulas by reproducible method decision or metric family. Use figures, tables, and equations as support inside that logic, not as the logic itself.

12. **Make each paragraph earn its place.**
   Each paragraph should have one main message and a clear role in the section. For substantial drafts, mentally reverse-outline the section after writing: if a paragraph's function cannot be named as gap, design choice, evidence, mechanism, boundary, or transition, merge, move, or delete it.

13. **Write engineering Methods as design, rationale, and validation role.**
   For engineering manuscripts, Methods should not be a software, equipment, or parameter inventory. State what was designed or tested, why the design choices are appropriate, and how they support reproducibility, fair comparison, mechanism isolation, validation, robustness, or application assessment.

14. **Choose the Discussion architecture deliberately.**
   A standalone Discussion is useful when mechanism explanation, literature comparison, implications, and boundaries need a separate conceptual section. For compact engineering papers, use `Results and Discussion` or `Results and Analysis` when each result can be interpreted immediately without duplicating a later Discussion. Do not keep a Discussion section that only restates numbers.

15. **Anchor every main figure and table in prose.**
   Figures and tables may appear in Introduction, Methods, Results, Discussion, or other body sections, but they should not be orphaned. Do not make a figure or table the first substantive item after a section or subsection heading unless a target template explicitly requires it. In manuscript prose, provide lead-in text before the visual to state the question, claim, comparison, or method decision it supports, and provide uptake text after the visual to interpret the key observation, design implication, boundary, or transition. Captions support this work but do not replace manuscript explanation.

16. **Formalize engineering definitions when prose would be ambiguous.**
   In engineering, simulation, modeling, algorithm, and technical empirical papers, actively decide whether models, metrics, objective functions, constraints, data processing, or statistical definitions need equations. Define every symbol and unit needed for reproducibility. Do not invent formulas without user evidence; ask, flag assumptions, or mark the equation as a candidate definition.

17. **Run a light pre-delivery audit.**
   Before presenting substantial prose or a revision plan, check for unsupported claims, citation padding, result/discussion role mixing, unnecessary standalone Discussion, conclusion overclaiming, repeated caveats, paragraph role ambiguity, section role overlap, figure-by-figure result dumping, orphaned or unanchored figures/tables, and equation dumping. Fix issues directly when possible; otherwise flag the exact missing evidence or user decision.

18. **Default to paragraph-style journal conclusions.**
   For journal-style manuscripts, write conclusions as compact prose paragraphs by default. Do not format conclusions as `(1)`, `(2)`, `(3)`, `1.`, `2.`, `3.`, or `第一/第二/第三` unless the user explicitly asks for numbered conclusions, a provided target journal/template requires numbering, or the output is for a thesis/course report that requires enumerated findings.

## Top-Journal Pattern

High-level papers usually do not say "we did many things." They build a narrow, testable argument:

```text
Important problem
-> unresolved gap in existing literature
-> specific research question
-> method designed to isolate that question
-> evidence organized by research question
-> mechanism/implication
-> limitations and future work
```

Use this pattern for both Chinese and English, but adapt style:

- Chinese: clearer transitional logic and moderate context-building are acceptable.
- English: stronger topic sentences, shorter claims, explicit gap/contribution sentences, and less rhetorical padding.

## Anti-Bloat Checks

Before delivering a manuscript section or revision, check:

- Can the central argument be stated in one sentence?
- Does each section have a distinct job, or do two sections explain the same point?
- Is any paragraph mainly saying "this is important" without new evidence, mechanism, or decision?
- Are the same limitations repeated in more than two sections?
- Are methods details in prose that would be clearer as a table?
- Are Results organized as a figure/table sequence rather than a research-question or claim sequence?
- Does each paragraph have one identifiable message and section role?
- Is a standalone Discussion necessary, or is it repeating result numbers?
- Are formulas stacked as a metric list without purpose, scope, and interpretation prose?
- Can the conclusion be reduced to a compact prose synthesis of the supported findings without losing the contribution?

If two or more checks fail, revise structure before adding content.

## Revision Path for Verbose Drafts

When the user says a draft feels bloated, repetitive, report-like, thesis-like, or not like a journal paper:

1. Diagnose paper type mismatch first.
2. Map repeated claims and decide their single home.
3. Identify the main figure/table chain.
4. Decide what to delete, merge, table, caption, appendix, or supplement.
5. Rewrite high-level structure before polishing paragraphs.

Do not defend the existing text just because each section is locally correct. A manuscript can be locally sound and globally weak.

## Output Discipline

When drafting, provide publication-ready text unless the user asks for notes. When diagnosing, lead with structural issues before sentence-level edits. When revising, preserve the user's intended claim unless it is unsupported; if unsupported, narrow it rather than embellish it.

Follow the selected task mode's output contract. For substantial tasks, include enough diagnosis to make the revision defensible; for small edits, keep diagnosis brief and prioritize the revised text.

Default responses are chat-ready Markdown academic text. Do not create `.docx`, `.tex`, `.pdf`, or other manuscript files unless the user explicitly asks for file generation or conversion.

For paper sections, include figure/table references only when the user has provided or identified the evidence. Do not invent numerical results, citations, journal names, or "top journal" claims.
