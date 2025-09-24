# Manifest schema (v2) overview

Fields:
- `version` (string): manifest version
- `last_updated` (string): informational
- `pages` (map): title → { file, type, version, description? }
- `packs` (map): id → { description?, version, pages[], depends_on[], tags? }
- `groups` (map, optional): id → { description?, packs[], children? }

See tools repo for full JSON Schema:
- `labki-packs-tools/schema/root-manifest.schema.json`

Examples align with `pages/` layout and Windows-safe filenames.
