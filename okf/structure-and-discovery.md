---
type: Concept
title: Mekra structure and discovery
description: Define bundle locations and logical operating scope, and maintain individual entry points and discovery paths for multiple Mekras
sources:
  - id: okf-spec-v02
    resource: https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md
    title: Open Knowledge Format v0.2
---

# Mekra structure and discovery

The physical location of knowledge, the scope operated as one Mekra, and the path for finding that Mekra in an environment have different responsibilities. Understanding these boundaries together preserves sources of truth, operating context, and access paths when moving knowledge or connecting multiple Mekras.

Design structure within the [operating direction established with the user](construction-consultation.md). After establishing paths and links, check [actual connection to use](knowledge-operation.md#connecting-knowledge-to-actual-use); discoverability does not substitute for access permission or successful use.

## Bundle location and existing structure

As [the role and use of OKF](okf-format.md#bundle-boundaries-and-location) explains, adopting the OKF format and choosing a directory name are separate decisions. Identify existing bundles from their document format, entry points, and existing guidance, not just the name `okf/` or `mekra/`.

When a new file-based Mekra needs its own directory, use `mekra/` as the default location. Preserve an existing canonical location or use a structure better suited to the target. Names such as `knowledge/`, `domain/`, or `policy/` can express content or responsibility; when a repository distributes a single bundle, its root can serve as the bundle root.

`mekra/` is a consistent default name for new arrangements and adoption examples, not a required path. Do not rename an existing `okf/` or other directory merely to match the default; connect entry points and tools to the actual location chosen. `mekra/` itself can be the OKF bundle, without an extra `mekra/okf/` wrapper.

A separate subdirectory helps when bundle knowledge needs to be distinguished from code, research material, or operating guidance. If implementation or task guidance benefits from separate management, use an existing location such as `docs/`. Knowledge about operating the knowledge base can still be internalized in relevant concepts when it contains reusable meaning and decision criteria. Keep an existing location when it is suitable, and adapt files and instructions to the actual bundle boundary rather than the template's enclosing folder name. When moving a bundle, also inspect entry points, links, and path assumptions in related tools.

Do not treat the current structure as fixed. Where useful, a Mekra can be split, multiple Mekras can be connected or integrated, and existing structure can be reduced. Existing [source-of-truth responsibilities](source-of-truth.md) and [disclosure boundaries](disclosure-boundary.md) still apply to these choices; judge the concrete arrangement from the target's purpose and context.

## Knowledge operating entry point

An independently organized file-based Mekra uses `MEKRA.md` at its logical root as a common entry point. It describes that Mekra's purpose, scope, discovery paths, reference baseline, and specific operating context, and is linked from the target's agent entry instructions. In repositories using `AGENTS.md`, keep that link together with repository-wide development, execution, and deployment instructions and operating preferences in AGENTS. If knowledge operating guidance previously lived inside AGENTS, preserve its valid content, move it to MEKRA, and link to it. This is Mekra's adoption approach, not a required-file rule in the official OKF specification.

Choose the logical root according to the Mekra's operating scope and the unit that needs to move together. For a separate Mekra inside a code repository, the default example is `mekra/MEKRA.md`; when the entire repository operates as one Mekra, use root `MEKRA.md`. One Mekra may connect several OKF bundles or external documents and databases, so its knowledge need not all live in one physical directory. In environments without files, link an equivalent entry point such as a page.

When the file is included in a bundle, it must also follow the bundle's format. The reserved-filename rules in the baseline OKF specification treat Markdown files other than `index.md` and `log.md` as concept documents. A `MEKRA.md` inside a bundle therefore needs `type` frontmatter.[^okf-spec-v02] `type: Playbook` is one local choice for representing operating guidance; the filename `MEKRA.md` has no official format exemption.

An entry point is not a place to keep accumulating detailed principles and procedures. Internalize reusable reasoning in the relevant concepts, and leave the Mekra's specific context and discovery paths at the entry point. OKF's `index.md` lists the bundle's knowledge, while `MEKRA.md` explains the scope and context in which it operates; connect the two. The file's existence alone does not guarantee automatic loading or actual use, so check the agent's actual entry path. The [templates](../templates/README.md#choosing-an-entry-point-arrangement) show how to adapt locations and links to the target.

Another `MEKRA.md` in a nested directory does not, by physical containment alone, merge knowledge identity or responsibility for sources of truth. Read each entry point's purpose, scope, and responsibilities to judge the relationship. Referencing another Mekra, including an independent Mekra within a scope, and merging multiple Mekras describe relationships rather than fixed types or mandatory procedures. When merging, examine existing differences in meaning, source-of-truth responsibilities, evidence, and necessary history to establish new boundaries and references.

## Discovery index for multiple Mekras

In an environment where multiple Mekras are discovered and used together, use `MEKRAS.md` as the default discovery index. Place it somewhere accessible from the environment's entry instructions, such as the workspace root, and list known Mekras with names, brief descriptions, and links to each `MEKRA.md` or equivalent entry point. Detailed knowledge and operating rules belong in the individual Mekras. Connecting multiple Mekras in an index does not by itself define the environment as a new parent Mekra.

For an environment using just one Mekra, link directly to its `MEKRA.md` from agent instructions. For multiple Mekras, direct the agent to read `MEKRAS.md` and find those relevant to the current task. Connecting the actual entry point during adoption avoids repeating a separate discovery procedure in every product's instructions. Multiple agents using the same environment can share the same index.

Maintain Mekra structure and knowledge autonomously within the scope delegated by the environment and user. When creation, movement, splitting, or merging changes the structure, update relevant entry points and index links as well. The index communicates the current structure; discovering an entry does not grant new authority to act. Changes within delegated scope do not require separate permission merely to register the result in the index.

When index links or descriptions differ from the actual structure, verify the targets and sources of truth and correct them. Make the scope clear even in nested environments, and avoid unnecessarily maintaining independent copies of the same list. Markdown is the default example; fixed fields, a global registry, and an automatic discovery protocol are not additional requirements.

[^okf-spec-v02]: [OKF v0.2 §3.1: Reserved filenames](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#31-reserved-filenames), [§4.1: Frontmatter](https://github.com/GoogleCloudPlatform/open-knowledge-format/blob/ad30107c31c06aec8a7d5636e0d1058118604e6f/SPEC.md#41-frontmatter). Introducing and locating a MEKRA.md entry point is a local adoption choice.
