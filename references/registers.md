# Registers — templates and their justification

Every register below exists only because it passed the one rule in `SKILL.md`: *what future decision will this let us make that we couldn't make as reliably without it?* That justification is stated for each one — if a project's version of a register can't answer that question, don't create it, regardless of what's listed here. These are templates to adapt, not a mandatory paperwork set.

Keep every register as a plain, append-only log where practical (add entries, correct with visible strikethrough, never silently delete or rewrite history) — the record of a wrong turn has its own value, consistent with the Constitution's stance on observation before diagnosis.

---

### Source register (Phase 1)
**Decision it enables:** whether a claim can be trusted enough to build plot on, versus needs independent confirmation before the story depends on it.
- Source, reliability tier (primary/official, secondary-quality, unofficial compilation), what claim(s) it's used to support, access status (available / blocked / partial). When a higher-tier source later surfaces for a claim already recorded against a lower-tier one, recode the entry against the new source and note explicitly that the result was downgraded/upgraded — don't just add the new source alongside the old without revisiting the verdict it produced.

### Findings register, four buckets (Phase 1)
**Decision it enables:** what to actually write into the book versus deliberately keep out of it.
- Plot-critical fact / comprehension material / verisimilitude detail / **known-but-not-shown** — one line each, with the bucket assignment stated (not left implicit).

### Exploration candidates log (Phase 2, as needed)
**Decision it enables:** which of several genuinely different developments actually gets built into the architecture, on the strength of its consequences rather than which one was most fun to write.
- Candidate, its consequences (decision forced, relationship changed, information cost, what it forecloses, what it uniquely enables), selected/rejected, one line why. See the exploration protocol in `protocols.md`. Skip this register entirely when generation was trivial (one obvious option) — it exists for genuinely divergent inventing, not routine plotting.

### Architecture map (Phase 2)
**Decision it enables:** whether a beat earns its place before it's ever drafted, and whether the causal chain actually holds together.
- Beat, causal link to prior beat(s), both halves of the mandatory question's answer ("if cut, what becomes impossible" and, if nothing, "what becomes meaningfully different for the reader"), and — explicitly — whether any quantitative target mentioned is an estimate or (flagged, ideally never) a hard target.

### Continuity register (Phase 2, checked through Phase 7-8)
**Decision it enables:** catching silent drift in a fact established once, before a reader does — including structural facts, not only diegetic ones.
- Fact **or structural anchor** (a part boundary, a scene meant to carry a specific architectural role), where established, where it's referenced or relied on again (updated as the manuscript grows). Structural anchors drift silently during sequencing and drafting (a scene renumbered or moved can leave the part boundary pointing at the wrong chapter) — check them with the same discipline as a diegetic fact, at the latest before the freeze declaration.

### Character register (Phase 3)
**Decision it enables:** whether a character's actions in a given scene are earned by what's already true of them, or require them to become someone else for the scene to work.
- Character, the seven questions from Phase 3 (want-now / refuses to see / knows / wrongly believes / hides / would-do-under-pressure / relationship trajectory), updated as pilots and drafts test the answers.

### Sequencing document (Phase 4)
**Decision it enables:** whether a beat has a concrete home and a defensible cut point before it's drafted, and whether the skeleton has actually stopped being visible in the plan.
- Unit (chapter/section), beat(s) carried, ordinary-life answer, reader's-exiting-hypothesis answer, where the skeleton disappears, cut-point chosen and alternative(s) rejected. Marked explicitly as a discovery draft, not a fixed outline — restate this at the top of the document itself.

### Pilot log (Phase 5)
**Decision it enables:** whether a mechanism is trusted enough to inform a canonical scene — and, for rejected pilots, what specifically not to repeat.
- Hypothesis (stated before drafting), criteria (stated before drafting), verdict (pass/fail/indeterminate), one line why. Rejected pilots kept, not deleted.

### Narrative audit findings (Phase 7)
**Decision it enables:** whether a scene/chapter/act needs to go back to Phase 2, 3, 4, or 6 — and specifically which.
- Audit type (causality/character/information/tension/rhythm/artificiality/continuity), scale (scene/chapter/act/global), finding, evidence-doctrine category, proposed reopening (if any).

### Style-rule audit (Phase 7, once against the finished draft)
**Decision it enables:** whether a house rule adopted mid-draft (a stylistic constraint, a register boundary) still holds once the manuscript it was written for actually exists, versus needs narrowing or retiring.
- Rule as originally stated, source (where/why it was adopted), a check against the finished text (does an uncontested passage violate it as stated?), verdict (holds as-is / narrowed — with the narrower wording — / retired), one line why. Run this once the draft is complete, not during drafting — it's an audit of the rulebook against a finished text, not a drafting-time constraint.

### Factual claims inventory (Phase 8)
**Decision it enables:** whether a specific factual claim can stand as written, or needs correction, or needs to be marked unresolved.
- Claim, category (truth/plausibility/coherence/effectiveness), source and tier checked, verdict, risk ranking.

### Reader-response log (Phase 9)
**Decision it enables:** whether a reported effect meets the freeze reopening threshold — convergent across readers, or precisely localized by one.
- Reader, question asked, response (near-verbatim), evidence-doctrine tag (reading effect vs. causal interpretation), and — kept separate — any solution the reader volunteered unprompted.

### Freeze declaration (Phase 10)
**Decision it enables:** what specifically counts as grounds for reopening, decided once, referred back to every time a reopening is considered, rather than re-litigated each time.
- Date, the exact reopening threshold as stated (objectifiable error / convergent signal / precisely-localized single signal), what's explicitly declared as *not* meeting the threshold (a named example of a preference that doesn't qualify, if useful).

### Title-selection log (near Phase 10, before or at freeze)
**Decision it enables:** whether a title has actually survived a serious attempt to break it, versus merely being the first thing that sounded right — and keeping the reasoning attached so the title isn't quietly re-litigated from scratch later.
- Baseline ("étalon") title and the specific refutation attempted against it; exclusion constraints used to generate a small candidate family (words/moves ruled out, and why); each candidate's elimination reason (a factual/textual anchor conflict, premature resolution of the book's own central ambiguity, a promise the ending doesn't keep); the cold-page result (does it work printed alone, without the analysis built around it, for a reader who never saw that analysis); final epistemic status stated explicitly as *survived a real attempt to break it*, not *self-evidently right*. See the title-selection protocol in `protocols.md`.

### Procès log (Phase 10, ongoing)
**Decision it enables:** whether a specific post-freeze correction is properly bounded, tested, and closed — and a record for any future procès to check against so scope doesn't silently creep across separate corrections.
- One entry per procès: object (Step 1), candidate locations considered and rejected (Step 2), verification criteria (Step 3), execution and word count (Step 4), local-seam verification (Step 5), closure statement (Step 6). Include rejected procès outcomes (Step 3 criteria failed, no change made) with the same structure.

### Methodology-error log (any phase)
**Decision it enables:** preventing the same reasoning mistake from recurring silently across the project — this is the register most tempting to skip and most useful to keep.
- What was claimed, why it was wrong, the correction (via visible strikethrough in the original note, referenced here), what to watch for next time.

### Production changelog (Phase 11)
**Decision it enables:** distinguishing a rendering/typography fix from a content edit, so production work never needs procès justification and content work is never smuggled in as "just a formatting fix."
- What changed in output tooling/format, why, confirmation that the frozen source text itself was not touched.
