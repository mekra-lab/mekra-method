---
type: Pattern
title: Role and boundaries of facets
description: Use facets as thin lenses for reading target properties rather than presets or a duplicate knowledge layer
---

# Role and boundaries of facets

## Problem

Precomposed guides for particular use cases can behave like presets that cause an agent to choose structure and behavior before understanding the target. At the opposite extreme, turning every property of a target into a classification field lets taxonomy and metadata grow faster than the knowledge itself.

## Choice

A facet is a **descriptive lens** for reading one important aspect or property of a target. Facets do not form one mutually exclusive type system, and several facets may be relevant at the same time.

A facet does not preselect directory layout, file placement, work sequence, or implementation structure. The actual arrangement is determined through [autonomous judgment](agent-autonomy.md) from the target's current state, existing conventions, relevant OKF knowledge, and the user's purpose.

The role of a facet is not to redefine general OKF knowledge, but to connect a particular environment with the knowledge and judgment questions that become especially important there.

## Creating and maintaining facets

When a new property or use case appears, distinguish among these questions.

1. Are several existing facets together already sufficient?
2. Does this property repeatedly require different judgment such that a separate facet adds real discovery value?
3. Is it actually a general OKF pattern or concept reusable across environments rather than a lens for one kind of environment?
4. Is this merely an easily observable property that adds no useful judgment?
5. Would the facet be taking ownership of knowledge already explained well enough by a general OKF concept?

Do not create facets just to fill out the space of possible cases. Even an observable property should remain a facet only when it provides practical value by connecting the target to relevant OKF judgment.

The kind of entity being described, such as a student, restaurant, statute, or fictional character, does not by itself justify a new facet. Consider whether existing concepts and patterns explain the relevant judgments, and whether a lens that helps discover and apply that knowledge in a particular environment adds discovery value. Being explainable through general knowledge does not by itself remove a facet's value.

Evaluate an existing facet by what difference reading it makes to discovery or judgment. If it merely repeats summaries of linked concepts without adding distinct judgment value, it can be integrated into those concepts or its discovery path simplified.

## Expression and structure

Keep each facet as a single `facets/<name>.md` document by default. If several files seem necessary, first ask whether the additional material belongs in general OKF knowledge, a research note, an experiment, an example, or the target repository itself.

Do not preregister common facet combinations in a separate composition list. If consulting several facets together is sufficient, no extra layer is needed. Reconsider a separate representation only when recurring combinations produce independent interaction knowledge, conflicts, or additional judgment.

## Facets under research

A candidate whose need and judgment value are still being tested may be marked `preview`. A preview facet is not a prerequisite for default application; it is a research entry point for exploring related experiments and cases.

The concrete facet list lives in [Facets](../facets/README.md), while unresolved hypotheses about facet perspectives and boundaries stay in the [facet perspectives research note](../notes/facet-perspectives.md).
