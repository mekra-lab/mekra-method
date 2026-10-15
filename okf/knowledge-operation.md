---
type: Concept
title: Knowledge use and operational handoff
description: Check the connection between organized knowledge and actual use, and leave operating context for continued intake and updates
---

# Knowledge use and operational handoff

A knowledge build does not end with creating files. To sustain operation, check the scope in which knowledge can be found and used for the agreed purpose, and leave the target with guidance for incorporating later material and changes. The environment actually connected and the remaining scope inform [judgment of adoption completion](adoption.md#the-role-and-completion-expectations-of-an-initial-build).

[Entry points and discovery paths](structure-and-discovery.md) provide ways to reach knowledge. This document addresses using those paths and continued operation; [operational observations](feedback.md) separately examine whether use improves results. When a new operating direction needs to be decided, discuss it while carrying forward [existing intent and delegation](construction-consultation.md).

## Connecting knowledge to actual use

Stored knowledge can inform work only if the agent or product that uses it can discover and read it. Examine the target environment's entry instructions, discovery paths, and [access permissions and how they are implemented](disclosure-boundary.md), and check whether relevant concepts and evidence can be found and used for actual questions. Do not extend a connection confirmed in the current task to all other conversations, devices, or execution environments. Connecting knowledge for a development agent to a product AI's inputs may be a separate scope of work.

State what knowledge was organized and which usage environment was checked when reporting completion. If describing automatic updates, explain the execution mechanism actually connected and the scope in which success was confirmed. A saved index, a schedule setting, a successful run, and the incorporation of changes each require separate evidence. If connections or automation are outside the request's scope, explain what remains. Checking use does not require detailed logs for every task. Being able to read material and obtaining better results from using it are [different observations](feedback.md).

## Operation after adoption

Build or transition requests establish or change the target's operating system; follow-up requests such as "incorporate new material into the existing Mekra" use that system. During adoption, Mekra Method should leave operating guidance fitted to the target, while routine material incorporation continues from the target's own sources of truth, instructions, and knowledge graph. This distinction lets the target operate without rerunning Mekra Method's adoption procedure for every later update.

In follow-up updates, set exploration scope from the existing knowledge graph and the effects of the change. Do not repeat the breadth of initial design exploration every time. Redesign the needed scope when changed purposes, material, or constraints alter the sufficiency of the existing arrangement.

Omissions, inconsistencies, and new relationships discovered during routine reading and use also provide [opportunities to enrich context](context-propagation.md#context-discovered-through-reading-and-use). Incorporate them within the target's granted editing permissions and delegated scope; reading access alone grants neither writing authority nor automatic updates. Distinguish checks needed for the current request from additional maintenance, and address important deferred impacts together with the risks of reuse and triggers for resuming review.

Delegating design judgment does not mean the user should have to infer how to use the result afterward. At completion, explain the actual locations selected for source material and new knowledge and how to request incorporation, and leave that information in the target repository as well. If source material is external or no separate intake location is useful, explain that operating model instead.

The intake location depends on the responsibilities described in [source material and derived artifacts](external-sources.md) and the target's real material flow. Relevant [facets](../facets/README.md) may help identify which judgments deserve attention. Do not create a directory such as `raw/` uniformly. In a progressive transition, leave the trigger and method for absorbing unconverted knowledge so follow-up work can continue. Operational handoff is therefore part of completing a build or transition and part of the progressive-transition strategy. The practical entry point is the [application guide](../APPLICATION.md).

Reusable discoveries from operational handoff can be connected to [feedback](feedback.md). Later reviews of actual use should likewise examine the conditions under which the guide supported judgment and operation, rather than how closely it was followed. Recording a verifiable [reference baseline](../versions/README.md) and the scope actually adopted helps distinguish the influence of the guide at that time from later autonomous changes. Feedback is an optional activity that returns observations about the guide's usefulness and limits to research. Autonomous adaptation during application is not itself something that must be reported, and whether feedback is sent does not determine whether adoption is complete.

## Handing over design choices

Leave reasons for the current arrangement in the target when they will inform later use, updates, or redesign. Explain in relevant concepts or target-specific operating context which uses and constraints motivated separating or combining concepts, which assumptions the design depends on, and what changes would warrant reconsideration. Reuse sufficient existing explanations through links; no separate design record or fixed fields are required.

For example, if cancellation, refunds, and inventory were separated to support independent inventory queries and updates, preserve that reason and the condition for considering a synthesis if repeatedly assembling the overall flow becomes burdensome. The [body comparison example](knowledge-design-example.md#carrying-the-chosen-arrangement-forward) shows such a handoff. Distinguish observation from expectation, and limit claims of delegation to what the user actually chose or delegated.

Preserve reusable reasons for the adopted arrangement; there is no need to record every candidate considered or internal thought process. Keeping the reasons does not freeze the current structure. When intended use or assumptions change, update the affected knowledge and design explanation together. If past judgments need preserving, distinguish them from the current operating baseline.

## Optional operating preferences

After a build or transition, judge whether repository-level operating preferences would improve later work. Do not mechanically list every possible preference; select only those with real value for the target's material and workflow, and express them in terms the user can understand. If the user already stated the same preference or delegated the choice, it may be applied without asking again.

Examples that may be worth adding to the target's root `AGENTS.md` include:

- For document-like derived outputs, prefer creating a human-readable, editable source such as Markdown before deriving PDF, DOCX, PPTX, or similar final formats when that intermediate source is useful. Do not force it when the final format is itself canonical or the Markdown layer adds no value.
- After producing a report, analysis, design document, or similar output, check whether newly established concepts, rules, judgments, or relationships are worth reflecting into OKF. Update them when the case is clear and within delegated scope; ask when it depends on user intent. Do not copy the entire output into knowledge.
- When the user has not specified a method for a choice, prefer the recommended option and ask only about unresolved intent that materially changes the outcome.
- After substantial work, distinguish one-off notes from knowledge with durable reuse value and consider internalizing the latter into relevant OKF concepts.
- In repositories where provenance of derived outputs matters, preserve a path back to source material, sources of truth, or related OKF concepts.

Do not present operating principles already adopted by Mekra—such as [operating principles](../PRINCIPLES.md), [source of truth and context](source-of-truth.md), or [context propagation](context-propagation.md)—as user preferences that can simply be toggled on or off. Facets do not re-own those principles; they only connect environments to judgments that become especially important.

The [AGENTS template](../templates/AGENTS.md.template) provides an example section to copy. Persist only target-specific preferences agreed or delegated under the reasoning above; do not add every example wholesale.
