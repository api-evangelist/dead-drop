# Dead Drop (dead-drop)

Privacy-focused, ephemeral data-sharing API with zero-knowledge encryption. Open source under MIT, built on Cloudflare Workers, Hono, and Cloudflare D1.

- **Live site:** https://dead-drop.xyz
- **Production API:** `https://api.dead-drop.xyz/api/v1`
- **Documentation:** https://davorinrusevljan.github.io/dead-drop/
- **API reference (latest):** https://davorinrusevljan.github.io/dead-drop/latest/
- **OpenAPI:** https://davorinrusevljan.github.io/dead-drop/latest/openapi.json
- **GitHub (upstream):** https://github.com/davorinrusevljan/dead-drop
- **License:** MIT
- **api-search issue:** [#24](https://github.com/api-search/network/issues/24)

## Profile

- **Type:** opensource
- **Reconciled:** false (open source, no commercial offering surfaced)
- **Tags:** Messaging, Privacy, Anonymous, Open Source
- **Stack:** Cloudflare Workers, Hono, Cloudflare D1, Next.js, TypeScript, pnpm/Turbo monorepo
- **Topics:** api, cloudflare-workers, cloudflare-d1, hono, nextjs, openapi, encryption, ephemeral, privacy, zero-knowledge

## Features

- Free tier drops: 10KB payload, 7-day lifespan, text only
- Deep tier drops: 4MB payload, 90-day lifespan
- Zero-knowledge encryption: AES-256-GCM with PBKDF2-derived keys, content encrypted client-side
- Public and private drop visibility
- Version history (up to 5 versions retained per drop)
- EFF Diceware random 4-word kebab-case drop names
- SHA-256 hashed drop identifiers

## Operations

| Method | Path                                | Summary                            |
| ------ | ----------------------------------- | ---------------------------------- |
| GET    | `/health`                           | Health Check                       |
| GET    | `/drops/generate-name`              | Generate a Random Unused Drop Name |
| GET    | `/drops/check/{id}`                 | Check if a Drop Name Is Available  |
| POST   | `/drops`                            | Create a New Drop                  |
| GET    | `/drops/{id}`                       | Retrieve a Drop                    |
| PUT    | `/drops/{id}`                       | Update a Drop                      |
| DELETE | `/drops/{id}`                       | Delete a Drop                      |
| GET    | `/drops/{id}/history`               | List Drop History                  |
| GET    | `/drops/{id}/history/{version}`     | Get Specific Drop Version          |

## Artifacts

- [`apis.yml`](apis.yml) — APIs.yml profile
- [`openapi/dead-drop-openapi.yml`](openapi/dead-drop-openapi.yml) — OpenAPI 3.1 spec
- [`examples/`](examples) — request/response examples for each operation
- [`json-schema/`](json-schema) — JSON Schema for Drop, Drop Version, and Error envelope
- [`json-structure/`](json-structure) — JSON Structure for the Drop resource
- [`json-ld/dead-drop-context.jsonld`](json-ld/dead-drop-context.jsonld) — JSON-LD context
- [`vocabulary/dead-drop-vocabulary.yml`](vocabulary/dead-drop-vocabulary.yml) — domain vocabulary
- [`rules/dead-drop-rules.yml`](rules/dead-drop-rules.yml) — Spectral ruleset
- [`capabilities/ephemeral-messaging.yaml`](capabilities/ephemeral-messaging.yaml) — Naftiko capability

## Notes

This is an open-source project. No commercial offering, no published plans, rate limits, or FinOps data — `reconciled: false`. Hosted reference deployment is at `dead-drop.xyz`; subject to its terms of service.
