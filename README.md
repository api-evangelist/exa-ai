# Exa (exa-ai)
Exa is a web search API and AI research platform built specifically for LLMs and agents — semantic and keyword search across the open web with token-efficient highlights, structured outputs, sub-200ms latency tiers, and verticals for code, companies, news, people, research, and financials. The platform pairs the core Search, Contents, and Answer endpoints with Research (asynchronous deep research), Agent (managed multi-step agents at four effort modes), Monitors (scheduled searches with webhooks), and Websets (curated, enrichable result collections). Customers include Cognition (Devin), HubSpot, Monday, Databricks, AWS, and Cursor; Exa raised a $250M Series C to build the search engine for AIs.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/exa-ai/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Search, Web Search, Neural Search, LLM, Agents, Research, Websets

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Pricing Summary

| Plan | Price | Notes |
|---|---|---|
| Free | $0 | 1,000 requests / month, full feature access |
| Search | $7 per 1,000 requests | Real-time search + token-efficient contents |
| Deep Search | $12–$15 per 1,000 requests | Multi-step agent workflows with citations |
| Contents | $1 per 1,000 pages per content type | Full page contents for LLM context |
| Monitors | $15 per 1,000 runs | Scheduled searches + webhook delivery |
| Agent | $0.025 – $2.00 per run | Effort modes: low / medium / high / x-high |
| Enterprise | Contact | Custom datasets, dedicated support, SSO |

## APIs

### Exa Search API
Prompt-engineered semantic and keyword web search optimized for LLMs and agents. Bundles `/search`, `/contents`, and `/answer` with latency tiers (fast 180ms, auto ~1s, deep ~10s) and verticals (Code, Companies, News, People, Research, Financials).

