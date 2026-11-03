# Playbooks

One note per recurring marketing-leadership job. **A playbook is a well-stocked kitchen, not a verdict.** It holds what the trusted sources recommend and when each recommendation applies, so the owner can apply their own judgement to the situation in front of them. **Playbooks never carry the owner's call.** Their own views live in `principles/`.

Each **hub playbook** runs:

1. **The job** and its **typical length**.
2. **What success looks like**: a checklist for the end state, plus a mid-cycle test.
   **Where the sources agree**: the 5–8 must-do practices. Each needs 3+ independent sources, at least one from the canon, and no source in the research contradicting it. Each item lists its sources. These are practices, not outcomes. If a later source contradicts an item, it moves to *Where the sources disagree*.
3. **What changes the answer**: a table of *If the situation is…, then size the process like…*
4. **The process**: phases with timing, the steps (each sourced and dated), and a **checklist** per phase. Include a lightweight version where one exists.
5. **Resource directory**: *I need… → use… → where*. Templates, models and decks, with the exact file, link, slide or connector tool, plus the best podcast episodes and videos (with timestamps), posts, books and tools, so the owner can go straight to the best resource.
6. **Where the sources disagree**: framed as *when each view applies*.
7. **Failure modes.**
8. **Recipes**: links to child playbooks holding the *If X, then Y* moves for each moment within the job.
9. **Coverage**: what was searched, how deep the canon is on each moment, and known gaps.

**Child playbooks** (`parent:` in frontmatter) hold the recipes for one moment, each recipe naming its source and date. Keep each child under ~1,200 words. A **meeting guide** (`type: meeting-guide`) is a child for one recurring meeting: sizing, prep cycle, agenda with timings, who presents what, how to succeed, templates. Up to ~2,000 words. A hub can run to ~3,000 words, not counting the resource directory, which can be as long as it needs to be. **Completeness beats brevity:** if a moment needs more than a child can hold, split it into two children.

**Sources: canon first, then the best of the web.** Playbooks draw on every relevant piece from the canon, plus best-in-class material from the wider web, especially where the canon is thin. **Citations** are always a link to the library note with the source's full name, e.g. `([[Note Title - Jane Example|Jane Example]])`, with several separated by semicolons. No dates and no markers in the citation: the library note holds the date and its `tier` (whether the source is a trusted one). Only numbers and benchmarks carry an inline `(as of YYYY-MM)`. Build or refresh playbooks with `/build-playbook <job> [refresh]`.

## Your playbooks

Add a line per playbook as you build them with `/build-playbook`:

- [[positioning-example]] — positioning a B2B tech product, from competitive alternatives to sales narrative. EXAMPLE: delete once you've built your first real playbook
