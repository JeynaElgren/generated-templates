# Agentic novel workspace

A template for writing a novel with an AI assistant (built for Claude Code, but
it's plain Markdown and works with anything, including no assistant at all).

The idea: keep a **deep reference** (story bible) on everyone and everything, and
let the assistant **fetch only what each scene needs**. Strict rules keep that
depth underwater, so the prose shows instead of tells and subtext beats
omniscience.

## Getting started

1. Copy this folder into a new repo (or use the new repo as a template).
2. Fill in `story/premise.md` and `story/style-guide.md` first. Paste some of your
   own prose into *Voice samples*. It helps more than any rule does.
3. Create your main characters and locations: copy the `_TEMPLATE.md` in each
   `bible/` folder, or run `/new-entry character Mara Voss` and let the
   assistant interview you.
4. Sketch `story/outline.md`, especially the *Required story points*.
5. Add secrets to `ledgers/reveals.md` and planned Chekhov's guns to
   `ledgers/setups-payoffs.md` as you think of them.
6. Per scene: `/scene-brief ch01-s01` → `/draft-scene ch01-s01` →
   revise → `/continuity-check ch01-s01` → `/update-ledgers ch01-s01`.

You don't have to fill everything in. Empty fields are fine, and the assistant
is told not to invent answers for them.

## Layout

```
CLAUDE.md                 rules for the assistant (retrieval, show-don't-tell, canon limits)
.claude/skills/           slash commands: scene-brief, draft-scene, continuity-check,
                          update-ledgers, new-entry
story/
  premise.md              logline, genre promises, themes, tone, ending
  style-guide.md          POV, tense, prose rules, banned phrases, voice samples
  outline.md              structure, required story points, scene list
  timeline.md             backstory + in-story chronology
bible/                    AUTHOR'S REFERENCE (intent, mostly never shown verbatim)
  characters/  locations/  factions/  items/  lore/   (each with a _TEMPLATE.md)
  relationships.md        the web between characters
  glossary.md             invented terms, spellings
scenes/                   scene cards: the brief for each scene (chNN-sNN.md)
manuscript/               the prose, one file per scene (chNN-sNN.md)
ledgers/                  WHAT'S ACTUALLY ON THE PAGE
  reveals.md              who knows what, and when the reader learns it
  setups-payoffs.md       Chekhov's guns: planted → reinforced → fired
  threads.md              open questions and promises to the reader
  continuity.md           stated facts + current physical state
notes/inbox.md            ideas, questions, proposals, conflicts
```

## How it avoids info-dumps

- **Reveal tiers.** Every bible field is tagged `[Surface]` (anyone would notice),
  `[Earned]` (learned over time) or `[Hidden]` (secret). Hidden material only goes
  on the page when a scene card explicitly allows that reveal ID.
- **Reveals ledger.** It tracks what the reader and each character know, so
  the assistant can't state something before it's been earned, and dramatic
  irony is deliberate.
- **Knowledge fields.** Characters have *knows / doesn't know / wrongly believes*.
  POV narration is locked to them, false beliefs included.
- **Tells and voice.** Characters have *how anger/fear/lying/affection leaks out*
  and *what they avoid saying*: raw material for showing and for subtext.
- **Detail budget and familiarity filter.** 1–3 details on first appearance,
  then only changes. Familiar places aren't catalogued.
- **Snapshots first.** Each entry has a short summary at the top. The assistant
  reads that and pulls deeper sections only when the scene needs them.
- **Bible vs. page.** The bible is intent; the continuity ledger is what was
  actually written. Conflicts get flagged, never silently "fixed".

## Using it without an assistant

Everything is plain Markdown with guidance in `<!-- comments -->`, so the
templates work as a regular writing bible. The ledgers are especially handy by
hand: `reveals.md` and `setups-payoffs.md` catch most "wait, when did the reader
learn that?" problems in revision.

## Conventions

- **IDs:** kebab-case for bible entries (`mara-voss`), `chNN-sNN` for scenes,
  `SP-01` story points, `R-001` reveals, `G-001` setups, `T-001` threads.
- **Filenames** match IDs.
- `<!-- PROPOSED: … -->` in prose = canon the assistant invented and the author
  hasn't approved yet (also listed in `notes/inbox.md`).
