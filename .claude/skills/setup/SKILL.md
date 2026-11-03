---
name: setup
description: First-time setup interview for the Marketing Leadership OS. Learns who the owner is, who they serve, which sources they trust and how they work, then writes settings.md, their first trusted-source notes and their tag list. Run once at the start, and again any time to change the answers. Invoke with /setup.
disable-model-invocation: true
---

Set up this vault for its owner through a short interview, then write what you learn into the vault. Read `CLAUDE.md`, `settings.md`, `taxonomy.md` and `canon/_index.md` first.

**If `settings.md` already has a `## Profile` section,** this is a re-run. Show the current answers in a short summary and ask which round to redo (1–4, or all). Only rewrite what changes.

## How to interview

- **Four short rounds, one message each.** Never more than four questions in a message.
- **Number the questions** and give a sensible default in brackets, so the owner can reply "defaults" or answer only some.
- Keep it conversational and quick: the whole interview should take under ten minutes.
- If an answer is unclear, make a reasonable assumption, say what it is, and move on. Don't add extra rounds.

## Round 1: You

1. What's your name, and what should Claude call you?
2. What's your role and remit? [e.g. VP Marketing, owning demand gen, product marketing and brand]
3. Who should this vault serve: what kind of company and leader? This becomes the relevance bar for everything you save. [marketing leaders at B2B tech start-ups and scale-ups]
4. Where do you work, and what kind of business? This sets which benchmarks get flagged before they're applied. [e.g. UK, venture-backed SaaS]

## Round 2: Trusted sources

1. Name 3–10 people or publications whose thinking you rely on most: newsletters, blogs, podcasts, books' authors. Fewer is fine to start; you'll add more as you go. [if none come to mind, ask for suggestions]
2. Which of those are paid subscriptions? [none]
3. Any connectors you've added to Claude that can read them, such as a newsletter's own connector or a search tool? Most people answer "none", and Claude uses web search. [none]

If they ask for suggestions, offer 6–8 well-regarded, currently active operators who write for the audience in round 1, each with one line on their lens, and let the owner pick. Never add a source they didn't choose.

## Round 3: Topics

Show the current tag list from `taxonomy.md` as one compact line.

1. Any tags to drop, rename or add for your work? (Later, a new tag needs three notes to use it; at setup, add what you expect to need.) [keep as is]
2. Which 2–3 recurring jobs would you most like playbooks for first? [e.g. annual planning, board meetings, the first 90 days]

## Round 4: How you work

1. Will you keep context about your current employer in this vault (`workspaces/`)? [yes; check your employer's AI policy first]
2. Is there any other vault or folder Claude must never read from here, such as a personal or job-search vault? [none]
3. How will you capture things: Web Clipper in the browser, PDFs, screenshots, email to yourself? [Web Clipper and PDFs]
4. Keep the example notes that came with the kit for now, or delete them? [keep until I've added my own]

## Write it into the vault

1. **`settings.md`**: keep the intro, replace the `<!-- Run /setup … -->` comment, and write three sections as short bullet lists:
   - `## Profile`: name, role and remit, Audience (the relevance bar, word for word), region and business context.
   - `## Layers`: employer workspaces yes/no; Never read: the paths from round 4, or "none".
   - `## Sources`: trusted sources (names), paid subscriptions, connectors and tools, capture channels.
   - Under `## Profile`, also add `Playbooks wanted first:` with the jobs from round 3, in order. `/build-playbook` offers these when run without a job.
   Leave every `## /<skill>` section alone: each skill writes its own.
2. **Trusted sources**: for each source from round 2, write `canon/<Name>.md` in the structure from `canon/_index.md` and add a row to its table.
   - **Verify every link** with a web search or fetch before writing it. Leave out any you can't verify.
   - Add `subscription: paid` for paid sources.
   - **If a source already has an example note** (for example `canon/April Dunford.md`), make it the owner's own: remove `example: true` and the example callout from the note, and "(example)" from its index row. Don't write a second note.
   - Write honest blind spots. If you know too little about a source to write them, say "to be filled in as the library grows".
   - Remove the example row from the table if the owner chose to delete the examples.
3. **`taxonomy.md`**: apply round 3's changes. A new tag needs a one-line "Covers" description.
4. **`CLAUDE.md`**: change nothing, unless the owner asks. It reads `settings.md` for everything personal.
5. **Examples**: if the owner chose to delete them, delete every note with `example: true` in its frontmatter and its index lines, then check that no wikilink points at a deleted note. That includes notes you kept and made the owner's own, such as `canon/April Dunford.md`, which links the example playbook: remove or reword those links.
6. **Workspaces**: if they said yes in round 4, tell them to run `/workspace-setup <company>` next, after checking their employer's AI policy.

## Finish

Summarise in a few lines what you wrote. Then give the next three steps:

1. Install the Web Clipper templates (`setup/web-clipper/README.md`) and clip three pieces you've read recently.
2. Run `/process-inbox`.
3. Run `/build-playbook <job>` for the first job they named in round 3.

Mention that every other skill asks a few quick questions of its own the first time it runs, and that `/setup` can be run again at any time.
