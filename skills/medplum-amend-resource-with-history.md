---
name: Amend a resource and inspect its version history
description: Read a FHIR resource, update it, then read its version history and a specific prior version — the audit-friendly amendment pattern.
api: openapi/medplum-fhir-api-openapi.yml
operations: [readResource, updateResource, readResourceHistory, readVersion]
---

# Amend a resource and inspect its version history

Grounded in `readResource` (`GET /fhir/R4/{resourceType}/{id}`), `updateResource` (`PUT /fhir/R4/{resourceType}/{id}`), `readResourceHistory` (`GET /fhir/R4/{resourceType}/{id}/_history`), and `readVersion` (`GET /fhir/R4/{resourceType}/{id}/_history/{versionId}`).

## Steps

1. **Read** the current resource: `GET /fhir/R4/{resourceType}/{id}`. Note `meta.versionId` and `meta.lastUpdated`.
2. **Amend it.** Modify the fields that need correcting, then `PUT /fhir/R4/{resourceType}/{id}` with the full updated body. Medplum increments `meta.versionId` automatically — this is not a destructive overwrite; every prior version stays queryable.
3. **List the history.** `GET /fhir/R4/{resourceType}/{id}/_history` returns a `Bundle` of every version, newest first.
4. **Read a specific prior version** (e.g. to show what changed, or for an audit trail): `GET /fhir/R4/{resourceType}/{id}/_history/{versionId}` using a `versionId` from step 3.

## Why this matters for healthcare data

Regulatory and clinical-audit requirements (and Medplum's own ONC/HIPAA compliance posture — see `conformance/medplum-conformance.yml`) frequently require showing *what a record said at a point in time*, not just its current state. This resource-history pattern is the FHIR-native way to answer that without a separate audit table.

## Error handling

A `410 Gone` on step 1 means the resource has been deleted — its history is still retrievable via step 3/4 even though `readResource` on the current id now fails. See `errors/medplum-problem-types.yml`.
