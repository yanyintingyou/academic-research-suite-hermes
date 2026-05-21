---
name: academic-research-suite-hermes
description: "Use when conducting end-to-end academic research, writing academic papers, performing peer review simulations, or managing the full research-to-publication pipeline. Triggers on: research, deep research, literature review, write paper, academic paper, peer review, paper review, academic pipeline, research to paper, revise paper, systematic review, PRISMA, fact-check, guide my research, parse reviews. Supports 7 research modes, 10 paper-writing modes, 6 review modes, and a 10-stage orchestrated pipeline with mandatory integrity gates and devil's advocate checkpoints. Human-in-the-loop design with confirmation checkpoints at every stage."
version: 1.0.0
author: Adapted from Imbad0202/academic-research-skills for Hermes Agent
license: CC-BY-NC-4.0
metadata:
  hermes:
    tags: [academic, research, paper-writing, peer-review, literature-review, pipeline, scholarly]
    related_skills: [listed-company-research, arxiv, academic-writing-assistant]
---

# Academic Research Suite — Full Research-to-Publication Pipeline

A comprehensive academic research toolkit adapted for Hermes Agent. Covers the full scholarly workflow:

> **Research → Write → Integrity Check → Review → Revise → Re-Review → Finalize**

**Core principle**: AI is your copilot, not the pilot. This skill handles grunt work (literature search, citation formatting, consistency checks, verification) while you retain control over question definition, method choice, interpretation, and core arguments.

**Built-in safeguards**: Mandatory integrity gates, independent devil's advocate checkpoints, three-layer citation anchors, anti-sycophancy protections, and temporal integrity verification.

---

## Overview

This skill coordinates four integrated capabilities:

1. **Deep Research** — 13-agent team for rigorous literature investigation
2. **Academic Paper Writing** — 12-agent pipeline for drafting publishable manuscripts
3. **Academic Paper Review** — 7-agent multi-perspective peer review simulation
4. **Academic Pipeline Orchestrator** — 10-stage workflow manager with quality gates

All four can run independently or as a seamless pipeline. Every stage requires explicit user confirmation before proceeding.

---

## When to Use

- Conducting literature reviews, systematic reviews (PRISMA), or meta-analyses
- Writing journal articles, conference papers, theses, or policy briefs
- Simulating peer review before submission
- Revising papers based on reviewer comments
- Fact-checking claims against sources
- Need Socratic guidance to clarify research direction
- Managing the complete research-to-publication workflow

**Do NOT use for**:
- Non-academic creative writing → use `creative-writing` or general chat
- Simple web searches without scholarly depth → use `web_search` directly
- Code-only tasks without research component → use `software-development`

---

## Quick Start

```
Research the impact of AI on higher education quality assurance
```

```
Write a paper on cross-border capital flows and FOMC communication
```

```
Review this paper: [paste manuscript]
```

```
Run full academic pipeline for my research on demographic decline
```

**Default mode**: When ambiguous between guidance and execution, prefer guidance (`socratic`/`plan`).

---

## Mode Selection Guide

| Your Need | Sub-skill | Mode | Output |
|-----------|-----------|------|--------|
| Vague idea, need guidance | Deep Research | `socratic` | Clarified RQ + methodology |
| Clear RQ, full investigation | Deep Research | `full` | APA 7.0 research report |
| Quick brief (30 min) | Deep Research | `quick` | 500–1,500 word brief |
| Verify specific claims | Deep Research | `fact-check` | Verification report |
| Systematic review / meta-analysis | Deep Research | `systematic-review` | PRISMA-compliant report |
| Write paper from scratch | Academic Paper | `full` | Complete draft |
| Step-by-step paper guidance | Academic Paper | `plan` | Chapter plan + insights |
| Revise based on reviews | Academic Paper | `revision` | Revised draft + response letter |
| Parse reviewer comments | Academic Paper | `revision-coach` | Revision roadmap |
| Pre-submission review | Paper Reviewer | `full` | 5 reports + decision |
| Verify revisions addressed | Paper Reviewer | `re-review` | Traceability matrix |
| Full research-to-paper | Pipeline | `full` | Orchestrated 10-stage workflow |

**Not sure?** Start with `socratic` (deep-research) or `plan` (academic-paper) — guidance first, execution second.

---

## 10-Stage Academic Pipeline

The orchestrator manages the complete workflow:

