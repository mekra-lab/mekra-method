# Knowledge properties revealed by personal context

This note is a working document for exploring where existing OKF operating principles may be insufficient when handling personal context, before adopting `personal-context` as an independent facet.

Adopted general principles are linked to the relevant concepts below; the remaining questions are not treated as established principles or a formal classification system. Observe repeated needs and failures in a real personal-context repository, then reflect generalizable conclusions in `okf/` or a facet.

## Starting hypothesis

Personal context is closer to a knowledge graph that connects a person's experiences, relationships, states, preferences, actions, and their changes over time than to a simple list of personal information.

The same knowledge graph may be read from different perspectives, such as self-understanding and personalized support. For now, these are not split into separate facets or separate knowledge bases.

## Questions to explore

### Recorded statements versus facts about the world

A diary, message, or note can support the fact that a statement or experience was recorded, but it does not automatically make every claim inside it a source of truth about the outside world.

For example, if a note says "It felt like A was avoiding me," it can support that this was the person's feeling or interpretation at the time. It does not automatically establish that A intentionally avoided them.

The distinctions between canonical status and certainty, and between maintaining a record and accepting a claim as fact, are now reflected in [source of truth and context](../okf/source-of-truth.md). In personal context, we continue to observe how to express the status and evidence of uncertain interpretations and how to update related records when new experiences or corrections arrive.

### Temporal validity

In personal context, different statements from the past and present do not necessarily conflict. A state may have been valid in the past and later changed.

We need to observe whether it is useful to distinguish information that was wrong from information that was valid at the time, and when the lifecycle fields in OKF v0.2 are worth using.

### Internal access and external disclosure

The scope in which an agent may read sensitive context for internal judgment may differ from the authority to expose that information through an external message, document, API, public repository, or similar channel.

This distinction also recurred in [feedback](../okf/feedback.md) and [distribution](../okf/distribution.md), and was promoted into the general pattern [boundary between information access and external disclosure](../okf/disclosure-boundary.md). The personal-context experiment continues to observe whether sensitive personal material and inferences create additional operating requirements beyond that general principle.

### Withdrawal, deletion, and reverse propagation

Personal material often needs to be removed because of a deletion request, a relationship ending, withdrawal of consent, or abandonment of an incorrect inference.

When source material or a judgment is withdrawn, how far should dependent context and conclusions be re-examined? This may reveal whether [context propagation](../okf/context-propagation.md) needs an explicit notion of reverse change.

## Formalization deliberately deferred

For now, do not turn the following into rules:

- fixed categories such as Observation / Self-Stated / Hypothesis / Preference
- mandatory directory structures such as `state/`, `patterns/`, `people/`, or `relationships/`
- protocols that promote knowledge based only on repetition counts
- an independent `personal-context` facet

If real use repeatedly needs these distinctions, structure them then.

## Next validation

The [personal-context experiment](../experiments/personal-context/README.md) applies the [Knowledge-centered facet](../facets/knowledge-centered.md) and general OKF principles to a minimal structure.

The core questions are:

1. Can personal context be operated adequately using the existing Knowledge-centered facet and general OKF principles?
2. Are there recurring operating choices that are specific to personal context?
3. Which of the issues above are not personal-specific and deserve promotion into general OKF concepts?
4. Which structures or categories initially seemed necessary but prove unnecessary in actual use?
