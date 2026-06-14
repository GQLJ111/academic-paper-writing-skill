# Academic Paper Writing Skill

🌏 [中文](README.md) | English

This repository provides a Codex skill for **engineering academic paper writing**. It is designed to support manuscript planning, section drafting, structural revision, academic polishing, quality review, and reviewer responses.

The skill is suitable for common engineering manuscript types, including simulation studies, experimental studies, modeling papers, algorithm papers, and applied technical papers. Its purpose is not to replace the author's research judgment, but to help organize a stronger manuscript argument with clearer structure, evidence, and journal-style writing.

In terms of engineering domains, it focuses on mechanical/materials/civil engineering, electrical/control/automation, computer science/AI/algorithms, energy/chemical/environmental engineering, and traffic or automated-vehicle simulation. For other engineering fields, the same logic can be transferred by identifying the research object, variables, metrics, and scope boundaries.

## 🎯 Who This Is For

This skill is mainly intended for:

- Engineering master's students, PhD students, and early-career researchers.
- Authors preparing SCI/EI, Chinese core journal, or conference manuscripts.
- Authors converting thesis chapters, course reports, experiment notes, or material drafts into journal-style papers.
- Users revising abstracts, introductions, methods, results, discussions, conclusions, or reviewer responses.
- Users who want Codex to pay more attention to research questions, evidence chains, section roles, and claim boundaries.

It is not a generic copy-editing tool. It is biased toward **engineering research manuscripts**.

## ✨ Features

- 🧭 Whole-manuscript planning: research problem, contribution, evidence chain, and section architecture.
- ✍️ Section drafting and revision: abstract, introduction, methods, results, discussion, conclusions, and more.
- 🌐 Bilingual writing and translation adaptation: Chinese-to-English journal prose, English-to-Chinese academic prose, terminology preservation, and repair of literal translation artifacts.
- 📐 Engineering equations and notation: variables, units, metrics, models, constraints, and assumptions.
- 📊 Figure and table writing logic: avoid visual dumping and connect visuals to manuscript claims.
- 🔍 Manuscript quality review: repetition, unsupported claims, overclaiming, section-role overlap, and evidence gaps.
- 📨 Reviewer response support: response letters, point-by-point replies, and revision mapping.

## 🧠 Writing Philosophy

This skill does not encourage turning all available material into a long manuscript. It first builds a defensible paper spine:

```text
Important problem -> unresolved gap -> specific research question
-> method and experiment/simulation design -> evidence chain
-> mechanism or engineering implication -> limitations and future work
```

In practice, it tries to:

- Identify the paper type first: experiment, simulation, modeling, algorithm, engineering system, review, or thesis.
- Plan the whole manuscript before drafting individual sections.
- Place figures, tables, and equations inside the argument rather than stacking them.
- Use claim-evidence-boundary logic to control the strength of conclusions.
- Default to journal-style manuscript writing rather than report-like material accumulation.
- Use paragraph-style conclusions by default instead of forcing `(1)(2)(3)` findings.

## 🧩 Example Prompts

You can ask Codex to use this skill for tasks such as:

```text
Use $academic-paper-writing to review this manuscript structure, focusing on the research question, contribution, evidence chain, and section architecture.
```

```text
Use $academic-paper-writing to revise this Chinese abstract into a more engineering-SCI style abstract without overstating the findings.
```

```text
Use $academic-paper-writing to translate and restructure this Chinese Results paragraph into natural English journal prose, preserving terms, equation labels, and figure/table numbers while avoiding literal translation and AI-like phrasing.
```

```text
Use $academic-paper-writing to rewrite the introduction with a clearer research gap, contribution paragraph, and method logic.
```

```text
Use $academic-paper-writing to check the Methods section, especially experiment design, variables, controls, metric formulas, and reproducibility.
```

```text
Use $academic-paper-writing to revise the Results and Discussion so that the text is organized by research questions rather than by figure order.
```

```text
Use $academic-paper-writing to draft a point-by-point reviewer response with clear revision actions and manuscript locations.
```

## 📚 Built-In Reference Modules

