---
type: Concept
title: Applying Mekra Method
description: Judge the target's current state, needed changes, and adoption scope, and connect them to continued knowledge operation
---

# Applying Mekra Method

This document judges the target's current state, needed changes, and scope to complete in this pass, connecting the overall adoption context. Separate concepts hold detailed reasoning for build consultation, structure and discovery, and actual use and operational handoff. The [operating principles](../PRINCIPLES.md) explain the core principles and their relationships; the [application guide](../APPLICATION.md) provides the flow for starting adoption, finding relevant reasoning, and implementing it. Use work categories and examples to fit the target while meeting the knowledge representation and build-direction criteria.

Applying Mekra Method means understanding a target repository and reflecting adopted operating knowledge into structures and knowledge that fit its context. Copying templates is only a supporting technique; the goal is to improve actual operation while preserving the meaning of existing knowledge and the boundaries of its sources of truth. This is a Mekra Method operating approach, not a requirement of the official OKF specification.

A user can begin with the public guide's latest formal release URL and a request such as "apply Mekra." This repository provides the reasoning and discovery paths needed for application. Keeping research and application material together allows conclusions from observation to feed back into related concepts, facets, and templates. Find adopted principles in `PRINCIPLES.md` and detailed operating knowledge in `okf/`; unadopted content in `notes/` and `experiments/` is not a default basis for application.

## Natural-language requests and current state

Interpret requests that reach this repository by looking at both the user's desired result and the current state of the target. "Apply it" is a broad delegation to judge the work that is needed, while "build," "migrate," and "inspect" express narrower purposes. Names for work types and scope are vocabulary for organizing agent judgment; users do not need to learn them or use fixed phrases.

A request to "apply Mekra" does not automatically regenerate an existing knowledge graph. If Mekra or OKF knowledge is already present, judge what to preserve and improve or which operating practices to update. "Incorporate new material into the existing Mekra" focuses on finding knowledge worth retaining and [internalizing](knowledge-internalization.md) it in the relevant concepts and relationships. For an initial build, judge the needed arrangement against the role and completion expectations below.

Requests involving existing OKF material, including earlier wording such as "build an OKF" or "turn this repo into OKF," are also interpreted from their purpose and the target's state. An explicit request to update the OKF specification is distinct from an update to the Mekra Method baseline.

"Inspect it" focuses on diagnosis and improvement proposals, while "inspect it and fix what is needed" includes implementing improvements. The actual scope also incorporates delegated authority and constraints established earlier in the conversation. Autonomous judgment selects methods inside that intent; it is not a reason to expand diagnosis-only work into an automatic structural transition.

## The role and completion expectations of an initial build

