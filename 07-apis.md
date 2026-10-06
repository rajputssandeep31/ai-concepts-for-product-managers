# 07 · APIs and integration contracts

**Prerequisite:** [06](06-hallucinations-reliability.md). **Goal:** Understand the software interface that supplies data or actions.

## What is an API?

API means **Application Programming Interface**: a defined way for software to interact with other software. The interface specifies supported operations and how to use them. APIs can be local or remote; they are not all REST endpoints or internet services. [MDN's API definition](https://developer.mozilla.org/en-US/docs/Glossary/API) explains this wider meaning.

For a web API, a request might name an operation and provide inputs, while a response contains data or an error. Access restrictions, limits and failure behavior are part of the integration the product must understand.

## A PM example

Consider a fictional order service:

```text
Request: look up order DEMO-123 for the authenticated customer
Response: delivery status + last-updated time
```

The AI assistant should summarize the response rather than invent a delivery date. An order not found, an access denial and a service timeout are different outcomes. The interface and product should preserve that distinction.

This is conceptual pseudocode, not a real endpoint or request format.

## The decision this changes

Ask what the service can actually do before designing the experience. Does it return live or cached information? Can it only read, or can it change records? What identifies a completed operation? What happens if a write request is repeated after a timeout?

For an order assistant, launch scope could begin with status lookup while write operations remain outside scope. That is a product boundary, not a limitation of APIs as a category.

**Common misconception:** An API makes a model know everything in the connected service. The application must still choose operations, supply valid inputs and handle access and results.

## Check your understanding

An order API is available. Does this alone give every assistant user permission to read every order?

<details><summary>Suggested answer</summary>

No. Availability of an interface and authorization to particular records are separate. The integration needs to preserve the user's permitted scope and handle denied access explicitly.

</details>

[← Previous](06-hallucinations-reliability.md) · [Next: tool calling →](08-tool-calling.md)
