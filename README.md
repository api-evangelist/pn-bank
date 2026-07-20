# P&N Bank (pn-bank)

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
