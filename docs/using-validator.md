# Using the validator (labki-packs-tools)

Authoritative docs live in `labki-packs-tools`:
- Validator CLI: [docs/validator.md](https://github.com/Aharoni-Lab/labki-packs-tools/blob/main/docs/validator.md)
- CI integration: [docs/ci.md](https://github.com/Aharoni-Lab/labki-packs-tools/blob/main/docs/ci.md)

## CI (GitHub Actions)

```yaml
name: Validate content packs
on:
  pull_request:
  push:
    branches: [ main ]

jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/checkout@v4
        with:
          repository: Aharoni-Lab/labki-packs-tools
          path: tools-cache
      - uses: actions/setup-python@v5
        with:
          python-version: '3.11'
      - name: Install deps
        run: pip install pyyaml jsonschema
      - name: Validate manifest
        run: |
          # auto schema selection
          python tools-cache/tools/validate_repo.py validate manifest.yml
```

## Local

```bash
pip install pyyaml jsonschema
# auto schema selection
python tools-cache/tools/validate_repo.py validate manifest.yml
```

For advanced options and schema details, use the links above.
