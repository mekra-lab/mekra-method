# Current OKF baseline

| Item | Value |
| --- | --- |
| Recommended baseline | OKF v0.2 |
| Official specification | [SPEC.md](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/main/SPEC.md) |
| Verified on | 2026-09-18 |
| Verified SPEC blob | `c06e3eede0c910d0ecf12524c34204156f8795ac` |

## Use in this repository

- New templates and facets use v0.2 by default unless there is a specific reason not to.
- Existing bundles are not migrated merely because a newer version exists. Evaluate actual compatibility, benefit, and migration cost.
- This document does not duplicate the specification. Migration documents record only differences that affect how this repository operates.

In the currently verified v0.2, the only required frontmatter key for a concept is `type`, and a bundle-root `index.md` may declare `okf_version: "0.2"`. Provenance, trust, lifecycle, and attestation fields are optional and used when they add value.
