# Academic Paper Writing Skill

🌏 中文 | [English](README_EN.md)

这是一个面向 **工科论文写作** 的 Codex skill，主要用于辅助学术论文的结构规划、章节写作、逻辑审查、语言润色和审稿回复。

它适合仿真研究、实验研究、建模论文、算法论文、工程应用论文等常见工科写作场景。这个 skill 的目标不是替代研究者判断，而是帮助作者把论文写得更有结构、更有证据链、更接近期刊论文的表达方式。

## 🎯 适合谁使用

这个 skill 主要面向：

- 工科研究生、博士生和青年科研人员。
- 正在写 SCI/EI/中文核心/会议论文的作者。
- 需要把课程报告、学位论文材料或实验记录压缩成期刊论文的作者。
- 需要改摘要、改引言、改方法、改结果与讨论、改结论或回复审稿意见的作者。
- 希望让 Codex 在论文写作中更关注“研究问题、证据链、章节职责和边界条件”的用户。

它不是通用文案润色工具，而是偏向 **工程研究论文** 的写作辅助 skill。

## ✨ 功能特点

- 🧭 论文整体结构规划：从研究问题、创新点、证据链到章节安排。
- ✍️ 章节写作与改写：支持摘要、引言、方法、结果、讨论、结论等部分。
- 📐 工程公式与符号：辅助定义变量、单位、指标、模型和约束条件。
- 📊 图表写作逻辑：避免图表堆叠，让图表真正服务论证。
- 🔍 论文质量审查：检查重复、过度声明、证据不足、章节职责混乱等问题。
- 📨 审稿意见回复：辅助组织 response letter 和逐条回复。

## 🧠 这个 skill 的写作思路

这个 skill 不鼓励“把材料一股脑写成长文章”，而是先建立论文主线：

```text
重要问题 -> 现有研究缺口 -> 具体研究问题
-> 方法和实验/仿真设计 -> 证据链
-> 机理解释/工程意义 -> 局限性和未来工作
```

在具体写作时，它会尽量遵循以下原则：

- 先判断论文类型：实验、仿真、建模、算法、工程系统、综述或学位论文。
- 先梳理论文主线，再写单个章节。
- 将图、表、公式放在论证链条中，而不是简单堆叠。
- 用“主张-证据-边界”的方式控制结论强度。
- 默认按期刊论文风格写作，而不是写成课程报告或学位论文材料堆积。
- 默认结论采用段落式表达，不强制写成 `(1)(2)(3)`。

## 🧩 适用写作任务

你可以让 Codex 使用这个 skill 完成这些任务：

```text
使用 $academic-paper-writing 帮我审查这篇论文的整体结构，重点看研究问题、创新点、证据链和章节安排。
```

```text
使用 $academic-paper-writing 帮我把这段中文摘要改成更像工科 SCI 论文的摘要，注意不要夸大结论。
```

```text
使用 $academic-paper-writing 帮我重写引言，要求突出研究空白、本文贡献和方法逻辑。
```

```text
使用 $academic-paper-writing 帮我检查方法部分，重点看实验设计、变量、控制条件、指标公式和可复现性是否清楚。
```

```text
使用 $academic-paper-writing 帮我改结果与讨论，避免一张图接一张图地堆叠，要围绕研究问题组织证据。
```

```text
使用 $academic-paper-writing 帮我写审稿意见回复，要求逐条回应、说明修改位置，并保持语气克制。
```

## 📚 内置参考模块

skill 内部把写作知识拆成了多个按需加载的 reference，例如：

- `whole-manuscript-architectures.md`：整篇论文结构、IMRaD、讨论章节是否单独设置。
- `top-journal-section-patterns.md`：标题、摘要、引言、方法、结果、讨论、结论的章节写法。
- `engineering-empirical-and-simulation-template.md`：工科实验/仿真论文的通用模板。
- `engineering-equations-and-notation.md`：公式、符号、单位、指标定义和公式堆叠问题。
- `results-and-discussion.md`：结果、图表、讨论、局限性和结论写法。
- `paper-quality-review.md`：整篇论文质量审查和修改优先级。
- `material-to-journal-revision.md`：把材料型初稿压缩成期刊论文。

这些文件不是让用户手动阅读的，而是让 Codex 在不同论文写作任务中按需调用。

## 💡 使用边界

这个 skill 是一个写作辅助工具，可以帮助你梳理论文结构、检查逻辑问题、改进表达方式，但它不能替代作者自己的研究判断、实验设计、数据分析和学术责任。请始终以你的真实研究内容、可靠数据和目标期刊要求为准，并对最终论文内容进行独立判断和核查。

它不会自动保证论文能够发表，也不会替你生成真实实验数据、真实引用或不存在的结论。对于公式、数值、实验条件、文献引用和目标期刊格式，请始终以你的原始材料和期刊作者指南为准。

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

## 🔄 更新方式

如果你之前已经安装过这个 skill，想更新到 GitHub 最新版，可以让 Codex 帮你重新安装或覆盖更新：

```text
请帮我从 GitHub 更新这个 Codex skill：
https://github.com/GQLJ111/academic-paper-writing-skill

skill 路径是：
skills/academic-paper-writing

请覆盖本地旧版本，完成后提醒我重启 Codex。
```

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

## 🛠️ 设计原则

这个 skill 的设计重点是：

- 面向工科论文，而不是泛泛的学术写作。
- 优先结构和证据链，再做句子润色。
- 优先压缩和重组材料，再追求语言漂亮。
- 对公式、图表、实验设计和工程边界保持敏感。
- 避免把论文写成图表说明书、公式清单或文献堆砌。
- 对“顶刊风格”保持克制：强调清晰、证据、边界，而不是夸张表达。

## 🤝 交流与优化

欢迎交流、提出建议或一起优化这个 skill。你可以通过 Issue 或 Pull Request 反馈使用体验、提出改进方向，尤其欢迎来自工科论文写作、SCI 论文修改、审稿回复、实验设计表达等场景的真实问题。

如果这个 skill 对你有帮助，也欢迎 star 一下这个仓库。谢谢支持！

## License

This project is released under the MIT License.
