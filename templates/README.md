# Templates

These templates are examples of an operating approach built around [Open Knowledge Format](https://github.com/GoogleCloudPlatform/open-knowledge-format). The format follows the official specification, while structure and instructions are adapted to the purpose of each repository. See the [current version baseline](../versions/current.md) for the OKF version and specification point used here.

They are minimal starting points to copy into a real repository, remove what is unnecessary, and add repository-specific context.

All files under `templates/`, including this README, are provided under [CC0-1.0](LICENSE). Copying, adapting, or incorporating them does not require Mekra Method attribution or retention of a license copy. Recording an adoption baseline is your choice. CC0 does not eliminate third-party rights or rights such as trademarks and patents.

- [`AGENTS.md.template`](AGENTS.md.template): a **link to the MEKRA entry point and an optional section for repository operating preferences** to merge into a root `AGENTS.md`
- [`MEKRA.md.template`](MEKRA.md.template): an optional entry point describing the purpose and scope of the knowledge, where to start, reference baselines, and operating context
- [`okf/index.md`](okf/index.md): example OKF bundle root
- [`okf/concept.md`](okf/concept.md): minimal concept document

`concept.md` remains a minimal example, with a short authoring hint that features from the OKF specification in use can be selected when needed. The fields shown in the example do not represent the full range available. The current version baseline linked above provides the specification reference and the baseline used by this repository.

The `okf/` directory here holds an example bundle. A target can use a different name such as `knowledge/`, or use the repository root as its bundle. Copy the files inside `okf/` into the chosen bundle location and adapt instructions and links accordingly; the enclosing `okf/` folder need not be copied as-is. See [adoption judgment](../okf/adoption.md#bundle-location-and-existing-structure) for the reasoning behind location choices.

## Choosing an entry point arrangement

Choose one of the two arrangements to fit the target. `MEKRA.md` is an optional Mekra Method operating example, not a required file in the official OKF specification. The reasoning is in [knowledge operating entry points](../okf/adoption.md#knowledge-operating-entry-point).

- **Separate files:** In the default example, copy `MEKRA.md.template` to `MEKRA.md` at the repository root and merge the needed sections of `AGENTS.md.template` into the existing root `AGENTS.md`. Keep the purpose and scope of the knowledge and its operating context in `MEKRA.md`, with AGENTS directing readers to it.
- **AGENTS only:** Merge the needed content from `MEKRA.md.template` into the `OKF knowledge operation` section of the existing `AGENTS.md`. Omit the `# Mekra` heading and adjust the levels of the remaining headings. Omit the AGENTS template's first sentence, which directs readers to `MEKRA.md`, while preserving the rest of its scope explanation. Do not create a separate `MEKRA.md` file.

If the bundle and its operating context are copied or distributed independently, `MEKRA.md` can be placed at the bundle root. For example, if it is at `knowledge/MEKRA.md`, change the link in AGENTS to `knowledge/MEKRA.md` and the knowledge navigation link in MEKRA to `index.md`. If the repository itself is the bundle, the two roots coincide. A `MEKRA.md` inside the bundle must follow the format for concept documents, so add the following frontmatter at the beginning. `Playbook` is an example type for operating guidance. See [knowledge operating entry points](../okf/adoption.md#knowledge-operating-entry-point) for the location and format rationale.

```yaml
---
type: Playbook
---
```

When the whole repository is used as a bundle, this format rule also applies to other operational Markdown files included in that bundle, such as `AGENTS.md`.

Preserve existing repository instructions and specific choices, and maintain operating explanations in one place when moving them. If concepts already contain the operating principles, link to them from the entry point and shorten the template's general explanations. When recording an adoption baseline, follow [the actual reference baseline guidance](../versions/README.md#recording-the-actual-reference-baseline). Do not prefill the templates with unverified release numbers.

The autonomy principle for knowledge operation applies to OKF knowledge work. Keep the optional `Repository operating preferences` section at the same heading level as `OKF knowledge operation`, so it covers the later repository-wide work it describes. After application, check the links from the actual entry instructions to the knowledge bundle.

Keeping the template unchanged is not the goal. Use the target's actual material, relevant [facets](../facets/README.md), and OKF knowledge to keep only the structure that is useful.

When updating an existing OKF, do not overwrite it with template files. Preserve existing knowledge and repository-specific instructions while merging valid improvements. Use [adoption judgment](../okf/adoption.md) to set the scope of the current work and the [application guide](../APPLICATION.md) to leave the location and incorporation method for future material in the target repository. Put user-facing guidance in the target README or another suitable place, and link repository-specific choices that agents also need from the chosen knowledge operating entry point.
