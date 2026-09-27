---
type: Pattern
title: Source material and derivatives
description: Separate the responsibilities of source material, derivatives, and internalized knowledge
---

# External sources

## Problem

When source material is large or managed externally, moving all of it into OKF increases maintenance cost and creates ambiguity about the source of truth. On the other hand, recording only its location fails to internalize the knowledge needed for repeated judgment.

## Choice

Preserve source material in its original location or under `raw/` or `sources/`, and internalize in OKF the meanings and relationships repeatedly needed for understanding and judgment. Link the OKF knowledge back to the canonical location and supporting evidence of the source material.

Text extracted from originals and transcriptions in Markdown are derivatives, not source material. When originals are difficult to work with directly and need to be searched or cited repeatedly, you can preserve them as the source of truth while creating derivatives in a reusable format and linking OKF concepts or summaries to the relevant evidence locations. Preserve these derivatives as a separate layer such as `extracted/` only when they are reused repeatedly, expensive to regenerate, or accumulate manual corrections. When an original changes, also examine the impact on retained derivatives and on knowledge internalized from them.

These responsibilities also apply to material accessed through databases or APIs. Storage or access technology alone does not establish canonical authority: distinguish a database that manages source material from a search database derived from it. A connection should lead beyond the repository address to the passage or record supporting a conclusion and the surrounding context needed to interpret it. When a source may change, preserve the version, retrieval time, or query conditions needed to recheck the evidence.

In [post-adoption usage guidance](adoption.md), connect these responsibilities to actual intake locations. Explain where to preserve new originals, where directly authored knowledge belongs, and how to reflect it in OKF. For external originals, explain the reference method; if no separate source-material intake is needed, do not create an intake directory.

## Roles and valid scope of materials

Distinguish ideas, hypotheses, and proposals under review from currently adopted knowledge. Preserving material or completing its review or processing does not by itself mean a proposal has been adopted. If only some conclusions were adopted, distinguish their scope from the remaining proposals and make the current baseline discoverable in the updated [source of truth](source-of-truth.md).

A form and a completed copy with the same name, or a transcript and a summary derived from the same original, have different roles. Identical extracted text does not mean the originals have the same tables, layout, or attachments. Do not count multiple derivatives of one original as independent evidence. A saved query result records the conditions at that time; when answering about the current state, check whether its retrieval time, coverage, and query conditions are still appropriate.

When a derivative contains an error, compare it with the source material to judge which claims it can still support, and [reflect the correction in related knowledge](context-propagation.md#when-confidence-in-evidence-decreases). Do not record the entire source as validated merely because a derivative was created or a checking tool was run.

Excluding source material from Git is a separate decision from retaining or disposing of it. If material is stored elsewhere, record the storage location and access method as needed so readers can tell what a repository clone can restore on its own.

## Decision criteria

- Is this information repeatedly needed across multiple judgments?
- Can the core concept only be understood by rereading the source material?
- Is the cost or loss involved in regenerating the derivative greater than the cost of preserving it?
- Can an internalized conclusion be traced back to its source material?

Decide what knowledge to bring in from source material based on the reuse value of [internalization](knowledge-internalization.md). Applying this boundary to large bodies of material is described in [knowledge organization for large corpora](large-corpus.md).
