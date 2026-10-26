# Digio (digio)

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
