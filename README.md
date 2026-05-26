# Academic Research Suite Hermes / 学术研究 Agent Skill 套件

[English](#english) | [中文](#中文)

---

## English

A portable academic research skill for Hermes Agent, Claude Code, Codex/OpenAI agents, Cursor, and other agent frameworks. It helps with literature review, research planning, paper drafting, peer-review simulation, revision coaching, and citation/integrity audits.

> Adapted from the ideas of [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills), repackaged into a conventional single-skill repository structure.

### What changed in this version

- Added a canonical root `SKILL.md` for generic agent frameworks.
- Added Hermes-compatible path: `skills/research/academic-research-suite-hermes/SKILL.md`.
- Added compatibility files for Codex/OpenAI agents, Claude Code, and Cursor:
  - `agent instruction file`
  - `Claude-compatible instruction file`
  - `Cursor rule adapter`
  - `IDE rule adapter directory/academic-research-suite.mdc`
- Simplified the previous over-promising structure: the repository now ships one reliable, portable skill instead of referencing missing sub-skill folders.
- Tightened citation-integrity rules to prevent fabricated references and unsupported claims.

### Repository structure

```text
academic-research-suite-hermes/
├── SKILL.md                                      # Canonical cross-agent skill
├── README.md
├── LICENSE
├── agent instruction file                                    # Codex / OpenAI agent instructions
├── Claude-compatible instruction file                                    # Claude Code instructions
├── Cursor rule adapter                                 # Legacy Cursor rules
├── IDE rule adapter directory/academic-research-suite.mdc    # Cursor rule file
└── skills/
    └── research/
        └── academic-research-suite-hermes/
            └── SKILL.md                         # Hermes-compatible copy
```

### Installation

#### Hermes Agent

```bash
git clone https://github.com/yanyintingyou/academic-research-suite-hermes.git
mkdir -p ~/.hermes/skills/research
cp -r academic-research-suite-hermes/skills/research/academic-research-suite-hermes ~/.hermes/skills/research/
```

Restart Hermes or start a new session so the skill loader can discover it.

#### Claude Code

Clone the repository into your project or skill collection. Claude Code can read a repository-level compatibility adapter that points to the canonical `SKILL.md`.

#### Codex / OpenAI agents

Keep the repository-level compatibility adapter at repository root. Codex-style agents should load `SKILL.md` as the authoritative instruction file.

#### Cursor

Open the repository or copy `IDE rule adapter directory/academic-research-suite.mdc` into your project’s `IDE rule adapter directory` directory.

### Usage examples

```text
Use this skill to design a literature review on FOMC communication and cross-border capital flows.
```

```text
Simulate a journal peer review for this manuscript and produce a revision roadmap.
```

```text
Run an integrity audit: check whether each citation supports the adjacent claim.
```

### License and attribution

This adaptation is distributed under the license specified in `LICENSE`. Please also review and respect the license of the original inspiration repository: [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills).

---

## 中文

这是一个可移植的学术研究 Agent Skill，面向 Hermes Agent、Claude Code、Codex/OpenAI Agents、Cursor 以及其他通用 Agent 框架。它适用于文献综述、研究设计、论文写作、同行评议模拟、返修规划、引用核验与研究诚信审计。

> 本仓库基于 [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) 的思路进行 Hermes/通用 Agent 兼容化改造，并整理为常规单 Skill 仓库结构。

### 本次结构修正

- 新增根目录 `SKILL.md`，作为跨 Agent 框架的权威技能文件。
- 新增 Hermes 标准路径：`skills/research/academic-research-suite-hermes/SKILL.md`。
- 新增 Codex/OpenAI Agents、Claude Code、Cursor 兼容文件：
  - `agent instruction file`
  - `Claude-compatible instruction file`
  - `Cursor rule adapter`
  - `IDE rule adapter directory/academic-research-suite.mdc`
- 删除/替换原 README 中“存在多个子 skill 目录”的不准确描述；当前仓库提供一个稳定、可复制、可直接安装的单 Skill。
- 强化引用诚信规则，避免虚构文献、虚构 DOI、证据不足却强行下结论等问题。

### 仓库结构

```text
academic-research-suite-hermes/
├── SKILL.md                                      # 跨 Agent 通用主技能文件
├── README.md
├── LICENSE
├── agent instruction file                                    # Codex / OpenAI Agent 指令
├── Claude-compatible instruction file                                    # Claude Code 指令
├── Cursor rule adapter                                 # Cursor 旧版规则
├── IDE rule adapter directory/academic-research-suite.mdc    # Cursor 新版规则
└── skills/
    └── research/
        └── academic-research-suite-hermes/
            └── SKILL.md                         # Hermes 标准安装路径
```

### 安装方式

#### Hermes Agent

```bash
git clone https://github.com/yanyintingyou/academic-research-suite-hermes.git
mkdir -p ~/.hermes/skills/research
cp -r academic-research-suite-hermes/skills/research/academic-research-suite-hermes ~/.hermes/skills/research/
```

然后重启 Hermes 或开启新会话，让 skill loader 重新发现技能。

#### Claude Code

把本仓库克隆到项目目录或技能集合中即可。Claude Code 可读取仓库级兼容性适配文件，并由该文件指向根目录 `SKILL.md`。

#### Codex / OpenAI Agents

保留根目录的兼容性适配文件。Codex 风格 Agent 应把 `SKILL.md` 作为权威指令文件。

#### Cursor

直接打开本仓库，或将 `IDE rule adapter directory/academic-research-suite.mdc` 复制到你项目的 `IDE rule adapter directory` 目录。

### 使用示例

```text
用这个 skill 帮我设计一个关于 FOMC 沟通与跨境资本流动的文献综述框架。
```

```text
请模拟期刊同行评议，审查这篇论文并给出返修路线图。
```

```text
做一次研究诚信审计：检查每个引用是否真的支撑相邻论断。
```

### 许可证与署名

本改造版本遵循 `LICENSE` 中声明的许可证。请同时阅读并尊重原始灵感来源仓库 [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) 的许可证要求。
