# Flannel

A senior-dev pairing persona for Claude Code, for developers who get lost in jargon.

Flannel is the senior dev who pulls up a chair, explains what they're doing as they go, and makes
sure you're on the same page before moving on. It optimizes for the clearest code, and for you
understanding it.

Built for developers who:

- Find technical explanations full of jargon hard to parse
- Don't want to read a wall of text to get one answer
- Sometimes feel behind and want to be taught, not talked down to

## Install

```
/plugin marketplace add raymondware/flannel
/plugin install flannel@flannel-marketplace
```

## Commands

| Command | What it does |
|---|---|
| `/flannel:mode [lite\|full\|ultra\|off]` | Set how much narration and analogy happens this session |
| `/flannel:pair <task>` | Implement a task, narrating decisions in small steps |
| `/flannel:review [path]` | Review a diff for readability, with a plain-language why on each finding |
| `/flannel:explain <thing>` | Explain code or a concept in plain words, built up incrementally |
| `/flannel:audit [path]` | Repo-wide clarity scan |
| `/flannel:debt <what/where>` | Log a confusing spot for later instead of stopping to fix it |
| `/flannel:recap` | Plain-language summary of what changed and why |
| `/flannel:help` | One-line reference for every command |

## How it talks

- Short answer first, always. Detail only if you ask for it.
- Analogies before jargon — the formal term comes after the idea has already landed.
- Small steps instead of walls of text.
- No "obviously," "just," "simply," or "trivially." A knowledge gap is normal, not a deficiency.

## What it sounds like

Asked "what's a closure?", most tools answer like this:

> A closure retains a reference to its lexical scope even after the outer function has returned.

Flannel answers like this:

> A closure is like a backpack. When a function is created inside another function, it packs up the
> variables it needs and carries them around, even after the outer function is long gone.
>
> That's what people mean by a closure. Want to see where this bites you in practice, or is that
> enough?

Same fact. One of them you can repeat to a teammate an hour later.

See `skills/flannel/references/voice.md` and `skills/flannel/references/clarity-ladder.md` for the
full rules and worked examples.

## License

MIT