**Human URL:** [https://exa.ai/docs/reference/search-api-guide](https://exa.ai/docs/reference/search-api-guide)

- [Documentation — Search Guide](https://exa.ai/docs/reference/search-api-guide)
- [Documentation — Search Reference](https://exa.ai/docs/reference/search)
- [Documentation — Contents Guide](https://exa.ai/docs/reference/contents-api-guide)
- [Documentation — Answer](https://exa.ai/docs/reference/answer)
- [OpenAPI](openapi/exa-search-api-openapi.yml)
- [JSON Schema — Search Result](json-schema/exa-search-result-schema.json)
- [JSON-LD Context](json-ld/exa-ai-context.jsonld)
- [Naftiko Capability — Search](capabilities/search-search.yaml)

### Exa Research API
Asynchronous deep-research tasks under `/research/v1` — submit an instruction, Exa runs a multi-step Deep Search agent with structured outputs and web-grounded citations, you poll for the result.

**Human URL:** [https://exa.ai/docs/reference/research/overview](https://exa.ai/docs/reference/research/overview)

- [Documentation — Overview](https://exa.ai/docs/reference/research/overview)
- [Documentation — Create a Task](https://exa.ai/docs/reference/research/create-a-task)
- [OpenAPI](openapi/exa-research-api-openapi.yml)
- [Naftiko Capability — Research](capabilities/research-research.yaml)

### Exa Monitors API
Scheduled recurring searches that fire webhooks when fresh content matches. Exposes the legacy `/monitors` surface and the newer `/v0/monitors` surface aligned with Websets.

**Human URL:** [https://exa.ai/docs/reference/monitors-api-guide](https://exa.ai/docs/reference/monitors-api-guide)

- [Documentation — Monitors Guide](https://exa.ai/docs/reference/monitors-api-guide)
- [OpenAPI](openapi/exa-monitors-api-openapi.yml)
- [Naftiko Capability — Monitors](capabilities/monitors-monitors.yaml)

### Exa Agent API
Hosted research agent at four effort modes — low ($0.025), medium ($0.10), high ($0.50), x-high ($2.00) — under `/agent/runs` with create, list, get, cancel, delete, and event streaming.

**Human URL:** [https://exa.ai/docs/reference/agent-api-guide](https://exa.ai/docs/reference/agent-api-guide)

- [Documentation — Agent Guide](https://exa.ai/docs/reference/agent-api-guide)
- [OpenAPI](openapi/exa-agent-api-openapi.yml)
- [Naftiko Capability — Agent](capabilities/agent-agent.yaml)

### Exa Websets API
Curated, enrichable collections of web results scoped to a query, vertical, or import. Compose searches, attach LLM-driven enrichments, evaluate items, subscribe to webhooks, and import seed lists. Endpoints under `/v0/websets`, `/v0/webhooks`, `/v0/events`, and `/v0/imports`.

**Human URL:** [https://exa.ai/docs/websets/api-guide](https://exa.ai/docs/websets/api-guide)

- [Documentation — Websets Guide](https://exa.ai/docs/websets/api-guide)
- [OpenAPI](openapi/exa-websets-api-openapi.yml)
- [JSON Schema — Webset Item](json-schema/exa-webset-item-schema.json)
- [Naftiko Capability — Websets](capabilities/websets-websets.yaml)

### Exa Team API
`/v0/teams/me` — return the authenticated team identity and metadata for the API key.

- [OpenAPI](openapi/exa-team-api-openapi.yml)
- [Naftiko Capability — Team](capabilities/team-team.yaml)

### Exa Team Management API
Admin surface at `admin-api.exa.ai/team-management/api-keys` to create, list, get, update, and delete API keys with optional per-key rate limits and budgets, plus a per-key usage endpoint at `GET /api-keys/{id}/usage` — the foundation for per-workload cost allocation.

- [OpenAPI](openapi/exa-team-management-api-openapi.yml)
- [Naftiko Capability — Team Management](capabilities/team-management-team-management.yaml)

## Common

- [Portal](https://exa.ai)
- [Documentation](https://exa.ai/docs)
- [Getting Started](https://exa.ai/docs/getting-started)
- [Sign Up — Dashboard](https://dashboard.exa.ai)
- [Sandbox — API Playground](https://dashboard.exa.ai/playground)
- [Pricing](https://exa.ai/pricing)
- [Changelog](https://exa.ai/changelog)
- [Blog](https://exa.ai/blog)
- [Status Page](https://status.exa.ai)
- [Terms of Service](https://exa.ai/terms)
- [Privacy Policy](https://exa.ai/privacy)
- [LinkedIn](https://www.linkedin.com/company/exa-ai)
- [GitHub Organization](https://github.com/exa-labs)
- [Plans](plans/exa-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/exa-ai-rate-limits.yml)
- [FinOps](finops/exa-ai-finops.yml)

## SDKs, Tools, and Examples

- [Python SDK — exa-py](https://github.com/exa-labs/exa-py)
- [JavaScript / TypeScript SDK — exa-js](https://github.com/exa-labs/exa-js)
- [Exa MCP Server](https://github.com/exa-labs/exa-mcp-server)
- [Websets MCP Server](https://github.com/exa-labs/websets-mcp-server)
- [Zed Exa MCP Extension](https://github.com/exa-labs/zed-exa-mcp-extension)
- [Exa for Google Sheets](https://github.com/exa-labs/exa-for-sheets)
- [Exa n8n Integration](https://github.com/exa-labs/n8n-integration)
- [Hallucination Detector](https://github.com/exa-labs/exa-hallucination-detector)
- [Company Researcher](https://github.com/exa-labs/company-researcher)
- [Exa + DeepSeek R1 Chat](https://github.com/exa-labs/exa-deepseek-chat)
- [Exa + OpenAI o3-mini Chat](https://github.com/exa-labs/exa-o3mini-chat)
- [Exa Answer Chat App](https://github.com/exa-labs/answer-chat-app)
- [JFK Files Chat](https://github.com/exa-labs/jfk-files-app)
- [Research Paper App](https://github.com/exa-labs/research-paper-app)
- [Websets News Monitor](https://github.com/exa-labs/websets-news-monitor)

## Maintainers

- [Kin Lane](https://apievangelist.com) — info@apievangelist.com
