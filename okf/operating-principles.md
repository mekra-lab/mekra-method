---
type: Principle
title: OKF operating principles
description: Local operating principles for maintaining clear canonical responsibility together with necessary context
---

# OKF operating principles

Prioritize the agent's autonomous judgment. The principles below are starting points for judgment and may be applied differently depending on purpose and context.

Baseline: [Open Knowledge Format official specification](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/main/SPEC.md)

Use OKF to internalize curated knowledge as concepts and relationships. Do not reduce it to a simple document index or a list of source-material locations.

## Bundle location

OKF is a knowledge representation format and does not prescribe a directory name for bundles. The [official specification's bundle structure](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/main/SPEC.md#3-bundle-structure) permits a bundle to occupy a whole repository or a subdirectory of a larger one. `okf/` is neither a required name nor an officially recommended standard, and its use here should not be generalized into an established convention across the ecosystem.

This repository studies OKF itself and uses `okf/` to distinguish adopted knowledge from research material, templates, and tools. The roles below are choices made for this repository. [Choose](adoption.md) a different target's bundle location and name according to its purpose and existing structure.

| Location | Role |
| --- | --- |
| `okf/` | Concept meaning, boundaries, rules, relationships, and the context needed for judgment |
| `docs/` (optional) | Implementation or task guidance that benefits from separate management |
| `README.md` | Repository introduction, quick start, and major entry points |

## Principles

Give facts and rules a clear source of truth whenever practical. However, a single source of truth does not imply a single location for context.

Knowledge needed to understand another concept should also be sufficiently internalized from that concept's perspective. When one fact affects several concepts, reflect its meaning and impact in each of those concepts.

Do not avoid repetition itself. Avoid independently defining and maintaining the same fact in multiple places.

When implementation or task guidance accumulates enough to benefit from separate management, add `docs/` or an equivalent location. Knowledge about operating the knowledge base may itself be a subject of internalization, and reusable meanings, constraints, and decision criteria should be reflected in relevant OKF concepts regardless of document location.

When new knowledge or a change arrives, do not update only the source of truth; also update related concepts whose meaning changes.

Otherwise, choose structure, length, links, metadata, and writing style autonomously according to the official specification and the actual context.

These are local operating choices layered on top of the official format. We prioritize [autonomous judgment](agent-autonomy.md) to take advantage of OKF's natural-language context and flexible relationships, and determine the depth of [internalization](knowledge-internalization.md) by actual reuse value. Responsibility for canonical facts is described in [source-of-truth management](source-of-truth.md), and coordinated updates after change are described in [context propagation](context-propagation.md).
