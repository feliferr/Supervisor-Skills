# Rebuttal Guidance Completeness Checklist

Check every item before telling the user the guidance is complete.

## Completeness check

| # | Check | Pass |
|---|-------|------|
| 1 | Every W/Q in the user's input has a corresponding guidance block | ☐ |
| 2 | Every concern has been tagged with a type | ☐ |
| 3 | The matched mindset cluster and its confidence are stated | ☐ |
| 4 | Every concern has a recommended strategy dimension | ☐ |
| 5 | No fabricated experimental numbers (data not verified against the paper is marked [TO VERIFY]) | ☐ |
| 6 | Clarification-type and new-experiment-type concerns are clearly distinguished | ☐ |
| 7 | Defensive phrasing is flagged in the tone notes | ☐ |
| 8 | Overpromise risk is flagged on items where overpromise_risk is high | ☐ |

## Tone red lines (must be flagged in the guidance)

- "You misunderstood / You missed / This is trivial": aggressive, must be rewritten
- "Significantly / clearly / undoubtedly": empty words when no numbers back them up
- "We will fully address in future work": an avoidance signal when there is no action taken now
- Excessive apology ("We sincerely apologize for..."): weakens the argument

## Special note for low-openness reviewers

If the matched mindset has a **historical score-increase rate < 15%** (see mindset-library.md):

- Tell the user: text alone has limited persuasive power, so prioritize providing one decisive new experiment.
- Suggest a realistic goal: clarify the most central misunderstanding + provide one minimal, credible piece of new evidence.
- Do not encourage the user to write an overly long rebuttal: concise and forceful beats exhaustive.

## Common mistakes

| Error pattern | Symptom | Fix |
|---------------|---------|-----|
| Over-long clarification | Five paragraphs of explanation for an evidence_gap with no new data | Compress to 2 sentences and point to the new results |
| Blanket concession | Conceding too much on a scope_claim | After conceding, immediately argue that "the contribution holds within the narrowed scope" |
| Dodging novelty | Answering "contribution is not novel enough" with "our method is more practical" | State the concrete technical differences from the most closely related work |
| Neglecting Questions | Treating a Q like a W and answering with a long proof | A Q usually needs only 2–3 sentences + a pointer |
