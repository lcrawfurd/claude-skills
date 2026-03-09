---
layout: default
title: Paper Review
---

[← Back to all skills](./)

# Paper Review

Review academic research papers using established frameworks and guidelines.

## Usage

```
/paper-review <path-to-paper>
```

## Frameworks

When reviewing a paper, read the provided file first, then apply the following evaluation frameworks:

### 1. [Edmans' Framework for Editorial Assessment](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4336383)

Evaluate the research paper intended for submission to a top journal using Edmans' framework for editorial assessment. Assess the paper across the three key dimensions:

**Contribution**
- What is the paper's main contribution to the literature?
- Is the research question important and novel?
- Does it challenge existing knowledge or fill a significant gap?
- Would the findings change how academics or practitioners think or act?

**Execution**
- Is the methodology appropriate for the research question?
- Is the identification strategy sound and convincing?
- Are there threats to internal or external validity?
- Is the data appropriate and the analysis rigorous?
- Are alternative explanations adequately addressed?

**Exposition**
- Is the paper clearly written and well-organized?
- Is the contribution clearly articulated early in the paper?
- Are the results presented effectively?
- Is the paper the appropriate length?

**Feedback Format**

Provide specific, actionable feedback, highlighting:
- **Major concerns** that could lead to rejection
- **Minor issues** that could be improved
- **Strengths** worth preserving or emphasizing

---

### 2. [Nyhan's Checklist for Peer Review](https://polmeth.org/blog/checklist-manifesto-peer-review)

Based on Brendan Nyhan's "Checklist Manifesto for Peer Review" (built from 150+ manuscript reviews), evaluate the paper against these methodological criteria:

1. **Interaction terms**: Does the author properly interpret any interaction terms and include the necessary interactions to test subgroup differences?

2. **P-value interpretation**: Does the author avoid misinterpreting null findings as evidence that true effects equal zero?

3. **Replication materials**: Are questionnaires, study materials, and code included for reproducibility?

4. **Causal language**: Does the author avoid using causal language for correlational findings?

5. **Causal assumptions**: Are assumptions necessary for causal interpretation explicitly stated?

6. **Mediation models**: Are mediation models properly specified using current best practices?

7. **Post-treatment bias**: Does the author avoid controlling for variables affected by the treatment?

8. **Statistical power**: Does the study have sufficient statistical power to test the hypothesis of interest reliably?

9. **Subgroup analyses**: Are subgroup analyses adequately powered and theoretically justified rather than data-driven?

Provide actionable feedback on any checklist items where the manuscript falls short, with specific suggestions for improvement.

---

### 3. [Humphreys' Comprehensive Review Framework](https://macartan.github.io/teaching/how-to-critique)

Based on Macartan Humphreys' guide to critiquing research papers. Structure formal reviews in three parts:

**Part 1: Summary Paragraph**
- Summarize the key contribution as you see it
- Give an overall assessment
- Point to key issues, concerns, and strengths
- Articulate succinctly: what do you know now that you didn't know before reading this piece?

**Part 2: Major Themes (3-6 issues)**

Organize feedback by theme, drawing from these categories:

*Theory*
- Is the theory internally consistent?
- Is it consistent with past literature and findings?
- Is it novel or surprising?
- Are excluded/simplified elements plausibly unimportant?
- Is the theory general or specific? Could it draw on or contribute to more general theories?

*From Theory to Hypotheses*
- Is the theory really needed to generate the hypotheses?
- Does the theory generate more hypotheses than considered?
- Are the hypotheses really implied by the theory, or are there ambiguities (non-monotonicities, multiple equilibria)?
- Does the theory specify mechanisms and suggest heterogeneous effects?

*Hypotheses*
- Are hypotheses complex (multiple hypotheses bundled together)?
- Are hypotheses falsifiable?

*Evidence I: Design*
- External validity: Is the population representative? Are conditions consistent with conditions of interest?
- Measure validity: Do measures capture the theoretical objects?
- Consistency: Is the empirical model consistent with the theory?
- Mechanisms: Are mechanisms tested? How are they identified?
- Replicability: Can the study be replicated?
- Interpretation: Do results admit rival interpretations?

