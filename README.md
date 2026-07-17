# Digio (digio)

Digio is an India-based digital trust and paperwork automation platform. Its REST APIs deliver legally-valid Aadhaar and OTP eSign, eStamping, KYC (CKYC, KRA, DigiLocker, offline Aadhaar, and Video KYC), eNACH/NACH eMandates and UPI Autopay recurring payments, AML/CFT screening, and template-based document and agreement management. All endpoints use HTTPS with HTTP Basic authentication.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/digio/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/digio/refs/heads/main/apis.yml)

## Tags

- eSign
- KYC
- eNACH
- eMandate
- Digital Signature
- India
- Fintech
- Identity Verification

## Timestamps

- **Created:** 2026-07-17
- **Modified:** 2026-07-17

## APIs

### Digio eSign API

DigiSign - upload a PDF or template and collect legally-valid Aadhaar-based, OTP-based, or DSC electronic signatures, with signer tracking and signed-document download.

- **Human URL:** [https://documentation.digio.in/digisign/](https://documentation.digio.in/digisign/)
- **Base URL:** `https://api.digio.in`

#### Tags

- eSign
- Aadhaar
- Digital Signature
- DigiSign

#### Properties

- [Documentation](https://documentation.digio.in/digisign/)
- [API Reference](https://documentation.digio.in/digisign/api_integration/create_sign_request/)
- [OpenAPI](openapi/digio-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/digio.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Digio eMandate (eNACH) API

DigiCollect - create and manage NPCI eNACH electronic mandates, physical NACH, and UPI Autopay authorizations for recurring debit, returning a UMRN (Unique Mandate Reference Number).

- **Human URL:** [https://documentation.digio.in/digicollect/nach/nach_registration/](https://documentation.digio.in/digicollect/nach/nach_registration/)
- **Base URL:** `https://api.digio.in`

#### Tags

- eNACH
- eMandate
- NACH
- DigiCollect
- Recurring Payments

#### Properties

- [Documentation](https://documentation.digio.in/digicollect/nach/nach_registration/)
- [API Reference](https://documentation.digio.in/digicollect/nach/nach_registration/get_mandate_details/)
- [OpenAPI](openapi/digio-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/digio.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Digio KYC API

DigiKYC - template-driven identity verification workflows spanning CKYC, KRA, DigiLocker, ID-proof capture, offline Aadhaar, and Video KYC.

- **Human URL:** [https://documentation.digio.in/digikyc/](https://documentation.digio.in/digikyc/)
- **Base URL:** `https://api.digio.in`

#### Tags

- KYC
- Identity Verification
- CKYC
- KRA
- Video KYC
- DigiKYC

#### Properties

- [Documentation](https://documentation.digio.in/digikyc/)
- [API Reference](https://documentation.digio.in/digikyc/ckyc/api_integration/)
- [OpenAPI](openapi/digio-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/digio.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Digio DigiLocker API

Fetch government-issued documents (Aadhaar, PAN, driving licence and others) directly from India's DigiLocker with citizen consent for KYC.

- **Human URL:** [https://documentation.digio.in/digikyc/digilocker/](https://documentation.digio.in/digikyc/digilocker/)
- **Base URL:** `https://api.digio.in`

#### Tags

- DigiLocker
- KYC
- Document Verification

#### Properties

- [Documentation](https://documentation.digio.in/digikyc/digilocker/)

### Digio Documents & eStamp API

DigiDocs - generate agreements and documents from templates with state-specific eStamp duty collection, then route them into an eSign request.

- **Human URL:** [https://documentation.digio.in/digidocs/](https://documentation.digio.in/digidocs/)
- **Base URL:** `https://api.digio.in`

#### Tags

- Documents
- eStamp
- Agreements
- DigiDocs

#### Properties

- [Documentation](https://documentation.digio.in/digidocs/)
- [API Reference](https://documentation.digio.in/digidocs/api_integration/create_document_from_template_api/)
- [OpenAPI](openapi/digio-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/digio.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Digio AML/CFT API

DigiShield - Anti-Money-Laundering and Counter-Financing-of-Terrorism screening and ongoing monitoring against sanctions and watchlists.

- **Human URL:** [https://www.digio.in/](https://www.digio.in/)
- **Base URL:** `https://api.digio.in`

#### Tags

- AML
- CFT
- Screening
- DigiShield

#### Properties

- [Documentation](https://www.digio.in/)

## Common Properties

- [GitHub Organization](https://github.com/digio-tech)
- [LinkedIn](https://in.linkedin.com/company/digio.in)
- [Website](https://www.digio.in/)
- [Documentation](https://documentation.digio.in/)
- [Plans](plans/digio-plans-pricing.yml)
- [Rate Limits](rate-limits/digio-rate-limits.yml)
- [Fin Ops](finops/digio-finops.yml)
- [Blog](https://www.digio.in/blog/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
