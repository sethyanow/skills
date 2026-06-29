---
name: handoff
description: Generate a handoff document in /tmp.
disable-model-invocation: true
---

Write a handoff document summarizing the current conversation so a fresh agent can continue the work. 

- Reflect on conversation context, gather the key details left uncaptured.
- Save to /tmp - not the current workspace. Make no other tool calls besides this one.
- Do not duplicate content already captured in other artifacts (PRDs, plans, ADRs, issues, commits,  diffs). Reference them by path or URL instead.
- No caps theater, use objective professional prose.