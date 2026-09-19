---
type: Pattern
title: Source of truth and context
description: Centralize responsibility for change while preserving necessary restatement
---

# Source of truth

## Problem

Trying to keep a source of truth in one place can remove context that related concepts need. At the other extreme, several documents can end up independently owning the same fact.

## Choice

Keep responsibility for changing a fact or rule in one source of truth. When another concept needs that fact to understand its own meaning, conditions, or exceptions, restate it from that concept's perspective and link back to the source of truth.

A source of truth may be an OKF document, a policy source, code, configuration, schema, or an external document.

## Decision criteria

- Is it clear where the fact is defined and changed?
- Is the restated content prevented from becoming an independently maintained source of truth?
- When the source of truth changes, can the contexts that should be reviewed with it be found?

The thing to avoid is not repeating the same fact, but independently defining and changing the same fact in multiple places.

Because [internalization](knowledge-internalization.md) aims at understanding each concept rather than merely copying the source of truth, restatement may be necessary. [Context propagation](context-propagation.md) is how those restatements are kept from becoming stale.
