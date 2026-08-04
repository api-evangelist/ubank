# ubank (ubank)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ubank is an Australian digital-only bank offering savings accounts and home loans online and over the phone. Launched in 2008 as the online banking brand of National Australia Bank (NAB), ubank operates under NAB's authorised deposit-taking institution (ADI) licence and is registered in the Consumer Data Right (CDR) ecosystem as the "UBank" data holder brand under NAB (ABN 12 004 044 937). After NAB acquired neobank 86 400 in 2021, its customers and technology were migrated onto the 86 400 platform, which is why ubank's public CDR API surface is hosted at `public.cdr-api.86400.com.au`.

As a CDR data holder, ubank exposes a public, unauthenticated Product Reference Data (PRD) API conforming to the Consumer Data Standards. Authenticated consumer banking data is shared only with accredited data recipients under the CDR's OAuth2/OIDC (FAPI) authorization model. ubank does not publish a general-purpose developer portal beyond its CDR product-data pages.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ubank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ubank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Banking
- Open Banking
- CDR
- Consumer Data Right
- Product Reference Data
- Digital Bank
- Consumer Banking
- Australia

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### ubank CDR Product Reference Data API

Public, unauthenticated Consumer Data Right (CDR) Product Reference Data endpoint (`GET /banking/products`) returning ubank's openly available banking products - savings accounts and residential mortgages - with pricing, fees, and eligibility, conforming to the DSB Consumer Data Standards. Confirmed live returning HTTP 200 with an `x-v` response header on version 5 (14 products at time of review).

- **Human URL:** [https://www.ubank.com.au/cdr/apis](https://www.ubank.com.au/cdr/apis)
- **Base URL:** `https://public.cdr-api.86400.com.au/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Products

#### Properties

- [Documentation](https://www.ubank.com.au/cdr/apis)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-products)
- [OpenAPI](openapi/ubank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### ubank CDR Banking Product Detail API

Public, unauthenticated CDR endpoint (`GET /banking/products/{productId}`) returning the full detail for a single ubank banking product - rates, fees, features, eligibility, constraints, and terms - conforming to the DSB Consumer Data Standards Get Product Detail contract.

- **Human URL:** [https://www.ubank.com.au/cdr/apis](https://www.ubank.com.au/cdr/apis)
- **Base URL:** `https://public.cdr-api.86400.com.au/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Detail
- Banking

#### Properties

- [Documentation](https://www.ubank.com.au/cdr/apis)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-product-detail)
- [OpenAPI](openapi/ubank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.ubank.com.au/)
- [Documentation](https://www.ubank.com.au/cdr/apis)
- [LinkedIn](https://www.linkedin.com/company/ubank)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
