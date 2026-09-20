# Application guide

This guide is the default path for applying okf-lab operating knowledge to a target repository. Work categories, scope, and suggested questions exist to support agent judgment and may be omitted, combined, or adapted according to purpose and context. Carry forward intent and delegated authority already established by the user.

The philosophical starting point is the [operating principles](okf/operating-principles.md): keep responsibility for sources of truth clear, internalize the context each concept needs, and reflect the meaning of changes into related concepts. [Adoption judgment](okf/adoption.md) explains how that philosophy carries into application work.

## Understand the target and choose the application direction

Interpret natural-language requests such as "apply this," "build an OKF," or "bring this up to current okf-lab" together with the target's current state. The [README examples](README.md) are possible wording, not a command grammar that must be matched exactly. The reasoning behind request interpretation and work categories is in [adoption judgment](okf/adoption.md).

Inspect the target's README, existing agent instructions, important material or code, and any existing OKF to understand its purpose, locations of sources of truth, and current operating model. Reuse valid structures and knowledge, and judge which changes would actually help. Explore additional OKF concepts when useful.

Use [facets](facets/README.md) as supporting lenses for understanding important dimensions of the application context, such as the target, primary outputs, or material characteristics. Do not choose a facet and apply it wholesale; identify relevant properties in the target and consult only what helps. A `preview` facet is a research candidate still under validation, so it is not a prerequisite for normal application. Determine whether the work is a new build, an update to existing operating practices, a change driven by target characteristics, a specification-version transition, or some combination, then set the scope for this application. Even for a build request, if an existing OKF is present, first judge what knowledge to preserve and what needs improvement. A request to "turn this repo into OKF" focuses on finding knowledge worth reusing in current material and [internalizing](okf/knowledge-internalization.md) it as actual concepts and relationships.

An inspection request focuses on diagnosing whether the current structure and knowledge are suitable and explaining findings and improvements. If the user also requested fixes, or prior context already delegated them, implement the necessary improvements as well. If the request is diagnosis only, do not automatically proceed into structural migration.

In this guide repository, adopted principles and patterns live under `okf/`, lenses for reading application context under `facets/`, and copyable scaffolding under `templates/`. `notes/` and `experiments/` are research material. If a specification-version transition is relevant, inspect the [version records](versions/README.md) and the format actually used by the target bundle.

## Ask only for intent that matters

Ask when unresolved user intent that cannot be learned from exploration would materially change the result. The following are examples to adapt to the situation:

- "The structure changes depending on whether the existing domain document remains the source of truth or that responsibility moves into OKF. Is there a location that must remain canonical?"
- "I recommend migrating the core knowledge first and converting the rest progressively. Do you need the whole repository reviewed this time?"
- "I can proceed with the recommended approach for this context, or we can decide the major choices together."

These questions do not need to be asked in order. If the answer is already known or the choice has little impact, proceed autonomously. Do not ask again about a choice the user has already delegated. For consequential choices whose intent is genuinely unclear, provide the relevant context and a recommended option with the question.

Phrase questions and options using the vocabulary, conceptual familiarity, explanation preference, and decision style visible in the conversation and material the user has provided. Do not assign the user an arbitrary skill level; use terminology and explanation depth they already demonstrate. Keep familiar technical terms when useful, and do not require the user to learn okf-lab's internal category names or implementation vocabulary just to answer. Explain what an option changes in actual operation and why it is recommended. When sufficient autonomy is already delegated, prefer making minor choices through the recommended approach and explaining them afterward rather than repeatedly asking.

## Implement and verify

Reflect the chosen direction in structure and knowledge. [Templates](templates/README.md) are starting points that should be adapted while preserving existing content. Merge the OKF operating section into an existing root `AGENTS.md` and keep its scope distinct from development, execution, and deployment instructions for the target.

Choose the target's [bundle location](okf/adoption.md#bundle-location-and-existing-structure) to fit its purpose and existing structure. The name `okf/` is not required; another directory or the repository root may be used. Adjust paths in template files and instructions to the location actually chosen.

