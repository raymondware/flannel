# Flannel Plugin - Contributor Guide

## What This Is

Flannel is a Claude Code plugin: a senior-dev pairing persona for developers who find technical
explanations full of jargon, don't want to read walls of text, and sometimes feel behind. Flannel
talks, teaches, and pairs, optimizing for readability and maintainability instead of minimalism.

## Structure

```
flannel/
├── .claude-plugin/     # Plugin manifest (plugin.json, marketplace.json)
├── commands/           # /flannel:* slash commands
└── skills/flannel/     # SKILL.md + reference files (clarity-ladder, voice)
```

## Conventions

- All internal paths use `${CLAUDE_PLUGIN_ROOT}/` prefix.
- Every command file and the skill body point back to `references/voice.md` and
  `references/clarity-ladder.md` rather than restating the rules inline — one source of truth.
- Short-answer-first, chunked, analogy-when-it-helps: this shape applies to Flannel's own output,
  not just what it tells the user to do to their code.
- No banned condescension words ("obviously," "just," "simply," "trivially," "clearly," "of
  course") anywhere in command output or in this repo's own docs.

## Adding a New Command

1. Create `commands/your-command.md` with `description` frontmatter (and `allowed-tools` if it
   needs specific tool access).
2. Point back to `${CLAUDE_PLUGIN_ROOT}/skills/flannel/references/voice.md` rather than
   re-explaining the voice rules.
3. Add it to `commands/help.md` and to the command table in `skills/flannel/SKILL.md`.

## Adding to the Clarity Ladder or Voice Rules

Edit `skills/flannel/references/clarity-ladder.md` or `references/voice.md` directly. Keep new
entries in the same before/after or rule-plus-reason format already used there.

## Code Style

- No em-dashes.
- Plain, direct language — the same standard Flannel holds the user's code to applies to this
  repo's own prose.
- Conventional commits (feat:, fix:, docs:).
