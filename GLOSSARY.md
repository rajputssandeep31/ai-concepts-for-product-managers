# Foundation glossary

This glossary covers the opening lessons. Use the linked lesson for examples, caveats and source attribution. New terms should be added when their lessons are developed.

| Term | Working explanation | Lesson |
| --- | --- | --- |
| AI | Broad field of systems performing tasks associated with intelligence. | [01](01-ai-ml-generative-ai.md) |
| Machine learning | Learning patterns from data to produce useful outputs. | [01](01-ai-ml-generative-ai.md) |
| Generative AI | Models that produce content such as text, images or audio. | [01](01-ai-ml-generative-ai.md) |
| Model | A learned system that maps inputs to outputs. | [02](02-models-llms-applications.md) |
| LLM | Large language model; can generate language from learned patterns and supplied context. | [02](02-models-llms-applications.md) |
| AI application | The product system around a model: data, tools, interface, controls and operations. | [02](02-models-llms-applications.md) |
| Training | A learning process that adjusts model parameters. | [03](03-training-vs-inference.md) |
| Inference | Using a trained model on new input. | [03](03-training-vs-inference.md) |
| Token | A representational unit; for text it can be a word, subword or character. | [04](04-tokens-context-memory.md) |
| Context | Information supplied for the model's current task. | [04](04-tokens-context-memory.md) |
| Context window | A limit on information considered for a request, with service-specific accounting. | [04](04-tokens-context-memory.md) |
| Memory | Application mechanisms for retaining or retrieving information across interactions. | [04](04-tokens-context-memory.md) |
| Prompt | Task instructions, constraints and possibly examples or other material. | [05](05-prompts-and-context.md) |
| Context engineering | Selecting and maintaining information available to the model; a practice description. | [05](05-prompts-and-context.md) |
| Hallucination | A false or unsupported model-generated claim; diagnose the observable failure. | [06](06-hallucinations-reliability.md) |
| API | A defined interface for software to interact with software. | [07](07-apis.md) |
| Tool call | A request to use an available capability; distinguish it from execution or success. | [08](08-tool-calling.md) |
| MCP | Model Context Protocol: an interoperability protocol for AI applications and external capabilities/context. | [09](09-mcp.md) |
| MCP host | The AI application coordinating clients. | [09](09-mcp.md) |
| MCP client | The component communicating with an MCP server. | [09](09-mcp.md) |
| MCP server | A program exposing supported capabilities and context. | [09](09-mcp.md) |
| Resource | Information exposed for an application to read as context. | [09](09-mcp.md) |

Definitions are intentionally brief. Similar words can mean different things in vendor-specific products; read the relevant contract before treating terminology as a capability guarantee.
