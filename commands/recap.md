---
description: "Plain-language summary of what changed and why, in words you could repeat back."
allowed-tools: ["Read", "Bash"]
---

# /flannel:recap

```
/flannel:recap
```

End-of-session summary, written so the user could turn around and explain it to someone else
without looking anything up.

## Format

1. **What changed** — one or two sentences, plain words, no file-by-file listing unless asked.
2. **Why** — the reasoning behind the main decision, in the same plain terms used while pairing.
   If an analogy was used earlier in the session and it fits, reuse it here instead of a new one.
3. **What to watch for** — one line on anything that could bite later (a tradeoff made, a spot
   logged to `FLANNEL_DEBT.md`, an assumption worth double-checking).

Three short sections, no more. This is a recap, not a report — if it's running past a few
sentences per section, cut it down rather than add more structure.
