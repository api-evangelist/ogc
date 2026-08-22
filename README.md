# Open Geospatial Consortium (OGC)

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

A **standards-body** profile in the API Evangelist network — the third class of repo alongside API
producers (`pipeline-enrich`) and investors (`pipeline-vc`). A standard is not a product; it is a
coalition with artifacts, so this repo profiles the **specifications**, the **governance**, the
**maturity ladder**, and above all the **member organizations**.

Profiled 2026-08-20.

## What OGC is

The standards body for geospatial interoperability, founded 1994. It wrote the web-mapping layer the
public sector has run on for two decades — **WMS, WFS, WCS, WMTS, CSW** — and is replacing it with the
**OGC API family**: resource-oriented, OpenAPI-described standards over a common core.

**11 approved** — Features, Common, EDR, Tiles, Processes, Maps, Moving Features, Records, Connected
Systems, DGGS, SensorThings. **7 in draft** — Coverages, Styles, Joins, Routes, GeoDataCubes,
3D GeoVolumes, SOSA.

## The finding worth naming

**OGC publishes its results openly and its process privately.** Every adopted standard is a free
download, the OpenAPI documents are served anonymously from `schemas.opengis.net`, and drafting happens
in public across 361 GitHub repositories. But `portal.ogc.org` — where Technical Committee documents,
votes and delegate rosters live — returned **HTTP 401** to an anonymous probe on 2026-08-20. So the
coalition is measurable and the standards are measurable, but *who holds a committee seat* is not
public, and this repo records that gap rather than guessing at it.

The other thing to keep straight: **these contracts are specifications, not services.** The servers
block is a template. `ogcapi-features-1.yaml` is titled *"Building Blocks specified in OGC API -
Features - Part 1: Core"* and carries **no paths at all** — 5 parameters, 20 schemas, 10 responses. That
is OGC's design, not a defect, and it is why a standards body must never be scored with the provider
Kin Score composite.

## What is here

| Artifact | Contents |
|---|---|
| `apis.yml` | Identity + the 10 approved OGC API specifications OGC publishes as OpenAPI |
| `openapi/_original/` | 24 root OpenAPI documents harvested from `schemas.opengis.net/ogcapi/`, 256 operations |
| `companies/` | **362 member organizations** — level, type, country, own URL; 56 already in the network |
| `leads/` | **306 member organizations with no repo yet**, ranked by OGC membership level |
| `taxonomy/` | The OGC API family with observed maturity + the full 98-standard catalog |
| `working-groups/` | 62 Standards Working Groups + 35 Domain Working Groups |
| `governance/` | Bodies, membership levels, and every surface with its probed status code |
| `people/` | 37 OGC staff — **not** the member delegates, which OGC does not publish |
| `repositories/` `releases/` `contributors/` | 361 repos, 92 releases, 487 contributors |

## Matching note

Unlike most standards rosters — a bare org name typed into a table — **OGC publishes each member's own
URL**, so `in_network` is settled by authoritative domain match rather than name guessing. That found 49
members the name matcher missed (it found 21). Six more were matched by existing repo slug because the
network domain index has no entry for their domain (`all/google` exists while `google.com` is unindexed) —
a gap in the index, recorded per-company in `match_note`.

## Sources

- `https://portal.ogc.org/services/srv_active_members_csv_new.php` — the active member roster CSV, the
  data behind the OGC Member Directory ArcGIS dashboard
- `https://www.ogc.org/wp-json/wp/v2/` — OGC's own CMS API: `standards`, `standards-working-gr`,
  `groups`, `our-team`
- `https://ogcapi.ogc.org/` — the approval badges the maturity ladder is read from
- `https://schemas.opengis.net/ogcapi/` — the specifications
- `https://github.com/opengeospatial` — 361 repositories
