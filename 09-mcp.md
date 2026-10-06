# 09 · Model Context Protocol (MCP)

**Prerequisite:** [08](08-tool-calling.md). **Goal:** Understand the interoperability layer without attributing model intelligence to it.

## What MCP standardizes

MCP is an open protocol for connecting AI applications with external capabilities and context. Its architecture distinguishes a **host** application, **clients** that communicate with servers, and **servers** that expose capabilities. Servers can run locally or remotely. [The official MCP introduction](https://modelcontextprotocol.io/docs/getting-started/intro) and [architecture guide](https://modelcontextprotocol.io/docs/2026-07-28/learn/architecture) describe this structure.

Three server concepts are useful to distinguish:

| Concept | Role | Fictional example |
| --- | --- | --- |
| Tool | An executable operation | Look up an order's status. |
| Resource | Information the application can read as context | A shipping-policy document. |
| Prompt | A reusable interaction template | A template for reviewing a support issue. |

See the [official server-concepts guide](https://modelcontextprotocol.io/docs/2026-07-28/learn/server-concepts) for the definitions. Specific clients and servers can support different subsets; do not assume every integration exposes all three.

## A PM example

An order-service team exposes a small set of capabilities through an MCP server. Compatible AI applications can discover and use those supported capabilities. The server might call the team's existing order API behind the scenes.

The team still owns the meaning of each operation, appropriate access, errors and reliability. A common protocol can reduce bespoke interface work; it does not eliminate the underlying integration.

## The decision this changes

Ask which clients the product needs to support, which capabilities are appropriate to expose and whether the proposed server covers actual user tasks. Evaluate interoperability alongside security, operations and maintenance.

**Common misconception:** MCP is a new model, a memory system or a guarantee of safe autonomy. Its role is communication; the surrounding product determines how capabilities and context are used.

## Check your understanding

Your product has an MCP server. Does that prove every AI client can perform every operation?

<details><summary>Suggested answer</summary>

No. Client support, server capabilities, protocol compatibility, connectivity and authorization all matter. Verify the required client-operation combinations rather than treating the label as a compatibility guarantee.

</details>

[← Previous](08-tool-calling.md) · [Next: API versus MCP →](10-api-vs-mcp.md)