| Stage | Name | Capability | Deliverables |
|-------|------|-----------|-------------|
| 1 | **RESEARCH** | Deep Research | RQ Brief, Methodology, Bibliography, Synthesis |
| 2 | **WRITE** | Academic Paper | Paper Draft |
| 2.5 | **INTEGRITY** | Integrity Agent | Integrity report (blocking gate) |
| 3 | **REVIEW** | Paper Reviewer | 5 reviews + Editorial Decision + Roadmap |
| 4 | **REVISE** | Academic Paper | Revised Draft + Response to Reviewers |
| 3' | **RE-REVIEW** | Paper Reviewer | Verification review |
| 4' | **RE-REVISE** | Academic Paper | Second revised draft (if needed) |
| 4.5 | **FINAL INTEGRITY** | Integrity Agent | Final verification (must be 100% pass) |
| 5 | **FINALIZE** | Academic Paper | Formatted output (MD/DOCX/LaTeX/PDF) |
| 6 | **PROCESS SUMMARY** | Orchestrator | Collaboration record |

**Key rules**:
- Stage 2.5 and 4.5 are **mandatory integrity gates** — cannot be skipped
- Stage 4.5 must pass with **zero issues** before finalization
- Max 2 revision loops; unresolved items → "Acknowledged Limitations"
- Early-stop: if delta < 3 points + no critical issues → suggest convergence

**Mid-entry**: The pipeline detects your current stage from context. You can start at any stage:
- "I already have a paper, review it" → Stage 2.5
- "I got reviewer comments" → Stage 4
- "Just help me research X" → Stage 1 only

---

## Agent Teams

### Deep Research Team (13 Agents)

| Agent | Role | Phase |
|-------|------|-------|
| `research_question_agent` | Transforms topics into FINER-scoped RQs | 1 |
| `research_architect_agent` | Designs methodology blueprint | 1 |
| `bibliography_agent` | Systematic search + APA 7.0 annotated bibliography | 2 |
| `source_verification_agent` | Fact-checking, evidence hierarchy, predatory journal detection | 2 |
| `synthesis_agent` | Cross-source integration, contradiction resolution, gap analysis | 3 |
| `report_compiler_agent` | Full APA 7.0 report drafting | 4, 6 |
| `editor_in_chief_agent` | Q1 editorial review + verdict | 5 |
| `devils_advocate_agent` | Assumption challenges, logical fallacies, bias checks | 1, 3, 5 |
| `ethics_review_agent` | AI ethics, attribution, dual-use screening | 5 |
| `socratic_mentor_agent` | 5-layer Socratic guidance | Socratic Mode |
| `risk_of_bias_agent` | RoB 2 / ROBINS-I assessment | Systematic Review |
| `meta_analysis_agent` | Meta-analysis / narrative synthesis + GRADE | Systematic Review |
| `monitoring_agent` | Post-research alerts, retractions, new findings | Optional |

### Academic Paper Team (12 Agents)

| Agent | Role | Phase |
|-------|------|-------|
| `intake_agent` | Configuration interview + handoff detection | 0 |
| `literature_strategist_agent` | Search strategy + source screening | 1 |
| `structure_architect_agent` | Outline + word-count allocation | 2 |
| `argument_builder_agent` | Claim-evidence chains + logical flow | 3 |
| `draft_writer_agent` | Section-by-section drafting | 4 |
| `citation_compliance_agent` | Format verification + DOI checking | 5a |
| `abstract_bilingual_agent` | Bilingual abstract + keywords | 5b |
| `peer_reviewer_agent` | Simulated double-blind review | 6 |
| `formatter_agent` | LaTeX / DOCX / PDF / Markdown output | 7 |
| `socratic_mentor_agent` | Chapter-by-chapter guidance (plan mode) | Plan |
| `visualization_agent` | Publication-quality figures (matplotlib/ggplot2) | 4/7 |
| `revision_coach_agent` | Parse comments → structured roadmap | Revision-Coach |

### Paper Reviewer Team (7 Agents)

| Agent | Role |
|-------|------|
| `field_analyst_agent` | Auto-identifies field + configures 5 reviewer identities |
| `eic_agent` | Editor-in-Chief — journal fit, originality, quality |
| `methodology_reviewer_agent` | Research design, statistics, reproducibility |
| `domain_reviewer_agent` | Literature, theory, domain contribution |
| `perspective_reviewer_agent` | Cross-disciplinary, practical/ethical impact |
| `devils_advocate_reviewer_agent` | Core argument challenges, fallacy detection |
| `editorial_synthesizer_agent` | Consolidates reviews, makes decision |

**Decision thresholds**:
- ≥80: Accept
- 65–79: Minor Revision
- 50–64: Major Revision
- <50: Reject

### Pipeline Orchestrator Team (5 Agents)

