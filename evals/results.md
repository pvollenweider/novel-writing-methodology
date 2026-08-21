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

## Constitution red-team campaign — testing whether the invariants themselves earn their status

Eval 9's result (and the Phase 10 revision it prompted) raised a sharper question than "does the skill apply its rules correctly": does each Constitution item still produce the best judgment in the case constructed specifically to make it expensive? A review proposed a disciplined process for this, followed here: **construct the adversarial case first, get an independent judgment with no reference to the skill at all, and only then compare that judgment to what the invariant prescribes.** Writing the expected answer from the rule first would make every red-team a compliance eval in disguise. One invariant at a time, in priority order (4, then 8, 2, 7, 3), each free to change the Constitution before the next is designed.

### Item 4 — "Criteria before test" (first, since eval 11 showed pre-registration discipline is where the skill's real value concentrates)

**The case:** a novelist pre-registers a single test question (does a reconciliation scene feel earned or too-sudden) before showing it to four readers. All four, unprompted and independently, report something else entirely — they read the brother as lying, when the manuscript establishes elsewhere that he's sincere. None engage the pre-registered question at all.

**Independent judgment** (no mention of this skill, reasoned from first principles): the lying-finding is legitimate, high-value data — independent four-way convergence contradicting an established fact is about as clean as reader signal gets, and it's *upstream* of the original question (readers can't judge an earned reconciliation they don't believe is sincere). The pre-registration rule doesn't suppress it, because that rule exists to stop an author from rationalizing an unfavorable answer to their actual question by cherry-picking a flattering alternative — not to blind them to unsolicited, non-flattering, convergent signal about a different problem. Verdict: log the finding on its own evidentiary merits (independence, convergence, specificity, checkability against text); mark the original question **indeterminate**, not failed; retest both, separately, with fresh pre-registered criteria.

**Current skill, same case:** converged on the identical structure independently — reading effect (lying) separated explicitly from any theory of cause; the earned/sudden question marked indeterminate rather than failed, since "a reader busy deciding whether a character is lying is not in a position to also judge whether his reconciliation is earned"; investigate and locate the source of the sincerity misreading first, with its own narrow pre-registered criterion, before rerunning the original test with fresh readers; explicitly warned against papering over it with reassuring narration, since that would reintroduce the over-explanation problem before the actual cause is even known.

