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

Stop updating once confirmed impacts have been reflected. Keep uncertain impacts distinct from established facts by recording them in notes or as follow-up review items.

Even during a [progressive migration of operating practices](adoption.md), reflect the current change's effects on meaning together. Distinguish improvements that can wait from conflicts that must be resolved now, and record the remaining migration scope and its triggers. A full review does not require changing documents whose meaning and format remain suitable.

The [source of truth](source-of-truth.md) is the starting point for a change, while impact scope is left to the [agent's contextual judgment](agent-autonomy.md). Because the meaning of a relationship is expressed in natural language, the existence of a link alone cannot determine whether there is an impact, and concepts without existing links may still be affected. The autonomy to interpret these relationships is what turns OKF's flexible relationship expression into coordinated updates. The same principle applies when [source material](external-sources.md) changes.

## Limitations

Natural-language relationships and restatement help preserve the context each concept needs, but they do not guarantee that every semantic dependency can be tracked explicitly. When a source of truth or related knowledge changes, some concepts may therefore retain outdated meaning or decision criteria.

The actual frequency and conditions of this risk, and the appropriate methods for detecting it, are not yet settled. If the problem is repeatedly observed or a response is validated, use results from notes and experiments to incorporate a separate principle or pattern.
