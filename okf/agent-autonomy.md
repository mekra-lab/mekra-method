---
type: Principle
title: Agent autonomy
description: Prioritize autonomous judgment to make use of OKF's natural-language context and flexible relationship expression
---

# Agent autonomy

Prioritize the agent's autonomous judgment. The principles below are starting points for judgment and may be applied differently depending on purpose and context.

## Why this connects to OKF's strengths

OKF represents knowledge with minimal structured metadata, free-form bodies, and Markdown links. The specific meaning of a relationship is conveyed by the natural language around a link, and neither concept types nor body structure are fully prescribed by a fixed taxonomy. The basis for the format is the [official specification](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/main/SPEC.md).

In this structure, agents can read explanations written for humans and interpret conditions, exceptions, and relationships in light of the actual question. New knowledge can be connected to existing concepts without predefining every relationship and case as schemas or branches. To preserve this flexibility, we rely on the contextual interpretation and autonomous judgment of capable LLMs. This is not a behavior required by the official specification, but an operating philosophy chosen to take advantage of its mode of expression.

Using that advantage requires judgment about which concepts to create, how deeply to [internalize](knowledge-internalization.md) knowledge, and how far changes should [propagate](context-propagation.md), based on the actual content. Replacing these choices with detailed writing rules and fixed procedures can shift work away from natural-language meaning toward formal compliance with rules.

## Operational implications

Keep instructions short and focused on the repository's purpose and unique choices. Do not repeat generic guidance that can be inferred from the specification and context. The [operating principles](operating-principles.md) and profiles are starting points for judgment, and directory structures should also be selected according to actual need. For example, a knowledge-only repository has no reason to inherit a development project's `docs/` layout unchanged.

Autonomous judgment depends on sufficient knowledge. Even when instructions are short, the body should sufficiently [internalize](knowledge-internalization.md) the reasons, conditions, and relationships needed for judgment. This principle does not justify omitting domain facts or repository-specific context that the agent does not yet know.

Requiring a separate deviation record every time a principle is applied differently can impose more reporting and classification cost than judgment value. Whether a reusable decision should be reflected in knowledge or principles is itself context-dependent. Autonomy means discretion in interpretation and working method; it does not mean permission to arbitrarily alter the [source of truth and evidence](source-of-truth.md) and present the result as fact.

The same reasoning applies to [adoption judgment](adoption.md). Operation types, scope, suggested questions, and procedures are defaults that support judgment. Understand the target and user intent first, omit, combine, or adapt the defaults as needed, and do not reconfirm choices already delegated. Record the actual choices and usage guidance so users who delegated judgment can still add materials and continue operating the result.

OKF's human-readable format, portability, and version-control friendliness remain useful without LLMs. The reason for prioritizing autonomous judgment is specifically to make full use of an agent's ability to interpret and maintain a natural-language knowledge graph.
