---
layout: default
title: Claude Code Skills for Academic Research
---

# Claude Code Skills for Academic Research

These are [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skills — reusable prompt templates that run as slash commands inside Claude Code. They're designed for academic economists and social scientists working with research papers and replication packages.

## Skills

### [Paper Review](paper-review)
Review academic research papers using 5 established frameworks: Edmans' editorial assessment, Nyhan's peer review checklist, Humphreys' comprehensive review, Blattman's empirical paper guide, and Evans & Bellemare on introductions, abstracts, and conclusions.

### [Code Review](code-review)
Review a development economics project folder for replication best practices. Based on Gentzkow & Shapiro, DIME Analytics, Julian Reif, AEA Data Editor / Vilhuber, and the Social Science Data Editors Template README. Covers folder structure, master scripts, coding standards (Stata/R/Python), data management, output reproducibility, and documentation.

### [Referee 2](referee2)
A systematic computational reproducibility audit protocol with 5 parallel audits: code audit, cross-language replication, directory & replication package, output automation, and econometrics. Based on Scott Cunningham's MixtapeTools Referee 2 protocol.

### [Pre-Submission Review](backmanreview)
A 6-agent pre-submission referee report targeting a specified journal. Runs spelling/grammar, internal consistency, unsupported claims, mathematics/notation, tables/figures, and contribution evaluation agents in parallel, then consolidates into a prioritised report.

## Installation

To use these skills in Claude Code, copy each skill's markdown file into your `~/.claude/skills/` directory:

```
~/.claude/skills/
├── paper-review/
│   └── SKILL.md
├── code-review/
│   └── SKILL.md
├── referee2/
│   └── SKILL.md
└── backmanreview/
    └── SKILL.md
```

Then invoke them as slash commands:

```
/paper-review path/to/paper.pdf
/code-review path/to/project/
/referee2 path/to/project/
/backmanreview QJE path/to/paper.tex
```
