# Wisi – Performance Test Analysis

## Objective

This document is intended to analyse the actual JMeter results for the Wisi backend API journey.

## Current Evidence Status

The historical information currently recovered confirms:
- Apache JMeter was selected for API performance testing.
- An initial Test Plan and Thread Group were configured.
- Login, product details, listing details, and Add to Cart were discussed as part of the API journey.
- Checkout and TradeSafe payment execution were pending in the available notes.

No verified aggregate JMeter metrics are currently available in the recovered information.

## Performance Metrics

Populate this section only from the actual JMeter Summary Report, Aggregate Report, dashboard, or `.jtl` results.

| Metric | Result | Evidence reference |
|---|---|---|
| Sample count | Not available | Pending |
| Average response time | Not available | Pending |
| Median response time | Not available | Pending |
| 90th percentile | Not available | Pending |
| 95th percentile | Not available | Pending |
| 99th percentile | Not available | Pending |
| Throughput | Not available | Pending |
| Error percentage | Not available | Pending |
| Min / Max response time | Not available | Pending |

## API-Level Observations

Add one subsection per API after reviewing its actual JMeter results:

### Login API
- Observed response time:
- Throughput:
- Error rate:
- Response codes:
- Notes:

### Product Details API
- Observed response time:
- Throughput:
- Error rate:
- Response codes:
- Notes:

### Show Listing API
- Observed response time:
- Throughput:
- Error rate:
- Response codes:
- Notes:

### Add to Cart API
- Execution evidence:
- Observed response time:
- Error rate:
- Notes:

### Checkout / TradeSafe
- Execution status:
- Evidence:
- Notes:

## Findings & Recommendations

Do not add performance bottlenecks or pass/fail conclusions until supported by actual execution results.

Once the reports are recovered, document:
- Slow or inconsistent API responses
- Failed requests and response codes
- Throughput changes under different user loads
- Authentication or correlation failures
- Any observed application or environment limitations

## Conclusion

A performance conclusion cannot be made from the initial one-user setup alone. Complete this analysis after recovering and reviewing the actual JMeter execution results.
