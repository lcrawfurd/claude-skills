---
layout: default
title: OpenAI Review
---

[← Back to all skills](./)

# OpenAI Review: Deep Multi-Agent Paper Review

Based on [OpenAIReview](https://openaireview.github.io/blog.html) by [Chenhao Tan and the Chicago Human-AI Institute](https://github.com/ChicagoHAI/OpenAIReview). Deep-review an academic paper using parallel sub-agents for section-level scrutiny. Produces tiered findings (major/moderate/minor) and saves viz-compatible results.

## Usage

```
/openaireview <path-or-arxiv-url>
```

Examples:
- `/openaireview paper.pdf`
- `/openaireview https://arxiv.org/abs/2401.12345`
- `/openaireview paper.tex`

## How It Works

The skill runs a structured multi-pass review pipeline:

### Step 1 — Prepare Workspace

Automatically detects the input type (PDF, arXiv URL, `.tex`/`.txt`/`.md`), downloads if needed (arXiv HTML preferred, PDF fallback), parses the paper, splits it into sections, and writes a workspace to `/tmp/<slug>_review/`.

### Step 2 — Pass A: Understand the Paper

Reads the complete text including all appendices and tables, then builds a comprehensive structured summary covering:

- Research question and core hypothesis
- Methodology overview
- Key definitions, notation, and numerical parameters
- Main claims with evidence locations
- Section map and cross-references

### Step 3 — Pass B: Parallel Sub-Agent Review

Plans and launches **6-9 sub-agents in parallel**:

**Section sub-agents** (one per major section or logical group):
- Each gets a primary section file and 1-3 related section files for cross-references
- Small or closely related sections are grouped together (e.g., Abstract + Introduction)

**Cross-cutting sub-agents** (2-3, chosen based on what the paper needs):
- Do abstract/introduction claims match evidence in results?
- Are evaluation comparisons fair and consistent?
- Do stated limitations and mitigations hold up?
- Other paper-specific concerns identified in Pass A

### Step 4 — Consolidate and Tier Findings

After all sub-agents complete:

1. **Gather** results from all sub-agents
2. **Deduplicate** — remove duplicates, keeping the better-explained version
3. **Validate** — remove false positives, verify quotes appear in paper text
4. **Assign severity tiers:**
   - **Major** — undermines a key claim, methodology, or comparison; affects conclusions
   - **Moderate** — real error or gap that is localized and fixable
   - **Minor** — framing concern, mild overclaim, or ambiguity resolvable from context

### Step 5 — Present Review

Outputs a structured review grouped by severity, with each issue including:
- A descriptive title
- Issue type (`technical` or `logical`)
- An exact verbatim quote from the paper
- A clear explanation

### Step 6 — Save Viz JSON

Saves results to `./review_results/<slug>.json` for visualization with `openaireview serve`.

## Installation

This skill requires additional Python scripts bundled alongside the SKILL.md. See the [OpenAIReview GitHub repo](https://github.com/ChicagoHAI/OpenAIReview) for the full installation, or install via:

```bash
pip install openaireview
```