An initial build is expected to understand the target's material and existing knowledge system and provide knowledge and relationships needed for actual use. Examine what the existing system supports, what needs strengthening, and expected changes to judge Mekra's role and relationship to that system, then [discuss the build direction with the user](#discussing-options-for-an-initial-build).

An initial build sets the foundation for later knowledge operations, so invest sufficient effort in exploration and design. Examine material, purpose, existing knowledge, actual use, and expected changes broadly and deeply, actively discovering important concepts, conditions, evidence, and relationships in exceptions and change history. Do not conclude exploration early merely because documents are well organized or an initial arrangement answers basic questions. Consider whether further exploration could change knowledge discovery or design judgment.

Understand related knowledge together to discover conditions, conflicts, and dependencies, and [internalize the context each concept needs](knowledge-internalization.md#integrated-understanding-and-internalization-in-individual-concepts). There is no need to preconstruct every possible insight or a complete integrated model of the entire target. Compare [meaningful design alternatives](knowledge-design.md) against actual questions and changes, and consider whether knowledge can also be found and combined for different questions later. Invest the effort exploration needs while choosing the final scale of knowledge and explanation to fit actual use.

When existing knowledge is sufficient, use its sources of truth and strengthen connections needed for discovery, understanding, and updates. Where more internalization is needed, organize the conditions, evidence, exceptions, and relationships that change judgment for the agreed use. Mekra may strengthen the existing system or operate alongside it as a knowledge layer with a different role. If sufficient exploration shows current needs are met, a minimal arrangement or deferring further adoption can also be appropriate. Explain that judgment through what the existing system supports and what needs improvement.

Judge completion by both the ability to perform the agreed role and the [current knowledge representation requirements](okf-format.md). Mekra knowledge reuses existing OKF or is organized in OKF; a non-OKF arrangement that only adds operating guidance does not count as completed adoption. Check whether knowledge needed for the intended questions or tasks can be found and used for judgment through an understanding of its relationships and conditions. New file counts or entry point creation alone do not establish completion. For a progressive build, make the assigned core area usable now and explain the remaining scope. Choose verification methods and depth to fit the target, including [connection to use](#connecting-knowledge-to-actual-use) and [operational handoff](#operation-after-adoption).

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
| New build | Consider both the use of existing knowledge and further internalization. | Provide usable knowledge and relationships for the role established through exploration and discussion. |
| Update existing operating practices | Compare earlier templates or local practices with current Mekra Method and adopt valid improvements. | Transition the scaffold and key concepts first, then proceed progressively. |
| Specification-version transition | Judge the impact of official-format changes on the target bundle. | Set scope from compatibility and the actual changes involved. |
| Inspection and improvement | Examine the suitability of current structure, sources of truth, context, and target specification, then judge needed improvements. | Review the requested concerns and affected scope; implement improvements when fixes are delegated. |

Updating existing operating practices includes template migration and reapplying current Mekra Method guidance. A template change does not justify replacing every valid existing document. If the target's properties or scale change and different facets become relevant, do not treat that label change as its own migration project. Update the [sources of truth](source-of-truth.md), source-material responsibilities, and concept meaning that are actually affected within the work already being done.

The evidence for specification-version transitions is kept in the [version records](../versions/README.md). Updating Mekra Method operating practices and transitioning the official OKF version may be independently necessary, so keep them distinct.

Review knowledge first built as a prototype or under local instructions from the same starting point. Distinguishing the initial setup, the timing and scope of later changes informed by the guide, and the baseline used for the current retrospective helps preserve existing knowledge while transitioning what needs to change. Do not extend an adoption record for a parent workspace to every bundle within it. When early metadata conventions differ from the current format, consult the [optional compatibility review](../versions/README.md#reviewing-early-metadata-conventions).

## Bundle location and existing structure

Choose the bundle location from existing sources of truth and the unit that needs to move together. Use `mekra/` by default for new file-based arrangements while preserving suitable existing locations. [Structure and discovery](structure-and-discovery.md#bundle-location-and-existing-structure) explains choices about naming, location, splitting, and merging.

## Knowledge operating entry point

Connect purpose, scope, specific operating context, and discovery paths at each Mekra's logical root. `MEKRA.md`, agent instructions, and the OKF index have different responsibilities; align [entry point location and the format required inside a bundle](structure-and-discovery.md#knowledge-operating-entry-point).

## Discovery index for multiple Mekras

Environments using multiple Mekras connect their entry points through a discovery index and maintain it as structure changes. Discovering an index entry grants no authority to act. The [discovery index](structure-and-discovery.md#discovery-index-for-multiple-mekras) explains paths for single and multiple Mekras and maintenance responsibilities.

## Review scope and modification scope

A scaffold application establishes operating entry points such as instructions and indexes. A progressive transition also reflects key concepts and currently affected knowledge, leaving the rest to transition when used or changed later. A full review and transition examines the agreed or delegated target scope and completes changes that are actually needed.

A full review does not mean changing every file. Keep documents that are already appropriate, and even in a new build do not convert every source document into an OKF document. Reuse value from [internalization](knowledge-internalization.md) determines what belongs in the knowledge graph, while [context propagation](context-propagation.md) determines the actual modification scope of a change.

A progressive transition still needs to resolve conflicts that would break meaning or use under the new operating model. If the user limits scope, explain the conflict and required additional work and reconcile the scope. Leave remaining work and future transition triggers discoverable from the target repository. For a small bundle, reviewing everything at once may be cheaper, and specification compatibility may sometimes require transitioning all affected items together.

## User intent and delegated autonomy

The user decides or explicitly delegates unresolved directions that materially affect later use and updates. Within the established direction, the agent determines properties, relationships, directories, and other details. [Consultation and delegation](construction-consultation.md#user-intent-and-delegated-autonomy) explains the scope and wording of questions.

### Discussing options for an initial build

Develop a provisional design from the knowledge needed in actual material and what the existing arrangement covers or lacks. When different strengths and operational consequences remain, present representative options with reasons for the recommendation. The [reasoning and examples for consultation](construction-consultation.md#discussing-options-for-an-initial-build) are not a fixed survey; carry forward directions already chosen or explicitly delegated.

#### Example B — Aligning the role and build scope

The [hypothetical deployment and rollback example](construction-consultation.md#example-b--aligning-the-role-and-build-scope) derives a recommended arrangement from gaps in actual material and explains differences in role, scope, and depth.

#### Example A — Clarifying one future plan

The [hypothetical product-knowledge reuse example](construction-consultation.md#example-a--clarifying-one-future-plan) asks only about choices that depend on future intent even when current knowledge is sufficient.

## Connecting knowledge to actual use

Check whether the agent or product can access the knowledge and use relevant concepts and evidence for actual questions. Distinguish the environment checked from remaining implementation or automation work, and reflect [evidence of the connection to use](knowledge-operation.md#connecting-knowledge-to-actual-use) in the completion scope.

## Operation after adoption

Leave intake locations, how to request incorporation, and remaining transition scope and triggers in the target. Continue later updates according to the existing knowledge graph and change impacts without repeating the entire initial build. [Operational handoff](knowledge-operation.md#operation-after-adoption) is a completion condition that lets the next user continue operating the system.

### Optional operating preferences

Persist only preferences that actually help the target and have been agreed or delegated. Do not re-ask adopted Method principles as optional features. Adapt the [examples and boundaries of operating preferences](knowledge-operation.md#optional-operating-preferences) to the target.
