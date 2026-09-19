# Large corpus

Use this profile for hundreds or thousands of PDFs, image-based documents, or materials accumulated over time. OKF plays a stronger role as a concept graph, a set of core summaries, and a set of discovery paths than as a place to copy every source document.

## Recommended starting point

```text
repo/
├─ okf/
├─ sources/
├─ extracted/   # optional
├─ docs/
└─ AGENTS.md
```

## Key choices

- Preserve source material under `sources/` or in external storage.
- Put repeatedly used core concepts, relationships, decision criteria, and paths back to source material in `okf/`.
- Do not create an OKF entry for every document by default. Split concepts based on whether they are worth explaining and referencing independently.
- Leave infrequently needed details in the source material, while internalizing knowledge that would otherwise require important judgments to be reconstructed from the originals every time.

## When to keep extracted artifacts

Preserving extraction results is worthwhile when they are reused, expensive to regenerate, or accumulate manual corrections to OCR, tables, or paragraph structure. If they can be regenerated cheaply and deterministically, preserving the pipeline while generating outputs on demand may be enough.

Evaluate quality by whether core questions can be understood from OKF and whether answers can be traced back to supporting source material, rather than by the percentage of the source corpus that has been converted.

After adoption, explain whether new originals belong in `sources/` or external storage, and where to record reference locations and identifiers. If extracted artifacts are kept, link their generation and update method. Leave the location for directly authored knowledge and the incorporation request method in the target README or collection guide. For progressive migration, also explain the remaining material scope and the triggers for processing it.

The reasoning behind this configuration is described in [knowledge organization for large corpora](../../okf/large-corpus.md).
