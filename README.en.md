<div align="center">

<img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License">
<img src="https://img.shields.io/badge/Platform-OpenCode-7C3AED?style=flat-square" alt="OpenCode">
<img src="https://img.shields.io/badge/Skill%20Format-SKILL.md-10B981?style=flat-square" alt="SKILL.md">
<img src="https://img.shields.io/badge/Language-中文主讲-orange?style=flat-square" alt="Language">

</div>

<br>

> ⚠️ **Fork Notice**: This repo is a fork of [read2017/learn-anything-with-AI](https://github.com/read2017/learn-anything-with-AI).  
> We adapted it into an **OpenCode-native plugin** with one-line install, harness framework, and engineering structure.  
> Original project: [upstream repo](https://github.com/read2017/learn-anything-with-AI) · [中文说明](./README.md)

---

# 🎓 Learn Anything Skill for OpenCode

> A general-purpose AI learning skill. **Mentor + Project Coach** mode.  
> Doesn't just answer questions — **helps you truly learn.**

---

## ⚡ One-Line Install

Copy this sentence to your **OpenCode agent**:

```
Install learn-anything-skill by following the instructions at: https://raw.githubusercontent.com/darkLordIceCream/learn-anything-with-AI/main/docs/guide/installation.md
```

The agent reads the guide, downloads files, configures everything.  
You just **restart OpenCode**.

<p align="center"><b>🤖 Let the agent work. You rest.</b></p>

---

## 📖 What This Is

A portable `SKILL.md` workflow package built on two methods:

| Method | Description |
|--------|-------------|
| **Project-Driven Learning** | Every session produces a tangible output (demo, report, notes, script) |
| **Mastery Learning** | Mastery ≠ reading. Must explain, apply, transfer to pass |

**It can generate:**
- 📋 Study Plans  ·  📝 Notes  ·  🔄 Session Reviews
- 📦 Project Briefs  ·  ✅ Mastery Checklists  ·  🎯 Topic Explanations

---

## ✨ Key Features

### 🤖 Mentor Mode, Not a Q&A Bot

Auto-identifies task type:
```
New Topic → Roadmap → Project Coaching → Source Reading → Review → Mastery Check
```

### 🏗 Project-Driven (Not Just Code)

| Coding/Engineering | Non-Coding |
|-------------------|-----------|
| Minimal demo | Research report |
| Micro-project | Case analysis |
| Debugging task | Knowledge map |
| System brief | Teaching script |

### 📚 Auto-Sources Authority

```
Official Docs > Canonical Textbooks > Best Practices
```

Always distinguishes **factual basis** from **advisory judgment**.

### 🎯 Built-in Mastery Levels

```
Know → Use → Modify → Design → Transfer
```

Stops asking "Do you understand?" Starts checking "Can you do it?"

---

## 📂 Repo Structure

```
skills/learn-anything-skill/
├── SKILL.md              ← 🧠 Main skill file
├── agents/openai.yaml     ← OpenAI agent config
├── references/            ← 📖 Deep reference rules
│   ├── mastery-rubric.md
│   ├── project-patterns.md
│   ├── source-strategy.md
│   └── teaching-playbook.md
└── assets/                ← 📄 Output templates
    ├── learning-plan-template.md
    ├── study-notes-template.md
    ├── session-review-template.md
    ├── project-brief-template.md
    ├── mastery-check-template.md
    └── mistakes-log-template.md
```

---

## 🚀 Quick Start

### Trigger the Skill

In OpenCode:

```
help me learn calculus, give me a 4-week study plan
```

Or explicitly:

```
Use learn-anything-skill to teach me SQL and design a mini-project brief
```

### Workspace Tip

Create a dedicated directory per topic:

```bash
mkdir learn-ai && cd learn-ai
```

The skill auto-saves output to `study/` in your current directory.

---

## 💡 Use Cases

<details>
<summary><b>📋 Study Plan</b></summary>

```
Use learn-anything-skill to help me learn linear algebra.
I only know high-school math, 6h/week.
Create a 4-week plan with outputs and acceptance criteria.
```

→ Gets: level assessment · capability breakdown · weekly plan · deliverables · risk notes

</details>

<details>
<summary><b>📖 Guided Reading</b></summary>

```
Use learn-anything-skill to guide me through The Wealth of Nations Vol 1.
Help me build structure, take notes, prepare chapter review questions.
```

→ Gets: chapter structure · key concepts · common misunderstandings · review questions

</details>

<details>
<summary><b>🗣 Spoken English</b></summary>

```
Use learn-anything-skill to improve my spoken English.
Goal: 3-minute self-introduction in 6 weeks. Project-driven training.
```

→ Gets: staged roadmap · weekly scripts · recording tasks · retest criteria

</details>

<details>
<summary><b>💻 SQL + Project</b></summary>

```
Use learn-anything-skill to teach me SQL.
I know Python but not databases.
Give me a roadmap and a student-score analysis project brief.
```

→ Gets: prerequisite check · core concepts · graded exercises · project brief · checkpoints

</details>

<details>
<summary><b>✅ Mastery Check</b></summary>

```
Use learn-anything-skill to assess my understanding of conditional probability.
Don't ask if I understand — give me restatement, variation, and transfer tasks.
```

→ Gets: level judgment · evidence · weak points · reinforcement · retest standard

</details>

---

## 🎨 Suitable Topics

This skill isn't just for programmers:

`Coding` · `Math` · `Stats` · `Economics` · `Finance` · `English` · `Japanese` · `History` · `Social Science` · `Writing` · `Speaking` · `AI/LLM`

---

## 🛠 Customize

Want your own version? Start here:

| File | Controls |
|------|----------|
| `SKILL.md` | Overall behavior, task tree, teaching flow |
| `references/source-strategy.md` | Source lookup priority |
| `references/project-patterns.md` | Project-driven formats |
| `references/mastery-rubric.md` | Mastery criteria |

---

## 🔗 Compatibility

| Platform | Skill Format | Install |
|----------|-------------|---------|
| **OpenCode** | ✅ Native | `.opencode/skills/` or one-line install |
| Claude Code | ✅ Compatible | `.claude/skills/` |
| Codex / OpenAI | ✅ Compatible | `~/.codex/skills/` |

> The skill content is cross-platform. Install entry points vary slightly.

---

## 🙏 Acknowledgments

Forked from [read2017/learn-anything-with-AI](https://github.com/read2017/learn-anything-with-AI). Credits to the original author for the skill design and philosophy.

This fork adds:
- 🔌 OpenCode-native plugin packaging (`opencode.json` + `skills.paths`)
- ⚡ Oh-my-openagent style one-line install
- 🔧 Harness-creator engineering framework (`AGENTS.md` / `feature_list.json` / `progress.md`)
- 📝 Optimized SKILL.md description for OpenCode skill listing budget

---

## 📄 License

MIT · See [LICENSE](./LICENSE)
