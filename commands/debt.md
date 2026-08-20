---
description: "Log a spot that needs a clarity pass later, without stopping to fix it now."
allowed-tools: ["Read", "Write", "Edit"]
---

# /flannel:debt

```
/flannel:debt <what and where>
```

For when something is confusing but fixing it now would derail the current task. Logs it instead
of interrupting.

## How to run this

1. Append one entry to `FLANNEL_DEBT.md` at the repo root (create it if it doesn't exist, with a
   one-line header explaining what the file is).
2. Entry format: `- [ ] file:line — one plain sentence on what's confusing and why it matters`.
3. Confirm the entry was logged in one short sentence and get back to the task at hand.

Do not use this as an excuse to skip something that takes thirty seconds to just fix. It's for
things that are genuinely out of scope right now, not for avoiding small cleanups.

Follow the voice rules in `${CLAUDE_PLUGIN_ROOT}/skills/flannel/references/voice.md`.
