# okf-lab

A repository for studying how OKF evolves and how it can be used in practice, then turning that work into operational knowledge that agents can apply to target repositories.

> This repository is not a copy of the OKF specification or a framework every project must follow.  
> The canonical source for the official format is [GoogleCloudPlatform/open-knowledge-format](https://github.com/GoogleCloudPlatform/open-knowledge-format).

## Core perspective

okf-lab aims for a knowledge graph where **definition and change responsibility are concentrated in clear sources of truth, while the context needed for understanding is distributed across related concepts**.

Sources of truth establish the basis for facts and rules and prevent different documents from independently owning the same fact. At the same time, a single source of truth does not imply a single location for context. When one fact affects several concepts, each concept should restate as much as needed about how that fact affects its own meaning, conditions, exceptions, and judgment. Distributing context does not mean distributing responsibility for changing the fact itself.

The thing to avoid is therefore not repetition of the same fact, but having multiple places independently define and change it. Links should communicate the reason for and impact of a relationship through the surrounding prose rather than acting as bare addresses. When knowledge or implementation changes, use the source of truth as the baseline and also update the context of related concepts whose meaning changes.

In this balance, a domain is internalized not as one complete document but through the overlap and relationships between sources of truth that provide a center and documents that carry one another's meaning. See [operating principles](okf/operating-principles.md), [source of truth and context](okf/source-of-truth.md), [knowledge internalization](okf/knowledge-internalization.md), and [context propagation](okf/context-propagation.md) for the reasoning.

## What this repository does

- Tracks upstream version changes and their migration impact.
- Accumulates adopted operating principles and reusable patterns.
- Provides [facets](facets/README.md) as thin lenses for reading important properties of a target.
- Provides minimal templates that can be copied into real projects and adapted.
- Keeps unverified ideas and experiments separate from established guidance.

## Structure

| Location | Role |
| --- | --- |
| [`APPLICATION.md`](APPLICATION.md) | Target exploration, adoption judgment and questions, implementation, and operational handoff |
| [`FEEDBACK.md`](FEEDBACK.md) | Selecting reusable adoption experiences, drafting feedback, and submitting it |
| [`okf/`](okf/index.md) | Understanding of OKF, operating philosophy, reusable patterns, and conceptual relationships |
| [`facets/`](facets/README.md) | Thin lenses for finding important judgment from properties of the target |
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
| Build an OKF in this repository. / Turn this repository into OKF. | Inspect current materials and build the structure and knowledge graph that are actually useful |
| Migrate the existing OKF to okf-lab practices. / Bring it in line with current okf-lab. | Update operating practices while preserving valid existing knowledge |
| Organize this as a knowledge-centered repository. | Judge the operating approach with knowledge as the primary output |
| Upgrade the OKF version. | Assess and address the impact and need for an official specification transition |
| Inspect the current OKF. | Diagnose the suitability of its current structure and knowledge |
| Inspect the OKF structure and fix what needs improvement. | Diagnose and implement necessary improvements |

There is no exact wording to learn, nor do you need to know internal operation names. The agent starts with the [application guide](APPLICATION.md) and interprets the request together with the target's current state. "Apply it" delegates an overall assessment of necessary work; more specific requests guide exploration of relevant philosophy and facets within their purpose and scope.

The agent decides autonomously where the target supplies enough context and asks only when unresolved user intent materially affects the outcome. You may delegate judgment to the recommended approach or decide major choices together. On completion, the agent explains where new source material and knowledge belong and how to request their incorporation.

A facet is a judgment lens, not a preset or default configuration. Templates are also starting points to adapt when useful. Suitability is not determined by matching a file count or directory layout, but by whether knowledge is understood in the right context and whether the effects of change are reflected where needed.

## Research and applied knowledge

Shareable conclusions are developed in the research repository and published here as practical guidance. Feedback can be submitted where the guide is used, while case research and validation continue in the research space.

Public material is updated according to [publication scope and language responsibilities](okf/distribution.md). The last reviewed source and published file baselines are kept in the [synchronization record](SYNC.json).

Adopted reasoning belongs in `okf/`; `facets/` helps locate relevant judgment; `templates/` provides optional application scaffolding. `notes/` and `experiments/` contain research material, and unadopted content is not a default basis for application. Observations from real use can be reflected back into related concepts and application materials when they prove reusable.

Guide limitations and reusable improvements discovered during adoption can return as [feedback](FEEDBACK.md). An agent can generalize the context and draft it; ordinary applications do not require a separate report.

## Current baseline

- Recommended baseline: **OKF v0.2**
- Verification date and specification baseline: [`versions/current.md`](versions/current.md)
