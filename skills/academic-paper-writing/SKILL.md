---
name: academic-paper-writing
description: Use when the user asks for formal academic manuscript, thesis, journal, SCI/SSCI, or conference-paper writing; section drafting or revision; abstract/introduction/methods/results/discussion/conclusion rewriting; methods, formulas, equations, notation, metrics, or model-definition writing; academic polishing; manuscript compression; reviewer response or rebuttal; or Chinese requests such as 论文润色、改摘要、改引言、期刊论文压缩、审稿意见回复.
---

# Academic Paper Writing

This skill writes like a rigorous academic author, not a generic editor. The goal is a defensible paper argument: research problem, literature gap, method, evidence, interpretation, contribution, and limitations. SKILL.md is the control layer — it decides the task type, routes to the right reference file, and enforces a few non-negotiable rules. Detailed how-to lives in `references/` and is loaded on demand.

It supports both Chinese and English academic writing across engineering and technical fields. Do not simply translate between languages; adapt the rhetorical structure to the target language and publication context.

## Trigger Boundary

Use this skill when the user asks for it by name, or for clear academic-writing requests that do not name it: "revise this abstract", "make this introduction more journal-like", "compress this manuscript", "write a reviewer response", "论文润色", "改摘要", "改引言", "期刊论文压缩", "学术论文改写", "审稿意见回复".

Do not trigger for casual research brainstorming, literature reading, experiment planning, simulation setup, code work, or general technical discussion unless the user frames the task as academic writing or asks for this skill.

## First Decisions

Before writing, identify:

1. **Target language**: Chinese, English, or bilingual. If unspecified, use the user's current language.
2. **Paper type and target form**: journal paper, thesis chapter, conference paper, literature review, experiment paper, review response, or polishing task; and whether the user needs a full material draft, journal-style manuscript, thesis-style chapter, or final compressed version.
3. **Discipline and evidence type**: simulation, experiment, survey, dataset analysis, modeling, algorithm, engineering system/application, theoretical, or review.
4. **Engineering subtype when relevant**: physical experiment/test, simulation/numerical study, modeling/algorithm paper, engineering system/application paper, method-comparison paper, or review/synthesis paper.
5. **Current stage**: outline, first draft, revision, condensation, translation/adaptation, journal-style polishing, or reviewer response.

If these are unclear and the task is substantial, ask one concise question. For small edits, make a conservative assumption and state it.

## Decision Axes

For substantial tasks, classify the request before choosing references or writing:

| Axis | Values |
|---|---|
| `task_mode` | draft, revise, polish, compress, translate/adapt, audit, reviewer-response |
| `paper_type` | empirical, experiment, simulation, algorithm, modeling, engineering-system, theoretical, review, thesis-to-paper, report |
| `section` | title, abstract, introduction, literature review, methods, results, discussion, conclusion, response letter, whole manuscript |
| `language` | zh, en, bilingual, zh-to-en, en-to-zh |

Use the axes to load only the relevant reference files and to enforce section-specific duties. Do not apply the same polishing strategy to all sections.

## Task Mode Routing

Choose one task mode. If multiple apply, handle the highest level first: full-paper structure before section drafting, structural revision before sentence polishing, evidence/citation diagnosis before citation placement.

| User intent | Default mode | Required output |
|---|---|---|
| Full paper, major revision, journal conversion, or thesis-to-paper rewrite | Whole-manuscript planning | Pre-writing brief, target structure, evidence chain, compression plan, then prose or revision plan |
| Section drafting or rewriting | Section-level drafting | Section role note, publication-ready text, missing-evidence/boundary notes when needed |
| Abstract, title, conclusion, or short polishing | Focused polishing | Assumptions, revised text, brief note on any claim narrowed or unsupported |
| Verbose, repetitive, report-like, or thesis-like draft | Compression revision | Diagnosis table, keep/delete/merge/table/supplement decisions, revised outline or sample |
| Literature review, related work, gap, or contribution framing | Synthesis mode | Thematic structure, gap logic, representative citation functions, draft text |
| Methods, experiment, simulation, variables, formulas, equations, notation, metrics, model definitions, reproducibility | Methods mode | Design logic, variables/controls/metrics map, equation/notation needs, reproducibility details, prose or table-ready content |
| Results, figures, tables, discussion, limitations, conclusion | Evidence-interpretation mode | Claim-evidence-boundary map, result/discussion separation, draft text |
| Reviewer response, rebuttal, or response letter | Reviewer-response mode | Comment/action/location/response structure, with unresolved author-input flags |

For small one-paragraph edits, keep the mode implicit but preserve its output contract. For substantial tasks, show the mode or pre-writing brief before final prose unless the user asks to skip planning.

## Default Mode

