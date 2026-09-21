# Versions

Track changes in upstream OKF and record their impact on this repository's principles, patterns, and facets. This guide also covers release baselines for the okf-method knowledge used to interpret and apply that specification.

- [`current.md`](current.md): current recommended baseline and verified upstream reference
- [`migrations/`](migrations/): changes that require an actual transition between versions

## Specification and guide baselines

| Baseline | Meaning |
| --- | --- |
| OKF specification version and verified file reference | The official format being interpreted and applied |
| okf-method release tag | A fixed publication baseline for operating knowledge adopted on top of that specification |
| Repository and commit of the guidance consulted | The actual state of the guide read when applying it to a target |

The public repositories' `main` branches hold the latest adopted guidance and continue to evolve. Releases provide baselines for comparison and reproduction; they are not issued for every change. Use the official specification version in a target bundle's `okf_version`, not a OKF Method release name.

## okf-method releases

OKF Method is the new name for OKF Lab. The repositories were renamed from `okf-lab`, `okf-lab-kr`, and `okf-lab-dev` to `okf-method`, `okf-method-kr`, and `okf-method-dev`, respectively. Preserve the existing `okf-0.2-lab-1` tag and its commit as a historical baseline; do not retroactively rename repositories or tags in past adoption records.

New releases after the rename use the `method` convention below, starting at `okf-0.2-method-1` even on the same OKF 0.2 baseline. The rename itself does not publish a release or change the OKF specification version of a target bundle.

Tags follow `okf-<spec-version>-method-<sequence>`. For example, `okf-0.2-method-1` denotes the first OKF Method release recommending OKF 0.2, and the next release on the same specification baseline is `okf-0.2-method-2`. These names illustrate the convention; check actual tags in each public repository to determine whether a release has been published.

The sequence numbers releases based on that specification; it is not a SemVer compatibility classification. Consider a new baseline when the adoption model, a core interpretation, template operating practices, or a major usage flow changes meaningfully. Typographic, wording, or link corrections alone do not require a new release. Even if upstream advances its version, begin `method-1` for the new specification only when the recommended baseline changes after impact review.

`okf-method-kr` and `okf-method` use the same logical release name. Each tag points to a commit whose publication scope and meaning were reviewed against the same dev baseline, so the commit hashes differ. Keep tags fixed at the published commits; subsequent corrections belong in later commits and, when needed, a new release. Describe the main changes and their adoption or migration impact in each repository's language. A shared release is complete only after both repositories have been checked. The reasoning for this relationship is in the [distribution principles](../okf/distribution.md).

The research repository does not need a tag on every commit. Each public repository's `SYNC.json` connects it to the reviewed dev baseline, and users should be able to identify the guidance available at the time of adoption from the public repository they consulted alone.

## Recording the actual reference baseline

If adoption used `main` between releases, the nearest tag cannot stand in for the actual commit consulted. During [operational handoff](../APPLICATION.md), briefly recording the repository and commit actually read in the existing README or operating guide helps later comparison. A corresponding release and specification baseline can also be recorded separately, but there is no need for a separate `VERSION` file or repeated metadata on every concept.

If only some concepts were updated from newer guidance, record that scope too, so readers do not assume the entire repository moved to the same baseline. If a past reference was not recorded, recover what the history supports and leave the rest unverified. [Long-term feedback](../FEEDBACK.md) connects differences between the guide used then and the current guide to observed problems.

## Flow for adopting an upstream change

1. Check the version and diff of the official `SPEC.md`.
2. Evaluate format compatibility, semantic changes, and impact on operating principles and templates separately.
3. Update only the documents that need it and record whether existing projects require migration.
4. Judge the recommended version for new projects separately from the migration priority of existing projects.

Do not infer compatibility from a version number alone. The specification can change while retaining the same version label, so record both the verification date and the upstream file baseline.
