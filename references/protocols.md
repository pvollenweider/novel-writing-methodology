# Protocols — concrete step-by-step procedures

Each protocol below is a specific, repeatable procedure referenced from `phases.md`. Use the phase file to know *when* to apply one of these; use this file to know exactly *how*.

---

## The procès protocol (post-freeze correction)

The most load-bearing protocol in this skill — it is what makes Phase 9 (freeze) survivable rather than either a dead letter (everyone quietly keeps editing) or a straitjacket (real defects go uncorrected because nothing can ever change). Run it in full for every reopening under Phase 9's path (b) (external signal, localized or convergent). Do not run a partial version and call it a procès.

**Step 1 — Delimit the object, in writing, before anything else.** One point. Not "let's look at the shut-door material generally" — "these three specific occurrences of this term, and only whether they give the reader enough content to evaluate the inference built on them." Any adjacent question that surfaces during the procès gets explicitly set aside, named, and left for a separate procès later if it turns out to matter — never folded into the current one mid-stream.

**Step 2 — Find the least visible point of intervention.** Test multiple candidate locations and eliminate each with its own specific reason — never take the first plausible spot. The strongest candidate is usually one that **extends a gesture, habit, or device the text already uses**, rather than introducing a new one. (Example reasoning pattern: "this location requires no inference from the reader, so it doesn't need the fix" / "this location is the argument's own pivot — inserting an explanation here would interrupt the exact moment it needs to work" / "this location is where a character already, established elsewhere, delivers this kind of information to another character — it extends a practiced gesture rather than adding a new device.") Write down the candidates rejected and why, not just the one chosen.

**Step 3 — Fix verification criteria before executing, and make them symmetric.** Almost always two questions, checked in both directions:
- Does the reader now have what they need? (the defect being corrected)
- Does the fix over-correct — does the text start explaining what to *think*, not just what to *know*? (the symmetric failure mode)

Write both criteria down before touching the text.

**Step 4 — Execute at the necessary minimum, counting the cost.** Count words added. Justify the count. This word-by-word economy discipline belongs *here* — post-freeze, single-object correction — not in first-draft writing (see the Phase 5 warning in `phases.md`; do not let this discipline leak backward into drafting). If eight instances of a problem are found but the object was delimited to two, fix two and log the other six as out of scope for this procès, not silently expanded into.

**Step 5 — Verify the local seam.** Re-read the entire unit affected (the scene, the chapter) after the change, not just the edited sentence. Confirm nothing else needed to change as a side effect. If something else did need to change, that's a sign the object in Step 1 was delimited too narrowly — note it, and decide explicitly whether to widen this procès or close it and open a new one.

**Step 6 — Close without reopening further.** State the closure explicitly: what was fixed, what was deliberately left alone and why, and — importantly — that this procès does not, on its own, license a broader review pass. If new evidence later reopens the topic, that's a new procès, referencing this one, not an amendment to it.

**A valid outcome of a procès is rejection.** A correction drafted and tested against Step 3's criteria can fail those criteria — in which case it is discarded and the procès closes with "no change made," which is exactly as legitimate an outcome as a successful edit. Never rescue a rejected fix by loosening the criteria after seeing it fail; that is the identical mistake to the pilot-rescue trap in Phase 4, applied post-freeze where the stakes of getting it wrong are higher.

**Correcting your own procès note.** If a procès's own reasoning turns out to be flawed (overclaimed precision, too-generous categorization) after the fact, correct it with a visible strikethrough and a note of correction — never a silent rewrite. The trace of the original reasoning error has archival and methodological value in its own right.

---

## The crash-test protocol

Used to test a hypothesis of the shape "this is too long / too short / could be cut / needs more" — anywhere quantitative intuition needs to be checked against an actual test rather than trusted directly.

