# Bilingual Academic Writing Rules

## Language Decision

- If the user requests Chinese, write in Chinese academic style.
- If the user requests English, write in English journal style.
- If the user asks for translation, perform rhetorical adaptation, not literal translation.
- If language is unspecified, use the user's current language unless the target journal/thesis context implies otherwise.

## Chinese Academic Style

Chinese academic writing can use more explicit context-building, but should still be concise and evidence-led.

Prefer:

- “已有研究主要从……展开，但对……关注不足。”
- “为识别……的影响，本文进一步控制……”
- “结果表明……，但该结论受……条件约束。”
- “这说明……并非简单由……决定，而是受到……共同影响。”

Avoid:

- “随着社会经济的快速发展……” unless the paper truly needs a broad macro background.
- “具有重要理论意义和现实意义” without specifying what the meaning is.
- “显著提高”“大幅改善”“有效验证” without metric, comparison, or boundary.
- Repeated “本文首先……其次……最后……” when a more argumentative structure is possible.

### Chinese Sentence Skeleton

Treat `主谓宾定状补` as a diagnostic vocabulary, not a six-slot template. A sentence may omit a subject recoverable from the immediately preceding context and may not need an object or complement, but its semantic skeleton must remain unambiguous.

Before delivery, check:

- **Subject**: identify who or what performs the action, has the property, or undergoes the change. Restore the subject after a subject shift; do not add “本文” mechanically to every sentence.
- **Predicate**: use an explicit action, state, or relation. Do not deliver a heading-like noun phrase as a sentence.
- **Required completion**: include the object, result, degree, comparison baseline, condition, or scope needed to complete the claim.
- **Modifier attachment**: make every 定语、状语和补语 point to the intended noun or action; shorten nested `的` phrases when the center noun is hard to locate.
- **Reference**: replace ambiguous `其/该/这种/上述/这` with a specific noun phrase when more than one antecedent is possible.
- **Clause relation**: split comma-spliced clauses or add a precise logical connector when the relation is not self-evident.

Use these repair patterns:

| Faulty pattern | Problem | Repair direction |
|---|---|---|
| `通过构建不同渗透率场景，并分析交通效率。` | Only an introductory adverbial; no main subject-predicate clause | `本研究构建了不同渗透率场景，并分析了交通效率。` |
| `仿真结果表明，随着换道强度增加，降低了道路通行能力。` | The subject of `降低` is missing | `仿真结果表明，随着换道强度增加，道路通行能力逐渐降低。` |
| `基于跟驰间距与换道强度耦合作用的交通效率影响分析。` | Nominal fragment; no predicate | `本研究分析了跟驰间距与换道强度的耦合作用对交通效率的影响。` |
| `该结果说明其具有显著影响。` | `该结果` and `其` lack clear referents or an effect object | Name the result, influencing factor, affected metric, and comparison boundary explicitly |
| Several independent claims joined only by `，` | Subject drift and logical relation are hidden | Split the sentence or mark coordination, contrast, cause, or progression explicitly |

## English Journal Style

English papers should be direct, explicit, and claim-controlled. Use topic sentences. Put the gap and contribution in visible sentences.

Prefer:

- “However, these studies typically treat the components as a homogeneous class, leaving the role of unit-level heterogeneity unclear.”
- “To isolate the primary effect, the secondary factor was held fixed across the test conditions.”
- “The results suggest a threshold-like effect rather than a linear dose-response relationship.”
- “This finding should be interpreted as a simulation-based upper bound, not as a near-term field prediction.”

Avoid:

- “With the rapid development of society/technology...”
- “There are many studies about...”
- “The results are very obvious/significant” without statistical or practical grounding.
- Direct Chinese-to-English structures such as “Based on this, this paper...” repeated across paragraphs.

For sentence integrity, require a subject and finite verb in every independent sentence; repair fragments, subject shifts, and dangling introductory modifiers. Replace bare `this/these` with a concrete head noun when needed, and unpack long noun stacks when they hide the action, object, or relation.

Use these repair patterns:

| Faulty pattern | Problem | Repair direction |
|---|---|---|
| `Based on the simulation results.` | Prepositional fragment; no main subject or finite verb | `The simulation results show that ...`, only when the finding is supplied |
| `Using SUMO, traffic efficiency was evaluated under different penetration rates.` | Dangling introductory modifier and hidden agency | `We used SUMO to evaluate traffic efficiency under different penetration rates.` or use a clear passive construction |
| `This indicates a significant improvement.` | Vague referent; missing metric, baseline, and condition | Name the specific finding, affected metric, comparator, and applicable condition |
| `A vehicle behavior parameter impact mechanism analysis was conducted.` | Dense noun stack hides the action and relation | `We analyzed how vehicle-behavior parameters affect [specified outcome].` |

## Translation and Adaptation

Translation here means rhetorical adaptation, not literal conversion. Adapt the argument structure to the target language and venue; never make the target text claim more than the source evidence supports.

When the target is manuscript prose, output the adapted paper text rather than translating author-facing commentary. Do not carry over source phrases that merely explain how to understand a sentence or announce what the next paragraph will do; retain them only when they express a real logical relation, scope condition, or methodological purpose.

See also: keep one English term per concept using the glossary guidance in `terminology-and-phrases.md`; for sentence-level polishing principles use `revision-and-polishing.md`; for abstract skeletons use `top-journal-section-patterns.md`.

### Three-Pass Translation Procedure

This is the master procedure for sentence- and paragraph-level translation. Run three internal passes and output only the final version:

1. **Literal pass (直译)**: translate faithfully to capture the full meaning, keeping established terms and proper names untranslated. Do not polish yet.
2. **Diagnosis pass (问题识别)**: mark awkward phrasing, over-long sentences, wrong rhetorical order, and any claim/evidence/boundary problem. Apply the intent decomposition and the repair table below.
3. **Reinterpretation pass (意译/重构)**: rewrite into natural target-language manuscript prose — reordered by section function, hedged to match the source evidence, and de-AI'd. This is the delivered text.

The three passes are internal; deliver the reinterpreted version, not the literal draft or the notes (unless the user asks to see them).

### Translate Intent, Not Syntax (Chinese to English)

Chinese academic notes often pack background, motivation, method, and implication into one long sentence. Do not translate clause by clause. First decompose each source sentence or paragraph into its functional parts:

- claim
- evidence
- condition / scope
- comparison / baseline
- implication
- limitation / boundary

Then write the English in the order the target section requires, not the order of the Chinese sentence. The output should read like a manuscript paragraph built from the author's facts, not like a translated sentence.

Core moves:

1. Decompose the source into the functional parts above.
2. Move the main claim earlier; lead paragraphs with a topic sentence.
3. Convert implicit logic into explicit connectors: however, therefore, by contrast, in this setting, under this assumption.
4. Replace “本文” overuse with “this study,” “we,” or passive constructions depending on venue style.
5. Preserve limits. Do not make English sound stronger than the Chinese evidence.

### Chinese-Draft Repair Table

| Chinese-draft pattern | Repair in English |
|---|---|
| Broad importance stated before any concrete object | Name the system or problem earlier |
| Method list placed before the research gap | Move the gap before the method |
| `显著提高 / 明显改善 / 大幅` without a baseline | Add the comparator, or soften the verb (improved → increased by X relative to …) |
| `首次 / 创新性` without scope | Replace with a bounded novelty claim (to our knowledge, under …) |
| Mechanism inferred from correlation | Use `suggests`, `is consistent with`, or ask for mechanistic evidence |
| Results mixed with implications | Put the observation in Results and the meaning in Discussion |
| `通过……，本文……` repeated across paragraphs | Vary structure; lead with the finding, not the procedure |
| Chinese has no grammatical tense | Assign English tense by section: past for methods and results, present for established facts and for what the paper does |
| Chinese marks no articles or plurals | Check every noun for article (a / the / none) and singular vs plural |
| Comma-spliced run-on clauses (逗号流水句) | Break into separate sentences, or join with a proper connector — not a bare comma |

### English House-Style Discipline

When producing the English version, also enforce:

- **Sentence length**: keep most sentences within about 25-30 words; Chinese-to-English drafts most often fail by stacking clauses. Split the longest sentence in each paragraph first.
- **Hedging ladder**: match verb strength to evidence, mirroring the Chinese gradient — `表明` → show/demonstrate (direct support); `说明` → suggest/indicate (explanatory inference); `提示` → may reflect/point to (cautious implication). Do not upgrade the hedge in translation.
- **British vs American English**: choose one before drafting (e.g., analyse/analyze, modelling/modeling, behaviour/behavior) and keep it consistent across the manuscript; follow the target journal when known.
- **Overclaim control**: qualify or remove prove, conclusively, unprecedented, best, and unqualified first unless the evidence and scope are unusually strong.
- **Do not translate established terms**: keep standard acronyms, discipline terms, and proper names in their conventional form (e.g., AI, LLM, API, FEM, CFD, PID, SNR, gene/chemical symbols, SI units), and keep product/tool/library/dataset names as-is (e.g., SUMO, ABAQUS, PyTorch, ImageNet). Translate the surrounding prose, not the canonical term.
- **Preserve non-prose elements**: keep citations, equation labels, figure/table numbers, and already-defined symbols unchanged; translate the surrounding text only.
- **Naturalize and de-AI the output**: a literal or LLM-style translation often reads stiff. Remove generic AI tells (Moreover/Furthermore chains, "plays a crucial role", "it is worth noting that", empty intensifiers), vary sentence openings, and make the prose read as if written by a domain author in the target language.

### English to Chinese

1. Avoid mechanical word order.
2. Preserve the claim-evidence-boundary logic.
3. Use “研究对象、变量、场景、指标、边界” to make methods and results clear.
4. Do not inflate modest English claims into broad Chinese conclusions.

### Workflow and Author Notes

For substantial translation tasks:

1. Summarize the author's intended claim in the source language.
2. Identify missing evidence or an unstated boundary.
3. Draft the target-language paragraph by function, not by clause order (via the three-pass procedure).
4. Add a short note (in the author's language) explaining any structural change, so the author can verify the intent was preserved.

(Techniques here — intent-not-syntax decomposition, the Chinese-draft repair table, the three-pass 直译/问题识别/意译 procedure, the keep-terms-untranslated rule, and de-AI naturalization — are adapted and rewritten from several open-source community skills, including `nature-skills` and the `claude-code-settings` translate skill, then integrated into this skill's framework.)

## Bilingual Abstract Pattern

Chinese abstract:

```text
研究背景/问题 -> 研究目的 -> 方法与场景 -> 主要结果 -> 结论与意义
```

Default rhythm for Chinese journal abstracts:

```text
第1句：交代背景或问题，不展开综述。
第2-4句：交代研究目的、方法、场景/数据和主要比较内容。
第5-11句：简述主要结论，优先写有证据支撑的结果，可包含关键定量信息。
```

Aim for about 250-300 Chinese characters unless the journal specifies another length. Treat the sentence count as a pacing guide, not a rigid template.

English abstract:

```text
Problem/gap -> objective -> methods/data -> key quantitative findings -> contribution/implication
```

English abstracts usually need fewer broad background sentences and more explicit method/result sentences.