Default to **journal-style manuscript mode** unless the user explicitly asks for an exhaustive material draft, thesis chapter, or background report.

In this mode: write to a narrow argument; prefer fewer, stronger claims over comprehensive coverage; put detailed parameter listings, secondary checks, and repeated cautions in tables/appendices/notes; treat "complete" as logically complete, not long. For non-review empirical/experimental/simulation/modeling/engineering papers, start from the closest engineering article architecture rather than forcing one template — IMRaD is common, but `Results and Discussion` may be combined, and a separate Literature Review is added only when the venue requires it or the synthesis is too complex for the Introduction.

Use **full material draft mode** only when the user asks to collect all evidence or preserve exploratory reasoning, and mark it clearly as a material draft.

## Whole-Paper First

For any substantial task, reason from the full manuscript before drafting a section. Define manuscript type, section architecture, information flow (what each section adds), evidence map, and compression plan. Do not write sections as isolated essays.

For full-paper drafting or major revision, produce a short **pre-writing brief** (target article type, central claim, target structure, core contribution, evidence chain, reference strategy, what is omitted/moved) unless the user asks to skip planning. For architecture choices read `references/whole-manuscript-architectures.md`; for the manuscript spine, claim-evidence-citation map, and pre-delivery audit read `references/manuscript-spine-and-audit.md`.

## Output Contracts

Use the shape that matches the task mode (full templates in `references/manuscript-spine-and-audit.md`):

- **Pre-writing brief**: article type, central claim, structure, contribution, evidence chain, citation strategy, material to omit.
- **Structural diagnosis**: table of `Issue / Evidence in draft / Why it weakens the paper / Action`.
- **Compression decision table**: classify material as keep / merge / delete / table / caption / appendix / supplement.
- **Claim-evidence-citation map**: `Claim / User evidence / Citation function / Section / Boundary`.
- **Equation/notation block**: role, LaTeX math, symbol definitions, units, scope/assumptions, manuscript link.
- **Section draft**: publication-ready text first; short notes only for assumptions, unsupported claims, missing evidence, or boundary choices.
- **Reviewer response**: preserve each comment, assign a stable ID, map the action, cite location or placeholder, then respond.

Do not bury the answer under process notes. Diagnostic blocks should be short enough to improve the final text, not replace it.

## Reference Selection

Load only the references needed:

- Bilingual style, English SCI/SSCI, Chinese academic writing, translation/adaptation → `references/bilingual-writing-rules.md`.
- Full-paper architecture, article type, section order, thesis-vs-journal structure → `references/whole-manuscript-architectures.md`.
- General writing workflow, argument chain, writing from scattered materials → `references/writing-workflow.md`.
- Top-journal section patterns (title, abstract, introduction, methods, results, discussion, conclusion) → `references/top-journal-section-patterns.md`.
- Literature review, related work, paper comparison, synthesis → `references/literature-review.md`.
- Research gap, novelty, contribution statements, introduction logic → `references/research-gap-and-contribution.md`.
- Methodology, experiment design, simulation setup, variables, indicators, reproducibility, ablation/sensitivity → `references/experiment-methods.md`.
- Formulas, equations, notation, symbols, units, metric/model definitions, objectives, constraints → `references/engineering-equations-and-notation.md`.
- Results, figures/tables, discussion, limitations, conclusion → `references/results-and-discussion.md`.
- Whole-draft diagnosis, paper scoring, reviewer-style audit, what to revise first → `references/paper-quality-review.md`.
- Target journal family or fit decisions → `references/target-journal-fit.md`.
- Final polishing, logical diagnosis, abstract/title revision, reviewer response → `references/revision-and-polishing.md`.
- Manuscript spine, claim-evidence-citation mapping, figure contracts, section-aware audit, pre-delivery checks → `references/manuscript-spine-and-audit.md`.
- Academic terms, phrase banks, Chinese-English equivalents → `references/terminology-and-phrases.md`.
- Turning a verbose material/thesis/report draft into a journal manuscript → `references/material-to-journal-revision.md`.
- A full empirical/experimental/simulation engineering manuscript (IMRaD template, evidence chain, reviewer-attack checklist) → `references/engineering-empirical-and-simulation-template.md`.
- A concrete, field-appropriate framing (mechanical/materials/civil, electrical/control/automation, computer/AI/algorithms, energy/chemical/environmental, or traffic) → `references/engineering-domain-examples.md`.

## Citation Placement

Before adding or moving citations, decide whether references are the paper's primary evidence or supporting context.

For **review/meta-analysis/bibliometric/synthesis papers**, citations are the main evidence and may appear throughout, but organized by theme, method, finding, disagreement, or gap — never as a paper-by-paper list.

