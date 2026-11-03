---
name: advise
description: Answer a marketing-leadership question grounded in the owner's own playbooks, principles and library first, then trusted live sources, with citations. Invoke with /advise <question> [workspace:<company>], or /advise setup to change its settings.
disable-model-invocation: true
---

## 0. First run

1. Read `settings.md` at the vault root. If it has no `## Profile` section, tell the owner to run `/setup` first, then stop. `## Profile`, `## Layers` and `## Sources` apply throughout this skill.
2. If `settings.md` has no `## /advise` section, or `$ARGUMENTS` is `setup`, ask these in **one** message, numbered, each with its default in brackets, so the owner can reply "defaults":
   1. **Default workspace** to read when you don't name one (only if Layers turns employer workspaces on). [none: ask for context when it matters]
   2. **When the answer depends on context you haven't given** (stage, ACV, motion): ask in one line first, or answer with stated assumptions? [ask in one line]
   3. **Answer length:** *short* (the answer and sources only) or *standard* (answer, reasoning, disagreements, sources)? [standard]
   4. **Caveats to always flag:** benchmarks from contexts unlike yours, given your region and business model in Profile. [flag US venture-backed SaaS benchmarks before applying them to any other region, funding model or business model]
3. Write the answers as a short bullet list under `## /advise` in `settings.md` (add it at the end; replace it if re-running setup). Confirm in one line. Then answer the question, or stop if the owner only ran `setup`.

Answer the question in $ARGUMENTS.

**Context.** If `workspace:<company>` is given, or a default workspace is set in settings, read `workspaces/<company>/context.md` and judge every recommendation against that stage, ACV and motion. If Layers turns workspaces off, or there's no workspace, handle missing context the way settings say: ask for stage, ACV and motion in one line if the answer depends on them, or answer and state your assumptions. Don't silently assume.

**Retrieval order — stop going wider once the answer is well grounded:**
1. `playbooks/` and `principles/`: the synthesis and the owner's own view. Notes with `example: true` are samples shipped with the kit: you may use them, but say so (e.g. "the example playbook that came with the kit, built on three sources"). These outrank everything below. When a playbook has a **What changes the answer** section, establish those factors first (ask in one short message, or read them from the workspace). Then give the recipes that fit, not the whole playbook.
2. `library/`, `case-studies/` and `swipe/`: search all three by tag and keyword.
   - In the library, prefer notes with a "My take", and `tier: canon` over `tier: web`. When you lean on a `tier: web` source, say it's outside the trusted sources. If a note has `corporate_data: true`, say it's a big-company study before applying it to the owner's context.
   - **Case studies** are evidence that a recipe works in the real world. Cite them whenever one matches, saying they're web-researched, outside the canon, and giving their evidence labels.
   - **Swipe items** (search by format and technique) when the question is about creative or execution.
3. Live trusted sources: the connectors listed in `settings.md` under Sources, for the sources they cover; then web search restricted to the domains in `canon/_index.md` (WebSearch with `allowed_domains` set to those domains, or Exa with one `site:<domain>` query per domain; drop any result from another domain).
4. General web, **only if 1–3 come up thin**. Then open the answer with:
   > ⚠️ Outside the trusted sources — this draws on general web search.

**For a big or high-stakes question,** or one where the vault comes up thin, suggest `/advise-deep`, which adds full web research and tailors the answer to the owner's company and role. Say how it gets that context: it reads `workspaces/<company>/context.md` if they add `workspace:<company>`, otherwise it asks them one short set of numbered questions first. They don't need to pack the context into the prompt.

**Answer shape** (trim to the answer and sources if settings say *short*):
- **The answer first**, in 2–4 sentences, tailored to the context.
- **The reasoning**: the playbook or sources it rests on.
- **Where the experts disagree**, if they do, and which way this context tips it.
- **Sources**: clickable links to vault notes (see below) and URLs for live sources.

**Any test, pilot or experiment you recommend says how to judge it**, whatever the length setting: what to measure, against what comparison, over what period, and what result counts as a pass. Separate the early signals (weeks) from the lagging results (months), so a pass on one isn't mistaken for the other. If the sources don't say, say that, rather than leaving a gap.

**Freshness rules (read `freshness.md`). These are the slip-up guards:**
- **Cite like the playbooks:** the source's full name, linked to its note, with no date on the citation itself. **In chat, wikilinks aren't clickable**, so use a markdown link to the file's path, with spaces as `%20` and parentheses as `%28`/`%29`, e.g. `[Jane Example](library/Seed-Stage%20Positioning%20-%20Jane%20Example.md)`. Playbooks the same way: `[positioning](playbooks/positioning.md)`. Wikilinks (`[[note|Jane Example]]`) are only for text written into vault files.
- Every benchmark, number, platform behaviour or tool recommendation in an answer carries its date, in the form *"CAC payback of 12–18 months, as of 2024-02 (Jane Example)"*. No undated specifics, ever.
- From a note that's `aging`: use the principles freely. Quote a specific only with *"as of <date>, not re-verified"*. For `volatile` topics (AI visibility, AEO, platform algorithms, tools), check a live source before answering.
- From a note that's `superseded` or `expired`: never quote its specifics. Follow `superseded_by`.
- When old and new sources conflict, the newer one wins on specifics unless the older one carries `re-verified`. Say that you made that call.
- If the best available specific is past its window and can't be re-verified, say so plainly rather than presenting it as current.

**Rules:**
- Flag the caveats set in settings (by default, US venture-backed SaaS benchmarks) before applying a benchmark to a different region, funding model or business model from the owner's Profile.
- If the answer contradicts a `principles/` note, say so plainly. Don't quietly pick one.
- Never read any vault listed in `settings.md` under Layers → Never read.
- Never copy workspace data into a portable file. If the answer surfaces a reusable lesson, offer to add the *lesson* to a playbook.
