# Claude Code Skills for Academic Research

Reusable [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skills — markdown prompt files that run as slash commands — designed for academic economists and social scientists working with research papers and replication packages.

📄 **Full documentation: <https://lcrawfurd.github.io/claude-skills/>**

## Skills

| Skill | Purpose |
|---|---|
| [`paper-review`](paper-review.md) | Review papers using 5 frameworks (Edmans, Nyhan, Humphreys, Blattman, Evans/Bellemare) |
| [`code-review`](code-review.md) | Replication-package audit for Stata/R/Python projects (Gentzkow & Shapiro, DIME, AEA Data Editor, SSDE) |
| [`referee2`](referee2.md) | Computational reproducibility audit — 5 parallel audits (Scott Cunningham's MixtapeTools protocol) |
| [`backmanreview`](backmanreview.md) | 6-agent pre-submission referee report targeting a specific journal |
| [`openaireview`](openaireview.md) | Deep-review with parallel sub-agents for section-level scrutiny (OpenAIReview / Chicago HAI) |
| Coarse Review | Run the full [coarse.ink](https://coarse.ink) pipeline locally on your Claude Code subscription |

## Install

The easiest way is to point Claude Code at this repo and ask it to install the skills for you:

> Just paste <https://lcrawfurd.github.io/claude-skills/> into Claude Code and ask it to install the skills.

Or manually copy each skill's markdown into `~/.claude/skills/<skill-name>/SKILL.md`:

```
~/.claude/skills/
├── paper-review/SKILL.md
├── code-review/SKILL.md
├── referee2/SKILL.md
├── backmanreview/SKILL.md
└── openaireview/SKILL.md
```

Then invoke as slash commands:

```
/paper-review path/to/paper.pdf
/code-review path/to/project/
/referee2 path/to/project/
/backmanreview QJE path/to/paper.tex
/openaireview path/to/paper.pdf
```

## Also works on Codex

These are just markdown prompt files, so they work equally well in [OpenAI Codex](https://openai.com/codex/) (and other agentic coding tools that read local instruction files). Drop the SKILL contents into a Codex `AGENTS.md`, save as a Codex prompt, or paste in directly — the frameworks and checklists are model-agnostic.

## Author

Maintained by [Lee Crawfurd](https://lcrawfurd.github.io/) (Center for Global Development). Frameworks credited inline in each skill file. Contributions and issues welcome.
