# Case studies

Real-world examples, told as tactical guides: **who did something brilliantly, and exactly how.** Playbooks say what to do. Case studies show someone doing it.

**These sit outside the canon.** They're researched from the open web (founders' own posts, interviews, podcasts, credible press), not from [[canon/_index|trusted sources]]. So they follow stricter rules:

- `origin: web-research` on every case study.
- **Every factual claim carries a numbered citation.** Prefer primary sources: the people who built it, in their own words. That means their **podcast and YouTube interviews** (read from the transcript, cited with a timestamp) and their **LinkedIn and X posts** (cited by the post's own URL and date).
- **Results are labelled by evidence quality:** *verified* (published data or a primary source with numbers), *claimed* (stated by the company or founder, not independently checked) or *reported* (third-party, secondhand).
- **Volatile by default:** review every 6 months. Tactics decay fast once everyone copies them.
- `/advise` may cite case studies as examples, with a note that they're outside the trusted sources.
- **Visual:** the company logo, plus 2–4 screenshots of *public* pages showing the tactic, in `case-studies/images/<slug>/`. These are committed to git (unlike `attachments/`).
- **Builders are linkable:** verified LinkedIn, X or website links in `people_links`. Don't link private individuals.

Write them with `/research-case-study <company or tactic>`.

**Filtering:** the case-study view filters by `tactic` and by `tags`. Reuse an existing tactic where one fits; check the tactics already in use with `grep -h '^tactic:' case-studies/*.md`. Add a new one only for a genuinely different tactic. Tags come from `taxonomy.md`.

## Template

```markdown
---
title: "<Company>: <the tactic in a few words>"
company: <Company>
people: ["<Name> (<role>)"]
tactic: <short kebab-case, e.g. creator-program, founder-led-brand, employee-advocacy>
tags: [<1–3 from taxonomy.md>]
origin: web-research
period: <when it ran, e.g. 2024–present>
researched: YYYY-MM-DD
shelf_life: volatile
review_by: YYYY-MM-DD
freshness: current
confidence: high | medium | low
logo: "case-studies/images/<slug>/logo.svg"
people_links:
  "<Name>": { linkedin: https://..., x: https://..., website: https://... }
related_playbooks: []
---

# <Company>: <tactic>

> [!summary] At a glance
> One paragraph: what they did, why it's notable, the headline result (with its evidence label).

## Who built it
## How it worked
Step by step, concrete enough to copy: structure, selection, incentives, cadence, tooling, team.
## Results
| Claim | Evidence | Source |
## Why it worked
## When it transfers, and when it doesn't
## How to run your own
A checklist.
## Resources
Grouped, each with one line on why it's worth your time:
- **Watch and listen:** podcast episodes and YouTube interviews with the builders, with the timestamp where the tactic is discussed.
- **Posts from the builders:** the best LinkedIn and X posts, linked and dated.
- **Read:** the builders' blog posts and the best write-ups of the tactic.
- **Follow:** the builders and anyone who teaches the tactic well.
## Sources
1. …
```

## Case studies

Add a line per case study as you write them with `/research-case-study`.

- [[clay-narrow-icp-repositioning]] — EXAMPLE: Clay narrowing its ICP from a general-purpose tool to outbound sales, then to cold-email agencies. Delete once you have your own
