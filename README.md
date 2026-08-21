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

## What's inside

```
novel-writing-methodology/
├── SKILL.md                    — entry point: constitution, evidence doctrine, phase table
└── references/
    ├── phases.md                — full spec per phase (entry/exit conditions, what to do/refuse)
    ├── protocols.md             — step-by-step protocols (pilot test, crash-test, blind inventory,
    │                              character-voice audit, information audit, factual audit, procès)
    ├── reader-questions.md      — experience-first question bank for external readers
    └── registers.md             — templates for the registers this skill allows, each with its
                                    one-line justification (per "the one rule above the others")
└── evals/
    └── evals.json                — test prompts used to validate the skill (see below)
```

`SKILL.md` itself stays short by design (progressive disclosure): Claude reads it first, then follows pointers into the relevant `references/*.md` file only for the phase actually in play.

## Evaluation

`evals/evals.json` holds the test prompts used to check the skill actually changes behavior versus Claude's unassisted judgment; `evals/results.md` holds the scored outcomes. Four scenarios (research→architecture, scene diagnosis, reader-feedback triage after a near-freeze, character depth vs. biography) were run with and without the skill and graded against explicit assertions. The skill made the largest difference on research→architecture (1/5 → 5/5) and a real difference on character depth vs. biography (3/5 → 5/5, where the unassisted response reframed toward present-tense wants but never named self-deception/concealment or produced an explicit pressure test), a moderate difference on scene diagnosis (3/4 → 4/4), and — across three differently-worded attempts — no measurable difference on reader-feedback triage, where Claude's default judgment was already close to what the skill prescribes. See `evals/results.md` for the full breakdown; it's a case study on where the skill's marginal value actually lives, not a uniform "always helps" story.

## License

*(not yet chosen — add one before treating this as open for reuse by others)*

## Origin

The methodology's phase structure, the literary-evidence doctrine, and the post-freeze "procès" protocol were developed and stress-tested while writing an actual novel — a French-language literary novel about a young woman's crisis of trust in her upbringing, built around a documented factual investigation. No content, characters, or specifics from that novel appear in this skill; only the working method does.
