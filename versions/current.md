# Current OKF baseline

| Item | Value |
| --- | --- |
| Recommended baseline | OKF v0.2 |
| Official specification | [SPEC.md](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/main/SPEC.md) |
| Verified on | 2026-09-18 |
| Verified SPEC blob | `c06e3eede0c910d0ecf12524c34204156f8795ac` |

## Application in this repository

- New templates and profiles target v0.2 unless there is a specific reason not to.
- Existing bundles are not migrated merely because a new version exists. Evaluate actual compatibility, benefits, and migration cost.
- This document does not duplicate the specification. Migration documents record only differences that affect this repository's operating approach.

In the currently verified v0.2 specification, the only always-required frontmatter key for a concept is `type`, and a bundle-root `index.md` may declare `okf_version: "0.2"`. Provenance, trust, lifecycle, and attestation fields are used when needed.
