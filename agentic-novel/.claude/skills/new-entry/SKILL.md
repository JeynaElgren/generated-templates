---
name: new-entry
description: Create a new bible entry (character, location, faction, item, lore) from its template, either from the author's notes or by interviewing the author.
argument-hint: <character|location|faction|item|lore> <name> [notes]
---

# New bible entry

Create an entry for `$ARGUMENTS`.

1. Work out the type and the name. Make an `id` in kebab-case (e.g. `mara-voss`)
   and check that `bible/<type>s/<id>.md` doesn't already exist, including
   under an alias (`grep -ril`).
2. Copy `bible/<type>s/_TEMPLATE.md` to `bible/<type>s/<id>.md` and fill in the
   frontmatter.
3. Fill in what the author gave you: notes, pasted text, earlier conversation.
   Check `notes/inbox.md` and the manuscript for existing mentions, and pull in
   what's **already on the page** (cite the scene ids).
4. Don't invent content for the empty fields. Instead, interview the author:
   ask about **5–8 of the most useful fields at a time**, starting with the
   Snapshot. For characters, next ask about *Voice*, *Behaviour & tells* and
   *Knowledge*, since they matter most for drafting. Offer 2–3 concrete options
   when the author seems unsure, but let them pick.
5. Tag fields with reveal tiers ([Surface]/[Earned]/[Hidden]). Suggest a tier
   when it's obvious, and ask when it isn't.
6. Add every secret to `ledgers/reveals.md` with a new `R-` ID, and put the ID
   in the entry.
7. Delete template guidance comments from fields that are filled in. Leave
   fields the author wants to fill later blank.

Stop when the author says it's enough. An entry can grow over time.