| Agent | Role |
|-------|------|
| `pipeline_orchestrator_agent` | Stage detection, dispatching, transitions |
| `state_tracker_agent` | Records stages, materials, revision loops |
| `integrity_verification_agent` | 100% reference/citation/data verification (blocking) |
| `collaboration_depth_agent` | Advisory observer (non-blocking) |
| `claim_ref_alignment_audit_agent` | Opt-in claim-faithfulness audit |

---

## Orchestration Workflows

### Deep Research (6 Phases)

```
Phase 1: SCOPING (Interactive)
  → research_question_agent: FINER-scored RQ + scope boundaries
  → research_architect_agent: Methodology blueprint
  → devils_advocate_agent: CHECKPOINT 1
  [USER CONFIRMATION REQUIRED]

Phase 2: INVESTIGATION
  → bibliography_agent: Systematic search + annotated bibliography
  → source_verification_agent: Evidence grading + predatory screening

Phase 3: ANALYSIS
  → synthesis_agent: Thematic synthesis + gap analysis
  → devils_advocate_agent: CHECKPOINT 2 (cherry-picking, bias check)

Phase 4: COMPOSITION
  → report_compiler_agent: APA 7.0 full report

Phase 5: REVIEW (Parallel)
  → editor_in_chief_agent: Verdict
  → ethics_review_agent: Ethics clearance
  → devils_advocate_agent: CHECKPOINT 3

Phase 6: REVISION
  → Max 2 loops; unresolved → "Acknowledged Limitations"
```

### Academic Paper (8 Phases)

```
Phase 0: CONFIG → intake_agent → Paper Configuration Record
Phase 1: RESEARCH → literature_strategist → Search Strategy + Corpus
Phase 2: ARCHITECTURE → structure_architect → Outline + Evidence Map
Phase 3: ARGUMENTATION → argument_builder → Argument Blueprint
Phase 4: DRAFTING → draft_writer → Complete Draft
Phase 5a: CITATIONS → citation_compliance ──┐
Phase 5b: ABSTRACT → abstract_bilingual  ──┘ (parallel)
Phase 6: PEER REVIEW → peer_reviewer → Review Report (max 2 loops)
Phase 7: FORMAT → formatter → Final Output Package
```

**Iron rules**:
- User must confirm Paper Configuration Record before Phase 1
- User must approve outline before Phase 3
- Max 2 revision loops; unresolved → "Acknowledged Limitations"
- Critical peer-review issues block Phase 7

### Paper Reviewer (3 Phases)

```
Phase 0: FIELD ANALYSIS
  → field_analyst_agent: 5 reviewer identities
  [User can adjust identities]

Phase 1: PARALLEL MULTI-PERSPECTIVE REVIEW
  → eic_agent → EIC Report
  → methodology_reviewer_agent → Methods Report
  → domain_reviewer_agent → Domain Report
  → perspective_reviewer_agent → Perspective Report
  → devils_advocate_reviewer_agent → Devil's Advocate Report

Phase 2: EDITORIAL SYNTHESIS
  → editorial_synthesizer_agent: Decision + Roadmap

Phase 2.5: REVISION COACHING (if Minor/Major)
  → Socratic guidance through revision strategy
```

**Iron rules**:
- 5 reviewers review independently, no cross-referencing
- Synthesizer cannot fabricate comments
- Devil's Advocate CRITICAL issues → Decision cannot be Accept
- Reviewers are READ-ONLY; never modify the manuscript

---

## Output Formats

**Text**: Markdown (default), DOCX (via Pandoc), LaTeX (.tex + .bib), PDF

**Citations**: APA 7.0 (default), Chicago, MLA 9, IEEE, Vancouver

**Figures**: Python (matplotlib/seaborn) or R (ggplot2) code with APA 7.0 formatting, colorblind-safe palettes, LaTeX `\includegraphics`

**Languages**: English, Chinese (bilingual abstracts supported)

**Paper structures**: IMRaD, Thematic Literature Review, Theoretical Analysis, Case Study, Policy Brief, Conference Paper

---

## Quality Safeguards

### Integrity Verification (Stages 2.5 & 4.5)

5-phase blocking verification:
1. References existence and accessibility
2. Citation accuracy and completeness
3. Data and figure integrity
4. Originality screening
5. Claims verification

Plus mandatory 7-mode AI Research Failure Mode Checklist:
- Implementation bugs
- Hallucinated results
- Citation hallucinations
- Frame-lock
- Sycophancy
- Methodology fabrication
- Overgeneralization

**Stage 4.5 must pass with zero issues.**

### Three-Layer Citation Anchors (L3)

Every claim requiring support must have:
1. **Quote anchor**: Exact quote from source
2. **Page/section anchor**: Specific location
3. **Paragraph anchor**: Context within source argument

### Temporal Integrity Verification

