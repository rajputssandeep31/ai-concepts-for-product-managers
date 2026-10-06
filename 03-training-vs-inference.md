# 03 · Training versus inference

**Prerequisite:** [02](02-models-llms-applications.md). **Goal:** Distinguish learning from using a model.

## The distinction

During training, a learning process adjusts model parameters using data and an objective. During inference, the trained model processes new input to produce an output. Further training, including fine-tuning, can change model behavior. Supplying a document as input ordinarily changes the information available for that request, not the model's parameters. [Google's ML introduction](https://developers.google.com/machine-learning/intro-to-ml/what-is-ml) explains learning from data; its [LLM overview](https://developers.google.com/machine-learning/crash-course/llm/transformers) discusses training and use.

Do not confuse this distinction with provider data policies. Whether a service stores inputs or later uses them for training is a separate question that must be checked for the relevant service and agreement.

## A PM example

An assistant must explain a return policy that changes monthly.

**Option A:** Supply the currently applicable policy when answering.

**Option B:** Change the model through a training process.

These solve different problems. If the main failure is missing current policy information, first fix access to the current source. If the model repeatedly fails a specialized output task even with the right information, a behavior-improvement approach may be worth evaluating.

## The decision this changes

Describe the failure precisely: missing information, wrong interpretation, poor formatting or an inappropriate action. The intervention should target that failure. Decide who owns the source, how updates become available, and what happens when evidence is unavailable.

**Common misconception:** “We uploaded our documents, so we trained the model.” Uploading, indexing, retrieving and training are distinct operations. Ask which operation actually occurred.

## Check your understanding

A user corrects an assistant in a conversation. Does that prove the base model was retrained?

<details><summary>Suggested answer</summary>

No. The correction may be present in conversation context or stored by the application for later use. Changing the base model's parameters requires a training process. Check the application's memory behavior and the service's data policy separately.

</details>

[← Previous](02-models-llms-applications.md) · [Next: tokens, context and memory →](04-tokens-context-memory.md)
