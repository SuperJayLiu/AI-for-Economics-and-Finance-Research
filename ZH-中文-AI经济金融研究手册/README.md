# 中文入口：AI for Economics and Finance Research

这是本仓库的中文入口页。目标是帮助经济学和金融学研究者用中文理解本仓库如何使用，并快速找到可以直接复制使用的 AI research skills、workflow templates 和安全规则。部分专业术语保留英文，例如 prompt、skill、agent、MCP、Git、GitHub、LaTeX、Beamer、DiD、IV、RD。

> [!IMPORTANT]
> 本仓库不是提示词合集，也不是 AI 工具排行榜。它的核心目标是帮助研究者建立可核查、可复现、可追踪、负责任的 AI 辅助研究工作流。

如有中文版本建议，请邮件联系 [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk)，邮件标题建议使用 `[AI Econ Finance Chinese] 中文版本建议`。

## 安全获取更新

推荐优先使用 GitHub 原生通知，这样维护者不需要额外收集你的邮箱。

| 方式 | 如何使用 | 信息安全说明 |
| --- | --- | --- |
| GitHub Watch | 在仓库页面点击 Watch，选择通知类型。 | 最少额外个人信息，适合 GitHub 用户。 |
| GitHub Releases | 只关注 releases，接收稳定版本更新。 | 低频、低噪音。 |
| 邮件更新列表 | 给 [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) 发邮件，标题写 `[AI Econ Finance Updates] Subscribe`。 | 只需要姓名和邮箱。不要发送研究数据、论文草稿、审稿材料、学生数据、restricted/licensed data 或 confidential information。 |

邮件列表规则：

- 只用于本仓库更新、release notes、workshop 信息和重要 skill 更新。
- 只保存必要联系信息。
- 不向第三方分享邮件列表。
- 不通过订阅邮件接收或处理 confidential research material。
- 退订邮件标题写 `[AI Econ Finance Updates] Unsubscribe`。
- 如果学校、雇主、期刊、会议、基金、数据提供方或合作者有更严格的信息安全规则，请遵守更严格的规则。

## 快速选择

| 如果你想要... | 打开 |
| --- | --- |
| 像读书一样理解 AI 在经济金融研究中的使用 | [01 Start Here: Learn AI for Economics and Finance Research](../01-Start-Here-to-Learn-AI-for-Econ-Finance-Research/README.md) |
| 直接复制可用的 skills、instructions、templates | [02 Copy and Use: AI Research Instructions and Templates](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/README.md) |
| 设置 Codex、Claude Code、GitHub、agent、自动化工作流 | [03 Set Up: Agents and Automated Research Workflows](../03-Set-Up-Agents-and-Automated-Research-Workflows/README.md) |
| 看例子、图示、失败案例 | [04 See Examples: Diagrams and Failure Cases](../04-See-Examples-Diagrams-and-Failure-Cases/README.md) |
| 查官方文档、builder、外部资源和资料来源 | [05 Check Sources: Builders, Official Docs, and Resources](../05-Check-Builders-Official-Docs-and-Resources/README.md) |
| 教工作坊、培训 RA、练习 presentation、做 slides | [06 Teach and Share: Workshops, Practice Talks, and Slides](../06-Teach-Workshops-Practice-Talks-and-Share-Slides/README.md) |

## 最重要的原则

```text
AI 可以自动化劳动，但不能替代学术责任。
```

这意味着：

- AI 输出不是 evidence。
- AI 生成的 citation 必须逐条核查。
- AI 生成的代码必须运行、检查、对照研究设计。
- AI 不能替你决定 identification strategy。
- AI 不能替你判断 research question 是否重要。
- AI 不能替你决定能否上传 restricted、licensed、confidential 或 coauthor material。
- AI 不能替你承担 journal、conference、university、funder、data provider 的合规责任。

## 最小安全配置

 serious research 至少需要：

