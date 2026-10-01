# Application guide

This guide is the starting point for applying Mekra Method to a real target. It covers the flow from exploring the target through implementation, verification, and operational handoff, linking to the sources of truth for the judgments involved. Work categories, scope, and suggested questions support agent judgment and may be omitted, combined, or adapted according to purpose and context. Carry forward intent and delegated authority already established by the user.

The [operating principles](PRINCIPLES.md) explain the core principles and their relationships; [adoption judgment](okf/adoption.md) provides detailed reasoning and boundaries for scope, structure, delegation, and connection to actual use. [Facets](facets/README.md) help locate relevant judgments from properties of the target. Consult the [operating knowledge](okf/index.md) and [templates](templates/README.md) as needed. This guide does not separately define the reasoning owned by those documents.

## Confirm the adoption baseline

The default entry point is `releases/latest` in the public repository being consulted. At the start, verify the formal release's tag and the public repository commit it points to, then read `APPLICATION.md` and related documents pinned to that commit. If the release notes specify an adoption commit, check that it matches the tag's target. The `source_commit` in `SYNC.json` traces the dev source reviewed for publication; the actual adoption baseline is the commit of the public repository being read. Keep that baseline even if public `main` contains later explanatory improvements. On completion, record the public repository, release, and commit actually consulted. If the user specified a tag, commit, or dev working tree, keep that baseline. If the release baseline cannot be verified, report the limit instead of treating `main` as the latest formal release.

## Understand the target and choose the application direction

Interpret natural-language requests such as "apply Mekra," "incorporate new material into the existing Mekra," or "update this Mekra to the latest formal release" together with the target's current state. The [README examples](README.md) are possible wording, not a command grammar that must be matched exactly. The reasoning behind request interpretation and work categories is in [adoption judgment](okf/adoption.md).

Inspect the target's README, existing agent instructions, important material or code, and existing knowledge to understand its purpose, locations of sources of truth, and current operating model. Reuse valid structures and knowledge, and judge which changes would actually help. Explore relevant Method operating knowledge when useful.

Use [facets](facets/README.md) as supporting lenses for understanding important dimensions of the application context, such as the target, primary outputs, or material characteristics. Do not choose a facet and apply it wholesale; identify relevant properties in the target and consult only what helps. A `preview` facet is a research candidate still under validation, so it is not a prerequisite for normal application. Determine whether the work is a new build, an update to existing operating practices, a change driven by target characteristics, a specification-version transition, or some combination, then set the scope for this application. Even for an initial application request, if Mekra or OKF knowledge is already present, first judge what to preserve and what needs improvement. A request to incorporate new material focuses on finding knowledge worth retaining and [internalizing](okf/knowledge-internalization.md) it in the relevant concepts and relationships. When these kinds of work overlap, they can be handled together.

An inspection request focuses on diagnosing whether the current structure and knowledge are suitable and explaining findings and improvements. If the user also requested fixes, or prior context already delegated them, implement the necessary improvements as well. If the request is diagnosis only, do not automatically proceed into structural migration.

The entry point to this guide's principles is `PRINCIPLES.md`; `okf/` holds the adopted detailed operating knowledge, currently expressed in OKF. Distinguish the directory's representation format from the scope in which its reasoning applies. `notes/` and `experiments/` are research material, and unadopted content is not a default basis for application. If a specification-version transition is relevant, inspect the [version records](versions/README.md) and the format actually used by the target bundle.

## Existing OKF material and specification changes

For "apply Mekra Method to existing OKF material," preserve valid knowledge and sources of truth while assessing changes to operating practices. Earlier requests such as "build an OKF" or "turn this repo into OKF" can also be interpreted from their purpose and the target's state; they do not automatically require rebuilding. An explicit request to update the OKF specification is a format transition, distinct from updating the Method baseline. See the [version guide](versions/README.md) for the specification baseline and migration considerations.

## Ask only for intent that matters

