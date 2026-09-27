---
type: Principle
title: Mekra Method operating principles
description: Use autonomous judgment to maintain sources of truth and context, adapting knowledge, structure, and guidance to change and actual need
---

# Mekra Method operating principles

Mekra's operating principles guide how knowledge is organized and maintained so that agents can find the facts, reasons, and relationships needed for judgment in later work. The linked concepts explain each principle's reasoning and scope in detail.

## Autonomous judgment

Start from [autonomous judgment](agent-autonomy.md), and interpret and apply the principles below according to purpose and context. Facts, evidence, user intent, authority, and the target's constraints remain conditions of that judgment. Distinguish choices in an individual application from revisions to general principles.

Avoid continually adding detailed instructions for general matters that a capable LLM can judge from context. Provide enough facts, constraints, evidence, and context specific to the target to support that judgment.

## Sources of truth and context

Give facts and rules a clear [source of truth](source-of-truth.md) whenever practical. It holds responsibility for definition and change; concentrating that responsibility does not imply keeping all context in one place.

Knowledge needed to understand another concept should also be sufficiently [internalized](knowledge-internalization.md) from that concept's perspective. When one fact affects several concepts, reflect its meaning and impact in each. A source location or link alone cannot replace that explanation.

Do not avoid repetition itself. Avoid independently defining and maintaining the same fact in multiple places.

Knowledge about operating the knowledge base may itself be a subject of internalization. Reflect reusable meaning, constraints, and decision criteria in relevant concepts regardless of document location, while preserving the responsibilities and evidential scope of [source material and derivatives](external-sources.md).

## Reflecting changes

When new knowledge or a change arrives, [update](context-propagation.md) the source of truth and related concepts whose meaning changes. A link alone does not make a document an update target; examine where meaning, conditions, relationships, or judgments actually change.

Distinguish the scope of material preserved or processed from the conclusions adopted. Make uncertainty and its evidence clear, and preserve both the degree of certainty and [disclosure boundaries](disclosure-boundary.md) when carrying knowledge into other contexts.

## Reassessing structure and guidance

Choose structure, length, depth of internalization, metadata, and working practices according to the target's purpose and actual use. Keep valid knowledge and structure, and split, connect, combine, or simplify them as needed. Reassess these choices through [adoption experience](feedback.md), observing actual discovery, judgment, and the burden of updates.

[Self-erasure](self-erasure.md) applies the same judgment to supporting guidance and the method itself. Reduce their role as the need for help diminishes, while preserving knowledge, responsibilities, evidence, and important decision history specific to the target.

## OKF and practical adoption

Mekra currently uses [OKF's representation model](okf-format.md). These operating principles are Mekra's adopted criteria for judgment within that setting. Distinguish official format requirements from operating choices; the specification baseline is kept in the [current OKF baseline](../versions/current.md).

[Adoption judgment](adoption.md) covers a target's current state, work scope, bundle location, and entry point choices. The [repository structure](../README.md#structure) describes the directory layout used here.
