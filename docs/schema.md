# Manifest schema (v1) overview

Fields:
- `version` (string): manifest version
- `last_updated` (string): informational
- `pages` (map): title → { file, version, description? }
- `packs` (map): id → { description?, version, pages[], depends_on[], tags? }

See tools repo for full JSON Schema:
- `labki-packs-tools/schema/manifest.schema.json`

Examples align with `pages/` layout and Windows-safe filenames.
