---
type: Pattern
title: Context propagation
description: Update concepts whose meaning changes when knowledge changes
---

# Context propagation

## Problem

If new knowledge or a rule change is reflected only in the source of truth, related concepts can retain outdated meaning and decision criteria.

## Choice

Update concepts whose definitions, relationships, applicability conditions, exceptions, or judgments actually change. In each document, reflect the changed meaning for that concept rather than copying the entire source text.

## Scope

Consider not only existing links but also terminology and conceptual dependencies. Do not determine scope by file count or link distance, and do not modify every connected document merely because a connection exists.

If affected concepts have different disclosure scopes, reflect the meaning that may be shared in each location under the [disclosure boundary](disclosure-boundary.md). Consider what information is actually revealed even when summarizing a change or only linking a relationship.

Stop updating once confirmed impacts have been reflected. Keep uncertain impacts distinct from established facts by recording them in notes or as follow-up review items.

Even during a [progressive migration of operating practices](adoption.md), reflect the current change's effects on meaning together. Distinguish improvements that can wait from conflicts that must be resolved now, and record the remaining migration scope and its triggers. A full review does not require changing documents whose meaning and format remain suitable.

The [source of truth](source-of-truth.md) is the starting point for a change, while impact scope is left to the [agent's contextual judgment](agent-autonomy.md). Because the meaning of a relationship is expressed in natural language, the existence of a link alone cannot determine whether there is an impact, and concepts without existing links may still be affected. The autonomy to interpret these relationships is what turns OKF's flexible relationship expression into coordinated updates. The same principle applies when [source material](external-sources.md) changes.

## When confidence in evidence decreases

Even when source material is unchanged, discovering extraction errors or a misunderstanding of what was validated can change judgments drawn from it. For example, if an omission in an automatic transcript means a statement can no longer be regarded as confirmed, review both the transcript's explanation and assertions in concepts about decisions, responsibilities, or work that relied on it. Distinguish the scope where confidence has decreased from the scope still supported by other evidence.

Update current explanations with the reason for the correction, the valid scope of evidence, and what remains unconfirmed. Keep source material and past judgments traceable in history where retention is permitted, and connect them to the correction so current readers do not keep using withdrawn judgments. A list of corrected documents shows the update scope; it does not mean every connected claim has been validated again. When inputs or application conditions change, also recheck whether earlier validation results support the new judgment.

## Limitations

Natural-language relationships and restatement help preserve the context each concept needs, but they do not guarantee that every semantic dependency can be tracked explicitly. When a source of truth or related knowledge changes, some concepts may therefore retain outdated meaning or decision criteria.

As scale makes affected context harder to find, search or backlinks can help narrow the candidates for review. A candidate list supports semantic judgment; its existence or completed review does not prove that every impact has been found. Decide whether to introduce tools based on actual discovery effort and patterns of omission.

The actual frequency and conditions of this risk, and the appropriate methods for detecting it, are not yet settled. Use [operational observations](feedback.md) to examine outdated judgments left after changes and the cost of finding and correcting them. If the problem is repeatedly observed or a response is validated, use results from notes and experiments to incorporate a separate principle or pattern.
