# Software project

A facet for environments where software code and configuration are primary sources of truth for implementation facts. It helps determine what knowledge is not expressed clearly enough by implementation alone.

## What matters from this perspective

- Do not make OKF independently own implementation details that code and configuration already express well enough.
- Purpose, boundaries, business rules, and design intent that cannot be understood reliably from implementation alone may be worth internalizing in OKF.
- Identify the roles that existing READMEs, ADRs, and operational documents play as sources of truth and practical guides. Where separate maintenance is useful, keep guidance in existing documentation locations such as `docs/`. In OKF, internalize the context needed to understand related concepts and make judgments, while keeping responsibility for changes to the source of truth clear.
- When code or configuration changes the meaning, conditions, or judgment criteria of a concept, reflect that impact in the related OKF knowledge.
- Judge file and directory placement from the repository's existing conventions and actual working practices.

## Judgment questions

- Is this information already expressed sufficiently in code, configuration, or existing documents as its source of truth? What additional context is needed in OKF to understand related concepts and make judgments?
- Do we need to explain purpose, constraints, business meaning, or design judgment rather than implementation facts?
- Does this implementation change alter the meaning of any OKF concept?
- What outcomes and execution scope do labels such as `ready`, success, or `dry-run` actually guarantee? Does the [meaning of the concept](../okf/knowledge-internalization.md#meaning-of-states-and-results) also cover exceptions to the default behavior or differences between callers?
- Is the knowledge read by a development agent, or is it also connected as input to AI within the product? What is the [scope in which actual use has been confirmed](../okf/adoption.md#connecting-knowledge-to-actual-use)?
- After work from a branch or worktree is integrated, can you still find [evidence paths](../okf/source-of-truth.md#paths-to-current-sources-of-truth-and-historical-evidence) that match the cited content and version?
- Would using an existing location and convention be more natural than creating a new directory or document?

Related knowledge: [source of truth and context](../okf/source-of-truth.md), [knowledge internalization](../okf/knowledge-internalization.md), [context propagation](../okf/context-propagation.md)
