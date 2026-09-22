# Introducing Mekra Method

Mekra Method is **a method for organizing and maintaining knowledge and context for AI agents**. It brings project facts, decisions, reasons, and relationships into knowledge that people can read, helping agents find and understand that context when making judgments in later work.

This document introduces the name, origins, central ideas, and design choices. To apply the method, start with the [application guide](APPLICATION.md). The adopted judgments and their reasoning live in the [operating knowledge](okf/index.md).

## Name and origins

**Mekra is inspired by the Korean word for context.** Here, context is the background that makes a fact understandable: why it matters, under which conditions it holds, and how it relates to other knowledge. The name connects with the method's interest in making that context available where related concepts are explained.

Mekra developed through research into and practical work with Open Knowledge Format (OKF). The project has carried its knowledge and history through the names **OKF Lab → OKF Method → Mekra Method**. While interpreting and applying the format, it developed an operating perspective on what knowledge to retain, how to connect it, and which judgments to leave to agents.

It also drew inspiration from the ontological perspective of expressing meaning through relationships between concepts.

The name Mekra gives this operating method a name of its own. It connects and explains existing judgments under that name, while remaining built on OKF. The [version guide](versions/README.md) records continuity across repository names and releases.

## Knowledge finds its place.

The slogan's “place” is a metaphor for the context in which knowledge can support understanding and judgment. Knowledge finds its place when there is a clear reference for defining and changing a fact, its meaning is understandable in related concepts, and its evidence and relationships can be found when needed. One fact can have different implications for several concepts, so that place need not be a single file.

The phrase expresses the direction of the method in a few words. It does not impose an admission test for recording knowledge or a fixed rule for where to put it. What to record and how to structure it remain decisions made for the purpose and context.

## Central ideas

**Keep sources of truth clear, share context where it is needed, and delegate judgment.**

The first idea is to **keep definition and change responsibility clear while deliberately distributing the context needed for understanding across related concepts**. Establish where a fact is defined and changed, and explain its effects on the meaning, conditions, and exceptions of other concepts where those concepts are discussed. A single source of truth does not imply a single location for context.

The second idea is to **trust capable agents to interpret context and exercise judgment**. Instead of prescribing every sequence of work, provide the reasons, conditions, and relationships that support judgment, and leave the concrete working method to the agent wherever practical. That autonomy depends on sufficient evidence and context that the agent can actually find and read.

The two ideas work together. Natural-language explanations preserve relationships and reasons so agents can use their ability to interpret context and judge what the situation calls for. When facts change or new knowledge arrives, update both the source of truth and the related explanations whose meaning changes. **Distributing context brings a responsibility to maintain it together.**

Consider a hypothetical change to a booking policy's cancellation deadline. The policy document defines the deadline; refund and customer support documents explain what it means for their work. An agent can read those relationships and judge what to inspect and change within the request's scope. Distributing explanations alone does not guarantee that it will discover every effect or update everything correctly, so the evidence actually read and the resulting changes still need checking.

## Principles at a glance

These are summaries of adopted principles. The linked documents explain their scope and reasoning.

- **Distinguish canonical responsibility from the location of context.** Code, configuration, policies, and existing documents can be sources of truth, while related concepts can restate the context needed for understanding. The concern is independent definition and change in several places, rather than repetition of the same fact. [Source of truth and context](okf/source-of-truth.md)
- **Retain the meaning, reasons, conditions, and relationships needed for judgment.** Explain implications within a concept when links or summaries alone would leave them unclear. Procedures can also be knowledge worth retaining when they support judgment. [Knowledge internalization](okf/knowledge-internalization.md)
- **Reflect the meaning of a change in related knowledge.** Find and update concepts and explanations whose meaning changes when the source is revised. [Context propagation](okf/context-propagation.md)
- **Choose structure and depth from actual need.** Work with the existing structure and how knowledge is used, rather than moving all material or imposing the same directories and categories everywhere. [Operating principles](okf/operating-principles.md)
- **Start from autonomous agent judgment.** Discretion in interpretation and working method is distinct from authority to arbitrarily change facts, policies, or permissions. Tools can also verify clearly defined constraints. [Agent autonomy](okf/agent-autonomy.md)
- **Distinguish the status of a record from the certainty of its content.** Uncertain claims can be maintained with their status and evidence made clear. Maintaining a record is different from accepting its claim as fact. Proposals under investigation are also distinguished from adopted operating knowledge. [Source of truth and context](okf/source-of-truth.md) · [Operating knowledge](okf/index.md)

## What Mekra prioritizes

Mekra brings canonical responsibility, distributed context, and autonomous judgment into a shared operating approach. The following questions show its emphasis in concrete design work.

| Design activity | The question Mekra emphasizes |
| --- | --- |
| Choosing directories and document formats | Which structure actually helps people and agents understand and update this target's knowledge? |
| Collecting material and making it searchable | What does the fact we found mean here, and where is the reference for defining and changing it? |
| Specifying the agent's sequence of work | What evidence and context would let the agent judge how to proceed? |
| Updating a changed document | Which other concepts and explanations change meaning as a result? |

These questions do not define the limits of particular products or other methods. They can be used alongside search and RAG, work procedures, and tool-based checks. Within that combination, Mekra prioritizes **organizing and maintaining the knowledge that supports judgment**. Its effects are assessed through actual use, observing the effort needed to find, understand, and update knowledge, along with maintenance costs.

## Relationship to OKF

OKF is a format for representing knowledge that people and agents can read and exchange. Mekra is currently built on that format and provides an approach to deciding what to record and connect and how to maintain it.

The source of truth for the official format is [GoogleCloudPlatform/open-knowledge-format](https://github.com/GoogleCloudPlatform/open-knowledge-format). Mekra's operating principles are its own judgments on top of that specification, rather than additional official requirements or a separate extension specification. The new name preserves the distinction between the current implementation basis and responsibility for the official format.

## Getting started and further reading

Use the guide URL in [getting started in the README](README.md#get-started) and ask your agent to apply Mekra Method to the repository where you work. The agent examines existing material and structure, judges the useful scope, and explains how to handle new material and changes after adoption.

- [Application guide](APPLICATION.md): exploring the target, resolving necessary questions, making changes, and continuing to use the result.
- [Operating knowledge](okf/index.md): adopted principles and the reasoning behind them.
- [Facets](facets/README.md): lenses for finding important judgments from a target's properties.
- [Feedback guide](FEEDBACK.md): sharing effects and limitations observed in actual use.
