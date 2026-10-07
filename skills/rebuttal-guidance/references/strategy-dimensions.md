# Rebuttal Strategy Dimensions (Y Vector)

Ten strategy dimensions distilled from historical successful and failed rebuttal data, scored 1–5.
**overpromise_risk** and **vague_future_work** are risk items (the higher the score, the more dangerous).

## The ten dimensions at a glance

| Dimension | Meaning | Writing points |
|-----------|---------|----------------|
| **direct_address** | Hits the core of the concern directly, without detours | Give each W/Q its own heading; do not merge them |
| **specific_evidence** | Uses numbers, figures, and comparison results | No "significantly improve" without supporting numbers |
| **new_experiment_strength** | New experiments precisely answer the doubt | Explain how the new experiment relates to the main conclusion |
| **clarification_quality** | Misunderstandings are clarified clearly, pointing to the original text | 2–4 sentences + Section/Table pointer |
| **controlled_concession** | Acknowledges reasonable limitations without over-conceding | After conceding, immediately give the corresponding improvement or narrowed scope |
| **structure_quality** | Clear W/Q structure that is easy for the reviewer to map | Subheadings, numbered lists |
| **tone_confidence** | Confident, respectful, not defensive | Avoid defensive phrasing such as "you misunderstood" |
| **paper_grounding** | Claims anchored to specific locations in the main text/appendix | Do not introduce new claims the main text does not mention |
| **overpromise_risk** ↓ | Commitments are deliverable, with no over-promising | Avoid unrealistic phrasing such as "fully solve" |
| **vague_future_work** ↓ | Answer what can be answered; push little to future work | Pushing to future work = an avoidance signal |

## Dimension priorities conditioned on mindset

After a mindset is matched, read the corresponding cluster in `mindset-library.md`:

1. **rule_diff Top 3**: the 3 dimensions with the largest difference between the success group and the failure group (positive value = higher in success).
2. **Cohen's d effects**: d > 0.8 means the dimension strongly discriminates for that mindset.
3. **success_patterns / failure_patterns**: concrete strategy descriptions distilled by an LLM.

Principle: strengthen dimensions with a positive difference; be cautious with dimensions with a negative difference (when the failure group scores higher, it may signal over-compensation).

## Effective strategy combinations (interaction terms)

Data analysis found that the following dimension combinations have synergistic effects, with higher success rates when both score high:

- `direct_address` + `specific_evidence`: direct response + concrete evidence, the core combination
- `specific_evidence` + `paper_grounding`: data anchored to the paper, the highest credibility
- `new_experiment_strength` + `specific_evidence`: new experiments must come with concrete numbers
- `tone_confidence` + low `overpromise_risk`: confident but not exaggerated

## Strategy annotation format for each concern

```
R1.W2 → Prioritize: specific_evidence, paper_grounding, clarification_quality
         Avoid: high overpromise_risk, vague_future_work
```
