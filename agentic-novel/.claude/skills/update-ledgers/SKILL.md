---
name: update-ledgers
description: Sync ledgers (continuity, reveals, setups-payoffs, threads), the timeline and the outline status with what a drafted or revised scene actually put on the page.
argument-hint: <scene id, e.g. ch03-s02>
---

# Update ledgers

Sync the ledgers with `manuscript/$ARGUMENTS.md`. Record only what is
**actually on the page**, not what the scene card planned.

1. Read the prose and its scene card.
2. **`ledgers/continuity.md`:** add every concrete fact that could recur (names,
   physical details, objects, places, stated history). Update the *Physical
   state tracker*: who is where, holding what, injured how.
3. **`ledgers/reveals.md`:** fill in *Reader knows since* for each reveal that
   happened, add hints to *Hinted in*, and update *Characters who know*. If the
   prose reveals something by accident, flag it instead of recording it.
4. **`ledgers/setups-payoffs.md`:** update *Planted in*, *Reinforced in* and
   *Fired in*, and the status. Add new setup-like details as `candidate`.
5. **`ledgers/threads.md`:** add questions the scene raised and mark answered
   ones.
6. **`story/timeline.md`:** add or adjust this scene's row.
7. **`story/outline.md`:** update this scene's status, and tick story points it
   completes.
8. **`bible/relationships.md`:** log any relationship shift.
9. Update `status` in bible frontmatter (alive/dead/…) and `holder` on items,
   if they changed. These are the only bible fields you may change without
   asking.

Make the edits, then list what changed per file in a few lines. Put conflicts
you found in `notes/inbox.md`, under *Conflicts*.
