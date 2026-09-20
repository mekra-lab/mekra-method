# Versions

Track changes in upstream OKF and record their impact on this repository's principles, patterns, and facets.

- [`current.md`](current.md): current recommended baseline and verified upstream reference
- [`migrations/`](migrations/): changes that require an actual transition between versions

## Flow for adopting a new change

1. Check the version and diff of the official `SPEC.md`.
2. Evaluate format compatibility, semantic changes, and impact on operating principles and templates separately.
3. Update only the documents that need it and record whether existing projects require migration.
4. Judge the recommended version for new projects separately from the migration priority of existing projects.

Do not infer compatibility from a version number alone. The specification can change while retaining the same version label, so record both the verification date and the upstream file baseline.
