# 02 · Models, LLMs and AI applications

**Prerequisite:** [01](01-ai-ml-generative-ai.md). **Goal:** Separate a model capability from a complete product.

## What is an LLM?

A model is a learned system that maps inputs to outputs. A large language model, or LLM, learns language patterns and can generate text. Language modeling estimates probabilities over tokens; contemporary models can support tasks such as summarization, explanation and code generation. A fluent output is not a certificate of factual correctness. [Google's language-model introduction](https://developers.google.com/machine-learning/crash-course/llm) explains the basic mechanism.

A model is one component of an AI application. The application also decides what input to supply, which sources to trust, what access to allow, how to display results and what to do when something fails. A provider API can expose model capabilities without supplying all of these product decisions. [OpenAI's text-generation guide](https://developers.openai.com/api/docs/guides/text) provides an example of requesting generated text through an API.

## A PM example

Imagine a support assistant answering, “Where is my order?” A model may understand the question and produce a clear explanation. The product still needs an authorized way to retrieve that customer's order, identify the correct record and handle a delivery-service outage.

If it lacks order data, a polished response is not enough. If it retrieves another customer's record, the integration has failed even when the model writes an accurate summary of that record.

## The decision this changes

Separate the acceptance criteria:

- Can the model interpret the request and explain an outcome?
- Can the application obtain the correct evidence for the right user?
- Can the user tell whether the operation succeeded or failed?

This separation helps assign ownership and diagnose failures. Buying access to a better model will not automatically repair incorrect permissions or missing data.

**Common misconception:** A model trained on lots of data automatically knows the live state of your product. Live information needs an appropriate data path.

## Check your understanding

A new model produces better answers, but the assistant still shows stale delivery dates. What would you inspect first?

<details><summary>Suggested answer</summary>

Inspect retrieval freshness, caching and the underlying order source. Then check whether the application passes that evidence to the model and whether the answer reflects it. Do not assume a model upgrade solves a data-pipeline problem.

</details>

[← Previous](01-ai-ml-generative-ai.md) · [Next: training versus inference →](03-training-vs-inference.md)
