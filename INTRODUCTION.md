# Introducing Mekra Method

This introduction is for people new to Mekra Method. To apply it, start with the [application guide](APPLICATION.md). The adopted operating judgments and their reasoning live in the relevant [knowledge documents](okf/index.md).

## When the material exists, but the context still needs explaining

Project knowledge accumulates in different places. Meeting notes record why a decision was made, operating guides describe how to do the work, and code and configuration express current behavior. To answer "What needs to change if this condition changes?", you need to find the material and reconstruct the relationships between it.

The same problem can arise when working with an AI agent over time. Reading the files may not be enough to understand which account is current or how one decision affects another part of the project. A person then has to explain the context again.

Mekra Method is an approach to organizing and maintaining knowledge and context for use in later work. It provides the knowledge and context needed for judgment, while leaving the concrete way of working to the agent wherever practical.

## What should be authoritative, and what needs explaining elsewhere?

Imagine running a booking service. The following is a hypothetical example of how the approach works, not a report of measured results.

You decide to move the cancellation deadline from one day before a booking to two days before it. The policy document states the new deadline accurately. But unless refund guidance and customer support documents explain its implications, each task still requires someone to work them out again.

With Mekra, the policy document remains the clear reference for defining and changing the cancellation deadline: its **source of truth**. The refund explanation describes what that deadline means for refund eligibility. The support explanation describes which conditions to check and communicate. Each connects back to the policy source.

The same fact can be explained in several places while retaining its source of truth. What matters is that the refund and support documents do not independently define different cancellation deadlines. When the deadline changes, use the source as the reference and review the explanations whose meaning changes. The reasoning is in [source of truth and context](okf/source-of-truth.md), [knowledge internalization](okf/knowledge-internalization.md), and [context propagation](okf/context-propagation.md).

| How the knowledge is organized | What later work can draw on |
| --- | --- |
| Only the changed policy is recorded | The new deadline itself. Its effects on refunds and support still need to be found and interpreted. |
| Related explanations are updated from the policy | The new deadline, what that condition means in each activity, and a path back to the supporting source. |

Those explanations do not mean an agent will automatically discover every effect. Whether it actually reads the relevant material, whether the explanations are current, and whether it has authority to make changes still matter.

## Why leave the working method to the agent?

It is difficult to prescribe the files to read and steps to take for every possible change. Mekra works on the premise that capable agents can interpret reasons, conditions, and relationships expressed in natural language. It prioritizes organizing and maintaining that basis for judgment.

In the booking example, making the policy's effects on refunds and support understandable gives the agent a basis for examining relevant explanations and implementation within the request's scope, then choosing how to work. Sufficient context and actual exploration must support that judgment.

This discretion does not grant authority to arbitrarily change policy or publish material externally. Tools can also check clearly defined constraints. [Agent autonomy](okf/agent-autonomy.md) explains the scope in more detail.

## What happens when you apply it?

As shown in [getting started](README.md#get-started), ask your agent to apply this guide in the repository where you work. The agent examines existing material and instructions, builds on valid sources of truth and structures, and judges which knowledge to organize and at what depth. It asks when unresolved user intent would change the outcome and makes delegated choices in context.

The result may include explanations of relevant concepts and relationships, connections that help people and agents find them, and guidance for incorporating new material and changes. There is no need to copy the same folder layout into every project or rewrite all source material. Recording the actual choices and usage instructions helps the user continue the work.

Applying Mekra alone does not guarantee persistent agent memory or correct judgment. Later work must be able to find and read the relevant knowledge and update it when things change. [Experience in use](FEEDBACK.md) can show whether less context needs to be explained again, whether exploration becomes easier, whether outdated reasoning persists, and what maintenance costs arise.

## When might it help?

Consider it when knowledge and decisions carry across tasks, one change affects several concepts, or people repeatedly explain context specific to the project. Targets can include software projects as well as repositories where knowledge is the main material, such as research collections or fictional settings.

If the material needed for a single task is brief and sufficient, or existing documents already support understanding and updates well, a separate knowledge graph may cost more than it adds. Organize the scope that is useful and build on existing practices where they are sufficient.

## How Mekra relates to OKF

Mekra Method is currently built on Open Knowledge Format (OKF). OKF is a format for representing knowledge that people and agents can read. Mekra is an operating method for deciding what to record and connect and how to maintain it using that format. The [OKF specification repository](https://github.com/GoogleCloudPlatform/open-knowledge-format) is the source for the official format.

It continues the knowledge and history of OKF Method. The name Mekra is inspired by the Korean word for context. The [version guide](versions/README.md) explains continuity across names and releases.
