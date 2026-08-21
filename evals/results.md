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

## Eval 5 — post-freeze-correction-discipline

| | With skill | Without skill |
|---|---|---|
| Pass rate | 5/5 | 2/5 |

Real gap, same shape as evals 1 and 4. Unlike eval 3, the reopening decision itself was not in question here (convergent, precisely localized, self-confirmed) — this tests the *execution* discipline once a fix is already justified. The without-skill response had good instincts (it independently warned against overcorrection and favored a minimal fix) but had no named discipline for containing scope, systematically testing and rejecting intervention locations in favor of one that extends an existing gesture, or closing the correction explicitly rather than inviting further open-ended engagement — it drifted toward planting new material earlier in the book rather than searching the text for something already there to extend. The with-skill response ran the full six-step procès protocol: object delimited in writing, three candidate locations tested and rejected with stated reasons, symmetric before-the-fact criteria, word-cost accounting, and explicit closure — including naming "no change" as a legitimate outcome if no candidate passes.

## Anti-evals 6-10 — does the skill know when not to engage?

Tests the complementary failure mode: not whether the skill applies its method correctly, but whether a methodology-heavy skill knows when to stay out of the way. Unlike evals 1-5, "without skill" is not the baseline being improved on here — it's a second thing under test, since a skill that *introduces* over-engagement where unassisted judgment already showed restraint is a regression, not a win.

| Eval | Scenario | With skill | Without skill | Verdict |
|---|---|---|---|---|
| 6 | Raw one-sitting fragment, "what could this become?" | 4/5 | 5/5 | Baseline already generative and appropriately non-diagnostic. With-skill response was substantively correct (explicitly declined to audit, generated five genuinely divergent, unranked directions per the exploration protocol) but lost a point on tone — it narrated its own scaffolding to the user ("that's Phase 7 work," "per the constitution") rather than just reasoning naturally, which is its own version of the reader sensing the machine. |
| 7 | Contemplative scene passing the old causal-only necessity test | 5/5 | 5/5 | No gap — baseline already reasoned past "nothing becomes impossible" to what the scene does for the reader, unprompted. |
| 8 | Vague, unlocalized "something felt off" reader signal | 5/5 | 3/5 | Real gap. Baseline didn't discard the signal, but launched the author into an immediate self-directed hunt (a checklist of likely causes: tonal whiplash, POV drift, pacing, etc.) rather than logging it as a real-but-unlocalized signal and holding for convergence. With-skill response held the line explicitly: log verbatim, ask experience-only follow-ups, get a second blind reader, and only act on convergence — naming both failure modes (discarding the signal, and manufacturing a cause) as the thing being avoided. |
| 9 | Post-freeze "better idea," nothing broken, no external signal | 5/5 | **0/5** | Largest gap of any eval so far. Baseline said outright "yes, go ahead and make the change" and framed "I had a better idea" as "one of the few completely legitimate reasons to reopen finished work" — exactly the failure mode this anti-eval targets. With-skill response held the freeze correctly: named the two reopening paths (at the time — see the Phase 10 revision below), explained why "it's better" doesn't retroactively manufacture a defect, and offered legitimate alternatives instead of either caving or offering a disguised workaround. |
| 10 | Factual "error" that's a character's deliberate, signaled mistake | 5/5 | 5/5 | No gap — baseline already correctly attributed the claim to the character before evaluating it, without needing an explicit narrator/character framework to get there. |

