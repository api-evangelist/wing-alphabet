# Wing

Wing is Alphabet's drone delivery subsidiary, spun out of Google X in 2018. Wing designs, builds, and operates small fixed-wing electric VTOL aircraft that autonomously pick up and deliver packages to customers' homes, and operates an unmanned traffic management (UTM) stack used by drone pilots and aviation authorities.

This repository is an [API Evangelist](https://apievangelist.com) profile of Wing — a Tier-3 catalog entry, meaning the company exposes real commercial APIs but does not publish open documentation, OpenAPI specs, or a developer portal.

## What Wing Operates

Wing runs two distinct technical surfaces, both of which have APIs that are real but private:

- **Wing Delivery Platform** — the partner-only API and UI suite that lets retailers, restaurants, and logistics providers embed drone delivery into their own order flow. Public docs describe three high-level capabilities: assess drone delivery availability for an address, request a delivery, and provide real-time tracking of an in-flight package. Integration is gated through `partnerships@wing.com` and a Wing technical team — there is no self-serve developer portal. Known partners include Walmart, DoorDash, and Papa Johns.
- **OpenSky** — a consumer-facing drone airspace authorization app (FAA-approved LAANC USS in the United States; approved by CASA in Australia). Wing publishes an OpenSky API that allows companies to embed OpenSky's flight-brief and airspace-authorization flow inside their own apps, but the API itself is partner-only.

Wing also co-founded the [InterUSS Platform](https://github.com/interuss), an open-source UTM project that implements the ASTM F3411 Remote ID standard and the Discovery and Synchronization Service (DSS) — InterUSS is now hosted by the Linux Foundation and lives in its own organization rather than under Wing's GitHub.

## Why Tier-3

This profile is Tier-3 (catalog stub) rather than Tier-1 (fully artifacted) because:

- No public OpenAPI, AsyncAPI, JSON Schema, or developer reference exists for either the Wing Delivery Platform API or the OpenSky API.
- The [`wing-aviation`](https://github.com/wing-aviation) GitHub organization is empty and archived — Wing does not publish SDKs, clients, or sample code under its own org.
- The published technical material (wing.com/technology, wing.com/solutions, wing.com/partner, the partner blog posts) describes API behavior at a marketing level but does not document endpoints, request/response shapes, authentication, rate limits, or pricing.

Per the api-evangelist pipeline rules, no placeholder OpenAPI, Spectral rulesets, Naftiko capabilities, or schemas have been generated. If Wing publishes a partner developer portal or OpenAPI in the future, this repo will be re-run through the full pipeline and promoted to Tier-1.

## Files

- [`apis.yml`](./apis.yml) — APIs.json 0.20 catalog entry for Wing, with company description, tags, and the canonical set of `common` links (website, technology, partner program, OpenSky, aviation partners, GitHub org, InterUSS, LAANC, social).
- `README.md` — this file.

## Maintainer

- Kin Lane — kin@apievangelist.com
