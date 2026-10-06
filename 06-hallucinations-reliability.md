# 06 · Hallucinations and reliability

**Prerequisite:** [05](05-prompts-and-context.md). **Goal:** Design around incorrect answers rather than judging fluency.

## What can go wrong?

An LLM can produce a convincing statement that is false or unsupported. This is commonly called a hallucination. It can also misunderstand a request, omit an important exception or misapply evidence. [Google's LLM overview](https://developers.google.com/machine-learning/crash-course/llm/transformers#problems_with_llms) describes mistakes and other limitations.

For product work, identify the observable failure rather than arguing over the label. An incorrect account lookup, an outdated source and an invented claim require different repairs.

## A PM example

A fictional support assistant says, “Your refund has been processed,” even though it only drafted a response. The dangerous part is the user's belief that an operation occurred.

A better product distinguishes evidence states:

| State | Appropriate product behavior |
| --- | --- |
| No record retrieved | Explain that the status could not be checked. |
| Refund request submitted | Show submission, not completion. |
| Authorized system confirms completion | Report the confirmed result with an appropriate reference. |

These are example design choices, not a universal prescription for all refund products.

## The decision this changes

Define failure severity and the user's recovery path. A drafting assistant and an action-taking assistant can create different consequences from the same language error. Decide which claims need authoritative evidence and which actions need approval or deterministic validation.

Build evaluation examples for missing evidence, contradictory evidence, unavailable services and misleading requests. Later lessons will cover evaluation design in detail.

**Common misconception:** A confident tone or a cited URL proves an answer is correct. Check whether the evidence supports the actual claim and whether the claimed action occurred.

## Check your understanding

An assistant's answers sound more natural after a prompt change. Is that sufficient evidence to release it?

<details><summary>Suggested answer</summary>

No. Naturalness is one quality dimension. Check task correctness, unsupported claims, failure handling and any operational consequences on representative cases before judging release readiness.

</details>

[← Previous](05-prompts-and-context.md) · [Next: APIs →](07-apis.md)