*Evidence II: Analysis and Testing*
- Identification: Concerns with reverse causality? Omitted variable bias?
- Does the model control for pre-treatment variables only?
- Are poorly identified claims flagged as such?
- Robustness: Results robust to model changes, data subsetting, period changes, control variations?
- Standard errors: Do calculations use the design? Account for clustering?
- Presentation: Are results intelligible (fitted values, graphs)?
- Interpretation: Can "no evidence of effect" be interpreted as evidence of only weak effects?

*Evidence III: Other Sources of Bias*
- Fishing: Were hypotheses generated prior to testing? Training/test data separated?
- Measurement error: Is error correlated with outcomes?
- Spillovers/Contamination: Could control units be affected by treatment?
- Compliance: Did treated get treatment? Did controls avoid it?
- Hawthorne effects: Are subjects modifying behavior because they know they're under study?
- Measurement: Is treatment the only systematic difference, or are there measurement differences?
- Implications of bias: Do sources of bias work for or against the hypothesis?

*Explanation*
- Does evidence support the particular causal account given?
- Are mechanisms examined? Can they be?
- Are there observable implications for different possible mechanisms?

*Policy Implications*
- Do policy implications really follow from results?
- Would implementation have effects other than those specified?
- Have policy claims been tested directly?
- Is the author overselling or underselling findings?

**Part 3: Smaller Issues**

Bullet point items including:
- Ambiguities
- Estimation issues
- Pointers to other relevant work
- What to cut (reviews ask for more but worry about length)

**Review Conduct Guidelines**
- Point to literature authors may have missed, if relevant
- Maintain a tone you wouldn't be embarrassed by if the review became public
- Feel free to request replication data or analysis plans
- Don't ask authors to answer a different question — respond to the paper sent
- Be generous: don't assume intentional omissions, ethical lapses, or misleading reporting
- Use "you" or "they" for anonymous review even with single authorship

---

### 4. [Blattman's Empirical Paper Review Guide](https://chrisblattman.com/blog/2012/01/18/how-to-referee-an-academic-paper/)

Chris Blattman's structured approach for reading and reviewing empirical papers:

**Research Question and Hypothesis**
- Is the researcher focused on well-defined questions?
- Is the question interesting and important?
- Are the propositions falsifiable?
- Has the alternative hypothesis been clearly stated?
- Is the approach inductive, deductive, or data mining? Is this the right structure?

**Research Design**
- Is the author attempting to identify a causal impact?
- Is the "cause" clear? Is there a cause/treatment/program/first stage?
- Is the relevant counterfactual clearly defined and compelling?
- Is the method clear and compelling? Has statistical inference been confused with causal inference?
- Does the research design identify a very narrow or very general source of variation?
- Could the question be addressed with another approach?
- *Useful trick*: Ask yourself, "What experiment would someone run to answer this question?"

**Theory/Model**
- Is the theory/model clear, insightful, and appropriate?
- Could the theory benefit from being more explicit, developed, or formal?
- Are there clear predictions that can be falsified? Are these predictions "risky" enough?
- Does the theory generate any prohibitions that can be tested?
- Would an alternative theory/model be more appropriate?
- Could alternative models produce similar predictions — does evidence on predictions necessarily weigh on the model or explanation?
- Is the theory a theory, or a list of predictions?
- Is the estimating equation clearly related to or derived from the model?

**Data**
- Are the data clearly described?
- Is the choice of data well-suited to the question and test?
- Are there worrying sources of measurement error or missing data? Are proxies reasonable?
- Are there sample size or power issues?
- Could the data sources or collection method be biased?
- Are there better sources of data you would recommend?
- Are there types of data that should have been reported, or would be useful/essential?

