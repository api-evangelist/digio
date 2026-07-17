---
name: Run a DigiKYC identity-verification workflow
description: Start a template-driven KYC workflow (Aadhaar offline, DigiLocker, CKYC, KRA, Video KYC), then fetch the collected identity data and verification result.
api: openapi/digio-openapi.yml
operations: [createKycRequest, getKycResponse]
---

# Run a KYC workflow (DigiKYC)

Use Digio's DigiKYC product to verify a customer's identity via a pre-configured workflow template.

## Auth
- HTTP Basic: `Authorization: Basic Base64(client_id:client_secret)`, `Content-Type: application/json`.

## Steps
1. **Create the KYC request.** Call `createKycRequest` with `customer_identifier` (email/phone), `customer_name`, and `template_name` (the DigiKYC workflow — e.g. offline Aadhaar, DigiLocker, ID proof, CKYC, KRA, Video KYC). Set `notify_customer: true` to have Digio send the customer the journey link. The response `KycResponse` has an `id` prefixed `KID`.
2. **Fetch the result.** Poll `getKycResponse` with the `request_id` (or use the `kyc.approved` / `kyc.rejected` webhooks). Watch `status` (`requested` -> `approval_pending` -> `approved` | `rejected`) and read the extracted fields from `actions[]`.

## Rules
- KYC handles regulated personal identity data (Aadhaar/PAN) — collect only with consent and treat responses as sensitive.
- Persist the returned `KID`; do not re-create a request for the same customer without checking existing status.
- On `401`, verify environment-correct Basic credentials (`errors/digio-problem-types.yml`).
