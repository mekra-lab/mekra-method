# Software project

A facet for environments where software code and configuration are primary sources of truth for implementation facts. It helps determine what knowledge is not expressed clearly enough by implementation alone.

## What matters from this perspective

- Do not make OKF independently own implementation details that code and configuration already express well enough.
- Purpose, boundaries, business rules, and design intent that cannot be understood reliably from implementation alone may be worth internalizing in OKF.
- When code or configuration changes the meaning, conditions, or judgment criteria of a concept, reflect that impact in the related OKF knowledge.
- Judge file and directory placement from the repository's existing conventions and actual working practices.

## Judgment questions

- Is the information being recorded already represented sufficiently by code or configuration as its source of truth?
- Do we need to explain purpose, constraints, business meaning, or design judgment rather than implementation facts?
- Does this implementation change alter the meaning of any OKF concept?
- Would using an existing location and convention be more natural than creating a new directory or document?

Related knowledge: [source of truth and context](../okf/source-of-truth.md), [knowledge internalization](../okf/knowledge-internalization.md), [context propagation](../okf/context-propagation.md)
