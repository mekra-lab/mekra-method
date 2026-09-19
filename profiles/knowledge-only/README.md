# Knowledge-only

Use this profile for repositories where knowledge itself, rather than code, is the primary output.

## Recommended starting point

```text
repo/
├─ okf/
├─ raw/        # when source material should be preserved
├─ README.md
└─ AGENTS.md
```

## Key choices

- `raw/` contains source material; `okf/` contains curated and internalized knowledge.
- Do not reproduce all source material inside OKF. Internalize concepts, rules, and relationships that are repeatedly used for judgment.
- Add `docs/` when task guidance for collection, OCR, ingestion, or similar work accumulates enough to benefit from separate management. If it remains small, guidance in the README or relevant work directory is sufficient. Operational knowledge such as criteria for adopting material and evaluating evidence can live in OKF.
- When provenance, identifiers, rights, or preservation locations of source material matter, manage them in a ledger or manifest at the root of `raw/`.

Add `extracted/` when text extractions are reused repeatedly or expensive to regenerate. Treat extractions as derivatives rather than canonical source material.

After adoption, distinguish the preservation location for new originals from the location for directly authored knowledge. For example, originals might go in `raw/` and curated concepts in `okf/`; existing authoring locations can also be retained. Record the actual choices and a request such as "reflect the new materials in OKF" in the target README.

Related patterns: [External sources](../../okf/external-sources.md), [Source of truth](../../okf/source-of-truth.md)
