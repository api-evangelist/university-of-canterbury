# University of Canterbury (university-of-canterbury)

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

University of Canterbury (Te Whare Wananga o Waitaha) is a public research university in Christchurch, New Zealand, ranked #261 in the QS World University Rankings 2025. This repository catalogs the institution's public, machine-accessible developer and API footprint as an APIs.json provider profile. The footprint is centered on scholarly and research infrastructure (institutional repository, research data platform, engineering source control) rather than a unified developer portal.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-canterbury/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-canterbury-api-evangelist&utm_content=repo

## Type

- Index
- university / Public Research University
- Consumer
- Internal

## Tags

Education, Higher Education, University, New Zealand, Research, Research Repository, Open Access, OAI-PMH, Identity Federation, SAML, Learning Management

## APIs

Every entry carries an operator. `institution` means the University of Canterbury runs the thing the
entry describes. `tenant` means the institution's data and identity on someone else's platform — the
relationship is real, the contract is not theirs.

- **UC Research Repository OAI-PMH** (`institution`) — self-hosted DSpace 7 OAI-PMH 2.0 harvesting interface; verified live 2026-08-30 (HTTP 200, valid Identify, thirteen metadata formats). Base: https://ir.canterbury.ac.nz/server/oai/request
- **UC Research Repository DSpace REST API** (`institution`) — live but behind a Cloudflare bot challenge (HTTP 403). Base: https://ir.canterbury.ac.nz/server/api
- **UC API Gateway** (`institution`) — CA API Gateway 9.0 on the institution's own domain; every probed path returns HTTP 500 "Policy Falsified / Service Not Found". No public service routed, no catalogue published. Base: https://api.canterbury.ac.nz/
- **UC Shibboleth SAML 2.0 Service Provider Metadata** (`institution`) — three SPs on canterbury.ac.nz hosts publish valid SAML 2.0 metadata (HTTP 200): learn, assessment, eportfolio. Base: https://learn.canterbury.ac.nz/Shibboleth.sso/Metadata
- **LEARN LTI 1.3 Platform (Moodle)** (`institution`) — live LTI 1.3 JWKS on the institution's host (HTTP 200); Moodle web services disabled. Base: https://learn.canterbury.ac.nz/mod/lti/certs.php
- **UC Engineering GitLab API** (`institution`) — self-hosted GitLab REST API v4, authentication-gated (HTTP 401). Base: https://eng-git.canterbury.ac.nz/api/v4
- **Tuakiri Hosted Identity Provider for canterbury.ac.nz** (`tenant`) — the institution's IdP entityID is under canterbury.ac.nz, but every SSO/SLO endpoint is hosted by REANNZ at hosted-login.tuakiri.ac.nz. Base: https://hosted-login.tuakiri.ac.nz/hosting/canterbury.ac.nz/idp/profile/SAML2/Redirect/SSO
- **Canterbury Figshare Research Data Repository** (`tenant`) — the institution's research data repository on Figshare's platform; the API contract is Figshare's, served from the shared vendor host. Base: https://api.figshare.com/v2

## Conformance

- conformance/university-of-canterbury-conformance.yml — `education` regime domain standards: **oai-pmh**, **saml**, **shibboleth**, **lti** evidenced live; scim, oneroster, ed-fi, caliper, qti, orcid, datacite and crossref recorded as not found.

## Plans

- plans/university-of-canterbury-plans-pricing.yml

## Rate Limits

- rate-limits/university-of-canterbury-rate-limits.yml

## FinOps

- finops/university-of-canterbury-finops.yml

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-30

## Common Properties

- Website: https://www.canterbury.ac.nz/
- GitHubOrganization: https://github.com/uccser
- LinkedIn: https://www.linkedin.com/school/university-of-canterbury/
- SourceCode: https://eng-git.canterbury.ac.nz/
- PrivacyPolicy: https://www.canterbury.ac.nz/about-uc/corporate-information/policies/privacy-policy
- CourseCatalog: https://www.canterbury.ac.nz/study/academic-study/courses
- LibraryCatalog: https://www.canterbury.ac.nz/library
- ResearchRepository: https://ir.canterbury.ac.nz/
- IdentityFederation: https://directory.tuakiri.ac.nz/metadata/tuakiri-metadata-signed.xml
- Conformance, DomainSecurity, Plans, RateLimits, FinOps, Review pointers (see above)

## Notes

**Corrected 2026-08-30.** This profile was first built on 2026-06-03, before the enrichment pipeline
had an ownership check. Eleven of its fourteen API entries — `altmetric`, `articles`, `authors`,
`collections`, `institutions`, `oauth`, `other`, `profiles`, `projects`, `symplectic` and the
Figshare tenancy itself — were a **single Figshare API v2 OpenAPI**, split per tag by our own
refine step and attributed to this institution. Every one of those specs declared
`info.title: Figshare …`, `info.contact: Figshare Support` and `servers: https://api.figshare.com/v2`
— a generic vendor host every Figshare customer calls — while our `apis.yml` had re-based them onto
`ir.canterbury.ac.nz`, which is a different system entirely. That contract and the 47 files derived
from it (JSON Schema, JSON Structure, examples, rules, vocabulary, JSON-LD, scopes, authentication,
agentic-access, capability edges and twenty collections) have been removed. The tenancy remains,
recorded as a relationship.

All endpoints were re-probed 2026-08-30 with a browser User-Agent. Verified live and readable
(HTTP 200): the OAI-PMH interface, three Shibboleth SP metadata endpoints, and the LEARN LTI 1.3
JWKS. Live but closed: the API gateway (500, no service routed), the Engineering GitLab API (401),
the DSpace REST API (403, Cloudflare bot challenge). A 403 or a 202 challenge is a finding about
bot management, not evidence the host is dead. No `llms.txt` and no `.well-known/security.txt` are
published; `data.canterbury.ac.nz` and `developer.canterbury.ac.nz` do not resolve. No AI or
responsible-AI policy was found in the UC Policy Library. The UCCSER GitHub org is a Computer
Science Education Research group, not a university-wide API programme. No university-wide public
developer portal exists. No endpoints were fabricated.

## Maintainers

- Kin Lane — kin@apievangelist.com
