# First Principles Tutor

A Claude skill for deep, effortful learning. Instead of explaining a concept, Claude makes you rebuild it yourself, then checks that the rebuild holds.

Works in **claude.ai** (web and mobile), the **Claude desktop app**, and **Claude Code**.

It combines five techniques into one loop:

| Technique | What it does in the loop |
|---|---|
| **Socratic method** | Claude asks, hints and withholds instead of lecturing. |
| **First principles** | Each concept is chained down to bedrock and climbed back up, link by link. |
| **Genetic method** (Otto Toeplitz, 1927) | The concept is introduced as the answer to the problem that made it necessary. |
| **Proofs and refutations** (Imre Lakatos, 1976) | Your first claim gets attacked with counterexamples until the precise statement falls out. |
| **Feynman technique** | You explain it back, closed-book, and the gaps decide what comes next. |

Every session also:

- builds or loads a **persistent progress tracker** (a claude.ai artifact) with a topic map, your thought process, sessions, and a one-click handoff to a new chat;
- puts a **spoiler-free visual** in every teaching turn — it shows where your reasoning stands, never the answer;
- uses **delayed, unannounced retests** to check what actually stuck.

## Install

Pick the one that matches where you use Claude. You only need one.

### claude.ai and the Claude desktop app (most people)

1. Download this repo: click **Code → Download ZIP** above, and unzip it.
2. Inside, find the folder `skills/first-principles-tutor`. Zip **just that folder**, so the zip contains the `first-principles-tutor` folder at its top level.
3. In Claude, go to **Settings → Capabilities** and turn on **Code execution and file creation** (called **Create and edit files** in the newer settings layout). Skills need it.
4. Go to **Customize → Skills**, click **+**, then **+ Create skill → Upload a skill**, and choose your zip.
5. Make sure the skill is toggled on.

Skills work on Free, Pro, Max, Ultra, Team and Enterprise plans. On Team and Enterprise, an owner has to allow skills and code execution in Organization settings. See Anthropic's guide: [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

### Claude Code (terminal) — as a plugin

```
/plugin marketplace add IshritRai/first-principles-tutor
/plugin install first-principles-tutor@first-principles-tutor
```

### Claude Code (terminal) — as a plain skill

Copy `skills/first-principles-tutor/` into `~/.claude/skills/` (all projects) or `.claude/skills/` (one project).

## Use

Ask to learn something properly, for example:

- "Teach me Dijkstra's algorithm from first principles."
- "Help me really understand eigenvectors, not just memorize them."
- "Here's my syllabus — work through it with me before the exam."

The skill doesn't trigger for quick factual lookups.

## Notes

- The progress tracker page is a claude.ai artifact. Where artifacts aren't available, the skill keeps the same tracker as Markdown in the chat instead.
- The `.claude-plugin/` folder is only for the Claude Code plugin install. claude.ai users can ignore it.
- The method's sources are listed at the end of `SKILL.md`.

## License

MIT — see [LICENSE](LICENSE).
