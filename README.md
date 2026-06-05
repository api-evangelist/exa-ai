# Exa (exa-ai)

Exa is a web search API and AI research platform built specifically for LLMs and agents — semantic and keyword search across the open web with token-efficient highlights, structured outputs, sub-200ms latency tiers, and verticals for code, companies, news, people, research, and financials. The platform pairs the core Search, Contents, and Answer endpoints with Research (asynchronous deep research), Agent (managed multi-step agents at four effort modes), Monitors (scheduled searches with webhooks), and Websets (curated, enrichable result collections). Customers include Cognition (Devin), HubSpot, Monday, Databricks, AWS, and Cursor; Exa raised a $250M Series C to build the search engine for AIs. Open SDKs in Python and JavaScript, an MCP server, Google Sheets and n8n integrations, and a free tier of 1,000 requests/month round out the surface.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/exa-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/exa-ai/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI
- Search
- Web Search
- Neural Search
- LLM
- Agents
- Research
- Websets

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Exa Search API

Exa's prompt-engineered Search API performs semantic and keyword web search optimized for LLM and agent consumption. Returns a list of relevant results with URLs, titles, authors, published dates, relevance scores, and optional token-efficient highlights, summaries, or full text via the bundled Contents API. The Answer endpoint returns an LLM-generated answer grounded in web citations. Verticals include Code, Companies, News, People, Research, and Financials. Latency tiers run from fast (180ms) to auto (~1s) to deep (~10s).

