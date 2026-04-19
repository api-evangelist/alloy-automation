# Alloy Automation (alloy-automation)

Alloy Automation is the all-in-one integration infrastructure platform for SaaS and AI, offering embedded iPaaS, unified API, and connectivity API products that let companies launch native integrations, build workflows, and connect to 1000+ apps with a single endpoint.

**Portal:** [https://docs.runalloy.com/](https://docs.runalloy.com/)
**Website:** [https://runalloy.com/](https://runalloy.com/)

## APIs

### Alloy Automation Embedded API

Embed native integration workflows directly in your product. Manage end users, retrieve available integrations, trigger events, monitor workflow execution, and control workflow lifecycle.

- **Documentation:** [https://docs.runalloy.com/embedded/quick-start](https://docs.runalloy.com/embedded/quick-start)
- **Base URL:** `https://embedded.runalloy.com/2025-09`
- **OpenAPI:** [openapi/alloy-automation-embedded.yaml](openapi/alloy-automation-embedded.yaml)
- **JSON Schema:** [json-schema/alloy-embedded-user-schema.json](json-schema/alloy-embedded-user-schema.json)
- **JSON-LD Context:** [json-ld/alloy-automation-embedded-context.jsonld](json-ld/alloy-automation-embedded-context.jsonld)
- **Capability:** [capabilities/shared/embedded.yaml](capabilities/shared/embedded.yaml)

### Alloy Automation Connectivity API

Build native integration UIs with a single endpoint. Discover connectors, configure credentials, and execute actions across 1000+ third-party applications.

- **Documentation:** [https://docs.runalloy.com/connectivity-api/quick-start](https://docs.runalloy.com/connectivity-api/quick-start)
- **Base URL:** `https://production.runalloy.com`
- **OpenAPI:** [openapi/alloy-automation-connectivity.yaml](openapi/alloy-automation-connectivity.yaml)
- **JSON Schema:** [json-schema/alloy-connectivity-connector-schema.json](json-schema/alloy-connectivity-connector-schema.json)
- **JSON-LD Context:** [json-ld/alloy-automation-connectivity-context.jsonld](json-ld/alloy-automation-connectivity-context.jsonld)
- **Capability:** [capabilities/shared/connectivity.yaml](capabilities/shared/connectivity.yaml)

### Alloy Automation Unified API

Access-based app integrations across commerce, CRM, ERP, and other categories through a single standardized interface.

- **Documentation:** [https://docs.runalloy.com/unified-api/1.0.0/getting-started/quick-start/](https://docs.runalloy.com/unified-api/1.0.0/getting-started/quick-start/)

## Generated Artifacts

| Directory | Count | Description |
|-----------|-------|-------------|
| `openapi/` | 2 | OpenAPI 3.0.3 specifications |
| `json-schema/` | 31 | JSON Schema (draft 2020-12) files |
| `json-structure/` | 31 | JSON Structure documentation files |
| `json-ld/` | 2 | JSON-LD 1.1 context files |
| `examples/` | 31 | Example JSON files |
| `capabilities/shared/` | 2 | Per-API Naftiko capability definitions |
| `capabilities/` | 1 | Workflow capability composition |
| `rules/` | 1 | Spectral ruleset (15 rules) |
| `vocabulary/` | 1 | Domain vocabulary and taxonomy |

## Authentication

All APIs use Bearer API Key authentication:

```
Authorization: bearer YOUR_API_KEY
x-api-version: 2025-09
```

API keys are generated in the Alloy Dashboard → Settings → API Keys.

## API Patterns

- **JWT Tokens:** Server generates short-lived JWTs via `GET /users/{userId}/token` for frontend SDK auth
- **Connector Actions:** Discover → get schema → create credential → execute action
- **Workflow Lifecycle:** Activate, deactivate, and upgrade workflows per user

## SDKs

- [Node.js SDK](https://github.com/alloy-automation/alloy-node)
- [Python SDK](https://github.com/alloy-automation/alloy-python)

## Maintainer

Kin Lane — kin@apievangelist.com
