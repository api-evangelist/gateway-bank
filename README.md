# Gateway Bank (gateway-bank)

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