- **Human URL:** [https://exa.ai/docs/reference/search-api-guide](https://exa.ai/docs/reference/search-api-guide)
- **Base URL:** `https://api.exa.ai`

#### Tags

- AI
- Search
- Web Search
- Neural Search
- LLM

#### Properties

- [Documentation](https://exa.ai/docs/reference/search-api-guide)
- [Documentation](https://exa.ai/docs/reference/search)
- [Documentation](https://exa.ai/docs/reference/contents-api-guide)
- [Documentation](https://exa.ai/docs/reference/answer)
- [OpenAPI](openapi/exa-search-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/exa-search-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/exa-search-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/exa-search-result-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/exa-ai-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Exa Research API

Asynchronous multi-step deep-research tasks. Submit a research instruction, Exa orchestrates a Deep Search agent across the live web with structured outputs and web-grounded citations, and you poll for the completed report. Lives under /research/v1 with create, get, and list operations.

- **Human URL:** [https://exa.ai/docs/reference/research/overview](https://exa.ai/docs/reference/research/overview)
- **Base URL:** `https://api.exa.ai`

#### Tags

- AI
- Search
- Research
- Agents
- Deep Search

#### Properties

- [Documentation](https://exa.ai/docs/reference/research/overview)
- [Documentation](https://exa.ai/docs/reference/research/create-a-task)
- [Documentation](https://exa.ai/docs/reference/research/get-a-task)
- [Documentation](https://exa.ai/docs/reference/research/list-tasks)
- [OpenAPI](openapi/exa-research-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/exa-research-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/exa-research-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Exa Monitors API

Schedule recurring Exa searches and receive webhook notifications when fresh matching content appears on the web. Supports create, list, get, update, delete, batch actions, manual trigger, and run history. Two API versions are exposed — the original /monitors namespace and the newer /v0/monitors surface aligned with Websets.

- **Human URL:** [https://exa.ai/docs/reference/monitors-api-guide](https://exa.ai/docs/reference/monitors-api-guide)
- **Base URL:** `https://api.exa.ai`

#### Tags

- AI
- Search
- Monitors
- Webhooks
- Scheduled

#### Properties

- [Documentation](https://exa.ai/docs/reference/monitors-api-guide)
- [Documentation](https://exa.ai/docs/reference/monitors/create-a-monitor)
- [Documentation](https://exa.ai/docs/reference/monitors/list-monitors)
- [OpenAPI](openapi/exa-monitors-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/exa-monitors-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/exa-monitors-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Exa Agent API

Run an Exa-hosted research agent at four effort modes — low ($0.025), medium ($0.10), high ($0.50), and x-high ($2.00) — with built-in web search, content retrieval, structured outputs, and event streaming. Create, list, get, cancel, delete, and stream events from runs under /agent/runs.

- **Human URL:** [https://exa.ai/docs/reference/agent-api-guide](https://exa.ai/docs/reference/agent-api-guide)
- **Base URL:** `https://api.exa.ai`

#### Tags

- AI
- Agents
- Search
- LLM

#### Properties

- [Documentation](https://exa.ai/docs/reference/agent-api-guide)
- [Documentation](https://exa.ai/docs/reference/agent-api/create-a-run)
- [Documentation](https://exa.ai/docs/reference/agent-api/get-a-run)
- [OpenAPI](openapi/exa-agent-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/exa-agent-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/exa-agent-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Exa Websets API

Curated, enrichable collections of web results scoped to a query, vertical (companies, people, news, research), or imported list. Compose searches, attach LLM-driven enrichments, evaluate items, subscribe to webhooks for asynchronous events, and import seed lists. Endpoints under /v0/websets, /v0/webhooks, /v0/events, and /v0/imports.

- **Human URL:** [https://exa.ai/docs/websets/api-guide](https://exa.ai/docs/websets/api-guide)
- **Base URL:** `https://api.exa.ai`

#### Tags

- AI
- Search
- Websets
- Enrichment
- Webhooks
- Imports

#### Properties

- [Documentation](https://exa.ai/docs/websets/api-guide)
- [Documentation](https://exa.ai/docs/websets/api/overview)
- [Documentation](https://exa.ai/docs/websets/api/websets/create-a-webset)
- [OpenAPI](openapi/exa-websets-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/exa-websets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/exa-websets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/exa-webset-item-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Exa Team API

Lightweight team-info endpoint at /v0/teams/me — returns the authenticated team identity and metadata for the API key.

- **Human URL:** [https://exa.ai/docs](https://exa.ai/docs)
- **Base URL:** `https://api.exa.ai`

#### Tags

- AI
- Search
- Team
- Account

#### Properties

- [Documentation](https://exa.ai/docs)
- [OpenAPI](openapi/exa-team-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/exa-team-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/exa-team-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Exa Team Management API

Admin API for managing API keys within a team — create, list, get, update, delete keys with optional per-key rate limits and budgets, plus a per-key usage endpoint at GET /api-keys/{id}/usage. The foundation for per-workload cost allocation and FinOps reporting against Exa.

- **Human URL:** [https://admin-api.exa.ai/team-management](https://admin-api.exa.ai/team-management)
- **Base URL:** `https://admin-api.exa.ai/team-management`

#### Tags

- AI
- Search
- Administration
- API Keys
- Team Management

#### Properties

- [Documentation](https://exa.ai/docs)
- [OpenAPI](openapi/exa-team-management-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/exa-team-management-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/exa-team-management-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://exa.ai)
- [Documentation](https://exa.ai/docs)
- [Getting Started](https://exa.ai/docs/getting-started)
- [Documentation](https://exa.ai/docs/reference/search-api-guide)
- [Sign Up](https://dashboard.exa.ai)
- [Sandbox](https://dashboard.exa.ai/playground)
- [Pricing](https://exa.ai/pricing)
- [Changelog](https://exa.ai/changelog)
- [Blog](https://exa.ai/blog)
- [Status Page](https://status.exa.ai)
- [Terms of Service](https://exa.ai/terms)
- [Privacy Policy](https://exa.ai/privacy)
- [Support](https://exa.ai/contact)
- [LinkedIn](https://www.linkedin.com/company/exa-ai)
- [GitHub Organization](https://github.com/exa-labs)
- [SDK](https://github.com/exa-labs/exa-py)
- [SDK](https://github.com/exa-labs/exa-js)
- [Tool](https://github.com/exa-labs/exa-mcp-server)
- [Tool](https://github.com/exa-labs/websets-mcp-server)
- [Tool](https://github.com/exa-labs/zed-exa-mcp-extension)
- [Tool](https://github.com/exa-labs/exa-for-sheets)
- [Tool](https://github.com/exa-labs/n8n-integration)
- [Code Examples](https://github.com/exa-labs/exa-hallucination-detector)
- [Code Examples](https://github.com/exa-labs/company-researcher)
- [Code Examples](https://github.com/exa-labs/exa-deepseek-chat)
- [Code Examples](https://github.com/exa-labs/exa-o3mini-chat)
- [Code Examples](https://github.com/exa-labs/answer-chat-app)
- [Code Examples](https://github.com/exa-labs/jfk-files-app)
- [Code Examples](https://github.com/exa-labs/research-paper-app)
- [Code Examples](https://github.com/exa-labs/websets-news-monitor)
- [Authentication](https://exa.ai/docs/getting-started/authentication)
- [OpenAPI](https://exa.ai/docs/exa-spec.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](https://exa.ai/docs/team-management-spec.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plans](plans/exa-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/exa-ai-rate-limits.yml)
- [Fin Ops](finops/exa-ai-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
