---
name: Look up P&N Bank banking products
description: >-
  Retrieve P&N Bank's public banking product catalogue and drill into a single
  product's rates, fees, features, and eligibility using the unauthenticated CDR
  Product Reference Data API. No API key or authorization is required.
api: openapi/pn-bank-cds-banking-products-openapi.yml
operations: [listBankingProducts, getBankingProductDetail]
---

# Look up P&N Bank banking products

P&N Bank exposes a public, unauthenticated Consumer Data Right (CDR) Product
Reference Data API. Use it to list products and fetch full product detail.

## Base URL
`https://public.cdr-api.pnbank.com.au/cds-au/v1`

## Auth
None. These endpoints are public CDR product reference data — do not send any API
key, bearer token, or client credentials.

## Required header
Every request MUST include `x-v: 5` (the current endpoint version). Optionally send
`x-min-v` for the minimum acceptable version. The response echoes the served version
in its `x-v` header.

## Step 1 — List products (`listBankingProducts`)
`GET /banking/products`

Useful query params:
- `product-category` — filter by category (e.g. `TRANS_AND_SAVINGS_ACCOUNTS`,
  `RESIDENTIAL_MORTGAGES`, `CRED_AND_CHRG_CARDS`, `TERM_DEPOSITS`, `PERS_LOANS`).
- `effective` — `CURRENT` (default), `FUTURE`, or `ALL`.
- `updated-since` — ISO 8601 UTC timestamp; return only products changed since then.
- `brand` — filter by brand.
- `page`, `page-size` — page-number pagination (default page-size 25, max 1000).

Read `data.products[]` for the list and `meta.totalRecords` / `meta.totalPages` plus
the `links.next` cursor to page through results.

## Step 2 — Get product detail (`getBankingProductDetail`)
`GET /banking/products/{productId}`

Pass a `productId` from Step 1. The response `data` object adds the nested arrays:
`fees`, `depositRates`, `lendingRates` (each with `tiers`), `features`,
`constraints`, `eligibility`, and `bundles`.

## Error handling
Errors return the CDR envelope `{ "errors": [ { "code", "title", "detail" } ] }`
(see `errors/pn-bank-problem-types.yml`). Common cases:
- `400 urn:au-cds:error:cds-all:Header/Missing` — you omitted the `x-v` header.
- `406 urn:au-cds:error:cds-all:Version/Unsupported` — requested `x-v` not supported.
- `404 urn:au-cds:error:cds-all:Resource/Invalid` — unknown `productId`.
- `422 urn:au-cds:error:cds-all:Pagination/InvalidPage` — page beyond `totalPages`.

## Notes
Read-only surface (GET only) — there are no write or idempotency semantics. Anything
beyond product reference data (accounts, balances, transactions) requires CDR
accreditation and the OAuth2/OIDC FAPI flow and is NOT reachable here.