For **empirical/experimental/simulation/modeling/algorithm/technical papers**, concentrate citations by function: Introduction (importance, prior knowledge, gap); Literature Review if used (synthesis by theme); Methods (datasets, instruments, software, models, protocols, metric/calibration sources); Results (sparingly, only for direct comparison); Discussion (agreement, contradiction, mechanism, implication, boundary); Conclusion and Abstract (normally none). Avoid long citation chains on generic background, citations in Results to show familiarity, or citations that compensate for missing evidence. Detail in `references/manuscript-spine-and-audit.md`.

## Core Writing Rules

These are the non-negotiable principles; their detailed application is in the reference files.

1. **Each section answers a job-specific question.** Introduction: why the problem matters and what gap remains. Literature review: what was done, how streams differ, what is unresolved. Methods: how the claim is tested or reproduced. Results: what evidence answers each question. Discussion: why results occurred, what they imply, where they do not apply. Conclusion: what was found and what contribution survives limitations.
2. **Use claim-evidence-boundary.** Make a claim, tie it to evidence, state the boundary. For major claims, decide the citation function before attaching references.
3. **No paper-shaped filler.** Avoid generic openings, literature laundry lists, exaggerated novelty, unsupported causal language, and conclusions that merely repeat figures.
4. **Write from the reader's uncertainty.** Anticipate doubts: parameter validity, comparison fairness, robustness, external validity, missing baselines, interpretation limits.
5. **Separate observation, interpretation, and boundary.**
6. **Assign each idea one home.** Develop a claim/limitation/definition/motivation fully once: motivation+gap → Introduction; streams → Literature review; design+controls → Methods; numbers → Results; mechanism+implication+boundary → Discussion; durable takeaways → Conclusion.
7. **Use boundary statements sparingly.** State a boundary where the reader needs it; do not repeat the same caveat in every section.
8. **Compress before polishing.** Remove duplicated claims, merge overlapping subsections, demote secondary material before improving wording.
9. **Cite by function, not availability.** Select the minimum reference set; avoid padding and exhaustive coverage outside dedicated reviews.
10. **Combine top-down and bottom-up.** Start from argument, architecture, and article type; fill sections only where evidence is needed. If material does not support the architecture, revise the architecture.
11. **Do not let materials dictate prose order.** Organize Results by research question/claim/evidence cluster and Methods formulas by method decision or metric family — not by the order figures/tables/equations appear.
12. **Make each paragraph earn its place.** One message and a nameable role per paragraph; reverse-outline and merge/move/delete the rest.
13. **Engineering Methods = design, rationale, validation role** — not a software/equipment/parameter inventory.
14. **Choose the Discussion architecture deliberately** — standalone vs. `Results and Discussion`; never a Discussion that only restates numbers.
15. **Anchor every main figure/table in prose** — lead-in before, uptake after; captions support but do not replace explanation.
16. **Formalize engineering definitions when prose is ambiguous.** Define every symbol and unit needed for reproducibility. Never invent formulas, parameters, or values without user evidence — ask or flag a candidate definition.
17. **Run a light pre-delivery audit** for unsupported claims, citation padding, result/discussion mixing, conclusion overclaiming, repeated caveats, section overlap, figure-by-figure dumping, orphaned visuals, and equation dumping. Fix what you can; flag the exact missing input otherwise.
18. **Default to paragraph-style journal conclusions.** Do not number conclusions as `(1)/(2)/(3)`, `1./2./3.`, or `第一/第二/第三` unless the user asks, a target journal/template requires it, or the output is a thesis/course report requiring enumerated findings.

## Top-Journal Pattern

High-level papers build a narrow, testable argument rather than "we did many things":

```text
Important problem -> unresolved gap -> specific research question
-> method designed to isolate it -> evidence organized by question
-> mechanism/implication -> limitations and future work
```

Adapt by language: Chinese allows clearer transitional logic and moderate context-building; English needs stronger topic sentences, shorter claims, and explicit gap/contribution sentences. Before delivering, run the Anti-Bloat check: can the central argument be stated in one sentence? Does each section have a distinct job? Is any paragraph just "this is important"? Are limitations repeated across sections? Are Results figure-led instead of question-led? Is a standalone Discussion just repeating numbers? If two or more fail, revise structure before adding content. For verbose drafts, follow the revision path in `references/material-to-journal-revision.md`.

## Output Discipline

Provide publication-ready text unless the user asks for notes. When diagnosing, lead with structural issues before sentence-level edits. When revising, preserve the user's intended claim unless it is unsupported; if unsupported, narrow it rather than embellish it.

Default responses are chat-ready Markdown academic text. Do not create `.docx`, `.tex`, `.pdf`, or other manuscript files unless the user explicitly asks for file generation or conversion. Include figure/table references only when the user has provided or identified the evidence. Do not invent numerical results, citations, journal names, or "top journal" claims.
