# Open Geospatial Consortium (OGC)

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
