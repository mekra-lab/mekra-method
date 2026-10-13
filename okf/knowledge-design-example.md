---
type: Example
title: Integrating, separating, and combining the same order knowledge
description: Represent identical hypothetical source material in OKF bodies and compare arrangements through questions and changes
---

# Integrating, separating, and combining the same order knowledge

This hypothetical example illustrates [design exploration and sufficiency](knowledge-design.md) using actual document bodies. Filenames, types, and lengths below are not a fixed template. All three arrangements preserve the same rules; this is not an experimental finding that one performs better.

## Hypothetical source material

Assume `rules.md` contains the following source material. It owns rule definitions and changes, while OKF bodies internalize their meaning from each concept's perspective. Code blocks below represent example file contents. The same `rules.md` sits outside each arrangement's directory, and each bundle is assumed to have an `index.md` declaring `okf_version: "0.2"` and linking its concepts.

```markdown
# Order operating rules

1. Cancellation can be accepted before dispatch is confirmed, but not afterward.
2. An accepted cancellation before payment completes without a refund.
3. After payment, a successful refund completes cancellation.
4. A failed refund leaves cancellation incomplete, with refund processing still pending.
5. Currently, inventory reservations are released immediately when cancellation is accepted. They remain released even if the refund fails.
```

Acceptance of cancellation, completion of cancellation, and inventory release are distinct states. Losing that distinction loses necessary knowledge regardless of file count.

## Integrated arrangement

Read all conditions in one file, `integrated/cancellation.md`.

```markdown
---
type: Rule
title: Order cancellation
---

# Order cancellation

Cancellation can be accepted before dispatch is confirmed, but not afterward.
An accepted cancellation before payment completes without a refund;
after payment, it completes when the refund succeeds.
If the refund fails, cancellation remains incomplete and refund processing is still pending.

Inventory reservations are released immediately when cancellation is accepted.
They remain released even if the refund fails, so inventory release alone
does not establish that cancellation is complete.

[Order operating rules](../rules.md) owns definitions and changes.
```

Conditions for understanding cancellation as a whole are in one place. The same document is also used for inventory-only questions and changes.

## Separated arrangement

Split the knowledge into `split/eligibility.md`, `split/refund.md`, and `split/inventory.md`. Each explains the conditions needed for its own judgments and why a reader would follow a link to another concept.

`split/eligibility.md`:

```markdown
---
type: Rule
title: Cancellation eligibility
---

# Cancellation eligibility

Cancellation can be accepted before dispatch is confirmed, but not afterward.
Eligibility and completion are different. After acceptance, cancellation before
payment completes without a refund; after payment, it awaits a successful refund.
[Payment and refunds](refund.md) explains why failure leaves it incomplete.

Accepted cancellations are subject to [inventory release](inventory.md).
Judge inventory release and cancellation completion separately.
[Order operating rules](../rules.md) owns definitions and changes.
```

`split/refund.md`:

```markdown
---
type: Rule
title: Payment and refunds
---

# Payment and refunds

This concept concerns cancellations accepted before dispatch is confirmed.
Before payment, cancellation completes without a refund. After payment, it
completes on refund success; refund failure means it remains incomplete
with refund processing pending. After dispatch is confirmed, cancellation
cannot be accepted, so distinguish [eligibility](eligibility.md) first.

Refund failure does not itself mean an inventory reservation is retained.
Judge release timing separately through [inventory reservation](inventory.md) conditions.
[Order operating rules](../rules.md) owns definitions and changes.
```

`split/inventory.md`:

```markdown
---
type: Rule
title: Inventory reservation release
---

# Inventory reservation release

When cancellation is accepted before dispatch is confirmed, release inventory
reservations immediately. They remain released even if the refund fails.
However, cancellation after payment remains incomplete if its refund fails,
so do not mark cancellation complete on the basis of inventory release.

[Cancellation eligibility](eligibility.md) identifies the orders subject to release;
[payment and refunds](refund.md) explains completion conditions distinct from release.
[Order operating rules](../rules.md) owns definitions and changes.
```

Reading the inventory document alone provides applicability, timing, exceptions, and the distinction from cancellation completion. Detailed review of the whole process requires moving between concepts. Each explanation derives from the same source, so rule changes require reviewing related restatements as well.

