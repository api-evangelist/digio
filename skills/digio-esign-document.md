---
name: Collect a legally-valid eSignature on a document
description: Upload a PDF, request an Aadhaar/OTP/DSC signature from one or more signers, poll for completion, and download the signed document.
api: openapi/digio-openapi.yml
operations: [uploadDocumentForSign, uploadPdfForSign, getDocument, downloadSignedDocument]
---

# Collect a legally-valid eSignature (DigiSign)

Use Digio's DigiSign product to collect legally-valid Aadhaar, OTP, or DSC electronic signatures.

## Auth
- HTTP Basic: `Authorization: Basic Base64(client_id:client_secret)`, `Content-Type: application/json`.
- Use the sandbox host `https://ext.digio.in` for testing, `https://api.digio.in` in production. Credentials are environment-scoped (see `sandbox/digio-sandbox.yml`).

## Steps
1. **Create the sign request.** Call `uploadDocumentForSign` (multipart/base64 file via `file_data`) or `uploadPdfForSign` with the `signers[]` array — each signer needs an `identifier` (email or phone) and optional `sign_type` (`aadhaar` | `electronic` | `dsc`). The response is a `SignDocument` with an `id` prefixed `DID`.
2. **Track status.** Poll `getDocument` with the `document_id`, or subscribe to the `doc.signed` / `doc.sign.failed` webhooks (`asyncapi/digio-webhooks.yml`) instead of polling. Watch `agreement_status` (`requested` -> `completed` | `expired`) and per-party `signing_parties[].status`.
3. **Download.** Once `agreement_status` is `completed`, call `downloadSignedDocument` with the `document_id` to retrieve the signed PDF (`application/pdf`).

## Rules
- This creates a legally-binding signature — treat it as a write/high-consequence action and confirm with a human before sending (`agentic-access/digio-agentic-access.yml`).
- On `401`, re-check the environment-correct Basic credentials (`errors/digio-problem-types.yml`).
- Digio does not document idempotency; persist the returned `DID` so you never create a duplicate request.
