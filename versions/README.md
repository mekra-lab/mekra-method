# Versions

Track changes in upstream OKF and record their impact on this repository's principles, patterns, and facets. This guide also covers release baselines for the Mekra Method knowledge used to interpret and apply that specification.

- [`current.md`](current.md): current recommended baseline and verified upstream reference
- [`migrations/`](migrations/): changes that require an actual transition between versions

## Specification and guide baselines

| Baseline | Meaning |
| --- | --- |
| OKF specification version and verified file reference | The official format being interpreted and applied |
| Mekra Method release tag | A fixed publication baseline for the adopted method and operating knowledge |
| Repository and commit of the guidance consulted | The actual state of the guide read when applying it to a target |

The default adoption baseline is each public repository's latest formal release, reached through `releases/latest`. Public `main` contains the latest reviewed documents and can receive corrections to errors, wording, links, and usability between releases when they preserve adoption meaning. Changes to adoption judgments or core principles are reviewed in dev or a preparation branch and reach public `main` together with a release. Judge the boundary by meaning, not filenames or change size; do not use public `main` to trial unreleased principles. Use the official specification version in a target bundle's `okf_version`, not a Mekra Method release name.

Publish a new release to include improvements from public `main` in the formal adoption baseline. Urgent corrections needed in that baseline follow the same process. Corrections to errors, wording, or links that preserve meaning use a patch release; changes to adoption meaning use the appropriate level below. Urgency alone does not justify a patch version or moving an existing tag.

`SYNC.json` records the dev commit and publication manifest used to review that public state, along with the content fingerprints of the source and published files. Update the record when public content changes, and preserve past release records in their tags. Comparing new dev changes is separate from checking a published release against its own baseline.

`releases/latest` can point to a different release over time. At the start of an application, resolve the release tag and commit, then follow `APPLICATION.md` and related documents at that revision. Keep the same baseline throughout the work and record what was actually consulted on completion. If the user specified a tag, commit, or dev working tree, use that baseline.

## Mekra Method releases

Mekra Method continues the knowledge and history of OKF Lab and OKF Method. The repositories moved from `okf-lab`, `okf-lab-kr`, and `okf-lab-dev` through `okf-method`, `okf-method-kr`, and `okf-method-dev` to `mekra-method`, `mekra-method-kr`, and `mekra-method-dev`, respectively. Preserve the existing `okf-0.2-lab-1` tag and its commit as a historical baseline; do not retroactively rename repositories or tags in past adoption records.

### Names and the meaning of changes

New release tags use `mekra-X.Y`, or `mekra-X.Y.Z` for a separately published patch. `X`, `Y`, and `Z` are numbers. Choose which position to increment according to the impact on existing adoption and operation.

| Position | Meaning of the change |
| --- | --- |
| Major `X` | A change requiring review of important assumptions or operating practices in existing adoption |
| Minor `Y` | An improvement that can be adopted optionally while keeping existing practices |
| Patch `Z` | A separately published correction to errors, wording, or links that preserves meaning |

`mekra-X.Y` is the first release in that series, equivalent to patch zero. Do not add a duplicate `.0` tag for the same baseline; subsequent patches start at `.1`. Omit the patch position again when incrementing the minor version, and start the minor version at zero when incrementing the major version. Examples include `mekra-0.3`, `mekra-0.3.1`, `mekra-0.4`, and `mekra-1.0`. These illustrate the naming convention; they do not announce a release or select the next number.

This is a project convention for describing a method's impact, not a software API compatibility guarantee. Even a bug fix uses the appropriate level if it changes the meaning of adoption. Adding an optional arrangement, such as the trial `MEKRA.md` entry point, does not by itself require a major version. Document improvements that preserve meaning can reach public `main` between releases; updates to the formal adoption baseline are published as releases.

### Relationship to the OKF baseline

Record the Mekra version and OKF specification version independently. Keep OKF out of the release name, and state the underlying or recommended OKF version and reviewed specification reference in the release notes. Claims of additional support should describe the scope actually checked. A target bundle continues to declare its format through `okf_version`.

When changing the OKF baseline, judge the Mekra change level from its impact on actual adoption. A new specification number alone does not require incrementing Mekra's major version or restarting its numbering.

### Transition from earlier baselines

Dev adopted this convention on 2026-09-26. Preserve the names and targets of tags published under the earlier `okf-<spec-version>-method-<sequence>` convention and the `okf-…-lab-…` family. Do not mechanically translate old sequence numbers into new versions or rename existing tags. The combined `mekra-0.x-okf-0.y` notation considered in the inbox was not adopted.

