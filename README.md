# Scalar (scalar-api)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Scalar is an open-source (MIT) API platform built on the OpenAPI standard. Its core is a self-hostable **API Reference** renderer that turns an OpenAPI or AsyncAPI document into a beautiful, interactive reference with a built-in request-testing tool, plus a fully open-source, offline-first **API Client** (a Postman/Insomnia alternative available as a desktop app and in the browser). On top of the open-source components Scalar runs a hosted SaaS platform (`dashboard.scalar.com`) providing an **API Registry** that stores and versions OpenAPI documents behind a public read CDN (`registry.scalar.com`), a **Docs** product for developer portals with Git Sync and Markdown/MDX, **SDK generation** for TypeScript, Python, Go, Java, PHP, C#, and Ruby, **hosted MCP servers**, and an **AI Agent** for chatting with APIs. Scalar is the default API documentation UI for many frameworks (FastAPI, Hono, Elysia, NestJS, Laravel, and others).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/scalar-api/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/scalar-api/refs/heads/main/apis.yml)

## Access Model (Read This First)

Scalar is primarily **open-source components + a hosted SaaS platform**, not a single public REST API:

- **Open source (MIT), self-hosted:** the API Reference renderer, the API Client, the CLI, the OpenAPI parser, the mock server, and the Galaxy example API — [github.com/scalar/scalar](https://github.com/scalar/scalar). These are libraries/apps you run yourself, not network services Scalar exposes.
- **Confirmed public HTTP surfaces:** the registry **read CDN** serves published OpenAPI documents over HTTPS at `registry.scalar.com/@{namespace}/apis/{slug}` (append `?format=json` or `?format=yaml`), and the **Galaxy** example API is a live REST API at `galaxy.scalar.com`.
- **No fully documented public REST management API.** Registry publish/list/update/delete and docs deployment are performed through the authenticated **Scalar CLI** (`scalar registry ...`, API-key auth), which wraps the platform's internal API. Where this catalog lists management endpoints (OpenAPI + collections), they are **modeled (`endpointsModeled`)** from CLI behavior, not officially documented HTTP contracts.

## Tags

- API Documentation
- API Client
- Open Source
- Developer Tools
- API Reference
- OpenAPI

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### Scalar API Reference

Open-source (MIT) renderer that turns an OpenAPI/Swagger or AsyncAPI document into an interactive API reference with a built-in request-testing panel and multi-language code samples. Embeds from a single HTML file or the `@scalar/api-reference` npm package. Self-hosted component (`endpointsModeled`).

- **Human URL:** [https://guides.scalar.com/scalar/scalar-api-references/getting-started](https://guides.scalar.com/scalar/scalar-api-references/getting-started)

### Scalar API Client

Fully open-source, offline-first API client built on the OpenAPI standard — a Postman/Insomnia alternative for sending REST, GraphQL, and WebSocket requests, organizing collections and environments, and running collection runners. Desktop (Windows, macOS, Linux) and browser. Consumer-side developer tool (`endpointsModeled`).

- **Human URL:** [https://guides.scalar.com/scalar/scalar-api-client/getting-started](https://guides.scalar.com/scalar/scalar-api-client/getting-started)

### Scalar Registry API

Hosted registry that stores and versions OpenAPI documents. Published documents are served over a public HTTPS read CDN in the form `registry.scalar.com/@{namespace}/apis/{slug}`. Publishing/updating/deleting is done through the authenticated Scalar CLI; management operations are modeled here (`endpointsModeled`).

- **Human URL:** [https://guides.scalar.com/scalar/scalar-registry/getting-started](https://guides.scalar.com/scalar/scalar-registry/getting-started)
- **Base URL:** `https://registry.scalar.com`
- **Properties:** [OpenAPI](openapi/scalar-api-openapi.yml) · [Postman Collection](collections/scalar-api.postman_collection.json) · [Open Collection](collections/scalar-api.opencollection.json)

### Scalar Docs Platform

Hosted developer-portal product combining Markdown/MDX guides with generated API references, custom domains, themes, versions, and two-way Git Sync from GitHub. Hosted SaaS surface (`endpointsModeled`).

- **Human URL:** [https://guides.scalar.com/scalar/scalar-docs/getting-started](https://guides.scalar.com/scalar/scalar-docs/getting-started)

### Scalar CLI

Open-source `@scalar/cli` for validating and linting OpenAPI documents (Spectral rules), previewing references, and publishing/listing/updating/deleting registry documents. Authenticates with a Scalar API key. Command-line surface (`endpointsModeled`).

- **Human URL:** [https://guides.scalar.com/scalar/scalar-registry/cli](https://guides.scalar.com/scalar/scalar-registry/cli)

### Scalar SDK Generation

Hosted SDK generation producing type-safe client libraries from an OpenAPI document for TypeScript, Python, Go, Java, PHP, C#, and Ruby, kept in sync with the registry. Paid per-language add-on (`endpointsModeled`).

- **Human URL:** [https://scalar.com/products/sdks](https://scalar.com/products/sdks)

### Scalar Agent and MCP

AI layer that lets developers chat with an API inside the docs and exposes hosted MCP servers generated from an OpenAPI document. Metered in Agent Scalar credits (`endpointsModeled`).

- **Human URL:** [https://scalar.com/products/agent](https://scalar.com/products/agent)

### Scalar Galaxy API

Scalar Galaxy is Scalar's live, fictional example REST API (planets, celestial bodies, users, authentication) published as an OpenAPI 3.1.1 document and served at `galaxy.scalar.com`. A real, publicly reachable REST API used to test OpenAPI tooling and demo the API Reference and API Client.

- **Human URL:** [https://galaxy.scalar.com](https://galaxy.scalar.com)
- **Base URL:** `https://galaxy.scalar.com`
- **OpenAPI:** [https://registry.scalar.com/@scalar/apis/galaxy?format=json](https://registry.scalar.com/@scalar/apis/galaxy?format=json)

## Common Properties

- [Authentication](authentication/scalar-api-authentication.yml)
- [GitHub Organization](https://github.com/scalar)
- [LinkedIn](https://www.linkedin.com/company/scalar-com)
- [Website](https://scalar.com)
- [Documentation](https://guides.scalar.com)
- [Plans](plans/scalar-api-plans-pricing.yml)
- [Rate Limits](rate-limits/scalar-api-rate-limits.yml)
- [Fin Ops](finops/scalar-api-finops.yml)
- [Blog](https://scalar.com/blog)

## Pricing (captured 2026-07-11, verify at scalar.com/pricing)

- **Open Source (self-hosted):** free (MIT) — renderer, API Client, CLI, parser, Galaxy.
- **Free:** $0 — hosted docs, built-in API client, 1 editor seat, unlimited viewers, up to 3 APIs in registry, 50 Agent credits.
- **Pro:** $72/month — custom domains, Git Sync, MDX, hosted MCP, GitHub workflows, unlimited editors, private + public registry, 500 Agent credits.
- **SDK add-on:** ~$100 per language.
- **Enterprise:** custom — SSO/SAML, RBAC, SLAs, migration services.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
