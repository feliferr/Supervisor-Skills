# Response Templates

Three base templates, matched to different concern types. **This skill outputs a guidance plan, not final rebuttal text.**

---

## Suggested global structure

```
[Optional: 2-3 sentence opening: thanks + summary of revisions]

**R1.W1** [Title]
...

**R1.W2** [Title]
...

**R1.Q1** [Title]
...
```

---

## Template A: Clarify a misunderstanding (misunderstanding / writing_clarity)

```
**R?.W?** [Restate the reviewer's concern in one sentence]

Thank you for the comment. It may stem from [specific misreading].

**Clarification.** [2–4 sentences, pointing to Sec. X / Table Y / Appendix Z.]

**Evidence.** [One concrete fact or number from the paper.]

[If revised] An explanation has been added in Sec. X (revisions marked in blue).
```

**Suited mindset**: highly constructive reviewers respond well to clear clarifications.
**Avoid**: long explanations of more than 4 sentences; no pointer to a specific location in the paper.

---

## Template B: Add evidence (evidence_gap / baseline_fairness / efficiency)

```
**R?.W?** [Restate the concern]

We agree that [specific missing piece] would further strengthen the paper.

**New results.** We added [experiment/analysis]:
- [Metric] on [dataset]: our method X vs. baseline Y
- See Table N / Appendix M

**Conclusion.** [One sentence on how this addresses the concern.]
```

**Suited mindset**: experiment-oriented and hard-line, many-objection reviewers respond most positively to new experiments (significant Cohen's d).
**Avoid**: promising experiments that cannot be completed during the rebuttal period; numbers that do not come from actual results.

---

## Template C: Acknowledge the limitation, narrow the scope (scope_claim / novelty / theory)

```
**R?.W?** [Restate the concern]

We acknowledge [specific limitation]. The contribution of this paper is limited to [narrowed scope].

**The contribution still holds.** [1–2 sentences on why the contribution is valid within the narrowed scope.]

**Improvements.** [Revisions/additional analyses already made or to be made.]
```

**Suited mindset**: for highly skeptical, severe reviewers facing a scope_claim, narrowing the claim is more effective than defending it.
**Avoid**: conceding without giving an argument that the work "is still valuable within the limited scope".

---

## Guidance block format output by this skill

The agent outputs not final text but a guidance plan for each concern:

```
### R1.W2: [Short concern title]
- **Concern type**: evidence_gap
- **Recommended template**: B
- **Acknowledgement point**: Agree that ImageNet evaluation would strengthen the paper
- **Response angle**: Add high-resolution results (do not fabricate numbers)
- **Citable evidence**: Table 2 CIFAR results in the paper; new table (to be added)
- **Tone note**: Neutral, confident; avoid defensive phrasing
- **Avoid**: Long clarification paragraphs without new numbers
```
