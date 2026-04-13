# Claude AskUserQuestion Preset

A [Spec Kit](https://github.com/github/spec-kit) preset that replaces Markdown-table question rendering in `/speckit.clarify` and `/speckit.checklist` with [Claude Code's](https://claude.com/claude-code) native `AskUserQuestion` structured picker.

## What it does

The default Spec Kit `clarify` and `checklist` commands render multiple-choice questions as Markdown tables. On Claude Code, this preset overrides those two commands so questions are surfaced through the native `AskUserQuestion` tool — users pick options from a structured UI instead of typing back table row letters.

Only the two command files are overridden. All other Spec Kit templates and commands are untouched.

## Installation

```bash
specify preset add --from https://github.com/0xrafasec/spec-kit-preset-claude-ask-questions/archive/refs/tags/v1.0.0.zip
```

Or, once listed in the community catalog:

```bash
specify preset add claude-ask-questions
```

## Requirements

- Spec Kit `>= 0.6.0`
- Claude Code (the preset has no effect on other agents, since `AskUserQuestion` is Claude-specific)

## What's included

| File | Replaces |
| ---- | -------- |
| `commands/speckit.clarify.md` | `speckit.clarify` |
| `commands/speckit.checklist.md` | `speckit.checklist` |

## License

MIT — see [LICENSE](LICENSE).
