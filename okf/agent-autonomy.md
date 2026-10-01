---
type: Principle
title: Autonomous agent judgment
description: Start from the agent's autonomous judgment and use it to guide the application of other operating principles according to purpose and context
sources:
  - id: okf-spec-v02
    resource: https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md
    title: Open Knowledge Format v0.2
---

# Autonomous agent judgment

Start from the agent's autonomous judgment, and interpret and apply other operating principles according to purpose and context.

Autonomous judgment is a meta-principle that guides the application of other operating principles. Clear responsibility for sources of truth, distributed context, internalization, and propagation provide the evidence and understanding needed for judgment. Choose structure, internalization depth, tools, and work sequence according to the target's needs. Autonomous judgment is a starting point for achieving the user's purpose; increasing autonomy is not an end in itself.

Facts and evidence, the user's intent, actual authority, and the target's constraints are conditions of that judgment. Discretion over how to apply a principle does not permit arbitrary changes to those conditions.

[Preserving epistemic distinctions](epistemic-distinctions.md) concerns differences that must not disappear during judgment. Distinguish claims in the material or the user's perspective from the agent's interpretation. Even when updating an account to be more accurate, do not silently replace earlier states of knowledge needed for later judgment.

The agent also decides what to retain as knowledge, which conditions and relationships to preserve, where the source of truth belongs, and what to update or reorganize as things change. The knowledge and context organized and maintained this way become evidence for deciding what to do in later work as the situation requires.

## Applying principles and revising them

Distinguish a decision to apply a principle differently in one target from a decision to revise Mekra's general principles. A choice that works in one target does not by itself change a general principle. When evidence supports reuse elsewhere, examine the conditions and limits before reflecting it in the source of truth. Mekra's own principles are also open to this reassessment; [self-erasure](self-erasure.md) describes how to judge their role as the need for them diminishes.

## Why use OKF

[OKF](okf-format.md) expresses knowledge through minimal structured metadata, free-form bodies, and Markdown links. The concrete meaning of a relationship is carried by natural language around the link, and neither concept types nor body structure are fully prescribed by a fixed taxonomy.[^okf-spec-v02]

With this structure, agents can read explanations intended for people and interpret conditions, exceptions, and relationships in light of the actual question. New knowledge can be connected to existing concepts without encoding every possible relationship and case in advance as schema or branching logic. To preserve that flexibility, we rely on contextual interpretation and autonomous judgment by capable LLMs. This is not an attitude required by the official specification; it is an operating philosophy chosen to take advantage of its expressive style.

To use that advantage, the agent must be able to judge what concepts to create, how deeply to [internalize](knowledge-internalization.md), and how far a change should [propagate](context-propagation.md) based on the actual content. Replacing these choices with detailed authoring rules and fixed procedures can shift the work toward formal compliance rather than meaning.

## Operational implications

On the premise that capable agents can interpret context, we prioritize organizing and maintaining the knowledge needed for judgment over prescribing detailed sequences of work. We keep definition and change responsibility clear and make the reasons, conditions, and relationships understandable in related concepts, while leaving the concrete way of working to the agent.

Keep repository instructions focused on purpose and repository-specific choices. Do not repeat generic guidance that can already be inferred from the specification and context. [Operating principles](../PRINCIPLES.md) provide judgment criteria, while [facets](../facets/README.md) help identify which judgments become especially important for a target. Facets do not prescribe structure; directory organization is chosen from actual need.

Reassess the need for supporting guidance already in place. If the agent can make the judgment on its own, or principles, tools, or operating conditions have changed, consider whether keeping the guidance still has practical value. [Self-erasure](self-erasure.md) applies this reassessment to Mekra itself, expressing the aim of stepping back as its contribution to judgment becomes less necessary.

Autonomous judgment depends on sufficient knowledge. Even when instructions are brief, the body should [internalize](knowledge-internalization.md) enough reasons, conditions, and relationships for judgment. Omitting domain facts or repository-specific context that the agent does not already know is not the intent of this principle.

The ability to interpret context is distinct from the process of finding and reading the context needed. An agent may understand one concept well yet fail to discover another affected concept. Reliable autonomous judgment depends on the evidence and context actually explored as well as reasoning ability; [context propagation](context-propagation.md) must account for these limits of discovery.

Requiring a separate deviation record every time a principle is applied differently can spend more effort on reporting and classification than on judgment. Whether a reusable decision should be reflected back into knowledge or principles is itself context-dependent. Autonomy means discretion in interpretation and working method; it does not mean authority to arbitrarily alter [sources of truth and evidence](source-of-truth.md) and turn them into facts.

Autonomous judgment can coexist with tools that check explicitly defined constraints. Agents judge choices that depend on context, while tools verify mechanically checkable conditions such as files, links, and review baselines. Passing [publication checks](distribution.md) does not by itself establish semantic accuracy or [suitability for disclosure](disclosure-boundary.md).

The same principle carries into [adoption judgment](adoption.md). Work types, scope categories, suggested questions, and procedures are defaults that support judgment. Understand the target and user intent first, then omit, combine, or adapt them as needed, and do not ask again about choices that have already been delegated. Even when the user delegates judgment, leave the actual decisions and usage instructions needed for later operation.

OKF's human-readable format, portability, and ease of version control remain useful without an LLM. The reason to prioritize autonomous judgment is specifically to make fuller use of agents' ability to interpret and maintain a natural-language knowledge graph.

[^okf-spec-v02]: [OKF v0.2 §4: Concept documents](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#4-concept-documents), [§6.1: Links between concepts](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#61-links-between-concepts). Prioritizing autonomous judgment when using this format is Mekra's own choice.
