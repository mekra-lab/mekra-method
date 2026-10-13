---
type: Concept
title: Knowledge internalization
description: Reflect new knowledge in the meaning, conditions, relationships, and judgments of related concepts
---

# Knowledge internalization

Internalization means reflecting how new knowledge affects the meaning, conditions, relationships, and judgments of related concepts. Summarizing the source or copying the same sentence into several files is not enough to internalize it.

The [source of truth](source-of-truth.md) tells us where a fact is defined and changed. Each concept should explain what that fact means from its own perspective. For example, even if the mechanics for invoking order validation live in implementation documentation, related concepts should still make it possible to understand that a failed validation means the order is not established and how that affects payment and inventory.

The prose around a link should explain why the relationship matters and what effect it has. The goal is not to place all related knowledge into one document, but to provide enough context to understand the current concept without misunderstanding it. When new knowledge changes that context, [update the related concepts](context-propagation.md).

[Agent autonomy](agent-autonomy.md) is how OKF's natural-language context and flexible relationship expression are put to work in practice. Internalized reasons, conditions, and relationships must be rich enough for an agent to interpret questions and changes that were not enumerated in advance. Instead of specifying every action as an instruction, provide the knowledge that supports judgment. Short operating instructions do not imply thin knowledge bodies. Conversely, not every detail of a [large corpus](large-corpus.md) needs to be internalized; consider both the importance of the judgments needed and the benefits of repeated use.

Consider frequency of use alongside importance to judgment. Exceptions that reverse a conclusion, conditions that limit applicability, and premises on which other concepts depend must be understandable in the relevant concepts even when rare. For example, if most orders can be canceled but cancellation is unavailable after dispatch is confirmed, do not leave that condition only behind a source link because it is uncommon. Link to detailed evidence while internalizing the condition's meaning and effects.

Knowledge operations themselves can also be internalized, such as criteria for adopting collected material or how to interpret conflicting evidence. Do not send something to `docs/` automatically just because it is procedural; decide whether separate task guidance is needed based on how it is actually used.

When internalizing design conversations and research records, distinguish the user's purpose and [what was actually adopted](external-sources.md#roles-and-valid-scope-of-materials) from proposed filenames, categories, and procedures. Reflect later corrections to the context and connect reusable conclusions and their reasons to related concepts. For example, the operation categories in [adoption judgment](adoption.md) are vocabulary for understanding natural-language intent; their appearance in a conversation does not require fixed commands or separate directories. Choose the concrete document structure to fit the adopted purpose and its relationship to existing knowledge.

When integrating and restating material, preserve [epistemic distinctions that matter for judgment](epistemic-distinctions.md). Do not merge a source's claim and the agent's inference into a single confirmed fact, or erase perspectives, timing, or uncertainty needed for judgment while making an explanation easier to read.

## Concept boundaries and organization

Choose knowledge units according to the need to discover, reuse, and update them independently and the context that must be understood together. Existing document titles and file boundaries do not automatically define new knowledge boundaries. Consider separating concepts that answer different questions or respond to different changes, while keeping conditions, evidence, and exceptions together when separation would break their meaning. Relationships can explain directly what changes another concept's premises or outcomes, beyond parent-child classification.

| Approach | When it helps and costs to consider |
| --- | --- |
| Separate | Organize independent concepts when judgments found or changed separately are mixed in one document. Preserve enough context in each concept to understand its meaning, conditions, and relationships. |
| Integrate | Bring scattered conditions and exceptions into a coherent explanation when they must be read together. Check that unrelated judgments are not gathered into the same document. |
| Connect relationships | Explain relevant meaning and effects when a change in one concept alters judgment in another. Moving files or adding a link does not replace explanation of the relationship. |
| Deepen internalization | Strengthen context when the same reasoning requires repeatedly rereading source material. Also consider responsibility for the evidence and maintenance costs after changes. |
| Reuse | Use existing knowledge and strengthen what is needed when it sufficiently supports actual use and changes. Creating new files is not a goal in itself. |

These approaches provide design knowledge, not fixed procedures or document types. Compare arrangements with different granularity, explanatory depth, and synthesis against actual questions and changes when [judging sufficiency](knowledge-design.md). Document length and count alone do not determine concept boundaries or the quality of knowledge.

## Integrated understanding and internalization in individual concepts

During construction, understand related knowledge together to discover conditions, relationships, conflicts, and dependencies between concepts. Preserve that understanding as the context needed from each concept's perspective. A complete integrated model of the entire target is not a prerequisite for finding relationships; develop understanding through exploration, internalization, and connection. Keep unresolved conflicts and uncertainty visible in the judgments they affect.

Synthesis knowledge can be created when integrated judgments across several concepts are repeatedly needed. A synthesis explains the overall relationships and conditions acting together, without independently taking ownership of individual concepts' definitions or change responsibilities. In use, find and combine the concepts relevant to a question so that their meaning and relationships can support questions not anticipated during construction. There is no need to prewrite every insight as a synthesis document or defer all integration until a question arrives.

## Meaning of states and results

A state name alone may not convey enough meaning for the next judgment. For example, if `ready` only confirms that configuration is in place, judging whether a request actually succeeded requires separate evidence about connectivity, authentication, or other relevant conditions. If successful processing, completed storage, and business approval depend on different conditions, explain those conditions and responsibilities in the relevant concepts. Internalize the relationships when default behavior has exceptions or applicability differs by caller. Explain the judgments that are actually being confused rather than adding new fields to every state.

Also distinguish the scope of knowledge written from the scope an agent actually read and used. [Connection to actual use](knowledge-operation.md#connecting-knowledge-to-actual-use) addresses how knowledge connects to work and what counts as completed adoption; [operational observations](feedback.md) address its effects on results.

## Internalization depth and operating cost

Keeping needed context within a concept can help readers understand conditions and exceptions even when they read only part of the documentation. This is an expected benefit of internalization; adding explanation alone does not establish that understanding or work efficiency has improved. Judge appropriate depth by [observing real operation](feedback.md): the burden of rereading source material, the extent to which outdated judgments remain after changes, and the cost of maintaining knowledge.

Knowledge explaining an operating philosophy also has reading and maintenance costs. Examine whether restatement in each document adds reasons, conditions, or judgment needed for that concept. If repeated explanation only increases the effort required to reach domain knowledge, shorten it or link to the source of truth. Do not remove necessary context based on length alone.
