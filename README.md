# Academic Paper Writing Skill

🌏 中文 | [English](README_EN.md)

这是一个面向 **工科论文写作** 的 Codex skill，主要用于辅助学术论文的结构规划、章节写作、逻辑审查和语言润色。

它适合仿真研究、实验研究、建模论文、算法论文、工程应用论文等常见工科写作场景。这个 skill 的目标不是替代研究者判断，而是帮助作者把论文写得更有结构、更有证据链、更接近期刊论文的表达方式。

## ✨ 功能特点

- 🧭 论文整体结构规划：从研究问题、创新点、证据链到章节安排。
- ✍️ 章节写作与改写：支持摘要、引言、方法、结果、讨论、结论等部分。
- 📐 工程公式与符号：辅助定义变量、单位、指标、模型和约束条件。
- 📊 图表写作逻辑：避免图表堆叠，让图表真正服务论证。
- 🔍 论文质量审查：检查重复、过度声明、证据不足、章节职责混乱等问题。
- 📨 审稿意见回复：辅助组织 response letter 和逐条回复。

## 💡 使用边界

这个 skill 是一个写作辅助工具，可以帮助你梳理论文结构、检查逻辑问题、改进表达方式，但它不能替代作者自己的研究判断、实验设计、数据分析和学术责任。请始终以你的真实研究内容、可靠数据和目标期刊要求为准，并对最终论文内容进行独立判断和核查。

## 📦 安装方式

推荐方式：直接让 Codex 帮你安装。可以把下面这段话发给 Codex：

```text
请帮我从 GitHub 安装这个 Codex skill：
https://github.com/GQLJ111/academic-paper-writing-skill

skill 路径是：
skills/academic-paper-writing

安装完成后，请提醒我重启 Codex。
```

如果你想手动安装，也可以使用 Codex skill installer：

```powershell
python install-skill-from-github.py --repo GQLJ111/academic-paper-writing-skill --path skills/academic-paper-writing
```

安装完成后，请重启 Codex 以加载该 skill。

## 📁 仓库结构

```text
skills/
  academic-paper-writing/
    SKILL.md
    agents/
      openai.yaml
    references/
      ...
```

`SKILL.md` 包含核心工作流和路由规则。`references/` 目录包含按需加载的章节写作、工程公式、图表逻辑、审稿回复等参考材料。

## 🤝 交流与优化

欢迎交流、提出建议或一起优化这个 skill。你可以通过 Issue 或 Pull Request 反馈使用体验、提出改进方向，尤其欢迎来自工科论文写作、SCI 论文修改、审稿回复、实验设计表达等场景的真实问题。

如果这个 skill 对你有帮助，也欢迎 star 一下这个仓库。谢谢支持！

## License

This project is released under the MIT License.
