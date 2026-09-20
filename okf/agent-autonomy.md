---
type: Principle
title: Autonomous agent judgment
description: Prioritize autonomous judgment so OKF can benefit from natural-language context and flexible relationships
---

# Autonomous agent judgment

Prioritize the agent's autonomous judgment. The principles below are starting points for judgment and may be applied differently depending on purpose and context.

## Why this connects to OKF's strengths

OKF expresses knowledge through minimal structured metadata, free-form bodies, and Markdown links. The concrete meaning of a relationship is carried by natural language around the link, and neither concept types nor body structure are fully prescribed by a fixed taxonomy. The format itself is defined by the [official specification](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/main/SPEC.md).

With this structure, agents can read explanations intended for people and interpret conditions, exceptions, and relationships in light of the actual question. New knowledge can be connected to existing concepts without encoding every possible relationship and case in advance as schema or branching logic. To preserve that flexibility, we rely on contextual interpretation and autonomous judgment by capable LLMs. This is not an attitude required by the official specification; it is an operating philosophy chosen to take advantage of its expressive style.

To use that advantage, the agent must be able to judge what concepts to create, how deeply to [internalize](knowledge-internalization.md), and how far a change should [propagate](context-propagation.md) based on the actual content. Replacing these choices with detailed authoring rules and fixed procedures can shift the work toward formal compliance rather than meaning.

## Operational implications

Keep repository instructions focused on purpose and repository-specific choices. Do not repeat generic guidance that can already be inferred from the specification and context. [Operating principles](operating-principles.md) provide judgment criteria, while [facets](../facets/README.md) help identify which judgments become especially important for a target. Facets do not prescribe structure; directory organization is chosen from actual need.

Autonomous judgment depends on sufficient knowledge. Even when instructions are brief, the body should [internalize](knowledge-internalization.md) enough reasons, conditions, and relationships for judgment. Omitting domain facts or repository-specific context that the agent does not already know is not the intent of this principle.

The ability to interpret context is distinct from the process of finding and reading the context needed. An agent may understand one concept well yet fail to discover another affected concept. Reliable autonomous judgment depends on the evidence and context actually explored as well as reasoning ability; [context propagation](context-propagation.md) must account for these limits of discovery.

Requiring a separate deviation record every time a principle is applied differently can spend more effort on reporting and classification than on judgment. Whether a reusable decision should be reflected back into knowledge or principles is itself context-dependent. Autonomy means discretion in interpretation and working method; it does not mean authority to arbitrarily alter [sources of truth and evidence](source-of-truth.md) and turn them into facts.

The same principle carries into [adoption judgment](adoption.md). Work types, scope categories, suggested questions, and procedures are defaults that support judgment. Understand the target and user intent first, then omit, combine, or adapt them as needed, and do not ask again about choices that have already been delegated. Even when the user delegates judgment, leave the actual decisions and usage instructions needed for later operation.

OKF's human-readable format, portability, and ease of version control remain useful without an LLM. The reason to prioritize autonomous judgment is specifically to make fuller use of agents' ability to interpret and maintain a natural-language knowledge graph.
