# Gateway Bank (gateway-bank)

Gateway Bank Ltd is a 100% customer-owned Australian mutual bank headquartered in Sydney, New South Wales. Founded in 1955 as Gateway Credit Union and rebranded to Gateway Bank in 2018, it is an APRA-regulated Authorised Deposit-taking Institution (ADI) serving more than 30,000 members with over one billion dollars in assets. As an active ADI it is a designated data holder under Australia's Consumer Data Right (CDR / Open Banking) and exposes a public, unauthenticated Product Reference Data (PRD) API conforming to the Data Standards Body Consumer Data Standards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/gateway-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/gateway-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Mutual Bank
- Customer Owned
- Australia
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Gateway Bank CDR Product Reference Data API

Public, unauthenticated Consumer Data Right (CDR) Product Reference Data endpoints exposing Gateway Bank's retail banking products - transaction and savings accounts, residential mortgages, personal and car loans, and term deposits - in the machine-readable format defined by the DSB Consumer Data Standards. Confirmed live on 2026-07-20 returning HTTP 200 with x-v 5 and 147 products across 30 pages from `GET /banking/products`; per-product detail is available at `GET /banking/products/{productId}`.

- **Human URL:** [https://www.gatewaybank.com.au/important-information/consumer-data-right-cdr/](https://www.gatewaybank.com.au/important-information/consumer-data-right-cdr/)
- **Base URL:** `https://public.cdr-api.gatewaybank.com.au/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking Products
- Consumer Data Right

#### Properties

- [Documentation](https://www.gatewaybank.com.au/important-information/consumer-data-right-cdr/)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-products)
- [OpenAPI](openapi/gateway-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.gatewaybank.com.au/)
- [Documentation](https://www.gatewaybank.com.au/important-information/consumer-data-right-cdr/)
- [LinkedIn](https://au.linkedin.com/company/gateway-bank-ltd)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
