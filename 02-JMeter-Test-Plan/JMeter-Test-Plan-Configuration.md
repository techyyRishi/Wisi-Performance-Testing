# Wisi – JMeter Test Plan Configuration

## Test Plan

`WISI Performance Testing`

## Thread Group

`User Journey`

### Initial Configuration

- Number of Threads (Users): 1
- Ramp-up Period: 1 second
- Loop Count: 1

## HTTP Request Defaults

| Setting | Value |
|---|---|
| Protocol | HTTPS |
| Server Name / Host | `wisi-oi-dev-8e7c267d141d.herokuapp.com` |

## Components Discussed

- HTTP Request Defaults
- HTTP Cookie Manager (default settings)
- View Results Tree

## Authentication & Dynamic Variables

The following values were discussed for use across dependent requests:

- `access_token`
- `refresh_token`
- `listingId`
- `authorId`

Verify the actual extractors and header configuration from the original `.jmx` file before claiming they were fully implemented.

## Original JMeter File

Place the actual JMeter test plan in this folder using the filename:

`WISI-Performance-Testing.jmx`

Do not create a replacement `.jmx` from assumptions. Upload the original file only after removing credentials, cookies, access tokens, and other secrets.

## Configuration Verification Checklist

- [ ] Original `.jmx` opens successfully in JMeter.
- [ ] Test Plan and Thread Group names match.
- [ ] Thread Group settings match the saved plan.
- [ ] HTTP Request Defaults are verified.
- [ ] Cookie Manager configuration is verified.
- [ ] Authentication and token extraction are verified.
- [ ] Dynamic listing identifiers are verified.
- [ ] All secrets are removed or externalised before public upload.
