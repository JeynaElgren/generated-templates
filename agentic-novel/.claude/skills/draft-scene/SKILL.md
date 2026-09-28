---
name: draft-scene
description: Draft the prose for one scene from its scene card, following CLAUDE.md's retrieval protocol and information-discipline rules, then propose ledger updates.
argument-hint: <scene id, e.g. ch03-s02>
---

# Draft scene

Draft scene `$ARGUMENTS`.

## Before writing

1. Read `story/style-guide.md` in full.
2. Read `scenes/$ARGUMENTS.md`. If it's missing or thin (no purpose, no
   information control), stop and suggest running `/scene-brief` first.
3. Load the context pack, following CLAUDE.md §2: Snapshots first, then only the
   sections this scene needs. For a POV character, always load *Voice*,
   *Behaviour & tells*, *Knowledge* and "What they notice first". For other
   speaking characters, load *Voice* and *Behaviour & tells*.
4. Read the last ~50 lines of the previous scene in `manuscript/`, and the
   *Physical state tracker* in `ledgers/continuity.md`.
5. Make yourself a private checklist (don't write it into any file):
   - Reveal IDs allowed here, and everything that must stay hidden.
   - Setups to plant or fire.
   - What the POV character knows, doesn't know and wrongly believes.

## While writing

Follow CLAUDE.md §3 (the iceberg rule) strictly. The main points:
- POV lock and the familiarity filter.
- The detail budget: 1–3 details on first appearance, then only changes.
- Behaviour over labels; subtext over statement; no "as you know" dialogue.
- Nothing [Hidden] and nothing unrevealed unless its ID is on the card.
- Nothing from the style guide's banned list.
- End on a turn, a question or an image. Never on a summary of what the scene
  meant.

Match the target length in the style guide. Mark any canon you had to invent
as `<!-- PROPOSED: … -->`.

## After writing

1. Save to `manuscript/$ARGUMENTS.md` (prose only).
2. On the scene card: set `status: drafted` and fill in *Established on the
   page*.
3. Silently run through the `/continuity-check` criteria against your own draft
   and fix anything you find.
4. Report back briefly:
   - Word count.
   - Reveals made, setups planted or fired, threads touched (IDs).
   - `PROPOSED` items (also add them to `notes/inbox.md`).
   - Proposed ledger updates. Apply them only if the author has said to, or
     run `/update-ledgers`.
