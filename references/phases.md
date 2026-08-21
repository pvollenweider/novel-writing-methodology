# Phases — full specification

Each phase below has the same shape: **entry condition** (what must be true to start), **exit condition** (what must be true to move on), **allowed registers** (what files/notes this phase may produce — cross-check against the one rule in SKILL.md before creating any of them), **what to do**, **what to refuse**, and **questions to ask the author before acting**. "Reopening" describes what legitimately sends the project back to this phase from a later one.

---

## Phase 0 — Project contract

**Entry condition:** the author wants to write a novel and has *something* — an idea, a subject, a pile of research, a character, an image. Nothing else is required.

**Exit condition:** a short, explicit statement exists (even informally, in conversation) of: what the book is trying to do *to a reader* (not to a topic); the one or two principles that will arbitrate scene-level decisions later (e.g. "plot before thesis," "no comfortable outside position for the reader"); the real constraints (length, deadline, subject sensitivity, audience); and — this is the part most easily skipped — what is *deliberately left undecided* for now (an ending, a character's ultimate fate, a title, a tone call) so that later indecision on these points doesn't get mistaken for a stalled process.

**Allowed registers:** a project contract note. One document, short, revisited only when a later phase produces a reason to revise it (rare — treat contract changes as a big deal).

**Do:** ask the author to state the book's effect on a reader in one sentence before anything else; push back if the answer is a subject ("a novel about grief") rather than an effect ("a reader who finishes this should no longer trust their own account of why they forgave someone"). Write down what stays undecided as explicitly as what's decided. If it helps calibrate register or technique, naming one or two comparable published works and what specifically they do well for this project is a legitimate, lightweight part of this phase — an appendix to the contract note, not a separate register; the point is a working reference for technique, not a literature review.

**On the title and author-name specifically:** these are legitimate to leave undecided here (see the exit condition), but they don't resolve themselves by default — they need their own deliberate decision eventually. The title has its own protocol (`protocols.md`, title-selection protocol), typically run near the freeze (Phase 10). Attribution (real name, pseudonym, anonymous) is a separate decision from the title — don't let a production or packaging default (Phase 11) silently answer either one.

**Refuse:** to proceed to architecture or drafting without at least an informal answer to "what is this trying to do to a reader." A subject is not a contract.

**Ask the author:** What should a reader feel/believe/doubt by the last page that they didn't at the first? What's the one rule that, if violated, would mean the book failed even if every sentence were well-written? What are you *not* deciding yet, on purpose?

**Reopening:** almost never, and treat it as a serious event when it happens — a contract change this late usually means Phase 2 revealed the original premise doesn't hold up, which is a legitimate but expensive discovery.

---

## Phase 1 — Research & world

**Entry condition:** Phase 0 contract exists.

**Exit condition:** research stops producing reversals of understanding — moments where a source changes what the author thought was true or possible — and starts producing only more material of the same kind. Stop at the first point, not the second. This is a judgment call, not a countable threshold; when in doubt, ask the author whether the last few sources changed anything or just confirmed what was already known.

**Allowed registers:** a source register (what was consulted, its reliability tier, what it's used to support); explicitly, four separate buckets of findings — **plot-critical facts** (the story doesn't work without these being right), **comprehension material** (background the author needs to write convincingly but the reader doesn't need explicitly), **verisimilitude detail** (texture — names, places, procedures — wrong ones will be noticed by an informed reader but nothing structural depends on them), and **the bucket that matters most and is easiest to skip: knowledge that should probably never appear in the book at all.** A successful research phase produces things the author now knows *not* to show — dumping everything learned onto the page is the single most common way research-heavy fiction fails.

**Do:** grade sources by reliability tier (primary/official, secondary-quality, unofficial compilation) and never let a low-tier source carry a claim that needs a high-tier one. Pre-register what a piece of research is being used to test *before* reading it, where practical — this limits the temptation to read sources into confirming what's already assumed. Document access limits (a blocked source, an unverifiable claim) as findings, not as gaps to quietly paper over later.

**Refuse:** to treat "I found more information" as itself a reason to keep researching — the exit condition is about reversals, not volume. Refuse to let research run concurrently with *canonical* drafting (Phase 6) without an explicit decision that a specific fact is now locked; exploratory pilots (Phase 5) are fine to run in parallel with ongoing research, canonical text is not.

**Ask the author:** Of everything you've found, what changed your mind about the story, versus what just supports what you already assumed? What have you learned that you suspect should never actually appear on the page?

**Reopening:** a later audit (Phase 7 or 7) surfaces a fact the story depends on that was never actually verified — reopen narrowly, verify that one fact, close again. Don't let a narrow reopening become a general re-research pass.

---

## Phase 2 — Dramatic architecture

**Entry condition:** Phase 1 has produced enough plot-critical facts to build on (doesn't need to be finished — see the concurrency note above).

**Exit condition:** every major beat of the story has, at minimum, an answer to the mandatory question below, and the causal chain between beats holds — event B is possible/necessary *because* of event A, not merely sequenced after it.

**Before mapping causal beats, generate them separately from selecting among them.** When inventing what happens — between two established points, in response to a character's situation, to fill a gap the architecture reveals — don't require each candidate development to justify itself as it's produced; generate several genuinely different ones, including ones that will turn out to be wrong, redundant, or mutually exclusive. Only then, for each candidate, ask: what decision does it force, what relationship does it change, what information changes hands and at what cost, what future possibility does it close off, and what does it make possible that the alternatives don't? Select using those answers — see the exploration protocol in `protocols.md`. Running selection criteria *during* generation is the same mistake Phase 6 protects canonical drafting against, one phase earlier.

**This is the phase most existing "book governance" methods skip entirely**, and its absence is what makes a project intellectually rigorous without the story actually working. Work through, at minimum:

- **Desires and needs** for each major character — not the same thing; a want is conscious and stated (even to themselves), a need is what the story's shape suggests they actually require, and the gap between the two is usually where the story lives.
- **Antagonistic forces** — not necessarily a villain; can be another person's competing want, an institution, a circumstance, or a part of the protagonist's own mind.
- **Information asymmetries** — who knows what, when, and what it costs them to reveal or conceal it. Most real narrative tension is an information asymmetry with a cost attached to closing it.
- **Causality between events** — chronology is not causality; check that later events require earlier ones, not just follow them.
- **Irreversible decisions** and their cost — moments a character cannot undo, and what they pay for having made them.
- **How relationships evolve** — state-to-state, not just "conflict happens." What does the relationship look like before and after this beat, specifically?
- **Narrative promises and their disposition** — a strong expectation the text creates should not disappear by accident. It doesn't have to be paid in the sense of resolved as expected: it can be paid, deliberately displaced onto something else, consciously subverted, or knowingly frustrated (a red herring, a focalization effect, a piece of characterization about what this narrator or character thinks matters) — a Chekhov's-gun rule applied absolutely turns a novel into a closed puzzle-box and punishes exactly the kind of texture, misdirection, and false emphasis real fiction uses on purpose. What actually needs tracking is only this: whatever a promise's fate turns out to be, it should be a decision, on record, not an oversight discovered by a reader before the author.

**The mandatory question, applied to every scene in the architecture, before any scene is trusted — asked in two parts, not one:**

> *If this scene disappeared, what becomes impossible later?*
> *If nothing becomes impossible, what becomes meaningfully different for the reader — what they know, feel, suspect, or how they read something else?*

The first question tests causal load-bearing and is the one most existing methods (and an unguarded reading of this one) stop at — but a scene can be indispensable for changing how a reader interprets something without making any later event impossible, and a purely causal test will misclassify that scene as cuttable. Only when *both* answers are genuinely "nothing" is there a real presumption of unnecessity. "It provides atmosphere" or "it establishes tone" can be a legitimate answer to the second question — but the discipline is knowing that's the answer being given, in writing, rather than assuming every scene is load-bearing by default, and rather than only ever asking the first, causal-only version of the test.

**Allowed registers:** an architecture map (beats, causal links, the mandatory-question answer per beat); a continuity register (facts established once that must not silently drift — a birthdate, a distance, a promise made). Do **not** let quantitative targets (a target scene count, a target chapter count) become anything more than a rough estimate for planning — write down explicitly, at the moment such a number is first used, that it is an estimate and not a target, so it can't quietly harden into one later.

**Do:** build in "residue" deliberately — something in a scene that serves no plot function, so that a reader attentive enough to spot the machine can't reliably tell load-bearing information from texture just by noticing which details get narrative weight.

**Refuse:** to treat a fully mapped architecture as a chapter outline. The map is a causal skeleton, not a table of contents — the actual chapter boundaries get discovered during Phase 4 (sequencing) and tested in Phase 5-6, and forcing the map's granularity onto the manuscript produces exactly the over-planned, machine-visible feeling this phase exists to prevent.

**Ask the author:** For this beat, what becomes impossible if it's cut? Who doesn't know what here, and what does it cost them to find out? What have you promised the reader, even implicitly, that you haven't paid off yet?

**Reopening:** a Phase 7 causality audit finds a beat that doesn't actually follow from what precedes it; a Phase 9 reader report shows a promise's disposition (paid, displaced, or deliberately frustrated) isn't landing as intended. Reopen the specific beat, not the whole map.

---

## Phase 3 — Characters

**Entry condition:** Phase 2 architecture exists at least in draft form (characters and architecture inform each other — don't force strict sequencing here in practice, but don't skip character work either).

**Exit condition:** for every character who carries a scene, the seven questions below have real, specific answers — not personality-trait adjectives.

**Actively avoid encyclopedic biographical sheets** (childhood, full backstory, physical description inventories). They produce an illusion of depth without producing scenes that work — a character becomes novelistic through choices made under pressure, not through the quantity of information available about them off the page. Track instead, per character, kept current as the manuscript evolves:

1. What do they want *right now*, in this specific scene or stretch of the book — not their life goal, their immediate want?
2. What do they refuse to see?
3. What do they actually know?
4. What do they wrongly believe?
5. What are they hiding, and from whom?
6. What would they actually do under real pressure — tested, ideally, by writing it, not by asserting it?
7. How are their relationships changing, specifically, scene to scene?

**Allowed registers:** a living character register organized around these seven questions, updated as the manuscript reveals what's actually true of a character in practice (a character's answers can and should shift as pilots and drafts test them — that's a feature, not drift to be corrected).

**Do:** treat contradictions between what a character says about themselves and what question 6 (pressure-tested) reveals as material, not as errors to fix — that gap is frequently the actual story. Use dialogue/voice differentiation as a *check* on this register (if two characters are interchangeable in what they want and refuse to see, that will show up as interchangeable voices in Phase 7).

**Refuse:** to accept a character trait ("she's stubborn," "he's passive") as an answer to any of the seven questions — push for the specific instance: stubborn about what, refusing to see what, right now.

**Ask the author:** What does this character want in this specific scene, separate from what they want in the book overall? What would surprise even them about what they'd do here under real pressure?

**Reopening:** a Phase 7 audit finds two characters functionally indistinguishable, or a decision in Phase 6 that a character "wouldn't do that" without a clear reference for what they would do — reopen for that character specifically.

---

## Phase 4 — Chapter/beat sequencing

**Entry condition:** Phase 2 architecture exists at least in draft — a causal skeleton of beats, not yet a table of contents.

**Exit condition:** every beat has been assigned to a concrete narrative unit (chapter, section) with an answer to the four questions below, and the skeleton itself has stopped being visible in the assignment — see "Refuse" below.

**Why this is its own phase, not part of architecture or drafting:** the architecture map (Phase 2) is deliberately not a chapter outline — forcing its granularity directly onto the manuscript is exactly what produces the over-planned, machine-visible feeling Phase 2 warns against. But going straight from a causal skeleton to prose (Phase 6) skips the actual work of discovering what belongs *between* pivots, in what order, and where a chapter should end — decisions that are structural, not sentence-level, and that a first draft written straight through tends to make by inertia rather than by test. This phase exists to make those decisions deliberately, while still keeping them provisional.

For each narrative unit, answer:

1. **Which beat (or beats) from the Phase 2 architecture does this unit carry?**
2. **What ordinary, banal life surrounds the beat here** — the ostensible reason a reader (and the characters) would be in this scene at all, independent of its structural function?
3. **What hypothesis does the reader leave this unit believing** — not what they've been told, what they'd now bet on?
4. **Where, specifically, does the causal skeleton disappear from view** — the moment in this unit where a reader stops being able to see the architecture working, if it's working?

**The wrong-place test:** check the instinct to end a unit immediately after its twist or its best line. That placement is often exactly where the machine becomes visible — the unit announcing its own structure by stopping the second it's delivered its payload. Test at least one alternative cut point (earlier, so the payoff lands inside ordinary continuing action rather than as a closer; or later, so something inconsequential absorbs the ending beat) before defaulting to the obvious one.

**Allowed registers:** a sequencing document, explicitly marked as a discovery draft, not a fixed plan — state this in writing at the top of the document itself, since this is the register most likely to quietly harden into an outline that then gets defended rather than tested. One entry per unit: beat(s) carried, the four answers above, the cut-point decision and the alternative(s) rejected.

**Do:** let this phase discover units the Phase 2 architecture never anticipated — connective or breathing scenes that exist to carry the four questions above for their surrounding units, not to add a new beat. Let it run concurrently with Phase 5 pilots: a unit's sequencing questions and a pilot testing that same unit's specific mechanism inform each other.

**Refuse:** to treat a completed sequencing document as itself a table of contents to be defended — it remains a discovery document until Phase 6 drafting has tested it. If a unit doesn't survive contact with drafting, resequence rather than force the draft to match a plan that turned out to be wrong.

**Ask the author:** For this stretch of the book, what's the ordinary reason anyone is where they are? Where would this unit end if you weren't trying to land the line?

**Reopening:** a Phase 7 rhythm or artificiality finding (a unit that feels engineered, a cut that lands on the machine rather than past it) can send the project back here for that unit specifically, rather than straight to a Phase 6 rewrite with no structural rethink.

---

## Phase 5 — Pilot scenes

**Entry condition:** a specific narrative mechanism needs testing before it's worth writing into the canonical draft — can begin as soon as Phase 2/3 produce a testable hypothesis, in parallel with ongoing Phase 1 research.

**Exit condition:** a verdict — pass, fail, or indeterminate — recorded *before* any rhetorical after-the-fact rescue of a failed pilot is attempted.

**Do:**
1. State the hypothesis explicitly and narrowly. Example shape: *"Character A can learn fact X in this scene without Character B becoming a walking information dispenser."* Not "test the reveal scene" — name the specific risk being tested.
2. Fix the pass/fail criteria *before* drafting the pilot. If the criteria are written after reading the draft, the test is void — rewrite the pilot with real criteria fixed first, don't just retroactively grade what already exists.
3. Write the pilot as genuinely disposable — one pass, not polished, not defended. The verdict is about the mechanism, not the prose quality of the throwaway draft.
4. Render a verdict: **pass** (mechanism works, can inform the canonical scene), **fail** (mechanism doesn't work as conceived — record why, don't just discard), or **indeterminate** (test was inconclusive — usually means the criteria were wrong, not that the mechanism is fine; fix the criteria and retest, don't default to pass).

**Allowed registers:** a pilot log — hypothesis, criteria, verdict, one line on why — for both passed and *especially* rejected pilots. A rejected pilot with a clear reason is more valuable to keep than a vague success.

**Refuse:** any rhetorical rescue of a pilot that failed its own pre-stated criteria — "but it's not that bad if you consider..." is exactly the move this protocol exists to block. A failed pilot is discarded or redesigned with new criteria, never kept on the strength of an argument made after the fact.

**Ask the author:** What's the one thing this pilot needs to prove works, specifically? What would make you say "no, cut this" even if you like how it reads?

**Reopening:** rarely reopened directly — pilots feed forward into Phase 6. If a canonical scene isn't working and no pilot tested its specific mechanism, that's a sign to drop back and pilot it before continuing to revise it in place.

---

## Phase 6 — Canonical drafting

**Entry condition:** the scene has either a passed pilot behind it, or is judged simple/low-risk enough not to need one (a judgment call — narratively pivotal or structurally risky scenes should almost always have a pilot; connective or low-stakes scenes often don't need one).

**Exit condition:** the scene is written.

**The near-constitutional rule of this phase: do not audit a scene while writing it.** Write first. Examine later, in Phase 7, as a separate pass. This is not a productivity tip — it is a direct countermeasure to the project's central risk: a reader senses the machine because the author was sensing the machine constantly while building it. A scene drafted under continuous self-audit reads as controlled and machine-visible even when every individual line is defensible.

This also means: **Phase 6 is explicitly protected from the word-by-word economy discipline that governs Phase 10 procès corrections.** Counting and justifying every word belongs to surgical, post-freeze correction of a text that has already proven itself. Imposed on a first draft, it produces inhibited, over-controlled prose — the opposite of what a canonical draft needs. If you notice yourself (or the author) applying procès-style word-counting discipline during drafting, stop and name it explicitly as out of place here.

**Allowed registers:** the manuscript itself, plus routine continuity checks against the Phase 2 continuity register (geography, timeline, established facts) done *in the course of* drafting, not as a separate audit pass layered on top of writing.

**Do:** verify concrete facts (geography, schedules, calendar, exact names) as they come up during drafting rather than deferring all of it to a later pass — fixing a wrong bus schedule the moment it's noticed is cheap; finding it in Phase 7 costs a re-read.

**Refuse:** to run any of the Phase 7 narrative audits, the Phase 8 factual audit, or a procès-style line edit *during* this phase, even if the author asks for feedback mid-draft on a specific worry. Redirect: finish the draft, then audit — say why, briefly, rather than just declining.

**Ask the author:** (mostly none — this phase is protected from interruption by design) — if the author brings mid-draft doubts, the one useful question is whether the doubt is about a fact (fix it now) or about quality/effect (hold it for Phase 7).

**Reopening:** N/A — this phase produces the draft that the rest of the process works on.

---

## Phase 7 — Narrative audits

**Entry condition:** a canonical draft (of a scene, chapter, act, or the whole manuscript) exists.

**Exit condition:** each audit below has been run at least once at the appropriate scale (scene, chapter-block, or whole manuscript) and produced either a clean result or a located, actionable finding.

Run these as **separate, orthogonal passes**, not one mixed read-through — mixing them is how a rhythm problem gets mis-diagnosed as a causality problem or vice versa:

- **Causality** — does each event actually follow from what precedes it, or merely come after it?
- **Character** — does each character act consistently with their Phase 3 answers, or does a scene require them to become someone else for a beat to work?
- **Information** — apply the three-way distinction below; this single confusion produces most over-explanation in fiction.
- **Tension** — is there an active question pulling the reader forward at every point, or a stretch where nothing is genuinely uncertain? For a passage where the argument itself is the engine (see Constitution item 2), test several possible sources of directional pressure — irreversibility, escalation, changing stakes, a transformation of the perceiving consciousness or the reader's own frame, formal development, concrete particularity — without requiring all of them, or even a specific one of them. The decisive question is whether the sequence produces a cumulative change that depends materially on its order, not whether it clears a fixed list. A useful destructive test: try permuting the major units. If most of them can be reordered without changing the experience, the passage is probably static regardless of which properties it superficially has; if the order matters, it's moving.
- **Rhythm** — pacing at the sentence, scene, and chapter level; where does the text speed up or slow down, and is that deliberate?
- **Artificiality** — where does the reader feel the machine? (Often findable by asking: does any scene exist *only* because the plot needs the information in it, with no other reason for the characters to be where they are, doing what they're doing?)
- **Continuity** — cross-check against the Phase 2 register; facts established once must not silently drift.

**The three-way information distinction (apply constantly, not just in this phase):**

> Information necessary to the **author** (to keep the story straight) ≠ information necessary to the **character** (to act believably) ≠ information necessary to the **reader** (to follow and feel the story).

An enormous amount of novelistic over-explanation comes from confusing these three sets — writing something into the text because the *author* needs to track it, or because a *character* would logically know it, when the *reader* doesn't need it stated to feel the scene's effect. Before adding an explanatory line, ask explicitly which of the three sets it's serving, and whether that set is actually the reader's.

**Allowed registers:** one finding log per audit type, each finding tagged by evidence-doctrine category (fact / textual observation / reading effect / causal interpretation — see SKILL.md) and by scale (this scene / this chapter / this act / global).

**Do:** where a finding comes from a statistical inventory (e.g. counting a recurring device across the manuscript), **re-test it functionally, occurrence by occurrence**, before treating it as a homogeneous defect. A pattern detected by raw count frequently turns out to be two distinct families that only looked like one thing in aggregate, or to be doing different, necessary work in each instance.

**Refuse:** to treat "I can defend this on a re-read" as equivalent to "this passed the audit" — the audits are meant to be somewhat adversarial; a clean pass should survive an attempt to find the problem, not just an absence of looking.

**Ask the author:** For this scene, which of the seven audits above are you actually worried about? (Focuses the pass; running all seven with equal suspicion on a huge manuscript is expensive and usually unnecessary.)

**Reopening:** a finding here can send the project back to Phase 2 (architecture doesn't hold), Phase 3 (character inconsistency), or straight back to Phase 6 for a rewrite — record which, and why, in the finding log.

---

## Phase 8 — Documentary / factual audit

**Entry condition:** the manuscript contains claims presented as real-world fact (history, science, institutional process, real places/events) — skip this phase entirely for novels that don't.

**Exit condition:** every factual claim identified has been classified and, where the classification requires it, externally verified.

**Before classifying a claim's truth, locate whose claim it is and what kind.** A real-world assertion in the text can be the narrator's own (checkable, and if wrong, an objectifiable error under Phase 10), a character's stated belief (checkable against reality, but being wrong is not a manuscript defect if the character is written to be wrong — the defect question, if any, is whether the text signals the belief is false where that matters), a character's knowing lie (correct as written precisely when factually wrong), or a deliberate, unresolved ambiguity the text never settles (not a candidate for external verification at all). Running this audit without making that attribution first is how a factual audit becomes overzealous — "correcting" a lie, a wrong belief, or an intentional ambiguity as if it were the narrator's error.

Classify every claim that turns out to be a narrator assertion or a checkable character belief into exactly one of these, and **do not let a strong result in one column substitute for checking another**:

- **Factual truth** — is it actually correct, checked against a source outside the book?
- **Plausibility** — would it be believed as true within the story's world, independent of whether it is?
- **Internal coherence** — does it agree with everything else the book has already established?
- **Narrative effectiveness** — is it *used* well, regardless of the first three? (A fact can be perfectly true, plausible, and coherent, and still be a bad choice for the scene it's placed in.)

**Allowed registers:** a factual claims inventory (claim, category assigned, source checked or explicitly marked unverifiable, verdict). Order verification by risk (a claim central to the plot's credibility first, incidental color last) rather than by the order claims appear in the manuscript.

**Do:** mark claims that couldn't be verified (blocked source, no primary document available) as explicitly unresolved rather than silently accepting or silently cutting them — an honest "unverified" is more useful later than a guess dressed as a check.

**Refuse:** to let a source's authority alone settle a *narrative effectiveness* question — "this is historically accurate" is not an answer to "does this work in the scene."

**Ask the author:** Which factual claims in this manuscript would most damage the book's credibility if wrong? Start verification there.

**Reopening:** a factual error found late (even post-freeze) is one of the few things that can reopen a frozen manuscript directly as an objectifiable error (see Phase 10) — no procès required for a pure factual correction, though the correction should still be minimal and localized.

---

## Phase 9 — External readers

**Entry condition:** internal audits (Phase 7-8) are substantially run for broad beta reading. For a narrow, single-mechanism test on a specific worry, entry is much earlier — right after Phase 5/6 produce the scene in question — because some defects (boredom, confusion, failure to attach to a character) are ones the author is structurally worst-positioned to detect through more self-audit.

**Exit condition:** reader responses have been collected, classified by evidence-doctrine category, and either converged into a clear, actionable signal or explicitly logged as inconclusive.

**Ask readers to describe their experience, not propose solutions.** "What would you change?" produces noise — readers are rarely reliable diagnosticians of their own reactions, however reliable they are at reporting the reactions themselves. See `references/reader-questions.md` for the actual question bank; the shape is always: *what happened to you as a reader*, never *what should I do about it*.

**The critical distinction to hold onto:** a reader can correctly report an effect while incorrectly diagnosing its cause. "I stopped believing this character partway through" is a strong, usable signal even if the reader points to the wrong scene as the cause. Do not let "they identified the wrong scene" become a reason to discard what they actually experienced — treat the reported effect and the reader's proposed cause as two separate claims, in two separate evidence-doctrine categories (reading effect vs. causal interpretation), and test the effect independently before accepting or rejecting the proposed cause.

**Allowed registers:** a reader-response log per reader, transcribed close to verbatim, tagged by evidence category before any synthesis is attempted. A synthesis note (patterns across readers) is a separate, later document — never skip straight from raw responses to synthesis without the tagging step.

**Do:** treat divergence between two readers on the same point as a result, not noise — a split reaction is itself information (the text may be doing something genuinely ambivalent, on purpose or not) and deserves investigation before being resolved either way.

**Refuse:** to silently upgrade "these two fixes are technically compatible, we could do both" to "these two readers actually agree" — compatibility of fixes and agreement of readers are different claims; conflating them has produced real errors in past use of this method.

**Ask the author:** Before sending the manuscript out — what threshold will actually trigger a reopening? Fix this *before* reading responses, not after seeing whether you like them (this is Phase 10's freeze threshold, and it should already be decided by the time reader responses arrive).

**Reopening:** this phase's entire output either triggers Phase 10's reopening criteria or it doesn't — see Phase 10. Don't let a compelling-sounding but unlocalized preference from a reader reopen anything on its own.

---

## Phase 10 — Freeze & procès

**Entry condition:** internal audits and (at least one round of) external reading are complete; the author is willing to commit to a canonical text.

**Exit condition:** never fully exits — this is the phase the manuscript lives in from freeze onward. "Exit" only in the sense of a specific procès closing.

**On freezing:** state explicitly, in writing, the freeze rule before it's needed: no further change on simple rereading discomfort; reopening only for (a) an objectifiable error, (b) an external signal that is either convergent across independent readers or precisely localized by at least one, or (c) an exceptional revision that clears the much higher bar below. Distinguish these three reopening paths sharply and do not let one bleed into another:

- **(a) Objectifiable error** — factual, grammatical, or a demonstrable internal incoherence found *in the text itself*. Needs no external reader, no procès preamble — fix it directly, minimally, and log it.
- **(b) External signal, precisely localized or convergent** — requires the full procès protocol below before any text changes. This path exists to fix a located problem.
- **(c) Exceptional revision** — a proposed improvement that is not a response to any identified defect. Rare and deliberately expensive by design; see below.

**What the freeze is actually for, and what it is not.** The freeze exists to stop compulsive, ungoverned optimization — rereading-and-tweaking that erodes a text without ever producing a clear, tested improvement. It is not a claim that the frozen version is the best possible version, and it should never be defended as if it were: a rule whose job is to block *unexamined* change is not the same rule as one that blocks *all* change, and collapsing the two turns the freeze from a discipline into dogma — governance outranking the book it exists to protect. Path (c) exists precisely to keep that distinction real rather than theoretical.

**(c) in full — the exceptional-revision bar.** A genuinely better idea, on its own, does not clear this bar: "I had a better idea" and "nothing's broken" do not license a change, no matter how good the idea is or how confident the author is (this is the ordinary case — see the Constitution's stance on change requiring a stated, testable gain). What clears it is a proposal that has been made to pay for its own reopening, in this order, before any text is touched or any comparison is made:

1. **State the specific additional effect the new version should produce**, as a claim that could fail — not "it's better," but what a reader would experience, know, or feel differently, and how you'd recognize that happening.
2. **State what the new version must not damage** — which promises, which causal links, which established voice or rhythm — named explicitly before the comparison, not discovered after.
3. **Test blind against the frozen version**, not by rereading the new one in isolation and preferring it — a comparative test (see the exceptional-revision protocol in `protocols.md`) with the winning criteria fixed before anyone sees which version is which.
4. **Require a real threshold, not a narrow or split preference** — decide in advance what would count as the new version actually winning (e.g. strong, non-split convergence across several blind readers), so a marginal or divided result defaults to keeping the frozen version.
5. **If it passes, execute through the standard procès discipline** (Steps 4-6 of the procès protocol: minimum necessary change, verify the local seam, close explicitly) — passing the comparison earns the right to a procès, not a blank check to rewrite freely.

A path (c) revision that fails any of these — no stated effect, no named risk, no blind test, a split or marginal result — stays exactly what it was: a preference, not a defect, and the frozen version stands. This should be rare enough that most projects never use it; if it's being reached for often, that's a sign the freeze itself was declared too early, not that path (c)'s bar is wrong.

**A subtle trap to guard against explicitly:** a destructive test that shows a cut is "lossless" does **not** retroactively make that cut an objectifiable error under path (a). Passing a test is evidence for a procès under path (b) — it is not a shortcut around running one. The same applies to path (c): passing the blind comparison earns a procès, it does not retroactively prove the frozen version was defective. Keep these distinctions sharp; conflating "tested and preferred" with "was wrong" is the single easiest way for the freeze to erode without anyone deciding to erode it.

**Allowed registers:** the freeze declaration itself (with its threshold stated explicitly, including path (c)'s bar); from here on, all further registers are procès logs, plus an exceptional-revision log for any path (c) attempt (proposed and tested, whether it passed or not) — see `references/protocols.md` for the full six-step procès protocol and the exceptional-revision protocol.

**Do:** treat the freeze as a real commitment, not a formality — the value of freezing is precisely that it stops the kind of endless, ungoverned rereading-and-tweaking that erodes a text without ever producing a clear improvement. Treat path (c) as equally real but load-bearing in the opposite direction: it exists so the freeze doesn't become a reason to ship a worse book than the author is capable of writing, on the strength of chronology alone.

**Refuse:** any change proposed on the basis of an unlocalized preference ("I'd have liked more of X") or an untested "better idea," no matter how reasonable it sounds, without an objectifiable error, a properly run procès, or a path (c) revision that has actually cleared its bar (not merely been proposed).

**Ask the author:** each time a possible reopening arises — is this an objectifiable error, a signal that needs a procès, or a proposed improvement that needs the exceptional-revision test? If (b), what is its single, bounded object? If (c), what's the specific claimed gain, what must not be damaged, and what would the blind test need to show to actually win? (Never let a procès's or a revision's object drift wider once fixed.)

**Reopening:** by definition, this phase only reopens narrowly, via the three paths above, one bounded object at a time. It does not "exit" back to earlier phases except in the rare, serious case of a Phase 8-grade factual error significant enough to require re-examining a whole documentary thread — treat that as an exceptional event, not routine.

---

## Phase 11 — Production

**Entry condition:** a frozen (or at-least-currently-stable) canonical text exists.

**Exit condition:** N/A — production can run indefinitely and repeatedly (new formats, new editions, cover revisions) without ever touching this phase's own gate condition, which is exactly the point.

**The governing separation:** production (typography, layout, output formats, cover design, packaging) is categorically different from the "repasse rédactionnelle" (content revision) that Phase 10 tightly controls. Production never modifies the frozen source text — it reads it and derives output. This separation should be structural, not just a stated intention: whatever tooling generates output formats should read the frozen text as an immutable input and write to a separate derived file, so that a production fix (fixing a typographic widow, a bad line break, an EPUB rendering bug) can never accidentally become a content edit, and so content edits are never smuggled in "while we're in there anyway."

**Allowed registers:** a production changelog (what changed, in the output pipeline, and why) — kept separate from the procès log, because production changes don't need procès justification; they're typography, not content.

**Do:** verify production output against the frozen source after every pipeline change — a rendering bug (a silently dropped element, a mis-encoded character, an unwanted duplicate section) is still a defect even though it never touches "the text" in the Phase 10 sense. When deriving more than one output format from the same source (print PDF, EPUB, etc.), check each structural marker (a scene break, a part boundary, a frontmatter page break) against **every** target format separately — a marker coded for one rendering engine (e.g. a raw LaTeX block) commonly has no equivalent for another (e.g. an EPUB/pandoc writer), so it renders correctly in one output and silently vanishes or duplicates in another. This is a distinct failure mode from a single-format bug and needs its own check per format, not just a general "does it look right" pass on whichever format was checked first.

**Refuse:** to let a production-phase observation ("this sentence reads awkwardly in this typeface/format") become a content edit without going through Phase 10's reopening criteria like anything else. Production revealing an awkward sentence is not different, procedurally, from a reader revealing one.

**Ask the author:** for any output format or packaging decision that touches presentation of authorship, title, or framing (not just layout) — these are editorial identity decisions, not typography, and should be treated with the same deliberateness as a Phase 0 contract decision, not defaulted by whatever the production tooling happens to do.

**Reopening:** production issues never reopen Phase 10 on their own — if a production pass reveals the text itself needs a change (not just its rendering), that's a Phase 10 reopening on its own separate merits.
