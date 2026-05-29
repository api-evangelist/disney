# Disney API (disney)

Community-maintained RESTful and GraphQL API exposing a database of 9,820+ Disney characters and the films, short films, TV shows, video games, and park attractions they appear in. The project (BSD-3-Clause) is developed in the open by Manu Castrillon at https://github.com/ManuCastrillonM/disney-api and documented at https://disneyapi.dev. The REST surface is unauthenticated and read-only. Disney and Disney characters are trademarks of The Walt Disney Company; this project is community fan-content and is not affiliated with or endorsed by Disney.

**URL:** [Visit APIs.json URL](https://disneyapi.dev)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Entertainment, Characters, Disney, Open Source, Fan API, REST, GraphQL

## Timestamps

- **Created:** 2026-05-29
- **Modified:** 2026-05-29

## APIs

### Disney API (REST)

RESTful Disney character API. Four GET endpoints: a service index at the root, a paginated character list at /character, and two by-id endpoints (/character/:id and the plural alias /characters/:id). Supports field-level substring filters on name, films, shortFilms, tvShows, videoGames, parkAttractions, allies, enemies, and alignment.

**Human URL:** [https://disneyapi.dev/docs/](https://disneyapi.dev/docs/)
**Base URL:** `https://api.disneyapi.dev`

#### Tags

- Characters, REST

#### Properties

- [Documentation](https://disneyapi.dev/docs/)
- [APIReference](https://disneyapi.dev/docs/)
- [SourceCode](https://github.com/ManuCastrillonM/disney-api)
- [OpenAPI](openapi/disney-openapi.yml)
- [NaftikoCapability](capabilities/disney-characters.yaml)
- [Authentication — No authentication required (GET-only public API)](https://disneyapi.dev/docs/)

### Disney API (GraphQL)

GraphQL Disney character API hosted at /graphql. Single root field `characters(page, pageSize, filter)` returns a `CharacterPage` with `items` and `paginationInfo`. The `CharacterFilterInput` accepts id, name, films, shortFilms, tvShows, videoGames, alignment, parkAttractions, allies, and enemies as substring filters.

**Human URL:** [https://disneyapi.dev/docs/](https://disneyapi.dev/docs/)
**Base URL:** `https://api.disneyapi.dev/graphql`

#### Tags

- Characters, GraphQL

#### Properties

- [Documentation](https://disneyapi.dev/docs/)
- [SourceCode](https://github.com/ManuCastrillonM/disney-api/blob/main/src/graphql/typeDefs.js)
- [Authentication — No authentication required](https://disneyapi.dev/docs/)

## Common Properties

- [Website](https://disneyapi.dev)
- [Documentation](https://disneyapi.dev/docs/)
- [SourceCode — Disney API (RESTful and GraphQL server)](https://github.com/ManuCastrillonM/disney-api)
- [SourceCode — disneyapi.dev documentation site (Gatsby)](https://github.com/ManuCastrillonM/disneyapi.dev)
- [License — BSD-3-Clause](https://github.com/ManuCastrillonM/disney-api/blob/main/LICENSE)
- [StatusPage](https://status.disneyapi.dev/)
- [SignUp — Support Us (donations to underwrite hosting)](https://disneyapi.dev/support-us/)
- [GitHubRepository — disney-api](https://github.com/ManuCastrillonM/disney-api)
- [GitHubRepository — disneyapi.dev](https://github.com/ManuCastrillonM/disneyapi.dev)
- [SpectralRules](rules/disney-rules.yml)
- [Vocabulary](vocabulary/disney-vocabulary.yml)
- [JSONLD](json-ld/disney-context.jsonld)
- [JSONSchema — Character](json-schema/disney-character-schema.json)
- [JSONSchema — CharacterPage](json-schema/disney-character-page-schema.json)
- [JSONSchema — PageInfo](json-schema/disney-page-info-schema.json)
- [JSONSchema — ServiceIndex](json-schema/disney-service-index-schema.json)
- [JSONStructure — Character](json-structure/disney-character-structure.json)
- [JSONStructure — CharacterPage](json-structure/disney-character-page-structure.json)
- [JSONStructure — PageInfo](json-structure/disney-page-info-structure.json)
- [JSONStructure — ServiceIndex](json-structure/disney-service-index-structure.json)
- [Example — Character Example](examples/disney-character-example.json)
- [Example — CharacterPage Example](examples/disney-character-page-example.json)
- [Example — ServiceIndex Example](examples/disney-service-index-example.json)
- [RateLimits](rate-limits/disney-rate-limits.yml)

## Features

| Name | Description |
|------|-------------|
| 9,820+ Disney Characters | Database of nearly ten thousand Disney character records harvested from the Disney Fandom Wiki. |
| Rich Cross-Reference Fields | Each character lists their films, shortFilms, tvShows, videoGames, parkAttractions, allies, and enemies as named string arrays. |
| Substring Filtering On Every Field | Every character field can be filtered by case-insensitive substring through query parameters, enabling targeted lookups (e.g., all characters in a specific film). |
| Page-Based Pagination | Standard `page` + `pageSize` pagination with previousPage and nextPage URLs returned inline in the `info` envelope. |
| REST And GraphQL | The same backing data is exposed both as a REST API and as a GraphQL endpoint at /graphql. |
| No Authentication | All endpoints are publicly accessible — no API key, OAuth, or signup is required. |
| Open Source (BSD-3-Clause) | Server source is available at github.com/ManuCastrillonM/disney-api and documentation source at github.com/ManuCastrillonM/disneyapi.dev. |
| Service Index At Root | A `GET /` discovery endpoint enumerates the available REST routes as a JSON map. |

## Use Cases

| Name | Description |
|------|-------------|
| Disney Fan Apps And Character Browsers | Powers casual fan apps that let users browse, search, and bookmark Disney characters and their appearances. |
| Trivia And Quiz Games | Provides ground truth for Disney trivia games (which films features which character, who are X's allies, etc.). |
| Bot And Chatbot Integrations | Plain JSON payloads are easily injected into Discord, Slack, and Twitter bots that respond to Disney character lookups. |
| Frontend Tutorial Fixture | Richer than typical Hello-World APIs, useful for teaching pagination, filtering, and image rendering in React/Vue/Svelte tutorials. |
| Data Exploration And Visualization | The cross-reference arrays (films / TV / games / attractions / allies / enemies) make the dataset a natural fit for graph and network-visualization demos. |
| API Profiling And Mocking Demos | A small but realistic public API surface that is commonly used to demonstrate OpenAPI generation, Spectral linting, and Microcks mocking. |

## Integrations

| Name | Description |
|------|-------------|
| Disney Fandom Wiki | Source of truth — character names, films, TV shows, images, and source URLs are harvested from disney.fandom.com. |
| Heroku | Historical hosting platform for the API and MongoDB instance (per upstream README and Procfile). |
| MongoDB | Backing data store; characters are modeled as Mongoose documents with mongoose-sequence numeric ids. |
| GitHub | Source of truth for the BSD-3-Clause licensed implementation, contributors, releases, and Gatsby documentation site. |
| Cloudflare (Disney Parks MCP) | A related (but unaffiliated) Disney Parks MCP server (`cameronsjo/mouse-mcp`) exposes Disney parks attractions and dining data; not the same API as disneyapi.dev but a sibling Disney data source useful for agent workflows. |

## Solutions

| Name | Description |
|------|-------------|
| Public Disney Character Reference | A donation-funded, community-maintained reference dataset for Disney characters that fills the absence of any official Disney developer API. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Disney API OpenAPI](openapi/disney-openapi.yml) — 4 operations (`GET /`, `GET /character`, `GET /character/{id}`, `GET /characters/{id}`) across two tags (Characters, Index), with reusable parameters, named examples, and Microcks dispatcher extensions.

### JSON Schema

- [Character](json-schema/disney-character-schema.json)
- [CharacterPage](json-schema/disney-character-page-schema.json)
- [PageInfo](json-schema/disney-page-info-schema.json)
- [ServiceIndex](json-schema/disney-service-index-schema.json)

### JSON Structure

- [Character](json-structure/disney-character-structure.json)
- [CharacterPage](json-structure/disney-character-page-structure.json)
- [PageInfo](json-structure/disney-page-info-structure.json)
- [ServiceIndex](json-structure/disney-service-index-structure.json)

### JSON-LD

- [disney-context.jsonld](json-ld/disney-context.jsonld) — Maps Character, CharacterPage, PageInfo, and ServiceIndex; aligns `name`, `url`, `image`, `description`, and `identifier` with schema.org and `sourceUrl` with `dcterms:source`.

### Examples

- [Character example](examples/disney-character-example.json)
- [CharacterPage example](examples/disney-character-page-example.json)
- [ServiceIndex example](examples/disney-service-index-example.json)

## Capabilities

Naftiko capabilities exposing the Disney API endpoints over both a Spectral-compliant REST surface and an MCP tool surface.

### Disney API

- [Disney API — Characters](capabilities/disney-characters.yaml) — 4 consumed operations, 4 REST resources, 4 MCP tools.

## Rate Limits

- [Disney API Rate Limits](rate-limits/disney-rate-limits.yml) — Provider does not publish per-key or per-account request-rate numbers; the service is donation-funded. Captures platform-level Heroku caps and best-effort backoff guidance.

## Vocabulary

- [Disney API Vocabulary](vocabulary/disney-vocabulary.yml) — Unified taxonomy mapping 2 resources, 2 actions, 1 workflow, and 4 personas across operational (OpenAPI) and capability (Naftiko) dimensions.

## Rules

- [Disney API Spectral Rules](rules/disney-rules.yml) — 41 rules across 12 categories enforcing Disney API conventions (OpenAPI 3.0.x, HTTPS, canonical host, camelCase operationIds prefixed `get`/`list`, Title Case summaries prefixed with "Disney API", page/pageSize pagination, `{info, data}` envelope, no auth, no request bodies).

## Source

This entry was created as a profile stub on 2026-05-29 and enriched on the same day with a full opensource pipeline pass (OpenAPI, JSON Schema, JSON Structure, JSON-LD, examples, Naftiko capability, Spectral rules, vocabulary, rate limits). The profile targets the community Disney character API at disneyapi.dev because Disney itself does not publish a public developer API; disneyapi.dev is the most documented, still-live community alternative.

- **x-type:** opensource
- **x-tier:** 3 (community fan-API for Disney character data)
- **source:** [ManuCastrillonM/disney-api](https://github.com/ManuCastrillonM/disney-api) — BSD-3-Clause community project

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
