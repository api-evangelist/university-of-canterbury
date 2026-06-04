# University of Canterbury (university-of-canterbury)

University of Canterbury (Te Whare Wananga o Waitaha) is a public research university in Christchurch, New Zealand, ranked #261 in the QS World University Rankings 2025. This repository catalogs the institution's public, machine-accessible developer and API footprint as an APIs.json provider profile. The footprint is centered on scholarly and research infrastructure (institutional repository, research data platform, engineering source control) rather than a unified developer portal.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-canterbury/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-canterbury-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party

## Tags

Education, Higher Education, University, Research, Open Data, Repository, OAI-PMH, New Zealand

## APIs

- **UC Research Repository OAI-PMH** — DSpace 7 OAI-PMH 2.0 metadata harvesting interface (verified live). Docs: https://ir.canterbury.ac.nz/ — Base: https://ir.canterbury.ac.nz/server/oai/request
- **UC Research Repository DSpace REST API** — DSpace 7 REST API (root present, returned 403 to unauthenticated probe). Docs: https://ir.canterbury.ac.nz/ — Base: https://ir.canterbury.ac.nz/server/api
- **Canterbury Figshare (figshare REST and OAI-PMH)** — institutional Figshare research data platform on figshare's public REST and OAI-PMH endpoints. Docs: https://docs.figshare.com/ — Base: https://api.figshare.com/v2
- **UC Engineering GitLab API** — self-hosted GitLab REST API v4 (present, authentication-gated). Docs: https://eng-git.canterbury.ac.nz/ — Base: https://eng-git.canterbury.ac.nz/api/v4

## Plans

- plans/university-of-canterbury-plans-pricing.yml

## Rate Limits

- rate-limits/university-of-canterbury-rate-limits.yml

## FinOps

- finops/university-of-canterbury-finops.yml

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.canterbury.ac.nz/
- GitHub: https://github.com/uccser
- LinkedIn: https://www.linkedin.com/school/university-of-canterbury/
- SourceCode: https://eng-git.canterbury.ac.nz/
- Plans, RateLimits, FinOps, Review pointers (see above)

## Notes

All endpoints were probed during review (2026-06-03). Verified live (HTTP 200): the UC Research Repository OAI-PMH endpoint (valid DSpace 7 Identify response) and figshare's public REST API and OAI-PMH endpoints. The DSpace REST API root (403) and the Engineering GitLab REST API (401) exist but are gated/unauthenticated-blocked. The Canterbury Figshare portal returned a Cloudflare 202 challenge to automated requests; the repository home (403) and LinkedIn (999) block bots but are browser-accessible. The UCCSER GitHub org is a Computer Science Education Research group (31 public repos), not a university-wide API program. No university-wide public developer portal was found. No endpoints were fabricated.

## Maintainers

- Kin Lane — kin@apievangelist.com
