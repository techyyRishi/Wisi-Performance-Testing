# Wisi – Test Execution Record

## Purpose

Use this document to record actual JMeter execution details. Only enter values that can be verified from JMeter output, `.jtl` results, screenshots, or execution notes.

## Known Initial Setup

| Item | Confirmed detail |
|---|---|
| Test Plan | `WISI Performance Testing` |
| Thread Group | `User Journey` |
| Initial users | 1 |
| Ramp-up | 1 second |
| Loop count | 1 |
| Tool | Apache JMeter |

## Execution History

The available historical notes confirm initial setup and API-flow preparation. They do not contain a verified completed load-test run or aggregate performance metrics.

| Run | Date | Users | Ramp-up | Duration / Loops | Status | Evidence |
|---|---|---:|---:|---|---|---|
| Initial configuration | Date not verified | 1 | 1 second | 1 loop | Setup documented; execution outcome not verified | Recover original screenshot / JMX |

## Results to Record

| Metric | Actual result |
|---|---|
| Total samples | Not available in recovered notes |
| Successful samples | Not available |
| Failed samples | Not available |
| Error percentage | Not available |
| Average response time | Not available |
| Median response time | Not available |
| 90th percentile | Not available |
| 95th percentile | Not available |
| 99th percentile | Not available |
| Throughput | Not available |
| Minimum response time | Not available |
| Maximum response time | Not available |

## Execution Notes

- Record the exact environment and execution date.
- Record the exact Thread Group configuration.
- Note which API samplers were enabled for the run.
- Capture errors and response codes.
- Export JMeter results where available.
- Do not infer missing metrics from screenshots that do not display them.

## Pending Evidence

- [ ] Original `.jmx` file
- [ ] JMeter run screenshot
- [ ] Summary Report / Aggregate Report
- [ ] `.jtl` result file, if available
- [ ] Error and response details
