# Wisi – API Performance Testing Portfolio

## Project Overview

This repository documents my performance-testing work on the Wisi application using **Apache JMeter**.

The testing focus was on backend API performance for the customer purchase journey. The work was structured around the sequence:

**Login → Product Details → Add to Cart → Cart → Checkout → TradeSafe Payment → Success**

The UI itself was not the load-testing target; the focus was on the backend APIs supporting the journey.

## My Role

I worked on preparing and configuring a JMeter test plan, understanding the API dependencies in the purchase flow, and setting up request handling and response inspection.

## Tools & Components

- Apache JMeter
- HTTP Request samplers
- HTTP Request Defaults
- HTTP Cookie Manager
- View Results Tree
- Postman/API knowledge for understanding request and response behaviour

## Repository Contents

| Section | Purpose |
|---|---|
| `01-Test-Planning` | Scope, objectives, tested flow, and workload assumptions |
| `02-JMeter-Test-Plan` | JMeter test-plan notes and the original `.jmx` file when available |
| `03-API-Scenarios` | API sequence, dependencies, and dynamic variables |
| `04-Test-Execution` | Execution record and results template |
| `05-Analysis-and-Observations` | Performance analysis template and documented limitations |
| `06-Evidence` | Screenshots and supporting evidence |

## Confirmed Setup Details

- Test Plan: `WISI Performance Testing`
- Thread Group: `User Journey`
- Initial Thread Group configuration: 1 user, 1-second ramp-up, 1 loop
- HTTP Request Defaults host: `wisi-oi-dev-8e7c267d141d.herokuapp.com`
- Protocol: HTTPS
- HTTP Cookie Manager: added with default settings
- View Results Tree: used for inspecting individual sampler responses

The above is the initial configuration discussed during setup. It should not be interpreted as a completed load test at higher concurrency.

## API Flow & Known Progress

The following API areas were discussed:

1. Login: `POST https://flex-api.sharetribe.com/v1/auth/token`
2. Product details by slug: `/api/findListingBySlug/${slug}`
3. Show listing: `/v1/api/listings/show?id=${listingId}`
4. Add to Cart: API request was part of the planned purchase flow.
5. Checkout and TradeSafe payment: these stages were still pending in the documented progress.

Dynamic values discussed for correlation included `access_token`, `refresh_token`, `listingId`, and `authorId`. The exact extraction configuration and remaining transaction/payment identifiers should be verified against the original JMeter file or screenshots before publication.

## Execution Status & Reporting

The available historical notes confirm the initial JMeter setup and API-flow preparation. They do **not** contain verified aggregate performance metrics such as average response time, throughput, error percentage, or completed concurrent-user results.

Do not publish assumed performance numbers. Add actual JMeter reports or screenshots only after verifying the original execution evidence.

## Important Notes

- This repository documents the work and setup that can currently be substantiated.
- The 1-user configuration is an initial setup, not evidence of a stress, load, or scalability result.
- Checkout and TradeSafe payment execution were pending in the available historical notes.
- Remove credentials, access tokens, cookies, personal data, and private environment details before publishing any JMeter file or screenshot.
