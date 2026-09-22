# Corpus connection strategies and selection conditions

Status: research candidates · Compiled: 2026-09-22

The central question is: **Under which conditions should we combine which ways of connecting material so agents can find and understand evidence and maintain knowledge after changes?** The approaches and combinations below are candidates for investigation, not implementation patterns validated in Mekra or required components.

## Adopted judgments and research scope

Responsibilities for originals and derivatives belong in [source material and derivatives](../okf/external-sources.md). The boundary between selection and internalization belongs in [knowledge organization for large corpora](../okf/large-corpus.md). The judgment that facets and implementation techniques do not correspond one to one has been incorporated into [the role and boundaries of facets](../okf/facet-boundaries.md).

[Large corpus](../facets/large-corpus.md) is an entry point for environments where scale or complexity changes selection and discovery. This note addresses the broader problem of connecting material. Precise relationships, external system queries, or inspection of the original layout can matter even in small collections.

## Different roles within the same list

Full Markdown conversion, PDF indexes, ontologies, corpus databases, APIs, and other databases are not mutually exclusive alternatives. They can coexist in one arrangement.

| Candidate | Main role to consider | Distinction to preserve |
| --- | --- | --- |
| Converting all material to Markdown | A derived representation that is easier to read and search | Conversion scope and knowledge internalization scope are separate. Check whether the meaning conveyed by tables, figures, and layout is preserved. |
| Indexes attached to PDFs or other documents | Paths back to documents, passages, pages, tables, and figures | Document catalogs, summaries, annotations, and search indexes can do different jobs. |
| Ontologies | Explicit representation of the meaning and constraints of concepts and relationships | A linked graph or a graph database does not by itself provide the same role. |
| Corpus databases | Retaining and querying a collection of material | This describes a role, not a single technology. Originals, metadata, extractions, and search indexes may be managed together or separately. |
| APIs | Access to material or query capabilities | An API can expose storage, databases, or search; it is not a separate storage approach that replaces them. |
| Other databases | Managing and querying structured content such as business facts, tabular data, and relationships | Determine whether the database is a business source of truth, a replica, or a regenerable derivative for discovery. |

These distinctions explain choices; they are not a new metadata classification system. Start by examining the tools and material flows already present in the target.

## Implementation options to investigate

These are neither fixed stages nor a checklist to complete. Compare only what actual questions and material call for.

| Option | Situation to investigate | Question to test |
| --- | --- | --- |
| Direct access to originals | Existing tools can read the needed sources | Can they find and interpret the evidence passage without a separate derivative? |
| Complete text or Markdown derivatives | Broad coverage is repeatedly searched or cited | Does repeated use justify conversion, review, and update costs? |
| On-demand extraction or OCR with caching | Access concentrates on part of the material | What determines whether to extract again or retain a corrected result? |
| Per-document indexes and annotations | Pages, tables, figures, or paragraphs must be located in PDFs | Can the same evidence be checked after the original is revised or rearranged? |
| Metadata catalogs | Candidates should first be narrowed by source, period, or topic | Is the information needed for selection actually available and maintained? |
| Topic maps and hierarchical summaries | Questions span several sources and need a starting point | Is there a path to check conditions and counterexamples omitted from the summary? |
| Full-text search | Exact terms or phrases matter | How will we find material missed because of wording differences and inspect context around a quotation? |
| Semantic or hybrid search | Questions and originals use different wording | How will we distinguish a similar sentence from evidence that actually supports the claim? |
| Structured database queries | Filtering, aggregation, or relationship queries matter | Can we trace the original records and the definitions that give the result its meaning? |
| Relationship graphs and ontologies | Relationship discovery or explicit semantics and constraints matter | Are informal links sufficient, or is separately maintaining relationship definitions and constraints worthwhile? |
| APIs and queries across sources | External systems manage the material | How do permissions, query conditions, and source updates affect the ability to recheck evidence? |

## The hypothesis of operating with an ontology

The hypothesis is that **an ontology may support Mekra's knowledge operations where recurring relationship queries or precise semantics and constraints matter**. Intellectual influence, as recorded in the introduction, and the effectiveness of an implementation are separate claims. An influence does not imply that an ontology layer is already in use or has been validated.

Two possible arrangements can be investigated.

- **An existing ontology holds canonical definitions:** maintain concept and relationship definitions there, while related OKF concepts internalize the reasons, conditions, and context needed for judgment. Check which explanations must change when a definition changes.
- **An ontology or graph is a derivative:** build a representation for discovery or querying from existing sources of truth, with responsibility for generation, correction, and regeneration made clear. When modifying the derivative, distinguish changes that belong in the source of truth.

These are candidate arrangements to test. They do not establish an ontology as a fixed layer beneath Mekra or require all natural-language knowledge to be converted into an ontology. Corpus scale and the need for formalization are separate judgments. A small collection may require precise relationships; a large one may meet its purpose with search and summaries.

## Examples of combinations to investigate

These are hypothetical illustrations, not recommended presets or observed successes.

- For PDFs, one could test a combination of preserved originals, a document catalog, OCR of selected pages, and links to evidence by page, while retaining recurring judgment criteria in OKF.
- For an external business database, one could test reading current records through an API or queries while explaining terms, calculation conditions, and exceptions in OKF. Whether all records need Markdown copies is a separate decision.
- Where relationship definitions matter, one could compare keeping an existing ontology canonical and connecting natural-language context with generating a discovery graph from existing documents.

## Next validation

Choose real material and recurring questions, then use the current approach to **find evidence → understand its context → make a judgment → update after a source change**. Identify where it falls short and compare the smallest useful addition.

Observe whether the right evidence passage was found, whether the conclusion preserves its conditions, whether outdated indexes, summaries, and concepts were discovered and updated after a change, and how much search time and maintenance effort this required. Retrieval success or passing checks alone does not establish semantic accuracy.

For the ontology hypothesis, compare against simple links and natural-language definitions to identify the recurring queries or changes where a difference appears. Once useful conditions and costs are clear, incorporate only the reusable judgments into the relevant concepts or patterns. No implementation or effectiveness results are available yet.

## Implementation references

External sources checked: 2026-09-22. These primary sources establish capabilities of individual techniques, not the effectiveness of combining them with Mekra.

- [W3C OWL 2 Overview](https://www.w3.org/TR/owl2-overview/): an example of ontology representation with formal semantics. This does not imply that all ontologies must use OWL.
- [W3C Web Annotation Data Model](https://www.w3.org/TR/annotation-model/): examples of identifying target passages through quotations and text positions. Connections still need checking after source changes.
- [SQLite FTS5](https://www.sqlite.org/fts5.html): an example of full-text search and indexes maintained separately from original content.
- [pgvector](https://github.com/pgvector/pgvector): an example of vector similarity search in PostgreSQL and combination with full-text search.
