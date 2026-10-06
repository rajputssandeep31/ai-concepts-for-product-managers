# 05 · Prompts and context design

**Prerequisite:** [04](04-tokens-context-memory.md). **Goal:** Specify the task and supply the material required to do it.

## Instructions and evidence

A prompt communicates a task, constraints and sometimes examples. Context can also contain source material, conversation history and tool results. Clear instructions and relevant evidence support useful responses, but they do not guarantee correctness. [OpenAI's prompt-engineering guide](https://developers.openai.com/api/docs/guides/prompt-engineering) discusses instructions, examples and context.

The phrase **context engineering** is often used for the broader work of selecting, arranging and maintaining information available to the model. Treat the phrase as a practice description, not a single standardized component.

## A PM example

“Summarize customer feedback” leaves important decisions unspecified. A better task definition for a fictional research assistant is:

> Group the supplied feedback by the stage of the checkout journey. For each group, describe the friction and link to the supplied feedback IDs. Separate observed comments from your hypotheses. If a claim lacks supporting feedback, leave it out. Do not treat this sample as representative of all customers.

The application must also supply the permitted feedback and IDs. A well-written instruction cannot compensate for an empty or incorrectly scoped dataset.

## The decision this changes

Define the output contract with the people who will use it. What evidence should appear? What should happen when the source contradicts itself? What distinguishes a useful result from a fluent but unhelpful one?

Version the task definition and evaluate changes on representative examples. Avoid treating a successful one-off conversation as release evidence.

**Common misconception:** More instructions always improve performance. Unnecessary or conflicting material can make the task harder to specify and assess.

## Check your understanding

The prompt requires citations, but the application supplies source text without stable references. What needs to change?

<details><summary>Suggested answer</summary>

Provide references the application can resolve and verify, then evaluate whether the cited material actually supports each claim. Asking for citations alone does not establish grounded answers.

</details>

[← Previous](04-tokens-context-memory.md) · [Next: hallucinations and reliability →](06-hallucinations-reliability.md)
