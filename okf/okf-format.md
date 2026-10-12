---
type: Concept
title: The role and use of OKF
description: Explain the OKF representation model and bundle boundaries used by Mekra, distinguishing the official format from operating judgments
sources:
  - id: okf-spec-v02
    resource: https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md
    title: Open Knowledge Format v0.2
---

# The role and use of OKF

Mekra currently uses Open Knowledge Format (OKF) to represent knowledge and context. OKF provides a format that people and agents can read and exchange, while Mekra provides an approach to deciding what knowledge to retain and how to connect and maintain it.

## Representing concepts and relationships

An OKF concept document consists of YAML frontmatter and a Markdown body. `type` is always required, and concept types are not restricted to a centrally fixed list. The body has no required sections; relationships between concepts are expressed through Markdown links and the surrounding natural language.[^okf-spec-v02]

Mekra uses this representation to [internalize](knowledge-internalization.md) definitions, reasons, conditions, exceptions, and effects on other concepts. Relying on [autonomous judgment](agent-autonomy.md) to interpret relationships and determine the scope of change is Mekra's operating choice. Consider both whether files follow the format and whether their knowledge is sufficient for judgment.

## Bundle boundaries and location

A bundle is a directory tree of knowledge documents and may be distributed as a whole repository or a subdirectory of a larger one. Within a bundle, `index.md` and `log.md` are reserved filenames; other `.md` files are concept documents.[^okf-spec-v02]

The official specification does not prescribe `okf/` as the bundle directory name. The default `mekra/` location for a new file-based Mekra is also a Method adoption choice, not an official format requirement. Choose a target's bundle boundaries from the existing location of its knowledge and what needs to move together. [Adoption judgment](adoption.md#bundle-location-and-existing-structure) explains those choices.

`index.md` is an optional reserved file that supports navigation by collecting concept links and short descriptions, and it can be generated automatically.[^okf-spec-v02] In Mekra, an index may also own unique navigation information, such as question-based groupings and reading order. When regenerating an index, choose an update method that preserves this navigation information and the necessary metadata. Domain rules and evidence belong in the relevant concepts, while responsibility for changing navigation information may remain with the index. This applies [source of truth and context](source-of-truth.md) to index maintenance; it is not a specification rule guaranteeing the preservation behavior of a particular generator.

## Choosing specification features

OKF v0.2 provides fields for provenance, generation, verification, and lifecycle information, along with a format for attested computation. Consult the official specification for the conditions applying to each field and concept type.[^okf-spec-v02] A [minimal template](../templates/mekra/concept.md) does not limit the available forms of expression.

In Mekra, choose the representation needed for information you actually have to convey, such as traceable sources, the scope of completed verification, or judgments about validity. Metadata and prose should refer to the same evidential scope. The presence or number of attributes alone does not establish accuracy, freshness, or adoption. These choices also follow the [operating principles](../PRINCIPLES.md).

## Responsibilities of the format and the method

The OKF specification is the source of truth for the official format. The edition Mekra uses is recorded in the [current OKF baseline](../versions/current.md). This concept explains the context needed to use the format without reproducing the entire specification.

Autonomous judgment, the management of sources of truth and context, facets, the `MEKRA.md` entry point for each Mekra, and the `MEKRAS.md` index for environments using multiple Mekras are approaches adopted by Mekra. They are not additional OKF requirements. Updating Mekra's operating approach and migrating to another OKF format version may serve different needs and have different effects; the [version guide](../versions/README.md) and [adoption judgment](adoption.md) distinguish them.

[^okf-spec-v02]: [OKF v0.2 §3: Bundle structure](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#3-bundle-structure), [§4: Concept documents](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#4-concept-documents), [§5: Provenance, trust, and lifecycle](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#5-provenance-trust-and-lifecycle), [§6.1: Links between concepts](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#61-links-between-concepts), [§8: Index files](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#8-index-files), [§10: Attested computations](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#10-attested-computations-concept). These sections support the format descriptions; Mekra's operating choices are explained separately.
