# Marketing Leadership OS — starter kit

A personal operating system for marketing leaders: a library of the best thinking you read, playbooks distilled from it for the jobs you do again and again, real-world case studies, a swipe file of great marketing, and your own principles. You can ask it for advice grounded in all of it.

It's an [Obsidian](https://obsidian.md) vault of plain markdown files, maintained by [Claude Code](https://claude.com/claude-code) skills. Nothing here is a black box: every note is a file you own, and it goes with you into every role.

This kit is the empty shell, plus one short example per layer so you can see what each note looks like. Built by [Andy Parker](https://www.linkedin.com/in/parkeracs).

## How it works

1. **Capture**: clip articles with Obsidian Web Clipper, drop in PDFs and screenshots.
2. **Process**: `/process-inbox` turns each clip into a short library note: the durable principles, the dated numbers and tactics, tags and source.
3. **Curate**: notes link to the people you trust most (your trusted sources), and age out on a schedule so stale benchmarks are never served as current.
4. **Synthesise**: `/build-playbook` reads everything relevant from your trusted sources, researches the wider web, and writes a playbook for one job: what changes the answer, the process, where experts agree and disagree, and the best templates and resources.
5. **Apply**: `/advise` answers questions from your own playbooks and library, with citations. `/advise-deep` works through your company context for the big questions.

## What you need

- **Claude Code** with a Claude plan ([install](https://docs.claude.com/en/docs/claude-code/overview)). The desktop app or the terminal both work.
- **Obsidian** 1.9 or later (free), for reading and browsing the vault. The views on the home page use Obsidian's built-in Bases.
- **Obsidian Web Clipper** (free browser extension), for capturing articles.
- Optional: **git** and a private GitHub repository, for history and backup.

## Setup (about 15 minutes)

**The easy way:** paste this into Claude Code, in any folder:

```
Set up my Marketing Leadership OS from https://github.com/parkeracs/marketing-leadership-os. Follow the "Let Claude set it up" section of its README.
```

Claude makes your own private copy, then walks you through the rest. To do it by hand instead, follow these steps.

1. **Get the files.** Click **Use this template** on GitHub to make your own copy, and make it **private**: your library will hold paid and personal material. Or download the ZIP. Put the folder somewhere permanent, such as `~/marketing-leadership-os`.
2. **Open it in Obsidian.** *Open folder as vault*. The home page is `Home.md`; its views fill up as you process clips.
3. **Open Claude Code in the folder** and run **`/setup`**. It's a short interview, four rounds, under ten minutes. It learns your role, who you serve, the sources you trust and how you work, then writes `settings.md`, your first trusted-source notes and your tag list.
4. **Install the Web Clipper templates.** Follow `setup/web-clipper/README.md`.
5. **Run the loop once.** Clip three pieces you've read recently, run `/process-inbox`, then run `/build-playbook <a job you do often>`. Then ask `/advise` something real.

Every skill asks two to four quick questions the first time you run it, to fit how you work, and saves the answers in `settings.md`. Run any skill with `setup` (for example `/build-playbook setup`) to change them.

## Let Claude set it up

*Instructions for Claude Code, when the owner asks it to set up this kit.* Explain each step in a line as you go, and ask before installing anything.

1. **Make the owner's copy.** Ask where to put it [`~/marketing-leadership-os`]. Then, from the parent folder:
   - If the GitHub CLI is installed and signed in (`gh auth status`): `gh repo create <folder-name> --template parkeracs/marketing-leadership-os --private --clone`. The copy must be **private**: the library will hold paid and personal material.
   - Otherwise, if git is installed: `git clone https://github.com/parkeracs/marketing-leadership-os <folder>`, then `git remote remove origin`, so it never points at the template.
   - Otherwise: download `https://github.com/parkeracs/marketing-leadership-os/archive/refs/heads/main.zip` and unzip it into the folder.
2. **Read** the new copy's `CLAUDE.md` and this README.
3. **Obsidian.** Ask whether Obsidian 1.9+ is installed. If not, point the owner to https://obsidian.md. Then have them choose *Open folder as vault* and pick the new folder.
4. **The interview.** Read `.claude/skills/setup/SKILL.md` in the new copy and follow it exactly, working on the files in that folder.
5. **Web Clipper.** Walk the owner through `setup/web-clipper/README.md`.
6. **Finish.** Tell the owner to quit and reopen Claude Code *in the new folder*, so `/process-inbox`, `/build-playbook`, `/advise` and the other skills work as commands. Then give them step 5 of Setup, "Run the loop once".

## The skills

| Skill | What it does |
|---|---|
| `/setup` | The first-time interview. Re-run any time |
| `/workspace-setup <company>` | Records your current company's context (stage, ACV, motion, goals) for tailored advice. Kept out of git |
| `/process-inbox` | Turns clips and PDFs into library notes, with dated specifics and freshness |
| `/process-swipe` | Categorises screenshots and examples into the swipe file |
| `/build-playbook <job>` | Researches and writes a playbook for one recurring job |
| `/research-case-study <company tactic>` | Researches a real-world example from public sources, fully cited |
| `/advise <question>` | A quick answer from your playbooks and library, with sources |
| `/advise-deep <question>` | A considered answer: your context, the whole vault and deep web research |
| `/red-team <plan>` | Stress-tests a plan or budget ask the way a CFO, CEO or board would |
| `/freshness-review` | Monthly: finds benchmarks and tactics past their review date |
| `/trusted-sources-review` | Quarterly: proposes sources to add or review, with the evidence |

## The rules that keep it trustworthy

- **Employer data stays in `workspaces/`**, which git ignores. Lessons can move into playbooks; numbers, names and plans never do. Check your employer's AI policy before adding a workspace.
- **Every number has a date.** Benchmarks and tactics carry an *as of* date and a review window, so old figures aren't passed off as current. See `freshness.md`.
- **Every claim is cited**, and anything from outside your trusted sources is labelled as such.
- **Paid content is for you alone.** Never bulk-download a paid archive, and never publish your library.
- **Your voice is yours.** Claude never writes your "My take" notes or your principles for you.

The full rules are in `CLAUDE.md`, which Claude Code reads automatically.

## The examples

Each layer has one example note on positioning, marked `example: true`. They're built from free public sources and show the format. `/setup` asks whether to keep them; delete them whenever you like.

## Credits

Partly inspired by Kieran Flanagan's Marketing Intelligence Layer. Built with Claude Code.

## Licence

MIT. Copy it, adapt it, share it. See `LICENSE`.
