---
name: trusted-sources-review
description: Regular review of the trusted sources (the canon). Finds web creators who keep proving their worth and should join, and trusted sources that have stopped earning their place, with the evidence for each. The owner decides. Invoke with /trusted-sources-review, or /trusted-sources-review setup to change its settings.
disable-model-invocation: true
---

## 0. First run

1. Read `settings.md` at the vault root. If it has no `## Profile` section, tell the owner to run `/setup` first, then stop. `## Profile` and `## Sources` apply throughout this skill.
2. If `settings.md` has no `## /trusted-sources-review` section, or `$ARGUMENTS` is `setup`, ask these in **one** message, numbered, each with its default in brackets, so the owner can reply "defaults":
   1. **How often will you run this?** [quarterly]
   2. **The bar to propose adding a creator:** how many of the three signals (enough notes across playbooks, relied on by *agree* items, clipped by you) must they meet, and how many notes? [2 of 3 signals; 4+ notes across 2+ playbooks]
   3. **Recency window:** how long since their last relevant piece before a creator can't be added, or a trusted source gets flagged for review? [18 months]
   4. **Vendor-tied creators** (they sell what they write about): allowed if their material is the best on the topic and the tie is named, or never? [allowed, named]
3. Write the answers as a short bullet list under `## /trusted-sources-review` in `settings.md` (add it at the end; replace it if re-running setup), plus a `last run:` line left blank. Confirm in one line. Then carry on with the review, or stop if the owner only ran `setup`.

Review the trusted sources. Read `canon/_index.md` (its structure and list), `settings.md` (the relevance bar in Profile → Audience) and `playbooks/_index.md` first. If the `last run:` date in settings is more recent than the cadence set there, say so in one line and ask whether to carry on. **Only the owner adds or removes a trusted source.** This skill gathers evidence and proposes; it changes nothing until they say yes.

## 1. Gather the evidence (read-only)

**For each creator behind `tier: web` notes in `library/`** (group by author; treat a show, newsletter or company as one creator):
- **Notes:** how many, and how many distinct pieces.
- **Use:** how many playbooks cite them, and how many *Where the sources agree* items rely on them.
- **The owner's picks:** how many of their notes are `origin: clip`. The owner's own clips are the strongest signal.
- **Recency:** their newest piece's `published` date. Are they still active?
- **Fit:** do they pass the relevance bar? Are they an operator who has done the job? Any vendor tie (they sell what they write about)? Any `corporate_data` notes?
- **Mentions:** whether they're named under "Canon candidates" in any playbook's Coverage section.

**For each current trusted source** in `canon/`:
- **Notes:** library notes and playbook citations.
- **Recency:** their newest piece in the library, and whether they're still publishing.
- **Freshness:** the share of their notes that are `aging` or `superseded`.
- **Fit:** whether their recent work still passes the relevance bar.

## 2. Apply the bar

The thresholds below are the defaults; use the ones set in settings.

**Propose adding** a creator who meets at least two of these (or the number set in settings):
- 4+ notes, cited across 2+ playbooks
- relied on by 2+ *agree* items
- 2+ pieces the owner clipped themselves

They must also:
- have published within the recency window set in settings (default 18 months)
- pass the relevance bar
- write mostly from operating experience, not from selling a product (a vendor tie is allowed only if settings allow it, their material is the best on the topic, and the tie is named)

**Watch list:** creators close to the bar. One more strong piece or playbook and they'd qualify.

**Propose reviewing a trusted source** if they:
- are cited in no playbook, or
- have published nothing relevant within the recency window, or
- have mostly aging notes with nothing newer, or
- have drifted off the relevance bar.

Reviewing doesn't mean removing: some trusted sources are rarely cited but still the best on their topic. Say which.

## 3. Show the owner one table

| Creator | Proposal (add / watch / review) | Evidence (notes, playbooks, agree items, clips, last piece) | Fit and caveats |
|---|---|---|---|

Order it by strength of evidence. Then wait for their decisions, in one exchange.

## 4. Apply what they approve

**Adding a creator:**
1. **Write `canon/<Name>.md`,** following the note structure in `canon/_index.md`. Use only **verified** links (search for their profiles and check each one), and include honest blind spots. If they're a paid source, fill in `subscription:` and suggest the owner adds them under Sources in `settings.md`.
2. **Add a row** to the table in `canon/_index.md`.
3. **Re-tier their library notes:** `tier: canon`, `author: ["[[Name]]"]`. For guest appearances, keep the host as `contributor`.
4. **Playbook frontmatter:** in every playbook that cites them, move them from `sources_web` to `sources`. Citations need no change: each note's `tier` records whether it's a trusted source.

**Removing or demoting a creator:**
1. **Move** their canon note to `archive/` and remove their row from the index.
2. **Re-tier their notes** to `tier: web`, and make `author` plain text.
3. **Playbook frontmatter:** move them from `sources` to `sources_web`. Never delete library notes.

Then check that every wikilink resolves, set `last run:` under `## /trusted-sources-review` in `settings.md` to today's date, and report what changed.