1. State the hypothesis precisely and as a claim that could fail: "chapter 8 could lose 150 words without losing anything the story needs" — not "chapter 8 feels long."
2. Perform the cut (or the addition) as an actual edit, not a thought experiment.
3. Test the result against the Phase 2 architecture (does the causal chain still hold?) and, ideally, against a reader or a fresh read.
4. Record the actual delta and the verdict, including a **negative result** — a test that finds nothing to cut is real information ("the hypothesis that brevity was a defect did not survive a test designed to find one"), not a failed test.
5. Never treat a crash-test result as proof of the opposite absolute ("this proves the text is the correct length") — a passed test only means one specific hypothesis about a specific defect didn't hold up under one specific attempt to confirm it.

**A note on the origin of quantitative targets:** if a target (word count, page count, chapter count) surfaces during a crash-test as the thing under scrutiny, trace where it came from. A generic external benchmark (a genre convention, a publishing format norm) masquerading as a derived requirement of *this specific story* is a common false signal — check the target's origin before trusting a crash-test that's oriented around hitting or missing it.

---

## The blind inventory protocol

Used whenever a suspected pattern (a repeated device, a character's distinctiveness of voice) needs testing without the tester's own prior diagnosis contaminating the result.

1. **Inventory first, mechanically** — count/list every instance of the suspected pattern without judging any individual instance yet.
2. **Strip identifying context** where feasible — anonymize speaker labels for a voice audit, present instances out of their narrative order for a device audit — specifically to block the topic/content of an instance from doing the identifying work that the *form* (word choice, rhythm, structure) is supposed to be tested for.
3. **Judge each instance individually against a fixed rubric**, decided before looking at the inventory (for voice: sentence length, precision, register/address, relationship to silence; for a repeated device: what functional job does *this* instance do, independent of the others).
4. **Only then compare across instances** and look for real groupings — expect, going in, that a pattern which looked homogeneous by raw count often splits into two or more distinct families once tested individually, or turns out to include instances that are doing necessary, non-redundant work despite superficial similarity.
5. Report the finding with its evidence-doctrine category made explicit: a raw count is a textual observation; "these four all read the same" only becomes a defect claim once you can say *why*, tested per-instance, not asserted from the aggregate.

---

## The character-voice audit (an instance of the blind inventory protocol)

Anonymize and shuffle a sample of dialogue lines across all major characters into unlabeled blocks. Score each block on fixed, pre-declared axes (sentence length, precision/vagueness, formal/informal address, relationship to silence and interruption — adapt axes to the project) *before* revealing who said what. Reveal identities only after scoring. A voice audit that scores lines with speaker identity visible is not testing what it claims to test — topical content will do the identifying work instead of form, and the audit will falsely pass characters who differ only in what they talk about, not how.

---

## The information audit (operationalizing the three-way distinction)

For a scene or passage under suspicion of over-explaining:

1. List every piece of information conveyed in the passage.
2. For each, mark which of the three sets it actually serves: **author** (bookkeeping the writer needs), **character** (what this person would know/say, in-world), **reader** (what's needed for the intended reading effect).
3. Any information marked *author-only* or *character-only*, with no reader-facing job, is a candidate for cutting — its presence is usually the actual mechanism of a "this over-explains" complaint, more often than sentence-level prose quality.
4. Cross-check against Phase 8 reader reports: an "I didn't understand X" report should be checked against this audit before assuming the fix is *adding* information — it is at least as often a sign that the *reader-facing* function of an existing passage is being crowded out by author/character-only material sitting in the same space.

---

## The factual audit (operationalizing Phase 7)

1. Extract every claim in the manuscript presented as fact about the real world (not fictional-world facts, which are Phase 2/6 continuity concerns instead).
2. Classify each: factual truth / plausibility / internal coherence / narrative effectiveness (see Phase 7 in `phases.md` for what each means).
3. Rank by risk — a claim central to the plot's credibility outranks a claim that's pure incidental color — and verify in that order, not manuscript order.
4. For each claim, record the verification source and tier (primary/official, secondary-quality, unofficial compilation), and mark explicitly as **unresolved** anything that couldn't be checked, rather than defaulting to either accepting or silently cutting it.
5. Log corrections the same way any other finding is logged: what changed, and why, distinguishing a pure fact correction (no procès needed, Phase 9 path (a)) from a correction that also touches how the fact is *used* narratively (which may need a procès, Phase 9 path (b), if the manuscript is already frozen).
