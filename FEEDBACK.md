# Feedback guide

Experience from real application can help improve okf-lab guidance and patterns. Feedback is optional; application and operational handoff are complete even when nothing is sent. The reasoning is in [feedback from adoption](okf/feedback.md).

## When to recommend it

Recommend brief feedback when reviewing usefulness and fit reveals something that may help other applications. Examples include a case that existing facets and OKF knowledge do not explain well, conflicting principles or unclear boundaries, recurring template friction, problems caused by a default scope, or a simpler and more effective approach. Knowing what worked and under which conditions can also be useful evidence.

Autonomous adaptation alone does not need to be reported. Keeping an existing `sources/` directory or reviewing a small repository in one pass are already allowed choices. Even a large adaptation may have little reporting value if current guidance explains it well, while a small ambiguity may matter if it repeats. In ordinary applications, omit a feedback request and do not ask for a "nothing unusual" report.

An operational handoff can add something like:

> This application exposed a case where two sources of truth were valid under different conditions, and the current guide did not make the judgment clear. That may be useful for improving the guide. If you want, I can draft a shareable feedback report.

## What to include

Draft from context the agent already understands; the user should not have to fill out a survey again. Select the items that materially support judgment and keep them concise.

- Application context: request, target character and scale, relevant facets, work and scope, and the guide or baseline used.
- Observation: what was useful, what explanation did not fit, and what actually happened.
- Response and limitations: what was adapted, whether it helped, and what remains unverified.
- Possible improvement: related documents, clarification that may help, and questions worth checking in other contexts.

No fixed form or score is required. Distinguish observed facts from guesses about cause and from proposals. When available, include the okf-lab commit or document consulted and the target OKF specification version so different baselines are not confused.

Generalize the draft to preserve only relationships and conditions needed for judgment. Do not copy company, customer, or personally identifying information, private-repository URLs, original documents, code, or logs directly. Apply the same standard to email. If generalization cannot preserve the meaning of the case, external submission can be skipped.

## How to send it

Public feedback should go to the repository whose guidance was used.

| Guidance used | Feedback destination |
| --- | --- |
| `okf-lab-kr` | [existing issues](https://github.com/muffinbox/okf-lab-kr/issues) · [new issue](https://github.com/muffinbox/okf-lab-kr/issues/new) |
| `okf-lab` | [existing issues](https://github.com/muffinbox/okf-lab/issues) · [new issue](https://github.com/muffinbox/okf-lab/issues/new) |

A problem shared by both repositories only needs to be reported once. If relevant discussion already exists, connect to that issue instead of submitting duplicate reports or asking the user to translate and submit the same content twice. Access to the private research repository `okf-lab-dev` is not required for submitting feedback.

Email for either repository can be sent to [muffinboxapps@gmail.com](mailto:muffinboxapps@gmail.com). It can be used when a public issue is unsuitable or GitHub submission is inconvenient. The agent can prepare the subject and body for the user to send from their usual email client.

Choose the route based on available tools and the user's preference. Do not judge submission capability only from whether GitHub CLI is installed; an authenticated tool or browser may also be available. Do not require installation of a new tool or a new login solely for feedback.

| Route | How to use it |
| --- | --- |
| GitHub Issue | When public sharing is appropriate and an authenticated write path is available, draft and submit a title and body. If a related issue already exists, connect to that discussion rather than opening a duplicate. |
| Email | Prepare a subject and body for the shared address above. If an email tool is connected and transmission has been requested, it may be used. |
| Skip transmission | If no convenient route exists, provide the draft only or omit feedback. Application work can still be completed. |

External transmission occurs only within the scope the user requested. General delegation to apply okf-lab does not by itself authorize sending an issue or email. Present the content and destination to be sent, and for a GitHub Issue make clear that it will be public. If the user has already delegated transmission of that content through that route, do not ask for the same intent again. After sending, report the issue link or actual send result; drafting alone is not a completed transmission.

## How received feedback is used

Ambiguity or errors raised in feedback are reviewed in the related documents. Cases without a conclusion can be connected to [notes](notes/README.md), and hypotheses needing validation to [experiments](experiments/README.md). A suggestion appearing in a public issue or email is not automatically adopted guidance; confirmed conclusions are reflected in the relevant OKF concepts, facets, and templates. When privately received material is moved into the repository, preserve its permitted sharing scope.

Keep public intake separate from storage of research cases. Detailed analysis and validation can remain in the research space, while public guidance reflects only shareable evidence and generalized conclusions. Translation or explanation problems specific to one repository can be reviewed there; improvements to shared principles or patterns should connect the necessary changes across published repositories. Public issues should link only to publishable outcomes and changed documents; receiving feedback does not create authority to disclose private source material.
