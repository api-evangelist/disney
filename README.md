# Disney API (disney)

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
