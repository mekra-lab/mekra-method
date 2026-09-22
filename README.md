# Mekra Method

*Knowledge finds its place.*

Mekra Method helps you organize and maintain project knowledge so AI agents can understand the context and carry it into later work.

If you keep explaining the same background or tracing how one decision affects another task, you can record those reasons and relationships where they matter. Provide the knowledge and context needed for judgment, and leave the concrete way of working to the agent wherever practical.

## Get started

In the repository you want to work on, ask an agent with access to read and edit it:

> Apply https://github.com/muffinbox/mekra-method to this repository.

The agent examines existing material and structure, then judges which knowledge to organize and connect. After making the changes, it explains where and how to incorporate new material and updates.

[**Introducing Mekra Method**](INTRODUCTION.md) explains the problem and approach for newcomers. To apply the method, start with the [application guide](APPLICATION.md).

## Core perspective

**Keep sources of truth clear, share context where it is needed, and delegate judgment.**

Keep a clear reference for defining and changing a fact. In related concepts, restate as much as needed about what that fact means for their conditions and judgments. Avoid having several documents independently define and change the same fact; repeating it is not the problem. When the reference changes, review the related explanations too.

Mekra prioritizes organizing and maintaining the knowledge needed for judgment over prescribing detailed sequences of work. Agents choose how to work according to the purpose and situation, using the evidence and context they have actually read.

The reasoning is in [source of truth and context](okf/source-of-truth.md), [knowledge internalization](okf/knowledge-internalization.md), [context propagation](okf/context-propagation.md), [agent autonomy](okf/agent-autonomy.md), and [operating principles](okf/operating-principles.md).

## How to use it

You can also describe the work more specifically. Here are requests you can use with the same URL:

| Example request | Main intent |
| --- | --- |
| Build an OKF in this repository. / Turn this repository into OKF. | Inspect current materials and build the structure and knowledge graph that are actually useful |
| Migrate the existing OKF to Mekra Method practices. / Bring it in line with current Mekra Method. | Update operating practices while preserving valid existing knowledge |
| Organize this as a knowledge-centered repository. | Judge the operating approach with knowledge as the primary output |
| Upgrade the OKF version. | Assess and address the impact and need for an official specification transition |
| Inspect the current OKF. | Diagnose the suitability of its current structure and knowledge |
| Inspect the OKF structure and fix what needs improvement. | Diagnose and implement necessary improvements |

There is no exact wording to learn, nor do you need to know internal operation names. The agent starts with the [application guide](APPLICATION.md) and interprets the request together with the target's current state. "Apply it" delegates an overall assessment of necessary work; more specific requests guide exploration of relevant philosophy and facets within their purpose and scope.

The agent decides autonomously where the target supplies enough context and asks only when unresolved user intent materially affects the outcome. You may delegate judgment to the recommended approach or decide major choices together. On completion, the agent explains where new source material and knowledge belong and how to request their incorporation.

A facet is a judgment lens, not a preset or default configuration. Templates are also starting points to adapt when useful. Suitability is not determined by matching a file count or directory layout, but by whether knowledge is understood in the right context and whether the effects of change are reflected where needed.

## Relationship to OKF

Mekra Method is currently built on Open Knowledge Format (OKF), a format for representing knowledge that people and agents can both read and exchange. It continues the work previously called OKF Method. This repository provides the adopted principles and practical guidance.

This guide is not a copy of the specification or a framework every project must follow. The source for the official format is [GoogleCloudPlatform/open-knowledge-format](https://github.com/GoogleCloudPlatform/open-knowledge-format).

## Structure

| Location | Role |
| --- | --- |
| [`INTRODUCTION.md`](INTRODUCTION.md) | The problem, approach, and illustrative examples for newcomers |
| [`APPLICATION.md`](APPLICATION.md) | Target exploration, adoption judgment and questions, implementation, and operational handoff |
| [`FEEDBACK.md`](FEEDBACK.md) | Investigating adoption and long-term operating experience, drafting feedback, and submitting it |
| [`okf/`](okf/index.md) | Understanding of OKF, operating philosophy, reusable patterns, and conceptual relationships |
| [`facets/`](facets/README.md) | Thin lenses for finding important judgment from properties of the target |
| [`templates/`](templates/README.md) | Minimal scaffolding to copy into a project and adapt to its context |
| [`versions/`](versions/README.md) | OKF version baselines, Mekra Method releases and actual reference points, and migration records |
| [`experiments/`](experiments/README.md) | Hypotheses and methods under validation |
| [`notes/`](notes/README.md) | Observations and reflections not yet consolidated |

## Research and applied knowledge

Shareable conclusions are developed in the research repository and published here as practical guidance. Feedback can be submitted where the guide is used, while case research and validation continue in the research space.

Public material is updated according to [publication scope and language responsibilities](okf/distribution.md). The last reviewed source and published file baselines are kept in the [synchronization record](SYNC.json).

Adopted reasoning belongs in `okf/`; `facets/` helps locate relevant judgment; `templates/` provides optional application scaffolding. `notes/` and `experiments/` contain research material, and unadopted content is not a default basis for application. Observations from real use can be reflected back into related concepts and application materials when they prove reusable.

Guide limitations and reusable improvements discovered during adoption can return as [feedback](FEEDBACK.md). After actual use, you can ask in the target repository:

> `Review our experience using Mekra Method in this repository and draft feedback for https://github.com/muffinbox/mekra-method.`

The agent examines the target repository, relevant history, and the guide consulted to produce a shareable draft. Investigation and drafting start with the [feedback guide](FEEDBACK.md); external transmission stays within the scope delegated by the user. Ordinary applications do not require a separate report.

## Current baseline

- Recommended baseline: **OKF v0.2**
- Verification date and specification baseline: [`versions/current.md`](versions/current.md)

The public repositories' `main` branches contain the latest adopted guidance, while releases provide fixed baselines for comparison and reproduction. Mekra Method releases use the name `okf-<spec-version>-method-<sequence>`. See the [version guide](versions/README.md) for what the name means and how to record the commit actually used during adoption.

## License

Unless otherwise noted, files are licensed under [Apache-2.0](LICENSE). All files under `templates/`, including its README, are provided under [CC0-1.0](templates/LICENSE); copied or adapted templates do not require Mekra Method attribution. See the [distribution policy](okf/distribution.md#license-scope) for the scope.
