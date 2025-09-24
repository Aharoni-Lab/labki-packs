# Repository structure (content repo)

```text
labki-packs/
├─ manifest.yml          # Root registry (real content)
├─ README.md             # Minimal; how to use these packs
├─ pages/                # All page files (.wiki/.md), optionally grouped by type
│  ├─ Templates/
│  ├─ Forms/
│  ├─ Categories/
│  ├─ Properties/
│  ├─ Layouts/
│  └─ Modules/
└─ .github/workflows/validate.yml  # CI calling labki-packs-tools
```

Notes:
- Filenames must be Windows-safe (no `:`). Use `Template_Foo.wiki`, etc.
- Titles are the keys in `manifest.yml` under `pages:`.
- Track per-page version (`pages.*.version`) and per-pack version (`packs.*.version`).
