---
name: red-team
description: Stress-test a marketing plan, budget ask or strategy through a sceptical buyer's lens (CFO, CEO, board or CRO, set in settings) — weak assumptions, payback math, the questions they will ask. Invoke with /red-team <plan text or file> [workspace:<company>], or /red-team setup to change its settings.
disable-model-invocation: true
---

## 0. First run

1. Read `settings.md` at the vault root. If it has no `## Profile` section, tell the owner to run `/setup` first, then stop. `## Profile` and `## Layers` apply throughout this skill.
2. If `settings.md` has no `## /red-team` section, or `$ARGUMENTS` is `setup`, ask these in **one** message, numbered, each with its default in brackets, so the owner can reply "defaults":
   1. **Whose eyes should I read the plan through?** Any of: CFO, CEO, board member or investor, CRO. [CFO and CEO]
   2. **How harsh?** *Blunt* (no softening, critique only) or *constructive* (same critique, plus a one-line fix per weak point). [blunt]
   3. **Which trusted sources speak for that side of the table?** Canon creators whose lens is finance, boards, investors or sales leadership. [any `canon/` note whose Lens mentions finance, boards, investors or revenue leadership]
3. Write the answers as a short bullet list under `## /red-team` in `settings.md` (add it at the end; replace it if re-running setup). Confirm in one line. Then red-team the plan, or stop if the owner only ran `setup`.

Red-team the plan in $ARGUMENTS as the sceptical reader(s) set in settings would. If a workspace is named (and Layers turns workspaces on), read `workspaces/<company>/context.md` and test the plan against it.

**Read first:** `playbooks/` and `principles/` relevant to the plan, and the canon notes set in settings as the buy-side view. If none qualify yet, say so and work from the playbooks.

**Output, in this order:**
1. **Verdict in one line.** Would this get funded as written? Yes, no, or yes-if.
2. **The three weakest assumptions**, ranked by how much of the plan collapses if each one is wrong.
3. **The maths check.** CAC, payback, pipeline coverage or conversion assumptions, recomputed from what's given. Show the arithmetic. Say what's missing to check it. Any benchmark you compare against carries its source and date (`freshness.md`).
4. **The five questions the chosen reader(s) will ask**, phrased the way they'd actually ask them.
5. **What would change their mind**: the evidence, pilot or milestone that would turn a no into a yes.

**Rules:** match the harshness set in settings. With *blunt*: don't soften, and don't rewrite the plan unless asked. Critique only. With *constructive*: the same critique, plus one line per weak point on how to fix it, but still no rewrite unless asked. Never invent company figures; where data is missing, name the gap. Never copy workspace data into a portable file.