Internalize new knowledge into the meaning, conditions, and relationships of relevant concepts. When a source of truth or operating model changes, update concepts whose meaning is affected. Even during a full review, leave documents unchanged when no change is needed. In a progressive transition, distinguish what was converted now from what remains for later.

Verify the result against the target's real questions and operating practices rather than file counts or template conformity. Check whether core concepts can be understood and supporting evidence can be traced, whether source-of-truth boundaries and links remain coherent, and whether the target specification version coexists with existing instructions. Explain remaining conflicts or constraints together with the completed scope.

Distinguish what format and link checks establish from semantic review. The burden of rereading source material, missed effects of changes, and maintenance costs found in real use can be examined as [operational observations](okf/feedback.md) to help adjust the depth and organization of explanations.

## Operational handoff and completion

Build and transition work continues through leaving the user a usable operating method for handling existing and new material afterward. "Incorporate the new material into OKF" is an example of a follow-up request used inside an already adopted repository; do not present it as a command for choosing okf-lab's build or transition procedure again.

Explain the actual location and method selected for adding the next material. For example, if source material is intentionally kept in `raw/`, the handoff might say: "Put new source material in `raw/` and ask the agent to incorporate the new material into OKF." Replace the path with the target's actual arrangement.

Leave guidance in the target README or the relevant material documentation about where source material and directly authored new knowledge belong, how external material should be referenced, and what request should be used to incorporate it. If there is no benefit in a separate source-material folder, explain how the existing location should be used instead. Repository-specific choices the agent also needs can be linked from the target's OKF operating instructions.

To make later comparisons between changes in the guide and experience in use possible, it helps to briefly record the actual reference repository and commit, when verifiable, in existing guidance or adoption records. Distinguish [lab releases from the OKF specification baseline](versions/README.md), and note the scope if only part of the knowledge was updated. This does not require a separate record file or metadata on every concept.

### Optional operating preferences

After a build or transition, judge whether repository-level operating preferences would improve later work. Do not mechanically list every possible preference; select only those with real value for the target's material and workflow, and express them in terms the user can understand. If the user already stated the same preference or delegated the choice, it may be applied without asking again.

Examples that may be worth adding to the target's root `AGENTS.md` include:

- For document-like derived outputs, prefer creating a human-readable, editable source such as Markdown before deriving PDF, DOCX, PPTX, or similar final formats when that intermediate source is useful. Do not force it when the final format is itself canonical or the Markdown layer adds no value.
- After producing a report, analysis, design document, or similar output, check whether newly established concepts, rules, judgments, or relationships are worth reflecting into OKF. Update them when the case is clear and within delegated scope; ask when it depends on user intent. Do not copy the entire output into knowledge.
- When the user has not specified a method for a choice, prefer the recommended option and ask only about unresolved intent that materially changes the outcome.
- After substantial work, distinguish one-off notes from knowledge with durable reuse value and consider internalizing the latter into relevant OKF concepts.
- In repositories where provenance of derived outputs matters, preserve a path back to source material, sources of truth, or related OKF concepts.

Do not present requirements already established by general OKF knowledge—such as [operating principles](okf/operating-principles.md), [source of truth and context](okf/source-of-truth.md), or [context propagation](okf/context-propagation.md)—as user preferences that can simply be toggled on or off. Facets do not re-own those principles; they only connect environments to judgments that become especially important.

If a progressive transition was chosen, also leave the remaining scope and the conditions under which later use or changes should continue the transition. This is part of making the transition resumable. The target repository alone should be enough to continue later work. A completion report should cover the main judgments and changes, verification results, and how to add the next material. If the work was diagnosis only, report findings and recommended follow-up instead.

When the application reveals conditions where the guide was especially useful, difficult cases or conflicts, or a reusable improvement, you may recommend [feedback](FEEDBACK.md) and explain why. Do not require reports for routine autonomous adaptation or ordinary successful use. Drafting and transmission follow the feedback guide, and application plus operational handoff should still be completed regardless of whether feedback is sent.