Ask when unresolved user intent that cannot be learned from exploration would materially change the result, explaining the practical difference and the recommended option. Carry forward established intent and delegation without asking about the same choice again. See [user intent and delegated autonomy](okf/adoption.md#user-intent-and-delegated-autonomy) for the scope, wording, and examples of questions.

## Implement and verify

Reflect the chosen direction in structure and knowledge. Preserve existing content and target-specific instructions when choosing the [bundle location](okf/adoption.md#bundle-location-and-existing-structure) and [knowledge operating entry point](okf/adoption.md#knowledge-operating-entry-point). Adapt the [templates](templates/README.md) as needed, and verify links for the actual location and the format of documents inside the bundle. Keep the scope of knowledge operating guidance distinct from development, execution, and deployment instructions for the target.

Identify the [role of new material and which conclusions have been adopted](okf/external-sources.md#roles-and-valid-scope-of-materials), then internalize that knowledge in the meaning, conditions, and relationships of relevant concepts. When a source of truth or operating model changes, update concepts whose meaning is affected. Even during a full review, leave documents unchanged when no change is needed. In a progressive transition, distinguish what was converted now from what remains for later.

Verify the result against the target's real questions and operating practices rather than file counts or template conformity. Check whether core concepts can be understood and supporting evidence can be traced, whether source-of-truth boundaries and links remain coherent, and whether the target specification version coexists with existing instructions. Explain remaining conflicts or constraints together with the completed scope.

Also check that the entry point and relevant evidence can actually be found in the environment where this knowledge will be used. If it serves different readers, such as development agents and AI within a product, distinguish [how each is connected to the knowledge](okf/adoption.md#connecting-knowledge-to-actual-use).

Distinguish what format and link checks establish from semantic review. The burden of rereading source material, missed effects of changes, and maintenance costs found in real use can be examined as [operational observations](okf/feedback.md) to help adjust the depth and organization of explanations.

## Operational handoff and completion

Build and transition work continues through leaving the user a usable operating method for handling existing and new material afterward. "Incorporate new material into the existing Mekra" is an example of a follow-up request used inside an already adopted repository; do not present it as a command for choosing Mekra Method's build or transition procedure again.

Having one adoption entry point does not mean that every knowledge lookup or routine material update must pass through this guide. After adoption, continue from the target's own entry points and operating knowledge, returning to this guide and relevant reasoning when its operating system needs reassessment.

Explain the actual location and method selected for adding the next material. For example, if source material is intentionally kept in `raw/`, the handoff might say: "Put new source material in `raw/` and ask the agent to incorporate the new material into the existing Mekra." Replace the path with the target's actual arrangement.

Explain the [division of responsibility](okf/context-propagation.md#human-and-agent-roles): people supply new facts, intent, evidence, and corrections, while the agent explores related context and updates the source of truth and affected knowledge together. For example: "This condition has changed; check the evidence and update the related knowledge." After a person edits knowledge directly, they can ask: "Review the meaning and impact of this change and update related knowledge too."

Leave guidance in the target README or the relevant material documentation about where source material and directly authored new knowledge belong, how external material should be referenced, and what request should be used to incorporate it. If there is no benefit in a separate source-material folder, explain how the existing location should be used instead. Repository-specific choices the agent also needs can be linked from the target's Mekra operating instructions.

Also explain where use was confirmed and whether updates happen at the user's request or through automation that has actually been connected. Specify where the knowledge is stored and which entry point to use next. Distinguish the verified scope of completion from connections in other environments or automation that has not been implemented.

To make later comparisons between changes in the guide and experience in use possible, it helps to briefly record the actual reference repository and commit, when verifiable, in existing guidance or adoption records. Distinguish [Mekra Method releases from the OKF specification baseline](versions/README.md), and note the scope if only part of the knowledge was updated. This does not require a separate record file or metadata on every concept.

### Optional operating preferences

Where repository-level preferences would help later work, consult the [selection criteria and exceptions](okf/adoption.md#optional-operating-preferences) and persist only what has been agreed or delegated. The [AGENTS template](templates/AGENTS.md.template) provides an example section to copy. Do not re-ask Method operating principles as optional features or add them as duplicate rules.

If a progressive transition was chosen, also leave the remaining scope and the conditions under which later use or changes should continue the transition. This is part of making the transition resumable. The target repository alone should be enough to continue later work. A completion report should cover the main judgments and changes, verification results, and how to add the next material. If the work was diagnosis only, report findings and recommended follow-up instead.

When the application reveals conditions where the guide was especially useful, difficult cases or conflicts, or a reusable improvement, you may recommend [feedback](FEEDBACK.md) and explain why. Do not require reports for routine autonomous adaptation or ordinary successful use. Drafting and transmission follow the feedback guide, and application plus operational handoff should still be completed regardless of whether feedback is sent.
