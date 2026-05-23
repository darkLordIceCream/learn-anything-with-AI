# AGENTS.md

## This is NOT a software project

There is no build, test, lint, or runtime. No `package.json`, no CI, no code to execute.
This repo is a portable AI skill pack (`learn-anything-skill`) distributed to AI agents (OpenAI Codex, Claude Code, OpenCode).

## Repository structure

```
skills/learn-anything-skill/
├── SKILL.md              ← Primary file. Read this first.
├── agents/openai.yaml     ← OpenAI agent config
├── references/            ← Supplementary detail SKILL.md delegates to
│   ├── mastery-rubric.md
│   ├── project-patterns.md
│   ├── source-strategy.md
│   └── teaching-playbook.md
└── assets/                ← Templates for learning outputs
    ├── learning-plan-template.md
    ├── study-notes-template.md
    └── ...
```

## Working with the skill

- **`SKILL.md`** is the entry point. It defines the agent's behavior, task decision tree, teaching flow, mastery rules, and file output conventions.
- **`references/`** files are detail expansions that SKILL.md explicitly delegates to for deeper rules. They should not override SKILL.md.
- **`assets/`** are templates to fill in per-user progress; never serve them verbatim.
- The skill's `name` in YAML frontmatter is `learn-anything-skill`.

## Key conventions the skill enforces

- **Language**: Chinese-first teaching. Retain English for technical terms (API names, formulas, code identifiers).
- **File output**: Writes Markdown outputs to `study/<topic>-*.md` in the user's current working directory by default. Reuse existing files and directories rather than creating duplicates.
- **Mastery levels**: "know → use → modify → design → transfer." Never accept "I understand" as mastery; verify through restatement, variation, transfer, or concrete output.
- **Source authority**: Official docs > canonical textbooks > best practices. Always distinguish factual basis from judgment/advice.
- **Project-driven by default**: Even for non-coding topics, generate a concrete output (report, outline, case analysis, etc.), not just conceptual explanation.

## Startup workflow

Before modifying files in this repo:
1. Read `SKILL.md` — the primary behavior definition
2. Read `feature_list.json` — current milestone state
3. Read `progress.md` — context from prior sessions
4. Understand which task type the change falls under (new skill feature, description fix, reference update, template improvement)

## Working rules

- **One feature at a time** — pick exactly one unfinished feature from `feature_list.json`
- **SKILL.md is the source of truth** — `references/` expand on it, never override it
- **Update artifacts before ending** — `progress.md` and `feature_list.json` must reflect current state
- **No speculative edits** — only change what the feature or user request demands

## Definition of done

A feature is done when:
- [ ] Target changes are implemented
- [ ] `feature_list.json` updated with status and evidence
- [ ] `progress.md` reflects the completion
- [ ] If changing SKILL.md: skill still loads correctly in OpenCode (no syntax errors in frontmatter)
- [ ] If changing references/ or assets/: the delegation paths in SKILL.md remain valid

## End of session

Before ending:
1. Update `progress.md` with current state, blockers, decisions
2. Update `feature_list.json` statuses
3. Commit with descriptive message

## What NOT to do

- Do not try to build, test, lint, typecheck, or run anything — there is no executable code.
- Do not modify `agents/openai.yaml` casually; it's agent routing config.
- Do not treat `README.md` as agent instruction. It's human-facing installation docs for different platforms (Codex, Claude Code, OpenCode). The actual agent behavior is in `SKILL.md`.
- Do not inline reference content into SKILL.md — keep the delegation structure intact.
