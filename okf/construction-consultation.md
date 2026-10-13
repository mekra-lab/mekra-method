---
type: Concept
title: Consultation and delegation for the build direction
description: Use a provisional design grounded in actual material to decide consequential operating choices with the user and delegate detailed judgments
---

# Consultation and delegation for the build direction

Discussing the build direction establishes what knowledge will be used and how it will be used and updated. [Design exploration](knowledge-design.md) develops candidates grounded in actual material and intended use; unresolved choices that materially change operation are decided with the user. Within a direction already chosen or explicitly delegated, the agent determines the concrete knowledge structure.

[Adoption judgment](adoption.md) establishes the current state and scope to complete in this pass. This document explains who decides what in that process. Reflect the chosen direction in [structure and discovery paths](structure-and-discovery.md) and [actual use and operational handoff](knowledge-operation.md). If new operating choices emerge, revisit the established direction and scope of delegation.

## User intent and delegated autonomy

Explore the target first; existing documents and instructions can provide answers. Focus questions on unresolved intent that materially changes the outcome, such as whether a source of truth may move or how much change this pass should absorb. Judge what needs discussion by its effect on later use and updates, rather than the name of a work item. Within the established direction, the agent autonomously handles detailed design, implementation, and maintenance, including OKF properties, concept relationships, and directory organization. If design reveals a new operating choice, explain the difference in actual use and updates and decide it with the user.

A user may delegate judgment to the recommended approach or choose major decisions together. This is a preference for degree of involvement, not a fixed mode that must be selected every time. Once that judgment is explicitly delegated, do not ask again for the same choice. Adapt the form of questions and the order of work to the purpose and context.

Phrase questions and options using the vocabulary, conceptual familiarity, explanation preference, and decision style visible in the conversation and material the user has provided. Do not assign the user an arbitrary skill level; use terminology and explanation depth they already demonstrate. Keep familiar technical terms when useful, and do not require the user to learn Mekra Method's internal category names or implementation vocabulary just to answer. Explain what an option changes in actual operation and why it is recommended. When sufficient autonomy is already delegated, proceed with the recommended approach without asking again about minor choices.

### Discussing options for an initial build

For an initial build, explore the target and develop a provisional design. Present unresolved choices that materially affect later use and updates with a recommendation, alternatives, and their differences, and decide them with the user. Carry forward choices already made or judgment explicitly delegated. Within the established direction, the agent autonomously determines the concrete knowledge structure and implementation.

Ground the provisional design in actual material and intended use, making it concrete enough to explain the knowledge, relationships, and reasoning needed and what existing knowledge does or does not cover. Establish reasons for a choice through [comparing alternatives and expanding exploration](knowledge-design.md#expanding-and-concluding-exploration). If viable options with different strengths and operational consequences remain, present representative options with the recommendation and its reasons. Reusing existing OKF with small additions can be a valid option. Distinguish expected improvement from effects actually confirmed; there is no need to implement or report every alternative considered.

Choose the number and grouping of questions and options to fit the target and unresolved intent. Ask about a single choice or present related choices as an arrangement; do not turn exploration, provisional design, and consultation into a fixed survey or a checklist with separately completed steps every time. If no existing knowledge is available, there is no need to offer an option that relies only on it; if the user requested a full review, carry that scope forward. You can offer a **"Proceed with the recommended approach"** path alongside individual adjustments and additional comments. Reassess even the initial direction as purpose and knowledge change.

Review scope, depth of knowledge development, and the scope to complete now are separate choices. You can review all material and select reusable knowledge, or build a core area deeply first. A depth preference conveys overall expectations and priorities; judge each concept's precision by the meaning needed for the agreed use. Even when focusing on key concepts, preserve conditions and exceptions that change the judgment.

#### Example B — Aligning the role and build scope

Consider a hypothetical repository containing deployment procedures, incident response, service dependencies, and past incident records. Suppose exploration finds clear individual procedures and ownership, but deployment stop criteria and rollback constraints are scattered across documents, and exceptions found in past incidents are not connected to current procedures. In an actual application, explain what the target's material covers and lacks rather than copying this example's subject matter.

> The existing procedures identify the deployment sequence and owners. What needs strengthening is the context for deciding "Can deployment continue when errors increase?" and "Which rollback conditions need review when a dependency changes?" I recommend organizing deployment stop criteria, rollback constraints, and service dependencies as OKF knowledge with supporting evidence and connections to exceptions found in past incidents. Keep the existing procedures as sources of truth, and first check judgment and change-impact tracking for one frequently operated service.

| Topic to discuss | Options for this situation |
| --- | --- |
| Mekra's role | **Preserve existing procedures as sources of truth and strengthen judgment context in OKF — recommended** / Move the canonical procedures into OKF and manage them together |
| Review scope | Focus on current deployment and incident-response documents / **Also review service dependencies and past incident records — recommended** |
| Depth of knowledge development | Focus on deployment-stop and rollback decisions / **Also organize related service constraints, past exceptions, and change impacts — recommended** |
| Scope to complete now | **Make knowledge usable for actual judgment in one frequently operated service, then expand — recommended** / Build deployment and incident-response knowledge for all operating services in this pass |

Preserving existing sources of truth keeps the location for procedure changes unchanged; reflect the meaning of changed conditions in related OKF knowledge too. Moving the sources of truth also changes where procedures are edited and how existing tools connect. Reviewing past records and dependencies can reveal exceptions beyond current procedures, but requires more material review. Even a focus on rollback decisions includes service constraints that change those decisions; broader depth also builds knowledge for tracking changes in related services. Covering all services now increases the immediately usable scope as well as construction and verification costs.

> You can **proceed with the recommended approach** or **adjust individual choices**. Add any main tasks you want to delegate or constraints that require preserving the existing structure.

These recommendations and four topics fit this hypothetical target; they are not a required questionnaire. Omit or combine topics according to meaningful differences in judgment and intent already provided. The agent designs OKF properties and directory details to fit the chosen direction.

#### Example A — Clarifying one future plan

In this hypothetical situation, existing OKF sufficiently describes one product's support conditions and usage limits, while future growth in products or plans could change the role of the build. Assume current questions can be answered from existing knowledge and no need for additional concepts has been found.

> The existing OKF can support the current product's conditions and limits. If you plan to keep adding products or plans, it would help to strengthen common conditions, product-specific exceptions, and relationships to revisit after changes. What use do you expect?
>
> 1. Keep adding material and tasks and develop it over time
> 2. Use it while keeping roughly the current material and scale
> 3. Not decided yet

Future plans are information the user supplies, so do not recommend an answer about whether growth is expected. If plans are undecided, recommend an arrangement that meets current needs and adjust its role and depth as the purpose becomes clearer.
