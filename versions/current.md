# Current OKF baseline

This document records the recommended baseline for the official specification. The [version guide](README.md) distinguishes Mekra Method releases from the commits actually consulted.

| Item | Value |
| --- | --- |
| Recommended baseline | OKF v0.3 |
| Official repository | [open-knowledge-format/open-knowledge-format](https://github.com/open-knowledge-format/open-knowledge-format) |
| Official specification | [SPEC.md](https://github.com/open-knowledge-format/open-knowledge-format/blob/main/SPEC.md) |
| Verified on | 2026-11-23 |
| Verified SPEC blob | `0dc3f7aa0fc710e588ba918eb115935d41eb2943` |
| Fixed specification reference | [SPEC.md @ 527e81a](https://github.com/open-knowledge-format/open-knowledge-format/blob/527e81aff55992be21507e97004286789126f88c/SPEC.md) |

The official specification link opens the current upstream document; the fixed link opens the reference matching the blob above. On 2026-11-23, the GitHub API confirmed that `main` in the new official repository was at `527e81a` and that the `SPEC.md` blob matched this record. The former official repository, [GoogleCloudPlatform/open-knowledge-format](https://github.com/GoogleCloudPlatform/open-knowledge-format), states that development has moved to the new repository and no further updates are made there.

## Use in this repository

- New templates and facets use v0.3 by default unless there is a specific reason not to.
- Existing bundles are not migrated merely because a newer version exists. Evaluate actual compatibility, benefit, and migration cost. See the [v0.2 → v0.3 migration guide](migrations/v0.2-to-v0.3.md) for what to check when moving from v0.2.
- This document does not duplicate the specification. Migration documents record only differences that affect how this repository operates.

Under the verified v0.3 specification, a concept is a Markdown file with a non-empty `type` in its frontmatter. Markdown files without `type` can still belong to a conforming bundle without counting as concepts. A bundle-root `index.md` may declare `okf_version: "0.3"` and the optional fields `title`, `description`, and `license`. Provenance, trust, lifecycle, and attestation fields are optional and used when they add value.

## Tools that only support OKF v0.2

Among the external tools checked as of 2026-11-23, Google Knowledge Catalog's `kcmd` supports OKF as documented for v0.2 and rejects a push if `bundle/` contains a `.md` file without `type` ([PR #672](https://github.com/GoogleCloudPlatform/knowledge-catalog/pull/672)). If you need to exchange bundles with tools like this, you can keep the v0.2 layout by retaining `okf_version: "0.2"` and including `type` in every Markdown file in the bundle. Check which version a tool supports when you use it, since support can change.

## Previous baseline

| Period | Recommended baseline | Verified SPEC blob | Fixed reference |
| --- | --- | --- | --- |
| 2026-09-18 to 2026-11-23 | OKF v0.2 | `c06e3eede0c910d0ecf12524c34204156f8795ac` | [SPEC.md @ ad30107](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md) |

Keep using the links for that version in bundles built against the previous baseline and in the pinned references for past releases.
