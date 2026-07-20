# ubank (ubank)

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
