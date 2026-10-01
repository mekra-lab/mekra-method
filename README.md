# Mekra Method

*Knowledge finds its place.*

Mekra Method lets AI agents decide for themselves what to retain as knowledge and how to organize, connect, and maintain it, based on the available material and purpose.

Agents use the knowledge and context maintained this way to decide what to do in later work as the situation requires.

It provides application guides, templates, and operating knowledge to put the method into practice.

If you keep explaining the same background or tracing how one decision affects another task, you can record those reasons and relationships where they matter. Provide the knowledge and context needed for judgment, and leave the concrete way of working to the agent wherever practical.

## Get started

In the repository you want to work on, ask an agent with access to read and edit it:

> Apply https://github.com/mekra-lab/mekra-method/releases/latest to this repository.

The default adoption baseline is the latest formal release. Resolve its tag and commit at the start, then follow the application guide and related documents at that same revision. The documents on `main` may include later wording or link improvements.

The agent examines existing material and structure, then judges which knowledge to organize and connect. After making the changes, it explains where and how to incorporate new material and updates.

[**Introducing Mekra Method**](INTRODUCTION.md) presents the name, origins, slogan, central ideas, and principles. To apply the method, start with the [application guide](APPLICATION.md).

## Core perspective

**Keep sources of truth clear, share context where it is needed, and delegate judgment.**

Keep a clear reference for defining and changing a fact. In related concepts, restate as much as needed about what that fact means for their conditions and judgments. Avoid having several documents independently define and change the same fact; repeating it is not the problem. When the reference changes, review the related explanations too.

Mekra prioritizes organizing and maintaining the knowledge needed for judgment over prescribing detailed sequences of work. Agents choose how to work according to the purpose and situation, using the evidence and context they have actually read.

The [operating principles](PRINCIPLES.md) explain the core principles and their relationships. Follow the linked [operating knowledge](okf/index.md) for detailed reasoning and application boundaries.

## How to use it

You can also describe the work more specifically. Here are requests you can use with the same URL:

| Example request | Main intent |
| --- | --- |
| Apply Mekra to this folder. | Examine current material and organize the knowledge and context that are needed |
| Incorporate new material into the existing Mekra. | Review new knowledge and changes, then update the source of truth and affected context |
| Inspect this Mekra. | Diagnose its knowledge organization and operating practices |
| Inspect this Mekra and fix what needs improvement. | Diagnose and implement the necessary improvements |
| Update this Mekra to the latest formal release. | Preserve valid knowledge while adopting the selected Method baseline |
| Organize this as a knowledge-centered repository. | Judge the operating approach with knowledge as the primary output |

There is no exact wording to learn, nor do you need to know internal operation names. The agent starts with the [application guide](APPLICATION.md) and interprets the request together with the target's current state. "Apply it" delegates an overall assessment of necessary work; more specific requests guide exploration of relevant philosophy and facets within their purpose and scope.

The agent decides autonomously where the target supplies enough context and asks only when unresolved user intent materially affects the outcome. You may delegate judgment to the recommended approach or decide major choices together. On completion, the agent explains where new source material and knowledge belong and how to request their incorporation.

A facet is a judgment lens, not a preset or default configuration. Templates are also starting points to adapt when useful. Suitability is not determined by matching a file count or directory layout, but by whether knowledge is understood in the right context and whether the effects of change are reflected where needed.

## Relationship to OKF

Mekra Method currently uses Open Knowledge Format (OKF) to represent knowledge. OKF is a format that people and agents can both read and exchange. Mekra continues the knowledge and history previously called OKF Method. This repository provides the adopted principles and practical guidance.

For existing OKF material, you can ask: "Apply Mekra Method to the existing OKF material." If the format itself needs updating, ask: "Review the impact of the OKF specification change and update what is needed." These requests preserve valid existing knowledge and are interpreted within their purpose and scope. See the [application guide](APPLICATION.md) and [version guide](versions/README.md).

