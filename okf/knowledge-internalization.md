---
type: Concept
title: Knowledge internalization
description: Reflect new knowledge in the meaning, conditions, relationships, and judgments of related concepts
---

# Knowledge internalization

Internalization means reflecting how new knowledge affects the meaning, conditions, relationships, and judgments of related concepts. Summarizing the source or copying the same sentence into several files is not enough to internalize it.

The [source of truth](source-of-truth.md) tells us where a fact is defined and changed. Each concept should explain what that fact means from its own perspective. For example, even if the mechanics for invoking order validation live in implementation documentation, related concepts should still make it possible to understand that a failed validation means the order is not established and how that affects payment and inventory.

The prose around a link should explain why the relationship matters and what effect it has. The goal is not to place all related knowledge into one document, but to provide enough context to understand the current concept without misunderstanding it. When new knowledge changes that context, [update the related concepts](context-propagation.md).

[Agent autonomy](agent-autonomy.md) is how OKF's natural-language context and flexible relationship expression are put to work in practice. Internalized reasons, conditions, and relationships must be rich enough for an agent to interpret questions and changes that were not enumerated in advance. Instead of specifying every action as an instruction, provide the knowledge that supports judgment. Short operating instructions do not imply thin knowledge bodies. Conversely, not every detail of a [large corpus](large-corpus.md) needs to be internalized; the depth should be determined by the judgments that are repeatedly reused.

Knowledge operations themselves can also be internalized, such as criteria for adopting collected material or how to interpret conflicting evidence. Do not send something to `docs/` automatically just because it is procedural; decide whether separate task guidance is needed based on how it is actually used.

When internalizing a design conversation, distinguish the user's purpose and adopted judgments from proposed filenames, categories, and procedures. Reflect later corrections to the context and connect reusable conclusions and their reasons to related concepts. For example, the operation categories in [adoption judgment](adoption.md) are vocabulary for understanding natural-language intent; their appearance in a conversation does not require fixed commands or separate directories. Choose the concrete document structure to fit the adopted purpose and its relationship to existing knowledge.

## Internalization depth and operating cost

Keeping needed context within a concept can help readers understand conditions and exceptions even when they read only part of the documentation. This is an expected benefit of internalization; adding explanation alone does not establish that understanding or work efficiency has improved. Judge appropriate depth by [observing real operation](feedback.md): the burden of rereading source material, the extent to which outdated judgments remain after changes, and the cost of maintaining knowledge.

Knowledge explaining an operating philosophy also has reading and maintenance costs. Examine whether restatement in each document adds reasons, conditions, or judgment needed for that concept. If repeated explanation only increases the effort required to reach domain knowledge, shorten it or link to the source of truth. Do not remove necessary context based on length alone.
