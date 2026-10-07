# Reviewer Mindset Library (Skill Snapshot)

## Table of Contents

- [Cluster 3: Precise Constructive](#cluster-3-precise-constructive)
- [Cluster 4: Mild Skeptic](#cluster-4-mild-skeptic)
- [Cluster 0: Authoritative Negativist](#cluster-0-authoritative-negativist)
- [Cluster 5: Harsh Dismissive](#cluster-5-harsh-dismissive)
- [Cluster 1: Gentle Constructive](#cluster-1-gentle-constructive)
- [Cluster 2: Concise Affirmative](#cluster-2-concise-affirmative)

> Auto-generated from `data/behavior/mindset_library.json`.

Modeling method: `behavior_space_kmeans_llm`, 6 mindset clusters in total.

---

## Cluster 3: Precise Constructive

**Profile**: These reviewers care deeply about the paper's executability and concrete details, and tend to make clear, actionable suggestions that cite specific literature or methods. Their criticism is moderate in severity but highly constructive, and they are easy to persuade; the core mindset is to help the authors improve the paper rather than to reject the work.

| Metric | Value |
|--------|-------|
| Share of samples | 9.5% (95 reviews) |
| Historical score-increase rate | 36.1% |
| Acceptance rate | 43.2% |
| Successful rebuttal samples | 44 |

### Recognition signals

- Points out missing specifics, such as parameter sizes, formula forms, or implementation steps
- Cites specific literature or methods and points out contradictions or shortcomings relative to existing work
- Makes explicit revision suggestions, such as "please clarify" or "a concrete form needs to be given"

### Rule-statistic differences (Top 3)

- **Explicit commitment to revise**: success 65.9% vs failure 81.8% (Δ -15.9)
- **Direct quotation / point-by-point response**: success 77.3% vs failure 66.7% (Δ +10.6)
- **New experiments / new results**: success 61.4% vs failure 51.5% (Δ +9.9)

### Strategy-vector effects (Cohen's d)

**Significantly higher in the success group (Cohen's d):**
- `structure_quality`: success mean 4.614 / failure mean 3.157 (d=1.107)
- `paper_grounding`: success mean 4.386 / failure mean 2.98 (d=1.074)
- `clarification_quality`: success mean 4.636 / failure mean 3.235 (d=1.07)

**Higher in the failure group (risk dimensions):**
- `vague_future_work`: success mean 1.386 / failure mean 2.333 (d=-0.727)
- `overpromise_risk`: success mean 1.295 / failure mean 1.745 (d=-0.432)

### Success patterns (LLM-derived)

- **Structured, direct response**: Respond to each of the reviewer's weaknesses with a number or heading, quote the original comment, and give a concrete explanation or evidence, avoiding vague explanations.
- **Specific evidence and paper grounding**: Provide new experiments, figures, or quantitative results to support the argument, and cite specific locations in the paper (such as sections, figures, tables) to increase credibility.
- **Confident and restrained tone**: Respond in a positive, confident tone while staying constructive, avoiding defensiveness or over-promising, and stating the improvements already made when acknowledging limitations.
- **Controlled concessions and commitments**: While acknowledging limitations, state clearly the improvements already made or future directions, avoiding vague "future work" or over-promising.

### Failure patterns (LLM-derived)

- **Vague future-work commitments**: Using vague phrasing such as "future work" or "we plan to" with no concrete action or evidence, leading the reviewer to feel the response is inadequate or evasive.
- **Over-promising or generalities**: Promising many improvements without a concrete plan or evidence, or responding only with general statements, so the reviewer finds it unrealistic or not credible.
- **Long explanations without structure**: Lengthy responses that do not directly quote the reviewer's specific questions, making it hard for the reviewer to locate key information quickly and lowering persuasiveness.
- **Over-explaining or dodging the core issue**: Giving long theoretical explanations to a technical doubt without new evidence or a direct acknowledgment of the limitation, leaving the reviewer unconvinced.

### Key strategy

Structured direct response + specific evidence + confident, restrained tone

---

## Cluster 4: Mild Skeptic

**Profile**: These reviewers are mild in attitude and their criticism is not sharp, but they lack concrete suggestions and constructiveness. They tend to express confusion or point to surface-level omissions rather than analyze in depth or offer actionable improvements. Their mindset may be neutral or slightly negative toward the paper, but they are reluctant to reject it harshly, so they give middling scores and leave vague doubts.

| Metric | Value |
|--------|-------|
| Share of samples | 20.5% (205 reviews) |
| Historical score-increase rate | 18.7% |
| Acceptance rate | 47.3% |
| Successful rebuttal samples | 99 |

### Recognition signals

- Opens with vague doubts such as 'I am confused' or 'If I’m understanding correctly'
- Points out problems without giving concrete revision suggestions or alternatives
- Short comments lacking in-depth technical analysis of the method or results

### Rule-statistic differences (Top 3)

- **Moderate acknowledgment**: success 54.5% vs failure 66.2% (Δ -11.7)
- **Clarifying explanation**: success 53.5% vs failure 64.6% (Δ -11.1)
- **Explicit commitment to revise**: success 59.6% vs failure 49.2% (Δ +10.4)

### Strategy-vector effects (Cohen's d)

**Significantly higher in the success group (Cohen's d):**
- `tone_confidence`: success mean 4.535 / failure mean 3.0 (d=1.246)
- `direct_address`: success mean 4.515 / failure mean 3.048 (d=1.116)
- `clarification_quality`: success mean 4.404 / failure mean 2.943 (d=1.148)

**Higher in the failure group (risk dimensions):**
- `vague_future_work`: success mean 1.616 / failure mean 2.543 (d=-0.687)
- `overpromise_risk`: success mean 1.404 / failure mean 2.219 (d=-0.685)

### Success patterns (LLM-derived)

- **Confident, direct response**: Respond to the reviewer's doubts directly in a high-confidence tone, avoiding hedging or excessive apology, and showing command of the work.
- **High-quality clarification and paper grounding**: Provide clear, specific clarifications and closely cite the paper's text, figures, appendix, or concrete experimental evidence to support the argument, avoiding empty explanations.
- **Controlled concession with specific evidence**: While acknowledging limitations, immediately balance them with specific evidence (such as new data, analysis, or a controllable improvement plan), avoiding hollow promises or over-conceding.

### Failure patterns (LLM-derived)

- **Over-conceding and vague future work**: Frequently admitting shortcomings without a concrete improvement plan, or using vague commitments such as "future work", which looks unconfident and short on real action and weakens persuasiveness.
- **Long explanations without focus**: Spending too much space clarifying misunderstandings or adding background instead of addressing the problem directly, producing a long response that drifts from the core and lowers the reviewer's reading efficiency.
- **Over-clarifying without paper grounding**: Providing lots of clarifying explanation without citing specific content from the paper (such as tables or appendix), so the response feels empty and cannot persuade the reviewer.

### Key strategy

Respond confidently and directly, anchor to evidence in the paper, concede in a controlled way, and avoid vague commitments.

---

## Cluster 0: Authoritative Negativist

**Profile**: These reviewers are confident and picky, and tend to point out the paper's shortcomings from a position of authority, citing specific literature or technical details to support their negative evaluation. Their writing is direct and concise, often in lists or short sentences, focusing on the paper's flaws and limitations, with low acceptance of the authors' defenses.

| Metric | Value |
|--------|-------|
| Share of samples | 20.4% (204 reviews) |
| Historical score-increase rate | 14.7% |
| Acceptance rate | 27.9% |
| Successful rebuttal samples | 62 |

### Recognition signals

- Lists criticisms in short sentences or list form, such as 'Unclear text encoder'
- Cites specific literature or technical details to negate the paper's contribution, such as 'has been studied in [1]'
- Directly states that the paper's claims are too strong or unsupported, such as 'claims are too strong'

### Rule-statistic differences (Top 3)

- **Explicit commitment to revise**: success 51.6% vs failure 66.2% (Δ -14.6)
- **Direct quotation / point-by-point response**: success 72.6% vs failure 58.8% (Δ +13.8)
- **New experiments / new results**: success 46.8% vs failure 40.0% (Δ +6.8)

### Strategy-vector effects (Cohen's d)

**Significantly higher in the success group (Cohen's d):**
- `clarification_quality`: success mean 4.419 / failure mean 2.794 (d=1.198)
- `direct_address`: success mean 4.613 / failure mean 3.0 (d=1.112)
- `tone_confidence`: success mean 4.452 / failure mean 2.858 (d=1.177)

**Higher in the failure group (risk dimensions):**
- `vague_future_work`: success mean 1.419 / failure mean 2.603 (d=-0.801)
- `overpromise_risk`: success mean 1.323 / failure mean 2.333 (d=-0.767)

### Success patterns (LLM-derived)

- **Confident, direct response**: Respond head-on to the reviewer's specific doubts in a high-confidence, direct tone, avoiding evasion or vague wording.
- **High-quality clarification and paper grounding**: Provide clear, in-depth explanations closely anchored to the paper's text, theoretical basis, or supplementary experiments, showing a deep understanding of the work.
- **Controlled concession with specific evidence**: While acknowledging the reviewer's reasonable points or the work's limitations, support the core contribution with specific experimental data, theoretical analysis, or new evidence, avoiding hollow promises.

### Failure patterns (LLM-derived)

- **Vague future work or over-promising**: Answering criticism with "will be addressed in future work" or exaggerated promises, with no immediate evidence or concrete plan, which is read as dodging the core issue.
- **Dismissive or defensive responses**: Playing down or over-defending against the reviewer's specific criticism, such as 'the bug does not affect the results' or 'not pursuing SOTA', without taking it seriously or explaining in detail, which deepens distrust.
- **Weak defense of novelty**: Defending novelty without specific comparisons or evidence, merely stressing that the method is different, and failing to rebut the reviewer's doubt about insufficient innovation.

### Key strategy

Respond confidently and directly, support with grounding in the paper and specific evidence, and avoid vague commitments

---

## Cluster 5: Harsh Dismissive

**Profile**: These reviewers tend to evaluate the paper in a harsh, dismissive tone, with strong criticism but low constructiveness; they rarely offer actionable suggestions and are hard for authors to persuade. They focus on the paper's obvious defects (such as writing quality, misleading motivation, method limitations) but cite few specific details; the overall style is concise, direct, and negative.

| Metric | Value |
|--------|-------|
| Share of samples | 9.8% (98 reviews) |
| Historical score-increase rate | 13.8% |
| Acceptance rate | 27.6% |
| Successful rebuttal samples | 30 |

### Recognition signals

- Uses strongly negative words such as 'not well-written', 'misleading', 'limited'
- Criticism lacks constructiveness and gives no concrete direction for improvement
- Concise, direct tone, often listing problems in short sentences or lists

### Rule-statistic differences (Top 3)

- **New experiments / new results**: success 60.0% vs failure 34.3% (Δ +25.7)
- **Explicit commitment to revise**: success 43.3% vs failure 60.0% (Δ -16.7)
- **Clarifying explanation**: success 63.3% vs failure 77.1% (Δ -13.8)

### Strategy-vector effects (Cohen's d)

**Significantly higher in the success group (Cohen's d):**
- `direct_address`: success mean 4.5 / failure mean 2.691 (d=1.241)
- `tone_confidence`: success mean 4.4 / failure mean 2.603 (d=1.307)
- `clarification_quality`: success mean 4.333 / failure mean 2.588 (d=1.212)

**Higher in the failure group (risk dimensions):**
- `vague_future_work`: success mean 1.433 / failure mean 2.574 (d=-0.721)
- `overpromise_risk`: success mean 1.533 / failure mean 2.309 (d=-0.551)

### Success patterns (LLM-derived)

- **Confident, direct response**: Respond head-on to the reviewer's criticism in a confident, direct tone, not dodging the core issue, and showing a deep understanding of the work.
- **Backed by specific evidence**: Provide new experiments, quantitative results, or concrete data as evidence rather than relying only on explanations or promises, to increase persuasiveness.
- **Clear structured exposition**: Organize the response with clear structure (such as bullet points and headings) to improve readability, and give high-quality clarification for each criticism.
- **Controlled concession**: While acknowledging some shortcomings, immediately turn to stressing one's own contribution or improvements, avoiding wholesale self-rejection.

### Failure patterns (LLM-derived)

- **Vague future-work commitments**: Substituting vague commitments such as "will be addressed in future work" for present evidence, which cannot meet the reviewer's demand for immediate verification.
- **Over-promising risk**: Exaggerating the method's capabilities or promising unrealistic results, which triggers stronger distrust in the reviewer.
- **Over-conceding and self-negation**: Readily admitting criticism and substantially revising terminology or positioning, which weakens the sense of contribution and leads the reviewer to think the authors lack confidence.

### Key strategy

Respond confidently and directly, and replace vague commitments with specific evidence

---

## Cluster 1: Gentle Constructive

**Profile**: The core mindset of these reviewers is to support the authors in improving the paper rather than to pick at defects. Their writing is gentle and specific, often raising improvement points as questions or suggestions, with a focus on executability, low criticism severity, and ease of persuasion. They value the paper's contribution and baselines, but raise constructive questions about details.

| Metric | Value |
|--------|-------|
| Share of samples | 34.5% (345 reviews) |
| Historical score-increase rate | 13.4% |
| Acceptance rate | 50.4% |
| Successful rebuttal samples | 177 |

### Recognition signals

- Uses gentle question patterns such as 'It would be helpful if...' or 'Is this still true...'
- The review explicitly mentions 'Strengths' and 'Questions', with a clear structure and a positive opening
- Suggestions are specific and actionable, such as asking for a particular task or analysis to be added, rather than general criticism

### Rule-statistic differences (Top 3)

- **New experiments / new results**: success 56.5% vs failure 46.6% (Δ +9.9)
- **Clarifying explanation**: success 60.5% vs failure 68.6% (Δ -8.1)
- **Moderate acknowledgment**: success 54.2% vs failure 61.0% (Δ -6.8)

### Strategy-vector effects (Cohen's d)

**Significantly higher in the success group (Cohen's d):**
- `tone_confidence`: success mean 4.593 / failure mean 3.398 (d=1.036)
- `direct_address`: success mean 4.689 / failure mean 3.512 (d=0.985)
- `clarification_quality`: success mean 4.492 / failure mean 3.349 (d=0.963)

**Higher in the failure group (risk dimensions):**
- `overpromise_risk`: success mean 1.35 / failure mean 2.018 (d=-0.637)
- `vague_future_work`: success mean 1.542 / failure mean 2.157 (d=-0.51)

### Success patterns (LLM-derived)

- **Confident, direct response**: Respond head-on to each of the reviewer's specific questions in a confident, direct tone, avoiding vagueness, evasion, or excessive apology, which strengthens persuasiveness.
- **Backed by specific evidence**: Provide new experiments, quantitative results, data, or specific citations from the paper as evidence rather than empty promises, directly addressing the reviewer's core concern.
- **Controlled concession**: While acknowledging that the reviewer's view is reasonable or that the work has limitations, clearly explain one's own position, core contribution, or existing evidence, avoiding wholesale self-rejection.
- **High-quality clarification and structure**: Provide clear, structured explanations, organize the reply with headings, numbering, or paragraphs, and cite specific content from the paper (such as tables and sections) to improve readability and persuasiveness.

### Failure patterns (LLM-derived)

- **Over-promising risk**: Promising too much future work or improvements that cannot be verified immediately (such as 'will be addressed in future work') with no concrete action plan, leading the reviewer to doubt feasibility.
- **Vague future work**: Using vague future plans (such as 'will be explored') in place of a concrete response, failing to address the reviewer's core concern directly and weakening persuasiveness.
- **Unconfident justification**: Hesitant tone or excessive apology and a lack of directly targeted explanation, making the reviewer doubt the authors' confidence in the work, or producing a response that drifts from the reviewer's specific question.

### Key strategy

Respond confidently and directly, support with specific evidence, and avoid empty promises.

---

## Cluster 2: Concise Affirmative

**Profile**: These reviewers tend to give short, general positive evaluations and rarely provide specific details or actionable suggestions. Their mindset may be that the paper is already good enough and needs no in-depth criticism, or their own reviewing effort is limited, so they give only summary feedback.

| Metric | Value |
|--------|-------|
| Share of samples | 5.3% (53 reviews) |
| Historical score-increase rate | None% |
| Acceptance rate | 52.8% |
| Successful rebuttal samples | 27 |

### Recognition signals

- The review is very short, usually only a sentence or two
- Uses general positive words such as 'rigorous', 'strong', 'good', but lacks specific support
- Points out no specific problems or directions for improvement; extremely low constructiveness

### Rule-statistic differences (Top 3)

- **New experiments / new results**: success 48.1% vs failure 65.0% (Δ -16.9)
- **Clarifying explanation**: success 59.3% vs failure 75.0% (Δ -15.7)
- **Explicit commitment to revise**: success 74.1% vs failure 60.0% (Δ +14.1)

### Strategy-vector effects (Cohen's d)

**Significantly higher in the success group (Cohen's d):**
- `tone_confidence`: success mean 4.731 / failure mean 3.44 (d=1.136)
- `clarification_quality`: success mean 4.654 / failure mean 3.48 (d=1.043)
- `direct_address`: success mean 4.808 / failure mean 3.64 (d=1.008)

**Higher in the failure group (risk dimensions):**
- `overpromise_risk`: success mean 1.154 / failure mean 1.6 (d=-0.646)
- `vague_future_work`: success mean 1.423 / failure mean 1.64 (d=-0.24)

### Success patterns (LLM-derived)

- **Confident, direct response**: Respond directly to each of this reviewer's questions in a confident, assertive tone, avoiding vague or defensive language and stressing a clear understanding of the issue.
- **High-quality clarification**: Provide clear, well-grounded clarifications that draw on the paper's content or cited literature rather than relying only on new experiments, showing a deep understanding of the problem.
- **Controlled concession**: While acknowledging limitations, clearly show the improvements already made or concrete plans, avoiding hollow promises and holding firm on the core contribution.
- **Paper grounding**: Anchor the response tightly in the paper's text, citing specific sections, figures, tables, or revision locations to increase credibility and verifiability.
- **Structured response**: Organize the response with numbering or paragraphs so the reviewer can easily track the answer to each question, improving clarity and professionalism.

### Failure patterns (LLM-derived)

- **Over-promising risk**: Promising to open-source code or run many experiments in the future without providing concrete evidence in the rebuttal, so the reviewer finds it unreliable or distracting.
- **Vague future work**: Deferring key issues to future research (such as 'will be explored in future') rather than resolving them directly in the rebuttal, which looks like dodging the core doubt.
- **Providing many new experiments without targeting**: Although more new experiments are provided, they do not directly address the core doubt and instead look redundant or off-point, leading the reviewer to think the authors missed the key issue.
- **Defensive argument**: Arguing with the reviewer over terminology or definitions instead of solving the problem directly, leading the reviewer to think the authors are not open-minded or are dodging the substantive issue.

### Key strategy

Respond confidently and directly, give high-quality clarification, concede in a controlled way, and avoid over-promising

---
