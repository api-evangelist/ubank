---
name: Look up ubank banking products
description: >-
  Discover ubank's openly offered banking products (savings accounts and
  residential mortgages) and fetch full detail for one, using ubank's public,
  unauthenticated CDR Product Reference Data API. No credentials required.
api: openapi/ubank-cds-banking-products-openapi.yml
base_url: https://public.cdr-api.86400.com.au/cds-au/v1
operations: [listBankingProducts, getBankingProductDetail]
generated: '2026-07-20'
method: generated
---

# Look up ubank banking products

ubank exposes two public, unauthenticated Consumer Data Right (CDR) Product
Reference Data operations. Use them to browse ubank's product catalogue and read
the rates, fees, features, and eligibility for any product. No API key or token
is needed.

## Rules that apply to every call

- **Send an `x-v` header on every request.** It is the integer payload version.
  Use `x-v: 5` for Get Products and `x-v: 7` for Get Product Detail (current at
  time of writing). A missing `x-v` returns HTTP 400; an unsupported version
  returns HTTP 406 with the supported version in the `x-v` response header.
- The base URL is `https://public.cdr-api.86400.com.au/cds-au/v1`.
- Responses are JSON; errors use the CDS `ResponseErrorList` envelope
  (`errors[]` with `code`/`title`/`detail`) — see `errors/ubank-error-codes.yml`.
- Optionally send `x-fapi-interaction-id` (a UUID) for request tracing; it is
  echoed back in the response.

## Step 1 — List products (`listBankingProducts`)

`GET /banking/products` with header `x-v: 5`.

Useful query filters:
- `product-category` — filter to a category (e.g. a savings or mortgage category).
- `effective` — `CURRENT` (default), `FUTURE`, or `ALL`.
- `updated-since` — only products updated after a DateTimeString.
- `page` / `page-size` — standard pagination (default page 1, page-size 25).

Read `data.products[]` from the response. Paginate using `meta.totalPages` and
`meta.totalRecords`, or follow `links.next`. Capture each product's `productId`.

## Step 2 — Get product detail (`getBankingProductDetail`)

`GET /banking/products/{productId}` with header `x-v: 7`, using a `productId`
from Step 1.

The detail response embeds the full product: `features`, `fees`, `constraints`,
`eligibility`, `depositRates`, `lendingRates`, `bundles`, `instalments`, and
`additionalInformation` document URIs. An unknown or malformed `productId`
returns HTTP 404 (`Resource/NotFound` or `Resource/Invalid`).

## Notes

- This is read-only public data. There is no write, idempotency, or webhook
  surface. Consumer account/transaction data is only available to CDR Accredited
  Data Recipients via the FAPI-secured authorization model — not through this API.
