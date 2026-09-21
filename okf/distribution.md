---
type: Pattern
title: Research and multilingual distribution
description: Keep a shared source of truth and publication boundaries while aligning meaning across language editions
---

# Research and multilingual distribution

`okf-method-dev` is the source of truth for research and adopted shared knowledge, while `okf-method-kr` and `okf-method` are the Korean and global English editions. Synchronization exists to align the meaning of publishable knowledge. Research source material and internal Git history do not need to be distributed with it.

## Publication scope and language responsibilities

Select files for publication explicitly, and reread changed content even when the path is already listed. Under the [disclosure boundary](disclosure-boundary.md), a path being publishable or accessible does not imply that every new change is publishable. General guidance from `notes/` and `experiments/` may be published, while concrete cases and source material are judged separately. Research-only tools and records are not automatic distribution targets either.

If private research inputs need to be retained in the research repository, first establish the need and permission to retain them, then use `research-private/` to keep them separate from publishable research explanations. Paths under this name must not be included in the publication manifest or in exceptions for edition-only files. Some files under `notes/` and `experiments/` are also publication targets, so do not assume a research directory is private. A separate path helps prevent accidental file inclusion; content copied into a public document still needs a publication review.

The Korean edition reflects selected shared knowledge. The English edition must convey the same meaning, conditions, exceptions, and reasoning. Translation should neither add nor weaken principles. Titles, edition notes, repository URLs in examples, and repository-specific role descriptions may be adjusted for the edition. The official OKF version and a language edition's synchronization baseline are separate pieces of information.

## License scope

Public repositories use Apache-2.0 for files unless otherwise noted. All files under `templates/`, including its README, are provided under [CC0-1.0](../templates/LICENSE) so they can be copied, adapted, and incorporated into a target repository. Using these templates does not require okf-method attribution or an adoption record. This exception does not extend to documents or experimental scaffolds outside `templates/`.

When applying CC0 or adding content later, check the rights to that content and any third-party notices. Include `templates/LICENSE` in the publication manifest and retain the Apache-2.0 `LICENSE` at each public repository's root. The public repositories' default license does not establish a license for all of dev; licensing for dev-only `scripts/` remains undecided.

## Agent judgment and tool verification

The agent compares changes since the last publication and decides whether direct edits in an edition should be preserved or folded back into shared knowledge. Following [context propagation](context-propagation.md), update related concepts, facets, and templates, then review the meaning of the English edition. Tools verify the presence of listed files, links, content changes, and synchronization records. Matching hashes do not prove translation accuracy or publication suitability.

Before publication, check file boundaries in the actual commits to be sent and in any intervening history that will become public, as well as in the working directory. Deleting a file from the final state does not keep it private if an earlier commit still contains it. Pin the verified commit and the destination's remote baseline for transmission, and check again if the remote changes after verification. This check does not automatically identify sensitive content inside allowed files or judge the meaning of a translation.

Regression tests for the tools check that the validator behaves as intended in the cases covered. Passing them does not guarantee semantic correctness across the entire knowledge graph. Differences exposed by checks are evidence for review; decide which content to change in which repository by considering meaning and publication scope.

Recording the reviewed source baseline and content fingerprints for each edition makes later source changes distinguishable from direct edition edits. If only part of the work is complete, report that scope as-is; do not record the entire synchronization as complete before both editions have been checked. Public repositories keep their own histories and receive only selected file changes.

Git history in an edition should explain the meaning users will see rather than the synchronization operation itself. Build commit messages by reviewing both the accumulated dev commits since the last publication and the actual edition diff, then naturally summarize the most important changes in that repository's language. Do not use titles such as `sync`, `synchronize`, or `apply distribution` that describe only the operation. When several changes are published together, put the most important user-visible change in the title and leave only useful details in the body.

## Releases and adoption baselines

Synchronization aligns the meaning and source baselines of public repositories; a release gives a reviewed state a name that remains available for later comparison. Not every synchronization needs a new release. Establishing a baseline after meaningful changes in the adoption model or operating judgments helps [long-term feedback](feedback.md) explain differences between the guide used then and the guide available now.

The same release name in the Korean and English repositories denotes shared knowledge reviewed against the same dev baseline. Each keeps its own Git history and commits, with synchronization records connecting source and published content. If only one has been published, do not report the shared release as complete. Moving a published tag changes the meaning referenced by earlier users, so corrections belong in subsequent changes.

A release is a convenient publication baseline, but it does not precisely identify the guidance used by targets that adopted it between releases. Checking the actual public repository, commit, and adoption scope makes past choices easier to interpret. Naming and reference-recording practices belong in the [version guide](../versions/README.md); distinguish the official OKF specification version from the OKF Method release sequence.

## Changes flowing back from an edition

When [feedback](feedback.md) or a direct edition edit reveals an improvement to shared knowledge, reflect it in the relevant dev concept before distributing it again as needed. Language-specific wording problems may be solved within that edition. Do not overwrite direct edition changes without comparison or allow the same knowledge to split into independently maintained [sources of truth](source-of-truth.md).

The [application-guide link improvement](https://github.com/muffinbox/okf-method-kr/commit/5ee3ca639f4fd85a4370d3826e6df4d71c43b0ca) on 2026-09-20 is a concrete example. A check comparing file destinations across languages exposed a link to the internalization concept that existed only in the English text. Review found it useful in context, so it was incorporated into dev and the Korean text as well. This demonstrates the process of reviewing a difference and returning it to shared knowledge; it does not establish effectiveness in other domains.