**Verdict: item 4 survives, but with a scope clarification, not unchanged.** That distinction matters and is worth keeping separate from a clean pass: no divergence between independent judgment and the skill's actual behavior — Phase 8/9's evidence doctrine and "effect vs. cause" distinction already produce the right answer in practice, so this isn't a rule rescued by adding an exception after the fact. What *was* genuinely underspecified was the Constitution's one-line summary of item 4, which — read in isolation, without the fuller phase text — could plausibly be misapplied as "nothing outside the pre-registered criteria counts." Reworded (not rewritten) to make the distinction self-contained: pre-registration disciplines the *interpretation* of the question asked; it does not gate what counts as valid data. Logged as eval 12. (Caught in review: an earlier draft of this eval's expected answer said "fix the sincerity misread" — itself a small violation of item 3, observation before diagnosis, since locating a cause has to precede prescribing a fix. Corrected to "investigate and resolve.")

**Red-team verdict taxonomy, adopted going forward:** *survives unchanged* (no divergence, no wording issue), *survives but scope clarification needed* (item 4's result — the principle was already right, the one-line summary wasn't self-contained), or *fails / substantive revision needed* (item 5's result before the Phase 10 revision). Recording which of the three applies is itself part of what the red-team is supposed to produce — "survives" alone discards the information a clarification-only outcome still carries.

### Item 8 — "Generation and selection are different operations"

**The case:** a novelist generates the idea that A and B first meet at the funeral of B's father, then discovers mid-development that it hard-contradicts an already-written, keep-worthy scene (the father is alive in chapter 17). Developing the idea that far already revealed something real: what she actually wanted was B receiving unwanted sympathy while emotionally checked-out — a configuration independent of anyone dying.

**Independent judgment:** the generation/judgment distinction, as usually stated, conflates two different operations. *Feasibility-checking* (does this contradict established fact?) is closer to a continuity check than an aesthetic judgment, costs nothing, and should happen immediately — there's nothing generative left to gain from elaborating an impossible premise. *Value-judgment* (is this good, relative to alternatives?) is the part that genuinely benefits from deferral. The mistake is letting a hit on the first stand in for a verdict on the second. Concretely: disqualify the funeral instantly, but before discarding the idea, separate its disposable "packaging" (the specific scenario) from its portable "engine" (the underlying emotional configuration), write the engine down as a form-independent design target, and treat it as a fresh, still-open generation target.

**Current skill, same case:** converged independently on the identical two-part structure — clean, immediate discard of the funeral "for a plain textual reason," explicitly distinguished from the idea having "failed" ("generating it without asking it to justify itself first... let it run far enough to produce consequences, and it did"); separated "surface idea" (dead) from "emotional configuration" (alive) using almost the same vocabulary as the independent judgment's packaging/engine split; proposed a fresh generation pass for alternative forms of the same configuration rather than canonizing the first replacement.

**Verdict: item 8 survives, scope clarification needed** — same shape as item 4. No behavioral divergence: the skill (via the exploration protocol's existing "work out consequences" step and general reasoning) already handled the hard-contradiction case correctly in practice. What was underspecified was the Constitution's one-line summary ("don't require each option to justify its existence... apply criteria only afterward, during selection"), which read in isolation doesn't distinguish a *fact* check from a *preference* judgment, and doesn't name the yield-extraction step at all — a genuine addition, not just a wording fix. Reworded item 8 to state the distinction directly (hard contradictions disqualify immediately; only preference-based criteria wait for selection) and added the extraction step — disqualified ≠ worthless, separate the candidate from what it revealed — to both the Constitution and the exploration protocol (new step 2), plus a disqualified/rejected-by-preference distinction in the exploration-candidates-log register. Logged as eval 13.

### Item 2 — "Narrative experience before demonstration" (first real fall since the pre-revision item 5)

**The case:** a novelist writing an essayistic, philosophical novel whose entire pull is watching the narrator's own argument develop and partially dismantle itself — no subplot, no external mystery, no relationship arc. A beta reader suggested bolting on a secondary plot thread "so readers have a reason to keep reading that isn't just the argument." The novelist suspects that would make the book worse.

**Independent judgment:** built three concrete literary test cases rather than arguing in the abstract — Nicholson Baker's *The Mezzanine* (an entire novel of escalating, loving attention to trivia, no external stakes at all), David Markson's *Wittgenstein's Mistress* (a possibly-last-person-alive narrator, pull comes from watching her pattern of error and self-correction shift), and the "Part About the Crimes" section of Bolaño's *2666* (hundreds of pages of forensic catalog, deliberately withholding conventional mystery resolution). In each case, adding a conventional second engine wouldn't just fail to help — it would directly refute the book's own thesis, because each book's argument is partly *about* not needing that kind of rescue (ordinary attention doesn't need drama to justify its length; an isolated consciousness doesn't need a solvable mystery to be worth inhabiting; structural violence doesn't need a redemptive investigator to be worth documenting). Conclusion: "independent" was the wrong axis. What actually distinguishes a demonstration that works from one that "argues at the reader" is whether the argument itself has the structural properties a plot ordinarily supplies — irreversibility (each step forecloses the last, doesn't just restate it), escalation (cost/scope/stakes increase, not just accumulate), a consciousness with something real to lose in how it resolves, and concrete particularity (enacted through specifics, not paraphrasable as a thesis). A demonstration passing all four needs no second engine and actively suffers from being given one.

**Current skill, same case (before this revision):** more sophisticated than a naive "yes, add a subplot," but still fell into the trap. It reframed the diagnostic question usefully (is the narrator's reasoning staged as drama, with something at stake, rather than delivered as content) and correctly told the author not to add a subplot — but it did so by insisting a "consciousness under real personal stakes" is required to satisfy "the independent-engine requirement," i.e. it kept the word *independent* and kept a mandatory-stakes condition. That framing would misdiagnose *The Mezzanine* as failing — its narrator has no personal risk, loss, or stake in the conventional sense; the escalating extremity of attention itself is what's doing the work. The skill's answer captured only one of the independent judgment's four structural properties (stakes) and treated it as the necessary and sufficient condition, rather than one of several ways a demonstration can move like a plot.

**Verdict: item 2 fails — substantive revision, not a wording fix.** Unlike items 4 and 8, this is the first round since the pre-revision item 5 (freeze) where the skill's actual behavior, not just its one-line summary, produced a worse answer than the case demanded — a real, if less severe, instance of the same failure shape: a constitutional rule doing work its own justification doesn't support.

**Three passes, each caught by checking the revision against the campaign's own test cases.**

*Pass one* dropped "independent engine" but replaced it with a four-property checklist ("a demonstration passing all four is functioning as real causality") — which immediately reintroduced a version of the same mistake: eval 14's own assertions already required that no single property (specifically, personal stakes) be treated as a hard universal, since *The Mezzanine* clears the bar with none of them in the conventional sense. A rule requiring all four contradicted the eval written to test it.

*Pass two* fixed that (the dimensions became diagnostic, not a checklist — a demonstration could pass on the strength of any one), but replaced the checklist with a single universal test: does the reader's experience *develop* (order-dependent) rather than merely *accumulate*, verified by permuting the major units. This is exactly right for a **sequential** demonstration and exactly wrong for a **cumulative** one — the campaign's own third test case, Bolaño's "Part About the Crimes," derives its force from saturation and repetition, not from precise sequencing; a large fraction of its individual murder descriptions could likely be permuted without collapsing the architecture, which the pass-two test would misread as "static" when the accumulation itself is doing real, load-bearing work. A universal permutation test contradicted the third of the campaign's own three test cases.

*Pass three* (current): named three distinct shapes a demonstration's development can take — **sequential** (order load-bearing: A must precede B, which changes what C means), **cumulative** (saturation/repetition load-bearing, precise order much less so: the fiftieth instance does something the fifth didn't because forty-five have piled up, not because of where it's sequenced), and **formal/perceptual** (what develops is the reader's recognition of a pattern, even while the specific instances filling it stay largely interchangeable) — and matched the destructive test to the shape rather than applying one test to all three: permute units for sequential, remove a substantial fraction for cumulative, break/reorder the pattern itself for formal. The dimensions list (irreversibility, escalation, cumulative pressure/saturation, transformed consciousness/reader-frame, formal development, concrete particularity) stays diagnostic and non-required, now explicitly not privileging any one shape. Underlying general test, unifying all three: could the experience of the material be replaced by a concise statement of its conclusion without meaningful loss? If yes, lecture; if no, literature, regardless of which shape carried it. Both `SKILL.md` and Phase 7's tension audit updated accordingly.

Three failed formulations in sequence, each one falling to a case the campaign had already generated to test the previous one — worth keeping as the record, since it's a working demonstration of exactly the "observation before diagnosis" / iterative-correction discipline the skill itself prescribes, not just a description of the final rule.

**Campaign running total:** item 4 — survives unchanged in substance (wording clarified); item 8 — survives unchanged in substance (wording clarified, one genuine protocol addition); item 2 — fails, substantively revised, and the first revision itself needed a second pass caught by checking it against its own eval. Next: item 7 (factual truth's "non-negotiable," against a deliberate authorial counterfactual — a historical figure moved in time, a composited event, a knowingly altered geography, signaled as fictional device rather than narrator error, character belief, or lie).

## Takeaways

- The skill's marginal value is concentrated where Claude's unassisted judgment lacks a specific *named mechanism* to reach for (the research-bucket distinction in eval 1, self-deception/pressure-test in eval 4, scope-delimitation/candidate-rejection/closure in eval 5, convergence-before-action in eval 8, "better ≠ defect" in eval 9) — not in domains where default judgment already tracks good practice (eval 3, and anti-evals 7 and 10).
- A methodology skill's restraint is not free: applying it correctly can still leak the methodology's own vocabulary into a response where plain reasoning would have done the same job less visibly (eval 6). Worth checking for on any future eval, not just whether the verdict was right.
- Raw materials (full transcripts, per-run `grading.json`, aggregated `benchmark.json`/`.md`, browsable `review.html`) are not committed to this repo — they're working artifacts, not part of the skill or its documentation.