| 工具/文件 | 用途 |
| --- | --- |
| ChatGPT / Claude / institution-approved tool | 读写、解释、代码辅助 |
| GitHub repo | 记录 AI 改了什么，防止文件丢失 |
| `README.md` | 项目说明 |
| `DATA.md` | 数据来源、权限、敏感性规则 |
| `AGENTS.md` 或 `CLAUDE.md` | 给 AI agent 的项目规则 |
| `AI-USE-LOG.md` | 记录 AI 使用、人工核查、剩余不确定性 |
| `.gitignore` | 防止 raw/restricted/private data 被提交 |

## 最常用的中文导航

| 任务 | 直接打开 |
| --- | --- |
| 检查研究想法 | [Research Idea Stress Test](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/01-ideas-brainstorming-proposal-and-literature-skills.md#skill-1-research-idea-stress-test) |
| 写 literature review | [Literature Review and Source Synthesis Skills](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/10-literature-review-and-source-synthesis-skills.md) |
| 写 proposal | [Proposal Builder](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/01-ideas-brainstorming-proposal-and-literature-skills.md#skill-2-proposal-builder-for-econfinance) |
| 写 introduction | [Introduction Spine Builder](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/02-paper-drafting-revision-and-citation-skills.md#skill-1-introduction-spine-builder) |
| 写 applied economics methods | [Empirical Methods Skills for Economics Research](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/03-empirical-methods-skills-for-economics-research.md) |
| 写 finance empirical methods | [Empirical Methods Skills for Finance Research](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/04-empirical-methods-skills-for-finance-research.md) |
| 检查 causal inference / econometrics / time series | [Causal Inference, Econometrics, and Time-Series Skills](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/11-causal-inference-econometrics-and-time-series-skills.md) |
| 检查 theory model / proof / assumptions | [Theory Model and Math Skills](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/12-theory-model-and-math-skills.md) |
| 处理 referee comments / revision response | [Referee Reports and Peer Review Skills](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/13-referee-reports-and-peer-review-skills.md) |
| 清理旧项目并设置 Git | [Clean Existing Research Project and Set Up Git](../03-Set-Up-Agents-and-Automated-Research-Workflows/01-clean-existing-research-project-and-set-up-git.md) |
| 建立 one paper one repo one AI project | [One Paper, One Repo, One AI Project](../03-Set-Up-Agents-and-Automated-Research-Workflows/02-one-paper-one-repo-one-ai-project.md) |
| 练习 seminar / job talk | [Practice My Presentation With AI](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/06-presentations-slides-websites-and-talk-practice-skills.md#skill-3-practice-my-presentation-with-ai) |

## 使用任何 skill 前都要加的安全指令

```text
Do not invent citations, data sources, coefficients, robustness checks, institutional details, mathematical derivations, or claims about the literature. If information is missing, say exactly what is missing and what I must verify manually. Separate verified facts, interpretation, suggestions, and uncertainty.

Follow all university, employer, journal, conference, funder, data-provider, and coauthor policies on AI use. If the relevant rule is stricter than this instruction, follow the stricter rule.
```

## 适合中文读者的使用方式

1. 先读本页，理解总体结构。
2. 打开 `01` 文件夹，把它当成一本 handbook 读。
3. 进入 `02` 文件夹，选择一个具体任务，只复制一个 skill。
4. 用自己的研究事实替换方括号内容。
5. 要求 AI 先给 plan，不要直接执行。
6. 人工核查 citation、code、data、coefficients、identification、theory proof。
7. 把接受的 AI 输出和人工核查记录到 `AI-USE-LOG.md`。

## 未来中文版本方向

本页先提供完整中文导航。后续可逐步把最常用页面翻译成中文版本，例如：

- literature review skills
- empirical methods skills
- causal inference and econometrics skills
- Git/data/research safety templates
- agents and automated workflows
- teaching/workshop materials

专业术语会尽量保留英文，同时用中文解释其在经济金融研究中的含义。
