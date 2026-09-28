---
name: continuity-check
description: Review manuscript prose for continuity errors, POV breaks, premature reveals, info dumps, voice drift and style-guide violations. Reports issues with line references; does not rewrite.
argument-hint: <scene id or manuscript file path>
---

# Continuity check

Review `$ARGUMENTS`. **Report only. Don't edit the prose** unless the author
asks.

Load the scene card, the style guide, and the bible entries and ledger rows for
every entity that appears. Then check:

1. **Continuity:** contradictions with `ledgers/continuity.md`, the physical
   state tracker, `story/timeline.md` (time of day, travel times, injuries) or
   the previous scene.
2. **Premature reveals:** any fact that is [Hidden] or [Earned] in the bible,
   whose reveal ID isn't on this scene card and isn't marked as known to the
   reader in `ledgers/reveals.md`. Include indirect leaks, e.g. narration that
   only makes sense if the reader already knows the secret.
3. **POV breaks:** the narration knows something the POV character couldn't
   (someone else's thoughts stated as fact, events out of sight, the POV
   character's own appearance described).
4. **Knowledge errors:** a character acts on information they don't have yet.
5. **Info dumps:** more than ~3 consecutive sentences of exposition; inventory
   descriptions; "as you know" dialogue; lore explained that's listed under
   *Never explained on the page*.
6. **Show-then-tell:** a behaviour followed by a label for the same emotion.
   Also subtext that gets explained.
7. **Voice drift:** dialogue that doesn't match the speaker's *Voice* entry, or
   two characters who sound interchangeable.
8. **Style guide:** banned phrases, the wrong tense or POV, dialogue-tag rules,
   length targets.
9. **Setups:** anything that reads like a new Chekhov's gun but isn't in the
   ledger; setups from the card that didn't get planted.
10. **Bible drift:** anything on the page that contradicts the bible. Note which
    side is probably right, but let the author decide.

Output a list grouped by category. For each issue give the line or a short
quote, what's wrong, and a one-line suggested fix. If a category has nothing,
say "none". End with the 3 most important fixes.
