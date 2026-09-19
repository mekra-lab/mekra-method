# Project repository

Use this profile when code is central to the product and OKF supports the project's meaning, rules, and relationships.

## Recommended starting point

```text
repo/
├─ src/
├─ okf/
├─ docs/
├─ README.md
└─ AGENTS.md
```

## Key choices

- Put the project's purpose, concepts, boundaries, business rules, and relationships in `okf/`.
- Code and configuration are the source of truth for actual implementation; put run instructions, design, and verification processes in `docs/`.
- When a code change alters the meaning of knowledge or its decision criteria, update the related OKF concepts as well.
- Make sure cloning the project alone is enough to understand the minimum operating principles it needs. okf-lab is reference material, not a required runtime dependency.

For starting instructions, adapt [`templates/AGENTS.md.template`](../../templates/AGENTS.md.template) and merge it as a section into the existing root `AGENTS.md`.

Explain how to add code, configuration, and documents in the project's existing locations and reflect changes to meaning or business rules in related OKF concepts. Define a separate source-material intake location only when preservation requires one. Leave actual usage guidance in the target README or related task documentation.
