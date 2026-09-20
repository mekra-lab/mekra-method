---
type: Concept
title: OKF adoption judgment
description: Judge the target's current state, needed changes, and application scope, then connect the result to continued knowledge operation
---

# OKF adoption judgment

Applying okf-lab means understanding a target repository and reflecting adopted operating knowledge into structures and knowledge that fit its context. Copying templates is only a supporting technique; the goal is to improve actual operation while preserving the meaning of existing knowledge and the boundaries of its sources of truth. This is an okf-lab operating approach, not a requirement of the official OKF specification.

A user can begin with a repository URL and a request such as "apply this." This repository provides the reasoning and discovery paths needed for application. Keeping research and application material together allows conclusions from observation to feed back into related concepts, facets, and templates. Adopted reasoning belongs in `okf/`; unadopted content in `notes/` and `experiments/` is not a default basis for application.

## Natural-language requests and current state

Interpret requests that reach this repository by looking at both the user's desired result and the current state of the target. "Apply it" is a broad delegation to judge the work that is needed, while "build," "migrate," and "inspect" express narrower purposes. Names for work types and scope are vocabulary for organizing agent judgment; users do not need to learn them or use fixed phrases.

A request to "build an OKF" does not automatically regenerate an existing knowledge graph. If OKF is already present, judge whether to preserve and improve current knowledge or update its operating approach. "Turn this repo into OKF" includes the purpose of finding reusable knowledge in current material and [internalizing](knowledge-internalization.md) it as actual concepts and relationships. Whether an empty scaffold is sufficient depends on the requested scope and state of the material.

"Inspect it" focuses on diagnosis and improvement proposals, while "inspect it and fix what is needed" includes implementing improvements. The actual scope also incorporates delegated authority and constraints established earlier in the conversation. Autonomous judgment selects methods inside that intent; it is not a reason to expand diagnosis-only work into an automatic structural transition.

## Three distinctions that support judgment

| Distinction | Question answered | Examples |
| --- | --- | --- |
| Facet | Which property of the target makes certain judgments worth examining more closely? | software project, knowledge-centered, large corpus, personal context |
| Work type | What should be checked or changed from the current state? | new build, operating-practice update, specification-version transition, inspection |
| Application scope | How far should this pass review and reflect changes? | scaffold, progressive transition, full review and transition |

These distinctions do not substitute for one another. A facet is a [descriptive lens](facet-boundaries.md) on a property of the target, not a work mode, and several facets may be relevant at the same time. The same knowledge-centered environment differs between a new build and an update to existing knowledge, and the same update can be performed at different scopes. These labels are vocabulary that supports [autonomous judgment](agent-autonomy.md), not a fixed procedure.

## Judgment by work type

| Work | Core judgment | Starting point for scope |
| --- | --- | --- |
| New build | Select knowledge worth internalizing from existing material. | Inspect current material and build the selected scope sufficiently. |
| Update existing operating practices | Compare earlier templates or local practices with current okf-lab and adopt valid improvements. | Transition the scaffold and key concepts first, then proceed progressively. |
| Specification-version transition | Judge the impact of official-format changes on the target bundle. | Set scope from compatibility and the actual changes involved. |
| Inspection and improvement | Examine the suitability of current structure, sources of truth, context, and target specification, then judge needed improvements. | Review the requested concerns and affected scope; implement improvements when fixes are delegated. |

Updating existing operating practices includes template migration and reapplying current okf-lab guidance. A template change does not justify replacing every valid existing document. If the target's properties or scale change and different facets become relevant, do not treat that label change as its own migration project. Update the [sources of truth](source-of-truth.md), source-material responsibilities, and concept meaning that are actually affected within the work already being done.

The evidence for specification-version transitions is kept in the [version records](../versions/README.md). Updating okf-lab operating practices and transitioning the official OKF version may be independently necessary, so keep them distinct.

## Review scope and modification scope

A scaffold application establishes operating entry points such as instructions and indexes. A progressive transition also reflects key concepts and currently affected knowledge, leaving the rest to transition when used or changed later. A full review and transition examines the agreed or delegated target scope and completes changes that are actually needed.

A full review does not mean changing every file. Keep documents that are already appropriate, and even in a new build do not convert every source document into an OKF document. Reuse value from [internalization](knowledge-internalization.md) determines what belongs in the knowledge graph, while [context propagation](context-propagation.md) determines the actual modification scope of a change.

A progressive transition still needs to resolve conflicts that would break meaning or use under the new operating model. If the user limits scope, explain the conflict and required additional work and reconcile the scope. Leave remaining work and future transition triggers discoverable from the target repository. For a small bundle, reviewing everything at once may be cheaper, and specification compatibility may sometimes require transitioning all affected items together.

## User intent and delegated autonomy

Explore the target first; existing documents and instructions often answer questions that otherwise would be sent back to the user. Focus questions on unresolved intent that materially changes the outcome, such as whether a source of truth may move or how much change this pass should absorb. Do not repeatedly hand back choices such as facet labels or document placement when context is sufficient to judge them.

A user may delegate judgment to the recommended approach or choose major decisions together. This is a preference for degree of involvement, not a fixed mode that must be selected every time. Once judgment is delegated, do not ask again for the same choice. Suggested questions, work categories, and application procedures may themselves be omitted, combined, or adapted according to purpose and context.

Question wording is also part of context. Use vocabulary, conceptual understanding, explanation preferences, and decision style visible in the user's conversation and material. Do not make users learn internal work names or classifications before they can choose; explain what each choice changes in actual operation. Terms the user already knows can be used directly. With sufficient delegated autonomy, applying the recommended option and then explaining the judgment may be more appropriate than repeatedly asking about minor choices.

## Operation after adoption

Build or transition requests establish or change the target's operating system; follow-up requests such as "incorporate the new material into OKF" use that system. During adoption, okf-lab should leave operating guidance fitted to the target, while routine material incorporation continues from the target's own sources of truth, instructions, and knowledge graph. This distinction lets the target operate without rerunning okf-lab's adoption procedure for every later update.

Delegating design judgment does not mean the user should have to infer how to use the result afterward. At completion, explain the actual locations selected for source material and new knowledge and how to request incorporation, and leave that information in the target repository as well. If source material is external or no separate intake location is useful, explain that operating model instead.

The intake location depends on the responsibilities described in [source material and derived artifacts](external-sources.md) and the target's real material flow. Relevant [facets](../facets/README.md) may help identify which judgments deserve attention. Do not create a directory such as `raw/` uniformly. In a progressive transition, leave the trigger and method for absorbing unconverted knowledge so follow-up work can continue. Operational handoff is therefore part of completing a build or transition and part of the progressive-transition strategy. The practical entry point is the [application guide](../APPLICATION.md).

Optional repository-wide operating preferences may also be suggested when they improve later work: preferring Markdown sources for document-like derived outputs, reflecting newly confirmed knowledge from outputs back into OKF, preferring the recommended option for unspecified choices, reviewing durable knowledge after substantial work, or preserving provenance paths for derived outputs. Select only preferences with real value to the target and user, and persist only what has been agreed or delegated in a root `AGENTS.md` or similar instructions. Do not re-ask source-of-truth management, context propagation, source-material separation, and other established OKF principles as if they were optional toggles. A facet is not a rule that reasserts those principles.

Reusable discoveries from operational handoff can be connected to [feedback](feedback.md). Feedback is an optional activity that returns observations about the guide's usefulness and limits to research. Autonomous adaptation during application is not itself something that must be reported, and whether feedback is sent does not determine whether adoption is complete.