## Combined arrangement

In `combined/`, keep the three separated concepts with the same contents and add `cancellation-flow.md`. This synthesis explains conditions acting together, rather than owning an independent set of rules.

```markdown
---
type: Concept
title: The overall cancellation flow
---

# The overall cancellation flow

Accept cancellation before dispatch is confirmed according to [eligibility](eligibility.md).
Release [inventory reservations](inventory.md) immediately on acceptance.
According to [payment and refunds](refund.md), cancellation before payment
completes without a refund; after payment, it awaits refund success.
If the refund fails, cancellation is incomplete even though inventory has been released.

When assessing the overall state, distinguish eligibility, inventory release,
and cancellation completion. [Order operating rules](../rules.md) is the source of truth.
When individual conditions change, revisit the sequence and state interpretation
in this synthesis as well.
```

Whole-process questions can start with the synthesis, while questions about inventory conditions alone can start with the individual concept. The synthesis consequently needs maintenance after changes too.

## Reading for the same question

The question is: "Cancellation was accepted before dispatch was confirmed, and the refund failed after payment. What are the inventory reservation and cancellation states?" All three arrangements should support the answer: **The inventory reservation is released; cancellation is incomplete and refund processing remains pending.**

| Arrangement | Path supporting the answer | Difference to examine |
| --- | --- | --- |
| Integrated | Acceptance, refund, and inventory conditions in `cancellation.md` | One document contains the evidence, but the same document is read even for an individual judgment. |
| Separated | Exceptions and state distinctions in `inventory.md`, with completion conditions in `refund.md` if needed | The individual concept retains core context and links directly to refund details. |
| Combined | Overall state in `cancellation-flow.md`, with individual concepts if needed | Readers can choose whole-process explanation or individual discovery, with more restatement to maintain. |

For a request after dispatch is confirmed, all three must first conclude that cancellation cannot be accepted. Check whether reading from the refund or inventory document still preserves that premise. This table illustrates reading paths supported by the text; it is not an agent reading trace or a measurement result.

## Applying the same change

Suppose rule 5 in the source changes as follows, with all other rules unchanged:

> Before payment, release inventory reservations when cancellation is accepted. After payment, release them on refund success and retain them if the refund fails.

The integrated arrangement changes inventory conditions and the state explanation in `cancellation.md`. The separated arrangement changes both `inventory.md` and the statement in `refund.md` that "Refund failure does not itself mean an inventory reservation is retained." That statement now becomes "If the refund fails, cancellation is incomplete and the inventory reservation is retained." `eligibility.md` does not directly prescribe release timing, so no sentence needs changing for this update, but that judgment requires reading its contents. The combined arrangement additionally updates immediate release and refund-failure explanations in `cancellation-flow.md`.

After the change, the key explanation in `inventory.md` for the separated and combined arrangements becomes:

```markdown
For cancellations accepted before dispatch is confirmed, release inventory
reservations immediately if payment has not occurred. After payment, release
them on refund success and retain them if the refund fails. Cancellation with
a failed refund remains incomplete, with refund processing and inventory release pending.
```

The combined synthesis must also explain release timing by payment state instead of "immediately on acceptance." The new answer to the same question is: **The inventory reservation is retained; cancellation is incomplete, with refund processing and inventory release pending.** Check the canonical change, updates to related meanings, and interpretation of the question after the change together. Fewer edited files alone do not establish a better arrangement.

## Carrying the chosen arrangement forward

Choose an arrangement according to actual questions and change patterns. If frequent inventory questions lead to the separated arrangement, its operating context might preserve the reason as follows:

> Cancellation eligibility, refunds, and inventory are separate because inventory conditions are frequently queried and updated independently. Each concept preserves dispatch-confirmation conditions and the distinction from cancellation completion. Consider adding a synthesis if repeatedly assembling the whole cancellation flow becomes burdensome.

This illustrates [handing over design choices](knowledge-operation.md#handing-over-design-choices). Do not invent a reason such as "frequently" without observations. If the choice rests on assumptions, leave those assumptions and the conditions to check. If separation continues to help, consider finer separation; if integration helps, broaden the scope read together and revisit the [exploration boundary](knowledge-design.md#expanding-and-concluding-exploration).