The skill separates writing guidance into reference files that Codex can load on demand. The main groups are:

- **Whole-manuscript structure and workflow**: `whole-manuscript-architectures.md`, `writing-workflow.md`, `manuscript-spine-and-audit.md`, `material-to-journal-revision.md`.
- **Section writing and argument design**: `top-journal-section-patterns.md`, `literature-review.md`, `research-gap-and-contribution.md`, `results-and-discussion.md`, `revision-and-polishing.md`, `target-journal-fit.md`.
- **Engineering methods and evidence writing**: `engineering-empirical-and-simulation-template.md`, `experiment-methods.md`, `engineering-equations-and-notation.md`, `engineering-domain-examples.md`.
- **Bilingual writing and terminology control**: `bilingual-writing-rules.md`, `terminology-and-phrases.md`.
- **Quality review**: `paper-quality-review.md`.

These files are not intended as user-facing documentation. They are context modules for Codex to use when a specific writing task requires them.

## 💡 Usage Boundary

This skill is a writing assistant. It can help organize manuscript structure, identify logical issues, and improve academic expression, but it cannot replace the author's own research judgment, experimental design, data analysis, or academic responsibility. Please always rely on your real research evidence, reliable data, and target-journal requirements, and independently review the final manuscript content.

It does not guarantee publication and should not be used to fabricate data, citations, formulas, or unsupported conclusions. For numerical results, equations, experimental settings, references, and target-journal formatting, always follow your source materials and the journal's author guidelines.

## 📦 Installation

Recommended: ask Codex to install this skill for you. You can send Codex the following prompt:

```text
Please help me install this Codex skill from GitHub:
https://github.com/GQLJ111/academic-paper-writing-skill

The skill path is:
skills/academic-paper-writing

After installation, please remind me to restart Codex.
```

If you prefer manual installation, clone the repository and copy the skill folder into Codex's skills directory. This repository does not include a standalone `install-skill-from-github.py` installer script.

```powershell
git clone https://github.com/GQLJ111/academic-paper-writing-skill.git
$skillRoot = Join-Path $env:USERPROFILE ".codex\skills"
New-Item -ItemType Directory -Force -Path $skillRoot
Copy-Item -LiteralPath ".\academic-paper-writing-skill\skills\academic-paper-writing" -Destination $skillRoot -Recurse -Force
```

After installation, restart Codex so the skill can be picked up.

## 🔄 Updating

If you have already installed this skill and want to update it to the latest GitHub version, ask Codex to reinstall or overwrite the local copy:

```text
Please help me update this Codex skill from GitHub:
https://github.com/GQLJ111/academic-paper-writing-skill

The skill path is:
skills/academic-paper-writing

Please overwrite the old local version and remind me to restart Codex after installation.
```

For a manual update, run `git pull` in the cloned repository and copy `skills/academic-paper-writing` into `~/.codex/skills/` again.

## 📁 Repository Structure

```text
skills/
  academic-paper-writing/
    SKILL.md
    agents/
      openai.yaml
    references/
      ...
```

`SKILL.md` contains the main workflow and routing rules. The `references/` directory contains optional guidance for section writing, engineering equations, figure/table reasoning, reviewer responses, and other manuscript tasks.

## 🛠️ Design Principles

This skill is designed around several principles:

- Focus on engineering manuscripts rather than generic academic writing.
- Prioritize structure and evidence chain before sentence polishing.
- Compress and reorganize material before improving wording.
- Treat equations, figures, tables, experiment design, and engineering boundaries as first-class writing problems.
- Avoid turning a manuscript into a figure manual, equation list, or citation inventory.
- Keep "top-journal style" grounded: clarity, evidence, and boundaries matter more than exaggerated phrasing.

## 🤝 Feedback and Contributions

Suggestions, issues, and pull requests are welcome. If you use this skill in real academic writing, especially for engineering manuscripts, SCI revision, reviewer responses, or experimental-method writing, your feedback would be very helpful for improving it.

If this project is useful to you, a star would be appreciated.

## License

This project is released under the MIT License.
