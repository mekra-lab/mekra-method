# Feedback guide

Experience during adoption and subsequent real operation can help improve Mekra Method guidance and patterns. Feedback is optional; application and operational handoff are complete even when nothing is sent. The reasoning is in [feedback from adoption](okf/feedback.md).

## When to recommend it

Recommend brief feedback when reviewing usefulness and fit reveals something that may help other applications. Examples include a case that existing facets and OKF knowledge do not explain well, conflicting principles or unclear boundaries, recurring template friction, problems caused by a default scope, or a simpler and more effective approach. Knowing what worked and under which conditions can also be useful evidence.

Autonomous adaptation alone does not need to be reported. Keeping an existing `sources/` directory or reviewing a small repository in one pass are already allowed choices. Even a large adaptation may have little reporting value if current guidance explains it well, while a small ambiguity may matter if it repeats. In ordinary applications, omit a feedback request and do not ask for a "nothing unusual" report.

An operational handoff can add something like:

> This application exposed a case where two sources of truth were valid under different conditions, and the current guide did not make the judgment clear. That may be useful for improving the guide. If you want, I can draft a shareable feedback report.

## Looking back after use

In the repository where you use the guide, you can ask your agent:

> `Review our experience using Mekra Method in this repository and draft feedback for https://github.com/mekra-lab/mekra-method.`

Use the URL or name of the repository whose guidance you consulted. The agent examines the target repository and that guide, investigates the conditions under which the guide helped or fell short in real operation, and presents a shareable draft. Choose the investigation's depth and structure to fit its purpose and available material. This request alone does not authorize external transmission; if the content and destination have already been delegated, continue within that scope.

Alongside current documents, examine accessible Git history, adoption records, and operating context as needed. Useful clues include how an introduced structure was maintained, adapted, or removed; whether changes to sources of truth were reflected in related concepts; and why practices absent from the guide took hold. A different arrangement may have been more appropriate in practice, so do not score compliance. Discoveries made during adoption and later retrospectives need not be split into separate modes or fixed schedules.

Where possible, identify the repository, commit, or release actually consulted and compare it with the current guide. Distinguish limitations that have since been addressed from problems that remain. If the baseline cannot be found, leave it unverified; similar wording alone does not establish that a particular release was adopted. The [specification, release, and reference commit](versions/README.md) are distinct baselines.

For example: "We first built this using our own instructions, later consulted the guide to improve only the main concepts, and are now reviewing the experience against a newer guide." If the original instructions cannot be found, leave them unverified and record only the scope of later adoption and the changes observed. If the model, tools, material, or additional support from the user also changed, consider those changes when interpreting the effects.

Git history shows what changed, but does not fully explain how often documents were read or why they changed. A long period without edits does not by itself imply neglect, nor do repeated revisions or deletions necessarily mean failure. Supplement the history with existing operating records or the user's explanation when needed, and distinguish confirmed changes from interpretations of their causes. Even with limited history, a draft can draw on observations supported by current material.

## Filling information gaps through conversation

Use accessible material and records first, then ask the user about information needed for feedback that remains unverified. Investigate adoption scope, knowledge depth, and roles alongside other systems; carry forward purpose and experience already provided. The user's account can fill gaps about inaccessible operating environments. Distinguish [information sources and ways to verify them](okf/feedback.md#information-sources-and-how-to-verify-them).

