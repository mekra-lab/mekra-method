---
type: Concept
title: Knowledge design exploration and sufficiency
description: Compare meaningful arrangements against actual use and changes, and judge the scope of exploration and reasons for a choice
---

# Knowledge design exploration and sufficiency

Design knowledge structures to support judgments needed for actual use and expected changes. Consider reusing existing arrangements alongside alternatives that differ in concept granularity, integration, relationships, and internalized reasoning, then choose what fits the purpose. Available approaches and evidence for judging sufficiency support [autonomous judgment](agent-autonomy.md). A plausible first arrangement does not establish that important possibilities have been explored.

This document addresses exploring and choosing arrangements. [Knowledge internalization](knowledge-internalization.md) covers semantic boundaries and necessary context; [adoption judgment](adoption.md) covers initial build scope, consultation, and completion. The current [OKF representation requirements](okf-format.md), sources of truth, permissions, and target constraints set the conditions for candidates.

## Starting a comparison

Derive comparison questions and change scenarios from the work the user intends to delegate, conditions and exceptions in actual material, previously difficult judgments, and expected changes. Choosing only questions that a candidate can easily answer after designing it can make an insufficient arrangement appear sufficient. Include needs discovered during exploration, and distinguish assumptions from purposes actually stated by the user.

Consider both answering representative questions and combining knowledge for different questions later. Even knowledge not directly used in a current question can preserve valuable premises, exceptions, and meaningful relationships. Rather than predicting every future question, keep the meaning and applicability of knowledge from being tied to a single answer.

## Developing meaningful alternatives

Focus alternatives on arrangements that change actual discovery, judgment, and updates, rather than variants differing only in names or file counts. Relevant possibilities include reusing knowledge, separating independent judgment units, integrating conditions that must be understood together, connecting direct relationships, deepening internalized reasoning, and combining individual concepts with synthesis. [Concept boundaries and organization](knowledge-internalization.md#concept-boundaries-and-organization) explains when these approaches help.

Design depth and document length are separate choices. Thorough exploration can lead to linked short concepts or a longer document containing context that needs to be understood together. Reusing existing knowledge with limited additions can also be the result of careful consideration. There is no need to make a candidate that skips analysis for comparison.

Do not fix the number or types of candidates or require every combination. Compare provisional concept boundaries, key relationships, and representative explanations; try the parts needed where differences are hard to judge. There is no need to write every candidate's complete documents. Preserve the same knowledge, conditions, and exceptions when comparing organizational effects; if candidates also differ in coverage, make that difference explicit.

## Perspectives on sufficiency

| Perspective | Differences to examine through actual questions and changes |
| --- | --- |
| Discovery | Can the needed concepts and evidence be found accurately? Does finding them require unrelated reading or repeated link traversal? |
| Judgment | Can conditions, exceptions, and relationships be understood? Is knowledge needed together scattered, or are independent judgments unnecessarily grouped? |
| Updates | Can change responsibilities and affected concepts be found? Do outdated judgments or conflicting definitions remain after an edit? |
| Operating cost | Are the burdens of construction, discovery, review, maintenance, and user correction appropriate for the use? |
| New uses | Can new facts and questions connect to existing knowledge? Has explanation tailored to a particular question lost meaning or relationships? |

These perspectives are not a fixed scorecard. One arrangement may favor discovery while another favors contextual understanding or maintenance cost. Judge the benefits and losses that matter for the target rather than erasing differences in one combined score. Distinguish expectations with limited evidence from behavior actually checked.

## Expanding and concluding exploration

When favorable candidates cluster at one boundary of the range examined, consider additional designs beyond that boundary. For example, if increasingly separated concepts are easier to find and update, examine whether further separation retains those benefits and whether loss of context or link maintenance burdens grow. The same judgment can apply to integration, internalization depth, or reuse scope. Also consider whether combining another arrangement with a change in one direction can reduce its costs.

Conclude exploration when additional designs offer little benefit or increase losses, costs, or constraints, and sufficient evidence supports a choice. There is no need to prove an optimum on every dimension or mathematical convergence. Viable alternatives with different strengths can remain. If access limits or the work budget prevented examination of important possibilities, reflect that uncertainty in the reasons for the choice.

## Representative options and user consultation

If viable alternatives with different strengths and operational consequences remain, [present representative options to the user](construction-consultation.md#discussing-options-for-an-initial-build), explaining the recommendation. Describe what knowledge each organizes, how it is arranged, and what changes when adding material, asking questions, or incorporating updates. The user can accept the recommendation, select another option, adjust parts, or delegate judgment.

Carry forward explicit delegation that already covers the choice. The agent determines properties, filenames, directories, and similar details within the established direction; do not add variants without meaningful operational differences as user choices. Explain the chosen arrangement and key reasons without requiring reports of every alternative or the exploration process.

[Preserve reasons and reconsideration conditions in the target's operating context](knowledge-operation.md#handing-over-design-choices) when they matter for later work. Distinguishing reasons grounded in observation from assumptions still to check helps later agents judge changed conditions instead of preserving the structure unconditionally or rebuilding without reason.

## An example of organizing the same knowledge differently

Consider hypothetical order-processing knowledge. Cancellation is allowed before dispatch is confirmed; cancellation before payment requires no refund. After payment, cancellation requires a refund, and refund failure leaves it incomplete. Inventory reservations for canceled orders are released. Every arrangement below preserves these conditions, exceptions, evidence, and change responsibilities.

| Arrangement | How it holds the knowledge | Expected benefits and costs |
| --- | --- | --- |
| Integrated | One cancellation document explains timing, payment state, inventory release, and refund failure. | The cancellation process is easy to understand together, but reviewing refunds alone may require unrelated reading. |
| Separated | Eligibility, payment and refunds, and inventory reservations are separate concepts explaining their conditions and effects on each other. | Individual questions and changes can be addressed directly, but understanding cancellation as a whole requires moving between concepts. |
| Combined | Individual concepts remain, while a synthesis explains cancellation sequence and interactions. | It can support both individual discovery and overall understanding, but the synthesis context also needs maintenance after changes. |

Compare cancellation before payment and refund failure after payment in each arrangement to see whether necessary conditions are missed. Also compare the concepts and explanations to revisit if inventory release timing changes. In the separated arrangement, a link to another file does not replace explaining what a condition means for the current concept. The combined arrangement's synthesis explains how concepts act together, rather than merely listing links. Keep definition and change responsibility with the [source of truth](source-of-truth.md).

If separation continues to help, consider separating payment state from refund-failure handling further. If integration is preferable, consider expanding the related processing explained together. This illustrates possible comparisons, not an experimental finding that one arrangement is superior. Check actual effects through [adoption experience](feedback.md).

The [comparison using actual OKF bodies](knowledge-design-example.md) represents the same source material in three arrangements and shows which evidence is read and which restatements change for the same question and rule update.
