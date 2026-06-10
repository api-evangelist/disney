# Disney API GraphQL API

GraphQL Disney character API hosted at /graphql. Single root field `characters(page, pageSize, filter)` returns a `CharacterPage` with `items` and `paginationInfo`. The `CharacterFilterInput` accepts id, name, films, shortFilms, tvShows, videoGames, alignment, parkAttractions, allies, and enemies as substring filters. Schema is derived directly from the published source.

**Endpoint:** https://api.disneyapi.dev/graphql

**Documentation:** https://disneyapi.dev/docs/

**References:**

- Documentation: https://disneyapi.dev/docs/
- Authentication: https://disneyapi.dev/docs/
