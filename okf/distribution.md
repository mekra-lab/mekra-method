---
type: Pattern
title: Synchronizing research and multilingual editions
description: Align the meaning of language editions while preserving canonical ownership and publication boundaries
---

# Synchronizing research and multilingual editions

`okf-lab-dev` is the source of truth for research and adopted shared knowledge. `okf-lab-kr` and `okf-lab` are the Korean and global English editions. Synchronization aligns the meaning of knowledge suitable for publication. Research source materials and internal Git history do not need to be distributed with it.

## Publication scope and language responsibilities

Select published files explicitly, and review changed content for suitability even when its file is already listed. An unchanged path does not make new content publishable. General guidance in `notes/` and `experiments/` may be public, but actual cases and source materials require separate judgment. Development-only tools and records are not automatically included either.

The Korean edition reflects selected shared knowledge. The English edition conveys the same meaning, conditions, exceptions, and reasoning. Do not introduce or weaken principles during translation. Adapt titles, language links, repository URLs in usage examples, and descriptions of the repository's own role to each edition. The official OKF version and an edition's synchronization baseline are separate information.

## Agent judgment and tool verification

The agent compares changes since the last synchronization and decides whether direct edits in a public edition should be retained or reflected in shared knowledge. Update related concepts, profiles, and templates according to [context propagation](context-propagation.md), and review the meaning of the English edition. Tools check listed files, links, content changes, and synchronization records. Matching hashes do not prove translation accuracy or suitability for publication.

Recording the reviewed source baseline and output content fingerprints for each edition makes later source changes distinguishable from direct edits to the edition. Report partial completion accurately; do not record the entire synchronization as complete until both editions have been checked. Public repositories keep their own histories and receive only selected file changes.

## Changes returning from an edition

If [feedback](feedback.md) or direct edits reveal improvements to shared knowledge, reflect them in the relevant dev concepts and then in the affected editions. Language-specific wording can be resolved within that edition. Do not overwrite direct changes without comparison, or split the same knowledge into independently maintained [sources of truth](source-of-truth.md).
