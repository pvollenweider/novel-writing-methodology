# Eval results

With-skill vs without-skill comparisons, `claude-sonnet-5`, single run per configuration unless noted. Grading is assertion-based (see `evals.json`) — each response checked against explicit pass/fail expectations, with quoted evidence.

## Eval 1 — research-to-architecture

| | With skill | Without skill |
|---|---|---|
| Pass rate | 5/5 | 1/5 |

Largest gap of the four evals. Unassisted response stayed at theme/character-want level and never reached a reader-effect question, the research-bucket distinction, or the scene-necessity test.

## Eval 2 — scene-diagnosis-information-audit

| | With skill | Without skill |
|---|---|---|
| Pass rate | 4/4 | 3/4 |

Moderate gap.

## Eval 3 — reader-feedback triage / freeze discipline

Run in three different prompt shapes across iterations, because the first two versions gave the user's own threshold language back to Claude and it's unclear whether that was doing the discriminating work instead of the skill.

| Iteration | Prompt shape | With skill | Without skill |
|---|---|---|---|
| 1 — `freeze-and-reader-feedback-triage` | user states an explicit freeze rule and asks Claude to apply it | 5/5 | mixed (see `iteration-1/benchmark.json`) |
| 2 — `eval-freeze-threshold-discipline` | user states their own reopening threshold, asks whether two new signals clear it | 5/5 | 5/5 (no gap) |
| 3 — `unprompted-evidence-triage` (current, in `evals.json`) | user states no rule or threshold at all, just dumps five raw signals | 5/5 | 5/5 (no gap) |

No version discriminates. Claude's default judgment on triaging beta-reader feedback and freeze thresholds is already close to what the skill prescribes, with or without the user supplying their own rule first. Kept as eval 3 in `evals.json` as a documented, honest limitation, not a hidden failure — it says more about this particular eval than about the skill.

## Eval 4 — character-depth-vs-biography

| | With skill | Without skill |
|---|---|---|
| Pass rate | 5/5 | 3/5 |

Real gap. The without-skill response correctly avoided recommending more backstory and reframed toward present-tense wants, but never named self-deception / wrongly-held belief / concealment as more character-defining than biography, and never produced an explicit pressure/forced-choice test comparable to the skill's "write it, don't assert it" test — it substituted a want/cost sentence exercise instead.

## Takeaways

- The skill's marginal value is concentrated where Claude's unassisted judgment lacks a specific *named mechanism* to reach for (the research-bucket distinction in eval 1, self-deception/pressure-test in eval 4) — not in domains where default judgment already tracks good practice (eval 3).
- Raw materials (full transcripts, per-run `grading.json`, aggregated `benchmark.json`/`.md`, browsable `review.html`) are not committed to this repo — they're working artifacts, not part of the skill or its documentation.