5 failure modes checked:
- P1: Citing outdated sources when newer exist
- P2: Temporal misattribution (presenting old finding as current)
- P3: Missing temporal context in claims
- P4: Inconsistent timeline across sections
- P5: Failed update after monitoring alerts

### Anti-Sycophancy Protections

- **Concession Threshold Protocol**: Flag uncritical acceptance of feedback
- **Intent Detection**: Distinguish user preference from suggestion
- **Dialogue Health Indicator**: Monitor for degradation in critical distance

### Style Calibration & Writing Quality

- Optional style learning from 3+ past papers (soft guide)
- Writing quality check flags: AI-typical terms, em-dash overuse, throat-clearing openers, uniform paragraphs, monotonous rhythm

---

## Adaptive Checkpoint System

After every stage, proactively prompt user confirmation. Three checkpoint types:

| Type | When | Can Skip? |
|------|------|-----------|
| **FULL** | First checkpoint; integrity boundaries; before finalization; after 4+ continues | No |
| **SLIM** | After 2+ consecutive "continue" on non-critical stages | No |
| **MANDATORY** | Integrity gates (2.5/4.5), review decisions, Stage 5 | **Never** |

**Self-check questions** (before every FULL checkpoint):
1. Citation integrity: any unverified citations?
2. Sycophantic concession: uncritical acceptance of feedback?
3. Quality trajectory: output ≥ previous stage quality?
4. Scope discipline: any off-roadmap content added?
5. Completeness: all requested sections delivered?

**Decision Dashboard template** (FULL checkpoints):
```
━━━ Stage [X] [Name] Complete ━━━
Metrics:
- Word count: [N] (target: [T])    [OK/OVER/UNDER]
- References: [N] (min: [M])       [OK/LOW]
- Coverage: [N]/[T] sections       [COMPLETE/PARTIAL]
Flagged: [issues or "None"]
Ready to proceed to Stage [Y]?
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Cross-Model Verification (Optional)

Set environment preference `ARS_CROSS_MODEL=1` to enable:
- Critical claims verified against a second model
- Discrepancies flagged for human resolution
- Confidence scoring per claim

**Claim Audit** (`ARS_CLAIM_AUDIT=1`): L3 claim-faithfulness audit at Stage 4→5 transition. HIGH-WARN classes gate-refuse output.

---

## Common Pitfalls

1. **Skipping integrity gates (2.5 / 4.5)**. These are blocking for a reason — AI failure modes (hallucinated citations, fabricated methodology) are common. Never bypass.

2. **Letting the AI define your research question without pushback**. The `socratic` mode is guidance, not authority. Challenge assumptions, refine scope, make the RQ your own.

3. **Accepting devil's advocate findings at face value**. Devil's Advocate is designed to be contrarian — some challenges will be weaker than others. Use your judgment.

4. **Running full pipeline when you only need one stage**. If you just need a literature review, use Deep Research directly. Pipeline overhead is only justified for end-to-end workflows.

5. **Ignoring the "Acknowledged Limitations" section**. Unresolved issues from revision loops must be documented, not buried. Transparency strengthens credibility.

6. **Forgetting bilingual abstracts for Chinese-English papers**. The `abstract_bilingual_agent` produces both zh-CN and EN abstracts with 5–7 keywords each. Request explicitly if needed.

7. **Over-relying on AI for statistical analysis**. The `visualization_agent` generates code — you must verify the analysis logic, check assumptions, and run the code yourself.

8. **Not using `plan`/`socratic` mode when uncertain**. When in doubt, guide first. Producing a full draft for a poorly scoped question wastes tokens and time.

9. **Treating reviewer simulation as ground truth**. The simulated peer review is a pre-submission tool, not a guarantee of actual review outcomes. Use it to find weaknesses, not to predict decisions.

10. **Modifying the manuscript during review mode**. Review agents are READ-ONLY. If an agent tries to rewrite your paper during review, stop and redirect to report generation.

---

## Verification Checklist

- [ ] Frontmatter `name`, `description`, `version`, `author`, `license`, `metadata.hermes` all present
- [ ] Description ≤ 1024 chars and starts with trigger description
- [ ] Total file ≤ 100,000 chars
- [ ] `name` ≤ 64 chars, lowercase + hyphens
- [ ] `related_skills` references are valid in-repo or user-local skills
- [ ] Structure: `# Title` → `## Overview` → `## When to Use` → body → `## Common Pitfalls` → `## Verification Checklist`
- [ ] File is at `skills/research/academic-research-suite-hermes/SKILL.md` (in-repo) or `~/.hermes/skills/academic-research-suite-hermes/SKILL.md` (user-local)
- [ ] `git add` + `git commit` completed if in-repo
