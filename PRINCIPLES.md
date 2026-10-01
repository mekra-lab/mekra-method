# Mekra Method operating principles

Mekra's operating principles guide how knowledge is organized and maintained so that agents can find the facts, reasons, and relationships needed for judgment in later work. This document owns the list of principles, their core meaning, and their relationships; the linked concepts own the detailed meaning, reasoning, and application boundaries. When revising a principle, update both the summary and the detailed explanations whose meaning changes.

## Autonomous judgment

Start from [autonomous judgment](okf/agent-autonomy.md), and interpret and apply the principles below according to purpose and context. Facts, evidence, user intent, authority, and the target's constraints remain conditions of that judgment. Distinguish choices in an individual application from revisions to general principles.

Avoid continually adding detailed instructions for general matters that a capable LLM can judge from context. Provide enough facts, constraints, evidence, and context specific to the target to support that judgment.

## Preserving epistemic distinctions

[Preserve epistemic distinctions that matter for judgment](okf/epistemic-distinctions.md). Do not silently replace claims, perspectives, or uncertainty in the material or the user's account with newly established facts or the agent's interpretation. Distinguish observations, claims, and inferences made at the same time as well. When correcting an account, connect earlier context needed for later judgment to the current assessment. This principle does not require retaining errors as facts, preserving every perspective or historical record, or using fixed fields.

## Sources of truth and context

Give facts and rules a clear [source of truth](okf/source-of-truth.md) whenever practical. It holds responsibility for definition and change; concentrating that responsibility does not imply keeping all context in one place.

Knowledge needed to understand another concept should also be sufficiently [internalized](okf/knowledge-internalization.md) from that concept's perspective. When one fact affects several concepts, reflect its meaning and impact in each. A source location or link alone cannot replace that explanation.

Do not avoid repetition itself. Avoid independently defining and maintaining the same fact in multiple places.

Knowledge about operating the knowledge base may itself be a subject of internalization. Reflect reusable meaning, constraints, and decision criteria in relevant concepts regardless of document location, while preserving the responsibilities and evidential scope of [source material and derivatives](okf/external-sources.md).

## Reflecting changes

When new knowledge or a change arrives, [update](okf/context-propagation.md) the source of truth and related concepts whose meaning changes. A link alone does not make a document an update target; examine where meaning, conditions, relationships, or judgments actually change.

The [default operating model](okf/context-propagation.md#human-and-agent-roles) is for people to supply new facts, intent, evidence, and corrections, while the agent explores related context and updates the source of truth and affected knowledge together.

Distinguish the scope of material preserved or processed from the conclusions adopted. Make uncertainty and its evidence clear, and preserve both the degree of certainty and [disclosure boundaries](okf/disclosure-boundary.md) when carrying knowledge into other contexts.

## Reassessing structure and guidance

Choose structure, length, depth of internalization, metadata, and working practices according to the target's purpose and actual use. Keep valid knowledge and structure, and split, connect, combine, or simplify them as needed. Reassess these choices through [adoption experience](okf/feedback.md), observing actual discovery, judgment, and the burden of updates.

[Self-erasure](okf/self-erasure.md) applies the same judgment to supporting guidance and the method itself. Reduce their role as the need for help diminishes, while preserving knowledge, responsibilities, evidence, and important decision history specific to the target.

## OKF and practical adoption

Mekra currently uses [OKF's representation model](okf/okf-format.md). These operating principles are Mekra's adopted criteria for judgment within that setting. Distinguish official format requirements from operating choices; the specification baseline is kept in the [current OKF baseline](versions/current.md).

Start practical adoption with the [application guide](APPLICATION.md). [Adoption judgment](okf/adoption.md) covers the detailed reasoning for a target's current state, work scope, bundle location, and entry point choices. The [repository structure](README.md#structure) describes the directory layout used here.