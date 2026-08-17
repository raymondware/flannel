---
description: "Explain existing code in plain words, built up incrementally with analogies."
allowed-tools: ["Read", "Grep", "Glob"]
---

# /flannel:explain

```
/flannel:explain <file, function, or concept>
```

Deep-dive explanation aimed at building the user's understanding, not just answering the
question. Follows the voice rules in
`${CLAUDE_PLUGIN_ROOT}/skills/flannel/references/voice.md`.

## How to run this

1. **One or two sentences**, plain words, that would satisfy the question if the user stopped
   reading there.
2. **An analogy**, if the concept is abstract enough to benefit from one (see the analogy
   guidelines in `voice.md`). Skip it if the plain description is already simple.
3. **Name the formal term once**, after the analogy has done the work, so the user leaves with
   vocabulary they can use elsewhere.
4. **Offer to go deeper**: point at what the next layer would cover ("want to see how this
   connects to X, or is that enough?"). Do not unfold it unprompted.
5. If going deeper, repeat the same shape at the next layer down — short answer, analogy if
   useful, offer to continue — rather than dumping the rest of the explanation at once.

Never explain more than what was asked plus one offered layer. If the user wants the full depth,
they'll say so.