Choose the first number in the new scheme after reviewing the actual release content and transition impact. Explain the relationship to the previous public baseline and the changes in the first release notes. Adopting the convention does not itself publish a release or change a target's adoption baseline.

### Publication across languages

`mekra-method-kr` and `mekra-method` use the same logical release name. Each tag points to a commit whose publication scope and meaning were reviewed against the same dev baseline, so the commit hashes differ. Keep tags fixed at the published commits; subsequent corrections belong in later commits and ship as new releases when included in the formal adoption baseline. Describe the main changes, adoption or migration impact, and separate OKF baseline in each repository's language. Release notes link directly to `README.md` and `APPLICATION.md` at that repository's release tag. After checking both repositories, designate the same formal release as latest and verify both `releases/latest` destinations before reporting the shared release complete. The reasoning for this relationship is in the [distribution principles](../okf/distribution.md).

The research repository does not need a tag on every commit. Each public repository's `SYNC.json` connects it to the reviewed dev baseline, and users should be able to identify the guidance available at the time of adoption from the public repository they consulted alone.

## Recording the actual reference baseline

When starting from the latest release, record the actual tag and commit resolved. The moving `latest` URL alone does not identify the baseline used at the time. When consulting public `main`, a release candidate, or dev, verify the actual commit; do not describe content that differs from a release as belonging to the nearest tag. During [operational handoff](../APPLICATION.md), briefly recording the repository and commit actually read in the existing README or operating guide helps later comparison. A corresponding release and specification baseline can also be recorded separately, but there is no need for a separate `VERSION` file or repeated metadata on every concept.

If only some concepts were updated from newer guidance, record that scope too, so readers do not assume the entire repository moved to the same baseline. If a past reference was not recorded, recover what the history supports and leave the rest unverified. [Long-term feedback](../FEEDBACK.md) connects differences between the guide used then and the current guide to observed problems.

If an adoption guide such as `MEKRA.md` uses `version`, it means the Mekra Method release consulted when building or updating the knowledge system. It does not mean an individual concept's revision, freshness, or completion of the entire transition. Record the release actually consulted; if material outside that release was also used, add the repository, commit, and scope. A separate file or field is optional.

In dev, where the method itself is developed, the working tree containing adopted knowledge can be described as the application baseline. Identify any uncommitted changes, and do not present an unpublished number as the release applied. When fixing a state for comparison or reproduction, record its commit.

## Reviewing early metadata conventions

When a local convention differs from an official field's meaning, check how actual consumers read it and which scope is being updated. The official meanings below come from [OKF v0.2 §5.2 and §5.4](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#52-trust-generated-and-verified), matching the [current baseline](current.md). The transition choices are this repository's adoption guidance.

| Earlier convention | Official meaning and transition judgment |
| --- | --- |
| Keeping `generated.at` as the first creation date | Its official meaning is the time of the last meaningful content change. Correct it when actual creation or change evidence exists; do not invent a timestamp. The optional field can be omitted, or the initial creation history can be preserved separately. If retaining `generated`, also check its required `by` key. |
| Using `status: active` to mean operational | Official document states are `draft`, `stable`, and `deprecated`, with `stable` as the default when omitted. Preserve operational status in prose or an extension field, and choose the document state according to its meaning. Do not replace every `active` with `stable` mechanically. |
| Treating an old `verified` entry as current verification after editing | Generation or editing and verification are separate. Do not update the verifier or timestamp without actual verification. Review the valid scope of the earlier check, correct claims it no longer supports, and retain needed historical evidence. |

Adding optional fields is not itself a quality improvement. Preserve the meaning of protected references and historical copies, and review only the compatibility needed within the current scope. These corrections alone do not require a specification upgrade or a complete rewrite.

## Flow for adopting an upstream change

1. Check the version and diff of the official `SPEC.md`.
2. Evaluate format compatibility, semantic changes, and impact on operating principles and templates separately.
3. Update only the documents that need it and record whether existing projects require migration.
4. Judge the recommended version for new projects separately from the migration priority of existing projects.

Do not infer compatibility from a version number alone. The specification can change while retaining the same version label, so record both the verification date and the upstream file baseline.

Record the SPEC blob and a link to the matching file at a fixed commit in the [current baseline](current.md). The same fixed link in release notes lets readers inspect the specification reviewed at the time. Consider a dev snapshot when an actual local copy is needed for offline validation or comparison, and a fork when modifying or distributing OKF or maintaining a separate compatibility branch requires one.