**Empirical Analysis**
- Are the statistical techniques well suited to the problem?
- What are the endogenous and exogenous variables?
- Has the paper adequately dealt with measurement error, simultaneity, omitted variables, selection, and other identification problems?
- Is there selection not just in who receives treatment, but in who we observe or measure?
- Is the empirical strategy convincing?
- Could differencing or fixed effects exacerbate measurement error?
- Did the author make assumptions for identification (distributions, exogeneity, etc.)?
- Were these assumptions tested? If not, how would you test them?
- Are results robust to alternative assumptions?
- Does the disturbance term have an interpretation, or is it just tacked on?
- Are observations i.i.d.? If not, have corrections to standard errors been made?
- What additional robustness tests would you suggest?
- Are there dangers in the empirical strategy (sensitivity to identification assumptions)?
- Can you imagine a better or alternative empirical strategy?

**Results**
- Do results adequately answer the question?
- Are conclusions convincing? Are appropriate caveats mentioned?
- What variation in the data identifies the model elements?
- Are there alternative explanations, and can we test for them?
- Could the author take analysis further (impact heterogeneity, causal mechanisms, effects on other variables)?
- Is absence of evidence confused with evidence of absence?

**Scope**
- Can we generalize these results?
- Has the author specified scope conditions?
- Have causal mechanisms been explored?
- Are there further analyses that would illuminate external validity or causal mechanisms?
- Are there other data or approaches that would complement this one?

---

### 5. Evans & Bellemare: Introduction, Abstract, and Conclusion Structure

Based on David Evans' guides on writing [introductions](https://www.cgdev.org/blog/how-write-introduction-your-development-economics-paper) and [abstracts](https://www.cgdev.org/blog/how-write-abstract-your-development-economics-paper) for development economics papers, and Marc Bellemare's ["Conclusion Formula"](https://marcfbellemare.com/wordpress/12060).

**Introduction Structure (Evans, drawing on Keith Head's "Introduction Formula")**

You win or lose readers with the introduction. Papers with more readable introductions get cited more. Evaluate whether the introduction follows this pattern:

1. **Hook** (1-2 paragraphs): Does it attract reader interest by showing the topic matters?
   - Y matters (people are hurt or helped)
   - Y is puzzling (defies easy explanation)
   - Y is controversial
   - Y is big or common
   - The motivation must be about the economics — NEVER start with literature or a new technique

2. **Research Question** (1 paragraph): Is the question clearly stated?
   - Lead with YOUR question
   - Be specific and motivate YOUR research question

3. **Antecedents** (integrated): What prior work does this build on?
   - No need for a separate "Literature Review" section
   - Should be woven into the introduction
   - Focus on the closest 5-7 studies

4. **Value-Added** (1 paragraph): How does this add to prior work?
   - Approximately 3 contributions relative to antecedents
   - This may be the most important paragraph for convincing referees
   - Contributions should make sense only in light of prior work

5. **Roadmap**: Brief guide to paper structure

**Abstract Structure (Evans)**

Use all words allowed and use them wisely. More readable abstracts (simpler words, shorter sentences) get more citations. Typical structure:

1. (Sometimes) One sentence of motivation
2. Research question and empirical approach — often start directly here
3. Detailed discussion of results (most of the space)
4. (Sometimes) One sentence on implications

Word limits vary: AER/AEJ allow 100 words (~4-5 sentences); QJE allows 250; JDE allows 150.

**Conclusion Structure (Bellemare's "Conclusion Formula")**

1. **Summary**: Tell them what you told them — but differently from abstract/intro. Present as narrative if possible.

2. **Limitations**: Emphasize constraints of methodology and approach.

3. **Policy Implications**: Discuss real-world applications, but avoid unsupported claims.
   - Assess costs against benefits, even approximately
   - Identify clear winners and losers (2-3 sentences)
   - Evaluate political feasibility and implementation difficulty

4. **Future Research**: Acknowledge imperfections and suggest extensions.
   - How could theoretical contributions be generalized?
   - How might empirical work achieve better causal identification?
   - How could findings be tested in additional contexts?

**Evaluation Questions**

When reviewing, ask:
- Does the introduction clearly convey: why this matters, what was done, what was learned, how it builds on prior work?
- Is the hook about economics/policy, not about literature or methods?
- Does the value-added paragraph make clear contributions relative to specific prior papers?
- Does the abstract lead with the question and spend most space on results?
- Does the conclusion go beyond summary to discuss limitations, implications, and future directions?
- Is the author overselling or underselling findings in the conclusion?
