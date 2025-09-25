# Overview (content repository)

`labki-packs` stores versioned MediaWiki content packs and a root `manifest.yml` that defines:
- `pages`: canonical titles mapped to files under `pages/`
- `packs`: flat registry of packs (version, pages, depends_on)

Goals:
- Provide curated packs our group maintains
- Serve as an example for others to model their own content repos
- Validate on every PR using `labki-packs-tools`
