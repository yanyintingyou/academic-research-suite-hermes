# academic-research-suite-hermes

**A comprehensive suite of Hermes Agent skills for academic research, literature review, paper writing, and peer review simulation.**

> **Adapted from [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) for Hermes Agent.**

This repository ports and adapts the powerful academic research skill collection originally developed by **Imbad0202** into a format that is fully optimized and natively compatible with the **Hermes Agent** multi-model AI agent system.

---

## Overview

`academic-research-suite-hermes` provides specialized, production-ready skills that support the entire academic research workflow inside Hermes Agent. Whether you are conducting literature reviews, drafting papers, simulating peer review, or managing research projects, these skills bring structured, high-quality assistance directly into your agent environment.

### Key Capabilities

- **Literature Review & Synthesis**: Intelligent search, summarization, gap analysis, and thematic organization of academic papers.
- **Research Planning & Outlining**: Structured paper planning, hypothesis generation, and methodology design.
- **Academic Writing Support**: Drafting sections with proper academic tone, argumentation, and citation integration.
- **Peer Review Simulation**: Generating constructive, critical feedback as if from real reviewers (with different personas).
- **Citation & Reference Management**: Assisting with citation formatting, consistency checking, and reference list generation.
- **Research Methodology Guidance**: Help with experimental design, statistical approaches, and academic rigor.

These skills are designed to work seamlessly with other Hermes skills (such as document conversion, web search, and data analysis tools).

---

## Why Adapt for Hermes Agent?

The original `academic-research-skills` by Imbad0202 is an outstanding open-source contribution. However, to fully leverage it inside a modern agent framework like **Hermes**, several adaptations were necessary:

- Proper `SKILL.md` metadata and registration system for automatic discovery
- Consistent directory layout under `skills/<skill-name>/`
- Optimized prompts and tool-calling patterns compatible with Hermes' multi-model routing and fallback mechanisms
- Better integration points with complementary skills (e.g., `markitdown-auto-converter-agent-skill`, PDF handling, etc.)
- Improved error handling, output formatting, and context management tailored for long research sessions

This adaptation preserves the spirit and quality of the original work while making it a first-class citizen in the Hermes ecosystem.

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yanyintingyou/academic-research-suite-hermes.git
```

### 2. Install into Hermes

Copy the skills into your Hermes skills directory:

```bash
cp -r academic-research-suite-hermes/skills/* ~/.hermes/skills/
```

Or if you use a skills tap / collection:

```bash
cp -r academic-research-suite-hermes/skills/academic-research-suite-hermes ~/.hermes/skills/
```

### 3. Restart Hermes

Restart your Hermes Agent session (or reload skills). The suite will be automatically registered.

---

## Project Structure

```
academic-research-suite-hermes/
├── LICENSE
├── README.md
├── .gitignore
└── skills/
    └── academic-research-suite-hermes/          # Skill suite container
        ├── SKILL.md
        ├── literature_review/
        ├── paper_writing/
        ├── peer_review_simulation/
        └── ... (additional sub-skills)
```

> **Note**: Individual skills are organized under `skills/academic-research-suite-hermes/`. Explore this directory to see all available capabilities.

---

## Usage Examples

Once loaded in Hermes, you can invoke the skills naturally:

- "帮我做一个这篇论文的文献综述"
- "Simulate a peer review for this manuscript with 3 reviewers"
- "Help me outline a paper on multimodal Fed communication analysis"
- "Review the methodology section for potential weaknesses"

The skills are designed to be triggered by clear academic intent and will leverage Hermes' multi-model capabilities for best results.

---

## Credits & Attribution

**This is an adaptation project.**

### Original Work
- **Repository**: [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills)
- **Author**: Imbad0202

### Hermes Adaptation
- **Adapted and maintained by**: yanyintingyou (Tingyou Li)
- **Purpose**: Make the original skills fully compatible and easy to use inside the Hermes Agent framework

All core prompts, research methodologies, and skill logic originate from the outstanding work of Imbad0202. This repository focuses on packaging, restructuring, Hermes-specific optimizations, and ongoing maintenance for the Hermes ecosystem.

**We strongly encourage users to also star and support the original repository.**

---

## License

- **This repository** (structure, Hermes adaptations, and integration code): **MIT License**
- **Original skill content**: Follows the license of [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) (typically CC-BY-NC-4.0 or similar — please check the original repo)

---

## Related Projects

- Original academic research skills: https://github.com/Imbad0202/academic-research-skills
- markitdown-auto-converter-agent-skill (companion document processing skill)
- Other Hermes skills by yanyintingyou

---

## Contributing

Contributions, improvements, and additional academic skills are welcome! Please open an issue or pull request. When contributing new skills, try to follow the existing structure and include proper `SKILL.md` metadata.

---

**Thank you to Imbad0202 for the original high-quality work that made this adaptation possible.**
