---
name: scene-brief
description: Build or complete a scene card in scenes/ and assemble the minimal context pack (which bible sections and ledger rows) needed to draft it. Use before drafting any scene that lacks a complete card.
argument-hint: <scene id, e.g. ch03-s02, or a short description>
---

# Scene brief

Build the brief for scene `$ARGUMENTS`.

1. If `scenes/<id>.md` exists, read it. If not, copy `scenes/_TEMPLATE.md` to it.
   For a description with no id, find the right slot in `story/outline.md` and
   propose an id.
2. Read `story/outline.md` (this scene's row, plus its neighbours) and the
   previous scene's card, if there is one.
3. Fill in what the outline and neighbours already determine: POV, location,
   cast, story points, rough beats.
4. Check the ledgers:
   - `ledgers/reveals.md`: which reveals are planned here or overdue? Which
     facts must stay hidden?
   - `ledgers/setups-payoffs.md`: anything to plant, reinforce or fire here?
   - `ledgers/threads.md`: which open threads should this scene touch?
   Fill in *Information control* with the IDs.
5. Read only the **Snapshot** of each cast member, the location and any items.
   Use them to suggest *Subtext* and *Sensory anchors*.
6. Leave anything that's the author's call (outcome, key choices, reveals not
   in the outline) as a question under *Notes*. Don't decide it.
7. Set `status: carded`.

Finish by showing the **context pack**: a short list of the exact files and
sections `/draft-scene` should load. Then list any open questions for the
author.
