# Medplum

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

Medplum is an Apache 2.0 open-source, FHIR-native developer platform for shipping clinical software. It bundles a FHIR R4 datastore, REST and GraphQL APIs, a TypeScript SDK, React component library, OAuth 2.0 / SMART on FHIR authentication, declarative Access Policies, Subscriptions, and TypeScript-based serverless Bots — sold as a hosted service at api.medplum.com and as a self-hostable monorepo on GitHub. Medplum is HIPAA, SOC 2 Type II, and ONC-certified.

**Areas:** Healthcare · FHIR · Open Source · Developer Platform · HIPAA · SMART on FHIR · Clinical · Interoperability

## Medplum on APIs.io

Everything profiled for Medplum is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/medplum/](https://apis.io/providers/medplum/)** — or go straight to one of the APIs or properties below.

### APIs (4)

- [Medplum GraphQL API](https://apis.io/apis/medplum/medplum-graphql-api/) — FHIR-aware GraphQL endpoint at https://api.medplum.com/fhir/R4/$graphql. Supports typed nested queries, reverse-reference traversal (_reference),…
- [Medplum Bots](https://apis.io/apis/medplum/medplum-bots/) — Bots are TypeScript serverless functions (AWS Lambda-style) executed in response to FHIR Subscriptions, HTTP triggers, or scheduled cron. Bots are the…
- [Medplum Subscriptions](https://apis.io/apis/medplum/medplum-subscriptions/) — FHIR Subscription resources that match a search criteria and dispatch real-time notifications via REST hooks (webhooks) or Websockets when matching…
- [Medplum Fhir API](https://apis.io/apis/medplum/medplum-fhir-api/) — Medplum's FHIR R4 REST API, as described by its own OpenAPI (https://api.medplum.com/openapi.json): batch/transaction, search, create (incl. conditional…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (11)

Multi-step workflows that chain operations into a business task.

- [Medplum Amend Resource With History](https://apis.io/arazzos/medplum/medplum-amend-resource-with-history-workflow/)
- [Medplum Clinical Data Query](https://apis.io/arazzos/medplum/medplum-clinical-data-query-workflow/)
- [Medplum Create Diagnostic Report](https://apis.io/arazzos/medplum/medplum-create-diagnostic-report-workflow/)
- [Medplum Deploy Bot](https://apis.io/arazzos/medplum/medplum-deploy-and-run-bot-workflow/)
- [Medplum FHIR Resource CRUD](https://apis.io/arazzos/medplum/medplum-fhir-resource-crud-workflow/)
- [Medplum Finalize Observation](https://apis.io/arazzos/medplum/medplum-finalize-observation-workflow/)
- [Medplum Find And Delete Resource](https://apis.io/arazzos/medplum/medplum-find-and-delete-resource-workflow/)
- [Medplum Register Patient With Observation](https://apis.io/arazzos/medplum/medplum-register-patient-with-observation-workflow/)
- [Medplum FHIR Resource Versioning](https://apis.io/arazzos/medplum/medplum-resource-versioning-workflow/)
- [Medplum Schedule Encounter](https://apis.io/arazzos/medplum/medplum-schedule-encounter-workflow/)
- [Medplum Upsert Patient](https://apis.io/arazzos/medplum/medplum-upsert-patient-workflow/)

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Medplum Webhooks](https://apis.io/asyncapis/medplum/medplum-webhooks/)

#### GraphQL (1)

GraphQL schemas.

- [Medplum GraphQL API](https://apis.io/graphqls/medplum/medplum-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Medplum MCP Server](https://apis.io/servers/medplum/medplum-mcp-server/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Medplum Agentic Access](https://apis.io/agentic-access/medplum/medplum-agentic-access/)

#### JSON Schema (9)

The data models the API reads and writes.

- [Bot](https://apis.io/schemas/medplum/medplum-bot/)
- [Condition](https://apis.io/schemas/medplum/medplum-condition/)
- [Encounter](https://apis.io/schemas/medplum/medplum-encounter/)
- [MedicationRequest](https://apis.io/schemas/medplum/medplum-medicationrequest/)
- [Observation](https://apis.io/schemas/medplum/medplum-observation/)
- [Organization](https://apis.io/schemas/medplum/medplum-organization/)
- [Patient](https://apis.io/schemas/medplum/medplum-patient/)
- [Practitioner](https://apis.io/schemas/medplum/medplum-practitioner/)
- [Subscription](https://apis.io/schemas/medplum/medplum-subscription/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Medplum Patient Structure](https://apis.io/json-structure/medplum/medplum-patient-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Medplum Context](https://apis.io/jsonld/medplum/medplum-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Medplum Vocabulary](https://apis.io/vocabularies/medplum/medplum-vocabulary/)

#### Examples (5)

Example requests and responses.

- [Medplum Bot Hl7 To Fhir Example](https://apis.io/examples/medplum/medplum-bot-hl7-to-fhir-example/)
- [Medplum Graphql Patient Query Example](https://apis.io/examples/medplum/medplum-graphql-patient-query-example/)
- [Medplum Observation Bloodpressure Example](https://apis.io/examples/medplum/medplum-observation-bloodpressure-example/)
- [Medplum Patient Create Example](https://apis.io/examples/medplum/medplum-patient-create-example/)
- [Medplum Subscription Webhook Example](https://apis.io/examples/medplum/medplum-subscription-webhook-example/)

#### Collections (2)

Postman and Open Collection request collections.

- [Medplum - OpenAPI 3.0 Fhir API](https://apis.io/collections/medplum/open-medplum-fhir-api/)
- [Medplum - OpenAPI 3.0](https://apis.io/collections/medplum/postman-medplum-openapi-original/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Medplum Fhir Api Overlay](https://apis.io/overlays/medplum/medplum-fhir-api-overlay/)
- [Medplum Fhir Api Phrasing Overlay](https://apis.io/overlays/medplum/medplum-fhir-api-phrasing-overlay/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Medplum — jsonschema rules](https://apis.io/rules/medplum/medplum-jsonschema-spectral-rules/)
- [Medplum API Rules](https://apis.io/rules/medplum/medplum-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Medplum Authentication](https://apis.io/security/medplum/medplum-authentication/)
- [Medplum Domain Security](https://apis.io/security/medplum/medplum-domain-security/)
- [Medplum Trust Center](https://apis.io/security/medplum/medplum-trust-center/)
- [Medplum Vulnerability Disclosure](https://apis.io/security/medplum/medplum-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Medplum Scopes](https://apis.io/scopes/medplum/medplum-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Medplum Plans Pricing](https://apis.io/plans/medplum/medplum-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Medplum Rate Limits](https://apis.io/rate-limits/medplum/medplum-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Medplum Finops](https://apis.io/finops/medplum/medplum-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.medplum.com)
- [Documentation](https://www.medplum.com/docs)
- [Getting started](https://www.medplum.com/docs/tutorials)
- [API reference](https://www.medplum.com/docs/api)
- [Pricing](https://www.medplum.com/pricing)
- [Blog](https://www.medplum.com/blog)
- [Compliance](https://www.medplum.com/docs/compliance)
- [Terms of service](https://www.medplum.com/terms)
- [Privacy policy](https://www.medplum.com/privacy)
- [GitHub](https://github.com/medplum)
- [Status](https://status.medplum.com)

## API Evangelist rating

**Kin Score 71.7** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 66.7 |
| Contract quality | 74.1 |
| Contract governance | 35.6 |
| Operational transparency | 73.7 |
| Developer ergonomics | 74.4 |
| Access clarity | 55.3 |

**Agent readiness 55.8** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 57.8** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/medplum/](https://apis.io/providers/medplum/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Medplum: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/medplum/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
