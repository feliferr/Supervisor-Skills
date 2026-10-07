# Concern Classification

Before choosing a response strategy, classify each Weakness / Question.

## Classification table

| Type | Recognition signals (reviewer's own words) | Priority strategy dimensions | Recommended template |
|------|-------------------------------------------|------------------------------|---------------------|
| **misunderstanding** | "seems", "unclear whether", clearly contradicts the main text | clarification_quality + paper_grounding | Template A |
| **evidence_gap** | "more experiments", "ablation", "only one dataset" | new_experiment_strength + specific_evidence | Template B |
| **novelty** | "incremental", "similar to X", "limited contribution" | specific_evidence + differentiated wording; controlled_concession when needed | A or C |
| **baseline_fairness** | "unfair comparison", "weak baseline", "missing SOTA" | add comparison experiments + explain the experimental protocol | Template B |
| **scope_claim** | "overclaim", "overstated", "not supported by evidence" | controlled_concession to narrow the claim | Template C |
| **writing_clarity** | "hard to follow", "notation", "organization" | reword + example + pointer into the main text | Template A |
| **theory** | "proof", "assumption", "bound", "convergence" | pointer to the formula/proof, or acknowledge the limitation | A or C |
| **efficiency** | "complexity", "scalability", "overhead" | complexity analysis + measured latency | Template B |
| **other** | no obvious match to the above | restate first, then reclassify | depends on content |

## How Weaknesses and Questions are handled differently

| | Weakness | Question |
|--|----------|----------|
| Reviewer mindset | "There is a flaw here" | "I didn't understand / please confirm" |
| Response focus | Evidence + revise where necessary | Short answer + Section/Table pointer |
| Common mistake | Explaining without acting | Excessive apology |

## Quick keyword classification

```
novelty:     novel, contribution, incremental, original, marginal
experiments: experiment, baseline, ablation, dataset, evaluation
writing:     clarity, unclear, confusing, notation, presentation
theory:      proof, theorem, assumption, bound, convergence
efficiency:  scalable, complexity, computation, overhead, efficient
scope:       limitation, generalize, broader, overclaim, overstated
```

## Handling compound concerns

If a single W contains both novelty + evidence_gap, split it into two sub-concerns and give a strategy for each.
Address first the one the **reviewer cares about most** (usually the one in the first paragraph).
