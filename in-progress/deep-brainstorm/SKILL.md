---
name: deep-brainstorm
description: An in-depth brainstorming session.
disable-model-invocation: true
---

A deeper grilling session that keeps a living `BRAINSTORM.md` so decisions survive context loss.

# BRAINSTORM.md

A living doc with an append-only `# Decision Log` at the end, seeded from [`BRAINSTORM.template.md`](BRAINSTORM.template.md). It guards against drift, and lets a subagent or a fresh session pick up the work without re-explanation.

On first response, negotiate where it lives. Recommend a location if the conversation makes one obvious; otherwise default to `BRAINSTORM.md` in the working dir. If one already exists, say so but don't read it unprompted — it might cloud your context.

Append each user decision to the `# Decision Log` with shell `>>`, so edit-tool string replacements don't eat context. Update a branch's section in place when it resolves.

When in doubt, ask. This is collaborative. Guide me to ideas I might not be considering, don't drive for me.

# Grilling

Interview me relentlessly about every aspect of this plan until we reach a shared understanding. Walk down each branch of the design tree, resolving dependencies between decisions one-by-one. For each question, provide your recommended answer.

Ask the questions one at a time, waiting for feedback on each question before continuing. Asking multiple questions at once is bewildering.

If a question can be answered by exploring the codebase, explore the codebase instead.

# Confidence and the lightning round

Keep grilling until 3 questions remain and they're independent, as in their answers won't shift no matter how the others resolve. That's the 85% mark: it counts independent unknowns, not a vibe.

Then fire a lightning round with the final 3 questions at once. Afterwards offer to fan each to a subagents for fresh eyes adversarial assessment.

# Procedure

1. Seed BRAINSTORM.md from template (where, when, first log entry)
2. Grill one question at a time, append decisions in real time to the doc
3. Resolve branches in-doc as decisions land
4. Gate — three independent unknowns remain
5. Lightning round — then optional adversarial fan-out