<div align="center">

<img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License">
<img src="https://img.shields.io/badge/Platform-OpenCode-7C3AED?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIHZpZXdCb3g9IjAgMCAxNiAxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cmVjdCB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIHJ4PSIzIiBmaWxsPSIjN0MzQUVEIi8+PHRleHQgeD0iOCIgeT0iMTIiIGZvbnQtc2l6ZT0iOCIgdGV4dC1hbmNob3I9Im1pZGRsZSIgZmlsbD0id2hpdGUiIGZvbnQtZmFtaWx5PSJzYW5zLXNlcmlmIj5PPC90ZXh0Pjwvc3ZnPg==" alt="OpenCode">
<img src="https://img.shields.io/badge/Skill%20Format-SKILL.md-10B981?style=flat-square" alt="SKILL.md">
<img src="https://img.shields.io/badge/Language-中文主讲-orange?style=flat-square" alt="Language">

</div>

<br>

> ⚠️ **Fork Notice**：本仓库是 [read2017/learn-anything-with-AI](https://github.com/read2017/learn-anything-with-AI) 的 fork。  
> 在原项目基础上，我们将其改造为 **OpenCode 专用插件**，增加了一键安装、harness 框架和 GitHub 工程化结构。  
> 原始项目说明请见 [上游仓库](https://github.com/read2017/learn-anything-with-AI) ｜ [English README](./README.en.md)

---

# 🎓 Learn Anything Skill for OpenCode

> 一个 **中文导师 + 项目教练** 式的通用 AI 学习 Skill。  
> 不只回答问题，**帮你真的学会。**

---

## ⚡ 一句话安装

把下面这句话复制给你的 **OpenCode Agent**：

```
安装 learn-anything-skill，按这里的指南操作：https://raw.githubusercontent.com/darkLordIceCream/learn-anything-with-AI/main/docs/guide/installation.md
```

Agent 会自动读取安装指南、下载 skill 文件、完成配置。  
你只需要 **重启 OpenCode**。

<p align="center"><b>🤖 让 Agent 干活，人类休息。</b></p>

---

## 📖 这是什么

`learn-anything-skill` 是一个可移植的 `SKILL.md` 工作流包，核心方法论：

| 方法 | 说明 |
|------|------|
| **项目驱动学习** | 每轮学习落到一个产出（代码 demo、报告、笔记、演讲稿等），不空谈概念 |
| **Mastery Learning** | 掌握 ≠ 看懂。必须能解释、能应用、能迁移才算过 |

**它能帮你生成：**
- 📋 学习计划  ·  📝 学习笔记  ·  🔄 课后复盘
- 📦 项目任务书  ·  ✅ 掌握度检查单  ·  🎯 单次主题讲解

---

## ✨ 核心特性

### 🤖 导师模式，不是问答机器人

自动判断任务类型：
```
学新知识 → 路线规划 → 项目陪练 → 资料精读 → 课后复盘 → 掌握度评估
```

目标不清晰？先补关键信息。目标清晰？直接开讲。

### 🏗 项目驱动（不限编程）

| 编程/工程主题 | 非编程主题 |
|-------------|-----------|
| 最小功能 demo | 研究短报告 |
| 微项目 | 案例分析 |
| 调试任务 | 知识地图 |
| 系统任务书 | 教学讲义 |

### 📚 自动补权威来源

```
官方文档 > 经典教材 > 最佳实践
```

回答严格区分 **事实依据** 与 **建议判断**。

### 🎯 内置掌握度分级

```
知道 → 会用 → 会改 → 会设计 → 会迁移
```

不问「懂了没」，只验证「能不能做」。

---

## 📂 仓库结构

```
skills/learn-anything-skill/
├── SKILL.md              ← 🧠 Skill 主文件（入口）
├── agents/openai.yaml     ← OpenAI 代理配置
├── references/            ← 📖 深度参考规则
│   ├── mastery-rubric.md      掌握度分级细则
│   ├── project-patterns.md    项目化模式
│   ├── source-strategy.md     资料策略
│   └── teaching-playbook.md   教学操作手册
└── assets/                ← 📄 输出模板
    ├── learning-plan-template.md
    ├── study-notes-template.md
    ├── session-review-template.md
    ├── project-brief-template.md
    ├── mastery-check-template.md
    └── mistakes-log-template.md
```

---

## 🚀 快速开始

### 触发 Skill

在 OpenCode 里直接说：

```text
帮我学微积分，给我做一个 4 周学习计划
```

或显式调用：

```text
用 learn-anything-skill 教我 SQL，并设计一个小项目任务书
```

### 工作目录建议

建议为每个学习主题单独建目录：

```bash
mkdir learn-ai && cd learn-ai
```

Skill 会自动把学习产出写入当前目录的 `study/` 子文件夹，持续积累。

---

## 💡 使用案例

<details>
<summary><b>📋 生成学习计划</b></summary>

```text
用 learn-anything-skill 帮我学线性代数。
我现在只会高中数学，每周能学 6 小时。
给我做一个 4 周学习计划，每周都要有产出和验收标准。
```

→ 得到：起点评估 · 能力拆解 · 周计划 · 验收标准 · 风险提示

</details>

<details>
<summary><b>📖 读书陪练</b></summary>

```text
用 learn-anything-skill 带我读《国富论》第一卷。
帮我建立结构、做读书笔记，安排每章后的复盘问题。
```

→ 得到：章节结构 · 关键概念 · 易误解点 · 精读问题 · 复盘问题

</details>

<details>
<summary><b>🗣 英语口语训练</b></summary>

```text
用 learn-anything-skill 帮我提升英语口语。
目标是 6 周后能做 3 分钟英文自我介绍。
请按项目驱动方式安排训练。
```

→ 得到：分阶段路线 · 每周脚本 · 录音任务 · 复测标准

</details>

<details>
<summary><b>💻 SQL + 小项目</b></summary>

```text
用 learn-anything-skill 教我 SQL。
我会一点 Python，但没系统学过数据库。
给我一个学习路线，设计一个学生成绩分析的小项目任务书。
```

→ 得到：前置诊断 · 核心概念 · 梯度练习 · 项目任务书 · 掌握检查点

</details>

<details>
<summary><b>✅ 掌握度检查</b></summary>

```text
用 learn-anything-skill 检查我对条件概率和贝叶斯公式的掌握度。
不要只问我懂不懂，给我复述题、变式题和迁移题。
```

→ 得到：等级判定 · 证据 · 薄弱点 · 补强任务 · 复测标准

</details>

---

## 🎨 适用主题

这个 Skill 不只是给程序员用的：

`编程` · `数学` · `统计` · `经济学` · `金融` · `英语` · `日语` · `历史` · `社会科学` · `写作` · `演讲` · `AI/LLM`

---

## 🛠 定制你自己的版本

想修改？优先动这些文件：

| 文件 | 控制什么 |
|------|---------|
| `SKILL.md` | 整体行为、任务决策树、教学流程 |
| `references/source-strategy.md` | 资料查找优先级 |
| `references/project-patterns.md` | 项目化方式 |
| `references/mastery-rubric.md` | 掌握度判定标准 |

---

## 🔗 兼容性

| 平台 | Skill 格式 | 安装方式 |
|------|-----------|---------|
| **OpenCode** | ✅ 原生支持 | `.opencode/skills/` 或一句话安装 |
| Claude Code | ✅ 兼容 | `.claude/skills/` |
| Codex / OpenAI | ✅ 兼容 | `~/.codex/skills/` |

> Skill 内容本身跨平台通用，安装入口略有不同。

---

## 🙏 致谢

本仓库 fork 自 [read2017/learn-anything-with-AI](https://github.com/read2017/learn-anything-with-AI)，感谢原作者的 Skill 设计与理念。

本 fork 的增量工作：
- 🔌 改造为 OpenCode 原生插件（`opencode.json` + `skills.paths`）
- ⚡ 实现 oh-my-openagent 风格一句话安装
- 🔧 接入 harness-creator 工程化框架（`AGENTS.md` / `feature_list.json` / `progress.md`）
- 📝 优化 SKILL.md description 适配 OpenCode skill 预算

---

## 📄 License

MIT · 详见 [LICENSE](./LICENSE)