Frame questions with options and free text suited to the target and missing information. Do not recommend or preselect answers about actual experience. [Discussing options for an initial build](okf/adoption.md#discussing-options-for-an-initial-build) helps decide future work; here, the purpose is to collect experience and evidence. Recommendations can be offered when proposing improvements after the response.

Show only the findings needed to understand the questions, and let the user answer or supplement the relevant parts. Choose question count and order from the material and context. One or two questions may fill the gaps needed for a detailed report; if existing material is sufficient, omit further questions.

### Example — Adding one account of use

In this hypothetical case, the adoption purpose is already known, but records of usage experience are limited. The explanation and question below are not a fixed survey; in an actual investigation, connect them to the evidence and scope examined.

> I confirmed the main rules and their links to related documents. The current records do not show how you experienced the updates in actual work after the change.
>
> **What was your experience using the related knowledge after the change?** You can select several items or describe it yourself.
>
> - The needed content was incorporated and helped with the work
> - Missing content or outdated explanations caused difficulty
> - I used it after the change and had no particular difficulty
> - I have not used it since the change
> - I have used it but find it difficult to judge
> - Another experience: free text
>
> If you want, add one task where it helped or caused difficulty. You can also skip the question.

In the final feedback, distinguish investigated connections from the user's reported experience, and interpret causes of update outcomes and contributions of individual tools within the evidence available.

## What to include

Synthesize the agent's investigation and the user's responses into a self-contained feedback report that can be read and reviewed independently. The report can serve as the basis for a GitHub issue or email body and does not need to be saved as a separate file. Select the items that materially support judgment and explain them at the depth needed.

- Application context: request, target purpose, character and scale, relevant facets, actual adoption scope and knowledge depth, division of roles with existing systems and other tools, and the guide or baseline used.
- Observation: what was useful, what explanation did not fit, and what actually happened.
- Response and limitations: what was adapted, whether it helped, and what remains unverified.
- Possible improvement: related documents, clarification that may help, and questions worth checking in other contexts.

No fixed form or score is required. Distinguish observed facts from guesses about cause and from proposals. When verifiable, include the period and scope examined, the Mekra Method repository and commit or release consulted, and the target OKF specification version so different baselines are not confused. If there are no usage records or no improvements were identified, explain that limitation; do not invent effects or problems merely to have something to report.

Distinguish confirmation that documents exist, evidence that an agent read and used them, the user's reported experience, and measured outcomes. If the only evidence is an AI response saying "I applied it," preserve it as a report at that level. Multiple bundles and copies from the same working environment may be related observations; do not add them up as independent successes. The reasoning behind these distinctions is in [operational observations](okf/feedback.md#observations-from-real-operation).

Generalize the draft to preserve only relationships and conditions needed for judgment. Do not copy company, customer, or personally identifying information, private-repository URLs, original documents, code, or logs directly. Apply the same standard to email. If generalization cannot preserve the meaning of the case, external submission can be skipped.

## How to send it

Public feedback should go to the repository whose guidance was used.

| Guidance used | Feedback destination |
| --- | --- |
| `mekra-method-kr` | [existing issues](https://github.com/mekra-lab/mekra-method-kr/issues) · [new issue](https://github.com/mekra-lab/mekra-method-kr/issues/new) |
| `mekra-method` | [existing issues](https://github.com/mekra-lab/mekra-method/issues) · [new issue](https://github.com/mekra-lab/mekra-method/issues/new) |

A problem shared by both repositories only needs to be reported once. If relevant discussion already exists, connect to that issue instead of submitting duplicate reports or asking the user to translate and submit the same content twice. Access to the private research repository `mekra-method-dev` is not required for submitting feedback.

Email for either repository can be sent to [feedback@mekralab.org](mailto:feedback@mekralab.org). It can be used when a public issue is unsuitable or GitHub submission is inconvenient. The agent can prepare the subject and body for the user to send from their usual email client.

For general inquiries and collaboration proposals, contact [contact@mekralab.org](mailto:contact@mekralab.org).

Choose the route based on available tools and the user's preference. Do not judge submission capability only from whether GitHub CLI is installed; an authenticated tool or browser may also be available. Do not require installation of a new tool or a new login solely for feedback.

| Route | How to use it |
| --- | --- |
| GitHub Issue | When public sharing is appropriate and an authenticated write path is available, draft and submit a title and body. If a related issue already exists, connect to that discussion rather than opening a duplicate. |
| Email | Prepare a subject and body for the shared address above. If an email tool is connected and transmission has been requested, it may be used. |
| Skip transmission | If no convenient route exists, provide the draft only or omit feedback. Application work can still be completed. |

External transmission occurs only within the scope the user requested. General delegation to apply Mekra Method does not by itself authorize sending an issue or email. Present the content and destination to be sent, and for a GitHub Issue make clear that it will be public. If the user has already delegated transmission of that content through that route, do not ask for the same intent again. After sending, report the issue link or actual send result; drafting alone is not a completed transmission.

## Boundaries between feedback and reuse

Mekra Method does not require rights to the target repository, source materials, code, or logs examined to prepare feedback merely because it receives that feedback.

Reviewing feedback for clues to improvement is distinct from incorporating a submitter's specific wording, code, or detailed case into published materials. Before copying, translating, or adapting such content for inclusion, check what the submission channel and the terms in effect at the time permit, and seek further clarification from the submitter when needed.

General problems or ideas identified in feedback can inform the project's own explanations and knowledge. Even then, check for personally identifying information, confidential material, or protected expression belonging to others.

## How received feedback is used

Ambiguity or errors raised in feedback are reviewed in the related documents. Cases without a conclusion can be connected to [notes](notes/README.md), and hypotheses needing validation to [experiments](experiments/README.md). A suggestion appearing in a public issue or email is not automatically adopted guidance; confirmed conclusions are reflected in the relevant OKF concepts, facets, and templates.

Do not copy the original text or detailed cases from privately received feedback into a public repository without separate permission to disclose them. If they are worth retaining for research, capture shareable observations and questions in notes or experiments. If the original must be retained, preserve its existing private scope and stay within the permitted uses.

Keep public intake separate from storage of research cases. Detailed analysis and validation can remain in the research space, while public guidance reflects only shareable evidence and generalized conclusions. Translation or explanation problems specific to one repository can be reviewed there; improvements to shared principles or patterns should connect the necessary changes across published repositories. Public issues should link only to publishable outcomes and changed documents; receiving feedback does not create authority to disclose private source material.
