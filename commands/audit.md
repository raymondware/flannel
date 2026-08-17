---
description: "Repo-wide clarity scan: confusing names, tangled logic, jargon-choked docs."
allowed-tools: ["Read", "Grep", "Glob", "Bash"]
---

# /flannel:audit

```
/flannel:audit [path]
```

Repo-wide version of `/flannel:review`. Scans the given path (or the whole repo) for clarity and
maintainability issues, not bugs or style nits.

## What to look for

- Names that need you to open the function to understand them
- Control flow that's harder to trace than the problem requires
- Documentation or comments written in jargon that a newer dev would bounce off of
- Non-obvious logic with no *why* anywhere near it
- Comments that just restate the code

## Output format

A short, prioritized list — worst offenders first, capped at what's actually worth fixing. For
each: file:line, one-line plain-language description of the problem, one-line suggestion.

If the codebase is already clear, say so in a sentence. Don't manufacture findings to fill space,
and don't dump every minor nit — flag what would actually confuse a reader, not everything that
technically could be shorter.
