# Overview (content repository)

`labki-packs` stores versioned MediaWiki content packs and a root `manifest.yml` with:
- `pages`: canonical titles mapped to files under `pages/`
- `packs`: registry of packs (version, pages, depends_on)

Goals:
- Provide curated packs our group maintains
- Serve as an example for others to model their own content repos
- Validate on every PR using `labki-packs-tools`

Authoritative docs for schema and validator live in `labki-packs-tools`:
- Schema: [`schema/manifest.schema.json`](https://github.com/Aharoni-Lab/labki-packs-tools/blob/main/schema/manifest.schema.json)
- Validator CLI: [`docs/validator.md`](https://github.com/Aharoni-Lab/labki-packs-tools/blob/main/docs/validator.md)
- CI integration: [`docs/ci.md`](https://github.com/Aharoni-Lab/labki-packs-tools/blob/main/docs/ci.md)
