---
type: Pattern
title: Boundary between information access and external disclosure
description: Distinguish information that may be used for internal judgment from authority to disclose or transmit it externally
---

# Boundary between information access and external disclosure

## Problem

An agent's ability to access information does not by itself grant authority to disclose that information, or context derived from it, externally.

Even work that benefits from broad context—such as internal analysis, drafting feedback, publication review, or personalized support—still requires a separate decision about what may actually be sent outside and to whom.

## Choice

Distinguish the scope in which information may be read and used for internal judgment from authority to disclose or transmit it through external messages, documents, issues, APIs, public repositories, or similar channels.

For external actions, use only the information needed for the purpose, recipient, disclosure scope, and authority the user has already granted. Do not treat all accessible context as automatically within the disclosure scope.

When authority for the purpose and scope is already clear, there is no need to mechanically reconfirm the same decision. Conversely, do not infer new external-disclosure authority merely from internal access or delegated autonomy over the task.

## Application questions

- Is the information needed for internal judgment the same information that must appear in the actual output?
- Are the purpose and recipient of the disclosure or transmission within the current authority?
- Does sensitive or identifying context need to be transmitted directly, or can it be generalized while preserving meaning?
- If an action creates a new disclosure scope, is that authority clear?

[Feedback from adoption](feedback.md) distinguishes discretion to identify and draft useful feedback from authority to actually send it. [Research and multilingual distribution](distribution.md) reassesses publication suitability for each change even when file paths and the shared source of truth remain the same.
