# CLAUDE.md — Marketing Leadership OS

The owner's personal marketing-leadership operating system: a library of the best thinking they've read, the playbooks distilled from it, real-world case studies, a swipe file of great marketing, and their own principles. **It's built to outlive any single job.** It goes with them into every role and keeps compounding.

Captured with Obsidian Web Clipper, queried and maintained with Claude Code. **Read `settings.md` before doing anything.** It holds the owner's profile, their relevance bar, and how each skill should behave for them. If it has no `## Profile` section, ask the owner to run `/setup` first.

## 🔑 The three-layer rule — read before writing anything

| Layer | Lives in | Owner | Leaves with them? | Can ever be public? |
|---|---|---|---|---|
| **Portable** | `canon/` `library/` `playbooks/` `case-studies/` `swipe/` `principles/` `.claude/skills/` | The owner | Yes, forever | Only what they choose to share |
| **Employer workspace** | `workspaces/<company>/` (git-ignored) | **The employer** | **No.** Deleted on exit | Never |
| **Private** | Any other vault or folder listed in `settings.md` under Layers → Never read | The owner | n/a | Never |

1. **Employer data never leaves `workspaces/`.** No company ARR, pipeline, customer names, plans or internal metrics in any portable file, not even "anonymised" figures copied from a workspace. A playbook may learn a *lesson* from a workspace; it may not carry the *data*. Check the employer's AI policy before creating a workspace: the right home for their context may be their sanctioned AI tool, not this vault.
2. **Never read anything listed under Layers → Never read** in `settings.md`. Dependencies run one way.
3. **Nothing paywalled goes public.** `library/` may hold clips of paid newsletters for private use. If the owner ever shares this vault, share the structure, never that content.

## 💳 Paid sources

**Never bulk-download or scrape a paid archive**, whether the owner is subscribed now or not. Paid access is personal reading while subscribed; archiving everything to keep after cancelling is what the paywall exists to prevent.

- **Clip what the owner actually reads**, one piece at a time, for private use.
- **The durable asset is the synthesis, not the text.** Every library note's takeaways must stand on their own if the full text were deleted.
- **Claude may research on the owner's behalf.** When building a playbook (`/build-playbook`), Claude reads every trusted-source piece relevant to that job, plus best-in-class sources from the wider web, and writes library notes marked `origin: research` (with `tier: canon` or `tier: web`). Notes the owner clipped are `origin: clip`. For paid sources, research notes hold **only the synthesis and a link, never the full text**. Research is per topic, never a sweep of a creator's whole archive.
- **Before cancelling a subscription,** the owner does a manual harvest pass: they clip the 10–20 pieces they'd genuinely miss. Each paid creator's trusted-source note carries a `subscription:` field so this isn't forgotten.

## Folders

- `inbox/` — Web Clipper drops new clips here; PDFs go in `inbox/pdfs/` and swipe examples in `inbox/swipe/`. Run `/process-inbox` or `/process-swipe`.
- `attachments/` — source PDFs kept after processing, linked from their library note. Git-ignored, except `attachments/swipe/` (screenshots of public marketing only).
- `archive/` — source files triaged as drop, kept out of the working vault. Never processed or cited. Git-ignored. **Employer files never go here.**
- `library/` — processed clips. One note per piece; the same work in another format (blog, post, thread, repost) is merged into one note, with the most complete original as its source. Flat folder, organised by `tags` and `author`.
- `canon/` — the **trusted sources**: one note per creator (`April Dunford.md`): why they matter, their lens, their blind spots. **An index of why, not an archive of what.** Title Case filenames so Web Clipper's `[[author]]` links resolve. Review quarterly with `/trusted-sources-review`; only the owner adds or removes a trusted source.
- `playbooks/` — one note per recurring marketing-leadership job, built with `/build-playbook` from the trusted sources plus the best of the wider web. Synthesis across sources: what changes the answer, where sources agree and disagree, and *If X, then Y* recipes. **No verdicts on the owner's behalf**: they apply their own judgement to the situation in front of them. Format in `playbooks/_index.md`. This is the layer that compounds.
- `case-studies/` — real-world tactical guides: who did something brilliantly, and exactly how. **Researched from the open web, outside the trusted sources**, so every claim is cited and results are labelled verified, claimed or reported. Write them with `/research-case-study`.
- `swipe/` — great marketing the owner has saved, one note per item, categorised by format and technique. **Only the owner's picks**; Claude categorises, never curates. Process with `/process-swipe`.
- `principles/` — the owner's own point of view. **Only the owner writes or confirms these.** Claude may draft from their stated views, marked `status: draft`, never promoted on their behalf.
- `workspaces/` — employer context, set up with `/workspace-setup`. Git-ignored except `_index.md`.
- `Home.md` and `_views/` — the Obsidian front door, built on Bases views.
- `setup/` — tool configs (Web Clipper templates).
- `settings.md` — the owner's profile and per-skill preferences, written by `/setup` and each skill's first-run interview.
- `taxonomy.md` — the fixed tag list. Every tag in `library/` must come from it.
- `freshness.md` — **how knowledge ages.** Claims split into durable principles and dated, perishable numbers and tactics, each with a review window. Read it before writing or citing any benchmark, tactic or tool advice.

## Clip lifecycle

`inbox/` (status: inbox) → `/process-inbox` checks metadata, writes the takeaways and tags, links the creator → `library/` (status: library) → when a tag has 3+ library notes and no playbook, suggest one.

**"My take" is optional and added over time.** The owner annotates the pieces that matter to them. Don't ask for takes during processing. **Never write one for them.** A note with a take carries more weight than one without.

## ⏳ Never serve stale specifics as current

Every benchmark, number, platform behaviour or tool recommendation carries an `(as of YYYY-MM)` date wherever it appears: library notes, playbooks and answers. Citations themselves carry no date: the library note holds it. Past its `review_by`, a specific is quoted only with an explicit date caveat or after re-verification. Superseded or expired specifics are never quoted. Rules in `freshness.md`; run `/freshness-review` monthly.

## Answering questions

Use `/advise` for quick, grounded answers, and `/advise-deep` for big or nuanced questions (it gathers company and personal context and runs deep web research). Retrieval order: playbooks → principles → library → trusted sources → live sources (connectors in `settings.md`, then web search restricted to trusted-source domains: WebSearch with `allowed_domains`, or one `site:` query per domain) → general web, **with an explicit warning that it's outside the trusted sources**. Case studies and swipe items can be offered as examples at any point, with case studies flagged as outside the trusted sources. Always cite. Flag benchmarks from a different context (for example US venture-backed SaaS) before applying them to the owner's region or business model in `settings.md`.

In chat, cite vault notes as markdown links to the file path (spaces as `%20`) so they're clickable; use `[[wikilinks]]` only inside vault files.

## Relevance

The vault serves the audience in `settings.md` (Profile → Audience). Leave out material that doesn't serve it. Big-company studies are used only where nothing closer exists, and their library notes carry `corporate_data: true`.

## Vault hygiene

Link creators, playbooks and principles with `[[wikilinks]]`. Don't invent links to files that don't exist: `author` is a wikilink only for creators with a note in `canon/`. Keep library notes short: one over ~600 words is two notes. The limit counts the takeaways and Notes, not a clipped `## Content` section kept below them. Playbooks favour completeness: a child can run to ~1,200 words and a hub to ~3,000, plus its resource directory (see `playbooks/_index.md`). Notes marked `example: true` are samples shipped with the starter kit; delete them once the owner has their own.
