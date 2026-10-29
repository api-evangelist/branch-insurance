# Branch

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

Branch is a Columbus, Ohio insurtech that bundles home and auto insurance (with optional umbrella coverage) and issues policies in seconds from just a name and address. The company operates as Branch Insurance Exchange, a reciprocal insurer, plus the managing General Branch Agency / Branch Financial, Inc. holding company, and originally targeted direct-to-consumer customers with a quote-and-bind flow that prefills rating data from public sources. Branch raised a $147M Series C at a $1.05B valuation in 2022 (Weatherford Capital, Acrew Capital, Anthemis, Cherry Creek Holdings, Greycroft, HSCM Bermuda, AmFam Ventures, others), partnered with SimpliSafe (home security bundle) and ADT, and runs an embedded "Quote to Bind" GraphQL API used by affinity partners (mortgage originators, lenders, aggregators) to embed home + auto quotes inside their own apps. The Quote to Bind v2 GraphQL API (https://docs.v2.api.ourbranch.com) exposes requestQuoteV2, recalculateQuoteV2, addCar, addDriver, requestBind, getOffer, enhancedGetOffer, getBoundPoliciesByOfferId, getPolicyDocuments, and getOfferPDF, plus optional webhook / SFTP / S3 postbacks for bind and document-signed events. Partners authenticate with an API key in the Authorization header and an x-affinity-code header when responsible for multiple agencies, and may either run the whole flow via the API or hand customers off to ourbranch.com / staff.ourbranch.com for customize / review / checkout / sign-documents steps. A staging endpoint at https://staging.v2.api.ourbranch.com mirrors production with shared test users and payment methods. Branch operates in roughly two dozen US states including Ohio, Texas, Illinois, Arizona, Missouri, and others, and emphasises community-discount pricing, a community pledge / giveback program, and B Corp certification (2023). There is no public OpenAPI specification — the API is GraphQL-only and the schema is browsable on Apollo Studio (studio.apollographql.com/public/Branch-Quote-to-Bind-Staging) with an API key.

**Areas:** Insurance · Home Insurance · Auto Insurance · Umbrella Insurance · Bundled Insurance · Insurtech · Reciprocal Exchange · Embedded Insurance · Quote to Bind · GraphQL · Partner API · Affinity

## Branch on APIs.io

Everything profiled for Branch is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/branch-insurance/](https://apis.io/providers/branch-insurance/)** — or go straight to one of the APIs or properties below.

### APIs (1)

- [Branch Quote to Bind API](https://apis.io/apis/branch-insurance/branch-quote-to-bind-api/) — Branch's Quote to Bind GraphQL API exposes everything an affinity partner needs to go from initial quote to final purchase of Branch home + auto (and…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [Branch GraphQL API](https://apis.io/graphqls/branch-insurance/branch-insurance-graphql/)

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Branch Insurance Domain Security](https://apis.io/security/branch-insurance/branch-insurance-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.ourbranch.com/)
- [Documentation](https://www.ourbranch.com/s/blog/branch_insurance_exchange)
- [Getting started](https://docs.v2.api.ourbranch.com/)
- [Blog](https://www.ourbranch.com/s/blog)
- [Terms of service](https://www.ourbranch.com/s/blog/terms-of-use)
- [Privacy policy](https://www.ourbranch.com/s/blog/privacy-policy)
- [GitHub](https://github.com/OurBranch)

## API Evangelist rating

**Kin Score 24.1** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 67.0 |
| Contract quality | 0.0 |
| Contract governance | 0.0 |
| Operational transparency | 6.6 |
| Developer ergonomics | 47.6 |
| Access clarity | 34.2 |

**Agent readiness 6.4** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | unknown |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 17.5** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/branch-insurance/](https://apis.io/providers/branch-insurance/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Branch: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/branch-insurance/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
