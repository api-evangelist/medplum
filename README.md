# Medplum (medplum)

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

Medplum is an Apache 2.0 open-source, FHIR-native developer platform for shipping clinical software. It bundles a FHIR R4 datastore, REST and GraphQL APIs, a TypeScript SDK, React component library, OAuth 2.0 / SMART on FHIR authentication, declarative Access Policies, Subscriptions, and TypeScript-based serverless Bots — sold as a hosted service at `api.medplum.com` and as a self-hostable monorepo on GitHub. Medplum is HIPAA, SOC 2 Type II, and ONC-certified.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/medplum/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **License:** Apache 2.0
- **Governance:** Medplum Inc. (commercial-open-source)
- **Primary Language:** TypeScript

## Tags

Healthcare, FHIR, Open Source, Developer Platform, HIPAA, SMART on FHIR, Clinical, Interoperability

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Medplum FHIR REST API

FHIR R4 REST API exposed at `https://api.medplum.com/fhir/R4`. Supports the full generic FHIR resource surface — create, read, update, patch, delete, search, history, and version-read — across every FHIR R4 resource type, with US Core, SMART App Launch, and Bulk Data 2.0 conformance.

- **Human URL:** [https://www.medplum.com/docs/api](https://www.medplum.com/docs/api)
- **Base URL:** `https://api.medplum.com/fhir/R4`

#### Properties

- [Documentation](https://www.medplum.com/docs/api)
- [APIReference](https://www.medplum.com/docs/api)
- [OpenAPI](openapi/medplum-openapi-original.yml)
- [Authentication](https://www.medplum.com/docs/auth)
- [RateLimits](https://www.medplum.com/docs/rate-limits)
- JSON Schema: [Patient](json-schema/medplum-patient-schema.json), [Observation](json-schema/medplum-observation-schema.json), [Encounter](json-schema/medplum-encounter-schema.json), [Practitioner](json-schema/medplum-practitioner-schema.json), [Organization](json-schema/medplum-organization-schema.json), [Condition](json-schema/medplum-condition-schema.json), [MedicationRequest](json-schema/medplum-medicationrequest-schema.json), [Subscription](json-schema/medplum-subscription-schema.json)
- JSON Structure: [Patient](json-structure/medplum-patient-structure.json)
- Examples: [Create Patient](examples/medplum-patient-create-example.json), [Blood Pressure Observation](examples/medplum-observation-bloodpressure-example.json), [Subscription Webhook](examples/medplum-subscription-webhook-example.json)
- Naftiko Capability: [medplum-fhir-rest.yaml](capabilities/medplum-fhir-rest.yaml)

### Medplum GraphQL API

FHIR-aware GraphQL endpoint at `https://api.medplum.com/fhir/R4/$graphql`. Supports typed nested queries, reverse-reference traversal (`_reference`), FHIRPath-style array filtering, and access-policy enforcement at the field level.

- **Human URL:** [https://www.medplum.com/docs/graphql](https://www.medplum.com/docs/graphql)
- **Base URL:** `https://api.medplum.com/fhir/R4/$graphql`

#### Properties

- [Documentation](https://www.medplum.com/docs/graphql)
- Example: [Patient query](examples/medplum-graphql-patient-query-example.json)
- Naftiko Capability: [medplum-graphql.yaml](capabilities/medplum-graphql.yaml)

### Medplum Bots

TypeScript serverless functions (AWS Lambda-style) executed in response to FHIR Subscriptions, HTTP triggers, or scheduled cron. Bots are the backbone of Medplum integrations — HL7v2 to FHIR conversion, document generation, webhook fan-out, and questionnaire-driven workflow automation.

- **Human URL:** [https://www.medplum.com/docs/bots](https://www.medplum.com/docs/bots)

#### Properties

- [Documentation](https://www.medplum.com/docs/bots)
- [JSON Schema (Bot)](json-schema/medplum-bot-schema.json)
- Example: [HL7v2 to FHIR Bot](examples/medplum-bot-hl7-to-fhir-example.json)
- Naftiko Capability: [medplum-bots.yaml](capabilities/medplum-bots.yaml)

### Medplum Subscriptions

FHIR Subscription resources that match search criteria and dispatch real-time notifications via REST hooks (webhooks) or Websockets when matching resources change. Subscriptions are the primary trigger for Bots and external system integrations.

- **Human URL:** [https://www.medplum.com/docs/subscriptions](https://www.medplum.com/docs/subscriptions)

#### Properties

- [Documentation](https://www.medplum.com/docs/subscriptions)
- Example: [Subscription Webhook](examples/medplum-subscription-webhook-example.json)

## Common Properties

- [Website](https://www.medplum.com)
- [Documentation](https://www.medplum.com/docs)
- [Getting Started](https://www.medplum.com/docs/tutorials)
- [API Reference](https://www.medplum.com/docs/api)
- [Authentication](https://www.medplum.com/docs/auth)
- SDK: [@medplum/core](https://www.npmjs.com/package/@medplum/core), [@medplum/react](https://www.npmjs.com/package/@medplum/react), [Core SDK docs](https://www.medplum.com/docs/sdk/core)
- [CLI](https://www.medplum.com/docs/cli)
- [Console](https://app.medplum.com)
- [Pricing](https://www.medplum.com/pricing)
- [Terms of Service](https://www.medplum.com/terms)
- [Privacy Policy](https://www.medplum.com/privacy)
- [Blog](https://www.medplum.com/blog)
- [GitHub Organization](https://github.com/medplum)
- [GitHub Repository](https://github.com/medplum/medplum)
- [Discord](https://discord.gg/medplum)
- [License (Apache 2.0)](https://www.apache.org/licenses/LICENSE-2.0)
- [Spectral Rules](rules/medplum-rules.yml)
- [Vocabulary](vocabulary/medplum-vocabulary.yml)
- [JSON-LD Context](json-ld/medplum-context.jsonld)
- [Plans & Pricing](plans/medplum-plans-pricing.yml)
- [Rate Limits](rate-limits/medplum-rate-limits.yml)
- [FinOps](finops/medplum-finops.yml)

## Features

- **FHIR-Native Datastore** — PostgreSQL-backed datastore that natively models FHIR R4 resources, including search, history, and versioning.
- **REST + GraphQL APIs** — Dual API surface sharing the same authorization, schema, and access policies.
- **Bots** — AWS Lambda-style TypeScript functions executed by Subscriptions, HTTP, or cron; the integration backbone of Medplum.
- **Subscriptions** — FHIR Subscription resources dispatch real-time notifications when matching resources change.
- **Access Policies** — Declarative resource- and field-level authorization rules attached to ProjectMembership.
- **SMART on FHIR + OAuth 2.0** — Standards-based authentication; supports SMART App Launch 2.0.0 and Bulk Data 2.0.0.
- **TypeScript SDK and React Components** — `@medplum/core`, `@medplum/react`, `@medplum/react-hooks`.
- **On-Premise Agent** — Bridges local clinical systems (HL7v2, DICOM, MLLP) to Medplum cloud.
- **AWS CDK Deployment** — First-class CDK constructs for self-hosting on AWS.

## Use Cases

- Custom EHR development
- Patient engagement portals
- AI scribe and clinical documentation
- HL7v2 to FHIR integration
- Population health and analytics
- Care management workflows
- Revenue cycle automation

## Integrations

AWS, HL7v2, FHIRcast, Stripe, Twilio, DocuSeal / DocuSign, SendGrid / Mailgun, AWS HealthLake.

## Solutions

Custom EHR, Patient Portal, Provider Portal, AI-Powered Clinical Scribe, Population Health Platform, Revenue Cycle Management.

## Maintainers

- **Kin Lane** — kin@apievangelist.com
