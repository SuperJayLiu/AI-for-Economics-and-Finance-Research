# Use This Repository As One AI Skill

This folder is for readers who want to use the handbook inside ChatGPT, Claude, Codex, Claude Code, Cursor, or another AI assistant without copying many separate prompts.

The user-facing skill is:

```text
skill-pack/ai-econ-finance-research/
```

It feels like one skill. Internally, it contains small reference files for literature review, writing, empirical methods, coding, agents, datasets, slides, verification, examples, and Chinese use.

## Best Use Case

Use this when you are working on a real research project and want AI to guide you step by step.

The practical rule is:

```text
One paper = one AI project + one Git repo + one AI-use log.
```

## Download From GitHub

### Option A: Download ZIP

1. Open the GitHub repository.
2. Click the green `Code` button.
3. Click `Download ZIP`.
4. Unzip the downloaded file.
5. Open this folder:

```text
AI-for-Economics-and-Finance-Research/skill-pack/ai-econ-finance-research/
```

### Option B: Clone With Git

```bash
git clone https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research.git
cd AI-for-Economics-and-Finance-Research/skill-pack/ai-econ-finance-research
```

## Use In ChatGPT Or Claude Projects

1. Open `skill-pack/ai-econ-finance-research/SKILL.md`.
2. Copy all text.
3. Create a new ChatGPT Project or Claude Project.
4. Paste the copied text into the project instructions.
5. Upload the whole `references/` folder if your tool allows it.
6. If your tool does not allow folder upload, upload or paste only the reference files needed for your current task.
7. Start a new chat and type:

```text
Use the AI Econ Finance Research skill.
First ask what I want to do.
```

The assistant should then ask what research task you want help with and route you to the right reference.

## Exact First Messages

For a new paper or project, start with this:

```text
Use the AI Econ Finance Research skill.
I am working on one economics/finance research project.
First ask what I want to do, what stage I am at, what materials are safe to share, and what output format I need.
Do not produce a long answer until I confirm your proposed structure and assumptions.
```

For a specific task, start with this:

```text
Use the AI Econ Finance Research skill.
Task: help me with a source-grounded literature review / empirical methods draft / Stata debug / finance data merge / seminar presentation.
First ask clarifying questions if any required input is missing or unclear.
End by stating what was produced, what was not changed, what I must verify, and questions for me.
```

## Use In Codex Or Claude Code Style Tools

If your AI tool supports local skills, copy this folder into the tool's skills directory:

```text
skill-pack/ai-econ-finance-research/
```

Then start with:

```text
Use the ai-econ-finance-research skill. I want help with my research project.
```

If the tool cannot read the reference files automatically, paste the reference file it asks for.

## Set Up One Research Project

Use this sequence for a serious paper or project.

1. Create one AI Project or workspace for the paper.
2. Paste `SKILL.md` into the project instructions.
3. Upload or paste only the reference files needed for the current stage.
4. Add safe project materials: abstract, outline, variable dictionary, code snippets, public links, toy data, or non-confidential notes.
5. Do not upload restricted data, licensed extracts, referee reports, private coauthor notes, student data, or proprietary information unless policy and consent allow it.
6. Ask the assistant to classify the task and missing inputs.
7. For long outputs, require `Proposed structure and assumptions` before the full answer.
8. Verify every citation, result, code change, data rule, and empirical claim.
9. Record accepted AI use in an AI-use log.

## Day-To-Day Project Workflow

Use the skill as a project assistant, not as a one-time prompt.

1. Begin each new task by naming the task: literature, data, code, methods, writing, revision, slides, or verification.
2. Tell the assistant what can and cannot be shared.
3. Ask it to choose the reference file it needs.
4. Give only safe materials or a synthetic/toy version.
5. Confirm the proposed structure before long output.
6. Run the verification checklist.
7. Save accepted outputs and record AI use.
8. Start a new chat when the topic changes substantially.

## Recommended Reference Files By Stage

| Research stage | Load these references |
| --- | --- |
| new idea | `00-task-router.md`, `01-handbook-core-concepts.md`, `12-examples-failure-cases.md` |
| literature review | `03-literature-review.md`, `11-verification-disclosure.md` |
| empirical design | `05-empirical-methods-economics.md` or `06-empirical-methods-finance.md`, plus `09-datasets-access-confidentiality.md` |
| coding and data | `07-coding-data-stata-r-python.md`, `08-agentic-workflows-git-github.md`, `11-verification-disclosure.md` |
| paper writing and revision | `04-writing-revision-referee.md`, `11-verification-disclosure.md` |
| presentation or teaching | `10-slides-teaching-websites.md`, `12-examples-failure-cases.md` |
| Chinese workflow | `13-chinese-router.md` plus the task-specific English or Chinese reference needed |

## 中文使用说明

1. 下载或 clone 本仓库。
2. 打开 `skill-pack/ai-econ-finance-research/SKILL.md`。
3. 复制全文到 ChatGPT Project、Claude Project 或其他 AI 工具的 project instructions。
4. 如果工具允许上传文件，上传 `references/` 文件夹。
5. 如果不能上传文件，只在需要时粘贴相关 reference 文件。
6. 第一条消息写：

```text
Use the AI Econ Finance Research skill.
I want to work in Chinese. First ask what I want to do.
```

7. 如果是一个具体任务，可以写：

```text
Use the AI Econ Finance Research skill.
I want to work in Chinese.
Task: 帮我做文献综述 / 写实证方法 / debug Stata/R/Python / 设置 GitHub 和 agent / 准备 seminar slides。
如果必要信息不清楚，请先问澄清问题。
长输出前先给结构和假设，并等我确认。
最后说明：你产出了什么、没有改什么、我必须核查什么、还有哪些问题需要我回答。
```

8. 日常使用时，把它当作一个项目助手：先说明任务和材料安全级别，再让 AI 选择需要的 reference 文件；长答案先确认结构；最后人工核查并记录 AI-use log。
9. 不要上传受限数据、授权数据库 extracts、审稿材料、学生数据、合作者未同意的草稿或任何保密材料。
