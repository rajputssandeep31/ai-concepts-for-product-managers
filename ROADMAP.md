# Learning roadmap

Read in order. Lessons 01–10 are written in this first editorial draft. Later lessons below are planned; their titles are a learning sequence, not empty articles or claims of completed coverage.

## Stage 1 · Foundations

| Lesson | Topic | Status |
| --- | --- | --- |
| 01 | [AI, ML and generative AI](01-ai-ml-generative-ai.md) | Draft written |
| 02 | [Models, LLMs and applications](02-models-llms-applications.md) | Draft written |
| 03 | [Training versus inference](03-training-vs-inference.md) | Draft written |
| 04 | [Tokens, context windows and memory](04-tokens-context-memory.md) | Draft written |
| 05 | [Prompts and context design](05-prompts-and-context.md) | Draft written |
| 06 | [Hallucinations and reliability](06-hallucinations-reliability.md) | Draft written |

**Milestone:** Explain why a model alone is not a complete product and describe a useful task, required evidence and failure behavior.

## Stage 2 · Interfaces and tools

| Lesson | Topic | Status |
| --- | --- | --- |
| 07 | [APIs](07-apis.md) | Draft written |
| 08 | [Tool calling](08-tool-calling.md) | Draft written |
| 09 | [MCP](09-mcp.md) | Draft written |
| 10 | [API versus MCP](10-api-vs-mcp.md) | Draft written |

**Milestone:** Trace a user request through a model, a tool handler and an underlying service; explain where authorization and success are established.

## Stage 3 · Retrieval and grounding

All topics in this stage are planned.

11. Embeddings: what a numerical representation is useful for.
12. Semantic search versus keyword search: choosing and combining retrieval approaches.
13. Vector indexes and databases: storage, filtering and retrieval responsibilities.
14. Chunking and indexing: how document preparation changes what can be found.
15. Retrieval-augmented generation (RAG): from question to evidence to answer.
16. Reranking and retrieval evaluation: which failure belongs to search?
17. Grounding and citations: whether a source supports the claim.
18. Freshness and permissions in retrieval: current evidence for the right user.

**Milestone:** Diagnose a wrong answer as missing retrieval, poor ranking, outdated evidence or incorrect use of evidence rather than reflexively changing the model.

## Stage 4 · Model behavior and output design

All topics in this stage are planned.

19. Structured outputs and schemas: valid structure versus correct meaning.
20. Sampling and decoding controls: variation, reproducibility and provider differences.
21. Fine-tuning: behavior adaptation and its limits.
22. Prompting versus RAG versus fine-tuning: choosing the intervention.
23. Reasoning models and inference-time compute: quality, latency and cost tradeoffs.
24. Multimodal models: text, images, audio and video as product inputs and outputs.

**Milestone:** Match the intervention to an observed failure and evaluate the full task rather than selecting a technique by popularity.

## Stage 5 · Workflows and agents

All topics in this stage are planned.

25. Deterministic workflows versus model-directed agents.
26. Agent loops: plans, actions, observations and stopping conditions.
27. State and memory: what persists, where, and under whose control.
28. Planning, routing and orchestration: assigning work to the right capability.
29. Human approval and bounded autonomy: when the system may act.
30. Multi-agent systems: coordination benefits, complexity and evaluation.

**Milestone:** Justify the degree of autonomy needed for a task and specify limits, recovery and completion evidence.

## Stage 6 · Quality, safety and evaluation

All topics in this stage are planned.

31. Task evaluations and representative datasets.
32. Offline evaluations, online experiments and launch criteria.
33. Model-based grading, human review and calibration.
34. Prompt injection and untrusted content.
35. Authentication, authorization and least privilege.
36. Guardrails, adversarial testing and failure recovery.
37. Privacy, data retention and model/provider boundaries.

**Milestone:** Produce a release argument grounded in task evidence, failure consequences and operating controls.

## Stage 7 · Production and product economics

All topics in this stage are planned.

38. Latency, streaming and time to useful output.
39. Cost per task, token accounting and inference economics.
40. Caching, routing, batching and model selection.
41. Rate limits, retries, idempotency and fallbacks.
42. Observability: traces, task success and failure diagnosis.
43. Model/version updates, regressions and controlled rollout.
44. Build versus buy, hosting and dependency choices.
45. Pricing and packaging for AI capabilities.
46. Adoption and trust: helping users learn when to rely on the product.
47. Differentiation: which part of the system creates durable user value?
48. Capstone: write and defend an AI feature PRD.

**Milestone:** Connect task quality and operating cost to a useful, maintainable product proposition.

## Changes to the sequence

Add new concepts when they resolve an actual PM decision and their prerequisites are clear. Split overloaded lessons rather than filling one article with unexplained vocabulary. Keep existing lesson IDs stable; record additions, corrections and moves in the changelog. The next lesson to develop is **11: embeddings** after review of this opening sequence.
