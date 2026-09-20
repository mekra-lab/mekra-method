---
type: Pattern
title: Research and multilingual distribution
description: Keep a shared source of truth and publication boundaries while aligning meaning across language editions
---

# Research and multilingual distribution

`okf-lab-dev` is the source of truth for research and adopted shared knowledge, while `okf-lab-kr` and `okf-lab` are the Korean and global English editions. Synchronization exists to align the meaning of publishable knowledge. Research source material and internal Git history do not need to be distributed with it.

## Publication scope and language responsibilities

Select files for publication explicitly, and reread changed content even when the path is already listed. Under the [disclosure boundary](disclosure-boundary.md), a path being publishable or accessible does not imply that every new change is publishable. General guidance from `notes/` and `experiments/` may be published, while concrete cases and source material are judged separately. Research-only tools and records are not automatic distribution targets either.

The Korean edition reflects selected shared knowledge. The English edition must convey the same meaning, conditions, exceptions, and reasoning. Translation should neither add nor weaken principles. Titles, edition notes, repository URLs in examples, and repository-specific role descriptions may be adjusted for the edition. The official OKF version and a language edition's synchronization baseline are separate pieces of information.

## Agent judgment and tool verification

The agent compares changes since the last publication and decides whether direct edits in an edition should be preserved or folded back into shared knowledge. Following [context propagation](context-propagation.md), update related concepts, facets, and templates, then review the meaning of the English edition. Tools verify the presence of listed files, links, content changes, and synchronization records. Matching hashes do not prove translation accuracy or publication suitability.

Recording the reviewed source baseline and content fingerprints for each edition makes later source changes distinguishable from direct edition edits. If only part of the work is complete, report that scope as-is; do not record the entire synchronization as complete before both editions have been checked. Public repositories keep their own histories and receive only selected file changes.

Git history in an edition should explain the meaning users will see rather than the synchronization operation itself. Build commit messages by reviewing both the accumulated dev commits since the last publication and the actual edition diff, then naturally summarize the most important changes in that repository's language. Do not use titles such as `sync`, `synchronize`, or `apply distribution` that describe only the operation. When several changes are published together, put the most important user-visible change in the title and leave only useful details in the body.

## Changes flowing back from an edition

When [feedback](feedback.md) or a direct edition edit reveals an improvement to shared knowledge, reflect it in the relevant dev concept before distributing it again as needed. Language-specific wording problems may be solved within that edition. Do not overwrite direct edition changes without comparison or allow the same knowledge to split into independently maintained [sources of truth](source-of-truth.md).
