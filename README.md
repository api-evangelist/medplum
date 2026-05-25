# Medplum (medplum)

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
