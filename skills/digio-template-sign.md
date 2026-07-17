---
name: Generate a document from a template and collect eSign
description: Use a DigiDocs template (with optional eStamp) to generate an agreement and create an eSign request in one call, then track and download it.
api: openapi/digio-openapi.yml
operations: [createSignRequestFromTemplate, getDocument, downloadSignedDocument]
---

# Template document + eSign (DigiDocs)

Use Digio's DigiDocs product to generate an agreement from a template (with optional state-specific eStamp) and route it straight into an eSign request.

## Auth
- HTTP Basic: `Authorization: Basic Base64(client_id:client_secret)`, `Content-Type: application/json`.

## Steps
1. **Generate + request signature.** Call `createSignRequestFromTemplate` with `template_id`, a `template_values` object (the merge fields for the template), and the `signers[]` array. This produces the document and an eSign request in one call, returning a `SignDocument` with a `DID` id.
2. **Track status.** Poll `getDocument` with the `document_id` (or use the `doc.signed` webhook). Watch `agreement_status` (`requested` -> `completed`).
3. **Download.** Once `completed`, call `downloadSignedDocument` with the `document_id` to retrieve the signed PDF.

## Rules
- Template-driven signing still produces a legally-binding agreement — confirm with a human before sending (`agentic-access/digio-agentic-access.yml`).
- Verify all `template_values` are correct before the call; the generated document is what gets signed.
- Persist the `DID`; on `401` re-check environment-correct Basic credentials (`errors/digio-problem-types.yml`).
