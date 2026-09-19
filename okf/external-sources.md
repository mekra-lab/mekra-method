---
type: Pattern
title: Source material and derivatives
description: Separate the responsibilities of source material, extracted artifacts, and internalized knowledge
---

# External sources

## Problem

When source material is large or managed externally, moving all of it into OKF increases maintenance cost and creates ambiguity about the source of truth. On the other hand, recording only its location fails to internalize the knowledge needed for repeated judgment.

## Choice

Preserve source material in its original location or under `raw/` or `sources/`, and internalize in OKF the meanings and relationships repeatedly needed for understanding and judgment. Link the OKF knowledge back to the canonical location and supporting evidence of the source material.

Text extractions are derivatives, not source material. Preserve them as a separate layer such as `extracted/` only when they are reused repeatedly, expensive to regenerate, or accumulate manual corrections.

In [post-adoption usage guidance](adoption.md), connect these responsibilities to actual intake locations. Explain where to preserve new originals, where directly authored knowledge belongs, and how to reflect it in OKF. For external originals, explain the reference method; if no separate source-material intake is needed, do not create an intake directory.

## Decision criteria

- Is this information repeatedly needed across multiple judgments?
- Can the core concept only be understood by rereading the source material?
- Is the cost or loss involved in regenerating the extraction greater than the cost of preserving it?
- Can an internalized conclusion be traced back to its source material?

Decide what knowledge to bring in from source material based on the reuse value of [internalization](knowledge-internalization.md). Applying this boundary to large bodies of material is described in [knowledge organization for large corpora](large-corpus.md).
