# Versions

Track upstream OKF changes and record how they affect this repository's principles, patterns, and profiles.

- [`current.md`](current.md): current recommended baseline and the verified upstream reference point
- [`migrations/`](migrations/): changes that require an actual transition between versions

## How to incorporate a new change

1. Check the version and diff of the official `SPEC.md`.
2. Evaluate format compatibility, semantic changes, and effects on operating principles and templates separately.
3. Update only the documents that need to change and record whether existing projects require migration.
4. Decide the recommended version for new projects separately from the migration priority for existing projects.

Do not infer compatibility from the version number alone. The specification can change under the same version label, so record the verification date and upstream file reference point as well.
