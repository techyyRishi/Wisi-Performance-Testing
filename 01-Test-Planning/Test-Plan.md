# Wisi – Performance Test Plan

## 1. Objective

Document the API performance-testing approach prepared for the Wisi customer purchase journey using Apache JMeter.

## 2. Application & Testing Scope

The work focused on backend APIs supporting the customer purchase journey. The browser/UI was not the load-testing target.

### Purchase Journey

1. Customer login
2. Retrieve product details
3. Add product to cart
4. Review cart
5. Proceed to checkout
6. TradeSafe payment
7. Payment success

## 3. In-Scope API Areas

| Journey stage | API / area | Historical status |
|---|---|---|
| Login | `POST https://flex-api.sharetribe.com/v1/auth/token` | Discussed for JMeter setup |
| Product details | `/api/findListingBySlug/${slug}` | Discussed |
| Show listing | `/v1/api/listings/show?id=${listingId}` | Discussed |
| Add to Cart | Add-to-cart API | Part of planned flow; exact request details require verification |
| Checkout | Checkout API | Pending in available historical notes |
| TradeSafe payment | Payment API / flow | Pending in available historical notes |

## 4. Test Tool & Configuration

- Tool: Apache JMeter
- Test Plan name: `WISI Performance Testing`
- Thread Group: `User Journey`
- Initial configuration: 1 user, 1-second ramp-up, 1 loop
- Protocol: HTTPS
- Host in HTTP Request Defaults: `wisi-oi-dev-8e7c267d141d.herokuapp.com`
- Components discussed: HTTP Request Defaults, HTTP Cookie Manager, View Results Tree

## 5. Request Dependencies & Correlation

The following dynamic values were identified as relevant to the journey:

- `access_token`
- `refresh_token`
- `listingId`
- `authorId`

The exact JSONPath/regular-expression extractors, variable scopes, and request-to-request mappings must be verified from the original `.jmx` file or screenshots before being documented as implemented.

## 6. Test Data

Record the actual test data used before execution:

| Data item | Value / source |
|---|---|
| Test environment | Confirm exact environment |
| Test account | Use a dedicated non-production account; do not publish credentials |
| Product slug | Confirm from original test data |
| Listing ID | Extract dynamically where supported |
| Cart / transaction identifiers | Confirm from actual API responses |

## 7. Workload Model

The only confirmed initial configuration in the available notes is 1 user, 1-second ramp-up, and 1 loop. No higher concurrency profile or sustained-duration workload is confirmed here.

Record any additional workload only from the original JMeter plan or execution evidence.

## 8. Entry & Exit Criteria

### Entry
- Target environment is accessible.
- Valid test account and test data are available.
- Required API requests and authentication are configured.
- Sensitive values are stored securely and not hardcoded in public files.

### Exit
- Planned API requests have been executed.
- Results and errors have been reviewed.
- Actual metrics are captured from JMeter reports.
- Any incomplete or blocked stages are documented.

## 9. Limitations

Checkout and TradeSafe payment execution were pending in the available historical notes. Do not mark the full purchase journey as completed unless the original evidence confirms it.
