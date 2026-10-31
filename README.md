# Rho Protocol

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Rho Protocol (Rho Labs) operates Rho X, a decentralized multi-asset trading and settlement layer for on-chain capital markets — interest-rate futures, perpetuals, and tokenized real-world assets tradable from a single cross-margined account. It offers off-exchange collateral custody (BitGo OES or self-custody), zero-gas settlement, and a private cross-chain RFQ swap service (Rho Relay) bridging Ethereum and Canton Network assets. Rho X exposes a REST API, a WebSocket streaming API, an npm SDK, and an official Model Context Protocol (MCP) server for programmatic trading, market data, and account management. Backed by Speedinvest.

**Areas:** Company · Trading · DeFi · Derivatives · Capital Markets · Blockchain · Market Data · WebSocket · MCP · Real-Time

## Rho Protocol on APIs.io

Everything profiled for Rho Protocol is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/rho-protocol/](https://apis.io/providers/rho-protocol/)** — or go straight to one of the APIs or properties below.

### APIs (4)

- [Rho Protocol Market Data API](https://apis.io/apis/rho-protocol/rho-protocol-market-data-api/) — The Market Data API from Rho Protocol — 7 operation(s) for market data.
- [Rho Protocol Stats API](https://apis.io/apis/rho-protocol/rho-protocol-stats-api/) — The Stats API from Rho Protocol — 1 operation(s) for stats.
- [Rho Protocol Trading API](https://apis.io/apis/rho-protocol/rho-protocol-trading-api/) — The Trading API from Rho Protocol — 3 operation(s) for trading.
- [Rho Protocol User Data API](https://apis.io/apis/rho-protocol/rho-protocol-user-data-api/) — The User Data API from Rho Protocol — 12 operation(s) for user data.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Rho X WebSocket API](https://apis.io/asyncapis/rho-protocol/rho-protocol-ws-asyncapi/)

#### Event channels (14)

Individual events and webhooks the provider emits.

- [market-floating-rate-candles.{marketId}](https://apis.io/channels/rho-protocol/market-floating-rate-candles-marketid/)
- [order-book.{symbol}](https://apis.io/channels/rho-protocol/order-book-symbol/)
- [symbol-candles.{symbol}](https://apis.io/channels/rho-protocol/symbol-candles-symbol/)
- [symbol-trades.{symbol}](https://apis.io/channels/rho-protocol/symbol-trades-symbol/)
- [ticker.{symbol}](https://apis.io/channels/rho-protocol/ticker-symbol/)
- [user-account](https://apis.io/channels/rho-protocol/user-account/)
- [user-account-candles](https://apis.io/channels/rho-protocol/user-account-candles/)
- [user-balances](https://apis.io/channels/rho-protocol/user-balances/)
- [user-margin-account](https://apis.io/channels/rho-protocol/user-margin-account/)
- [user-margin-account-candles](https://apis.io/channels/rho-protocol/user-margin-account-candles/)
- [user-orders](https://apis.io/channels/rho-protocol/user-orders/)
- [user-positions](https://apis.io/channels/rho-protocol/user-positions/)
- [user-trades](https://apis.io/channels/rho-protocol/user-trades/)
- [user-transfers](https://apis.io/channels/rho-protocol/user-transfers/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [rho-mcp](https://apis.io/servers/rho-protocol/rho-mcp/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Rho Protocol Agentic Access](https://apis.io/agentic-access/rho-protocol/rho-protocol-agentic-access/)

#### Collections (4)

Postman and Open Collection request collections.

- [Rho Exchange Market Data API](https://apis.io/collections/rho-protocol/open-rho-protocol-market-data-api/)
- [Rho Exchange Market Data Stats API](https://apis.io/collections/rho-protocol/open-rho-protocol-stats-api/)
- [Rho Exchange Market Data Trading API](https://apis.io/collections/rho-protocol/open-rho-protocol-trading-api/)
- [Rho Exchange Market Data User Data API](https://apis.io/collections/rho-protocol/open-rho-protocol-user-data-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Rho Protocol Openapi Overlay](https://apis.io/overlays/rho-protocol/rho-protocol-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Rho Protocol Authentication](https://apis.io/security/rho-protocol/rho-protocol-authentication/)
- [Rho Protocol Domain Security](https://apis.io/security/rho-protocol/rho-protocol-domain-security/)

#### Rate limits (1)

Published request limits.

- [Rho Protocol Rate Limits](https://apis.io/rate-limits/rho-protocol/rho-protocol-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://x.rho.trading/)
- [Documentation](https://docs.rho.trading/)
- [Getting started](https://docs.rho.trading/getting-started/quick-start-first-trade.md)
- [API reference](https://docs.rho.trading/api-reference/rest-api-reference.md)
- [Support](https://docs.rho.trading/faq-and-support/contact-support.md)
- [Blog](https://docs.rho.trading/)
- [GitHub](https://github.com/RhoLabs)

## API Evangelist rating

**Kin Score 37.5** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 50.8 |
| Contract governance | 4.5 |
| Operational transparency | 39.5 |
| Developer ergonomics | 66.1 |
| Access clarity | 0.0 |

**Agent readiness 29.2** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 15.7** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/rho-protocol/](https://apis.io/providers/rho-protocol/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Rho Protocol: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/rho-protocol/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
