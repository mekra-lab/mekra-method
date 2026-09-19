# okf-lab

A public English-language repository for studying how OKF evolves and how it can be used in practice, and for organizing operational knowledge that agents can apply to target repositories.

> Korean version: [muffinbox/okf-lab-kr](https://github.com/muffinbox/okf-lab-kr)

> Examples and application contexts are generalized so they do not identify specific individuals or organizations.

> This repository is not a copy of the OKF specification or a framework every project must follow.  
> The canonical source for the official format is [GoogleCloudPlatform/open-knowledge-format](https://github.com/GoogleCloudPlatform/open-knowledge-format).

## Core perspective

okf-lab aims for a knowledge graph where **definition and change responsibility are concentrated in clear sources of truth, while the context needed for understanding is distributed across related concepts**.

Sources of truth establish the basis for facts and rules and prevent different documents from independently owning the same fact. At the same time, a single source of truth does not imply a single location for context. When one fact affects several concepts, each concept should restate as much as needed about how that fact affects its own meaning, conditions, exceptions, and judgment. Distributing context does not mean distributing responsibility for changing the fact itself.

The thing to avoid is therefore not repetition of the same fact, but having multiple places independently define and change it. Links should communicate the reason for and impact of a relationship through the surrounding prose rather than acting as bare addresses. When knowledge or implementation changes, use the source of truth as the baseline and also update the context of related concepts whose meaning changes.

In this balance, a domain is internalized not as one complete document but through the overlap and relationships between sources of truth that provide a center and documents that carry one another's meaning. See [operating principles](okf/operating-principles.md), [source of truth and context](okf/source-of-truth.md), [knowledge internalization](okf/knowledge-internalization.md), and [context propagation](okf/context-propagation.md) for the reasoning.

## What this repository does

- Tracks upstream version changes and their migration impact.
- Separates and accumulates adopted operating principles, reusable patterns, and profiles for different usage modes.
- Provides minimal templates that can be copied into real projects and adapted.
- Keeps unverified ideas and experiments separate from established guidance.

## Structure

| Location | Role |
| --- | --- |
| [`APPLICATION.md`](APPLICATION.md) | Target exploration, adoption decisions and questions, implementation, and operational handoff |
| [`FEEDBACK.md`](FEEDBACK.md) | Selecting reusable adoption experiences, drafting feedback, and submitting it |
| [`okf/`](okf/index.md) | Understanding of OKF, operating philosophy, reusable patterns, and conceptual relationships |
| [`profiles/`](profiles/README.md) | Starting points that combine patterns for specific usage modes |
| [`templates/`](templates/README.md) | Minimal scaffolding to copy into a project and adapt to its context |
| [`versions/`](versions/README.md) | OKF version baselines, impact analysis, and migration records |
| [`experiments/`](experiments/README.md) | Hypotheses and methods under validation |
| [`notes/`](notes/README.md) | Observations and reflections not yet consolidated |

## How to use it

In the target repository, ask your agent:

> Apply https://github.com/muffinbox/okf-lab to this repository.

You can also describe the work more specifically. Here are requests you can use with the same URL:

| Example request | Main intent |
| --- | --- |
| Build an OKF in this repository. / Turn this repository into OKF. | Inspect current materials and build the structure and knowledge graph needed |
| Migrate the existing OKF to okf-lab practices. / Bring it in line with current okf-lab. | Update operating practices while preserving existing knowledge |
| Switch to the knowledge-only approach. | Change the operating model to fit its purpose |
| Upgrade the OKF version. | Assess and address the impact and need for an official specification transition |
| Inspect the current OKF. | Diagnose the suitability of its structure and knowledge |
| Inspect the OKF structure and fix what needs improvement. | Diagnose and implement necessary improvements |

There is no exact wording to learn, nor do you need to know internal operation names. The agent starts with the [application guide](APPLICATION.md) and interprets the request together with the target's current state. "Apply it" delegates an overall assessment of necessary work; more specific requests guide exploration of relevant philosophy and profiles within their purpose and scope.

The agent decides autonomously where the target supplies enough context and asks only when unresolved user intent materially affects the outcome. You may delegate judgment to the recommended approach or decide major choices together. On completion, the agent explains where new source materials and knowledge belong and how to request their incorporation.

Profiles and templates are examples and defaults. Suitability is not determined by matching a file count or directory layout, but by whether knowledge is understood in the right context and whether the effects of change are reflected where needed.

## Research and applied knowledge

This is the global English edition. It provides shareable knowledge adopted in the research space; the same knowledge is also distributed in the [Korean edition](https://github.com/muffinbox/okf-lab-kr). Feedback is received where the user encountered the guide, while case research and validation continue in the research space.

Editions are updated according to [publication boundaries and language responsibilities](okf/distribution.md). The last reviewed source and published file baselines are kept in the [synchronization record](SYNC.json).

Adopted reasoning belongs in `okf/`, with practical configurations and scaffolding in `profiles/` and `templates/`. `notes/` and `experiments/` contain research material; unadopted content is not a default basis for application. Record observations from real use there and reflect reusable conclusions in related concepts and application materials.

Guide limitations and reusable improvements discovered during adoption can return as [feedback](FEEDBACK.md). An agent can generalize the context and draft it; ordinary applications do not require a separate report.

## Current baseline

- OKF: **v0.2**
- Verified on: **2026-09-18**
- Detailed baseline: [`versions/current.md`](versions/current.md)
