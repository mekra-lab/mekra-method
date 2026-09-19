# Application guide

This guide provides a default path for applying okf-lab's operational knowledge to a target repository. The operation categories, scope, and questions support the agent's judgment and can be omitted, combined, or adapted to the purpose and context. Carry forward the user's stated intent and delegated scope.

Start with the [operating principles](okf/operating-principles.md): keep responsibility for canonical facts clear, internalize the context each concept needs, and reflect the meaning of changes in related concepts. [Adoption judgment](okf/adoption.md) explains how this philosophy informs application work.

## Understand the target and choose a direction

Interpret natural-language requests such as "apply it," "build an OKF," or "bring this in line with the current okf-lab" together with the target's current state. The [README examples](README.md) illustrate possible wording; they are not an exact command syntax. [Adoption judgment](okf/adoption.md) explains the reasoning and operation categories.

Inspect the target's README, existing agent instructions, main materials or code, and existing OKF to understand its purpose, canonical locations, and current operation. Reuse valid structure and knowledge, and identify changes that would actually help. Explore related OKF concepts when necessary.

Use a [profile](profiles/README.md) as a starting point for the operating model. Determine whether the work involves initial construction, updating existing practices, a profile transition, or a specification upgrade, and choose the scope for this application. Even for a construction request, if an OKF already exists, first consider which knowledge to retain and what needs improvement. A request to "turn this repository into OKF" focuses on finding knowledge worth internalizing in the existing materials and expressing it as concepts and relationships. Combine operations when they overlap.

An inspection request focuses on assessing the current structure and knowledge and explaining findings and proposed improvements. Implement improvements if the user also requested changes or already delegated them in the preceding context. Do not automatically proceed from a diagnosis-only request to a structural transition.

Find adopted principles and patterns in `okf/`, application configurations in `profiles/`, and copyable scaffolding in `templates/`. Treat `notes/` and `experiments/` as research materials. For a specification upgrade, inspect the [version records](versions/README.md) and the formats actually used by the target bundle.

## Questions and delegation

Ask when user intent that cannot be inferred from inspection would materially change the result. Adapt examples such as these to the situation:

- "The structure depends on whether the current domain documents remain canonical or that responsibility moves into OKF. Are there locations that must be retained?"
- "I recommend progressively migrating the core knowledge first. Do you need a full review this time?"
- "I can proceed using the approach I recommend for this context, or we can decide the major choices together."

These questions do not need to be asked in sequence. Proceed autonomously when the answer is already known or the choice has little impact. Do not reconfirm the same choices after the user has delegated judgment. When a consequential decision depends on intent that is hard to infer, present the relevant context and a recommendation.

Questions and choices should use vocabulary, conceptual depth, explanation preferences, and decision style evident in the user's conversation and materials. Rather than assigning an arbitrary proficiency level, follow the terms and level of explanation the user already uses. Do not unnecessarily unpack technical terms the user already knows, and do not make users learn okf-lab's internal category names or implementation terminology just to answer. When presenting choices, explain what each one changes in actual operation and why one is recommended rather than relying on labels. When judgment has already been sufficiently delegated, proceed with the recommended approach instead of repeatedly asking about minor choices.

## Apply and verify

Reflect the chosen direction in structure and knowledge. [Templates](templates/README.md) are starting points to adapt where needed while preserving existing content. Merge the OKF operations section into the existing root `AGENTS.md`, keeping its scope distinct from development, execution, and deployment instructions.

Internalize new knowledge in the meaning, conditions, and relationships of related concepts. When canonical responsibility or the operating model changes, update affected concepts as well. Even during a full review, retain documents that do not need changes. For progressive migration, distinguish what has been completed from what remains.

Evaluate the result using the target's real questions and workflows rather than file counts or template conformity. Check whether core concepts can be understood, evidence can be traced, canonical boundaries and links are maintained, and the target format and existing instructions remain compatible. Explain remaining conflicts or constraints along with the completed scope.

## Operational handoff and completion

Construction and transition work extends through leaving enough operating guidance for the user to handle existing materials and new information. "Reflect the new materials in OKF" is a follow-up request within the adopted repository; do not present it as a command to select okf-lab's construction or transition process again.

Explain the actual locations and method chosen for adding materials. For example, when originals are preserved in `raw/`, say: "Put new originals in `raw/`, then ask the agent to reflect the new materials in OKF." Replace the path with the target's actual configuration.

Record where originals and directly authored knowledge belong, how external materials are referenced, and how to request internalization in the target README or the relevant material guide. If a separate source-material directory is unnecessary, explain how to use the existing location. Repository-specific choices that agents also need can be linked from the target's OKF operations instructions.

### Optional repository operating preferences

After construction or transition, consider whether repository-level operating preferences would help subsequent work. Do not mechanically list every option. Select only preferences that are genuinely useful for the target's materials and workflow, and describe them in terms the user can readily understand. If the user has already expressed the same preference or delegated its application, it can be recorded without asking again.

Examples of preferences that may be added to the target root `AGENTS.md` include:

- For document-like derivative deliverables, prefer first creating a human-readable and editable source such as Markdown, then deriving final formats such as PDF, DOCX, or PPTX. Do not force an intermediate Markdown file when the final format itself is canonical or the intermediate source has no practical value.
- After producing a report, analysis, design document, or other derivative, consider whether newly established concepts, rules, decisions, or relationships are worth reflecting in OKF. If incorporation is clear and within the delegated scope, update it together; when the decision depends on user intent, ask whether to incorporate it. Do not copy the entire deliverable into the knowledge base.
- When the user has not specified a method for a choice, prefer the agent's recommended option and ask only about unresolved intent that materially changes the result.
- At the end of a meaningful body of work, distinguish one-off notes from knowledge that will remain reusable. If durable knowledge emerged, consider whether it should be internalized in the relevant OKF concepts.
- Where traceability matters for derivative outputs, leave a path back to supporting source material, canonical sources, or related OKF concepts.

Do not present requirements already established by the [operating principles](okf/operating-principles.md), [source of truth and context](okf/source-of-truth.md), [context propagation](okf/context-propagation.md), or the selected profile as optional preferences that can be toggled according to taste. These choices supplement repository-wide follow-up work; they do not replace OKF principles.

For progressive migration, also record the remaining scope and how to migrate it when it is used or changed. This guidance is part of making continued migration possible. Make the target repository sufficient to resume work, and include major decisions, changes, verification results, and material intake instructions in the completion report. If only a diagnosis was performed, report the findings and recommended follow-up work.

When you discover conditions in which the guide was useful, hard-to-explain cases or conflicts, or reusable improvements, you may recommend [feedback](FEEDBACK.md) with a reason. Do not require a report for ordinary autonomous adaptations or uneventful applications. Follow the feedback guide for drafting and sending; complete application and handoff regardless of whether feedback is submitted.
