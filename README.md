# novel-writing-methodology

A [Claude Code skill](https://docs.claude.com/en/docs/claude-code/skills) that guides the full lifecycle of writing a novel — from preliminary research and dramatic architecture through character design, pilot scenes, canonical drafting, narrative/factual audits, external-reader testing, manuscript freeze, and disciplined post-freeze correction ("procès"), to production.

It is a **governance system**, not a prose generator: it will not write your book for you, and it actively resists becoming a checklist that produces documentation instead of a better book. See `SKILL.md` for the full rationale, in particular "The one rule above the others."

This skill was extracted from documenting, in detail, the real practice used to write one specific novel, then generalized and corrected for blind spots (it originally under-specified dramatic architecture, character, and voice; some of its rules were sound for that one project but dangerous stated as universal laws — see "Four corrections already built into this version" in `SKILL.md`).

## Installation

Skills are plain directories Claude Code reads from disk — no build step, no package manager.

### Option A — for yourself, across every project (recommended)

```bash
git clone https://github.com/pvollenweider/novel-writing-methodology.git /tmp/nwm
mkdir -p ~/.claude/skills
cp -r /tmp/nwm/novel-writing-methodology ~/.claude/skills/
rm -rf /tmp/nwm
```

Or, if you'd rather keep it updatable via `git pull`:

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/pvollenweider/novel-writing-methodology.git ~/.claude/skills/novel-writing-methodology-repo
ln -s ~/.claude/skills/novel-writing-methodology-repo/novel-writing-methodology ~/.claude/skills/novel-writing-methodology
```

### Option B — for one project only

From the root of your novel's repository:

```bash
mkdir -p .claude/skills
git clone https://github.com/pvollenweider/novel-writing-methodology.git /tmp/nwm
cp -r /tmp/nwm/novel-writing-methodology .claude/skills/
rm -rf /tmp/nwm
```

Commit `.claude/skills/novel-writing-methodology/` to your project's repo if you want it to travel with the project and be available to collaborators automatically.

### Verify it's installed

Start Claude Code in a directory where the skill is visible (per option A or B above) and ask something like *"help me test whether this scene works"* or *"I want to freeze my draft and stop fiddling with it."* Claude should mention consulting the `novel-writing-methodology` skill before answering. You can also just ask directly: *"what skills do you have available?"*

## Usage

Give Claude your manuscript (or describe where you are with it) and tell it what you need: a cold editorial diagnosis, help developing a draft, or a rigorous revision of an existing manuscript. The skill handles the methodology and picks the appropriate phase itself — you don't need to name a phase, invoke a rule, or reproduce any of `SKILL.md`'s structure in your prompt.

- **When to use it:** any stage of work on a novel — early research and architecture, drafting, scene-level diagnosis, reconciling reader feedback, deciding whether a manuscript is ready to freeze, or disciplined post-freeze correction. It also applies to narrower asks that are really one phase of this — "does this scene earn its place," "am I over-explaining this," "how do I make sense of conflicting beta reads," "a character from an earlier book of mine is showing up here, how do I handle the continuity."
- **How to invoke it:** nothing special — just ask, in your own words, as part of a normal Claude Code conversation in a directory where the skill is installed (see above). Claude decides whether the request falls under this skill.
- **What to provide:** the manuscript or excerpt itself (as files, or pasted), plus whatever context actually changes the answer — the stage you think you're at, prior reader feedback, or a specific worry. Don't pre-digest it into a phase or protocol name.
- **What it will do:** determine which part of the methodology is relevant to the task and the project's current state, read the corresponding `references/*.md` guidance, and apply the constitution and evidence doctrine from there — diagnosis before prescription, always.

Examples, phrased as intent rather than method:

- *"Read this manuscript cold and give me a rigorous editorial diagnosis."*
- *"Help me revise this novel without assuming every unusual choice is a defect."*
- *"This manuscript is nearly finished. Identify only changes that can demonstrate a real gain."*

For what actually happens at each phase, see `SKILL.md` and `references/phases.md` — that's the skill's own specification, not something to restate in your prompt.

## A full walkthrough, start to finish

None of this is a required script — the skill infers the phase from context and you can jump in anywhere (most real use is a single request like the ones above, not a guided tour). But if you're starting a short story or novel from nothing and want to see the whole shape, here's one example prompt per phase, in order, phrased the way you'd actually type them:

1. **Project contract.** *"I want to write a short story about a driving instructor. Before anything else, help me nail down what this should actually do to a reader — not the subject, the effect — and what I want to leave undecided for now."*
2. **Research.** *"Here's what I've found out about how driving lessons actually work, day to day. Sort it into what the plot depends on, what I need to understand to write convincingly, what's just texture, and what should probably never make it onto the page at all."*
3. **Dramatic architecture.** *"Here's my rough situation and cast. Before we outline chapters, map the causal architecture — what has to happen, in what order, why B is only possible because of A — and run the two-part necessity test on each beat."*
4. **Characters.** *"For each of my main characters, work out what they want right now, what they refuse to see, what they wrongly believe, and what they'd actually do under real pressure — not adjectives, the specific instance."*
5. **Chapter/beat sequencing.** *"Take this architecture and turn it into real chapter units — which beat lives where, what ordinary life surrounds it, and where the structure stops being visible. Also run a blind boundary pass once I have draft-sized units — I don't want to fix a chapter count in advance."*
6. **Pilot scenes.** *"I'm not sure the scene where she finds out will actually land without over-explaining. Write a disposable pilot that tests just that risk before I draft it for real, and give me a pass/fail verdict against criteria fixed before you write it."*
7. **Canonical drafting.** *"Draft chapter 3 from the sequencing doc. Don't audit it while you write — just write it; we'll examine it in a separate pass."*
8. **Narrative audits.** *"Run the narrative audits on the full draft — causality, character, information, tension, rhythm, artificiality, continuity — as separate passes, not one mixed read-through."*
9. **Factual/documentary audit.** *"There are some real claims in here about how a Swiss driving school actually operates. Run the factual audit and tell me what's verified, what's plausible-but-unchecked, and what's a licensed invention I don't need to check."*
10. **External readers.** *"Here are three beta readers' raw responses, pasted below. Help me work out what actually converges into something worth fixing versus what's an individual preference or a real but as-yet-unlocalized signal."*
11. **Freeze & procès.** *"I think this is done. Help me write an explicit freeze declaration with a real reopening threshold, then run a full procès on this one specific line before I touch anything else."*
12. **Production.** *"Generate the EPUB and print PDF from the frozen manuscript, and check that a scene-break marker didn't silently survive in one format and vanish in the other."*

And for a story that's part of a larger cycle sharing a world: *"A minor character from my last book — barely a page — is becoming the protagonist here. Walk me through handling the continuity properly before I start building her."*

## What's inside

```
novel-writing-methodology/
├── SKILL.md                    — entry point: constitution, evidence doctrine, phase table
└── references/
    ├── phases.md                — full spec per phase (entry/exit conditions, what to do/refuse)
    ├── protocols.md             — step-by-step protocols (cycle-continuity, reader-convergence,
    │                              montage/juxtaposition test, exploration, pilot test, crash-test,
    │                              blind inventory, character-voice/information/factual audits,
    │                              style-rule audit, title selection, back-cover test, procès,
    │                              exceptional revision)
    ├── reader-questions.md      — experience-first question bank for external readers
    └── registers.md             — templates for the registers this skill allows, each with its
                                    one-line justification (per "the one rule above the others")
└── evals/
    ├── evals.json                — test prompts used to validate the skill (see below)
    └── results.md                — scored with/without-skill comparisons
```

`SKILL.md` itself stays short by design (progressive disclosure): Claude reads it first, then follows pointers into the relevant `references/*.md` file only for the phase actually in play.

## Evaluation

`evals/evals.json` holds the test prompts used to check the skill actually changes behavior versus Claude's unassisted judgment; `evals/results.md` holds the scored outcomes. Five scenarios so far (research→architecture, scene diagnosis, reader-feedback triage after a near-freeze, character depth vs. biography, post-freeze correction discipline) were run with and without the skill and graded against explicit assertions. The skill made the largest difference on research→architecture (1/5 → 5/5), and real differences on character depth vs. biography (3/5 → 5/5) and post-freeze correction discipline (2/5 → 5/5), a moderate difference on scene diagnosis (3/4 → 4/4), and — across three differently-worded attempts — no measurable difference on reader-feedback triage, where Claude's default judgment was already close to what the skill prescribes. See `evals/results.md` for the full breakdown; it's a case study on where the skill's marginal value actually lives, not a uniform "always helps" story.

Evals 6-10 are **anti-evals**: they test whether the skill knows when *not* to engage its own machinery (a raw first-draft fragment, a contemplative scene, a vague unlocalized reader signal, a post-freeze "better idea" with no defect behind it, a factual "error" that's actually a character's deliberate, signaled mistake) — a methodology-heavy skill that always audits, always tests, always corrects is failing in the opposite direction from having no method at all. Results: no gap on 3 of 5 (baseline judgment was already sound), a large gap on the post-freeze "better idea" case (0/5 without skill vs. 5/5 with — unassisted judgment caved and called it "one of the few completely legitimate reasons to reopen finished work"), a real gap on the vague-signal case (3/5 vs. 5/5), and one new failure mode the skill introduced on its own (jargon leaking into user-facing text on the raw-fragment case) — fixed in `SKILL.md`. See `evals/results.md`.

Eval 9's 0/5-vs-5/5 result exposed a hidden assumption worth naming: it shows the skill enforces its own freeze policy far more consistently than unassisted judgment, not that the policy itself was correct as originally stated (absolute — no reopening without a defect, full stop). A follow-up **red-team eval** (11, not compliance-scored) constructed the opposite case — a frozen manuscript, a non-defect improvement that was actually tested rigorously (a stated claim, a blind A/B against the frozen version, a real non-split result) — to check whether the skill could say yes when a case had genuinely earned it. It couldn't, under the original absolute rule. **Phase 10 now has a third reopening path** (exceptional revision: a deliberately expensive but real route for a tested, non-defect improvement to earn reopening), and Constitution item 5 was reworded accordingly, alongside two other rules the same review flagged as overstated (foreclosure-as-inherently-weak in the exploration protocol; promises-must-always-be-paid in Phase 2). See `evals/results.md` for the full writeup, including the one thing the current eval 11 assertions don't yet catch: the with-skill response checked whether the test's claim and threshold were fixed *before* the results came in, and baseline didn't — a distinction worth its own eval.

A follow-up **Constitution red-team campaign** (evals 12-16) asked a sharper question than any single scenario: does each Constitution invariant still produce the best judgment in a case built specifically to make it expensive? Five items were attacked, one at a time, each with an independent judgment worked out from first principles *before* checking it against the skill, to avoid writing the expected answer from the rule itself. Two survived with scope clarifications only (item 4, "criteria before test"; item 8, "generation and selection are different operations"). Three required substantive revision: item 2 ("narrative experience before demonstration") took four passes to stop conflating narrative movement with one specific shape of it (sequential order) when cumulative and formal/perceptual demonstrations move differently; item 7 ("factual truth is non-negotiable") took five passes to separate licensed reconstruction from licensed counterfactual and to replace a single blunt truth-check with three orthogonal failure modes (contract deception, evidentiary fabrication, consequential distortion); item 3 ("observation before diagnosis") took one pass to stop regulating the chronological order a mind arrives at a hunch instead of the justificatory threshold an action actually needs. The cross-cutting finding — none of the three failed because the underlying value was wrong, each had been compressed into an operational proxy narrower than the value itself — is logged as an attack angle for future campaigns, not yet a new Constitution item. Full writeups, including the cases and the passes that failed along the way, in `evals/results.md`.

The cycle-continuity protocol, the reader-convergence protocol, the montage/juxtaposition test, and roughly fifteen smaller rules across `phases.md` and `registers.md` were added later from a different kind of evidence than the evals above: a structured review of a completed 8-book short-story cycle written under an earlier version of this method — first its genèse (design) notes, then, separately, its raw git commit history. Neither pass is a scored with/without-skill eval; both are logged honestly as provisionally justified rather than eval-confirmed, with the specific evidence for each addition (independent convergence across unrelated books, in most cases) stated in the provenance notes at the end of `evals/results.md`.

## License

MIT — see `LICENSE`.

## Origin

The methodology's phase structure, the literary-evidence doctrine, and the post-freeze "procès" protocol were developed and stress-tested while writing an actual novel — a French-language literary novel about a young woman's crisis of trust in her upbringing, built around a documented factual investigation. No content, characters, or specifics from that novel appear in this skill; only the working method does.
