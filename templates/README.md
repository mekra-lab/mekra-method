# Templates

These templates are local operating examples for using [Open Knowledge Format](https://github.com/GoogleCloudPlatform/open-knowledge-format). The format follows the official specification, while structure and instructions should be adapted to each repository's purpose. See the [current version baseline](../versions/current.md) for the target version and specification reference point.

These are minimal templates intended to be copied into a real repository, stripped of unnecessary parts, and supplemented with repository-specific context.

- [`AGENTS.md.template`](AGENTS.md.template): an **OKF knowledge operations section** to incorporate into a root `AGENTS.md`
- [`okf/index.md`](okf/index.md): example OKF bundle root
- [`okf/concept.md`](okf/concept.md): minimal concept-document example

In actual use, merge the contents of `AGENTS.md.template` into the existing root `AGENTS.md` as one section. It is not a replacement for repository-wide instructions. Because changes outside OKF may still require knowledge updates, the guidance belongs at the root; the autonomy principle in this section applies specifically to OKF knowledge operations.

The goal is not to preserve the templates unchanged. Choose a profile, inspect the actual materials, and keep only the structure that is needed.

When updating an existing OKF, merge useful improvements while preserving its knowledge and local instructions instead of overwriting it with template files. Choose the current scope using [adoption judgment](../okf/adoption.md), and follow the [application guide](../APPLICATION.md) to leave future intake locations and incorporation methods in the target repository. Put user-facing guidance in the target README or similar locations, and link agent-relevant choices from the OKF operations section.
