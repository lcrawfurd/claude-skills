---
layout: default
title: Claude Code Skills for Academic Research
---

# Claude Code Skills for Academic Research

These are [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skills — reusable prompt templates that run as slash commands inside Claude Code. They're designed for academic economists and social scientists working with research papers and replication packages.

## What are Claude Code skills?

[Claude Code](https://docs.anthropic.com/en/docs/claude-code) is Anthropic's AI coding agent that runs in your terminal or in the app. **Skills** are reusable prompt files (written in markdown) that you can invoke as slash commands — like `/paper-review` or `/code-review` — to run structured, multi-step tasks. When you type a slash command, Claude Code reads the skill file and follows its instructions, applying the frameworks and checklists defined within it to whatever file or folder you point it at.

## Skills

### [Paper Review](paper-review)
Review academic research papers using 5 established frameworks: [Edmans'](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4336383) editorial assessment, [Nyhan's](https://polmeth.org/blog/checklist-manifesto-peer-review) peer review checklist, [Humphreys'](https://macartan.github.io/teaching/how-to-critique) comprehensive review, [Blattman's](https://chrisblattman.com/blog/2012/01/18/how-to-referee-an-academic-paper/) empirical paper guide, and [Evans](https://www.cgdev.org/blog/how-write-introduction-your-development-economics-paper) & [Bellemare](https://marcfbellemare.com/wordpress/12060) on introductions, abstracts, and conclusions.

### [Code Review](code-review)
Review a development economics project folder for replication best practices. Based on [Gentzkow & Shapiro](https://web.stanford.edu/~gentzkow/research/CodeAndData.pdf), [DIME Analytics](https://worldbank.github.io/dime-data-handbook/coding.html), [Julian Reif](https://julianreif.com/guide/), [AEA Data Editor / Vilhuber](https://aeadataeditor.github.io/), and the [Social Science Data Editors Template README](https://social-science-data-editors.github.io/template_README/). Covers folder structure, master scripts, coding standards (Stata/R/Python), data management, output reproducibility, and documentation.

### [Referee 2](referee2)
A systematic computational reproducibility audit protocol with 5 parallel audits: code audit, cross-language replication, directory & replication package, output automation, and econometrics. Based on [Scott Cunningham's MixtapeTools](https://github.com/scunning1975/MixtapeTools) Referee 2 protocol.

### [Pre-Submission Review](backmanreview)
A 6-agent pre-submission referee report targeting a specified journal. Runs spelling/grammar, internal consistency, unsupported claims, mathematics/notation, tables/figures, and contribution evaluation agents in parallel, then consolidates into a prioritised report. Based on [Claes Backman's AI Research Feedback](https://github.com/claesbackman/AI-research-feedback).

### [OpenAI Review](openaireview)
Deep-review an academic paper using parallel sub-agents for section-level scrutiny. Runs a multi-pass pipeline: first understanding the full paper, then launching 6-9 parallel sub-agents (section reviewers + cross-cutting checks), then consolidating and tiering findings as major/moderate/minor. Based on [OpenAIReview](https://openaireview.github.io/blog.html) by [Chenhao Tan and the Chicago Human-AI Institute](https://github.com/ChicagoHAI/OpenAIReview).

## Installation

The easiest way to install is to give Claude Code the link to this page and ask it to install the skills:

```
Just paste https://lcrawfurd.github.io/claude-skills/ into Claude Code
and ask it to install the skills for you.
```

Or manually copy each skill's markdown file into your `~/.claude/skills/` directory:

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
