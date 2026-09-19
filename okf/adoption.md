---
type: Concept
title: OKF adoption judgment
description: Choose the operating model, necessary changes, and scope, and connect the result to continued knowledge operations
---

# OKF adoption judgment

Applying okf-lab means understanding a target repository and reflecting adopted operational knowledge in structure and knowledge appropriate to that context. Copying templates supports this work; the purpose is to improve actual operation while preserving the meaning of existing knowledge and canonical boundaries. This is our own application approach, not a requirement of the official OKF specification.

The user can start with the repository URL and a request to "apply it." This repository supplies the reasoning and navigation needed for application. Keeping research and application materials together makes it possible to update concepts, profiles, and templates with conclusions drawn from observations. Adopted reasoning belongs in `okf/`; unadopted content in `notes/` and `experiments/` is not a default basis for application.

## Natural-language requests and current state

Interpret requests that reach this repository by considering the desired outcome and the target's current state together. "Apply it" broadly delegates judgment about the necessary work; "build," "migrate," and "inspect" express more specific purposes. Operation and scope names are vocabulary for the agent's reasoning. Users need not learn them or use fixed wording.

Do not regenerate an existing knowledge graph merely because the user said "build an OKF." If OKF already exists, decide whether to preserve and supplement its knowledge or update its operating practices. "Turn this repository into OKF" expresses an intent to find reusable knowledge in existing materials and [internalize](knowledge-internalization.md) it as concepts and relationships. Whether bare scaffolding is sufficient depends on the requested scope and available materials.

Distinguish "inspect it," meaning diagnosis and proposed improvements, from "inspect and fix it," which includes implementing changes. Interpret actual scope together with delegation and constraints from earlier conversation. Autonomous judgment chooses methods within that intent; it does not justify expanding a diagnosis-only request into a structural transition.

## Three distinctions that support judgment

| Dimension | Question | Examples |
| --- | --- | --- |
| Profile | How will the repository operate? | Code-centered, knowledge-centered, large corpus |
| Operation | What should be examined or changed from the current state? | Initial construction, updating practices, profile transition, specification upgrade, inspection |
| Scope | How much will be reviewed and addressed this time? | Scaffolding, progressive migration, full review and migration |

These dimensions do not substitute for each other. Initial construction and updating existing knowledge differ even under the same knowledge-centered profile; updates can also differ in the scope undertaken now. The categories support [autonomous judgment](agent-autonomy.md), so operations can be combined and profiles or scope adapted.

## How judgment differs by operation

| Operation | Main judgment | Starting scope |
| --- | --- | --- |
| Initial construction | Select knowledge worth internalizing from existing materials. | Survey current materials and adequately build out the selected scope. |
| Updating existing practices | Compare older templates or local practices with current okf-lab and adopt useful improvements. | Progressively migrate scaffolding and key concepts first. |
| Profile transition | Evaluate how changes in purpose or scale affect knowledge, source materials, and canonical boundaries. | Review the affected scope. |
| Specification upgrade | Assess how changes to the official format affect the target bundle. | Decide based on compatibility and the actual changes. |
| Inspection and improvement | Assess structure, canonical ownership, context, and conformity to the target specification. | Review the requested concerns and affected scope; implement improvements when changes have also been delegated. |

Updating practices includes template migration and reapplying the current okf-lab. A changed template does not call for replacing valid existing documents wholesale. A profile transition also goes beyond moving directories: if [canonical ownership](source-of-truth.md) or conceptual roles change, reflect those meanings too.

The [version records](../versions/README.md) provide the basis for specification transitions. Updating okf-lab practices and upgrading the official OKF version may be needed independently and should be distinguished.

## Review scope and change scope

Scaffolding establishes entry points, instructions, indexes, and other operational foundations. Progressive migration additionally updates key concepts and currently affected knowledge, leaving other material to migrate when it is used or changed. Full review and migration examines the entire agreed or autonomously selected scope and completes the changes that are needed.

A full review does not mean rewriting everything. Preserve suitable documents, and do not turn every original into an OKF document even during initial construction. The reuse value of [internalization](knowledge-internalization.md) determines what belongs in scope, and the [propagation of meaning](context-propagation.md) determines actual edits.

Even progressive migration may need to resolve conflicts that break meaning or use under the new practices. If the user limited scope, explain the conflict and necessary additional work and reconcile the scope. Leave the remaining work and its triggers discoverable in the target repository. A small bundle may be cheaper to review at once, and format compatibility may require migrating all affected items together.

## User intent and delegation

Inspecting the target first often supplies answers from existing documents and instructions. Concentrate questions on unresolved intent that materially affects the result, such as willingness to move canonical responsibility or the amount of change to undertake now. Do not repeatedly ask users to choose profile names or document locations that context can resolve.

Users may delegate judgment to the recommended approach or decide major choices together. This is a preference about involvement, not a fixed mode everyone must select. Do not reconfirm decisions already delegated. Question examples, operation categories, and application procedures can themselves be omitted, combined, or adapted to purpose and context.

The wording of questions is also part of context. Use vocabulary, conceptual understanding, explanation preferences, and decision style evident in the user's conversation and materials to choose the terminology and depth of questions. Do not make users learn internal operation names or categories in order to decide; explain the operational difference each choice makes instead. Technical terms the user already uses can be retained, and when judgment has already been sufficiently delegated, applying a recommended option and then explaining the decision can be more appropriate than repeatedly asking for a choice.

## Operation after adoption

Construction and transition requests establish or change the target's operating model; follow-up requests such as "reflect the new materials in OKF" use that model. During application, okf-lab leaves operating guidance appropriate to the target. Routine material intake then proceeds using the target's canonical sources, instructions, and knowledge graph. This lets the target operate without repeating okf-lab's application process each time.

Autonomous application delegates design decisions; it should not leave users guessing how to proceed. On completion, explain and record the actual intake locations for originals and new knowledge and how to request internalization. If originals live externally or no separate intake location is needed, explain that arrangement.

Intake locations depend on the responsibilities of [source materials and derivatives](external-sources.md) and the [profile](../profiles/README.md). Do not impose a directory name such as `raw/`. Progressive migration needs a record of when and how remaining knowledge will be incorporated so that follow-up work can continue. Operational handoff is therefore part of completing construction or transition, and part of the progressive migration strategy. Start actual application with the [application guide](../APPLICATION.md).

If repository-wide working preferences would help after adoption, optional preferences can also be proposed. Examples include preferring a Markdown source for document-like derivative outputs, reflecting newly established durable knowledge from deliverables back into OKF, preferring recommended defaults when a choice is unspecified, reviewing for reusable knowledge after substantial work, and retaining evidence paths for derivative artifacts. Select only items that provide real value to the target and user, and record only preferences that have been agreed or delegated in persistent instructions such as the root `AGENTS.md`. Do not re-present source-of-truth management, context propagation, source-material separation, or other requirements already established by OKF operating principles or the selected profile as optional features.

Handoff can connect reusable discoveries to [feedback](feedback.md). This optional activity returns the guide's usefulness and limitations to research. Autonomous adaptations alone do not require reports, and external submission does not determine whether application is complete.
