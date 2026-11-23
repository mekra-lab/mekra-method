---
type: Concept
title: The role and use of OKF
description: Explain the OKF representation model and bundle boundaries used by Mekra, distinguishing the official format from operating judgments
sources:
  - id: okf-spec-v03
    resource: https://github.com/open-knowledge-format/open-knowledge-format/blob/527e81aff55992be21507e97004286789126f88c/SPEC.md
    title: Open Knowledge Format v0.3
---

# The role and use of OKF

Mekra currently requires Open Knowledge Format (OKF) as its knowledge representation format. There is no need to convert all existing material or sources of truth; Mekra knowledge reuses existing OKF or is organized in OKF. A non-OKF arrangement that only adds operating guidance does not count as completed Mekra adoption.

OKF provides a format that people and agents can read and exchange, while Mekra provides an approach to deciding what knowledge to retain and how to connect and maintain it. Requiring OKF is the current Mekra adoption criterion and can be reconsidered if actual applications reveal a need for other representations.

## Representing concepts and relationships

An OKF concept document consists of YAML frontmatter and a Markdown body. Every concept requires `type`, and concept types are not restricted to a centrally fixed list. The body has no required sections; relationships between concepts are expressed through Markdown links and the surrounding natural language. Links express directed, untyped relationships. The surrounding prose conveys what each relationship means.[^okf-spec-v03]

Resolve links and path field values starting with `/` from the bundle root. Resolve other relative values from the directory containing the file in which they appear. Values that resolve outside the bundle root are external references. Consumers reading the bundle on its own do not read these targets from the local filesystem.[^okf-spec-v03]

Mekra uses this representation to [internalize](knowledge-internalization.md) definitions, reasons, conditions, exceptions, and effects on other concepts. Relying on [autonomous judgment](agent-autonomy.md) to interpret relationships and determine the scope of change is Mekra's operating choice. Consider both whether files follow the format and whether their knowledge is sufficient for judgment.

## Bundle boundaries and location

A bundle is a directory tree of knowledge documents and may be distributed as a whole repository or a subdirectory of a larger one. The names `index.md` and `log.md` are reserved at every depth. Other `.md` files are concepts if their frontmatter contains a non-empty `type`. Markdown files without frontmatter or a `type` field can still belong to a conforming bundle without counting as concepts. Files without the `.md` extension are assets.[^okf-spec-v03]

In bundles that Mekra puts together, treat documents with frontmatter as concepts and always give them a `type`. This authoring convention keeps intended concepts from being silently skipped when `type` is missing. The convention goes beyond the specification's requirements. Non-concept guides such as `README.md` may omit frontmatter. Tools that only support v0.2 may still try to read these documents as concepts. Check which version your tools support against the [current OKF baseline](../versions/current.md).

Agents reading the full repository can also use links to documents outside the bundle as discovery paths. When distributing or consuming the bundle on its own, those targets are unavailable. Check whether the knowledge in the bundle is sufficient for the judgments readers need to make.

The official specification does not prescribe `okf/` as the bundle directory name. The default `mekra/` location for a new file-based Mekra is also a Method adoption choice, not an official format requirement. Choose a target's bundle boundaries from the existing location of its knowledge and what needs to move together. [Structure and discovery](structure-and-discovery.md#bundle-location-and-existing-structure) explains those choices.

`index.md` is an optional reserved file that supports navigation by collecting concept links and short descriptions, and it can be generated automatically. Only the bundle-root `index.md` may have frontmatter. Its frontmatter holds `okf_version`, optional `title`, `description`, and `license` fields, and extension keys. Tools that regenerate the index must preserve the existing frontmatter.[^okf-spec-v03] In Mekra, use `title` and `description` when there is a bundle name and a scope to convey. Include `license` only after confirming the rights. Write `description` as one sentence that helps readers choose among bundles without repeating the purpose stated in `MEKRA.md`.

In Mekra, an index may also own unique navigation information, such as question-based groupings and reading order. When regenerating an index, choose an update method that preserves this navigation information and the necessary metadata. Domain rules and evidence belong in the relevant concepts, while responsibility for changing navigation information may remain with the index. This applies [source of truth and context](source-of-truth.md) to index maintenance; it is not a specification rule guaranteeing the preservation behavior of a particular generator.

## Choosing specification features

OKF v0.3 provides fields for provenance, generation, verification, and lifecycle information, `superseded_by` to point to a deprecated concept's replacement, and a format for attested computation. Consult the official specification for the conditions applying to each field and concept type.[^okf-spec-v03] A [minimal template](../templates/mekra/concept.md) does not limit the available forms of expression.

In Mekra, choose the representation needed for information you actually have to convey, such as traceable sources, the scope of completed verification, or judgments about validity. Metadata and prose should refer to the same evidential scope. The presence or number of attributes alone does not establish accuracy, freshness, or adoption. These choices also follow the [operating principles](../PRINCIPLES.md).

In v0.3, the trust tier is calculated using only verification from the last meaningful change (`generated.at`) onward. A lower tier is appropriate when the changed content has yet to be verified again. Leave verification records and timestamps alone when the only work done is a format conversion, translation, or link repair. Use `superseded_by` when existing references to a moved or replaced concept need to keep working. Use links in the body for ordinary related documents.

## Responsibilities of the format and the method

The OKF specification is the source of truth for the official format. The edition Mekra uses is recorded in the [current OKF baseline](../versions/current.md). This concept explains the context needed to use the format without reproducing the entire specification.

Autonomous judgment, the management of sources of truth and context, facets, the `MEKRA.md` entry point for each Mekra, and the `MEKRAS.md` index for environments using multiple Mekras are approaches adopted by Mekra. They are not additional OKF requirements. Updating Mekra's operating approach and migrating to another OKF format version may serve different needs and have different effects; the [version guide](../versions/README.md) and [adoption judgment](adoption.md) distinguish them.

[^okf-spec-v03]: [OKF v0.3 §3: Bundle structure and how to identify concepts](https://github.com/open-knowledge-format/open-knowledge-format/blob/527e81aff55992be21507e97004286789126f88c/SPEC.md#3-bundle-structure), [§4: Concept documents](https://github.com/open-knowledge-format/open-knowledge-format/blob/527e81aff55992be21507e97004286789126f88c/SPEC.md#4-concept-documents), [§5: Provenance, trust, and lifecycle](https://github.com/open-knowledge-format/open-knowledge-format/blob/527e81aff55992be21507e97004286789126f88c/SPEC.md#5-provenance-trust-and-lifecycle), [§6: Links and paths](https://github.com/open-knowledge-format/open-knowledge-format/blob/527e81aff55992be21507e97004286789126f88c/SPEC.md#6-links-and-paths), [§8: Index files and bundle metadata](https://github.com/open-knowledge-format/open-knowledge-format/blob/527e81aff55992be21507e97004286789126f88c/SPEC.md#8-index-files), [§10: Attested computations](https://github.com/open-knowledge-format/open-knowledge-format/blob/527e81aff55992be21507e97004286789126f88c/SPEC.md#10-attested-computations). These sections support the format descriptions; Mekra's operating choices are explained separately.
