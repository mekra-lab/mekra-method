---
type: Concept
title: Knowledge organization for large corpora
description: Internalize core concepts and connect detailed evidence through summaries and discovery paths
---

# Knowledge organization for large corpora

As a body of material grows, the cost of turning every detail into concept documents and the propagation cost of change both increase. In that situation, OKF should maintain a core concept graph while also providing summaries and paths back to the original material.

[Internalize](knowledge-internalization.md) meanings, conditions, and decision criteria that are needed repeatedly, and link infrequently needed details to their supporting locations. Do not set the boundary solely by the number or size of source documents. Summaries and indexes may be kept together or separated depending on their roles.

[Source material, extracted artifacts, and knowledge](external-sources.md) have different responsibilities. Decide whether to preserve extracted artifacts based on factors such as image-based PDFs, the amount of tables and figures, searchability, reuse value of extraction results, and regeneration cost. Figures or layouts that cannot be understood from text extraction alone still require reference to the original material.

Humans should also be able to read concept documents and navigate back to the source. Separate human and agent versions are not inherently necessary; broader topic summaries may be added when they improve navigation.

A concrete directory starting point is provided by the [large-corpus profile](../profiles/large-corpus/README.md). Domains such as medicine and law, where provenance and applicability conditions matter, can begin with this structure and evolve into separate profiles when their actual requirements diverge.
