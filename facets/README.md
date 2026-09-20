# Facets

A facet is a lens for reading **one important aspect or property of a target**. Several facets may be relevant at once, and a facet is not a preset to apply or a repository-structure template.

The agent identifies relevant facets from the target's actual state and then uses linked OKF knowledge and the repository's existing conventions to judge structure and working practices autonomously. Matching a facet does not determine OKF suitability.

| Facet | Meaning |
| --- | --- |
| [Software project](software-project.md) | Environments where code and configuration are primary sources of truth for implementation facts |
| [Knowledge-centered](knowledge-centered.md) | Environments where knowledge itself is the primary output |
| [Large corpus](large-corpus.md) | Environments where scale or complexity makes full internalization impractical |
| [Personal context (preview)](personal-context.md) | An environment under study for treating a person's life, relationships, state, and preferences as long-lived context |

Do not create a new facet just to cover another possible case. A property that is easy to observe but adds no distinct judgment, or a problem already explained by general OKF knowledge, should not be re-owned by a facet. See [Role and boundaries of facets](../okf/facet-boundaries.md).

A `preview` facet is a research candidate that has not yet been adopted. It is not a prerequisite for default application and is consulted when exploring related experiments or cases.

Use one Markdown document as the default unit for a facet. Do not create a subdirectory until facet-specific material genuinely needs multiple files; first decide whether new material belongs in general OKF knowledge, a note, experiment, example, or elsewhere.

The source of truth for design judgment is the [OKF knowledge graph](../okf/index.md). Facets are thin lenses that make that knowledge easier to read in a particular environment.
