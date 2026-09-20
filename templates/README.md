# Templates

These templates are examples of an operating approach built around [Open Knowledge Format](https://github.com/GoogleCloudPlatform/open-knowledge-format). The format follows the official specification, while structure and instructions are adapted to the purpose of each repository. See the [current version baseline](../versions/current.md) for the OKF version and specification point used here.

They are minimal starting points to copy into a real repository, remove what is unnecessary, and add repository-specific context.

All files under `templates/`, including this README, are provided under [CC0-1.0](LICENSE). Copying, adapting, or incorporating them does not require okf-lab attribution or retention of a license copy. Recording an adoption baseline is your choice. CC0 does not eliminate third-party rights or rights such as trademarks and patents.

- [`AGENTS.md.template`](AGENTS.md.template): sections for **OKF knowledge operation and optional repository-wide operating preferences** to merge into a root `AGENTS.md`
- [`okf/index.md`](okf/index.md): example OKF bundle root
- [`okf/concept.md`](okf/concept.md): minimal concept document

The `okf/` directory here holds an example bundle. A target can use a different name such as `knowledge/`, or use the repository root as its bundle. Copy the files inside `okf/` into the chosen bundle location and adapt instructions and links accordingly; the enclosing `okf/` folder need not be copied as-is. See [adoption judgment](../okf/adoption.md#bundle-location-and-existing-structure) for the reasoning behind location choices.

When using `AGENTS.md.template`, merge each needed section into the context of the existing root `AGENTS.md`. It is not a replacement for repository-wide instructions. The autonomy principle in the `OKF knowledge operation` section applies to OKF knowledge work. If the `Repository operating preferences` section is selected, keep it as a peer section whose scope covers the repository-wide follow-up work it describes.

Keeping the template unchanged is not the goal. Use the target's actual material, relevant [facets](../facets/README.md), and OKF knowledge to keep only the structure that is useful.

When updating an existing OKF, do not overwrite it with template files. Preserve existing knowledge and repository-specific instructions while merging valid improvements. Use [adoption judgment](../okf/adoption.md) to set the scope of the current work and the [application guide](../APPLICATION.md) to leave the location and incorporation method for future material in the target repository. Put user-facing guidance in the target README or another suitable place, and link agent-relevant repository-specific choices from the OKF operating section when useful.
