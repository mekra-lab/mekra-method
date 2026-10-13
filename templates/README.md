# Templates

These templates illustrate Mekra Method operating practices and use [Open Knowledge Format](https://github.com/GoogleCloudPlatform/open-knowledge-format) to represent knowledge. The format follows the official specification, while structure and instructions are adapted to the purpose of each repository. See the [current version baseline](../versions/current.md) for the OKF version and specification point used here.

The templates are examples to support application. Use or adapt the parts that help; in particular, design concept document types, properties, and body structure to suit the target's material and intended use.

Use the [application guide](../APPLICATION.md) to examine the target and scope when judging which templates are useful. The Method's [operating principles](../PRINCIPLES.md) and detailed concepts provide reasoning; they do not require copying those documents or the guide repository's layout into the target.

All files under `templates/`, including this README, are provided under [CC0-1.0](LICENSE). Copying, adapting, or incorporating them does not require Mekra Method attribution or retention of a license copy. Recording an adoption baseline is your choice. CC0 does not eliminate third-party rights or rights such as trademarks and patents.

- [`AGENTS.md.template`](AGENTS.md.template): a **link to the MEKRA entry point and an optional section for repository operating preferences** to merge into a root `AGENTS.md`
- [`mekra/MEKRA.md`](mekra/MEKRA.md): the common entry point describing an individual Mekra's purpose, scope, discovery paths, reference baselines, and operating context
- [`MEKRAS.md.template`](MEKRAS.md.template): an example discovery index for an environment using multiple Mekras
- [`mekra/index.md`](mekra/index.md): example OKF bundle root using the default directory name
- [`mekra/concept.md`](mekra/concept.md): minimal concept document

`concept.md` remains a minimal example, with guidance on choosing properties suited to the target and defining custom properties where needed. The fields shown in the example do not represent the full range available. The current version baseline linked above provides the specification reference and the baseline used by this repository.

When a new file-based Mekra needs its own directory, use `mekra/` as the default location. The `mekra/` directory here is an example OKF bundle using that default. Preserve an existing canonical location or use a structure better suited to the target, including a name such as `knowledge/` or the repository root. Copy the files inside `mekra/` into the chosen bundle location and adapt instructions and links accordingly. See [adoption judgment](../okf/structure-and-discovery.md#bundle-location-and-existing-structure) for the reasoning behind location choices.

## Choosing an entry point arrangement

Align each Mekra's entry point with the environment's discovery path. The roles of `MEKRA.md` and `MEKRAS.md` are Mekra operating practices, not required-file rules in the official OKF specification. See [knowledge operating entry points](../okf/structure-and-discovery.md#knowledge-operating-entry-point) and the [discovery index for multiple Mekras](../okf/structure-and-discovery.md#discovery-index-for-multiple-mekras) for the reasoning.

- **A separate Mekra within a repository:** Copy the example files from `mekra/` to the target's `mekra/` or chosen location. Keep `MEKRA.md` with that Mekra, and merge the needed sections of `AGENTS.md.template` into the existing AGENTS to link it.
- **The whole repository as one Mekra:** Place `MEKRA.md` at the repository root and link directly from AGENTS. Adapt MEKRA's knowledge navigation links to the actual `index.md`, `okf/index.md`, or other location. The knowledge need not all move into the same directory.
- **An environment using multiple Mekras:** Copy `MEKRAS.md.template` to `MEKRAS.md` in an accessible location such as the environment root, and populate it with actual Mekra names, brief descriptions, and entry point links. Change the first sentence of AGENTS to direct readers through the index to relevant Mekras. For a single Mekra, link directly to MEKRA.

The default example connects `AGENTS.md → mekra/MEKRA.md → index.md`. With multiple Mekras, use `AGENTS.md → MEKRAS.md → the relevant MEKRA.md`. Update related entry points and index links whenever structure changes.

A `MEKRA.md` inside a bundle follows the concept document format. The supplied example already includes the following frontmatter; `Playbook` is a type choice for operating guidance. Moving the entry point outside an OKF bundle does not impose the same format requirement on its new location.

```yaml
---
type: Playbook
---
```

When the whole repository is used as an OKF bundle, the concept document format also applies to other operational Markdown files included in that bundle, such as `AGENTS.md` or `MEKRAS.md`.

If knowledge operation started as a section in an existing AGENTS, move its valid explanations to `MEKRA.md`, leaving the link and repository-wide operating instructions in AGENTS. Before creating a duplicate entry point, check the purpose, scope, and location of any existing one. If concepts already contain the operating principles, link to them from the entry point and shorten the template's general explanations. When recording an adoption baseline, follow [the actual reference baseline guidance](../versions/README.md#recording-the-actual-reference-baseline). Do not prefill the templates with unverified release numbers.

The autonomy guidance in these templates applies to authoring and updating knowledge and reflecting related changes in it. Keep the optional `Repository operating preferences` section at the same heading level as `Knowledge operation`, so it covers the later repository-wide work it describes. After application, check the links from the actual entry instructions to the knowledge bundle.

Keeping the template unchanged is not the goal. Use the target's actual material, relevant [facets](../facets/README.md), and OKF knowledge to keep only the structure that is useful.

When updating an existing OKF, do not overwrite it with template files. Preserve existing knowledge and repository-specific instructions while merging valid improvements. Use [adoption judgment](../okf/adoption.md) to set the scope of the current work and the [application guide](../APPLICATION.md) to leave the location and incorporation method for future material in the target repository. Put user-facing guidance in the target README or another suitable place, and link repository-specific choices that agents also need from the chosen knowledge operating entry point.
