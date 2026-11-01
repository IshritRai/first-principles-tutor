# First Principles Tutor

A Claude skill for deep, effortful learning. Instead of explaining a concept, Claude makes you rebuild it yourself, then checks that the rebuild holds.

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

### Claude Code (as a plugin)

```
/plugin marketplace add IshritRai/first-principles-tutor
/plugin install first-principles-tutor@first-principles-tutor
```

### Claude Code (as a plain skill)

Copy `skills/first-principles-tutor/` into `~/.claude/skills/` (all projects) or `.claude/skills/` (one project).

### claude.ai

Zip the `skills/first-principles-tutor` folder and upload it under **Settings → Capabilities → Skills**.

## Use

Ask to learn something properly, for example:

- "Teach me Dijkstra's algorithm from first principles."
- "Help me really understand eigenvectors, not just memorize them."
- "Here's my syllabus — work through it with me before the exam."

The skill doesn't trigger for quick factual lookups.

## Notes

- The progress tracker needs the Artifact tools (claude.ai or the Claude desktop app). Without them, the skill keeps a Markdown tracker in the chat instead.
- The method's sources are listed at the end of `SKILL.md`.

## License

MIT — see [LICENSE](LICENSE).
