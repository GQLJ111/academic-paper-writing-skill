# Academic Paper Writing Skill

🌏 [中文](README.md) | English

This repository provides a Codex skill for **engineering academic paper writing**. It is designed to support manuscript planning, section drafting, structural revision, academic polishing, and quality review.

The skill is suitable for common engineering manuscript types, including simulation studies, experimental studies, modeling papers, algorithm papers, and applied technical papers. Its purpose is not to replace the author's research judgment, but to help organize a stronger manuscript argument with clearer structure, evidence, and journal-style writing.

## ✨ Features

- 🧭 Whole-manuscript planning: research problem, contribution, evidence chain, and section architecture.
- ✍️ Section drafting and revision: abstract, introduction, methods, results, discussion, conclusions, and more.
- 📐 Engineering equations and notation: variables, units, metrics, models, constraints, and assumptions.
- 📊 Figure and table writing logic: avoid visual dumping and connect visuals to manuscript claims.
- 🔍 Manuscript quality review: repetition, unsupported claims, overclaiming, section-role overlap, and evidence gaps.
- 📨 Reviewer response support: response letters, point-by-point replies, and revision mapping.

## 💡 Usage Boundary

This skill is a writing assistant. It can help organize manuscript structure, identify logical issues, and improve academic expression, but it cannot replace the author's own research judgment, experimental design, data analysis, or academic responsibility. Please always rely on your real research evidence, reliable data, and target-journal requirements, and independently review the final manuscript content.

## 📦 Installation

Recommended: ask Codex to install this skill for you. You can send Codex the following prompt:

```text
Please help me install this Codex skill from GitHub:
https://github.com/GQLJ111/academic-paper-writing-skill

The skill path is:
skills/academic-paper-writing

After installation, please remind me to restart Codex.
```

If you prefer manual installation, use the Codex skill installer:

```powershell
python install-skill-from-github.py --repo GQLJ111/academic-paper-writing-skill --path skills/academic-paper-writing
```

After installation, restart Codex so the skill can be picked up.

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

## 🤝 Feedback and Contributions

Suggestions, issues, and pull requests are welcome. If you use this skill in real academic writing, especially for engineering manuscripts, SCI revision, reviewer responses, or experimental-method writing, your feedback would be very helpful for improving it.

If this project is useful to you, a star would be appreciated.

## License

This project is released under the MIT License.
