# Wisi – API Flow & Correlation Notes

## Overview

The JMeter work was organised around the backend API sequence supporting the Wisi customer purchase journey.

The UI was not the load-testing target.

## API Sequence

### 1. Login

**Method:** POST  
**Endpoint:** `https://flex-api.sharetribe.com/v1/auth/token`

Dynamic values discussed:
- `access_token`
- `refresh_token`

Verify the actual request body, headers, and extractors against the original request/JMeter file.

### 2. Product Details by Slug

**Endpoint pattern:** `/api/findListingBySlug/${slug}`

The product slug is used to retrieve the relevant listing. Confirm the exact request method and parameter handling from the source request.

### 3. Show Listing

**Endpoint pattern:** `/v1/api/listings/show?id=${listingId}`

Dynamic value discussed:
- `listingId`

### 4. Add to Cart

The Add to Cart API was part of the planned purchase journey. The exact endpoint, method, request body, and response correlation must be recovered from the original JMeter file or screenshots.

### 5. Checkout & TradeSafe Payment

Checkout and TradeSafe payment were part of the intended end-to-end flow but were pending in the available historical notes.

Do not document these stages as executed until the original evidence confirms completion.

## Correlation Variables Discussed

| Variable | Purpose |
|---|---|
| `access_token` | Authentication for subsequent requests |
| `refresh_token` | Token refresh flow, if required |
| `listingId` | Listing identifier for listing-related requests |
| `authorId` | Listing/provider author identifier |

The exact extractor type, JSON path, variable scope, and usage in later requests must be verified against the original JMeter configuration.

## Validation Checklist

- [ ] Login response is validated.
- [ ] Token extraction is verified.
- [ ] Authenticated requests use the correct token.
- [ ] Product slug resolves to the expected listing.
- [ ] Listing ID is extracted and reused correctly.
- [ ] Add-to-cart request details are verified.
- [ ] Checkout and payment stages are verified before marking complete.
- [ ] Response assertions are based on actual API contracts.
