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

Being a source of truth does not guarantee that a statement is objectively true. It establishes what serves as the reference, within what scope, and where the content is defined and changed. Having a source of truth for an observation, claim, or interpretation does not by itself establish the external facts it describes.

Claims and hypotheses whose truth is not established can still be recorded with their status and evidence made clear. Deciding where to maintain and update a record is distinct from accepting its claim as fact. There is no need to force every interpretation to have a source of truth that guarantees objective truth. When restating it in related concepts, preserve the necessary evidence and scope so that a recorded statement does not become an established fact.

Restating the context each concept needs is a choice intended to reduce the burden of reconstructing meaning from several sources while reading. It also creates the cost of finding and updating related restatements when the source of truth changes. Judge this balance by its usefulness for understanding and its maintenance cost during change, rather than the amount of duplicated text.

## Temporal validity and corrections

When updating a current source of truth, distinguish a change in the subject's state from a correction to a past explanation. For example, if a policy changes next month, the earlier policy may remain evidence for the earlier period. An explanation based on a misreading of the source needs a correction and a link to the current reference; it should not be preserved as a policy that was valid at the time.

The time something was recorded or retrieved may differ from the time its content applies to. Use evidence for the relevant period and conditions, depending on whether the question concerns the current state or a past judgment. If dates or conditions change the conclusion, make their scope clear in the prose or evidence references. A recent document edit alone does not establish current validity.

Consider both the need to retain historical records and the need to change current explanations. If a change in current facts or a correction to a past interpretation alters related concepts, [update their context](context-propagation.md). Express temporal differences where they affect understanding and reuse, without requiring period fields in every document.

## Paths to current sources of truth and historical evidence

The path to a current definition and the evidence needed to reconstruct a past judgment may serve different roles. Preserve the conditions of the time in historical copies and provide a path to the current baseline, so an old explanation found through search is not treated as the current source of truth. Do not rewrite historical statements retroactively to fit current policy.

If evidence came from a document in a temporary branch or worktree, check whether the readers who need it can still reach it after integration or relocation. When reconnecting to a corresponding document in the main repository, compare the cited content and version, and preserve the baseline needed for the historical judgment. A matching filename alone does not justify substitution. A path missing from one copy is not evidence that the material has disappeared from its original environment. A working link or matching content hash does not guarantee that the content is current, true, or approved.

## Decision criteria

- Is it clear where the fact is defined and changed?
- Is the restated content prevented from becoming an independently maintained source of truth?
- When the source of truth changes, can the contexts that should be reviewed with it be found?

The thing to avoid is not repeating the same fact, but independently defining and changing the same fact in multiple places.

Because [internalization](knowledge-internalization.md) aims at understanding each concept rather than merely copying the source of truth, restatement may be necessary. [Context propagation](context-propagation.md) is how those restatements are kept from becoming stale.
