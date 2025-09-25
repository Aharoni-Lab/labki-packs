# Manifest schema (authoritative)

- See the canonical JSON Schema in `labki-packs-tools`:
  - `schema/manifest.schema.json` — [link](https://github.com/Aharoni-Lab/labki-packs-tools/blob/main/schema/manifest.schema.json)
- Validator CLI docs live in the tools repo:
  - `docs/validator.md` — [link](https://github.com/Aharoni-Lab/labki-packs-tools/blob/main/docs/validator.md)
  - `docs/manifest.md` — [link](https://github.com/Aharoni-Lab/labki-packs-tools/blob/main/docs/manifest.md)

Current top-level fields validated by the schema (summary):
- `schema_version` (string, semantic version)
- `$schema` (optional override)
- `last_updated` (UTC timestamp string)
- `pages` (object: title → { file, version, description? })
- `packs` (object: id → { version, description?, pages[], depends_on[], tags? })

Refer to the schema file for full constraints and definitions. Examples in this repo should conform to the schema and to Windows-safe filenames under `pages/`.
