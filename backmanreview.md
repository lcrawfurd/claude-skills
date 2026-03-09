---
layout: default
title: Pre-Submission Review
---

[← Back to all skills](./)

# Pre-Submission Review: 6-Agent Referee Report

Based on [Claes Backman's AI Research Feedback](https://github.com/claesbackman/AI-research-feedback). A rigorous pre-submission review of an academic economics paper. Runs 6 specialized review agents in parallel and consolidates their findings into a structured report.

## Usage

```
/backmanreview [journal] [path-to-paper]
```

Examples:
- `/backmanreview QJE paper.tex` — review targeting the Quarterly Journal of Economics
- `/backmanreview AER` — review targeting AER, auto-detecting the paper
- `/backmanreview paper.tex` — review with general top-field standards

**Supported journals:** AER, QJE, JPE, Econometrica, REStud, JF, JFE, RFS, JFQA, AEJMacro, JME, RED

## Phase 1: Discover the Paper

The skill automatically:
1. Finds the main LaTeX file (the one with `\documentclass` or `\begin{document}`)
2. Extracts all `\input{}`, `\include{}`, and `\subfile{}` references
3. Reads all component .tex files
4. Locates all figure and table files

## Phase 2: The 6 Agents

All 6 agents launch in parallel, each reading the paper independently.

---

### Agent 1 — Spelling, Grammar & Academic Style

A copy editor at a top economics journal checking:

1. **Spelling errors** — including proper nouns and technical terms
2. **Grammar errors** — subject-verb agreement, tense consistency, article usage, dangling modifiers
3. **Awkward phrasing** — sentences that require re-reading
4. **Style violations** — flags filler words ("interestingly", "importantly", "it is worth noting"), tautologies, misuse of "significant", passive voice, inconsistent first person
5. **Typographic consistency** — hyphenation, dashes, spacing
6. **Number formatting** — spelling out numbers below 10, consistent percentage notation

---

### Agent 2 — Internal Consistency & Cross-Reference Verification

A technical reviewer checking internal coherence:

1. **Numerical consistency** — every number in text verified against tables/figures
2. **Abstract vs. body** — do numbers and claims match?
3. **Introduction vs. results** — does the intro preview what the results deliver?
4. **Cross-reference correctness** — every "Figure X", "Table Y", "Appendix A" verified
5. **Terminology consistency** — key terms used consistently throughout
6. **Sample description** — consistent across abstract, data section, and table notes
7. **Fixed effects and controls** — match between text and tables
8. **Magnitude consistency** — direction and magnitude consistent across all mentions
9. **Literature citations** — cited papers exist in bibliography, characterizations plausible

---

### Agent 3 — Unsupported Claims & Identification Integrity

A skeptical econometrician enforcing "claim discipline":

1. **Causal language without causal identification** — flags "causes", "leads to", "drives" where only correlation is shown
2. **Generalization beyond the sample** — extending findings beyond the data's scope
3. **Mechanism claims stated as facts** — proposed explanations asserted rather than argued
4. **Unsupported robustness claims** — "robust to X" without showing the check
5. **Missing necessary caveats** — obvious threats to validity not discussed
6. **Literature overclaiming** — "we are the first" claims that may be false
7. **Statistical vs. economic significance conflation**
8. **Hedging failures** — both overconfident and underconfident

---

### Agent 4 — Mathematics, Equations & Notation

A mathematical economist reviewing formal content:

1. **Mathematical correctness** — derivations, algebra, regression subscripts
2. **Notation consistency** — same symbol for same quantity throughout
3. **Undefined notation** — symbols used without definition
4. **Equation numbering** — numbered equations referenced, unreferenced equations flagged
5. **Regression specification consistency** — equation matches text, tables, and controls
6. **Return/growth rate definitions** — annualization, percentage vs. percentage points
7. **Statistical notation** — SE, t-stat, CI formulas correct
8. **LaTeX formatting** — missing `\left`/`\right`, improper multiplication, text in math mode

---

### Agent 5 — Tables, Figures & Their Documentation

A journal production editor checking completeness:

**For every table:**
- Title accurately describes contents
- Column headers clear and unambiguous
- Notes cover: sample, dependent variable, controls, fixed effects, SE clustering, significance stars
- Standard errors reported in every column
- N reported in every column
- Referenced in main text

**For every figure:**
- Title is self-contained
- Axes labeled with units
- Legend present for multiple series
- Confidence intervals shown (binscatter, coefficient plots, event studies)
- Notes cover: sample, what is plotted, data source

---

### Agent 6 — Contribution Evaluation (Adversarial Referee)

A demanding associate editor with journal-specific standards:

1. **Central Contribution** — is the finding genuinely new? Rate: Transformative / Significant / Incremental / Insufficient
2. **Identification and Credibility** — is variation plausibly exogenous? What are the threats?
3. **Required Analyses** (3-5 blockers) — missing robustness checks, alternative explanations, placebo tests
4. **Suggested Analyses** (3-5 improvements) — mechanism tests, subgroup analyses, extensions
5. **Literature Positioning** — right papers cited? Best framing?
6. **Journal Fit** — recommendation: Send to referees / Revise before sending / Desk reject
7. **Pointed Questions** — 4-7 hard questions for the authors

## Phase 3: Consolidated Report

Saved to `PRE_SUBMISSION_REVIEW_[YYYY-MM-DD].md` with:

- Overall assessment and preliminary recommendation
- All 6 agent outputs in full
- **Priority Action Items** ranked by triage hierarchy:
  - CRITICAL: identification failures, missing required analyses, internal inconsistencies
  - MAJOR: tables/figures documentation, mathematical errors
  - MINOR: style and grammar polish
