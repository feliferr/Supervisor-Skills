# Reviewer Mindset Matching Heuristics

Score the review text item by item (1 = low, 5 = high), then match against the mindset cluster profiles.

## Behavior signal scoring table

| Signal | High (5): typical phrasing | Low (1): typical phrasing |
|--------|---------------------------|---------------------------|
| **Openness** | "willing to raise", "if addressed", "open to" | "reject", "not convincing", "final decision" |
| **Severity** | "fundamental flaw", "fatal issue", "strong reject" | "minor concern", "small issue" |
| **Constructiveness** | "I suggest", "would strengthen if", "recommend adding" | Purely negative, no path to improvement |
| **Specificity** | Cites Table 2, Sec 3, equation numbers | "overall not convincing", no specific pointers |
| **Skepticism** | "not convinced", "insufficient evidence", "doubtful" | Neutral wording, no doubt expressed |
| **Harshness** | "reject", "misleading", "wrong", "unacceptable" | Polite and euphemistic |
| **Actionability** | "add experiment", "compare to X", "ablation needed" | No actionable suggestions |

## Quick reference for the six mindsets (current data-driven 6-cluster version)

| Mindset | Typical signal combination | Score-increase rate (reference) | Core response strategy |
|---------|---------------------------|--------------------------------|------------------------|
| **Precise constructive** | High constructiveness + high specificity + high actionability | ~36% | Respond point by point in a structured way, citing specific locations in the paper |
| **Mild skeptic** | Low severity + low actionability, vague wording | ~19% | Remove the confusion directly; be confident without over-explaining |
| **Experiment-oriented** | Strong evidence_gap doubts, repeated requests for comparisons | See mindset-library | Add experiments, or explain why the existing results suffice |
| **Highly skeptical and severe** | High skepticism + high severity + low scores | ~7-15% | Hard evidence first, narrow the claims, accept limitations |
| **Hard-line, many objections** | High harshness + many concerns + long review | ~12% | New experiments + direct citations to the paper + explicit commitments |
| **Other** | No obvious match | - | Identify the single most prominent signal first |

For detailed statistics (score-increase rates, Cohen's d effects) see [mindset-library.md](mindset-library.md).

## Matching procedure

1. Score 5–7 signals and record the specific phrases in the original text that triggered each score.
2. Compare the signal combination against the table above and pick the closest mindset.
3. If two mindsets are close, mark **primary + secondary**.
4. Confidence: 3 or more aligned signals → **high**; a review that is too short or generic → **low**.

## How confidence affects the output

| Confidence | Action |
|------------|--------|
| High | Use that mindset's success_patterns directly to guide the strategy |
| Medium | List primary + secondary and explain how the strategies differ |
| Low | Rely mainly on general strategy and state that the mindset judgment is uncertain |
