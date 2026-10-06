# 04 · Tokens, context windows and memory

**Prerequisite:** [03](03-training-vs-inference.md). **Goal:** Understand what information is available for a particular response.

## The terms

A **token** is a unit used to represent input or output. For text, it may be a word, part of a word or a character; exact splitting depends on the tokenizer. Word count and token count are not interchangeable. [Google's token explanation](https://developers.google.com/machine-learning/crash-course/llm) covers this distinction.

**Context** is information supplied for the current task, such as instructions, relevant conversation and evidence. A **context window** limits how much information a model can consider in a request; precise accounting depends on the model and service. [OpenAI's prompt-engineering guide](https://developers.openai.com/api/docs/guides/prompt-engineering#include-relevant-context-information) explains the limit.

**Memory** is a product capability for retaining or retrieving information over time. It should not be inferred from a large context window. Applications can supply previous messages or manage conversation state. [OpenAI's conversation-state guide](https://developers.openai.com/api/docs/guides/conversation-state) illustrates this application responsibility.

## A PM example

A user asks a policy assistant for a recommendation discussed last month. That discussion may be stored somewhere, but storage alone does not prove it is available for this response. The system must select and supply the relevant information, while respecting access and retention choices.

An interface that says “I remember” creates an expectation. Specify what is retained, how it is used and how the user can correct it.

## The decision this changes

Decide which information is essential for the task before increasing the amount supplied. Define behavior when important context is missing. A larger window may help with long material, but it does not establish that every important detail is used correctly.

**Common misconception:** Increasing context size is the same as improving memory or accuracy. These are different product and evaluation questions.

## Check your understanding

An assistant has a large context window. Can you promise it remembers every prior conversation?

<details><summary>Suggested answer</summary>

No. You need to know what the application stores, what it retrieves, what it supplies now, and whether the user permitted that use. Window size describes a request limit, not a universal memory guarantee.

</details>

[← Previous](03-training-vs-inference.md) · [Next: prompts and context design →](05-prompts-and-context.md)
