# Feedback guide

Experience from adoption can help improve okf-lab's guides and patterns. Feedback is optional: application and operational handoff can be complete without submitting it. See [learning from adoption feedback](okf/feedback.md) for the reasoning.

## When to recommend feedback

Consider how useful and suitable the guide was, and briefly recommend feedback when a discovery could help other applications. Examples include cases existing profiles cannot explain, conflicting principles or unclear boundaries, repeated template conflicts, problems with the default scope, and simpler or more effective methods. Explaining what helped and under which conditions can also support improvements.

Autonomous adaptation alone does not require a report. Keeping an existing `sources/` directory or reviewing a small repository all at once are already supported choices. Even a substantial adaptation may have little reporting value if the current guide explains it well; a small recurring ambiguity may be worth reporting. Skip feedback requests and "nothing unusual" reports for ordinary applications.

An operational handoff might include:

> In this application, two canonical sources were valid under different conditions, and the existing guidance did not make the decision clear. Feedback could help improve the guide. If you want, I can prepare a draft containing information suitable for sharing.

## What to include

The agent drafts from context it already understands; the user should not have to fill out another survey. Select the information that helps judgment and explain it briefly:

- Application context: the request, target purpose and scale, chosen profile, operation and scope, and the guidance or baseline used.
- Observations: what helped, which explanation did not fit, and what actually happened.
- Response and limitations: how the approach was adapted, its effect, and what remains unverified.
- Potential improvements: relevant documents, explanations to improve, and questions worth examining in other settings.

No fixed form or score is required. Distinguish observations from hypotheses about causes and from proposals. When available, identify the okf-lab commit or document used and the target OKF specification version so different baselines are not confused.

Generalize the draft to preserve only the relationships and conditions needed for judgment. Do not copy identifying company, customer, or personal information, private repository URLs, original documents, code, or logs verbatim. Apply the same standard to email. If generalization cannot preserve the meaning of the case, public submission can be skipped.

## How to send it

Submit public feedback to the repository of the edition you used.

| Edition used | Feedback destination |
| --- | --- |
| Korean edition, `okf-lab-kr` | [Existing issues](https://github.com/muffinbox/okf-lab-kr/issues) · [Create an issue](https://github.com/muffinbox/okf-lab-kr/issues/new) |
| Global English edition, `okf-lab` | [Existing issues](https://github.com/muffinbox/okf-lab/issues) · [Create an issue](https://github.com/muffinbox/okf-lab/issues/new) |

Issues shared by both editions need only be reported once. Connect to an existing discussion where appropriate; do not require duplicate submissions or translations for the other edition. Feedback does not require access to the research repository, `okf-lab-dev`.

Both editions accept email at [muffinboxapps@gmail.com](mailto:muffinboxapps@gmail.com). Use email when a public issue is unsuitable or GitHub submission is inconvenient. The agent can prepare a subject and body for the user to send from their usual email application.

Choose a route based on available tools and user preference at submission time. GitHub CLI installation alone does not determine whether submission is possible; consider authenticated tools or a browser as well. Do not require new tools or a new login just to provide feedback.

| Route | How to use it |
| --- | --- |
| GitHub Issue | If public sharing is appropriate and an authenticated writing tool is available, prepare a title and body and submit them. Connect to an existing related issue instead of duplicating it. |
| Email | Prepare a subject and body for the shared address above. A connected email tool can also be used when the user requests sending. |
| Skip submission | If no route is available or submission is burdensome, provide only a draft or skip feedback. Application can still be completed. |

Send externally only within the user's request. Delegation to apply the guide autonomously does not by itself authorize sending issues or email. Present the content and destination, explaining that a GitHub Issue is public. If the user already delegated sending that content through that route, do not reconfirm the same intent. After sending, provide the issue link or actual delivery result; do not report a draft as submitted.

## Using received feedback

Review reported ambiguity or errors in the relevant documents. Connect unresolved cases to [notes](notes/README.md) and hypotheses requiring validation to [experiments](experiments/README.md). A proposal in an issue or email is not automatically adopted guidance. Reflect confirmed conclusions in related OKF concepts, profiles, and templates. Respect the permitted sharing scope when moving privately received information into a repository.

Separate public intake from preservation of research cases. Analyze and validate detailed cases in the research space, and reflect shareable evidence and generalized conclusions in public distribution documents. Review translation or edition-specific wording in that edition, and connect improvements to common principles or patterns to the changes needed in both editions. Link public outcomes and changed documents back to the issue. Receiving feedback does not itself grant permission to publish private source material.