This guide is not a copy of the specification or a framework every project must follow. The source for the official format is [GoogleCloudPlatform/open-knowledge-format](https://github.com/GoogleCloudPlatform/open-knowledge-format).

## Structure

| Location | Role |
| --- | --- |
| [`INTRODUCTION.md`](INTRODUCTION.md) | Mekra's name, origins, slogan, central ideas, and design choices |
| [`PRINCIPLES.md`](PRINCIPLES.md) | The adopted principles, their core meaning and relationships, and links to detailed concepts |
| [`APPLICATION.md`](APPLICATION.md) | Adoption entry point: exploring the target, consulting relevant reasoning, implementation, verification, and operational handoff |
| [`FEEDBACK.md`](FEEDBACK.md) | Investigating adoption and long-term operating experience, drafting feedback, and submitting it |
| [`okf/`](okf/index.md) | Detailed reasoning and boundaries of principles, operating patterns, adoption judgments, and format guidance, currently expressed in OKF |
| [`facets/`](facets/README.md) | Thin lenses for finding important judgment from properties of the target |
| [`templates/`](templates/README.md) | Minimal scaffolding to copy into a project and adapt to its context |
| [`versions/`](versions/README.md) | OKF version baselines, Mekra Method releases and actual reference points, and migration records |
| [`experiments/`](experiments/README.md) | Hypotheses and methods under validation |
| [`notes/`](notes/README.md) | Research, observations, questions, and the background and follow-up to judgments |

## Research and applied knowledge

Shareable conclusions are developed in the research repository and published here as practical guidance. Feedback can be submitted where the guide is used, while case research and validation continue in the research space.

Public material is updated according to [publication scope and language responsibilities](okf/distribution.md). The last reviewed source and published file baselines are kept in the [synchronization record](SYNC.json).

The core meaning and relationships of adopted principles belong in `PRINCIPLES.md`, with detailed reasoning in `okf/`; `facets/` helps locate relevant judgment; `templates/` provides optional application scaffolding. `notes/` and `experiments/` contain research material, and unadopted content is not a default basis for application. Observations from real use can be reflected back into related concepts and application materials when they prove reusable.

Guide limitations and reusable improvements discovered during adoption can return as [feedback](FEEDBACK.md). After actual use, you can ask in the target repository:

> `Review our experience using Mekra Method in this repository and draft feedback for https://github.com/mekra-lab/mekra-method.`

The agent examines the target repository, relevant history, and the guide consulted to produce a shareable draft. Investigation and drafting start with the [feedback guide](FEEDBACK.md); external transmission stays within the scope delegated by the user. Ordinary applications do not require a separate report.

## Maintainer and contact

Mekra Method is developed and maintained by [Mekra Lab](https://github.com/mekra-lab).

- General inquiries and collaboration: [contact@mekralab.org](mailto:contact@mekralab.org)
- Adoption and usage feedback: [feedback@mekralab.org](mailto:feedback@mekralab.org). See the [feedback guide](FEEDBACK.md) for GitHub Issues and submission details.

## Current baseline

- Recommended baseline: **OKF v0.2**
- Verification date and specification baseline: [`versions/current.md`](versions/current.md)

The latest formal release is the default adoption baseline. Public `main` can receive reviewed corrections to wording, links, and usability between releases when they preserve adoption meaning. Changes to adoption judgments or core principles reach public `main` together with a release. Publish a new release to include an improvement in the formal adoption baseline. New Mekra Method releases use `mekra-X.Y`, or `mekra-X.Y.Z` for a separately published patch. Record the OKF specification baseline separately and preserve existing tags. See the [version guide](versions/README.md) for change levels and recording the actual reference commit.

## License

Unless otherwise noted, files are licensed under [Apache-2.0](LICENSE). All files under `templates/`, including its README, are provided under [CC0-1.0](templates/LICENSE); copied or adapted templates do not require Mekra Method attribution. See the [distribution policy](okf/distribution.md#license-scope) for the scope.
