---
name: Register an eNACH / UPI Autopay recurring-debit mandate
description: Create an NPCI eNACH / NACH / UPI Autopay mandate authorizing recurring debit, track registration to a UMRN, and cancel when done.
api: openapi/digio-openapi.yml
operations: [createMandate, getMandate, cancelMandate]
---

# Register a recurring-debit mandate (DigiCollect / eNACH)

Use Digio's DigiCollect product to authorize recurring debits via NPCI eNACH, physical NACH, or UPI Autopay.

## Auth
- HTTP Basic: `Authorization: Basic Base64(client_id:client_secret)`, `Content-Type: application/json`.

## Steps
1. **Create the mandate.** Call `createMandate` with `customer_identifier` (email/phone), `auth_mode` (`netbanking` | `debit_card` | `aadhaar` | `upi`), `maximum_amount`, `frequency` (`Adhoc` | `Monthly` | `Quarterly` | `Yearly`), and collection dates. The response is a `Mandate`.
2. **Track registration.** Poll `getMandate` with the `mandate_id` (or use the `mandate.register.*` webhooks). Watch `state` (`register_initiated` -> `register_success` | `register_failed`). On success, capture `umrn` (the NPCI Unique Mandate Reference Number) — it is the durable reference for downstream debits.
3. **Cancel.** Call `cancelMandate` with the `mandate_id` to revoke an active mandate.

## Rules
- A mandate authorizes money movement — this is a high-consequence action; require human confirmation and audit it (`agentic-access/digio-agentic-access.yml`).
- Store `mandate_id` and `umrn`; do not retry `createMandate` blindly (no documented idempotency).
- On `401`, verify environment-correct Basic credentials (`errors/digio-problem-types.yml`).
