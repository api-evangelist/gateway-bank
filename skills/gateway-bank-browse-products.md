---
name: Browse Gateway Bank banking products
description: List and inspect Gateway Bank's openly offered retail banking products
  (accounts, mortgages, personal/car loans, term deposits) via the public,
  unauthenticated CDR Product Reference Data API.
api: openapi/gateway-bank-cds-banking-products-openapi.yml
operations: [listBankingProducts, getBankingProductDetail]
---

# Browse Gateway Bank banking products

Gateway Bank exposes its product catalogue through the Australian Consumer Data Right
(CDR) Product Reference Data API. This surface is **public and unauthenticated** — no
API key, token, or CDR accreditation is required. (All other CDS operations —
accounts, balances, transactions, payees — DO require the CDR security profile and
are out of scope for this skill.)

Base URL: `https://public.cdr-api.gatewaybank.com.au/cds-au/v1`

## Rules

- Every request MUST send the version header `x-v: 5` (the currently served PRD
  version). Omitting it or sending an unsupported version returns HTTP `406`
  (Unsupported Version). Optionally send `x-min-v` to allow negotiation.
- Do NOT send credentials; the endpoint is intentionally open.
- Responses use the CDS envelope: `data`, `links`, `meta`. Errors use
  `{ errors: [ { code, title, detail } ] }` (see `errors/gateway-bank-problem-types.yml`).

## Steps

1. **List products** — call `listBankingProducts`:
   `GET /banking/products` with header `x-v: 5`.
   - Filter with `product-category` (e.g. `RESIDENTIAL_MORTGAGES`,
     `TRANS_AND_SAVINGS_ACCOUNTS`, `TERM_DEPOSITS`, `PERS_LOANS`), `effective`
     (`CURRENT`/`FUTURE`/`ALL`), `updated-since`, and `brand`.
   - Paginate with `page` (default 1) and `page-size` (default 25); read
     `meta.totalRecords` / `meta.totalPages` and follow `links.next` until absent.
     (147 products across 30 pages observed 2026-07-20.)

2. **Get product detail** — for a `productId` from the list, call
   `getBankingProductDetail`: `GET /banking/products/{productId}` with `x-v: 5`.
   Returns rates, fees, eligibility, features, constraints, and additional
   information for the single product. A missing/withdrawn product returns `404`.

## Conventions referenced

- Versioning + pagination + error envelope: `conventions/gateway-bank-conventions.yml`
- Version lifecycle: `lifecycle/gateway-bank-lifecycle.yml`
