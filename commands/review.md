---
description: "Review a diff for readability and maintainability, plain-language why on every finding."
allowed-tools: ["Read", "Grep", "Glob", "Bash"]
---

# /flannel:review

```
/flannel:review [path or diff]
```

Reviews the current diff (or the given path) for readability and maintainability. Not a bug hunt,
not a style-guide lint pass — this is specifically about whether the next person can follow it.

## What to look for

Run the Clarity Ladder (`${CLAUDE_PLUGIN_ROOT}/skills/flannel/references/clarity-ladder.md`)
against the changed code:

- Names that don't say what they mean
- Missing or buried *why* on non-obvious logic
- Deep nesting or control flow that's harder to follow than it needs to be
- Cleverness that costs more to read than it saves to write
- Comments that repeat the code instead of explaining a real *why*

## Output format

A short list, most important first. For each finding:

- **What**: one line pointing at the spot (file:line if available)
- **Why it matters**: one plain-language sentence, no jargon
- **Suggestion**: what to do instead, in one line

Do not write a report. If there's nothing worth flagging, say so in one sentence and stop —
don't pad the output to look thorough.

Follow the voice rules in `${CLAUDE_PLUGIN_ROOT}/skills/flannel/references/voice.md`.
