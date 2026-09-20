---
okf_version: "0.2"
---

# OKF research and applied knowledge

This bundle internalizes operating philosophy and design judgments adopted through work with OKF. It distinguishes the official specification itself from our interpretations; the baseline for the official format is kept in the [version documentation](../versions/current.md).

The core perspective is a balance: concentrate definition and change responsibility in clear sources of truth, while distributing the context needed for understanding across related concepts. A source of truth prevents independent ownership of the same fact, while each concept may naturally restate what that fact means for itself. Distributing context does not distribute ownership of the fact, and when something changes, its effects propagate from the source of truth into contexts whose meaning changes.

## Operating philosophy

- [Operating principles](operating-principles.md) - keep clear source-of-truth responsibility together with the context needed for understanding.
- [Autonomous judgment](agent-autonomy.md) - prioritize autonomous judgment so OKF can benefit from natural-language context and flexible relationships.
- [Knowledge internalization](knowledge-internalization.md) - reflect the meaning and impact of new knowledge in related concepts.

## Reusable patterns and boundaries

- [Source of truth and context](source-of-truth.md) - centralize change responsibility while preserving necessary restatement.
- [Context propagation](context-propagation.md) - update concepts whose meaning changes.
- [Source material and derivatives](external-sources.md) - separate the responsibilities of source material, derivatives, and internalized knowledge.
- [Boundary between information access and external disclosure](disclosure-boundary.md) - distinguish information usable for internal judgment from authority to disclose or transmit it externally.
- [Knowledge organization for large corpora](large-corpus.md) - combine core knowledge with summaries and discovery paths.
- [Role and boundaries of facets](facet-boundaries.md) - use facets as thin lenses on properties of the target rather than presets or a duplicate knowledge layer.

## Application

- [Adoption judgment](adoption.md) - distinguish operating form, needed changes, and scope, then connect them to continued knowledge operation.
- [Feedback from adoption](feedback.md) - select reusable observations and feed them back into research and operating knowledge.
- [Research and multilingual distribution](distribution.md) - update language editions while preserving publication boundaries and a shared source of truth.
- [Application guide](../APPLICATION.md) - the default path from target exploration and questions through implementation and operational handoff.
- [Facets](../facets/README.md) - thin lenses for finding relevant judgment from important properties of a target.
- [Templates](../templates/README.md) - starting points to copy and adapt.
