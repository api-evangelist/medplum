---
name: Register a patient and record a vital-sign observation
description: Create a FHIR Patient resource, then create an Observation referencing that patient — the core Medplum intake-to-vitals flow.
api: openapi/medplum-fhir-api-openapi.yml
operations: [createResource]
---

# Register a patient and record a vital-sign observation

Grounded in `createResource` (`POST /fhir/R4/{resourceType}`) — the only operation this flow needs, called twice.

## Steps

1. **Authenticate** with a Bearer JWT (SMART on FHIR / OAuth 2.0 — see `authentication/medplum-authentication.yml` and `scopes/medplum-scopes.yml` for the scope required, e.g. `user/Patient.c` and `user/Observation.c`).
2. **Create the Patient.** `POST /fhir/R4/Patient` with a FHIR `Patient` resource body (name, birthDate, etc.). If the patient may already exist, use a **conditional create** (`ifNoneExist` parameter, e.g. `identifier=<mrn-system>|<mrn-value>`) instead of a plain create — this is Medplum's idempotency mechanism for creates (see `conventions/medplum-conventions.yml`). Capture the returned `Patient.id`.
3. **Create the Observation.** `POST /fhir/R4/Observation` with `subject: { reference: "Patient/<id>" }`, a `code` (LOINC-coded vital sign), and a `valueQuantity`. Set `status` to `final` if the value is confirmed, or `preliminary` otherwise (see the companion `medplum-finalize-observation` skill for status transitions).

## Error handling

Medplum returns errors as FHIR `OperationOutcome` resources (`issue[].severity/code/details`), not RFC 9457 `application/problem+json` — see `errors/medplum-problem-types.yml`. A `422` means the resource failed FHIR structural/profile validation; check `issue[].details.text` for the failing element.

## Rate limits

Both calls count against the per-IP request-count limit AND the per-user/project weighted `fhirInteractions` limit (a `create` costs 100 points vs. 1 for a `read`) — see `rate-limits/medplum-rate-limits.yml`. Watch the `RateLimit` response header for remaining budget.
