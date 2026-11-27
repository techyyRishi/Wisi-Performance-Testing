# Wisi – Workload Model

## Purpose

This document records the JMeter workload configuration used or planned for the Wisi API performance-testing work.

## Confirmed Initial Configuration

| Setting | Value |
|---|---|
| Test Plan | `WISI Performance Testing` |
| Thread Group | `User Journey` |
| Number of Threads (Users) | 1 |
| Ramp-up Period | 1 second |
| Loop Count | 1 |

This is the initial configuration documented during setup. It is not, by itself, evidence of a completed load or stress test.

## Additional Workload Profiles

No verified higher-concurrency profiles, ramp-up stages, hold durations, or peak-load targets are available in the current historical notes.

If the original `.jmx` file or screenshots show additional profiles, record them here exactly as configured.

| Profile | Users | Ramp-up | Duration / Loops | Evidence |
|---|---:|---:|---|---|
| Initial setup | 1 | 1 second | 1 loop | Historical setup notes |
| Additional profile | Not verified | Not verified | Not verified | Add only after checking source |

## Metrics to Capture During a Verified Run

- Sample count
- Average response time
- Median response time
- 90th / 95th / 99th percentile response time, if available
- Throughput
- Error count and error percentage
- Minimum and maximum response time
- Received / sent throughput, if available

Do not enter estimated or invented values. Copy metrics from the actual JMeter results.
