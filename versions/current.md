# Current OKF baseline

This document records the recommended baseline for the official specification. The [version guide](README.md) distinguishes Mekra Method releases from the commits actually consulted.

| Item | Value |
| --- | --- |
| Recommended baseline | OKF v0.2 |
| Official specification | [SPEC.md](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/main/SPEC.md) |
| Verified on | 2026-09-18 |
| Verified SPEC blob | `c06e3eede0c910d0ecf12524c34204156f8795ac` |
| Fixed specification reference | [SPEC.md @ ad30107](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md) |

The official specification link opens the current upstream document; the fixed link opens the reference matching the blob above. On 2026-09-26, the GitHub API confirmed that the `SPEC.md` blob at that fixed link matches this record. This checks the reference path for the existing baseline; it does not review all current upstream changes or adopt a new baseline.

## Use in this repository

- New templates and facets use v0.2 by default unless there is a specific reason not to.
- Existing bundles are not migrated merely because a newer version exists. Evaluate actual compatibility, benefit, and migration cost.
- This document does not duplicate the specification. Migration documents record only differences that affect how this repository operates.

In the currently verified v0.2, the only required frontmatter key for a concept is `type`, and a bundle-root `index.md` may declare `okf_version: "0.2"`. Provenance, trust, lifecycle, and attestation fields are optional and used when they add value.
