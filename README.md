# P&N Bank (pn-bank)

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

P&N Bank is the retail banking brand of Police & Nurses Limited (ABN 69 087 651 876, AFSL/Australian Credit Licence 240701), a customer-owned (mutual) bank owned by its members rather than shareholders and one of Western Australia's largest locally based banks, headquartered in Perth. It grew out of the Police & Nurses Credit Society and today sits within the broader P&N Group, which also operates the bcu brand on the New South Wales / Queensland east coast. As an Authorised Deposit-taking Institution (ADI) it participates in Australia's Consumer Data Right (CDR / Open Banking), exposing a public, unauthenticated Product Reference Data (PRD) API built to the Data Standards Body (DSB) Consumer Data Standards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/pn-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/pn-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Customer Owned
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### P&N Bank CDR Product Reference Data API

Public, unauthenticated Consumer Data Right (CDR) Product Reference Data API exposing P&N Bank's banking product catalogue. `GET /banking/products` returns a paginated list of products and `GET /banking/products/{productId}` returns full product detail (rates, fees, features, eligibility, constraints). Confirmed live on 2026-07-20 returning HTTP 200 with a `data.products` array and an `x-v` response header of 5 (68 products at time of review). Built to the DSB Consumer Data Standards; no API key or authorization is required for product reference data.

- **Human URL:** [https://www.pnbank.com.au/help-and-support/open-banking/pn-bank-products-api/](https://www.pnbank.com.au/help-and-support/open-banking/pn-bank-products-api/)
- **Base URL:** `https://public.cdr-api.pnbank.com.au/cds-au/v1/banking/products`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Australia

#### Properties

- [Documentation](https://www.pnbank.com.au/help-and-support/open-banking/pn-bank-products-api/)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-products)
- [OpenAPI](openapi/pn-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.pnbank.com.au/)
- [Documentation](https://www.pnbank.com.au/help-and-support/open-banking/)
- [Privacy Policy](https://www.pnbank.com.au/important-information/privacy/)
- [Terms of Service](https://www.pnbank.com.au/important-information/terms-and-conditions/)
- [Support](https://www.pnbank.com.au/contact/)
- [LinkedIn](https://www.linkedin.com/company/p&n-bank)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
