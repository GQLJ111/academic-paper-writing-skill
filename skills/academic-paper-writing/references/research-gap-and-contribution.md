# Research Gap and Contribution

## What Counts as a Research Gap

A usable gap is specific, testable, and tied to evidence. It is not “there are few studies.”

Good gap components:

```text
Existing work has done X
but under assumption/context Y
so mechanism/outcome Z remains unclear
```

## Gap Types

| Gap Type | Use When | Example Form |
|---|---|---|
| Mechanism gap | Outcome known but cause unclear | “It remains unclear which behavioral parameter drives the capacity change.” |
| Heterogeneity gap | Prior work treats actors as homogeneous | “AVs are often modeled as one class despite conservative and cooperative behaviors.” |
| Scenario gap | Findings may not transfer across road contexts | “Link-level gains may not persist under merging interactions.” |
| Metric gap | Prior work relies on one metric | “Travel-time reductions may mask lower completion rates.” |
| Robustness gap | Prior work uses single parameter/scenario | “The penetration-rate effect has not been tested under sensitivity or distribution changes.” |

## Contribution Rules

Write contributions as intellectual value, not task lists.

Weak:

```text
This paper builds a SUMO model and draws several figures.
```

Strong:

```text
This paper distinguishes conservative AV and cooperative CAV car-following behaviors, showing that the same penetration rate can produce opposite efficiency effects under bottleneck and merging conditions.
```

## Contribution Pattern

Use 2-4 contributions:

1. **Conceptual contribution**: new distinction, framing, or mechanism.
2. **Methodological contribution**: experiment design, decomposition, robustness, or scenario hierarchy.
3. **Empirical/simulation finding**: key result with metric and boundary.
4. **Practical implication**: what the finding means for deployment, modeling, or evaluation.

## Chinese Contribution Phrases

- “本文的主要贡献体现在以下三个方面。”
- “不同于仅比较自动驾驶渗透率的研究，本文进一步区分……”
- “通过……实验，本文识别了……机制。”
- “结果表明……，这一发现提示……”

## English Contribution Phrases

- “This study contributes to the literature in three ways.”
- “First, it distinguishes ... rather than treating ... as a homogeneous class.”
- “Second, it decomposes ... by varying ... while controlling ...”
- “Third, it shows that ... under ..., suggesting that ...”

## Boundary Discipline

Never overstate novelty:

- Do not claim “first” unless verified.
- Prefer “extends,” “distinguishes,” “decomposes,” “tests,” “shows,” “provides evidence.”
- Add scenario boundaries: “in the simulated bottleneck setting,” “under the tested demand levels,” “with the adopted SUMO parameters.”
