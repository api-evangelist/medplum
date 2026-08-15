---
name: Upsert a patient by identifier
description: Search for a Patient by a business identifier and update it if found, otherwise create it — the safe re-run pattern for integrations.
api: openapi/medplum-fhir-api-openapi.yml
operations: [search, updateResource, createResource]
---

# Upsert a patient by identifier

Grounded in `search` (`GET /fhir/R4/{resourceType}`), `updateResource` (`PUT /fhir/R4/{resourceType}/{id}`), and `createResource` (`POST /fhir/R4/{resourceType}`).

## Steps

1. **Search** `GET /fhir/R4/Patient?identifier=<system>|<value>` to check whether a Patient with this business identifier already exists.
2. **If found** (a `Bundle` with `total >= 1`): take the matched `Patient.id` and call `updateResource` — `PUT /fhir/R4/Patient/<id>` with the full updated resource body. `updateResource` is naturally idempotent: repeating the identical PUT produces the identical resulting state (see `conventions/medplum-conventions.yml`).
3. **If not found** (`total: 0`): call `createResource` — `POST /fhir/R4/Patient` with the new resource, including the same identifier so a future upsert can match it.

## Why not conditional-update in one call?

FHIR conditional update (`PUT /fhir/R4/Patient?identifier=<system>|<value>`) does the search-then-create-or-update in a single request. Prefer the explicit two-step pattern above unless you have confirmed conditional-update is enabled for your Project — it is not separately documented as a guaranteed feature in this pass, so this skill uses the operations that are directly confirmed in the OpenAPI.

## Error handling

A `409 Conflict` on step 2 means an `If-Match` version precondition failed (someone else updated the resource between your search and your update) — re-fetch and retry. See `errors/medplum-problem-types.yml`.
