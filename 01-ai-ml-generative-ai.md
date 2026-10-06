# 01 · AI, machine learning and generative AI

**Prerequisites:** None. **Goal:** Choose the type of capability before choosing a model.

## Three terms, three levels

AI is the broad field of building systems that perform tasks associated with intelligence. Machine learning is an approach in which a model learns patterns from data. Generative AI produces content such as text, images or audio; generation is one capability within the wider landscape. [Google's introduction to machine learning](https://developers.google.com/machine-learning/intro-to-ml/what-is-ml) describes learning approaches and generative models.

Treat this as a useful orientation, not a complete taxonomy. Modern products can combine learned models, explicit rules, search and conventional software.

## A PM example

Suppose an expense product has three requests:

| User need | Candidate approach | Why it fits |
| --- | --- | --- |
| Reject a claim above a fixed policy limit | Explicit rule | The requirement is known and exact. |
| Estimate which claims merit review | Predictive model | Historical examples may help identify a pattern; errors need evaluation. |
| Draft an explanation of a policy decision | Generative model | The output is new language, but its claims must match the actual policy. |

The third request does not justify asking a language model to decide whether a claim violates a numerical limit. The product can calculate the decision with conventional logic and ask a model to explain the result.

## The decision this changes

Write the required output before the feature name. Is it a score, a label, retrieved evidence, new content or an action? Then compare a simple baseline with the AI approach. A capability is useful if it improves the user's outcome enough to justify its additional uncertainty and operating cost.

**Common misconception:** Every useful AI feature needs a conversational interface. A ranking improvement or document classifier may work best inside an existing workflow.

## Check your understanding

A PM wants AI to calculate sales tax, write a description of the calculation and predict which invoices will be paid late. Should one language model own all three?

<details><summary>Suggested answer</summary>

Separate the tasks. Use authoritative rules and exact calculations for tax, grounded generation for the explanation, and evaluate a predictive approach for late-payment risk. A shared UI can coordinate them without pretending they are the same capability.

</details>

[Next: models, LLMs and applications →](02-models-llms-applications.md) · [Learning guide](README.md)