Net: 24/25 with skill vs. 18/25 without, but the aggregate hides the shape — the skill's restraint value is concentrated almost entirely in evals 8 and 9 (unlocalized signals and post-freeze discipline), it's neutral where baseline judgment is already sound (7, 10), and it introduced one new, minor failure mode of its own (jargon leakage into user-facing text, eval 6). Fixed directly in `SKILL.md` ("How to use this skill," item 6: apply the reasoning, don't narrate the scaffolding) rather than left as a known issue.

## A hidden assumption in eval 9, and the Phase 10 revision it prompted

A review of this iteration pushed back correctly on how eval 9's result was being read. 0/5 vs. 5/5 shows the skill applies its own policy far more consistently than unassisted judgment — it does not, on its own, show the policy is right. Eval 9's original framing (absolute: reopening requires a defect, full stop) risked exactly what the skill's own "one rule above the others" warns against — governance outranking the book it protects. The red-team question that exposes this: construct the case where a non-defect improvement has actually earned reopening (stated gain, real risk-check, genuine blind test against the frozen version, a real non-split result) — does the skill still say no? If it does, the constitutional rule is too strong.

This led to a real change, not just a eval fix: **Phase 10 now has a third reopening path**, (c) exceptional revision — deliberately expensive (a falsifiable claimed gain and a named risk list, both fixed before drafting; a full-finish candidate; a blind comparative test against the frozen version; a winning threshold fixed before results are seen; execution through the ordinary procès discipline if it wins) but real. Constitution item 5 was reworded from "no correction without an identified defect" to "no change without a stated reason and a testable expected gain," with the post-freeze bar tightening sharply rather than becoming absolute. Two other rules flagged in the same review were loosened the same way: the exploration protocol's claim that heavy foreclosure is inherently weak (wrong — foreclosure is often the source of dramatic power; what's weak is foreclosure that buys nothing) and Phase 2's "narrative promises must be paid" (too Chekhov's-gun-absolute; a promise can legitimately be paid, displaced, subverted, or deliberately frustrated, as long as its fate is a decision, not an oversight).

**Eval 9 was rerun against the revised skill** (with-skill only; the without-skill failure mode is unchanged) and still scores 5/5 against updated assertions that now also check the response doesn't overclaim the freeze as absolutely closed to improvement — it correctly named path (c) as available in principle while still declining the change as actually described (no stated gain, no test, no threshold — none of path (c)'s bar had been cleared).

## Eval 11 — redteam-frozen-improvement-earns-reopening (methodology challenge, not compliance)

The concrete red-team case: frozen manuscript, a new ending with no defect behind the old one, three named promises resolved more cleanly, a real blind A/B test (unlabeled, randomized, naive readers), 4-of-5 convergent preference citing the specific claimed gain, zero reported damage. Unlike evals 1-10, this eval is not scored as with-skill-should-beat-without-skill — it exists to check whether the skill (now with path (c)) can say **yes** when a case has actually earned it, not just **no** by default.

| | With skill | Without skill |
|---|---|---|
| Pass rate | 5/5 | 5/5 |

No assertion gap — both responses correctly recognized this as a case that had (largely) earned reopening rather than refusing on principle, checked the rigor of the test rather than rubber-stamping it, and avoided claiming the frozen version was thereby proven wrong. Baseline's unassisted reasoning here was genuinely good, on par with evals 3, 7, and 10.

The qualitative difference the assertions don't fully capture: the with-skill response caught something baseline missed entirely — it explicitly interrogated whether the claimed gain, the risk list, and the winning threshold had been fixed *before* the author saw the results, or reconstructed afterward to fit them, and treated that sequencing as the actual load-bearing discipline (a threshold set after seeing "4 of 5 liked it" is not a real threshold, even if the number would have cleared a reasonable one). Baseline accepted the evidence at face value. This is the same distinction the exceptional-revision protocol is built around — worth watching for in a future eval built specifically to test for it, since the current assertions passed both responses without forcing that distinction to matter.

## Takeaways

- The skill's marginal value is concentrated where Claude's unassisted judgment lacks a specific *named mechanism* to reach for (the research-bucket distinction in eval 1, self-deception/pressure-test in eval 4, scope-delimitation/candidate-rejection/closure in eval 5, convergence-before-action in eval 8, "better ≠ defect" in eval 9) — not in domains where default judgment already tracks good practice (eval 3, and anti-evals 7 and 10).
- A methodology skill's restraint is not free: applying it correctly can still leak the methodology's own vocabulary into a response where plain reasoning would have done the same job less visibly (eval 6). Worth checking for on any future eval, not just whether the verdict was right.
- Raw materials (full transcripts, per-run `grading.json`, aggregated `benchmark.json`/`.md`, browsable `review.html`) are not committed to this repo — they're working artifacts, not part of the skill or its documentation.
