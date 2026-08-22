# Disney API (disney)

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

Community-maintained RESTful and GraphQL API exposing a database of 9,820+ Disney characters and the films, short films, TV shows, video games, and park attractions they appear in. The project (BSD-3-Clause) is developed in the open by Manu Castrillon at https://github.com/ManuCastrillonM/disney-api and documented at https://disneyapi.dev. The REST surface is unauthenticated and read-only. Disney and Disney characters are trademarks of The Walt Disney Company; this project is community fan-content and is not affiliated with or endorsed by Disney.

**APIs.json:** [https://disneyapi.dev](https://disneyapi.dev)

## Tags

- Entertainment
- Characters
- Disney
- Open Source
- Fan API
- REST
- GraphQL

## Timestamps

- **Created:** 2026-05-29
- **Modified:** 2026-05-29

## APIs

### Disney API (REST)

RESTful Disney character API. Four GET endpoints: a service index at the root, a paginated character list at /character, and two by-id endpoints (/character/:id and the plural alias /characters/:id). Supports field-level substring filters on name, films, shortFilms, tvShows, videoGames, parkAttractions, allies, enemies, and alignment.

- **Human URL:** [https://disneyapi.dev/docs/](https://disneyapi.dev/docs/)
- **Base URL:** `https://api.disneyapi.dev`

#### Tags

- Characters
- REST

#### Properties

- [Documentation](https://disneyapi.dev/docs/)
- [API Reference](https://disneyapi.dev/docs/)
- [Source Code](https://github.com/ManuCastrillonM/disney-api)
- [OpenAPI](openapi/disney-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/disney.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/disney.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Authentication](https://disneyapi.dev/docs/)

### Disney API (GraphQL)

GraphQL Disney character API hosted at /graphql. Single root field `characters(page, pageSize, filter)` returns a `CharacterPage` with `items` and `paginationInfo`. The `CharacterFilterInput` accepts id, name, films, shortFilms, tvShows, videoGames, alignment, parkAttractions, allies, and enemies as substring filters. Schema is derived directly from the published source.

- **Human URL:** [https://disneyapi.dev/docs/](https://disneyapi.dev/docs/)
- **Base URL:** `https://api.disneyapi.dev/graphql`

#### Tags

- Characters
- GraphQL

#### Properties

- [Documentation](https://disneyapi.dev/docs/)
- [Source Code](https://github.com/ManuCastrillonM/disney-api/blob/main/src/graphql/typeDefs.js)
- [Authentication](https://disneyapi.dev/docs/)
- [Postman Collection](collections/disney.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/disney.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://disneyapi.dev)
- [Documentation](https://disneyapi.dev/docs/)
- [Source Code](https://github.com/ManuCastrillonM/disney-api)
- [Source Code](https://github.com/ManuCastrillonM/disneyapi.dev)
- [License](https://github.com/ManuCastrillonM/disney-api/blob/main/LICENSE)
- [Status Page](https://status.disneyapi.dev/)
- [Sign Up](https://disneyapi.dev/support-us/)
- [GitHub Repository](https://github.com/ManuCastrillonM/disney-api)
- [GitHub Repository](https://github.com/ManuCastrillonM/disneyapi.dev)
- [Spectral Rules](rules/disney-rules.yml)
- [Vocabulary](vocabulary/disney-vocabulary.yml)
- [JSON-LD](json-ld/disney-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/disney-character-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/disney-character-page-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/disney-page-info-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/disney-service-index-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/disney-character-structure.json)
- [JSON Structure](json-structure/disney-character-page-structure.json)
- [JSON Structure](json-structure/disney-page-info-structure.json)
- [JSON Structure](json-structure/disney-service-index-structure.json)
- [Example](examples/disney-character-example.json)
- [Example](examples/disney-character-page-example.json)
- [Example](examples/disney-service-index-example.json)
- [Rate Limits](rate-limits/disney-rate-limits.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
